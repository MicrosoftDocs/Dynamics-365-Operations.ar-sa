---
title: "‏‫تخطيطات شاشة بيانات العرض التوضيحي‬ في نقطة البيع الحديثة (MPOS)/نقطة بيع المجموعة‬ (CPOS)"
description: "يقدم هذا الموضوع معلومات حول تخطيطات الشاشة المضمنة مع بيانات العرض التوضيحي المعينة لتجارب نقطة البيع (POS) في Microsoft Dynamics 365 for Retail."
author: zlinster
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: zlinster
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 41bd135c1b891841bd147d8ff9c905d49319b88e
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="demo-data-screen-layouts-in-mposcpos"></a><span data-ttu-id="46e10-103">‏‫تخطيطات شاشة بيانات العرض التوضيحي‬ في نقطة البيع الحديثة (MPOS)/نقطة بيع المجموعة‬ (CPOS)</span><span class="sxs-lookup"><span data-stu-id="46e10-103">Demo data screen layouts in MPOS/CPOS</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="46e10-104">يقدم هذا الموضوع معلومات حول تخطيطات الشاشة المضمنة مع بيانات العرض التوضيحي المعينة لتجارب نقطة البيع (POS) في Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="46e10-104">This topic provides information about the screen layouts that are included with the demo data set for the point of sale (POS) experiences in Microsoft Dynamics 365 for Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="46e10-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="46e10-105">Overview</span></span>

<span data-ttu-id="46e10-106">تقدم نماذج تخطيطات الشاشة المضمنة مع بيانات العرض التوضيحي للبيع بالتجزئة، تقدم المحتوى المُحسّن لقطاعات البيع بالتجزئة المختلفة، وأدوار العاملين بالمتاجر، والأجهزة.</span><span class="sxs-lookup"><span data-stu-id="46e10-106">The sample screen layouts that are included with Retail demo data provide content that is optimized for various retail segments, store worker roles, and devices.</span></span> <span data-ttu-id="46e10-107">يمكن أن يحتوي تخطيط واحد على عدة أحجام للتخطيطات ومجموعات من شبكات الأزرار للمساعدة في ضمان التغطية مع تنقل عاملي المتجر بين الأجهزة والمحطات.</span><span class="sxs-lookup"><span data-stu-id="46e10-107">A single layout can contain several layout sizes and combinations of button grids, to help ensure coverage as store workers move between devices and stations.</span></span> <span data-ttu-id="46e10-108">يوضح هذا الموضوع الاختلافات بين هذه التخطيطات والعمليات التي توفرها والتجارب العامة التي تقدمها.</span><span class="sxs-lookup"><span data-stu-id="46e10-108">This topic highlights the differences between these layouts, the operations that they provide, and the overall experiences that they deliver.</span></span>

