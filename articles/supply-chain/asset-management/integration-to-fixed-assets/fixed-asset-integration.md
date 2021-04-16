---
title: تكامل إدارة الأصول مع الأصول الثابتة
description: يوضح هذا الموضوع كيفية تكامل وحدات إدارة الأصول والوحدات النمطية للأصول الثابتة، بحيث يمكنك ربط الأصول الثابتة بأصول الصيانة.
author: kamaybac
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: a45bf1f62cdcc8abed2ec157a223e7f3fddec7ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809844"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="bd9c0-103">تكامل إدارة الأصول مع الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="bd9c0-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd9c0-104">من خلال تكامل وحدات **إدارة الأصول** و **الأصول الثابتة**، يمكنك ربط الأصول الثابتة مع أصول الصيانة.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="bd9c0-105">بعد ذلك يمكن لمستخدمي الأصول الثابتة إنشاء أصل صيانة من أصل ثابت موجود أو جديد، ويمكن لمستخدمي إدارة الأصول ربط أصل صيانة بأصل ثابت موجود.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="bd9c0-106">تعمل هذه الميزة أيضا على تسهيل قيام مستخدمي الأصول الثابتة بعرض التكاليف التي تم ترحيلها من أوامر العمل لأصول الصيانة ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="bd9c0-107">في هذا الموضوع، تشير *أصول الصيانة* إلى الأصول من وحدة **إدارة الأصول**، وتشير *الأصول الثابتة* إلى الأصول من وحدة **الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="bd9c0-108">تعيين موقع افتراضي لأصول الصيانة الجديدة التي تم إنشاؤها من الأصول الثابتة (اختياري)</span><span class="sxs-lookup"><span data-stu-id="bd9c0-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="bd9c0-109">يتيح لك هذا التكوين الاختياري تعيين موقع عمل افتراضي لأصول الصيانة الجديدة التي تم إنشاؤها من الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="bd9c0-110">يتعين عليك في العادة إكمال هذا التكوين مرة واحدة فقط، إذا كان ذلك مطلوبًا منك.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="bd9c0-111">لإكمال التكوين، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="bd9c0-112">انتقل إلى **إدارة الأصول‬ \> الإعداد‬ \> معلمات إدارة الأصول**.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="bd9c0-113">في علامة التبويب **الأصول الثابتة**، في الحقل **موقع العمل**، حدد الموقع الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="bd9c0-114">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="bd9c0-115">التعامل مع أصول الصيانة المتكاملة والأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="bd9c0-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="bd9c0-116">يوفر هذا القسم مجموعة من الإجراءات التي تعرض طرقًا متنوعة يمكنك من خلالها التعامل مع ميزات إدارة الأصول المتكاملة والأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="bd9c0-117">إقران أصل صيانة موجود بأصل ثابت</span><span class="sxs-lookup"><span data-stu-id="bd9c0-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="bd9c0-118">لإقران أصل صيانة موجود بأصل ثابت، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="bd9c0-119">انتقل إلى **إدارة الأصول \> الأصول \> كل الأصول** (أو **الأصول النشطة**).</span><span class="sxs-lookup"><span data-stu-id="bd9c0-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="bd9c0-120">حدد أحد الأصول.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-120">Select an asset.</span></span>
1. <span data-ttu-id="bd9c0-121">في علامة التبويب السريعة **الأصل الثابت**، في حقل **رقم الأصل الثابت**، حدد أصل ثابت موجود.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="bd9c0-122">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="bd9c0-123">عرض الأصل الثابت المقترن بأصل الصيانة المحدد</span><span class="sxs-lookup"><span data-stu-id="bd9c0-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="bd9c0-124">لعرض الأصل الثابت المقترن بأصل الصيانة المحدد، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="bd9c0-125">انتقل إلى **إدارة الأصول \> الأصول \> كل الأصول** (أو **الأصول النشطة**).</span><span class="sxs-lookup"><span data-stu-id="bd9c0-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="bd9c0-126">حدد أحد الأصول.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-126">Select an asset.</span></span>
1. <span data-ttu-id="bd9c0-127">في علامة التبويب السريعة **الأصل الثابت**، في حقل **رقم الأصل الثابت**، حدد الارتباط.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="bd9c0-128">يتم فتح صفحة **الأصول الثابتة** للأصل المحدد.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="bd9c0-129">(عاده ما يتم العثور على هذه الصفحة في **الأصول الثابتة \> الأصول الثابتة \> الأصول الثابتة**.)</span><span class="sxs-lookup"><span data-stu-id="bd9c0-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="bd9c0-130">عرض أصل الصيانة المقترن بالأصل الثابت المحدد</span><span class="sxs-lookup"><span data-stu-id="bd9c0-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="bd9c0-131">لعرض أصل الصيانة المقترن بالأصل الثابت المحدد، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="bd9c0-132">انتقل إلى **الأصول الثابتة \> الأصول الثابتة \> الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="bd9c0-133">حدد أحد الأصول.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-133">Select an asset.</span></span>
1. <span data-ttu-id="bd9c0-134">في جزء الإجراء، ضمن علامة التبويب **إدارة الأصول**، في مجموعة **‏‫عرض**، حدد **أصل الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="bd9c0-135">يتم فتح صفحة **أصل الصيانة** للأصل المقترن بالأصل الثابت المحدد.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="bd9c0-136">(عادة ما يتم العثور على هذه الصفحة في **إدارة الأصول \> الأصول \> كل الأصول**.)</span><span class="sxs-lookup"><span data-stu-id="bd9c0-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="bd9c0-137">عرض تكاليف الصيانة المقترنة بالأصل الثابت</span><span class="sxs-lookup"><span data-stu-id="bd9c0-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="bd9c0-138">يمكن ترحيل أوامر عمل إدارة الأصول لأصول الصيانة، وعادة ما يكون لكل أمر من أوامر العمل هذه تكلفة.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="bd9c0-139">عند اقتران أصل ثابت بأصل صيانة، يمكنك الانتقال مباشرة من الأصل الثابت لعرض التكاليف ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="bd9c0-140">لعرض تكاليف الصيانة المقترنة بالأصل الثابت، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="bd9c0-141">انتقل إلى **الأصول الثابتة \> الأصول الثابتة \> الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="bd9c0-142">حدد أحد الأصول.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-142">Select an asset.</span></span>
1. <span data-ttu-id="bd9c0-143">في جزء الإجراء، ضمن علامة التبويب **إدارة الأصول**، في مجموعة **‏‫عرض**، حدد **تكلفة الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="bd9c0-144">يتم فتح صفحة **تكلفة الصيانة** وعرض التكاليف ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="bd9c0-145">إنشاء أصل صيانة جديد لأصل ثابت موجود</span><span class="sxs-lookup"><span data-stu-id="bd9c0-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="bd9c0-146">لإنشاء أصل صيانة جديد لأصل ثابت موجود، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="bd9c0-147">انتقل إلى **الأصول الثابتة \> الأصول الثابتة \> الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="bd9c0-148">حدد أحد الأصول.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-148">Select an asset.</span></span>
1. <span data-ttu-id="bd9c0-149">في جزء الإجراء، ضمن علامة التبويب **إدارة الأصول**، في مجموعة **‏جديد**، حدد **إنشاء أصل صيانة**.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="bd9c0-150">(إذا لم يكن هذا الخيار متاحًا، فقد يكون أصل الصيانة مرتبطًا بالفعل بالأصل الثابت المحدد.)</span><span class="sxs-lookup"><span data-stu-id="bd9c0-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="bd9c0-151">قم بإنهاء إنشاء الأصل كما هو موضح في [إنشاء أصل](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="bd9c0-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="bd9c0-152">إنشاء أصل ثابت جديد وإضافة أصل صيانة موجود له</span><span class="sxs-lookup"><span data-stu-id="bd9c0-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="bd9c0-153">لإنشاء أصل ثابت جديد وإضافة أصل صيانة جديد له، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="bd9c0-154">انتقل إلى **الأصول الثابتة \> الأصول الثابتة \> الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="bd9c0-155">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="bd9c0-156">قم بإنهاء إنشاء الأصل الثابت كما هو موضح في [إنشاء أصل ثابت](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="bd9c0-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="bd9c0-157">في جزء الإجراء، ضمن علامة التبويب **إدارة الأصول**، في مجموعة **‏جديد**، حدد **إنشاء أصل صيانة**.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="bd9c0-158">قم بإنهاء إنشاء الأصل كما هو موضح في [إنشاء أصل](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="bd9c0-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="bd9c0-159">إزالة الاقتران بين أصلين</span><span class="sxs-lookup"><span data-stu-id="bd9c0-159">Remove the association between two assets</span></span>

<span data-ttu-id="bd9c0-160">في بعض الحالات، قد تضطر إلى إلغاء اقتران أصل صيانة بأصل ثابت.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="bd9c0-161">على سبيل المثال، إذا كنت ترغب في [إنشاء أصل صيانة جديد](#new-maintenance-from-fixed) من أحد الأصول الثابتة، فيجب أولا إزالة أي اقتران موجود.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="bd9c0-162">لإزالة الاقتران الموجود بي أصل صيانة وأصل ثابت، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="bd9c0-163">انتقل إلى **إدارة الأصول \> الأصول \> كل الأصول** (أو **الأصول النشطة**).</span><span class="sxs-lookup"><span data-stu-id="bd9c0-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="bd9c0-164">ابحث عن الأصل الثابت وافتحه.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="bd9c0-165">في علامة التبويب السريعة **الأصل الثابت**، قم بمسح القيمة من حقل **الموقع الوظيفي**.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="bd9c0-166">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bd9c0-166">On the Action Pane, select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]