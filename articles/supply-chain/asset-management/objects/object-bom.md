---
title: BOM الأصل
description: يصف هذا الموضوع قوائم مكونات الصنف (BOM) للأصل في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 761364c8c58258baf2268f917cb174ac300c4528
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783052"
---
# <a name="asset-boms"></a><span data-ttu-id="88697-103">BOM الأصل</span><span class="sxs-lookup"><span data-stu-id="88697-103">Asset BOMs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="88697-104">يصف هذا الموضوع قوائم مكونات الصنف (BOM) للأصل في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="88697-104">This topic describes asset bills of materials (BOMs) in Asset Management.</span></span> <span data-ttu-id="88697-105">تعرض صفحة **BOM الأصل** قائمة بجميع الأصناف (قطع الغيار والأصناف الأخرى) التي يتم استخدامها على أحد الأصول خلال عمره الكامل.</span><span class="sxs-lookup"><span data-stu-id="88697-105">The **Asset BOM** page shows a list of all items (spare parts and other items) that are used on an asset during its whole lifetime.</span></span> <span data-ttu-id="88697-106">عند إنشاء أصل جديد، يجب عليك إعداد BOM الأصل كجزء من إجراء الإعداد.</span><span class="sxs-lookup"><span data-stu-id="88697-106">When you create a new asset, you should consider setting up an asset BOM as a part of the setup procedure.</span></span> <span data-ttu-id="88697-107">وبهذه الطريقة، يمكنك تعقب محفوظات الأصناف التابعة للأصل من تاريخ الإنشاء.</span><span class="sxs-lookup"><span data-stu-id="88697-107">In this way, you can track item history for the asset from the creation date.</span></span>

<span data-ttu-id="88697-108">بعد الانتهاء من مهمة صيانة، وتسجيل استهلاك الصنف في أمر عمل، يمكنك تعقب استهلاك قطع الغيار والأصناف الأخرى المستخدمة في الأصل.</span><span class="sxs-lookup"><span data-stu-id="88697-108">After you've completed a maintenance job, and item consumption has been registered on a work order, you can track consumption of spare parts and other items that are used on the asset.</span></span> <span data-ttu-id="88697-109">تتيح لك هذه الوظيفة الاحتفاظ بسجل استهلاك كامل للأصناف لجميع الأصول.</span><span class="sxs-lookup"><span data-stu-id="88697-109">This functionality lets you keep a complete item consumption record for all your assets.</span></span> <span data-ttu-id="88697-110">على سبيل المثال، يمكنك استخدام السجل لمراقبة ما إذا كان يتم استبدال قطعة غيار معينة بشكل متكرر، أو لتعقب قطع الغيار أو الأصناف الأخرى المستخدمة حاليًا على الأصل.</span><span class="sxs-lookup"><span data-stu-id="88697-110">For example, you can use the record to monitor whether a specific spare part is often replaced, or to keep track of the spare parts or other items that are currently used on an asset.</span></span>

> [!NOTE]
> <span data-ttu-id="88697-111">في أمر العمل، قد يشمل استهلاك الصنف قطع الغيار وغيرها من الأصناف الإضافية، مثل مواد التشحيم والبراغي والحشايا.</span><span class="sxs-lookup"><span data-stu-id="88697-111">On a work order, item consumption might include both spare parts and other, additional items, such as lubricants, bolts, and gaskets.</span></span>

<span data-ttu-id="88697-112">يمكن تحديث BOM الأصل تلقائيًا استنادًا إلى الإعداد في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="88697-112">An asset BOM can be automatically updated based on the setup in Asset Management.</span></span> <span data-ttu-id="88697-113">إذا تم إنشاء حالة دورة حياة أمر عمل لمعالجة أوامر عمل منجزة أو مكتملة، وإذا تم تعيين الخيار **تحديث BOM‏‎ الأصل** لحالة دورة حياة أمر العمل هذا إلى **نعم** في صفحة **حالات دورة حياة أمر العمل**، فسيتم تحديث جميع الأصناف المستخدمة على أمر العمل بشكل تلقائي في صفحة **BOM‏‎ الأصل** عند تحديث أمر العمل إلى حالة دورة الحياة هذه.</span><span class="sxs-lookup"><span data-stu-id="88697-113">If a work order lifecycle state has been created to handle finished or completed work orders, and if the **Update asset BOM** option for that work order lifecycle state is set to **Yes** on the **Work order lifecycle states** page, all items that are used on the work order will be automatically updated on the **Asset BOM** page when the work order is updated to that lifecycle state.</span></span> 