![تخطيطات بيانات العرض التوضيحي عبر الأجهزة](../retail/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a><span data-ttu-id="46e10-110">تحليل لمعرف تخطيط شاشة</span><span class="sxs-lookup"><span data-stu-id="46e10-110">Anatomy of a screen layout ID</span></span>

<span data-ttu-id="46e10-111">للعثور على تخطيطات الشاشة في البيع بالتجزئة، انتقل إلى **البيع بالتجزئة**  >  **إعداد القناة**  >  **إعداد نقطة البيع**  >  **نقطة البيع**  >  **تخطيطات الشاشة**.</span><span class="sxs-lookup"><span data-stu-id="46e10-111">To find screen layouts in Retail, go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>

![صفحة تخطيطات الشاشة في البيع بالتجزئة](../retail/media/demo-screen-layouts-fig-2-1.png)

<span data-ttu-id="46e10-113">يمكن أن تتكون معرفات تخطيطات الشاشة من 10 أحرف كحد أقصى.</span><span class="sxs-lookup"><span data-stu-id="46e10-113">Screen layout IDs can have a maximum of 10 characters.</span></span> <span data-ttu-id="46e10-114">المعرف عبارة عن سلسلة تتألف من ثلاثة أجزاء من المعلومات، بالترتيب التالي:</span><span class="sxs-lookup"><span data-stu-id="46e10-114">The ID is a string that consists of three pieces of information, in this order:</span></span>

1. <span data-ttu-id="46e10-115">الشركة</span><span class="sxs-lookup"><span data-stu-id="46e10-115">Company</span></span>
2. <span data-ttu-id="46e10-116">إصدار التخطيط</span><span class="sxs-lookup"><span data-stu-id="46e10-116">Layout version</span></span>
3. <span data-ttu-id="46e10-117">الشخص</span><span class="sxs-lookup"><span data-stu-id="46e10-117">Persona</span></span>

### <a name="company"></a><span data-ttu-id="46e10-118">الشركة</span><span class="sxs-lookup"><span data-stu-id="46e10-118">Company</span></span>

| <span data-ttu-id="46e10-119">الحرف</span><span class="sxs-lookup"><span data-stu-id="46e10-119">Letter</span></span> | <span data-ttu-id="46e10-120">الشركة</span><span class="sxs-lookup"><span data-stu-id="46e10-120">Company</span></span>         |
|--------|-----------------|
| <span data-ttu-id="46e10-121">و</span><span class="sxs-lookup"><span data-stu-id="46e10-121">A</span></span>      | <span data-ttu-id="46e10-122">شركة المنتجات التجارية</span><span class="sxs-lookup"><span data-stu-id="46e10-122">Adventure Works</span></span> |
| <span data-ttu-id="46e10-123">F</span><span class="sxs-lookup"><span data-stu-id="46e10-123">F</span></span>      | <span data-ttu-id="46e10-124">شركة الاتحاد للتصنيع</span><span class="sxs-lookup"><span data-stu-id="46e10-124">Fabrikam</span></span>        |
| <span data-ttu-id="46e10-125">ش</span><span class="sxs-lookup"><span data-stu-id="46e10-125">C</span></span>      | <span data-ttu-id="46e10-126">شركة الرشيدي</span><span class="sxs-lookup"><span data-stu-id="46e10-126">Contoso</span></span>         |

### <a name="layout-version"></a><span data-ttu-id="46e10-127">إصدار التخطيط</span><span class="sxs-lookup"><span data-stu-id="46e10-127">Layout version</span></span>

| <span data-ttu-id="46e10-128">رقم الإصدار</span><span class="sxs-lookup"><span data-stu-id="46e10-128">Version number</span></span> | <span data-ttu-id="46e10-129">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="46e10-129">Description</span></span>                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="46e10-130">3</span><span class="sxs-lookup"><span data-stu-id="46e10-130">3</span></span>              | <span data-ttu-id="46e10-131">الإصدار الأساسي الذي يدعم العديد من أحجام الشاشات لأجهزة ونسب عرض إلى ارتفاع متنوعة</span><span class="sxs-lookup"><span data-stu-id="46e10-131">The base version that supports multiple screen sizes for various devices and aspect ratios</span></span> |
| <span data-ttu-id="46e10-132">3.1</span><span class="sxs-lookup"><span data-stu-id="46e10-132">3.1</span></span>            | <span data-ttu-id="46e10-133">الإصدار الأساسي الذي يحتوي على دعم إضافي للوحة **المنتجات الموصى بها**</span><span class="sxs-lookup"><span data-stu-id="46e10-133">The base version that has additional support for the **Recommended products** panel</span></span>        |

### <a name="persona"></a><span data-ttu-id="46e10-134">الشخص</span><span class="sxs-lookup"><span data-stu-id="46e10-134">Persona</span></span>

| <span data-ttu-id="46e10-135">الاختصار</span><span class="sxs-lookup"><span data-stu-id="46e10-135">Abbreviation</span></span> | <span data-ttu-id="46e10-136">الشخص</span><span class="sxs-lookup"><span data-stu-id="46e10-136">Persona</span></span>       | <span data-ttu-id="46e10-137">المحتويات</span><span class="sxs-lookup"><span data-stu-id="46e10-137">Contents</span></span> |
|--------------|---------------|----------|
| <span data-ttu-id="46e10-138">CSH</span><span class="sxs-lookup"><span data-stu-id="46e10-138">CSH</span></span>          | <span data-ttu-id="46e10-139">الصراف</span><span class="sxs-lookup"><span data-stu-id="46e10-139">Cashier</span></span>       | <span data-ttu-id="46e10-140">تتضمن تخطيطات الصراف عمليات مرتبطة بالحركات، مثل ‬‏‫أوامر العملاء، والمرتجعات، والخصومات، والإبطالات، وبطاقات الهدايا.</span><span class="sxs-lookup"><span data-stu-id="46e10-140">Cashier layouts include all transaction-related operations, such as customer orders, returns, discounts, voids, and gift cards.</span></span> <span data-ttu-id="46e10-141">تتضمن هذه التخطيطات أيضًا المهام اليومية لإدارة المخزون، مثل التحققات من السعر، وعمليات البحث عن المخزون، وعمليات جرد المخزون.</span><span class="sxs-lookup"><span data-stu-id="46e10-141">These layouts also include daily tasks for inventory management, such price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="46e10-142">يتم أيضًا توفير الإدارة الأساسية للورديات لمبالغ البدء، وتعليق الورديات، وساعة ضبط العمل.</span><span class="sxs-lookup"><span data-stu-id="46e10-142">Basic shift management is also provided for start amounts, suspending shifts, and time clock.</span></span> |
| <span data-ttu-id="46e10-143">MGR</span><span class="sxs-lookup"><span data-stu-id="46e10-143">MGR</span></span>          | <span data-ttu-id="46e10-144">مدير المتجر</span><span class="sxs-lookup"><span data-stu-id="46e10-144">Store Manager</span></span> | <span data-ttu-id="46e10-145">تتضمن تخطيطات مدير المتجر جميع العمليات المرتبطة بالحركات الموجودة في تخطيطات الصراف، وتتضمن أيضًا تجاوزات الضريبة.</span><span class="sxs-lookup"><span data-stu-id="46e10-145">Store Manager layouts include all transaction-related operations that are found in the Cashier layouts but also include tax overrides.</span></span> <span data-ttu-id="46e10-146">تتضمن هذه التخطيطات أيضًا المهام اليومية لإدارة المخزون مثل التحققات من السعر، وعمليات البحث عن المخزون، وعمليات جرد المخزون.</span><span class="sxs-lookup"><span data-stu-id="46e10-146">These layouts also include daily tasks for inventory management, such as price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="46e10-147">ويتم توفير إدارة الورديات لبدء الورديات وتعليقها وإقفالها.</span><span class="sxs-lookup"><span data-stu-id="46e10-147">Shift management is provided for starting, suspending, and closing shifts.</span></span> <span data-ttu-id="46e10-148">بالإضافة إلى ذلك، تتضمن التخطيطات عمليات الدرج للإدخالات، والإزالات، وإقرارات الدفع، والإيداعات البنكية والإيداعات بالخزينة.</span><span class="sxs-lookup"><span data-stu-id="46e10-148">Additionally, the layouts include drawer operations for entries, removals, tender declarations, and safe and bank drops.</span></span> <span data-ttu-id="46e10-149">وأخيرًا، تتضمن هذه التخطيطات إمكانية الوصول إلى تقارير الأداء، وتمكِّن تقارير X وZ للطباعة.</span><span class="sxs-lookup"><span data-stu-id="46e10-149">Finally, these layouts include access to performance reports, and enable X and Z reports to be printed.</span></span> |
| <span data-ttu-id="46e10-150">STK</span><span class="sxs-lookup"><span data-stu-id="46e10-150">STK</span></span>          | <span data-ttu-id="46e10-151">الموظف المسؤول عن المخزون</span><span class="sxs-lookup"><span data-stu-id="46e10-151">Stock Clerk</span></span>   | <span data-ttu-id="46e10-152">يتم تحسين تخطيطات الموظف المسؤول عن المخزون بهدف إدارة المخزون.</span><span class="sxs-lookup"><span data-stu-id="46e10-152">Stock Clerk layouts are optimized for inventory management.</span></span> <span data-ttu-id="46e10-153">وتتضمن إمكانية الوصول إلى المهام اليومية للتحققات من السعر، وعمليات البحث عن المخزون، و‏‫الانتقاء والاستلام‬، وعمليات جرد المخزون، وتفكيك المجموعة‬.‬</span><span class="sxs-lookup"><span data-stu-id="46e10-153">They include access to daily tasks for price checks, inventory lookups, picking and receiving, stock counts, and kit disassembly.</span></span> <span data-ttu-id="46e10-154">توفر هذه التخطيطات أيضًا العمليات الأساسية للورديات لوقت بدء العمل وتعليق الورديات.</span><span class="sxs-lookup"><span data-stu-id="46e10-154">These layouts also provide basic shift operations for time clock and suspending shifts.</span></span> <span data-ttu-id="46e10-155">وعلى الرغم من أن هذه التخطيطات مخصصة في الأساس لمهام المكاتب الخلفية، يكون لدى الموظفين المسؤولين عن المخزون نفس العمليات التي لدى الصرافين بالنسبة لشاشات الحركات.</span><span class="sxs-lookup"><span data-stu-id="46e10-155">Although these layouts are intended mainly for back-office tasks, stock clerks have the same operations as cashiers for transaction screens.</span></span> |

### <a name="example-layout"></a><span data-ttu-id="46e10-156">نموذج تخطيط</span><span class="sxs-lookup"><span data-stu-id="46e10-156">Example layout</span></span>

<span data-ttu-id="46e10-157">فيما يلي مثال لمعرف تخطيط شاشة لشركة الاتحاد للتصنيع، وإصدار التخطيط 3 والشخص مدير المتجر:</span><span class="sxs-lookup"><span data-stu-id="46e10-157">Here is an example of a screen layout ID for the Fabrikam company, layout version 3, and the Store Manager persona:</span></span>

<span data-ttu-id="46e10-158">F3MGR</span><span class="sxs-lookup"><span data-stu-id="46e10-158">F3MGR</span></span>

<span data-ttu-id="46e10-159">‏‫يوضح الرسم التوضيحي التالي مثالاً لشاشة ترحيب لمدير متجر شركة الاتحاد للتصنيع.</span><span class="sxs-lookup"><span data-stu-id="46e10-159">The following illustration shows an example of the Welcome screen for a Fabrikam store manager.</span></span>

![شاشة ترحيب لمدير متجر شركة الاتحاد للتصنيع](../retail/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a><span data-ttu-id="46e10-161">أحجام التخطيط</span><span class="sxs-lookup"><span data-stu-id="46e10-161">Layout sizes</span></span>

### <a name="full-vs-compact-layouts"></a><span data-ttu-id="46e10-162">التخطيطات الكاملة في مقابل الصغيرة</span><span class="sxs-lookup"><span data-stu-id="46e10-162">Full vs. compact layouts</span></span>

<span data-ttu-id="46e10-163">قد يحتوي تخطيط الشاشة على تكوينات لكل من الأجهزة الكاملة وصغيرة الحجم.</span><span class="sxs-lookup"><span data-stu-id="46e10-163">A screen layout can have configurations for both full devices and compact devices.</span></span> <span data-ttu-id="46e10-164">ولذلك، يمكن تعيين المستخدم إلى تخطيط شاشة واحد، والذي سوف يعمل عبر مختلف الأحجام وعوامل النموذج في المتجر.</span><span class="sxs-lookup"><span data-stu-id="46e10-164">Therefore, a user can be assigned to a single screen layout that will work across various sizes and form factors in the store.</span></span>

- <span data-ttu-id="46e10-165">**نقطة بيع حديثة - كبيرة الحجم** – تُعد التخطيطات الكاملة هي عادةً أفضل ما يمكن استخدامه للعروض الأكبر مثل شاشات الكمبيوتر أو أجهزة الكمبيوتر اللوحية.</span><span class="sxs-lookup"><span data-stu-id="46e10-165">**Modern POS - Full** – Typically, full layouts are best used for larger displays, such as desktop computer monitors or tablets.</span></span> <span data-ttu-id="46e10-166">يمكن للمستخدمين تحديد عناصر واجهة المستخدم التي يتضمنها التخطيط، وتحديد حجم هذه العناصر وموضعها، وتكوين الخصائص التفصيلية لها.</span><span class="sxs-lookup"><span data-stu-id="46e10-166">Users can select the UI elements that the layout includes, specify the size and placement of those elements, and configure their detailed properties.</span></span> <span data-ttu-id="46e10-167">تدعم التخطيطات الكاملة كل من تكوينات العمودي والأفقي على حد سواء.</span><span class="sxs-lookup"><span data-stu-id="46e10-167">Full layouts support both portrait and landscape configurations.</span></span>
- <span data-ttu-id="46e10-168">**نقطة بيع حديثة - صغيرة الحجم** – تُعد التخطيطات صغيرة الحجم هي عادةً أفضل ما يمكن استخدامه للهواتف أو أجهزة الكمبيوتر اللوحية الصغيرة.</span><span class="sxs-lookup"><span data-stu-id="46e10-168">**Modern POS - Compact** – Typically, compact layouts are best used for phones or small tablets.</span></span> <span data-ttu-id="46e10-169">وتُعد إمكانات التصميم بالنسبة للأجهزة الصغيرة محدودة إلى حد ما.</span><span class="sxs-lookup"><span data-stu-id="46e10-169">Design possibilities are limited for compact devices.</span></span> <span data-ttu-id="46e10-170">يمكن للمستخدمين تكوين الأعمدة والحقول لأجزاء الاستلام والإجماليات.</span><span class="sxs-lookup"><span data-stu-id="46e10-170">Users can configure the columns and fields for the receipt pane and the totals pane.</span></span>

### <a name="screen-resolutions-that-are-provided"></a><span data-ttu-id="46e10-171">مستويات دقة الشاشة التي يتم توفيرها</span><span class="sxs-lookup"><span data-stu-id="46e10-171">Screen resolutions that are provided</span></span>

<span data-ttu-id="46e10-172">يعرض الجدول التالي أحجام التخطيطات التي يتم توفيرها لمستويات دقة الشاشة العادية.</span><span class="sxs-lookup"><span data-stu-id="46e10-172">The following table shows the layout sizes that are provided for typical screen resolutions.</span></span>

| <span data-ttu-id="46e10-173">نوع التخطيط</span><span class="sxs-lookup"><span data-stu-id="46e10-173">Layout type</span></span> | <span data-ttu-id="46e10-174">الدقة</span><span class="sxs-lookup"><span data-stu-id="46e10-174">Resolution</span></span> | <span data-ttu-id="46e10-175">نسبة العرض إلى الارتفاع</span><span class="sxs-lookup"><span data-stu-id="46e10-175">Aspect ratio</span></span> | <span data-ttu-id="46e10-176">العرض الهدف</span><span class="sxs-lookup"><span data-stu-id="46e10-176">Target display</span></span>          |
|-------------|------------|--------------|-------------------------|
| <span data-ttu-id="46e10-177">صغيرة الحجم\*</span><span class="sxs-lookup"><span data-stu-id="46e10-177">Compact\*</span></span>   | <span data-ttu-id="46e10-178">480 × 853</span><span class="sxs-lookup"><span data-stu-id="46e10-178">480 × 853</span></span>  | <span data-ttu-id="46e10-179">16:9</span><span class="sxs-lookup"><span data-stu-id="46e10-179">16:9</span></span>         | <span data-ttu-id="46e10-180">الهواتف</span><span class="sxs-lookup"><span data-stu-id="46e10-180">Phones</span></span>                  |
| <span data-ttu-id="46e10-181">كبيرة الحجم</span><span class="sxs-lookup"><span data-stu-id="46e10-181">Full</span></span>        | <span data-ttu-id="46e10-182">1024 × 768</span><span class="sxs-lookup"><span data-stu-id="46e10-182">1024 × 768</span></span> | <span data-ttu-id="46e10-183">4:3</span><span class="sxs-lookup"><span data-stu-id="46e10-183">4:3</span></span>          | <span data-ttu-id="46e10-184">أجهزة الكمبيوتر اللوحية</span><span class="sxs-lookup"><span data-stu-id="46e10-184">Tablets</span></span>                 |
| <span data-ttu-id="46e10-185">كبيرة الحجم\*</span><span class="sxs-lookup"><span data-stu-id="46e10-185">Full\*</span></span>      | <span data-ttu-id="46e10-186">1280 × 720</span><span class="sxs-lookup"><span data-stu-id="46e10-186">1280 × 720</span></span> | <span data-ttu-id="46e10-187">16:9</span><span class="sxs-lookup"><span data-stu-id="46e10-187">16:9</span></span>         | <span data-ttu-id="46e10-188">أجهزة الكمبيوتر اللوحية</span><span class="sxs-lookup"><span data-stu-id="46e10-188">Tablets</span></span>                 |
| <span data-ttu-id="46e10-189">كبيرة الحجم</span><span class="sxs-lookup"><span data-stu-id="46e10-189">Full</span></span>        | <span data-ttu-id="46e10-190">1366 × 768</span><span class="sxs-lookup"><span data-stu-id="46e10-190">1366 × 768</span></span> | <span data-ttu-id="46e10-191">16:9</span><span class="sxs-lookup"><span data-stu-id="46e10-191">16:9</span></span>         | <span data-ttu-id="46e10-192">‏‫أجهزة الكمبيوتر اللوحية، الشاشات الكبيرة</span><span class="sxs-lookup"><span data-stu-id="46e10-192">Tablets, larger screens</span></span> |
| <span data-ttu-id="46e10-193">كبيرة الحجم</span><span class="sxs-lookup"><span data-stu-id="46e10-193">Full</span></span>        | <span data-ttu-id="46e10-194">1440 × 960</span><span class="sxs-lookup"><span data-stu-id="46e10-194">1440 × 960</span></span> | <span data-ttu-id="46e10-195">3:2</span><span class="sxs-lookup"><span data-stu-id="46e10-195">3:2</span></span>          | <span data-ttu-id="46e10-196">‏‫أجهزة الكمبيوتر اللوحية، الشاشات الكبيرة</span><span class="sxs-lookup"><span data-stu-id="46e10-196">Tablets, larger screens</span></span> |

<span data-ttu-id="46e10-197">\* لا تتوفر أحجام التخطيطات الإضافية هذه إلا في تخطيطات شركة المنتجات التجارية وشركة الاتحاد للتصنيع.</span><span class="sxs-lookup"><span data-stu-id="46e10-197">\* These additional layout sizes are available only in Adventure Works and Fabrikam layouts.</span></span>


>[!TIP]
> <span data-ttu-id="46e10-198">تحدد نقطة البيع تلقائيًا أحجام التخطيطات استنادًا إلى أقرب حجم متوفر لدقة شاشة إطار التطبيق الحالي.</span><span class="sxs-lookup"><span data-stu-id="46e10-198">POS automatically selects layout sizes, based on the closest size that is available for the screen resolution of the current app window.</span></span> <span data-ttu-id="46e10-199">للعثور على معرف تخطيط الشاشة ودقة التخطيط المستخدمين حاليًا، في نقطة البيع الحديثة للبيع بالتجزئة (MPOS) أو نقطة بيع المجموعة للبيع بالتجزئة (CPOS)، افتح صفحة **الإعدادات**، وابحث في القسم **معلومات جلسة العمل**.</span><span class="sxs-lookup"><span data-stu-id="46e10-199">To find the screen layout ID and layout resolution that are currently used, in Retail Modern POS (MPOS) or Retail Cloud POS (CPOS), open the **Settings** page, and look in the **Session information** section.</span></span> <span data-ttu-id="46e10-200">يمكنك أيضًا الاطلاع على دقة الإطار الفعلية لإطار المستعرض أو التطبيق الحالي.</span><span class="sxs-lookup"><span data-stu-id="46e10-200">You can also see the actual window resolution for your current application or browser frame.</span></span> <span data-ttu-id="46e10-201">بعد الحصول على هذه المعلومات، يمكنك العثور على مصدر محتوى التخطيط في البيع بالتجزئة بالانتقال إلى **إعداد القناة** > **إعداد نقطة البيع** > **نقطة البيع** > **تخطيطات الشاشة**.</span><span class="sxs-lookup"><span data-stu-id="46e10-201">After you have this information, you can find the source of the layout content in Retail by going to **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>


![تخطيطات الشاشة ومستويات دقة/أحجام التخطيطات في البيع بالتجزئة ونقطة البيع](../retail/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a><span data-ttu-id="46e10-203">الشركات والعلامات التجارية</span><span class="sxs-lookup"><span data-stu-id="46e10-203">Companies and brands</span></span>

<span data-ttu-id="46e10-204">يتم توجيه كل شركة وهمية لقطاع مختلف للبيع بالتجزئة وتتضمن كتالوجات منتجات يتم ضبطها لسوق الشركة.</span><span class="sxs-lookup"><span data-stu-id="46e10-204">Each fictitious company is targeted to a different retail segment and includes product catalogs that are tuned for the company's market.</span></span> <span data-ttu-id="46e10-205">يكون لكل شركة علامة تجارية مرئية فريدة مصاحبة لمنتجاتها.</span><span class="sxs-lookup"><span data-stu-id="46e10-205">Each company has a unique visual brand that accompanies its products.</span></span> <span data-ttu-id="46e10-206">وتتضمن عناصر العلامة التجارية لونًا تمييزيًا ونسقًا داكنًا أو فاتحًا وصور فوتوغرافية مصاحبة توفر تجارب واقعية.</span><span class="sxs-lookup"><span data-stu-id="46e10-206">Branding elements include the accent color, dark or light theme, and accompanying photographs that provide realistic experiences.</span></span>

### <a name="company-segment-and-visual-characteristics"></a><span data-ttu-id="46e10-207">شريحة الشركة والخصائص المرئية</span><span class="sxs-lookup"><span data-stu-id="46e10-207">Company segment and visual characteristics</span></span>

| <span data-ttu-id="46e10-208">الشركة</span><span class="sxs-lookup"><span data-stu-id="46e10-208">Company</span></span>         | <span data-ttu-id="46e10-209"> الموقع</span><span class="sxs-lookup"><span data-stu-id="46e10-209">Location</span></span> | <span data-ttu-id="46e10-210">الشريحة</span><span class="sxs-lookup"><span data-stu-id="46e10-210">Segment</span></span>        | <span data-ttu-id="46e10-211">التمييز</span><span class="sxs-lookup"><span data-stu-id="46e10-211">Accent</span></span> | <span data-ttu-id="46e10-212">النسق</span><span class="sxs-lookup"><span data-stu-id="46e10-212">Theme</span></span> |
|-----------------|----------|----------------|--------|-------|
| <span data-ttu-id="46e10-213">شركة المنتجات التجارية</span><span class="sxs-lookup"><span data-stu-id="46e10-213">Adventure Works</span></span> | <span data-ttu-id="46e10-214">سياتل</span><span class="sxs-lookup"><span data-stu-id="46e10-214">Seattle</span></span>  | <span data-ttu-id="46e10-215">المنتجات الرياضية</span><span class="sxs-lookup"><span data-stu-id="46e10-215">Sporting Goods</span></span> | <span data-ttu-id="46e10-216">أزرق</span><span class="sxs-lookup"><span data-stu-id="46e10-216">Blue</span></span>   | <span data-ttu-id="46e10-217">داكن</span><span class="sxs-lookup"><span data-stu-id="46e10-217">Dark</span></span>  |
| <span data-ttu-id="46e10-218">شركة الاتحاد للتصنيع</span><span class="sxs-lookup"><span data-stu-id="46e10-218">Fabrikam</span></span>        | <span data-ttu-id="46e10-219">هوستون</span><span class="sxs-lookup"><span data-stu-id="46e10-219">Houston</span></span>  | <span data-ttu-id="46e10-220">الموضة</span><span class="sxs-lookup"><span data-stu-id="46e10-220">Fashion</span></span>        | <span data-ttu-id="46e10-221">أخضر</span><span class="sxs-lookup"><span data-stu-id="46e10-221">Green</span></span>  | <span data-ttu-id="46e10-222">فاتح</span><span class="sxs-lookup"><span data-stu-id="46e10-222">Light</span></span> |
| <span data-ttu-id="46e10-223">شركة الرشيدي</span><span class="sxs-lookup"><span data-stu-id="46e10-223">Contoso</span></span>         | <span data-ttu-id="46e10-224">بوسطن</span><span class="sxs-lookup"><span data-stu-id="46e10-224">Boston</span></span>   | <span data-ttu-id="46e10-225">الإلكترونيات</span><span class="sxs-lookup"><span data-stu-id="46e10-225">Electronics</span></span>    | <span data-ttu-id="46e10-226">أحمر</span><span class="sxs-lookup"><span data-stu-id="46e10-226">Red</span></span>    | <span data-ttu-id="46e10-227">داكن</span><span class="sxs-lookup"><span data-stu-id="46e10-227">Dark</span></span>  |


>[!NOTE]
> <span data-ttu-id="46e10-228">شركة المنتجات التجارية و‏‫شركة الاتحاد للتصنيع هما العلامتان التجاريتان الرئيسيتان.</span><span class="sxs-lookup"><span data-stu-id="46e10-228">Adventure Works and Fabrikam are the two flagship brands.</span></span> <span data-ttu-id="46e10-229">شركة الرشيدي متاحة، ولكن لم يتم توفير جميع التخطيطات.</span><span class="sxs-lookup"><span data-stu-id="46e10-229">Contoso is available, but not all layouts have been provided.</span></span>


<span data-ttu-id="46e10-230">‏‫تبين الأشكال التوضيحية التالية أمثلة على صفحة الترحيب وصفحة الحركة للشركات الوهمية الثلاثة.</span><span class="sxs-lookup"><span data-stu-id="46e10-230">The following illustrations show examples of the welcome page and transaction page for the three fictitious companies.</span></span>

### <a name="adventure-works"></a><span data-ttu-id="46e10-231">شركة المنتجات التجارية</span><span class="sxs-lookup"><span data-stu-id="46e10-231">Adventure Works</span></span>

![صفحة ترحيب ‬‏‫بيانات العرض التوضيحي لشركة المنتجات التجارية](../retail/media/demo-screen-layouts-fig-4-1a.png)

![صفحة حركة ‬‏‫بيانات العرض التوضيحي لشركة المنتجات التجارية](../retail/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a><span data-ttu-id="46e10-234">شركة الاتحاد للتصنيع</span><span class="sxs-lookup"><span data-stu-id="46e10-234">Fabrikam</span></span>

![صفحة ترحيب ‬‏‫بيانات العرض التوضيحي لشركة الاتحاد للتصنيع](../retail/media/demo-screen-layouts-fig-4-2a.png)

![صفحة حركة ‬‏‫بيانات العرض التوضيحي لشركة الاتحاد للتصنيع](../retail/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a><span data-ttu-id="46e10-237">شركة الرشيدي</span><span class="sxs-lookup"><span data-stu-id="46e10-237">Contoso</span></span>

![‏‫تخطيطات بيانات العرض التوضيحي لشركة الرشيدي](../retail/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a><span data-ttu-id="46e10-239">علامة مستخدم في مصفوفة</span><span class="sxs-lookup"><span data-stu-id="46e10-239">User sign in matrix</span></span>

<span data-ttu-id="46e10-240">تم توفير المستخدمين لتخطيطات مختلفة للشاشة.</span><span class="sxs-lookup"><span data-stu-id="46e10-240">Users have been provided for the various screen layouts.</span></span> <span data-ttu-id="46e10-241">باستخدام الجدول التالي، يفترض أن تتمكن من الوصول إلى أي من الشاشات.</span><span class="sxs-lookup"><span data-stu-id="46e10-241">By using the following table, you should be able to access any of the screens.</span></span> <span data-ttu-id="46e10-242">ما عليك إلا تسجيل الدخول باستخدام معرف مشغل صحيح.</span><span class="sxs-lookup"><span data-stu-id="46e10-242">Just sign in by using an appropriate operator ID.</span></span>

| <span data-ttu-id="46e10-243">الشركة</span><span class="sxs-lookup"><span data-stu-id="46e10-243">Company</span></span>         | <span data-ttu-id="46e10-244">معرف تخطيط الشاشة</span><span class="sxs-lookup"><span data-stu-id="46e10-244">Screen layout ID</span></span> | <span data-ttu-id="46e10-245">الشخص</span><span class="sxs-lookup"><span data-stu-id="46e10-245">Persona</span></span>          | <span data-ttu-id="46e10-246">معرفات المشغلين</span><span class="sxs-lookup"><span data-stu-id="46e10-246">Operator IDs</span></span>           |
|-----------------|------------------|---------------   |------------------------|
| <span data-ttu-id="46e10-247">شركة المنتجات التجارية</span><span class="sxs-lookup"><span data-stu-id="46e10-247">Adventure Works</span></span> | <span data-ttu-id="46e10-248">A3MGR</span><span class="sxs-lookup"><span data-stu-id="46e10-248">A3MGR</span></span>            | <span data-ttu-id="46e10-249">مدير المتجر</span><span class="sxs-lookup"><span data-stu-id="46e10-249">Store Manager</span></span>    | <span data-ttu-id="46e10-250">000154، 000137، 000073</span><span class="sxs-lookup"><span data-stu-id="46e10-250">000154, 000137, 000073</span></span> |
| <span data-ttu-id="46e10-251">شركة المنتجات التجارية</span><span class="sxs-lookup"><span data-stu-id="46e10-251">Adventure Works</span></span> | <span data-ttu-id="46e10-252">A3CSH</span><span class="sxs-lookup"><span data-stu-id="46e10-252">A3CSH</span></span>            | <span data-ttu-id="46e10-253">الصراف</span><span class="sxs-lookup"><span data-stu-id="46e10-253">Cashier</span></span>          | <span data-ttu-id="46e10-254">000150، 000175، 000165</span><span class="sxs-lookup"><span data-stu-id="46e10-254">000150, 000175, 000165</span></span> |
| <span data-ttu-id="46e10-255">شركة المنتجات التجارية</span><span class="sxs-lookup"><span data-stu-id="46e10-255">Adventure Works</span></span> | <span data-ttu-id="46e10-256">A3STK</span><span class="sxs-lookup"><span data-stu-id="46e10-256">A3STK</span></span>            | <span data-ttu-id="46e10-257">الموظف المسؤول عن المخزون</span><span class="sxs-lookup"><span data-stu-id="46e10-257">Stock Clerk</span></span>      | <span data-ttu-id="46e10-258">000155، 000181، 000152</span><span class="sxs-lookup"><span data-stu-id="46e10-258">000155, 000181, 000152</span></span> |
| <span data-ttu-id="46e10-259">شركة الاتحاد للتصنيع</span><span class="sxs-lookup"><span data-stu-id="46e10-259">Fabrikam</span></span>        | <span data-ttu-id="46e10-260">F3MGR</span><span class="sxs-lookup"><span data-stu-id="46e10-260">F3MGR</span></span>            | <span data-ttu-id="46e10-261">مدير المتجر</span><span class="sxs-lookup"><span data-stu-id="46e10-261">Store Manager</span></span>    | <span data-ttu-id="46e10-262">000160، 000168، 000163</span><span class="sxs-lookup"><span data-stu-id="46e10-262">000160, 000168, 000163</span></span> |
| <span data-ttu-id="46e10-263">شركة الاتحاد للتصنيع</span><span class="sxs-lookup"><span data-stu-id="46e10-263">Fabrikam</span></span>        | <span data-ttu-id="46e10-264">F3CSH</span><span class="sxs-lookup"><span data-stu-id="46e10-264">F3CSH</span></span>            | <span data-ttu-id="46e10-265">الصراف</span><span class="sxs-lookup"><span data-stu-id="46e10-265">Cashier</span></span>          | <span data-ttu-id="46e10-266">000161، 000113، 000114</span><span class="sxs-lookup"><span data-stu-id="46e10-266">000161, 000113, 000114</span></span> |
| <span data-ttu-id="46e10-267">شركة الاتحاد للتصنيع</span><span class="sxs-lookup"><span data-stu-id="46e10-267">Fabrikam</span></span>        | <span data-ttu-id="46e10-268">F3STK</span><span class="sxs-lookup"><span data-stu-id="46e10-268">F3STK</span></span>            | <span data-ttu-id="46e10-269">الموظف المسؤول عن المخزون</span><span class="sxs-lookup"><span data-stu-id="46e10-269">Stock Clerk</span></span>      | <span data-ttu-id="46e10-270">000164، 000112، 000123</span><span class="sxs-lookup"><span data-stu-id="46e10-270">000164, 000112, 000123</span></span> |
| <span data-ttu-id="46e10-271">شركة الرشيدي</span><span class="sxs-lookup"><span data-stu-id="46e10-271">Contoso</span></span>         | <span data-ttu-id="46e10-272">C3MGR</span><span class="sxs-lookup"><span data-stu-id="46e10-272">C3MGR</span></span>            | <span data-ttu-id="46e10-273">مدير المتجر</span><span class="sxs-lookup"><span data-stu-id="46e10-273">Store Manager</span></span>    | <span data-ttu-id="46e10-274">000100, 000111</span><span class="sxs-lookup"><span data-stu-id="46e10-274">000100, 000111</span></span>         |
| <span data-ttu-id="46e10-275">شركة الرشيدي</span><span class="sxs-lookup"><span data-stu-id="46e10-275">Contoso</span></span>         | <span data-ttu-id="46e10-276">C3CSH</span><span class="sxs-lookup"><span data-stu-id="46e10-276">C3CSH</span></span>            | <span data-ttu-id="46e10-277">الصراف</span><span class="sxs-lookup"><span data-stu-id="46e10-277">Cashier</span></span>          | <span data-ttu-id="46e10-278">000110, 000120</span><span class="sxs-lookup"><span data-stu-id="46e10-278">000110, 000120</span></span>         |
| <span data-ttu-id="46e10-279">شركة الرشيدي</span><span class="sxs-lookup"><span data-stu-id="46e10-279">Contoso</span></span>         | <span data-ttu-id="46e10-280">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="46e10-280">Not applicable</span></span>   | <span data-ttu-id="46e10-281">الموظف المسؤول عن المخزون</span><span class="sxs-lookup"><span data-stu-id="46e10-281">Stock Clerk</span></span>      | <span data-ttu-id="46e10-282">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="46e10-282">Not applicable</span></span>         |


>[!TIP]
> <span data-ttu-id="46e10-283">للحصول على أفضل النتائج، قم بتنشيط سجل في موقع المتجر المطابق، وعيِّن الشركة إلى شركة الشخص الذي تعتزم استخدامه عند تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="46e10-283">For best results, activate a register in the corresponding store location, and set the company to the company of the persona that you plan to use when you sign in.</span></span> <span data-ttu-id="46e10-284">بهذه الطريقة، تساعد في ضمان انسجام ملف التعريف المرئي وصور العلامة التجارية عبر التجربة.</span><span class="sxs-lookup"><span data-stu-id="46e10-284">In this way, you help guarantee that the visual profile and branding images are aligned across the experience.</span></span> <span data-ttu-id="46e10-285">على سبيل المثال، إذا كنت ترغب في رؤية تخطيط شركة الاتحاد للتصنيع لأحد الصرافين، يجب تنشيط سجل في متجر هوستون.</span><span class="sxs-lookup"><span data-stu-id="46e10-285">For example, if you're interested in seeing a Fabrikam layout for a cashier, you should activate a register in the Houston store.</span></span>


<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail > Channel setup > POS setup > POS > Images**. -->

<!-- ![Images in Dynamics 365 for Retail](../retail/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../retail/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->

