---
title: "أكواد الأسباب لجرد المخزون"
description: "يصف هذا الموضوع كيفية إعداد وتطبيق أكواد الأسباب لمهام الجرد."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fe01425fa236655731e6e0723f3a1e57c05035cc
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="505f3-103">أكواد الأسباب لجرد المخزون</span><span class="sxs-lookup"><span data-stu-id="505f3-103">Reason codes for inventory counting</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="505f3-104">تتيح لك أكواد الأسباب تحليل نتائج عملية الجرد وأي تناقضات تحدث أثناء العملية.</span><span class="sxs-lookup"><span data-stu-id="505f3-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="505f3-105">يمكنك تحديد سبب القيام بالجرد، مثل بالتة مكسورة أو تعديل مخزون يستند إلى نماذج المخزون.</span><span class="sxs-lookup"><span data-stu-id="505f3-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="505f3-106">التوصيات</span><span class="sxs-lookup"><span data-stu-id="505f3-106">Recommendation</span></span>

<span data-ttu-id="505f3-107">قبل إعداد النظام، نوصي بأن تقوم بتحديد استراتيجية للعمل مع أكواد الأسباب.</span><span class="sxs-lookup"><span data-stu-id="505f3-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="505f3-108">على سبيل المثال، حاول الإجابة عن الأسئلة التالية:</span><span class="sxs-lookup"><span data-stu-id="505f3-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="505f3-109">هل يجب أن تكون أكواد الأسباب إلزامية في المستودعات؟</span><span class="sxs-lookup"><span data-stu-id="505f3-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="505f3-110">هل يجب أن تكون أكواد الأسباب إلزامية أو اختيارية في بعض الأصناف؟</span><span class="sxs-lookup"><span data-stu-id="505f3-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="505f3-111">كم عدد أكواد الأسباب التي تتطلبها؟</span><span class="sxs-lookup"><span data-stu-id="505f3-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="505f3-112">كيف يجب على مستخدمي الماسحات الضوئية للأكواد الشريطية استخدام أكواد الأسباب؟</span><span class="sxs-lookup"><span data-stu-id="505f3-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="505f3-113">هل يجب أن تكون أكواد الأسباب محددة مسبقًا أو إلزامية أو غير قابلة للتحرير؟</span><span class="sxs-lookup"><span data-stu-id="505f3-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="505f3-114">هل يتطلب العاملون في المستودع سلوك كود سبب مختلفًا في الماسحات الضوئية للأجهزة المحمولة؟</span><span class="sxs-lookup"><span data-stu-id="505f3-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="505f3-115">إذا كانت الإجابة بنعم، يمكنك إنشاء مزيد من أصناف القائمة وتعيينها إلى أشخاص مختلفين.</span><span class="sxs-lookup"><span data-stu-id="505f3-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="505f3-116">مواضع تطبيق أكواد الأسباب</span><span class="sxs-lookup"><span data-stu-id="505f3-116">Where reason codes apply</span></span>

<span data-ttu-id="505f3-117">يمكنك إنشاء العديد من سياسات أكواد الأسباب، ويمكن لكل سياسة كود سبب أن تشتمل على سياستي أكواد أسباب للجرد.</span><span class="sxs-lookup"><span data-stu-id="505f3-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="505f3-118">يمكن استخدام سياسات أكواد أسباب الجرد على مستوى المستودع أو مستوى الصنف.</span><span class="sxs-lookup"><span data-stu-id="505f3-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="505f3-119">إعداد سياسات أكواد الأسباب</span><span class="sxs-lookup"><span data-stu-id="505f3-119">Set up reason code policies</span></span>