<span data-ttu-id="88697-114">يمكنك أيضًا تحديث BOM‎ الأصل يدويًا عن طريق إنشاء بنود أصناف جديدة في صفحة **BOM‎ الأصل**.</span><span class="sxs-lookup"><span data-stu-id="88697-114">You can also manually update an asset BOM by creating new item lines on the **Asset BOM** page.</span></span>

<span data-ttu-id="88697-115">في صفحة **BOM‎ الأصل**، يمكنك تعقب محفوظات قطع الغيار للأصول بعد تسجيل استهلاك الأصناف في أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="88697-115">On the **Asset BOM** page, you can track spare parts history for assets after item consumption is registered on a work order.</span></span> <span data-ttu-id="88697-116">لاستخدام هذه الوظيفة، يجب تحديد مجموعات الأصناف التي يجب استخدامها لتسجيل قطع الغيار في صفحة **مجموعات أصناف قطع الغيار**.</span><span class="sxs-lookup"><span data-stu-id="88697-116">To use this functionality, you must select the item groups that should be used for spare parts registration on the **Spare parts item groups** page.</span></span>

<span data-ttu-id="88697-117">لاستخدام وظيفة BOM الأصل، يجب أولاً إعداد مجموعات أصناف قطع الغيار المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="88697-117">To use asset BOM functionality, you must first set up the required spare parts items groups.</span></span> <span data-ttu-id="88697-118">ثم، إذا كنت تريد تحديث BOM الأصل تلقائيًا عند اكتمال أمر عمل، يمكنك إعداد حالة دورة حياة أمر العمل لمعالجة هذا التحديث.</span><span class="sxs-lookup"><span data-stu-id="88697-118">Then, if you want the asset BOM to be automatically updated when a work order is completed, you can set up a work order lifecycle state to handle that update.</span></span> 


## <a name="set-up-spare-parts-item-groups"></a><span data-ttu-id="88697-119">إعداد مجموعات أصناف قطع الغيار</span><span class="sxs-lookup"><span data-stu-id="88697-119">Set up spare parts item groups</span></span>

<span data-ttu-id="88697-120">يستند إعداد محفوظات قطع الغيار إلى مجموعات الأصناف التي يتم إنشاؤها في الوحدة النمطية **إدارة المخزون والمستودعات‬**.</span><span class="sxs-lookup"><span data-stu-id="88697-120">The setup of spare parts history is based on item groups that are created in the **Inventory and warehouse management** module.</span></span> <span data-ttu-id="88697-121">في إدارة الأصول، يمكنك إعداد مجموعات الأصناف بحيث يمكنك تعقب محفوظات قطع الغيار للأصناف في مجموعات الأصناف المحددة.</span><span class="sxs-lookup"><span data-stu-id="88697-121">In Asset Management, you set up item groups so that you can track spare parts history for the items in the selected item groups.</span></span>

1. <span data-ttu-id="88697-122">حدد **إدارة الأصول** \> **الإعداد** \> **الأصل** \> **مجموعات أصناف قطع الغيار‬**.</span><span class="sxs-lookup"><span data-stu-id="88697-122">Select **Asset management** \> **Setup** \> **Asset** \> **Spare parts item groups**.</span></span>
2. <span data-ttu-id="88697-123">حدد **جديد** لإعداد مجموعة أصناف.</span><span class="sxs-lookup"><span data-stu-id="88697-123">Select **New** to set up an item group.</span></span>
3. <span data-ttu-id="88697-124">في حقل **مجموعة الأصناف**، حدد المجموعة.</span><span class="sxs-lookup"><span data-stu-id="88697-124">In the **Item group** field, select the group.</span></span> <span data-ttu-id="88697-125">يتم إدخال اسم المجموعة تلقائيًا في حقل **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="88697-125">The name of the group is automatically entered in the **Name** field.</span></span>

