--- 
title: "إنشاء حالة دورة حياة منتج افتراضية"
description: "يُظهر هذا الإجراء كيفية إنشاء حالة دورة حياة منتج افتراضية بالإضافة إلى كيفية إقران الحالة الافتراضية مع المنتجات الصادرة."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d445ea2f2362f146a1e3e7bcf747898dc2cc89ba
ms.openlocfilehash: 06a6c7c8fa767edf6fdf50c3c971b6d767f8755f
ms.contentlocale: ar-sa
ms.lasthandoff: 02/08/2018

---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="cc5ab-103">إنشاء حالة دورة حياة منتج افتراضية</span><span class="sxs-lookup"><span data-stu-id="cc5ab-103">Create a default product lifecycle state</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc5ab-104">يُظهر هذا الإجراء كيفية إنشاء حالة دورة حياة منتج افتراضية بالإضافة إلى كيفية إقران الحالة الافتراضية مع المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="cc5ab-105">إنشاء حالة دورة حياة افتراضية</span><span class="sxs-lookup"><span data-stu-id="cc5ab-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="cc5ab-106">انتقل إلى إدارة معلومات المنتج > الإعداد > حالة دورة حياة المنتج.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="cc5ab-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cc5ab-107">Click New.</span></span>
3. <span data-ttu-id="cc5ab-108">في حقل "الحالة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="cc5ab-109">حدد "نعم" في حقل "الإعداد الافتراضي عند إصدار منتج لكيان قانوني‬".‬</span><span class="sxs-lookup"><span data-stu-id="cc5ab-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="cc5ab-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="cc5ab-111">حدد "لا" في حقل "نشط للتخطيط‬".</span><span class="sxs-lookup"><span data-stu-id="cc5ab-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="cc5ab-112">إذا لم يكن من الضروري تضمين منتج جديد صادر في التخطيط الرئيسي‬‏‫، فحدد "لا".</span><span class="sxs-lookup"><span data-stu-id="cc5ab-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="cc5ab-113">أما إذا كان يجب تضمينه في التخطيط الرئيسي، فاترك عنصر التحكم معينًا إلى قيمته الافتراضية "نعم".</span><span class="sxs-lookup"><span data-stu-id="cc5ab-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="cc5ab-114">إنشاء منتج جديد صادر</span><span class="sxs-lookup"><span data-stu-id="cc5ab-114">Create a new released product</span></span>
1. <span data-ttu-id="cc5ab-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-115">Close the page.</span></span>
2. <span data-ttu-id="cc5ab-116">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="cc5ab-117">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cc5ab-117">Click New.</span></span>
4. <span data-ttu-id="cc5ab-118">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="cc5ab-119">في الحقل "اسم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="cc5ab-120">في الحقل "اسم البحث‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="cc5ab-121">في الحقل "مجموعة النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="cc5ab-122">في حقل "مجموعة الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="cc5ab-123">في الحقل "مجموعة بُعد التخزين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="cc5ab-124">في الحقل "مجموعة بُعد التعقب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="cc5ab-125">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="cc5ab-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="cc5ab-126">دورة حياة المنتج الافتراضية عبارة عن تعريف عمومي.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="cc5ab-127">تغيير المنتج إلى حالة نشطة</span><span class="sxs-lookup"><span data-stu-id="cc5ab-127">Change the product to an active state</span></span>
1. <span data-ttu-id="cc5ab-128">في الحقل "حالة دورة حياة المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="cc5ab-129">لنفترض أنك قمت بإعداد حالة نشطة، يمكنك الآن تحديد الحالة النشطة للسماح بأن يتم استخدام المنتج في الحساب على مستوى التخطيط الرئيسي وقائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="cc5ab-130">من الواضح أن هذا الأمر يعتبر منطقيًا إذا كانت جميع تفاصيل المنتج المطلوبة للتخطيط المتناسق محددة.</span><span class="sxs-lookup"><span data-stu-id="cc5ab-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  


