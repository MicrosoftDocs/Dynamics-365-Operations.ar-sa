---
title: إنشاء أصول استنادًا إلى أوامر الشراء
description: يشرح هذا الموضوع كيفية إنشاء قائمة تتضمن أصناف الأصول التي يمكن استخدامها كأساس لإنشاء أصول لمهام الصيانة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83419fa5c6b6aee0b321c526565c3518deaf4bd0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016974"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="e4a32-103">إنشاء أصول استنادًا إلى أوامر الشراء</span><span class="sxs-lookup"><span data-stu-id="e4a32-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e4a32-104">يشرح هذا الموضوع كيفية إنشاء قائمة تتضمن أصناف الأصول التي يمكن استخدامها كأساس لإنشاء أصول لمهام الصيانة في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="e4a32-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="e4a32-105">استنادًا إلى أصناف الأصول، يمكنك عرض قائمة ببنود أوامر الشراء التي تم إنشاؤها على هذه الأصناف.</span><span class="sxs-lookup"><span data-stu-id="e4a32-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="e4a32-106">الغرض من هذه الوظيفة هو إنشاء أصل بسهولة في إدارة الأصول استنادًا إلى أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="e4a32-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="e4a32-107">أولاً، يمكنك إعداد الأصناف المراد استخدامها لإنشاء أصول من أمر شراء في **أصناف الأصول**.</span><span class="sxs-lookup"><span data-stu-id="e4a32-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="e4a32-108">بعد إنشاء بند أمر شراء، يمكنك إنشاء الأصول في **الأصول المعلقة**.</span><span class="sxs-lookup"><span data-stu-id="e4a32-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="e4a32-109">من الممكن تحديد المرحلة في بند الشراء التي يجب فيها إنشاء الأصل.</span><span class="sxs-lookup"><span data-stu-id="e4a32-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="e4a32-110">تحديد أصناف الأصول</span><span class="sxs-lookup"><span data-stu-id="e4a32-110">Select asset items</span></span>

