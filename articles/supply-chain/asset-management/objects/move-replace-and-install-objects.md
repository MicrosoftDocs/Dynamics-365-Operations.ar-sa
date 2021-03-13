---
title: نقل الأصول واستبدالها وتثبيتها
description: يشرح هذا الموضوع كيفية نقل الأصول واستبدالها وتثبيتها في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 022ffc59b1b64913fedaf550f3fdb32141a94031
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020269"
---
# <a name="move-replace-and-install-assets"></a><span data-ttu-id="644a6-103">نقل الأصول واستبدالها وتثبيتها</span><span class="sxs-lookup"><span data-stu-id="644a6-103">Move, replace, and install assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="644a6-104">يشرح هذا الموضوع كيفية نقل الأصول واستبدالها وتثبيتها في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="644a6-104">This topic explains how to move, replace, and install assets in Asset Management.</span></span> <span data-ttu-id="644a6-105">يمكنك إنشاء أصول فرديه ليس لديها علاقات بأصول أخرى، أو يمكنك إنشاء بنية أصل تتضمن أصلاً أساسيًا (الأصل عالي المستوي) وأصولاً تابعة ذات صلة (الأصول الفرعية).</span><span class="sxs-lookup"><span data-stu-id="644a6-105">You can create individual assets that have no relations to other assets, or you can create an asset structure that includes a parent asset (top-level asset) and related child assets (sub-assets).</span></span> <span data-ttu-id="644a6-106">في إدارة الأصول، توجد ثلاث طرق لنقل موقع أحد الأصول وتغييره:</span><span class="sxs-lookup"><span data-stu-id="644a6-106">In Asset Management, there are three approaches to moving and changing the location of an asset:</span></span>

- <span data-ttu-id="644a6-107">**نقل** – نقل أصل إلى بنية أصل أخرى، أو إلى موقع آخر في بنية الأصل نفسها.</span><span class="sxs-lookup"><span data-stu-id="644a6-107">**Move** – Move an asset either to another asset structure or to another location in the same asset structure.</span></span>
- <span data-ttu-id="644a6-108">**استبدال** – إزالة أصل بشكل مؤقت من بنية أصل بحيث يمكن إصلاحه أو تجديده، ثم إعادة إضافة الأصل المجدد إلى بنية الأصل لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="644a6-108">**Replace** – Temporarily remove an asset from an asset structure so that it can be repaired or refurbished, and then add the refurbished asset back to the asset structure later.</span></span> <span data-ttu-id="644a6-109">وبدلا من ذلك، يمكنك استبدال الأصل المستخدم بأصل جديد بشكل دائم.</span><span class="sxs-lookup"><span data-stu-id="644a6-109">Alternatively, permanently replace a used asset with a new asset.</span></span>
- <span data-ttu-id="644a6-110">**تثبيت** – تثبيت أصل أساسي والأصول التابعة ذات الصلة في موقع عمل.</span><span class="sxs-lookup"><span data-stu-id="644a6-110">**Install** – Install a parent asset and any related child assets on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="644a6-111">قد يكون الأصل الذي تقوم بنقله أو استبداله أو تثبيته مرتبطًا بموقع عمل آخر.</span><span class="sxs-lookup"><span data-stu-id="644a6-111">The asset that you move, replace, or install might be related to another functional location.</span></span> <span data-ttu-id="644a6-112">وفي هذه الحالة، قد يستخدم الأصل الأبعاد المالية لموقع العمل.</span><span class="sxs-lookup"><span data-stu-id="644a6-112">In that case, the asset might use financial dimensions of the functional location.</span></span> <span data-ttu-id="644a6-113">في صفحة **أنواع مواقع العمل**، يمكنك إعداد معالجه الأبعاد المالية على مواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="644a6-113">On the **Functional location types** page, you set up the handling of financial dimensions on functional locations.</span></span>

## <a name="move-asset"></a><span data-ttu-id="644a6-114">نقل الأصل</span><span class="sxs-lookup"><span data-stu-id="644a6-114">Move asset</span></span>