1. <span data-ttu-id="505f3-120">حدد **إدارة المخزون**\>**الإعداد**\>**المخزون**\>**سياسات أكواد أسباب الجرد**، وقم بإنشاء سياسة كود سبب جديدة.</span><span class="sxs-lookup"><span data-stu-id="505f3-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="505f3-121">في حقل **نوع كود سبب الجرد**، حدد إما **إلزامي** أو **اختياري** لتحديد ما إذا كان يجب أن يكون تحديد كود سبب خيارًا اختياريًا أو إلزاميًا في أحد دفاتر يومية الجرد التالية:</span><span class="sxs-lookup"><span data-stu-id="505f3-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="505f3-122">الجرد الدوري (الجهاز المحمول)</span><span class="sxs-lookup"><span data-stu-id="505f3-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="505f3-123">الجرد الفوري (الجهاز المحمول)</span><span class="sxs-lookup"><span data-stu-id="505f3-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="505f3-124">جرد الحدود (الجهاز المحمول)</span><span class="sxs-lookup"><span data-stu-id="505f3-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="505f3-125">التسوية الواردة (الجهاز المحمول)</span><span class="sxs-lookup"><span data-stu-id="505f3-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="505f3-126">التسوية الصادرة (الجهاز المحمول)</span><span class="sxs-lookup"><span data-stu-id="505f3-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="505f3-127">دفتر يومية الجرد (عميل غني)</span><span class="sxs-lookup"><span data-stu-id="505f3-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="505f3-128">يمكنك أيضًا إعداد أكواد الأسباب للمستودعات الفردية وللمنتجات.</span><span class="sxs-lookup"><span data-stu-id="505f3-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="505f3-129">يمكن لإعداد كود السبب للمنتجات تجاهل الإعداد للمستودعات.</span><span class="sxs-lookup"><span data-stu-id="505f3-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="505f3-130">أكواد الأسباب الإلزامية</span><span class="sxs-lookup"><span data-stu-id="505f3-130">Mandatory reason codes</span></span>

<span data-ttu-id="505f3-131">في حالة تعيين معلمة **إلزامية** في التكوين الخاص بأكواد الأسباب للمستودعات أو للأصناف، لا يمكن إكمال دفتر يومية الجرد وإغلاقه حتى يتوفر كود سبب.</span><span class="sxs-lookup"><span data-stu-id="505f3-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="505f3-132">إعداد أكواد الأسباب للمستودعات</span><span class="sxs-lookup"><span data-stu-id="505f3-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="505f3-133">حدد **إدارة المخزون** \> **الإعداد** \> **تصنيف المخزون** \> **المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="505f3-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="505f3-134">في علامة التبويب **المستودع**، في حقل **سياسة كود سبب الجرد**، حدد أحد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="505f3-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="505f3-135">**فارغ** - يتم استخدام المعلمة التي يتم إعدادها للصنف لتحديد ما إذا كانت دفاتر يومية الجرد إلزامية للمنتج.</span><span class="sxs-lookup"><span data-stu-id="505f3-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="505f3-136">**إلزامي** - كود سبب مطلوب دائمًا في دفاتر يومية الجرد للمستودع.</span><span class="sxs-lookup"><span data-stu-id="505f3-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="505f3-137">**اختياري** - كود سبب غير مطلوب دائمًا في دفاتر يومية الجرد للمستودع.</span><span class="sxs-lookup"><span data-stu-id="505f3-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="505f3-138">إعداد أكواد الأسباب للمنتجات</span><span class="sxs-lookup"><span data-stu-id="505f3-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="505f3-139">حدد **إدارة معلومات المنتج** \> **المنتجات** \> **المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="505f3-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="505f3-140">في علامة التبويب **المنتج**، حدد **سياسة كود سبب الجرد**، ثم حدد أحد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="505f3-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="505f3-141">**فارغ** - يتم استخدام المعلمة التي يتم إعدادها للمستودع لتحديد ما إذا كانت دفاتر يومية الجرد إلزامية للمنتج.</span><span class="sxs-lookup"><span data-stu-id="505f3-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="505f3-142">**إلزامي** - كود سبب مطلوب دائمًا في دفاتر يومية الجرد للمنتج.</span><span class="sxs-lookup"><span data-stu-id="505f3-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="505f3-143">يتجاوز هذا الإعداد أي إعداد كود سبب عند مستوى المستودع.</span><span class="sxs-lookup"><span data-stu-id="505f3-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="505f3-144">**اختياري** - كود سبب غير مطلوب دائمًا في دفاتر يومية الجرد للمنتج.</span><span class="sxs-lookup"><span data-stu-id="505f3-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="505f3-145">يتجاوز هذا الإعداد أي إعداد كود سبب عند مستوى المستودع.</span><span class="sxs-lookup"><span data-stu-id="505f3-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="505f3-146">استخدم أكواد الأسباب في دفاتر يومية الجرد</span><span class="sxs-lookup"><span data-stu-id="505f3-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="505f3-147">في دفتر يومية جرد، يمكنك إضافة أكواد الأسباب لعدد الأنواع التالية:</span><span class="sxs-lookup"><span data-stu-id="505f3-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="505f3-148">جرد دوري</span><span class="sxs-lookup"><span data-stu-id="505f3-148">Cycle Count</span></span>
- <span data-ttu-id="505f3-149">جرد فوري</span><span class="sxs-lookup"><span data-stu-id="505f3-149">Spot Count</span></span>
- <span data-ttu-id="505f3-150">جرد الحدود</span><span class="sxs-lookup"><span data-stu-id="505f3-150">Threshold Count</span></span>
- <span data-ttu-id="505f3-151">تسوية واردة</span><span class="sxs-lookup"><span data-stu-id="505f3-151">Adjustment In</span></span>
- <span data-ttu-id="505f3-152">تسوية صادرة</span><span class="sxs-lookup"><span data-stu-id="505f3-152">Adjustment Out</span></span>