## <a name="view-and-update-asset-boms"></a><span data-ttu-id="88697-126">عرض وتحديث BOM الأصل</span><span class="sxs-lookup"><span data-stu-id="88697-126">View and update asset BOMs</span></span>

<span data-ttu-id="88697-127">بعد ترحيل استهلاك الصنف في أمر عمل، يمكنك عرض استهلاك الأصناف المسجلة في صفحة **BOM الأصل**.</span><span class="sxs-lookup"><span data-stu-id="88697-127">After you post item consumption on a work order, you can view the registered item consumption on the **Asset BOM** page.</span></span>

1. <span data-ttu-id="88697-128">حدد **إدارة الأصول** \> **عام** \> **الأصول** \> **الأصول‏‎ النشطة**.</span><span class="sxs-lookup"><span data-stu-id="88697-128">Select **Asset management** \> **Common** \> **Assets** \> **Active assets**.</span></span> <span data-ttu-id="88697-129">حدد الأصل في القائمة، ثم حدد‏‎ **BOM الأصل**.</span><span class="sxs-lookup"><span data-stu-id="88697-129">Select the asset in the list, and then select **Asset BOM**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="88697-130">لعرض جميع تسجيلات استهلاك الأصناف على جميع الأصول، حدد **إدارة الأصول** \> **الاستفسارات** \> **الأصول** \> **BOM‏‎ الأصل**.</span><span class="sxs-lookup"><span data-stu-id="88697-130">To view all item consumption registrations on all assets, select **Asset management** \> **Inquiries** \> **Assets** \> **Asset BOM**.</span></span>

2. <span data-ttu-id="88697-131">حدد **تحديث BOM الأصل**.</span><span class="sxs-lookup"><span data-stu-id="88697-131">Select **Update asset BOM**.</span></span> <span data-ttu-id="88697-132">يمكنك إضافة الأصول وأنواع الأصول والموارد إلى التحديث كما هو مطلوب من خلال تحديد **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="88697-132">You can add assets, asset types, and resources to the update as you require by selecting **Select**.</span></span> <span data-ttu-id="88697-133">حدد **موافق** لبدء التحديث.</span><span class="sxs-lookup"><span data-stu-id="88697-133">Select **OK** to start the update.</span></span> <span data-ttu-id="88697-134">يمكنك أيضًا اعداد وظيفة التحديث كوظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="88697-134">You can also set up the Update function as a batch job.</span></span>
3. <span data-ttu-id="88697-135">إذا كنت ترغب في عرض مزيد من المعلومات المرتبطة بالأصناف، فيمكنك إضافة أبعاد المخزون.</span><span class="sxs-lookup"><span data-stu-id="88697-135">If you want to see more information that is related to the items, you can add inventory dimensions.</span></span> <span data-ttu-id="88697-136">حدد **المخزون** \> **عرض الأبعاد‬**، ثم حدد خانات الاختيار للمتغيرات التي تريد استخدامها.</span><span class="sxs-lookup"><span data-stu-id="88697-136">Select **Inventory** \> **Dimensions display**, and then select the check boxes for the dimensions that you want to see.</span></span> <span data-ttu-id="88697-137">للاحتفاظ بهذا الاعداد لجميع الأصول في صفحة **BOM الأصل**، عيّن الخيار **حفظ الإعداد** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="88697-137">To keep this setup for all assets on the **Asset BOM** page, set the **Save setup** option to **Yes**.</span></span>
4. <span data-ttu-id="88697-138">للحصول علي نظرة عامة حول المكان في إدارة الأصول حيث يتم استخدام الصنف على البند المحدد، بالنسبة إلى الأصول والإعدادات الافتراضية لنوع الوظيفة وقطع الغيار وأوامر العمل، حدد **مكان استخدام الصنف**.</span><span class="sxs-lookup"><span data-stu-id="88697-138">To get an overview of where in Asset Management the item on the selected line is used, in relation to assets, job type defaults, spare parts, and work orders, select **Item where used**.</span></span> 
5. <span data-ttu-id="88697-139">إذا أردت رؤية بنود الصنف النشطة فقط، فحدد **عرض** \> **الحالي**.</span><span class="sxs-lookup"><span data-stu-id="88697-139">If you want to see only active item lines, select **View** \> **Current**.</span></span> <span data-ttu-id="88697-140">لعرض كافة بنود الأصناف، بما في ذلك البنود التي لديها تاريخ انتهاء صلاحية أبكر من التاريخ الحالي، حدد **عرض** \> **الكل**.</span><span class="sxs-lookup"><span data-stu-id="88697-140">To see all item lines, including lines where the expiration date is earlier than the current date, select **View** \> **All**.</span></span>

