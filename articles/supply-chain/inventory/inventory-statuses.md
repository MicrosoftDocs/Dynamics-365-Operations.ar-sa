---
title: "حالات المخزون"
description: "توضح هذه المقالة كيفية استخدام حالات المخزون لتصنيف المخزون وتعقبه."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 15ee75e11bfce55886052cc57729f5127f22d7da
ms.contentlocale: ar-sa
ms.lasthandoff: 01/17/2018

---

# <a name="inventory-statuses"></a><span data-ttu-id="2410d-103">حالات المخزون</span><span class="sxs-lookup"><span data-stu-id="2410d-103">Inventory statuses</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2410d-104">توضح هذه المقالة كيفية استخدام حالات المخزون لتصنيف المخزون وتعقبه.</span><span class="sxs-lookup"><span data-stu-id="2410d-104">This article describes how you can use inventory statuses to categorize and keep track of inventory.</span></span>

<span data-ttu-id="2410d-105">يمكنك استخدام حالات المخزون لتصنيف المخزون.</span><span class="sxs-lookup"><span data-stu-id="2410d-105">You can use inventory statuses to categorize inventory.</span></span> <span data-ttu-id="2410d-106">ويمكنك فيما بعد بدء الإجراءات المناسبة، مثل عمل الإبعاد أو التزويد.</span><span class="sxs-lookup"><span data-stu-id="2410d-106">You can then initiate appropriate actions, such as replenishment or put-away work.</span></span>

<span data-ttu-id="2410d-107">وفيما يلي بعض الأمثلة على طرق استخدام حالات المخزون:</span><span class="sxs-lookup"><span data-stu-id="2410d-107">Here are some examples of ways that you can use inventory statuses:</span></span>

-   <span data-ttu-id="2410d-108">إنشاء حالات المخزون المتوافر والحركات الصادرة والحركات الواردة.</span><span class="sxs-lookup"><span data-stu-id="2410d-108">Create inventory statuses for on-hand inventory, inbound transactions, and outbound transactions.</span></span>
-   <span data-ttu-id="2410d-109">تحديد حالة مخزون افتراضي لحركات المستودع.</span><span class="sxs-lookup"><span data-stu-id="2410d-109">Specify a default inventory status for warehouse transactions.</span></span>
-   <span data-ttu-id="2410d-110">قم بتغيير حالة مخزون للأصناف قبل وصولها، أو أثناء الوصول، أو عندما يتم تخزين الأصناف خلال حركة المخزون.</span><span class="sxs-lookup"><span data-stu-id="2410d-110">Change an inventory status for items before arrival, during arrival, or when the items are put away during inventory movement.</span></span>
-   <span data-ttu-id="2410d-111">استخدام حالة مخزون لأصناف الأسعار عند إرجاعها ولتخطيط تغطية الصنف أثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="2410d-111">Use an inventory status to price items that are returned and to plan item coverage during master planning.</span></span>

<span data-ttu-id="2410d-112">حالة مخزون هي أحد الأبعاد في مجموعة أبعاد التخزين.</span><span class="sxs-lookup"><span data-stu-id="2410d-112">An inventory status is one of the dimensions in the storage dimension group.</span></span> <span data-ttu-id="2410d-113">يمكن تصنيف حالات المخزون على أنها متوفرة أو غير متوفرة، ويمكنك استخدام معلمة **حظر المخزون** لحظر الأصناف التي تكون بحالة مخزون غير متوفر.</span><span class="sxs-lookup"><span data-stu-id="2410d-113">Inventory statuses can be categorized as available or unavailable, and you can use the **Inventory blocking** parameter to block items that have an unavailable inventory status.</span></span> <span data-ttu-id="2410d-114">وتعتبر الأصناف ذات حالة محظورة هي المخزون الفعلي ولا يمكن استخدامها في أمر الإنتاج أو أمر التوريد، أمر التحويل أو الحركة الصادرة.</span><span class="sxs-lookup"><span data-stu-id="2410d-114">Items that have a blocked status are considered physical inventory, and they can't be used on a production order, sales order, transfer order, or outbound transaction.</span></span>

<span data-ttu-id="2410d-115">يمكنك استخدام أصناف المستودع بحالات المخزون متوفرة أو غير متوفرة للعمل الوارد.</span><span class="sxs-lookup"><span data-stu-id="2410d-115">You can use warehouse items that have either available or unavailable inventory statuses for inbound work.</span></span> <span data-ttu-id="2410d-116">على سبيل المثال، يمكنك إنشاء حالة متاحة باسم **جاهزة**، وتتم تسمية الحالة غير المتاحة باسم **تالفة**، وتُسمى حالة محظورة باسم **محظورة**.</span><span class="sxs-lookup"><span data-stu-id="2410d-116">For example, you create an available status that is named **Ready**, an unavailable status that is named **Damaged**, and a blocked status that is named **Blocked**.</span></span> <span data-ttu-id="2410d-117">وعند إنشاء أمر شراء للأصناف المستلمة أو المرتجعة، إذا كانت أي أصناف تالفة أو مقطوعة، فيمكنك تغيير حالة المخزون لتلك الأصناف إلى **تالفة** في بند أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="2410d-117">When you create a purchase order for received or returned items, if any items are damaged or broken, you can change the inventory status of those items to **Damaged** on the purchase order line.</span></span> <span data-ttu-id="2410d-118">وبعد تلقي هذه الأصناف، يتم تعيين الحالة تلقائياً إلى **محظورة**.</span><span class="sxs-lookup"><span data-stu-id="2410d-118">After these items are received, the status is automatically set to **Blocked**.</span></span> <span data-ttu-id="2410d-119">إذا أجريت عملية مسح للأصناف التالفة باستخدام جهاز محمول، فباستطاعة تطبيق Microsoft Dynamics 365 for Finance and Operations استخدام توجيهات الموقع وقوالب العمل لإظهار معلومات حول الموقع المناسب أو مجموعة من المواقع حيث يمكنك التخلص من تلك الأصناف.</span><span class="sxs-lookup"><span data-stu-id="2410d-119">If you scan the damaged items by using a mobile device, Microsoft Dynamics 365 for Finance and Operations can use location directives and work templates to show information about an appropriate location or range of locations where you can put away those items.</span></span> <span data-ttu-id="2410d-120">وبالنسبة للاصناف المرتجعة، يتم إنشاء نوع الإصدار **حجز** في صفحة **حركات المخزون**.</span><span class="sxs-lookup"><span data-stu-id="2410d-120">For returned items, an issue type of **Reservation** is created on the **Inventory transactions** page.</span></span>

