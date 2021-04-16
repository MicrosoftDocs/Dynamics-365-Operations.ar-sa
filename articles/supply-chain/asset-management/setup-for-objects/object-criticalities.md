---
title: أنواع مستويات أهمية الأصول
description: يُوضح هذا الموضوع أنواع مستويات أهمية الأصول في إدارة الأصول.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb2da2d58b7f98fad80d0ea63bf4445ec4d08163
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808342"
---
# <a name="asset-criticality-types"></a><span data-ttu-id="d2d08-103">أنواع مستويات أهمية الأصول</span><span class="sxs-lookup"><span data-stu-id="d2d08-103">Asset criticality types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d2d08-104">يُوضح هذا الموضوع أنواع مستويات أهمية الأصول في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="d2d08-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="d2d08-105">يرتبط مستوى أهمية الأصل بالأصول ويتم تحويله إلى أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="d2d08-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="d2d08-106">لا يمكن تغييره على أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="d2d08-106">It can't be changed on a work order.</span></span> <span data-ttu-id="d2d08-107">يتم استخدام مستوى أهمية الأصل لحساب مستوى أهمية أمر عمل أثناء جدولة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="d2d08-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="d2d08-108">وبعبارة أخرى، يتم استخدامه لحساب مدى تأثير مهمة صيانة أحد الأصول على جدول الإنتاج والإنتاجية في شركتك.</span><span class="sxs-lookup"><span data-stu-id="d2d08-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="d2d08-109">لمزيد من المعلومات حول الإعداد المرتبط بحساب درجات التقييم لجدولة أمر العمل، راجع [معلمات إدارة الأصول](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d2d08-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="d2d08-110">لإعداد مستوى الأهمية، يترتب عليك أولاً إنشاء أنواع مستويات الأهمية التي يجب استخدامها في إعداد الأصول.</span><span class="sxs-lookup"><span data-stu-id="d2d08-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="d2d08-111">ثم إعداد مستويات أهمية الأصول.</span><span class="sxs-lookup"><span data-stu-id="d2d08-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="d2d08-112">إعداد أنواع مستويات الأهمية</span><span class="sxs-lookup"><span data-stu-id="d2d08-112">Set up criticality types</span></span>