> [!NOTE]
> <span data-ttu-id="88697-141">عندما تكمل أمر عمل، إذا انتهت صلاحيه بعض الأصناف أو قطع الغيار المرتبطة بالأصل ذي الصلة أو تم استبدالها بأصناف أو قطع غيار أخرى، فنحن ننصحك بتحديث BOM الأصل وفقًا لذلك.</span><span class="sxs-lookup"><span data-stu-id="88697-141">When you've completed a work order, if some items or spare parts that are related to the related asset have expired or have been replaced by other items or spare parts, we recommend that you update the asset BOM accordingly.</span></span>

## <a name="create-a-new-item-line-in-an-asset-bom"></a><span data-ttu-id="88697-142">إنشاء بند صنف جديد في BOM الأصل</span><span class="sxs-lookup"><span data-stu-id="88697-142">Create a new item line in an asset BOM</span></span>

<span data-ttu-id="88697-143">يمكنك إنشاء بنود الأصناف الخاصة بالأصول يدويًا.</span><span class="sxs-lookup"><span data-stu-id="88697-143">You can manually create item lines for assets.</span></span>

1. <span data-ttu-id="88697-144">في صفحة **BOM‎ الأصل‬**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="88697-144">On the **Asset BOM** page, select **New**.</span></span>
2. <span data-ttu-id="88697-145">في حقل **الأصل**، حدد الأصل المراد إضافة بند صنف له.</span><span class="sxs-lookup"><span data-stu-id="88697-145">In the **Asset** field, select the asset to add an item line for.</span></span>
3. <span data-ttu-id="88697-146">في الحقل **رقم البند**، أدخل رقم بند تسلسلي.</span><span class="sxs-lookup"><span data-stu-id="88697-146">In the **Line number** field, enter a sequential line number.</span></span>
4. <span data-ttu-id="88697-147">في الحقل **سارٍ‏‎** حدد تاريخ بدء الصنف.</span><span class="sxs-lookup"><span data-stu-id="88697-147">In the **Effective** field, enter a start date for the item.</span></span>
5. <span data-ttu-id="88697-148">إذا كان لدى الصنف تاريخ انتهاء صلاحية، فأدخل تاريخ الانتهاء في حقل **انتهاء الصلاحية**.</span><span class="sxs-lookup"><span data-stu-id="88697-148">If the item will expire, in the **Expiration** field, enter an end date.</span></span>
6. <span data-ttu-id="88697-149">في الحقل **رقم الصنف**، حدد الصنف.</span><span class="sxs-lookup"><span data-stu-id="88697-149">In the **Item number** field, select the item.</span></span> <span data-ttu-id="88697-150">يتم إدخال الاسم تلقائيًا في حقل **اسم المنتج**.</span><span class="sxs-lookup"><span data-stu-id="88697-150">The name is automatically entered in the **Product name** field.</span></span>
7. <span data-ttu-id="88697-151">في حقل **الكمية**، أدخل الكمية المستخدمة.</span><span class="sxs-lookup"><span data-stu-id="88697-151">In the **Quantity** field, enter the quantity that is used.</span></span> <span data-ttu-id="88697-152">يتم تحديث حقل **الوحدة** تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="88697-152">The **Unit** field is automatically updated.</span></span>
