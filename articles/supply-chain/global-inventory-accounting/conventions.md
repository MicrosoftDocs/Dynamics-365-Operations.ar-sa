---
title: الاصطلاحات
description: يصف هذا الموضوع كيفية إعداد القواعد لتحديد كيفية حساب التكاليف في محاسبة المخزون العالمي.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 74d99d3eefdcaaa7f6551668990b702396b32ffc
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273108"
---
# <a name="conventions"></a><span data-ttu-id="51780-103">الاصطلاحات</span><span class="sxs-lookup"><span data-stu-id="51780-103">Conventions</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="51780-104">القاعدة عبارة عن حاوية لمجموعة من السياسات التي تؤثر على سلوك النظام.</span><span class="sxs-lookup"><span data-stu-id="51780-104">A convention is a container for a set of policies that affect system behavior.</span></span> <span data-ttu-id="51780-105">استنادًا إلى متطلبات العمل، يجب تحديد القواعد باستخدام مجموعة من السياسات المختلفة التي تنشر كيفية حساب التكاليف في محاسبة المخزون العالمي.</span><span class="sxs-lookup"><span data-stu-id="51780-105">Based on your business requirements, you must define conventions by using a combination of the various policies that establish how costs should be accounted in Global Inventory Accounting.</span></span> <span data-ttu-id="51780-106">يمكنك إقران كل قاعدة بدفتر أستاذ واحد أو أكثر لضمان التناسق في سياسات المحاسبة التي يتم تطبيقها عبر دفاتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="51780-106">You can associate each convention with one or more ledgers to ensure consistency in accounting policies that are applied across ledgers.</span></span>

<span data-ttu-id="51780-107">لإعداد القواعد الخاصة بك، انتقل إلى **محاسبة المخزون العالمي \> الإعداد \> القواعد**.</span><span class="sxs-lookup"><span data-stu-id="51780-107">To set up your conventions, go to **Global inventory accounting \> Setup \> Conventions**.</span></span> <span data-ttu-id="51780-108">بالنسبة لكل قاعدة، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="51780-108">For each convention, set the following fields:</span></span>

- <span data-ttu-id="51780-109">**الاسم** - أدخل اسم القاعدة.</span><span class="sxs-lookup"><span data-stu-id="51780-109">**Name** – Enter the name of the convention.</span></span>
- <span data-ttu-id="51780-110">**الوصف** - أدخل وصفًا للقاعدة.</span><span class="sxs-lookup"><span data-stu-id="51780-110">**Description** – Enter a description of the convention.</span></span>
- <span data-ttu-id="51780-111">**سياسة كائن التكلفة** - حدد سياسة كائن التكلفة.</span><span class="sxs-lookup"><span data-stu-id="51780-111">**Cost Object policy** – Select a cost object policy.</span></span> <span data-ttu-id="51780-112">تحدد هذه السياسات مستوى النقاوة التي يطبقها النظام لحساب قيمة المخزون والاحتفاظ بها.</span><span class="sxs-lookup"><span data-stu-id="51780-112">These policies determine the level of granularity that the system applies to calculate and maintain the inventory value.</span></span> <span data-ttu-id="51780-113">يتوفر الخياران التاليان سابقان التحديد:</span><span class="sxs-lookup"><span data-stu-id="51780-113">The following predefined options are available:</span></span>

    - <span data-ttu-id="51780-114">منتج</span><span class="sxs-lookup"><span data-stu-id="51780-114">Product</span></span>
    - <span data-ttu-id="51780-115">المنتج – الموقع</span><span class="sxs-lookup"><span data-stu-id="51780-115">Product – Site</span></span>
    - <span data-ttu-id="51780-116">المنتج – الموقع – المستودع</span><span class="sxs-lookup"><span data-stu-id="51780-116">Product – Site – Warehouse</span></span>

    <span data-ttu-id="51780-117">على سبيل المثال، إذا قمت بتحديد *المنتج – الموقع* (تدفق داخل أو تدفق خارج)، يقوم النظام بحساب تكلفة المخزون لكل منتج وصيانتها على مستوى الموقع.</span><span class="sxs-lookup"><span data-stu-id="51780-117">For example, if you select *Product – Site*, for every inventory movement (inflow or outflow), the system calculates and maintains the inventory cost of each product at the site level.</span></span> <span data-ttu-id="51780-118">لذلك، لا تؤثر حركات المخزون في المستويات الأدنى، مثل مستوى المستودع، على قيمة المخزون.</span><span class="sxs-lookup"><span data-stu-id="51780-118">Therefore, inventory movements at lower levels, such as the warehouse level, don't affect the inventory value.</span></span> <span data-ttu-id="51780-119">(مثال على نقل مستوى المستودع هو نقل صنف بين مستودعين في موقع واحد.) وبالمثل، لا يمكنك عرض تكلفة المخزون على مستوى أدنى، مثل مستوى المستودع.</span><span class="sxs-lookup"><span data-stu-id="51780-119">(An example of a warehouse-level transfer is an item transfer between two warehouses in one site.) Likewise, you can't view the inventory cost at a lower level, such as the warehouse level.</span></span>

