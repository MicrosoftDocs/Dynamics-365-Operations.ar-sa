---
title: إنشاء أصل منتج
description: أنشئ أصل المنتج للمتغيرات المعرفة مسبقًا.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae2290cf8da4387155de7790dd3db88b34eb6e96
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150069"
---
# <a name="create-a-product-master"></a><span data-ttu-id="bb44a-103">إنشاء أصل منتج</span><span class="sxs-lookup"><span data-stu-id="bb44a-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bb44a-104">أنشئ أصل المنتج للمتغيرات المعرفة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="bb44a-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="bb44a-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="bb44a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bb44a-106">هذا الإجراء مخصص لمصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="bb44a-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="bb44a-107">إنشاء أصل منتج جديد</span><span class="sxs-lookup"><span data-stu-id="bb44a-107">Create a new product master</span></span>
1. <span data-ttu-id="bb44a-108">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة معلومات المنتج > المنتجات > أصول المنتجات‬‏‎**.</span><span class="sxs-lookup"><span data-stu-id="bb44a-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="bb44a-109">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="bb44a-109">Click **New**.</span></span>
3. <span data-ttu-id="bb44a-110">في الحقل **رقم المنتج**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bb44a-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="bb44a-111">يجب أن يكون الرقم فريدًا.</span><span class="sxs-lookup"><span data-stu-id="bb44a-111">The number must be unique.</span></span> <span data-ttu-id="bb44a-112">يمكن تعيين تسلسل رقمي في الحقل **رقم المنتج**.</span><span class="sxs-lookup"><span data-stu-id="bb44a-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="bb44a-113">في هذه الحالة، لا يحتاج المستخدم إلى إدخال قيمة.</span><span class="sxs-lookup"><span data-stu-id="bb44a-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="bb44a-114">في الحقل **اسم المنتج**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bb44a-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="bb44a-115">أدخل اسمًا وصفيًا للمنتج.</span><span class="sxs-lookup"><span data-stu-id="bb44a-115">Enter a descriptive product name.</span></span> <span data-ttu-id="bb44a-116">يتم تعيين القيمة إلى اسم البحث بشكل افتراضي، ولكن يمكن تغييرها من قِبل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="bb44a-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="bb44a-117">في الحقل **مجموعة أبعاد المنتج**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="bb44a-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="bb44a-118">تحدد مجموعة أبعاد المنتج أي واحد من الأبعاد الأربعة للمنتجات التي يمكن استخدامها لإنشاء متغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="bb44a-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="bb44a-119">يستخدم هذا المثال مجموعة مع اللون والحجم.</span><span class="sxs-lookup"><span data-stu-id="bb44a-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="bb44a-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="bb44a-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="bb44a-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bb44a-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="bb44a-122">تقنية **تقنية التكوين** الافتراضية هي "المتغير المعرف مسبقًا".</span><span class="sxs-lookup"><span data-stu-id="bb44a-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="bb44a-123">سيتم استخدامها لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="bb44a-123">This will be used for this example.</span></span>
8. <span data-ttu-id="bb44a-124">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bb44a-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="bb44a-125">تحديد مجموعات أبعاد المنتجات</span><span class="sxs-lookup"><span data-stu-id="bb44a-125">Select product dimension groups</span></span>
1. <span data-ttu-id="bb44a-126">في الحقل **مجموعة اللون‬‬‬‬**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="bb44a-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="bb44a-127">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="bb44a-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="bb44a-128">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bb44a-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="bb44a-129">في الحقل **حجم المجموعة‬‬‬‬**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="bb44a-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="bb44a-130">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="bb44a-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="bb44a-131">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bb44a-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="bb44a-132">إضافة مجموعات الأبعاد</span><span class="sxs-lookup"><span data-stu-id="bb44a-132">Add dimension groups</span></span>
1. <span data-ttu-id="bb44a-133">في **جزء الإجراءات**، انقر فوق **المنتج**.</span><span class="sxs-lookup"><span data-stu-id="bb44a-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="bb44a-134">انقر فوق **مجموعات الأبعاد** لفتح مربع الحوار المنسدل.</span><span class="sxs-lookup"><span data-stu-id="bb44a-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="bb44a-135">في الحقل **مجموعة أبعاد التخزين**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="bb44a-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="bb44a-136">تساعدك أبعاد التخزين على التحكم في كيفية تخزين الأصناف وأخذها من المخزون.</span><span class="sxs-lookup"><span data-stu-id="bb44a-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="bb44a-137">على سبيل المثال، يمكنك تضمين بُعد التخزين الموقع والمستودع.</span><span class="sxs-lookup"><span data-stu-id="bb44a-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="bb44a-138">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="bb44a-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="bb44a-139">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bb44a-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="bb44a-140">في الحقل **مجموعة أبعاد التعقب**‬، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="bb44a-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="bb44a-141">تحدد مجموعة بُعد التعقب أبعاد التعقب التي يمكنك إضافتها إلى منتج.</span><span class="sxs-lookup"><span data-stu-id="bb44a-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="bb44a-142">على سبيل المثال، يُستخدم رقم الدفعة والرقم المسلسل لتعقب أصناف المخزون.</span><span class="sxs-lookup"><span data-stu-id="bb44a-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="bb44a-143">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="bb44a-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="bb44a-144">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bb44a-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="bb44a-145">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bb44a-145">Click **OK**.</span></span>
10. <span data-ttu-id="bb44a-146">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bb44a-146">Click **Save**.</span></span>
11. <span data-ttu-id="bb44a-147">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bb44a-147">Close the page.</span></span>