<span data-ttu-id="2410d-121">وبالنسبة للعمل الصادر، استخدم أصنافًا بحالة مخزون متوفر.</span><span class="sxs-lookup"><span data-stu-id="2410d-121">For outbound work, use items that have an available inventory status.</span></span> <span data-ttu-id="2410d-122">إذا كان لديك أصناف ذات حالة **معطلة**, ويعمل التخطيط الرئيسي على هذه الأصناف، تعتبر الأصناف مفقودة ويتم تزويد المخزون تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="2410d-122">If you have items that have a status of **Broken**, and master planning is run on these items, the items are considered missing, and inventory is automatically replenished.</span></span>

<span data-ttu-id="2410d-123">وبعد إعداد حالات المخزون، يمكنك تعيين حالة المخزون الافتراضية للموقع والصنف والمستودع.</span><span class="sxs-lookup"><span data-stu-id="2410d-123">After you set up inventory statuses, you can set the default inventory status for a site, item, and warehouse.</span></span> <span data-ttu-id="2410d-124">كما يمكنك تعيين حالة افتراضية لأوامر المبيعات والتحويل والشراء.</span><span class="sxs-lookup"><span data-stu-id="2410d-124">You can also set a default status for sales, transfer, and purchase orders.</span></span> <span data-ttu-id="2410d-125">ولا يمكن أن تكون الحالة الافتراضية لأوامر المبيعات وأمر التحويل الصادر في خيار **حظر المخزون** قم تعيينها إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="2410d-125">The default status for sales orders and outbound transfer order can't have the **Inventory blocking** option set to **Yes**.</span></span> <span data-ttu-id="2410d-126">وحالة المخزون تكون موروثة من الإعدادات الافتراضية في موقع أو مستودع أو صنف أو أمر شراء أو أمر تحويل أو أمر مبيعات ويمكن تغييرها باستخدام الجهاز المحمول أو في بند أمر التحويل أو أمر الشراء أو أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="2410d-126">The inventory status that is inherited from the default settings on a site, warehouse, item, purchase order, transfer order or sales order can be changed by using the mobile device, or on the purchase order, sales order, or transfer order line.</span></span>

<span data-ttu-id="2410d-127">ولتخطيط تغطية الأصناف التي تكون بحالة مخزون متوفر، حدد خيار **خطة التغطية حسب البعد** لبُعد تخزين في صفحة **مجموعات أبعاد التخزين**.</span><span class="sxs-lookup"><span data-stu-id="2410d-127">To plan coverage for items that have an available inventory status, select the **Coverage plan by dimension** option for a storage dimension on the **Storage dimension groups** page.</span></span> <span data-ttu-id="2410d-128">وعند فتح معالج **تغطية الصنف**، تظهر الأصناف التي تكون بحالة متاحة في صفحة **الحالة**.</span><span class="sxs-lookup"><span data-stu-id="2410d-128">When you open the **Item Coverage** wizard, items that have an available status appear on the **Status** page.</span></span> <span data-ttu-id="2410d-129">لإنشاء إعدادات تغطية لهذه الأصناف، حدد معرف حالة المخزون لحالات المخزون المتاحة.</span><span class="sxs-lookup"><span data-stu-id="2410d-129">To create coverage settings for these items, select the inventory status ID for the available inventory statuses.</span></span> <span data-ttu-id="2410d-130">استناداً إلى إعدادات التغطية، يمكنك حساب متطلبات الصنف والتنبؤ بالعرض والطلب والأصناف المتوفرة أثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="2410d-130">Based on the coverage settings, you can calculate the item requirements and forecast the supply and demand of available items during master planning.</span></span> <span data-ttu-id="2410d-131">لا يمكنك إنشاء إعداد تغطية صنف بحالة مخزون محظور.</span><span class="sxs-lookup"><span data-stu-id="2410d-131">You can't create an item coverage setup that has a blocked inventory status.</span></span> <span data-ttu-id="2410d-132">وبدلاً من ذلك، استخدم صفحة **تغطية الصنف** لإنشاء أو تعديل معلمات تغطية الصنف.</span><span class="sxs-lookup"><span data-stu-id="2410d-132">Alternatively, use the **Item coverage** page to create or modify the item coverage parameters.</span></span>