- <span data-ttu-id="51780-120">**سياسة أساس قياس الإدخال** – حدد سياسة أساس قياس الإدخال.</span><span class="sxs-lookup"><span data-stu-id="51780-120">**Input measurement basis policy** – Select an input measurement basis policy.</span></span> <span data-ttu-id="51780-121">تحدد هذه السياسات التكاليف التي يجب أن تتدفق إلى حساب المخزون والتكاليف التي يجب أن يتم تحصيلها.</span><span class="sxs-lookup"><span data-stu-id="51780-121">These policies determine the costs that should flow into the inventory account and the costs that should be charged.</span></span> <span data-ttu-id="51780-122">الخيارات التالية ذات صلة للشركات التجارية:</span><span class="sxs-lookup"><span data-stu-id="51780-122">The following options are relevant for trading companies:</span></span>

    - <span data-ttu-id="51780-123">**تاريخي عادي** – تتدفق جميع مكونات التكلفة إلى حساب المخزون.</span><span class="sxs-lookup"><span data-stu-id="51780-123">**Normal historical** – All the cost components flow into the inventory account.</span></span>
    - <span data-ttu-id="51780-124">**قياسي** – تتدفق التكلفة المعيارية إلى حسابات المخزون، ويتم احتساب الفرق بين التكلفة المطبقة والتكاليف الفعلية على حسابات التباين.</span><span class="sxs-lookup"><span data-stu-id="51780-124">**Standard** – Standard cost flows into the inventory accounts, and the difference between the applied cost and the actual costs is charged to variance accounts.</span></span> <span data-ttu-id="51780-125">إذا كنت ترغب في إنشاء سياسة أساس قياس الإدخال *قياسي*، فيجب عليك أولاً إنشاء قائمة أسعار حيث يمكن للسياسة البحث عن التكلفة القياسية للصنف.</span><span class="sxs-lookup"><span data-stu-id="51780-125">If you want to create a *Standard* input measurement basis policy, you must first create a price list where the policy can look up the item's standard cost.</span></span>
    - <span data-ttu-id="51780-126">**قوائم الأسعار** – تدعم محاسبة المخزون العالمية جلب أسعار الأصناف من كيانات قانونية متعددة.</span><span class="sxs-lookup"><span data-stu-id="51780-126">**Price lists** – Global Inventory Accounting supports fetching item prices from multiple legal entities.</span></span> <span data-ttu-id="51780-127">يمكنك تحديد قائمة أسعار ستستخدمها سياسة أساس قياس الإدخال.</span><span class="sxs-lookup"><span data-stu-id="51780-127">You can define a price list that the input measurement basis policy will use.</span></span> <span data-ttu-id="51780-128">وبهذه الطريقة، فإن النظام يعرف مكان البحث عن سعر الصنف.</span><span class="sxs-lookup"><span data-stu-id="51780-128">In this way, the system will know where to look up the item price.</span></span> <span data-ttu-id="51780-129">لإعداد قوائم الأسعار‬، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="51780-129">Follow these steps to set up price lists:</span></span>

        1. <span data-ttu-id="51780-130">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="51780-130">In the **Name** field, enter a name.</span></span>
        1. <span data-ttu-id="51780-131">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="51780-131">In the **Description** field, enter a description.</span></span>
        1. <span data-ttu-id="51780-132">في الحقل **نوع التكلفة**، حدد نوع التكلفة (*تكلفة قياسية* أو *تكلفة مخططة*).</span><span class="sxs-lookup"><span data-stu-id="51780-132">In the **Costing type** field, select a costing type (*Standard cost* or *Planned cost*).</span></span>
        1. <span data-ttu-id="51780-133">في الحقل **نوع السعر**، حدد نوع السعر (*سعر التكلفة* أو *سعر الشراء* أو *سعر المبيعات*).</span><span class="sxs-lookup"><span data-stu-id="51780-133">In the **Price type** field, select a price type (*Cost*, *Purchase*, or *Sales price*).</span></span>
        1. <span data-ttu-id="51780-134">أضف إصدار التكلفة.</span><span class="sxs-lookup"><span data-stu-id="51780-134">Add a costing version.</span></span>
        1. <span data-ttu-id="51780-135">في جزء الإجراءات، حدد **السعر** للتحقق من صحة أسعار الأصناف في قائمة الأسعار.</span><span class="sxs-lookup"><span data-stu-id="51780-135">On the Action Pane, select **Price** to validate the item prices on the price list.</span></span>