<span data-ttu-id="505f3-153">تتم إضافة أكواد الأسباب إلى بنود دفتر اليومية في دفاتر يومية الجرد من نوع **دفتر يومية الجرد**.</span><span class="sxs-lookup"><span data-stu-id="505f3-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="505f3-154">حدد **إدارة المخزون** \> **إدخالات دفتر اليومية** \> **جرد الأصناف** \> **الجرد**.</span><span class="sxs-lookup"><span data-stu-id="505f3-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="505f3-155">في تفاصيل بنود دفتر يومية الجرد، في حقل **كود سبب الجرد**، حدد أحد الخيارات.</span><span class="sxs-lookup"><span data-stu-id="505f3-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="505f3-156">عرض محفوظات الجرد كما هي مسجلة بواسطة أكواد الأسباب</span><span class="sxs-lookup"><span data-stu-id="505f3-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="505f3-157">حدد **إدارة المخزون**\>**الاستعلامات والتقارير**\>**محفوظات الجرد**، ثم في حقل **كود سبب الجرد**، اعرض محفوظات الجرد التي تم تسجيلها من خلال كود سبب.</span><span class="sxs-lookup"><span data-stu-id="505f3-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="505f3-158">استخدام كود سبب لتسوية كمية</span><span class="sxs-lookup"><span data-stu-id="505f3-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="505f3-159">في صفحة **المخزون الفعلى**، حدد **تسوية كمية**.</span><span class="sxs-lookup"><span data-stu-id="505f3-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="505f3-160">يمكنك فتح صفحة **المخزون الفعلى** بعدة طرق.</span><span class="sxs-lookup"><span data-stu-id="505f3-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="505f3-161">على سبيل المثال، حدد **إدارة المخزون** \> **الاستعلامات والتقارير** \> **المخزون الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="505f3-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="505f3-162">حدد **تسوية كمية**، ثم في حقل **كود سبب الجرد**، حدد كود سبب.</span><span class="sxs-lookup"><span data-stu-id="505f3-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="505f3-163">تكوين أكواد الأسباب لعناصر قائمة الأجهزة المحمولة</span><span class="sxs-lookup"><span data-stu-id="505f3-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="505f3-164">يمكنك تكوين أكواد الأسباب لأي نوع من الجرد على عنصر قائمة جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="505f3-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="505f3-165">يتضمن التكوين الخاص بعنصر قائمة الجهاز المحمول المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="505f3-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="505f3-166">ما إذا كان يتم إظهار كود السبب لعامل الجهاز المحمول خلال عملية الجرد.</span><span class="sxs-lookup"><span data-stu-id="505f3-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="505f3-167">كود السبب الافتراضي الذي يظهر في عنصر قائمة جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="505f3-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="505f3-168">ما إذا كان بإمكان المستخدم تحرير كود السبب.</span><span class="sxs-lookup"><span data-stu-id="505f3-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="505f3-169">إعداد أكواد الأسباب على جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="505f3-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="505f3-170">حدد **إدارة المستودعات** \> **الإعداد** \> **الجهاز المحمول** \> **عناصر الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="505f3-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="505f3-171">في علامة التبويب **الجرد الدوري**، حدد **جرد دوري**.</span><span class="sxs-lookup"><span data-stu-id="505f3-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="505f3-172">في حقل **كود السبب الافتراضي للجرد**، قم بتعيين كود السبب الافتراضي الذي يجب أن يتم تسجيله عندما يتم إجراء الجرد باستخدام عنصر قائمة جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="505f3-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="505f3-173">في حقل **عرض كود سبب الجرد**، حدد **بند** لإظهار كود السبب بعد أن يتم تسجيل كل نسبة فرق.</span><span class="sxs-lookup"><span data-stu-id="505f3-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="505f3-174">بدلاً من ذلك، حدد **إخفاء** إذا كان يجب إلا يتم إظهار كود السبب.</span><span class="sxs-lookup"><span data-stu-id="505f3-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="505f3-175">قم بتعيين خيار **تحرير كود سبب الجرد** إلى إما **نعم** أو **لا**.</span><span class="sxs-lookup"><span data-stu-id="505f3-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="505f3-176">إذا قمت بتعيين هذا الخيار **نعم**، يستطيع العامل تحرير كود السبب عندما يظهر على الجهاز المحمول خلال عملية الجرد.</span><span class="sxs-lookup"><span data-stu-id="505f3-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="505f3-177">يمكن تمكين الزر **جرد دوري**على أي عنصر قائمة جهاز محمول حيث يمكن القيام بالجرد.</span><span class="sxs-lookup"><span data-stu-id="505f3-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="505f3-178">يتضمن المثال عناصر القائمة لعمليات الجرد الفوري والعمل الموجه من قِبل المستخدم والعمل الموجه بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="505f3-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="505f3-179">الموافقات على الجرد الدوري</span><span class="sxs-lookup"><span data-stu-id="505f3-179">Cycle count approvals</span></span>