1. <span data-ttu-id="d2d08-113">حدد **إدارة الأصول** \> **إعداد** \> **الأصول** \> **أنواع مستويات الأهمية**.</span><span class="sxs-lookup"><span data-stu-id="d2d08-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="d2d08-114">حدد **جديد** لإنشاء سجل.</span><span class="sxs-lookup"><span data-stu-id="d2d08-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="d2d08-115">في حقل **مستوى الأهمية**، أدخل رقمًا يشير إلى مستوى الأهمية.</span><span class="sxs-lookup"><span data-stu-id="d2d08-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="d2d08-116">في حقل **الاسم**، أدخل اسمًا لنوع مستوى الأهمية.</span><span class="sxs-lookup"><span data-stu-id="d2d08-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="d2d08-117">في حقل **المعامل**، أدخل معاملاً.</span><span class="sxs-lookup"><span data-stu-id="d2d08-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="d2d08-118">يُستخدم المعامل أثناء حساب جدولة أمر العمل لتحديد سجل مستوى الأهمية الذي يجب استخدامه.</span><span class="sxs-lookup"><span data-stu-id="d2d08-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="d2d08-119">(يتم استخدام السجل الذي يحتوي على أعلى معامل دائمًا.) يكون هذا الإعداد ذا صلة إذا تم إنشاء بنود مستويات الأهمية التي لها نفس قيمة الأهمية، كما هو موضح في الرسم التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="d2d08-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![صفحة أنواع الأهمية](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="d2d08-121">إعداد مستويات أهمية الأصول</span><span class="sxs-lookup"><span data-stu-id="d2d08-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="d2d08-122">حدد **إدارة الأصول** \> **إعداد** \> **مستويات أهمية الأصول**.</span><span class="sxs-lookup"><span data-stu-id="d2d08-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="d2d08-123">حدد **جديد** لإنشاء سجل.</span><span class="sxs-lookup"><span data-stu-id="d2d08-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="d2d08-124">وفقًا للمستوى المطلوب من التفاصيل لمستوى أهمية الأصل، قم بإجراء التحديدات ذات الصلة في الحقول **موقع العمل**، **نوع الأصل**، **الشركة المصنعة**، **النموذج**، **الأصل**، **فئة نوع المهمة**، **نوع المهمة**، **متغير نوع المهمة**، و **متطلبات المهمة**.</span><span class="sxs-lookup"><span data-stu-id="d2d08-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d2d08-125">عند تحديد مستوى أهمية الأصل، تمر إدارة الأصول عبر جميع سجلات مستويات أهمية الأصول للتحقق من احتمال وجود تطابق.</span><span class="sxs-lookup"><span data-stu-id="d2d08-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="d2d08-126">وهي تتحقق دائمًا من المجموعة الأكثر تحديدًا أولاً.</span><span class="sxs-lookup"><span data-stu-id="d2d08-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="d2d08-127">وبعبارة أخرى، تقوم إدارة الأصول أولاً بالتحقق من **متطلبات المهمة**.</span><span class="sxs-lookup"><span data-stu-id="d2d08-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="d2d08-128">إذا لم يتم العثور على تطابق، فإنه يتحقق من **متغير نوع المهمة**.</span><span class="sxs-lookup"><span data-stu-id="d2d08-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="d2d08-129">إذا لم يتم العثور على تطابق، فإنه يتحقق من **نوع المهمة**، وهكذا.</span><span class="sxs-lookup"><span data-stu-id="d2d08-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="d2d08-130">كما ترى في تخطيط الصفحة، يعني هذا السلوك أنه، للعثور على التركيبة الأكثر تحديدًا، تقوم إدارة الأصول بالتحقق من كل سجل من اليمين إلى اليسار للحصول على تطابق.</span><span class="sxs-lookup"><span data-stu-id="d2d08-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="d2d08-131">إذا لم يتم العثور على تطابق، يتم استخدام السجل "الافتراضي" الذي لا يحتوي على تحديدات.</span><span class="sxs-lookup"><span data-stu-id="d2d08-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="d2d08-132">في حقل **مستوى الأهمية**، حدد إحدى قيم مستوى الأهمية التي قمت بإنشائها في الإجراء السابق.</span><span class="sxs-lookup"><span data-stu-id="d2d08-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="d2d08-133">ملاحظات حول إعداد مستوى الأهمية</span><span class="sxs-lookup"><span data-stu-id="d2d08-133">Notes about criticality setup</span></span>

- <span data-ttu-id="d2d08-134">إذا قمت بتغيير مستوى أهمية أصل في هذا الإعداد بعد استخدامه فعليًا في أمر عمل، فلن يتم تحديث مستوى الأهمية في أمر العمل وفقًا لذلك.</span><span class="sxs-lookup"><span data-stu-id="d2d08-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="d2d08-135">يتم إعادة حساب مستوى الأهمية في أمر العمل في كل مرة تتم فيها إضافة بند أمر عمل إلى أمر العمل أو حذفه منه.</span><span class="sxs-lookup"><span data-stu-id="d2d08-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="d2d08-136">إذا كان أمر العمل يحتوي على العديد من مهام أمر العمل، يتم دائمًا استخدام أعلى مستوى أهمية، وفق حقل **المعامل** في صفحة **أنواع مستويات الأهمية** في أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="d2d08-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="d2d08-137">بشكل عام، يمكن أن يتغير مستوى أهمية الأصل خلال فترة ما.</span><span class="sxs-lookup"><span data-stu-id="d2d08-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="d2d08-138">ويمكن أن يتأثر مستوى الأهمية بشراء معدات جديدة، والتجديدات، وما إلى ذلك.</span><span class="sxs-lookup"><span data-stu-id="d2d08-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="d2d08-139">خذ بعين الاعتبار إعادة تقييم مستويات أهمية الأصول على فترات منتظمة (على سبيل المثال، مرة واحدة في السنة أو كل سنتين) للتأكد من تطابق تعريفات مستويات الأهمية مع إعداد الإنتاج الحالي.</span><span class="sxs-lookup"><span data-stu-id="d2d08-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]