1. <span data-ttu-id="e4a32-111">انقر فوق **إدارة الأصول** > **الإعداد** > **الأصول‏‎** > **الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="e4a32-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="e4a32-112">انقر فوق **جديد** لإنشاء صنف أصل جديد.</span><span class="sxs-lookup"><span data-stu-id="e4a32-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="e4a32-113">في الحقل **رقم الصنف**، حدد الصنف.</span><span class="sxs-lookup"><span data-stu-id="e4a32-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="e4a32-114">عندما تغدر هذا الحقل، يتم إدراج اسم الصنف بشكل تلقائي في حقل **اسم المنتج**.</span><span class="sxs-lookup"><span data-stu-id="e4a32-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="e4a32-115">على علامة التبويب السريعة **عام** حدد نوع أصل للصنف.</span><span class="sxs-lookup"><span data-stu-id="e4a32-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="e4a32-116">حدد الشركة المصنعة للأصل ونموذج الصنف.</span><span class="sxs-lookup"><span data-stu-id="e4a32-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="e4a32-117">احفظ الصنف.</span><span class="sxs-lookup"><span data-stu-id="e4a32-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="e4a32-118">إنشاء أصول من أصول معلقة</span><span class="sxs-lookup"><span data-stu-id="e4a32-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="e4a32-119">انقر فوق **إدارة‏‎ الأصول‏‎** > **عام** > **الأصول‏‎** > **الأصول‏‎ المعلقة**.</span><span class="sxs-lookup"><span data-stu-id="e4a32-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="e4a32-120">سترى قائمة محدثة بأوامر الشراء استنادًا إلى الأصناف المحددة في **أصناف الأصول**.</span><span class="sxs-lookup"><span data-stu-id="e4a32-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="e4a32-121">يمكنك تصفية حالة أوامر الشراء لتحديد حالة دورة الحياة التي يجب إنشاء الأصل عندها.</span><span class="sxs-lookup"><span data-stu-id="e4a32-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="e4a32-122">على سبيل المثال، قد ترغب فقط في إنشاء أصول عند ترحيل إيصال منتج في أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="e4a32-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="e4a32-123">حدد الارتباط‏‎ **رقم المرجع** في بند أمر شراء لعرض معلومات مفصلة حول الصنف.</span><span class="sxs-lookup"><span data-stu-id="e4a32-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="e4a32-124">إذا كنت ترغب في تحرير الأبعاد التي تظهر على علامة التبويب السريعة **أبعاد المخزون**، فانقر فوق الزر **عرض الأبعاد**، وبعد ذلك يمكنك إجراء تحديداتك.</span><span class="sxs-lookup"><span data-stu-id="e4a32-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="e4a32-125">إذا كنت ترغب في إنشاء أصل استنادًا إلى بند أمر شراء، فحدد خانة الاختيار في العمود **علامة** لهذا البند في صفحة القائمة، وانقر فوق **إنشاء أصول**.</span><span class="sxs-lookup"><span data-stu-id="e4a32-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="e4a32-126">ستظهر رسالة تعلمك بمعرف الأصل.</span><span class="sxs-lookup"><span data-stu-id="e4a32-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="e4a32-127">حدد الأصل في قائمة **كل الأصول** وانقر فوق **تحرير** لإضافة مزيد من المعلومات إلى الأصل.</span><span class="sxs-lookup"><span data-stu-id="e4a32-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="e4a32-128">في **الأصول‏‎ المعلقة**، إذا أردت حذف بند لأنك لا تريد إنشاء أصل، فحدد خانة الاختيار في العمود **علامة** لهذا البند، وانقر فوق **تجاهل الأصول المعلقة**.</span><span class="sxs-lookup"><span data-stu-id="e4a32-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="e4a32-129">ستظهر رسالة تعلمك بمعرف الأصل.</span><span class="sxs-lookup"><span data-stu-id="e4a32-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="e4a32-130">أنت لا تحذف أمر الشراء أو أمر المبيعات، بل فقط السجل الذي كان بإمكانك إنشاء أصل منه في **إدارة الأصول**.</span><span class="sxs-lookup"><span data-stu-id="e4a32-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="e4a32-131">يتم نقل جميع أبعاد المنتج (الحجم واللون والتكوين وما إلى ذلك) تلقائيًا إلى سمات الأصول.</span><span class="sxs-lookup"><span data-stu-id="e4a32-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="e4a32-132">يتم تخزين أبعاد التتبع (الرقم التسلسلي) مباشرة ً على الأصل عند إنشاء الأصل.</span><span class="sxs-lookup"><span data-stu-id="e4a32-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="e4a32-133">البحث عن الأصول المعلقة</span><span class="sxs-lookup"><span data-stu-id="e4a32-133">Find pending assets</span></span>

<span data-ttu-id="e4a32-134">يمكنك تشغيل عملية **تعداد الأصول المعلقة** للتحقق من الأصول المعلقة.</span><span class="sxs-lookup"><span data-stu-id="e4a32-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="e4a32-135">على سبيل المثال، يمكن استخدام هذه الوظيفة لتلقي إشعار في كل مرة يكون فيها الأصل المعلق جاهزًا لإنشائه كأصل.</span><span class="sxs-lookup"><span data-stu-id="e4a32-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="e4a32-136">انقر فوق **إدارة‏‎ الأصول‏‎** > **دوري** > **الأصول‏‎** > **تعداد الأصول‏‎ المعلقة**.</span><span class="sxs-lookup"><span data-stu-id="e4a32-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="e4a32-137">انقر فوق **موافق** لتشغيل الوظيفة وتحديث القائمة في **الأصول المعلقة**.</span><span class="sxs-lookup"><span data-stu-id="e4a32-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="e4a32-138">يمكنك إعداد هذه الوظيفة لتشغيلها وظيفة دفعية، على سبيل المثال، مرة كل يوم.</span><span class="sxs-lookup"><span data-stu-id="e4a32-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="e4a32-139">**تحذير:** إذا تغيرت البيانات في أمر شراء *بعد* إنشاء أصل استنادًا إلى الصنف المتعلق به، لن تظهر هذه التغييرات في الأصل.</span><span class="sxs-lookup"><span data-stu-id="e4a32-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>