- <span data-ttu-id="51780-136">**سياسة افتراض تدفق التكلفة** – حدد سياسة افتراض تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="51780-136">**Cost flow assumption policy** – Select a cost flow assumption policy.</span></span> <span data-ttu-id="51780-137">وتحدد هذه السياسات كيفية إزالة التكاليف من المخزون والإبلاغ عنها كتكلفة البضائع المبيعة.</span><span class="sxs-lookup"><span data-stu-id="51780-137">These policies determine how costs are removed from inventory and reported as the cost of goods sold.</span></span> <span data-ttu-id="51780-138">يتوفر الخياران التاليان سابقان التحديد:</span><span class="sxs-lookup"><span data-stu-id="51780-138">The following predefined options are available:</span></span>

    - <span data-ttu-id="51780-139">المتوسط</span><span class="sxs-lookup"><span data-stu-id="51780-139">Average</span></span>
    - <span data-ttu-id="51780-140">محدد – دُفعة</span><span class="sxs-lookup"><span data-stu-id="51780-140">Specific – Batch</span></span>

    > [!NOTE]
    > <span data-ttu-id="51780-141">إن محاسبة المخزون العالمي عبارة عن نظام المخزون الدائم.</span><span class="sxs-lookup"><span data-stu-id="51780-141">Global Inventory Accounting is a perpetual inventory system.</span></span> <span data-ttu-id="51780-142">لذلك، يتتبع النظام قيمة المخزون على أساس حركة بحركة.</span><span class="sxs-lookup"><span data-stu-id="51780-142">Therefore, the system tracks the inventory value on a transaction-by-transaction basis.</span></span>

- <span data-ttu-id="51780-143">**سياسة عنصر التكلفة** – يمكنك تحديد سياسات عنصر التكلفة وربطها بهذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="51780-143">**Cost element policy** – You can define cost element policies and link them to this field.</span></span> <span data-ttu-id="51780-144">يعتبر *عنصر التكلفة* تكلفة المصدر الذي يتم استهلاكه بحدث ما.</span><span class="sxs-lookup"><span data-stu-id="51780-144">A *cost element* is the cost of a resource that is consumed by an event.</span></span> <span data-ttu-id="51780-145">يمكنك استخدام عناصر التكلفة لتعقب التكاليف وتصنيفها.</span><span class="sxs-lookup"><span data-stu-id="51780-145">You can use cost elements to track and categorize costs.</span></span> <span data-ttu-id="51780-146">لإنشاء سياسة عنصر التكلفة، أدخل المعلومات في الأماكن التالية:</span><span class="sxs-lookup"><span data-stu-id="51780-146">To create cost element policies, enter information in the following places:</span></span>

    - <span data-ttu-id="51780-147">الحقل **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="51780-147">**Name** field</span></span>
    - <span data-ttu-id="51780-148">الحقل **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="51780-148">**Description** field</span></span>
    - <span data-ttu-id="51780-149">قائمة **عنصر التكلفة**</span><span class="sxs-lookup"><span data-stu-id="51780-149">**Cost element** list</span></span>
    - <span data-ttu-id="51780-150">شبكة **القواعد**</span><span class="sxs-lookup"><span data-stu-id="51780-150">**Rules** grid</span></span>

    <span data-ttu-id="51780-151">إذا كنت لا تريد تقسيم قيمة المخزون بشكل أكبر، فيجب عليك إنشاء قائمة عنصر تكلفة تحتوي على عنصر تكلفة واحد.</span><span class="sxs-lookup"><span data-stu-id="51780-151">If you don't want to break down the inventory value further, you must still create a cost element list that has a single cost element.</span></span> <span data-ttu-id="51780-152">ثم يجب إنشاء سياسة عنصر التكلفة لتعيين كافة أنواع القياس ذات الصلة (مكونات التكلفة) إلى عنصر التكلفة هذا.</span><span class="sxs-lookup"><span data-stu-id="51780-152">You must then create a cost element policy to map all the relevant measurement types (cost components) to that cost element.</span></span>