<span data-ttu-id="505f3-180">قبل أن تتم الموافقة على عملية جرد، يمكن للمستخدم تغيير كود السبب المرتبط بالحساب.</span><span class="sxs-lookup"><span data-stu-id="505f3-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="505f3-181">عندما تتم الموافقة على الحساب، يتم إدخال كود السبب في بنود دفتر يومية الجرد.</span><span class="sxs-lookup"><span data-stu-id="505f3-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="505f3-182">تعديل الموافقات على الجرد الدوري</span><span class="sxs-lookup"><span data-stu-id="505f3-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="505f3-183">حدد **إدارة المستودعات**\>**جرد دوري**\>**مراجعة عمل الجرد الدوري المعلق**.</span><span class="sxs-lookup"><span data-stu-id="505f3-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="505f3-184">حدد **جرد دوري**، ثم في حقل **كود السبب**، حدد كود سبب جديدًا.</span><span class="sxs-lookup"><span data-stu-id="505f3-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="505f3-185">تعديل عنصر قائمة الجهاز المحمول للتسوية الواردة والتسوية الصادرة</span><span class="sxs-lookup"><span data-stu-id="505f3-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="505f3-186">حدد **إدارة المستودعات**\>**الإعداد**\>**الجهاز المحمول**\>**عناصر قائمة الجهاز المحمول**، ثم قم بتحديد **التسوية الواردة والصادرة**.</span><span class="sxs-lookup"><span data-stu-id="505f3-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="505f3-187">قم بتعيين الخيار **استخدام العمل الموجود** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="505f3-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="505f3-188">في حقل **عملية إنشاء العمل**، حدد **التسوية الواردة**.</span><span class="sxs-lookup"><span data-stu-id="505f3-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="505f3-189">ستتم إضافة الحقول التالية إلى عنصر قائمة الجهاز المحمول عند تحديد **التسوية الواردة** أو **التسوية الصادرة** أثناء عملية إنشاء العمل:</span><span class="sxs-lookup"><span data-stu-id="505f3-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="505f3-190">كود سبب الجرد الافتراضي</span><span class="sxs-lookup"><span data-stu-id="505f3-190">Default counting reason code</span></span>
- <span data-ttu-id="505f3-191">عرض كود سبب الجرد</span><span class="sxs-lookup"><span data-stu-id="505f3-191">Display counting reason code</span></span>
- <span data-ttu-id="505f3-192">تحرير كود سبب الجرد</span><span class="sxs-lookup"><span data-stu-id="505f3-192">Edit counting reason code</span></span>

