---
title: إنشاء أصل منتج
description: أنشئ أصل المنتج للمتغيرات المعرفة مسبقًا.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d580d323409d84bab66dc03d39e084f5ee0cfc64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218479"
---
# <a name="create-a-product-master"></a><span data-ttu-id="d3d40-103">إنشاء أصل منتج</span><span class="sxs-lookup"><span data-stu-id="d3d40-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d3d40-104">أنشئ أصل المنتج للمتغيرات المعرفة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="d3d40-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="d3d40-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="d3d40-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d3d40-106">هذا الإجراء مخصص لمصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="d3d40-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="d3d40-107">إنشاء أصل منتج جديد</span><span class="sxs-lookup"><span data-stu-id="d3d40-107">Create a new product master</span></span>
1. <span data-ttu-id="d3d40-108">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة معلومات المنتج > المنتجات > أصول المنتجات‬‏‎**.</span><span class="sxs-lookup"><span data-stu-id="d3d40-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="d3d40-109">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d3d40-109">Click **New**.</span></span>
3. <span data-ttu-id="d3d40-110">في الحقل **رقم المنتج**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d3d40-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="d3d40-111">يجب أن يكون الرقم فريدًا.</span><span class="sxs-lookup"><span data-stu-id="d3d40-111">The number must be unique.</span></span> <span data-ttu-id="d3d40-112">يمكن تعيين تسلسل رقمي في الحقل **رقم المنتج**.</span><span class="sxs-lookup"><span data-stu-id="d3d40-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="d3d40-113">في هذه الحالة، لا يحتاج المستخدم إلى إدخال قيمة.</span><span class="sxs-lookup"><span data-stu-id="d3d40-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="d3d40-114">في الحقل **اسم المنتج**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d3d40-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="d3d40-115">أدخل اسمًا وصفيًا للمنتج.</span><span class="sxs-lookup"><span data-stu-id="d3d40-115">Enter a descriptive product name.</span></span> <span data-ttu-id="d3d40-116">يتم تعيين القيمة إلى اسم البحث بشكل افتراضي، ولكن يمكن تغييرها من قِبل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="d3d40-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="d3d40-117">في الحقل **مجموعة أبعاد المنتج**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d3d40-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="d3d40-118">تحدد مجموعة أبعاد المنتج أي واحد من الأبعاد الأربعة للمنتجات التي يمكن استخدامها لإنشاء متغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="d3d40-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="d3d40-119">يستخدم هذا المثال مجموعة مع اللون والحجم.</span><span class="sxs-lookup"><span data-stu-id="d3d40-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="d3d40-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d3d40-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="d3d40-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d3d40-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="d3d40-122">تقنية **تقنية التكوين** الافتراضية هي "المتغير المعرف مسبقًا".</span><span class="sxs-lookup"><span data-stu-id="d3d40-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="d3d40-123">سيتم استخدامها لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="d3d40-123">This will be used for this example.</span></span>
8. <span data-ttu-id="d3d40-124">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3d40-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="d3d40-125">تحديد مجموعات أبعاد المنتجات</span><span class="sxs-lookup"><span data-stu-id="d3d40-125">Select product dimension groups</span></span>
1. <span data-ttu-id="d3d40-126">في الحقل **مجموعة اللون‬‬‬‬**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d3d40-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="d3d40-127">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d3d40-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d3d40-128">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d3d40-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d3d40-129">في الحقل **حجم المجموعة‬‬‬‬**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d3d40-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d3d40-130">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d3d40-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="d3d40-131">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d3d40-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="d3d40-132">إضافة مجموعات الأبعاد</span><span class="sxs-lookup"><span data-stu-id="d3d40-132">Add dimension groups</span></span>
1. <span data-ttu-id="d3d40-133">في **جزء الإجراءات**، انقر فوق **المنتج**.</span><span class="sxs-lookup"><span data-stu-id="d3d40-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="d3d40-134">انقر فوق **مجموعات الأبعاد** لفتح مربع الحوار المنسدل.</span><span class="sxs-lookup"><span data-stu-id="d3d40-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="d3d40-135">في الحقل **مجموعة أبعاد التخزين**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d3d40-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="d3d40-136">تساعدك أبعاد التخزين على التحكم في كيفية تخزين الأصناف وأخذها من المخزون.</span><span class="sxs-lookup"><span data-stu-id="d3d40-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="d3d40-137">على سبيل المثال، يمكنك تضمين بُعد التخزين الموقع والمستودع.</span><span class="sxs-lookup"><span data-stu-id="d3d40-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="d3d40-138">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d3d40-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d3d40-139">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d3d40-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d3d40-140">في الحقل **مجموعة أبعاد التعقب**‬، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d3d40-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="d3d40-141">تحدد مجموعة بُعد التعقب أبعاد التعقب التي يمكنك إضافتها إلى منتج.</span><span class="sxs-lookup"><span data-stu-id="d3d40-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="d3d40-142">على سبيل المثال، يُستخدم رقم الدفعة والرقم المسلسل لتعقب أصناف المخزون.</span><span class="sxs-lookup"><span data-stu-id="d3d40-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="d3d40-143">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d3d40-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d3d40-144">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d3d40-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d3d40-145">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3d40-145">Click **OK**.</span></span>
10. <span data-ttu-id="d3d40-146">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d3d40-146">Click **Save**.</span></span>
11. <span data-ttu-id="d3d40-147">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d3d40-147">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]