<span data-ttu-id="644a6-115">استخدم وظيفة **نقل الأصل** لنقل أصل إلى بنية أصل أخرى أو إلى موقع آخر في بنية الأصل نفسها.</span><span class="sxs-lookup"><span data-stu-id="644a6-115">Use the **Move asset** function to move an asset either to another asset structure or to another location in the same asset structure.</span></span> <span data-ttu-id="644a6-116">يمكنك أيضًا نقل أصل من بنية أصل بحيث يصبح أصلاً مستقلاً ليس لديه علاقات مع البنية.</span><span class="sxs-lookup"><span data-stu-id="644a6-116">You can also move an asset out of an asset structure so that it becomes a standalone asset that has no structure relations.</span></span>

> [!NOTE]
> <span data-ttu-id="644a6-117">لا تستخدم هذه الوظيفة إذا كانت الأصول خاضعة لعملية إصلاح أو يتم استبدالها بشكل مؤقت.</span><span class="sxs-lookup"><span data-stu-id="644a6-117">Don't use this function if assets are being repaired or temporarily replaced.</span></span> <span data-ttu-id="644a6-118">بدلاً من ذلك، استخدم وظيفة **استبدال الأصل** التي سيرد وصفها لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="644a6-118">Instead, use the **Replace asset** functionality that is described later in this topic.</span></span>

1. <span data-ttu-id="644a6-119">حدد **إدارة الأصول** \> **عام** \> **الأصول‏‎** \> **كل الأصول‏‎** أو **الأصول‏‎**.</span><span class="sxs-lookup"><span data-stu-id="644a6-119">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="644a6-120">في القائمة، حدد الأصل الذي تريد نقله.</span><span class="sxs-lookup"><span data-stu-id="644a6-120">In the list, select the asset to move.</span></span> <span data-ttu-id="644a6-121">إذا كان الأصل يحتوي على أصول تابعة، فستنقل هذه الأصول أيضًا.</span><span class="sxs-lookup"><span data-stu-id="644a6-121">If the asset has child assets, you also move those assets.</span></span>
3. <span data-ttu-id="644a6-122">حدد **نقل الأصل**.</span><span class="sxs-lookup"><span data-stu-id="644a6-122">Select **Move asset**.</span></span>
4. <span data-ttu-id="644a6-123">لنقل الأصل بحيث يصبح جزءًا من بنية أصل، حدد الأصل الأساسي الجديد في الحقل **أصل أساسي**.</span><span class="sxs-lookup"><span data-stu-id="644a6-123">To move the asset so that it becomes part of an asset structure, select the new parent asset in the **Parent asset** field.</span></span> <span data-ttu-id="644a6-124">إذا كنت تعمل على نقل أصل تابع وتريد تحويله إلى أصل مستقل لا علاقة لها ببنية أصل، فاترك الحقل **أصل أساسي** فارغًا.</span><span class="sxs-lookup"><span data-stu-id="644a6-124">If you're moving a child asset, and you want to make it a standalone asset that has no structure relations, leave the **Parent asset** field blank.</span></span>
5. <span data-ttu-id="644a6-125">بشكل افتراضي، يتم تعيين الحقل **ساري** إلى التاريخ والوقت الحاليين.</span><span class="sxs-lookup"><span data-stu-id="644a6-125">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="644a6-126">ومع ذلك، يمكنك تحديد تاريخ ووقت مختلفين لبدء صلاحية نقل الأصل.</span><span class="sxs-lookup"><span data-stu-id="644a6-126">However, you can select a different date and time that the asset move is valid from.</span></span>
6. <span data-ttu-id="644a6-127">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="644a6-127">Select **OK**.</span></span>

## <a name="replace-asset"></a><span data-ttu-id="644a6-128">استبدال الأصل</span><span class="sxs-lookup"><span data-stu-id="644a6-128">Replace asset</span></span>

