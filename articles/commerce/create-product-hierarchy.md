---
title: إنشاء تدرج هرمي لمنتج جديد
description: يوضح هذا الموضوع كيفية إنشاء تدرج هرمي لمنتج جديد في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 724ec2e5af7837d574298d662911cd9c6ee9e9f2
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070411"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="2340a-103">إنشاء تدرج هرمي لمنتج جديد</span><span class="sxs-lookup"><span data-stu-id="2340a-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2340a-104">يوضح هذا الموضوع كيفية إنشاء تدرج هرمي لمنتج جديد في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2340a-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2340a-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="2340a-105">Overview</span></span>

<span data-ttu-id="2340a-106">يدعم Dynamics 365 Commerce عدة قنوات بيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="2340a-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="2340a-107">وتتضمن قنوات البيع بالتجزئة هذه المتاجر على إنترنت، ومراكز الاتصال، ومتاجر البيع بالتجزئة (تعرف أيضًا بالمتاجر التقليدية).</span><span class="sxs-lookup"><span data-stu-id="2340a-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="2340a-108">يمكن أن يكون لكل قناة متجر للبيع بالتجزئة طرق الدفع ومجموعات الأسعار وسجلات نقطة البيع (POS) وحسابات الإيرادات والمصروفات وفريق العمل الخاص بها.</span><span class="sxs-lookup"><span data-stu-id="2340a-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="2340a-109">ويجب إعداد كل هذه العناصر قبل إمكانية إنشاء قناة لمتجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="2340a-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="2340a-110">يتم استخدام التدرج الهرمي لمنتج تجاري لتحديد التدرج الهرمي الشامل للمنتجات لمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="2340a-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="2340a-111">ويمكنك استخدام التدرج الهرمي لمنتج تجاري للترويج للبضائع والتسعير والعروض وإعداد التقارير وتخطيط الفرز.</span><span class="sxs-lookup"><span data-stu-id="2340a-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="2340a-112">يمكن تعيين تدرج هرمي واحد للمنتجات التجارية لكل مؤسسة.</span><span class="sxs-lookup"><span data-stu-id="2340a-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="2340a-113">إنشاء تدرج هرمي لمنتج وتكوينه</span><span class="sxs-lookup"><span data-stu-id="2340a-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="2340a-114">لإنشاء تدرج هرمي للمنتجات التجارية وتكوينه، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2340a-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="2340a-115">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> المنتجات والفئات \> التدرج الهرمي للمنتج التجاري**.</span><span class="sxs-lookup"><span data-stu-id="2340a-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="2340a-116">في حالة عدم وجود تدرج هرمي بعد، في **جزء الإجراء**، حدد **جديد** لإنشاء جذر التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="2340a-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="2340a-117">ضمن **عام**:</span><span class="sxs-lookup"><span data-stu-id="2340a-117">Under **General**:</span></span>
    1. <span data-ttu-id="2340a-118">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="2340a-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="2340a-119">في مربع **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="2340a-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="2340a-120">في المربع **الاسم المألوف**، أدخل اسمًا مألوفًا.</span><span class="sxs-lookup"><span data-stu-id="2340a-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="2340a-121">عيِّن الخيار **نشط** على القيمة **نعم**.</span><span class="sxs-lookup"><span data-stu-id="2340a-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="2340a-122">إضافة عقد التدرج الهرمي</span><span class="sxs-lookup"><span data-stu-id="2340a-122">Add hierarchy nodes</span></span>

<span data-ttu-id="2340a-123">لإضافة عقد التدرج الهرمي، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="2340a-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="2340a-124">في جزء الإجراءات، حدد **تحرير التدرج الهرمي للفئات**.</span><span class="sxs-lookup"><span data-stu-id="2340a-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="2340a-125">حدد العقدة الأصل التي ترغب في إضافة عقدة جديدة إليها، ثم حدد **عقدة فئة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="2340a-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="2340a-126">في القسم **عام** أدخل **اسم** و**وصف** و**اسم مألوف** و**كلمات أساسية**.</span><span class="sxs-lookup"><span data-stu-id="2340a-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="2340a-127">ضمن **عام**:</span><span class="sxs-lookup"><span data-stu-id="2340a-127">Under **General**:</span></span>
    1. <span data-ttu-id="2340a-128">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="2340a-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="2340a-129">في مربع **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="2340a-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="2340a-130">في المربع **الاسم المألوف**، أدخل اسمًا مألوفًا.</span><span class="sxs-lookup"><span data-stu-id="2340a-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="2340a-131">في المربع**الكلمات الأساسية**، أدخل الكلمات الأساسية ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="2340a-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="2340a-132">في المربع **ترتيب العرض**، أدخل رقمًا لترتيب العرض (اختياري).</span><span class="sxs-lookup"><span data-stu-id="2340a-132">In the **Display order**box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="2340a-133">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2340a-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="2340a-134">كرر الخطوات المذكورة أعلاه لإضافة عقد إضافية.</span><span class="sxs-lookup"><span data-stu-id="2340a-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="2340a-135">توضح الصورة التالية إنشاء عقدة تدرج هرمي لمنتج جديد.</span><span class="sxs-lookup"><span data-stu-id="2340a-135">The following image shows the creation of a new product hierarchy node.</span></span>

![إنشاء تدرج هرمي للمنتج](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="2340a-137">إعدادات أخرى</span><span class="sxs-lookup"><span data-stu-id="2340a-137">Other settings</span></span>

<span data-ttu-id="2340a-138">يمكن أيضًا تعيين مجموعات سمات الفئة لكل مجموعة كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="2340a-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="2340a-139">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2340a-139">Additional resources</span></span>

[<span data-ttu-id="2340a-140">التدرجات الهرمية لـ ‎commerce</span><span class="sxs-lookup"><span data-stu-id="2340a-140">commerce hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="2340a-141">إدارة المنتجات وفئات المنتجات</span><span class="sxs-lookup"><span data-stu-id="2340a-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="2340a-142">تغيير ترتيب الفرز لكيانات ترويج البضائع</span><span class="sxs-lookup"><span data-stu-id="2340a-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)