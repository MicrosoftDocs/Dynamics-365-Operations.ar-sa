---
title: تخطيط الإنتاج
description: يصف هذا الموضوع التخطيط للإنتاج ويوضح كيفيه تعديل أوامر الإنتاج المخططة باستخدام تحسين التخطيط.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eda22aa6f1e8d665d8ef390f24b247a76d4c2956
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992385"
---
# <a name="production-planning"></a><span data-ttu-id="d2bff-103">تخطيط الإنتاج</span><span class="sxs-lookup"><span data-stu-id="d2bff-103">Production planning</span></span>

<span data-ttu-id="d2bff-104">تعتمد أمثليه التخطيط سيناريوهات إنتاج متعددة.</span><span class="sxs-lookup"><span data-stu-id="d2bff-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="d2bff-105">إذا كنت تقوم بالترحيل من مشغل التخطيط الرئيسي المضمن الموجود ، فمن المهم ان تكون علي علم ببعض السلوك المتغير.</span><span class="sxs-lookup"><span data-stu-id="d2bff-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<!-- The following video gives a short introduction to some of the current capabilities. 
KFM: Link to video for production functionality, coming soon... -->

## <a name="planned-production-orders"></a><span data-ttu-id="d2bff-106">أوامر الإنتاج المخططة</span><span class="sxs-lookup"><span data-stu-id="d2bff-106">Planned production orders</span></span>

<span data-ttu-id="d2bff-107">عندما يقوم التخطيط الرئيسي بإنشاء أوامر مخططه لاستيفاء المتطلبات، يتم تحديد نوع الأمر بقيمه حقل **نوع الأمر المخطط**.</span><span class="sxs-lookup"><span data-stu-id="d2bff-107">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="d2bff-108">إذا تم تعيين حقل **نوع الأمر المخطط** علي *الإنتاج*، سيتم إنشاء أوامر الإنتاج المخططة.</span><span class="sxs-lookup"><span data-stu-id="d2bff-108">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="d2bff-109">تشتمل أوامر الإنتاج المخططة هذه علي معلومات حول قائمة مكونات الصنف (BOM) ومعرف المسار من اعداد الإنتاج ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="d2bff-109">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="d2bff-110">المتطلبات من قوائم مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="d2bff-110">Requirements from BOMs</span></span>

<span data-ttu-id="d2bff-111">يتم اقتران معلومات قائمة مكونات الصنف اثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="d2bff-111">BOM information is honored during master planning.</span></span> <span data-ttu-id="d2bff-112">يتضمن إخراج الخطة توريد المواد لتغطيه طلب المواد ذات الصلة للإنتاج.</span><span class="sxs-lookup"><span data-stu-id="d2bff-112">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="d2bff-113">واثناء التخطيط الرئيسي، يتم استخدام قائمة مكونات الصنف النشطة الحالية لتحديد المواد المطلوبة للإنتاج.</span><span class="sxs-lookup"><span data-stu-id="d2bff-113">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="d2bff-114">يتم اجراء هذه الخطوة من خلال كافة مستويات بنيه قائمة مكونات الصنف المرتبطة بامر الإنتاج المطلوب.</span><span class="sxs-lookup"><span data-stu-id="d2bff-114">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="d2bff-115">يتم استيفاء متطلبات المواد باستخدام المخزون الفعلي المتاح، والتوريد القائم علي الطلب الموجود، والأوامر المخططة المعتمدة.</span><span class="sxs-lookup"><span data-stu-id="d2bff-115">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="d2bff-116">إذا كانت هناك مواد اضافيه مطلوبه في اي مكان، سيتم إنشاء أمر مخطط لتغطيه الطلب.</span><span class="sxs-lookup"><span data-stu-id="d2bff-116">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="d2bff-117">الجدولة اثناء التاكيد</span><span class="sxs-lookup"><span data-stu-id="d2bff-117">Scheduling during firming</span></span>