<span data-ttu-id="644a6-129">استخدم وظيفة **استبدال الأصل** فيما يتعلق بإصلاح أصل مستهلك أو تجديده أو استبداله بأصل جديد.</span><span class="sxs-lookup"><span data-stu-id="644a6-129">Use the **Replace asset** function in connection with repairs, refurbishment, or permanent replacement of a worn-out asset by a new asset.</span></span> <span data-ttu-id="644a6-130">تستخدم هذه الوظيفة لاستبدال الأصول الفرعية في بنية أصل.</span><span class="sxs-lookup"><span data-stu-id="644a6-130">This function is used to replace child assets in an asset structure.</span></span> <span data-ttu-id="644a6-131">بالنسبة إلى الأصول الأساسية (وهي الأصول التي ليس لديه أصل اساسي في الوقت الحالي)، يتم هذا الاستبدال في موقع عمل.</span><span class="sxs-lookup"><span data-stu-id="644a6-131">For parent assets (that is, assets that don't currently have a parent asset), this replacement is done on a functional location.</span></span> <span data-ttu-id="644a6-132">لمزيد من المعلومات حول كيفيه استبدال الأصول الأساسية في موقع عمل، راجع [تثبيت الأصول في مواقع العمل‬](../functional-locations/install-objects-on-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="644a6-132">For more information about how to replace parent assets on a functional location, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="644a6-133">إذا كانت إحدى ورشح التصليم مرتبطة بقسم الإنتاج، فيمكنك إنشاء مواقع عمل مثل **الإصلاح** و **الخردة‬** و **المخزن** لمعالجة عمليات إصلاح الأصول واستبدالها.</span><span class="sxs-lookup"><span data-stu-id="644a6-133">If a repair shop is related to your production department, you can create functional locations such as **Repair**, **Scrap**, and **Storage** to handle the repair and replacement of assets.</span></span>

1. <span data-ttu-id="644a6-134">حدد **إدارة الأصول** \> **عام** \> **الأصول‏‎** \> **كل الأصول‏‎** أو **الأصول‏‎**.</span><span class="sxs-lookup"><span data-stu-id="644a6-134">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="644a6-135">في القائمة، حدد الأصل التابع الذي تريد استبداله.</span><span class="sxs-lookup"><span data-stu-id="644a6-135">In the list, select the child asset to replace.</span></span> <span data-ttu-id="644a6-136">إذا كان الأصل يحتوي على أصول تابعة، فستستبدل هذه الأصول أيضًا.</span><span class="sxs-lookup"><span data-stu-id="644a6-136">If the asset has child assets, you also replace those assets.</span></span>
3. <span data-ttu-id="644a6-137">حدد **استبدال الأصل**.</span><span class="sxs-lookup"><span data-stu-id="644a6-137">Select **Replace asset**.</span></span>

    <span data-ttu-id="644a6-138">يظهر الحقل‏‎ **تغيير البنية**  آخر تاريخ ووقت تم فيه نقل الأصل المحدد والأصول التابعة المرتبطة في بنية الأصل.</span><span class="sxs-lookup"><span data-stu-id="644a6-138">The **Structure change** field shows the last date and time that the selected asset and related child assets were moved in the asset structure.</span></span>

4. <span data-ttu-id="644a6-139">في قسم **الأصل المحدد** في الحقل **موقع العمل الهدف**، حدد موقع العمل لنقل الأصل إليه.</span><span class="sxs-lookup"><span data-stu-id="644a6-139">In the **Selected asset** section, in the **Target functional location** field, select the functional location to move the asset to.</span></span> <span data-ttu-id="644a6-140">على سبيل المثال، حدد موقع **الإصلاح** أو **الخردة**.</span><span class="sxs-lookup"><span data-stu-id="644a6-140">For example, select the **Repair** or **Scrap** location.</span></span>

    <span data-ttu-id="644a6-141">في قسم **أصل أساسي**، يعرض الحقل **ساري‬** آخر تاريخ ووقت تم فيه تثبيت الأصل الأساسي والأصول التابعة المرتبطة به أو نقلها في موقع العمل الحالي.</span><span class="sxs-lookup"><span data-stu-id="644a6-141">In the **Parent asset** section, the **Effective** field shows the last date and time that the parent asset and related child assets were installed or moved on the current functional location.</span></span>

5. <span data-ttu-id="644a6-142">في قسم **أصل جديد**، في حقل **الأصل** حدد الأصل المراد إدراجه كبديل مؤقت أو دائم للأصل المحدد.</span><span class="sxs-lookup"><span data-stu-id="644a6-142">In the **New asset** section, in the **Asset** field, select the asset to insert as a temporary or permanent replacement for the selected asset.</span></span> <span data-ttu-id="644a6-143">قد يقع هذا الأصل في الوقت الحالي في موقع عمل آخر، مثل **المخزن**.</span><span class="sxs-lookup"><span data-stu-id="644a6-143">This asset might currently be located on another functional location, such as **Storage**.</span></span>
7. <span data-ttu-id="644a6-144">في الحقل **ساري من**، يتم تعيين الحقل **ساري** إلى التاريخ والوقت الحاليين بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="644a6-144">In the **Effective from** section, the **Effective** field is set to the current date and time by default.</span></span> <span data-ttu-id="644a6-145">ومع ذلك، يمكنك تحديد تاريخ ووقت مختلفين لبدء صلاحية بديل الأصل.</span><span class="sxs-lookup"><span data-stu-id="644a6-145">However, you can select a different date and time that the asset replacement is valid from.</span></span>
8. <span data-ttu-id="644a6-146">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="644a6-146">Select **OK**.</span></span>

## <a name="install-asset"></a><span data-ttu-id="644a6-147">تثبيت الأصل</span><span class="sxs-lookup"><span data-stu-id="644a6-147">Install asset</span></span>

<span data-ttu-id="644a6-148">استخدم وظيفة **تثبيت الأصل** لتثبيت بنية أصل في موقع عمل.</span><span class="sxs-lookup"><span data-stu-id="644a6-148">Use the **Install asset** function to install an asset structure on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="644a6-149">حدد دائمًا أصلاً أساسيًا.</span><span class="sxs-lookup"><span data-stu-id="644a6-149">Always select a parent asset.</span></span> <span data-ttu-id="644a6-150">سيتم نقل الأصل الأساسي والأصول التابعة المرتبطة إلى موقع العمل المحدد.</span><span class="sxs-lookup"><span data-stu-id="644a6-150">The parent asset and related child assets will be moved to the selected functional location.</span></span>

1. <span data-ttu-id="644a6-151">حدد **إدارة الأصول** \> **عام** \> **الأصول‏‎** \> **كل الأصول‏‎** أو **الأصول‏‎**.</span><span class="sxs-lookup"><span data-stu-id="644a6-151">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="644a6-152">في القائمة، حدد الأصل الأساسي المراد تثبيته في موقع عمل آخر.</span><span class="sxs-lookup"><span data-stu-id="644a6-152">In the list, select the parent asset to install on another functional location.</span></span>
3. <span data-ttu-id="644a6-153">حدد **تثبيت الأصل**.</span><span class="sxs-lookup"><span data-stu-id="644a6-153">Select **Install asset**.</span></span>

    <span data-ttu-id="644a6-154">يعرض قسم **السمات** سمات الأصول التي يتم إعدادها في الأصل الأساسي.</span><span class="sxs-lookup"><span data-stu-id="644a6-154">The **Attributes** section shows the asset attributes that are set up on the parent asset.</span></span>

4. <span data-ttu-id="644a6-155">في حقل **موقع العمل**، اختر الموقع الجديد.</span><span class="sxs-lookup"><span data-stu-id="644a6-155">In the **Functional location** field, select the new location.</span></span>
5. <span data-ttu-id="644a6-156">بشكل افتراضي، يتم تعيين الحقل **ساري** إلى التاريخ والوقت الحاليين.</span><span class="sxs-lookup"><span data-stu-id="644a6-156">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="644a6-157">ومع ذلك، يمكنك تحديد تاريخ ووقت مختلفين لبدء صلاحية التثبيت على بنية الأصل.</span><span class="sxs-lookup"><span data-stu-id="644a6-157">However, you can select a different date and time that the installation on the asset structure is valid from.</span></span>
6. <span data-ttu-id="644a6-158">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="644a6-158">Select **OK**.</span></span>