<span data-ttu-id="d2bff-118">تشتمل أوامر الإنتاج المخططة علي معرف المسار المطلوب لجدوله الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="d2bff-118">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="d2bff-119">ومع ذلك ، يكون اعتماد الجدولة اثناء تشغيل التخطيط للأوامر المخططة معلقا.</span><span class="sxs-lookup"><span data-stu-id="d2bff-119">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="d2bff-120">يتم استخدام معرف المسار لجدوله أوامر الإنتاج المخططة اثناء التاكيد.</span><span class="sxs-lookup"><span data-stu-id="d2bff-120">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="d2bff-121">التالي، يمكن ان يختلف زمن وصول البضاعة في أوامر الإنتاج المخططة عن زمن وصول البضاعة المجدولة وأوامر الإنتاج المؤكدة التي يتم إنشاؤها منها، كما هو موضح هنا:</span><span class="sxs-lookup"><span data-stu-id="d2bff-121">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="d2bff-122">**أمر الإنتاج المخطط** - يكون زمن وصول البضاعة مستندا إلى زمن وصول البضاعة الثابت من المنتج الذي تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="d2bff-122">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="d2bff-123">**أمر الإنتاج المؤكد** – يعتمد زمن وصول البضاعة علي الجدولة التي تستخدم معلومات المسار وقيود الموارد ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="d2bff-123">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="d2bff-124">للحصول علي مزيد من المعلومات حول أتاحه الميزات المتوقعة، راجع [التخطيط لملائمة تحسين الأداء](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d2bff-124">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="d2bff-125">إذا كنت تعتمد علي وظيفة الإنتاج التي لم تكن متوفرة بعد لتحسين التخطيط، يمكنك الاستمرار في استخدام مشغل التخطيط الرئيسي المضمن.</span><span class="sxs-lookup"><span data-stu-id="d2bff-125">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="d2bff-126">الاستثناء غير مطلوب.</span><span class="sxs-lookup"><span data-stu-id="d2bff-126">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="d2bff-127">التأخيرات</span><span class="sxs-lookup"><span data-stu-id="d2bff-127">Delays</span></span>

<span data-ttu-id="d2bff-128">إذا كان زمن وصول البضاعة المطلوبة أطول من الفترة بين تاريخ اليوم وتاريخ طلب المواد، سيتم تاجيل الأمر المخطط للمادة المطلوبة وأمر الإنتاج المرتبط.</span><span class="sxs-lookup"><span data-stu-id="d2bff-128">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="d2bff-129">بالنسبة للأوامر المخططة، يتم حساب التاخير (بالأيام) استنادا إلى زمن وصول البضاعة من المنتج الذي تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="d2bff-129">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="d2bff-130">يتم بعد ذلك نشر معلومات التاخير من خلال كافة مستويات بنيه قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="d2bff-130">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="d2bff-131">التالي، يمكنك اتباع تاثير المادة الخام المؤجلة علي النحو الآخر لأمر توريد العميل.</span><span class="sxs-lookup"><span data-stu-id="d2bff-131">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="d2bff-132">تعديل الأوامر المخططة</span><span class="sxs-lookup"><span data-stu-id="d2bff-132">Modifying planned orders</span></span>

<span data-ttu-id="d2bff-133">عند تغيير المعلومات في أمر مخطط ، تظهر الرسالة التالية: "لاحظ ان تاثير التغييرات اليدوية علي الأوامر المخططة لن يظهر في باقي الخطة حتى يتم تشغيل التخطيط الرئيسي التالي."</span><span class="sxs-lookup"><span data-stu-id="d2bff-133">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="d2bff-134">إذا كنت ترغب في تغيير المعلومات في أمر مخطط ومراجعه التاثير علي متطلبات المواد ذات الصلة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d2bff-134">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="d2bff-135">تحديث الأمر المخطط.</span><span class="sxs-lookup"><span data-stu-id="d2bff-135">Update the planned order.</span></span>
2. <span data-ttu-id="d2bff-136">الموافقة على الأمر المخطط.</span><span class="sxs-lookup"><span data-stu-id="d2bff-136">Approve the planned order.</span></span>
3. <span data-ttu-id="d2bff-137">تشغيل التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="d2bff-137">Run master planning.</span></span>

<span data-ttu-id="d2bff-138">عند تشغيل التخطيط الرئيسي، يجب عدم استخدام عوامل التصفية في حاله تضمين أوامر الإنتاج المخططة.</span><span class="sxs-lookup"><span data-stu-id="d2bff-138">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="d2bff-139">لمزيد من المعلومات، انظر القسم [عوامل التصفية](#filters) لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="d2bff-139">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="d2bff-140">في حاله تغيير تاريخ التسليم الخاص بالأمر المخطط إلى تاريخ لاحق، فقد يكون الطلب مثبتًا مقابل أمر مخطط جديد.</span><span class="sxs-lookup"><span data-stu-id="d2bff-140">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="d2bff-141">يحدث هذا السلوك عندما يتسبب تاريخ التوريد الجديد في حدوث تاخير لطلب مثبت ولكن وفقا لإعدادات زمن وصول البضاعة، يمكن تجنب التاخير.</span><span class="sxs-lookup"><span data-stu-id="d2bff-141">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="d2bff-142">صفحه تحديد إجمالي المكونات</span><span class="sxs-lookup"><span data-stu-id="d2bff-142">Explosion page</span></span>

<span data-ttu-id="d2bff-143">يمكنك استخدام صفحه **تحديد إجمالي** المكونات المطلوبة لتحليل الطلب المطلوب لأمر إنتاج معين أو أمر إنتاج مخطط، والتغطية ذات الصلة، ومعلومات تثبيت السعر.</span><span class="sxs-lookup"><span data-stu-id="d2bff-143">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="d2bff-144">يتم تحديث المعلومات الموجودة في صفحه **تحديد إجمالي المكونات** اثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="d2bff-144">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="d2bff-145">لا يمكنك تحديث المعلومات مباشره من صفحه **تحديد إجمالي المكونات** المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="d2bff-145">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="d2bff-146">عوامل التصفية</span><span class="sxs-lookup"><span data-stu-id="d2bff-146">Filters</span></span>

<span data-ttu-id="d2bff-147">بالنسبة لسيناريوهات التخطيط التي تتضمن الإنتاج، نوصي بتجنب تشغيل التخطيط الرئيسي المصفي.</span><span class="sxs-lookup"><span data-stu-id="d2bff-147">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="d2bff-148">للتاكد من ان أمثليه التخطيط لها المعلومات اللازمة لحساب النتيجة الصحيحة، يجب تضمين كافة المنتجات التي لديها إيه علاقة بالمنتجات في بنيه قائمة مكونات الصنف بالكامل للأمر المخطط.</span><span class="sxs-lookup"><span data-stu-id="d2bff-148">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="d2bff-149">علي الرغم من ان العناصر التابعة التابعة يتم الكشف عنها تلقائيا وتضمينها في التخطيط الرئيسي يتم تشغيلها عند استخدام مشغل التخطيط الرئيسي المضمن، فان تحسين التخطيط لا ينفذ هذا الاجراء.</span><span class="sxs-lookup"><span data-stu-id="d2bff-149">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="d2bff-150">علي سبيل المثال، إذا تم استخدام المسمار الواحد من بنيه شجره المواد للمنتج A أيضا لإنتاج المنتج B، يجب تضمين كافة المنتجات الموجودة في بنيه شجره المواد الخاصة بالمنتجات A وB في عامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="d2bff-150">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="d2bff-151">ونظرا لأنها قد تكون معقده جدا لضمان ان كافة المنتجات تعتبر جزءا من عامل التصفية، نوصي بتجنب تشغيل التخطيط الرئيسي الذي تم تصفيته عند تضمين أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="d2bff-151">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>
