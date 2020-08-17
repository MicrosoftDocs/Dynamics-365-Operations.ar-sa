---
title: سياسات العمل
description: يصف هذا الموضوع كيفية إعداد سياسات العمل.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 5ea93324547ed81df120db3412ee41fce2a93f4a
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/03/2020
ms.locfileid: "3651995"
---
# <a name="work-policies"></a><span data-ttu-id="ed450-103">سياسات العمل</span><span class="sxs-lookup"><span data-stu-id="ed450-103">Work policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed450-104">يوضح هذا الموضوع كيفية إعداد النظام وتطبيق المستودع لدعم سياسات العمل.</span><span class="sxs-lookup"><span data-stu-id="ed450-104">This topic explains how to set up the system and the warehouse app so that they support work policies.</span></span> <span data-ttu-id="ed450-105">يمكنك استخدام هذه الوظيفة لتسجيل المخزون بشكل سريع دون إنشاء عمل تخزين عندما تتلقى أوامر شراء أو أوامر تحويل، أو عندما تكمل عمليات التصنيع.</span><span class="sxs-lookup"><span data-stu-id="ed450-105">You can use this functionality to quickly register inventory without creating putaway work when you receive purchase or transfer orders, or when you complete manufacturing processes.</span></span> <span data-ttu-id="ed450-106">يقدم هذا الموضوع معلومات عامة.</span><span class="sxs-lookup"><span data-stu-id="ed450-106">This topic provides general information.</span></span> <span data-ttu-id="ed450-107">للحصول على معلومات مفصلة حول استلام لوحة الترخيص، راجع [استلام لوحة الترخيص من خلال تطبيق المستودع](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="ed450-107">For detailed information that is related to license plate receiving, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="ed450-108">تتحكم سياسة العمل بما إذا كان إنشاء عمل المستودع يتم عند الإعلام عن صنف مصنّع كمنتهٍ، أو عند استلام البضائع باستخدام تطبيق المستودع.</span><span class="sxs-lookup"><span data-stu-id="ed450-108">A work policy controls whether warehouse work is created when a manufactured item is reported as finished, or when goods are received by using the warehouse app.</span></span> <span data-ttu-id="ed450-109">يمكنك إعداد كل سياسة عمل عن طريق تعريف الشروط حيث تنطبق: أنواع وعمليات أوامر العمل وموقع المخزون و(اختياريًا) المنتجات.</span><span class="sxs-lookup"><span data-stu-id="ed450-109">You set up each work policy by defining the conditions where it applies: the work order types and processes, the inventory location, and (optionally) the products.</span></span> <span data-ttu-id="ed450-110">على سبيل المثال، يجب استلام أمر شراء للمنتج *A0001* في الموقع *RECV* في المستودع *24*.</span><span class="sxs-lookup"><span data-stu-id="ed450-110">For example, a purchase order for product *A0001* must be received in location *RECV* in warehouse *24*.</span></span> <span data-ttu-id="ed450-111">في وقت لاحق، يتم استهلاك المنتج في عملية أخرى في الموقع *RECV*.</span><span class="sxs-lookup"><span data-stu-id="ed450-111">Later, the product is consumed in another process at location *RECV*.</span></span> <span data-ttu-id="ed450-112">في هذه الحالة، يمكنك إعداد سياسة عمل لمنع إنشاء عمل التخزين عندما يقوم أحد العاملين بالإعلام عن المنتج *A0001* على أنه مستلم في الموقع *RECV*.</span><span class="sxs-lookup"><span data-stu-id="ed450-112">In this case, you can set up a work policy to prevent putaway work from being created when a worker reports product *A0001* as received in location *RECV*.</span></span>

> [!NOTE]
> - <span data-ttu-id="ed450-113">لكي تكون سياسة العمل نشطة، يجب عليك تحديد موقع واحد على الأقل فيها على علامة التبويب السريعة **مواقع المخزون** في صفحة **سياسات العمل**.</span><span class="sxs-lookup"><span data-stu-id="ed450-113">For a work policy to be active, you must define at least one location for it on the **Inventory locations** FastTab of the **Work policies** page.</span></span> 
> - <span data-ttu-id="ed450-114">لا يمكنك تحديد نفس الموقع لسياسات عمل متعددة.</span><span class="sxs-lookup"><span data-stu-id="ed450-114">You can't specify the same location for multiple work policies.</span></span>
> - <span data-ttu-id="ed450-115">لن يطبع الخيار **طباعة بطاقة‬** عناصر قائمة الجهاز المحمول بطاقة لوحة ترخيص إلا عند إنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="ed450-115">The **Print label** option for mobile device menu items won't print a license plate label unless work was created.</span></span>

## <a name="activate-the-features-in-your-system"></a><span data-ttu-id="ed450-116">تنشيط الميزات في النظام</span><span class="sxs-lookup"><span data-stu-id="ed450-116">Activate the features in your system</span></span>

<span data-ttu-id="ed450-117">لجعل كافة الوظائف الموضحة في هذا الموضوع متوفرة في النظام، قم بتشغيل الميزتين التاليتين في [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span><span class="sxs-lookup"><span data-stu-id="ed450-117">To make all the functionality that is described in this topic available in your system, turn on the following two features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span></span>

- <span data-ttu-id="ed450-118">عمليات تحسين استلام ‏‫لوحة الترخيص‬</span><span class="sxs-lookup"><span data-stu-id="ed450-118">License plate receiving enhancements</span></span>
- <span data-ttu-id="ed450-119">تحسينات سياسة العمل للعمل الوارد</span><span class="sxs-lookup"><span data-stu-id="ed450-119">Work policy enhancements for inbound work</span></span>

## <a name="the-work-policies-page"></a><span data-ttu-id="ed450-120">صفحة سياسات العمل</span><span class="sxs-lookup"><span data-stu-id="ed450-120">The Work policies page</span></span>

<span data-ttu-id="ed450-121">لإعداد سياسات العمل، انتقل إلى **إدارة المستودعات \> إعداد \> العمل \> سياسات العمل**.</span><span class="sxs-lookup"><span data-stu-id="ed450-121">To set up work policies, go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span> <span data-ttu-id="ed450-122">ثم، على علامة التبويب السريعة، قم بتعيين الحقول كما هو موضح في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="ed450-122">Then, on each FastTab, set the fields as described in the following subsections.</span></span>

### <a name="the-work-order-types-fasttab"></a><span data-ttu-id="ed450-123">علامة التبويب السريعة "أنواع أوامر العمل"</span><span class="sxs-lookup"><span data-stu-id="ed450-123">The Work order types FastTab</span></span>

<span data-ttu-id="ed450-124">على علامة التبويب السريعة **أنواع أوامر العمل**، أضف كافة أنواع أوامر العمل والعمليات ذات الصلة بالعمل، التي تنطبق عليها سياسة العمل.</span><span class="sxs-lookup"><span data-stu-id="ed450-124">On the **Work order types** FastTab, add all the work order types, and the related work processes, that the work policy applies to.</span></span> <span data-ttu-id="ed450-125">أنواع أوامر العمل التالية وعمليات العمل ذات الصلة مدعومة لسياسات العمل.</span><span class="sxs-lookup"><span data-stu-id="ed450-125">The following work order types and related work processes are supported for work policies.</span></span>

| <span data-ttu-id="ed450-126">نوع أمر العمل</span><span class="sxs-lookup"><span data-stu-id="ed450-126">Work order type</span></span> | <span data-ttu-id="ed450-127">عملية العمل</span><span class="sxs-lookup"><span data-stu-id="ed450-127">Work process</span></span> |
|---|---|
| <span data-ttu-id="ed450-128">انتقاء المواد الخام</span><span class="sxs-lookup"><span data-stu-id="ed450-128">Raw material picking</span></span>| <span data-ttu-id="ed450-129">جميع العمليات ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="ed450-129">All related processes</span></span> |
| <span data-ttu-id="ed450-130">تخزين منتج مساعد ومنتج ثانوي</span><span class="sxs-lookup"><span data-stu-id="ed450-130">Co-product and by-product put away</span></span> | <span data-ttu-id="ed450-131">جميع العمليات ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="ed450-131">All related processes</span></span> |
| <span data-ttu-id="ed450-132">تخزين البضائع المنتهية</span><span class="sxs-lookup"><span data-stu-id="ed450-132">Finished goods putaway</span></span> | <span data-ttu-id="ed450-133">جميع العمليات ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="ed450-133">All related processes</span></span> |
| <span data-ttu-id="ed450-134">استلام التحويل</span><span class="sxs-lookup"><span data-stu-id="ed450-134">Transfer receipt</span></span> | <span data-ttu-id="ed450-135">استلام ‏‫لوحة الترخيص‬ (وتخزينها)</span><span class="sxs-lookup"><span data-stu-id="ed450-135">License plate receiving (and putaway)</span></span> |
| <span data-ttu-id="ed450-136">أوامر الشراء</span><span class="sxs-lookup"><span data-stu-id="ed450-136">Purchase orders</span></span> | <ul><li><span data-ttu-id="ed450-137">استلام ‏‫لوحة الترخيص‬ (وتخزينها)</span><span class="sxs-lookup"><span data-stu-id="ed450-137">License plate receiving (and putaway)</span></span></li><li><span data-ttu-id="ed450-138">استلام صنف الحمل (وتخزينه)</span><span class="sxs-lookup"><span data-stu-id="ed450-138">Load item receiving (and putaway)</span></span></li><li><span data-ttu-id="ed450-139">استلام بند أمر الشراء (وتخزينه)</span><span class="sxs-lookup"><span data-stu-id="ed450-139">Purchase order line receiving (and putaway)</span></span></li><li><span data-ttu-id="ed450-140">استلام صنف أمر الشراء (وتخزينه)</span><span class="sxs-lookup"><span data-stu-id="ed450-140">Purchase order item receiving (and putaway)</span></span></li></ul> |

<span data-ttu-id="ed450-141">لإعداد سياسة عمل بحيث يتم تطبيها على عمليات عمل متعددة من نوع أمر العمل نفسه، أضف بندًا منفصلاً لكل عملية عمل إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="ed450-141">To set up a work policy so that it applies to several work processes of the same work order type, add a separate line for each work process to the grid.</span></span>

<span data-ttu-id="ed450-142">لكل بند في الشبكة، قم بتعيين حقل **طريقة إنشاء العمل** إلى إحدى القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ed450-142">For each line in the grid, set the **Work creation method** field to one of the following values:</span></span>

- <span data-ttu-id="ed450-143">**إطلاقًا** – سوف تمنع سياسة العمل إنشاء عمل المستودع لنوع أمر العمل المحدد وعمليات العمل المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="ed450-143">**Never** – The work policy will prevent warehouse work from being created for the selected work order type and related work process.</span></span>
- <span data-ttu-id="ed450-144">**توزيع البضائع** – ستقوم سياسة العمل بإنشاء عمل توزيع البضائع باستخدام السياسة التي تحددها في حقل **اسم سياسة توزيع البضائع**.</span><span class="sxs-lookup"><span data-stu-id="ed450-144">**Cross docking** – The work policy will create cross-docking work by using the policy that you select in the **Cross docking policy name** field.</span></span>

### <a name="the-inventory-locations-fasttab"></a><span data-ttu-id="ed450-145">علامة التبويب السريعة "مواقع المخزون"</span><span class="sxs-lookup"><span data-stu-id="ed450-145">The Inventory locations FastTab</span></span>

<span data-ttu-id="ed450-146">على علامة التبويب السريعة **مواقع المخزون**، أضف كافة المواقع التي يجب تطبيق سياسة العمل هذه فيها.</span><span class="sxs-lookup"><span data-stu-id="ed450-146">On the **Inventory locations** FastTab, add all the locations where this work policy should be applied.</span></span> <span data-ttu-id="ed450-147">إذا لم يتم ربط أي موقع بسياسة عمل، فلن يتم تطبيق سياسة العمل على أي عملية.</span><span class="sxs-lookup"><span data-stu-id="ed450-147">If no location is associated with a work policy, the work policy won't be applied to any process.</span></span>

<span data-ttu-id="ed450-148">لا يمكنك تحديد نفس الموقع لسياسات عمل متعددة.</span><span class="sxs-lookup"><span data-stu-id="ed450-148">You can't specify the same location for multiple work policies.</span></span>

<span data-ttu-id="ed450-149">يمكنك استخدام موقع مستودع تم تعيينه إلى ملف تعريف الموقع حيث الخيار **استخدام تعقب لوحة الترخيص** متوقف عن التشغيل.</span><span class="sxs-lookup"><span data-stu-id="ed450-149">You can use a warehouse location that is assigned to a location profile where the **Use license plate tracking** option is turned off.</span></span> <span data-ttu-id="ed450-150">في هذه الحالة، سيقوم العاملون بتسجيل المخزون الفعلي بشكل مباشر.</span><span class="sxs-lookup"><span data-stu-id="ed450-150">In this case, workers will directly register the on-hand inventory.</span></span>

### <a name="the-products-fasttab"></a><span data-ttu-id="ed450-151">علامة التبويب السريعة "المنتجات"</span><span class="sxs-lookup"><span data-stu-id="ed450-151">The Products FastTab</span></span>

<span data-ttu-id="ed450-152">على علامة التبويب السريعة **المنتجات**، قم بتعيين الحقل **تحديد المنتج** للتحكم في المنتجات التي يجب تطبيق السياسة عليها:</span><span class="sxs-lookup"><span data-stu-id="ed450-152">On the **Products** tab, set the **Product selection** field to control which products the policy should apply to:</span></span>

- <span data-ttu-id="ed450-153">**الكل** – يجب تطبيق السياسة على كافة المنتجات.</span><span class="sxs-lookup"><span data-stu-id="ed450-153">**All** – The policy should apply to all products.</span></span>
- <span data-ttu-id="ed450-154">**محدد** – يجب تطبيق السياسة فقط على المنتجات المذكورة في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="ed450-154">**Selected** – The policy should apply only to products that are listed in the grid.</span></span> <span data-ttu-id="ed450-155">استخدم شريط الأدوات على علامة التبويب السريعة **المنتجات** لإضافة منتجات إلى الشبكة أو لإزالتها من الشبكة.</span><span class="sxs-lookup"><span data-stu-id="ed450-155">Use the toolbar on the **Products** FastTab to add products to the grid or remove them from the grid.</span></span>

## <a name="default-and-custom-to-locations"></a><span data-ttu-id="ed450-156">مواقع "إلى" افتراضية ومخصصة</span><span class="sxs-lookup"><span data-stu-id="ed450-156">Default and custom "to" locations</span></span>

> [!NOTE]
> <span data-ttu-id="ed450-157">لجعل الوظيفة الموضحة في هذا القسم متوفرة في النظام، يجب عليك تشغيل الميزتين *تحسينات استلام لوحة الترخيص* و*تحسينات سياسة العمل للعمل الوارد* في [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ed450-157">To make the functionality that is described in this section available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="ed450-158">في السابق، كان النظام يدعم الاستلام فقط في الموقع الافتراضي الذي تم تحديده لكل مستودع.</span><span class="sxs-lookup"><span data-stu-id="ed450-158">Previously, the system supported receiving only at the default location that is defined for each warehouse.</span></span> <span data-ttu-id="ed450-159">ومع ذلك، توفر الآن عناصر قائمة الأجهزة المحمولة التي تستخدم عمليات إنشاء العمل التالية الخيار **استخدام البيانات الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="ed450-159">However, mobile device menu items that use the following work creation processes now provide the **Use default data** option.</span></span> <span data-ttu-id="ed450-160">يتيح لك هذا الخيار تعيين موقع "إلى" مخصص لواحد أو أكثر من عناصر القائمة.</span><span class="sxs-lookup"><span data-stu-id="ed450-160">This option lets you assign a custom "to" location to one or more menu items.</span></span> <span data-ttu-id="ed450-161">(كان هذا الخيار متوفرًا لبعض الأنواع الأخرى من عناصر القائمة.)</span><span class="sxs-lookup"><span data-stu-id="ed450-161">(This option was already available for some other types of menu items.)</span></span>

- <span data-ttu-id="ed450-162">استلام ‏‫لوحة الترخيص‬ (وتخزينها)</span><span class="sxs-lookup"><span data-stu-id="ed450-162">License plate receiving (and putaway)</span></span>
- <span data-ttu-id="ed450-163">استلام صنف الحمل (وتخزينه)</span><span class="sxs-lookup"><span data-stu-id="ed450-163">Load item receiving (and putaway)</span></span>
- <span data-ttu-id="ed450-164">استلام بند أمر الشراء (وتخزينه)</span><span class="sxs-lookup"><span data-stu-id="ed450-164">Purchase order line receiving (and putaway)</span></span>
- <span data-ttu-id="ed450-165">استلام صنف أمر الشراء (وتخزينه)</span><span class="sxs-lookup"><span data-stu-id="ed450-165">Purchase order item receiving (and putaway)</span></span>

<span data-ttu-id="ed450-166">يتجاوز إعداد **إلى الموقع** لعنصر قائمة موقع الاستلام الافتراضي للمستودع، لجميع الأوامر التي تتم معالجتها باستخدام عنصر القائمة هذا.</span><span class="sxs-lookup"><span data-stu-id="ed450-166">The **To location** setting for a menu item overrides the default receiving location for the warehouse, for all orders that are processed by using that menu item.</span></span>

<span data-ttu-id="ed450-167">لإعداد عنصر قائمة جهاز محمول لدعم الاستلام في موقع مخصص، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ed450-167">To set up a mobile device menu item to support receiving at a custom location, follow these steps.</span></span>

1. <span data-ttu-id="ed450-168">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="ed450-168">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ed450-169">حدد أو أنشئ عنصر قائمة يستخدم إحدى عمليات إنشاء العمل التي تم ذكرها في وقت سابق في هذا القسم.</span><span class="sxs-lookup"><span data-stu-id="ed450-169">Select or create a menu item that uses one of the work creation processes that are listed earlier in this section.</span></span>
1. <span data-ttu-id="ed450-170">في علامة التبويب السريعة **عام**، عيّن الخيار **استخدام البيانات الافتراضية** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="ed450-170">On the **General** FastTab, set the **Use default data** option to **Yes**.</span></span>
1. <span data-ttu-id="ed450-171">في جزء الإجراء، حدد **البيانات الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="ed450-171">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="ed450-172">في صفحة **البيانات الافتراضية**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ed450-172">On the **Default data** page, set the following values:</span></span>

    - <span data-ttu-id="ed450-173">**حقل البيانات الافتراضية:** قم بتعيين هذا الحقل إلى *إلى الموقع*.</span><span class="sxs-lookup"><span data-stu-id="ed450-173">**Default data field:** Set this field to *To location*.</span></span>
    - <span data-ttu-id="ed450-174">**المستودع:** حدد المستودع الوجهة المطلوب استخدامه مع عنصر القائمة هذا.</span><span class="sxs-lookup"><span data-stu-id="ed450-174">**Warehouse:** Select the destination warehouse to use with this menu item.</span></span>
    - <span data-ttu-id="ed450-175">**الموقع:** يسرد هذا الحقل كافة معرفات المواقع المتاحة للمستودع المحدد.</span><span class="sxs-lookup"><span data-stu-id="ed450-175">**Location:** This field lists all the location IDs that are available for the selected warehouse.</span></span> <span data-ttu-id="ed450-176">ومع ذلك، ليس لإعداد هذا الحقل أي تأثير فعليًا.</span><span class="sxs-lookup"><span data-stu-id="ed450-176">However, the setting of this field doesn't actually have any effect.</span></span> <span data-ttu-id="ed450-177">وبالتالي، يمكنك تركه فارغًا.</span><span class="sxs-lookup"><span data-stu-id="ed450-177">Therefore, you can leave it blank.</span></span> <span data-ttu-id="ed450-178">ومع ذلك، يمكنك استخدام القائمة لتأكيد المعرف الذي يجب إدخاله في الحقل **قيمة يتعذر تغييرها**.</span><span class="sxs-lookup"><span data-stu-id="ed450-178">Nevertheless, you can use the list to confirm the ID that you must enter in the **Hardcoded value** field.</span></span>
    - <span data-ttu-id="ed450-179">**قيمة يتعذر تغييرها:** أدخل معرف الموقع لموقع الاستلام الذي ينطبق على عنصر القائمة هذا.</span><span class="sxs-lookup"><span data-stu-id="ed450-179">**Hardcoded value:** Enter the location ID for the receiving location that applies to this menu item.</span></span>

> [!TIP]
> <span data-ttu-id="ed450-180">لا يمكن تطبيق سياسة عمل الا إذا تم سرد كافة مواقع الاستلام في إعداد سياسة العمل ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="ed450-180">A work policy can be applied only if all the receiving locations are listed in the relevant work policy setup.</span></span> <span data-ttu-id="ed450-181">ينطبق هذا الشرط بغض النظر عما إذا كنت تستخدم موقع استلام المستودع الافتراضي أو موقع "إلى" مخصصًا.</span><span class="sxs-lookup"><span data-stu-id="ed450-181">This requirement applies regardless of whether you're using the default warehouse receiving location or a custom "to" location.</span></span>

## <a name="example-scenario-warehouse-receiving"></a><span data-ttu-id="ed450-182">السيناريو المثال: مستودع الاستلام</span><span class="sxs-lookup"><span data-stu-id="ed450-182">Example scenario: Warehouse receiving</span></span>

<span data-ttu-id="ed450-183">يجب تسجيل كافة المنتجات التي يتم استلامها بواسطة *استلام صنف أمر الشراء (وتخزينه)‬* في الموقع *FL-001*، ويجب أن ان تكون متوفرة في المستودع *24*.</span><span class="sxs-lookup"><span data-stu-id="ed450-183">All products that are received by the *Purchase order item receiving (and putaway)* process must be registered in location *FL-001*, and they must be available in warehouse *24*.</span></span> <span data-ttu-id="ed450-184">ومع ذلك، يجب عدم إنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="ed450-184">However, work should not be created.</span></span> <span data-ttu-id="ed450-185">يجب أن يتم تسجيل المنتجات المستلمة بواسطة أي عمليه أخرى (أي باستخدام عناصر قائمة جهاز محمول آخر) في موقع مستودع الاستلام الافتراضي (*RECV*)، ويجب إنشاء العمل كالمعتاد.</span><span class="sxs-lookup"><span data-stu-id="ed450-185">Products that are received by any other process (that is, by using other mobile device menu items) should be registered at the default warehouse receiving location (*RECV*), and work should be created as usual.</span></span> <span data-ttu-id="ed450-186">(لا يعرض هذا السيناريو إعداد الاستلام الافتراضي.)</span><span class="sxs-lookup"><span data-stu-id="ed450-186">(This scenario doesn't show the default receiving setup.)</span></span>

<span data-ttu-id="ed450-187">يتطلب هذا السيناريو العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="ed450-187">This scenario requires the following elements:</span></span>

- <span data-ttu-id="ed450-188">سياسة عمل لعملية *استلام صنف أمر الشراء (وتخزينه)‬* في الموقع *FL-001*، لجميع المنتجات</span><span class="sxs-lookup"><span data-stu-id="ed450-188">A work policy for the *Purchase order item receiving (and putaway)* process in location *FL-001*, for all products</span></span>
- <span data-ttu-id="ed450-189">عنصر قائمة جهاز محمول يتضمن بيانات افتراضية، ويعيّن الحقل **إلى الموقع** إلى *FL-001*</span><span class="sxs-lookup"><span data-stu-id="ed450-189">A mobile device menu item that has default data, and that sets the **To location** field to *FL-001*</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ed450-190">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="ed450-190">Prerequisites</span></span>

<span data-ttu-id="ed450-191">لجعل الوظيفة الموضحة في هذا السيناريو متوفرة في النظام، يجب عليك تشغيل الميزتين *تحسينات استلام لوحة الترخيص* و*تحسينات سياسة العمل للعمل الوارد* في [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ed450-191">To make the functionality that is described in this scenario available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="ed450-192">يستخدم هذا السيناريو بيانات العرض التوضيحي القياسية.</span><span class="sxs-lookup"><span data-stu-id="ed450-192">This scenario uses the standard demo data.</span></span> <span data-ttu-id="ed450-193">وبالتالي، إذا أردت العمل عبر هذا السيناريو باستخدام القيم المتوفرة هنا، يجب أن تعمل على نظام حيث تم تثبيت بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="ed450-193">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="ed450-194">بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ed450-194">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-work-policy"></a><span data-ttu-id="ed450-195">إعداد سياسة عمل</span><span class="sxs-lookup"><span data-stu-id="ed450-195">Set up a work policy</span></span>

1. <span data-ttu-id="ed450-196">انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> سياسات العمل**.</span><span class="sxs-lookup"><span data-stu-id="ed450-196">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="ed450-197">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ed450-197">Select **New**.</span></span>
1. <span data-ttu-id="ed450-198">في حقل **اسم سياسة العمل**، أدخل *لا يوجد عمل تخزين لصنف الشراء*.</span><span class="sxs-lookup"><span data-stu-id="ed450-198">In the **Work policy name** field, enter *No purchase item putaway work*.</span></span>
1. <span data-ttu-id="ed450-199">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ed450-199">Select **Save**.</span></span>
1. <span data-ttu-id="ed450-200">على علامة التبويب السريعة **أنواع أوامر العمل**، حدد **إضافة** لإضافة صف إلى الشبكة، ثم عيّن القيم التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="ed450-200">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="ed450-201">**نوع أمر العمل:** *أوامر الشراء*</span><span class="sxs-lookup"><span data-stu-id="ed450-201">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="ed450-202">**عملية العمل:** *استلام صنف أمر الشراء (وتخزينه)*</span><span class="sxs-lookup"><span data-stu-id="ed450-202">**Work process:** *Purchase order item receiving (and putaway)*</span></span>
    - <span data-ttu-id="ed450-203">**أسلوب إنشاء العمل:** *إطلاقًا*</span><span class="sxs-lookup"><span data-stu-id="ed450-203">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="ed450-204">**اسم سياسة توزيع البضائع:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="ed450-204">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="ed450-205">على علامة التبويب السريعة **مواقع المخزون**، حدد **إضافة** لإضافة صف إلى الشبكة، ثم عيّن القيم التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="ed450-205">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="ed450-206">**المستودع:** *24*</span><span class="sxs-lookup"><span data-stu-id="ed450-206">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="ed450-207">**الموقع:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="ed450-207">**Location:** *FL-001*</span></span>

1. <span data-ttu-id="ed450-208">على علامة التبويب السريعة **المنتجات**، قم بتعيين حقل **تحديد المنتج** على *الكل*.</span><span class="sxs-lookup"><span data-stu-id="ed450-208">On the **Products** FastTab, set the **Product selection** field to *All*.</span></span>
1. <span data-ttu-id="ed450-209">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ed450-209">Select **Save**.</span></span>

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a><span data-ttu-id="ed450-210">إعداد عنصر قائمة جهاز محمول لتغيير موقع الاستلام</span><span class="sxs-lookup"><span data-stu-id="ed450-210">Set up a mobile device menu item to change the receiving location</span></span>

1. <span data-ttu-id="ed450-211">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="ed450-211">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ed450-212">في الجزء الأيمن، حدد عنصر القائمة **استلام الشراء**.</span><span class="sxs-lookup"><span data-stu-id="ed450-212">In the left pane, select the existing **Purchase receive** menu item.</span></span>
1. <span data-ttu-id="ed450-213">في علامة التبويب السريعة **عام**، عيّن الخيار **استخدام البيانات الافتراضية** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="ed450-213">On the **General** FastTab, set the **Use default data** option to *Yes*.</span></span>
1. <span data-ttu-id="ed450-214">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ed450-214">Select **Save**.</span></span>
1. <span data-ttu-id="ed450-215">في جزء الإجراء، حدد **البيانات الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="ed450-215">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="ed450-216">في صفحة **البيانات الافتراضية**، في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة، ثم عيّن القيم التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="ed450-216">On the **Default data** page, on the Action Pane, select **New** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="ed450-217">**حقل البيانات الافتراضية:** *إلى الموقع*</span><span class="sxs-lookup"><span data-stu-id="ed450-217">**Default data field:** *To location*</span></span>
    - <span data-ttu-id="ed450-218">**المستودع:** *24*</span><span class="sxs-lookup"><span data-stu-id="ed450-218">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="ed450-219">**الموقع:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="ed450-219">**Location:** Leave this field blank.</span></span>
    - <span data-ttu-id="ed450-220">**قيمة يتعذر تغييرها:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="ed450-220">**Hardcoded value:** *FL-001*</span></span>

1. <span data-ttu-id="ed450-221">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ed450-221">Select **Save**.</span></span>

### <a name="receive-a-purchase-order-without-creating-work"></a><span data-ttu-id="ed450-222">استلام أمر شراء بدون إنشاء العمل</span><span class="sxs-lookup"><span data-stu-id="ed450-222">Receive a purchase order without creating work</span></span>

<span data-ttu-id="ed450-223">يوضح المثال الوارد في هذا القسم كيفية استلام صنف أمر شراء، ولكن بدون إنشاء العمل، في موقع يختلف عن موقع الاستلام الافتراضي الذي تم إعداده للمستودع.</span><span class="sxs-lookup"><span data-stu-id="ed450-223">The example in this section shows how to receive a purchase order item, but without creating work, at a location that differs from the default receiving location that is set up for the warehouse.</span></span> <span data-ttu-id="ed450-224">يستخدم هذا المثال سياسة العمل وعنصر الجهاز المحمول الذي أنشأته سابقًا في هذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="ed450-224">This example uses the work policy and mobile device item that you created earlier in this scenario.</span></span>

#### <a name="create-a-purchase-order"></a><span data-ttu-id="ed450-225">إنشاء أمر شراء</span><span class="sxs-lookup"><span data-stu-id="ed450-225">Create a purchase order</span></span>

1. <span data-ttu-id="ed450-226">انتقل إلى **التدبير والتوريد \> أوامر الشراء \> كل أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="ed450-226">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="ed450-227">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ed450-227">Select **New**.</span></span>
1. <span data-ttu-id="ed450-228">في مربع الحوار **إنشاء أمر شراء**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ed450-228">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ed450-229">**حساب المورّد:** *US-101*</span><span class="sxs-lookup"><span data-stu-id="ed450-229">**Vendor account:** *US-101*</span></span>
    - <span data-ttu-id="ed450-230">**الموقع:** *2*</span><span class="sxs-lookup"><span data-stu-id="ed450-230">**Site:** *2*</span></span>
    - <span data-ttu-id="ed450-231">**المستودع:** *24*</span><span class="sxs-lookup"><span data-stu-id="ed450-231">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="ed450-232">حدد **موافق** لإغلاق مربع الحوار وفتح أمر الشراء الجديد.</span><span class="sxs-lookup"><span data-stu-id="ed450-232">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="ed450-233">على علامة التبويب السريعة **بنود أمر الشراء**، قم بتعيين القيم التالية للصف الفارغ:</span><span class="sxs-lookup"><span data-stu-id="ed450-233">On the **Purchase order lines** FastTab, set the following values for the empty row:</span></span>

    - <span data-ttu-id="ed450-234">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ed450-234">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="ed450-235">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="ed450-235">**Quantity:** *1*</span></span>

1. <span data-ttu-id="ed450-236">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ed450-236">Select **Save**.</span></span>
1. <span data-ttu-id="ed450-237">تدوين ملاحظة برقم أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="ed450-237">Make a note of the purchase order number.</span></span>

#### <a name="receive-a-purchase-order"></a><span data-ttu-id="ed450-238">استلام أمر شراء</span><span class="sxs-lookup"><span data-stu-id="ed450-238">Receive a purchase order</span></span>

1. <span data-ttu-id="ed450-239">على الجهاز المحمول، سجل دخولك إلى المستودع *24* باستخدام *24* كمعرف المستخدم و *1* ككلمة المرور.</span><span class="sxs-lookup"><span data-stu-id="ed450-239">On the mobile device, sign in to warehouse *24* by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="ed450-240">حدد **الوارد**.</span><span class="sxs-lookup"><span data-stu-id="ed450-240">Select **Inbound**.</span></span>
1. <span data-ttu-id="ed450-241">حدد **استلام الشراء**.</span><span class="sxs-lookup"><span data-stu-id="ed450-241">Select **Purchase receive**.</span></span> <span data-ttu-id="ed450-242">يجب تعيين حقل **الموقع** إلى *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="ed450-242">The **Location** field should be set to *FL-001*.</span></span>
1. <span data-ttu-id="ed450-243">أدخل رقم أمر الشراء لأمر الشراء الذي أنشأته في الاجراء السابق.</span><span class="sxs-lookup"><span data-stu-id="ed450-243">Enter the purchase order number for the purchase order that you created in the previous procedure.</span></span>
1. <span data-ttu-id="ed450-244">في الحقل **رقم الصنف**، أدخل *A0001*.</span><span class="sxs-lookup"><span data-stu-id="ed450-244">In the **Item number** field, enter *A0001*.</span></span>
1. <span data-ttu-id="ed450-245">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ed450-245">Select **OK**.</span></span>
1. <span data-ttu-id="ed450-246">في حقل **كمية** ، أدخل *1*.</span><span class="sxs-lookup"><span data-stu-id="ed450-246">In the **Quantity** field, enter *1*.</span></span>
1. <span data-ttu-id="ed450-247">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ed450-247">Select **OK**.</span></span>

<span data-ttu-id="ed450-248">تم الآن استلام أمر الشراء، ولكن لا يوجد عمل مقترن به.</span><span class="sxs-lookup"><span data-stu-id="ed450-248">The purchase order is now received, but no work is associated with it.</span></span> <span data-ttu-id="ed450-249">تم تحديث المخزون الفعلي، وتتوفر الآن الكمية *1* للصنف *A0001* في الموقع *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="ed450-249">The on-hand inventory has been updated, and a quantity of *1* of item *A0001* is now available at location *FL-001*.</span></span>

## <a name="example-scenario-manufacturing"></a><span data-ttu-id="ed450-250">السيناريو المثال: التصنيع</span><span class="sxs-lookup"><span data-stu-id="ed450-250">Example scenario: Manufacturing</span></span>

<span data-ttu-id="ed450-251">في المثال التالي، هناك أمرا إنتاج، *PRD-001* و*PRD-002*.</span><span class="sxs-lookup"><span data-stu-id="ed450-251">In the following example, there are two production orders, *PRD-001* and *PRD-002*.</span></span> <span data-ttu-id="ed450-252">يتضمن أمر الإنتاج *PRD-001* عملية تسمى *التجميع*، حيث يتم الإبلاغ عن المنتج *SC1* كمنتج منتهٍ في الموقع *001*.</span><span class="sxs-lookup"><span data-stu-id="ed450-252">Production order *PRD-001* has an operation that is named *Assembly*, where product *SC1* is being reported as finished to location *001*.</span></span> <span data-ttu-id="ed450-253">ويتضمن أمر الإنتاج *PRD-002* عملية تسمى *الطلاء* وهو يستهلك المنتج *SC1* من الموقع *001*.</span><span class="sxs-lookup"><span data-stu-id="ed450-253">Production order *PRD-002* has an operation that is named *Painting* and consumes product *SC1* from location *001*.</span></span> <span data-ttu-id="ed450-254">يستهلك أمر الإنتاج *PRD-002* أيضًا المواد الخام *RM1* من الموقع *001*.</span><span class="sxs-lookup"><span data-stu-id="ed450-254">Production order *PRD-002* also consumes raw material *RM1* from location *001*.</span></span> <span data-ttu-id="ed450-255">تكون المواد الخام *RM1* مخزنة في موقع المستودع *BULK-001* وسيتم نقل هذه المواد إلى الموقع *001* بواسطة عامل المستودع لانتقاء المواد الخام.</span><span class="sxs-lookup"><span data-stu-id="ed450-255">Raw material *RM1* is stored in warehouse location *BULK-001* and will be picked to location *001* by warehouse work for raw material picking.</span></span> <span data-ttu-id="ed450-256">يتم إنشاء عمل الانتقاء عند إصدار أمر الإنتاج *PRD-002*.</span><span class="sxs-lookup"><span data-stu-id="ed450-256">The picking work is generated when production *PRD-002* is released.</span></span>

<span data-ttu-id="ed450-257">[![سياسات عمل المستودع](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="ed450-257">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span>

<span data-ttu-id="ed450-258">عندما تخطط لتكوين سياسة عمل المستودع لهذا السيناريو، يجب مراعاة النقاط التالية:</span><span class="sxs-lookup"><span data-stu-id="ed450-258">When you're planning to configure a warehouse work policy for this scenario, you should consider the following points:</span></span>

- <span data-ttu-id="ed450-259">عمل المستودع لتخزين البضائع المنتهية غير مطلوب عند التبليغ عن المنتج *SC1* كمنتج منتهٍ من أمر الإنتاج *PRD-001* إلى الموقع *001‎*.</span><span class="sxs-lookup"><span data-stu-id="ed450-259">Warehouse work for putaway of finished goods isn't required when you report product *SC1* as finished from production order *PRD-001* to location *001*.</span></span> <span data-ttu-id="ed450-260">وسبب ذلك هو أن عملية *الطلاء* لأمر الإنتاج *PRD-002* تستهلك المنتج *SC1* في الموقع نفسه.</span><span class="sxs-lookup"><span data-stu-id="ed450-260">The reason is that the *Painting* operation for production order *PRD-002* consumes product *SC1* at the same location.</span></span>
- <span data-ttu-id="ed450-261">عمل المستودع لانتقاء المواد الخام مطلوب لنقل المواد الخام *RM1* من موقع المستودع *BULK-001* إلى الموقع *001*.</span><span class="sxs-lookup"><span data-stu-id="ed450-261">Warehouse work for raw material picking is required to move raw material *RM1* from warehouse location *BULK-001* to location *001*.</span></span>

<span data-ttu-id="ed450-262">إليك مثال عن سياسة العمل التي يمكنك إعدادها، استنادًا إلى هذه الاعتبارات:</span><span class="sxs-lookup"><span data-stu-id="ed450-262">Here is an example of a work policy that you can set up, based on these considerations:</span></span>

- <span data-ttu-id="ed450-263">**اسم سياسة العمل:** *لا يوجد عمل تخزين*</span><span class="sxs-lookup"><span data-stu-id="ed450-263">**Work policy name:** *No putaway work*</span></span>
- <span data-ttu-id="ed450-264">**أنواع أوامر العمل:** *تخزين البضائع المنتهية‬* و*تخزين منتج مساعد ومنتج ثانوي‬*</span><span class="sxs-lookup"><span data-stu-id="ed450-264">**Work order types:** *Finished goods put away* and *Co-product and by-product put away*</span></span>
- <span data-ttu-id="ed450-265">**مواقع المخزون:** المستودع *51* والموقع *001*</span><span class="sxs-lookup"><span data-stu-id="ed450-265">**Inventory locations:** Warehouse *51* and location *001*</span></span>
- <span data-ttu-id="ed450-266">**المنتجات:** *SC1*</span><span class="sxs-lookup"><span data-stu-id="ed450-266">**Products:** *SC1*</span></span>

<span data-ttu-id="ed450-267">يوفر السيناريو المثال التالي إرشادات خطوة بخطوة حول كيفية إعداد سياسة عمل المستودع لهذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="ed450-267">The following example scenario provides step-by-step instructions for setting up the warehouse work policy for this scenario.</span></span>

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="ed450-268">السيناريو المثال: الإبلاغ عن أمر إنتاج كمنتهٍ في موقع غير خاضع لمراقبة لوحة ترخيص</span><span class="sxs-lookup"><span data-stu-id="ed450-268">Example scenario: Report as finished to a location that isn't license plate–controlled</span></span>

<span data-ttu-id="ed450-269">يعرض هذا السيناريو مثالاً حيث يتم الإبلاغ عن أمر إنتاج كمنتهٍ إلى موقع غير خاضع لمراقبة لوحة الترخيص.‬</span><span class="sxs-lookup"><span data-stu-id="ed450-269">This scenario shows an example where a production order is reported as finished to a location that isn't license plate–controlled.</span></span>

<span data-ttu-id="ed450-270">يستخدم هذا السيناريو بيانات العرض التوضيحي القياسية.</span><span class="sxs-lookup"><span data-stu-id="ed450-270">This scenario uses the standard demo data.</span></span> <span data-ttu-id="ed450-271">وبالتالي، إذا أردت العمل عبر هذا السيناريو باستخدام القيم المتوفرة هنا، يجب أن تعمل على نظام حيث تم تثبيت بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="ed450-271">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="ed450-272">بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ed450-272">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="ed450-273">إعداد سياسة عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="ed450-273">Set up a warehouse work policy</span></span>

<span data-ttu-id="ed450-274">لا تشمل عمليات المستودع دائمًا عمل المستودع.</span><span class="sxs-lookup"><span data-stu-id="ed450-274">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="ed450-275">من خلال تحديد سياسة العمل، يمكنك منع إنشاء عمل لانتقاء المواد الخام وتخزين البضائع المنتهية بعيدًا مجموعة من المنتجات في مواقع محددة.</span><span class="sxs-lookup"><span data-stu-id="ed450-275">By defining a work policy, you can prevent the creation of work for raw material picking and putaway of finished goods for a set of products at specific locations.</span></span>

1. <span data-ttu-id="ed450-276">انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> سياسات العمل**.</span><span class="sxs-lookup"><span data-stu-id="ed450-276">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="ed450-277">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ed450-277">Select **New**.</span></span>
1. <span data-ttu-id="ed450-278">في حقل **اسم سياسة العمل**، أدخل *لا يوجد عمل تخزين*.</span><span class="sxs-lookup"><span data-stu-id="ed450-278">In the **Work policy name** field, enter *No putaway work*.</span></span>
1. <span data-ttu-id="ed450-279">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ed450-279">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ed450-280">على علامة التبويب السريعة **أنواع أوامر العمل**، حدد **إضافة** لإضافة صف إلى الشبكة، ثم عيّن القيم التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="ed450-280">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="ed450-281">**نوع أمر العمل:** *تخزين البضائع المنتهية‬*</span><span class="sxs-lookup"><span data-stu-id="ed450-281">**Work order type:** *Finished goods put away*</span></span>
    - <span data-ttu-id="ed450-282">**عملية العمل:** *جميع عمليات العمل ذات الصلة*</span><span class="sxs-lookup"><span data-stu-id="ed450-282">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="ed450-283">**أسلوب إنشاء العمل:** *إطلاقًا*</span><span class="sxs-lookup"><span data-stu-id="ed450-283">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="ed450-284">**اسم سياسة توزيع البضائع:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="ed450-284">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="ed450-285">حدد **إضافة** لإضافة صف ثانٍ إلى الشبكة، ثم عيّن القيم التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="ed450-285">Select **Add** again to add a second row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="ed450-286">**نوع أمر العمل:** *مخزون المنتج المساعد والمنتج الثانوي*</span><span class="sxs-lookup"><span data-stu-id="ed450-286">**Work order type:** *Co-product and by-product put away*</span></span>
    - <span data-ttu-id="ed450-287">**عملية العمل:** *جميع عمليات العمل ذات الصلة*</span><span class="sxs-lookup"><span data-stu-id="ed450-287">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="ed450-288">**أسلوب إنشاء العمل:** *إطلاقًا*</span><span class="sxs-lookup"><span data-stu-id="ed450-288">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="ed450-289">**اسم سياسة توزيع البضائع:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="ed450-289">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="ed450-290">على علامة التبويب السريعة **مواقع المخزون**، حدد **إضافة** لإضافة صف إلى الشبكة، ثم عيّن القيم التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="ed450-290">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="ed450-291">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="ed450-291">**Warehouse:** *51*</span></span>
    - <span data-ttu-id="ed450-292">**الموقع:** *001*</span><span class="sxs-lookup"><span data-stu-id="ed450-292">**Location:** *001*</span></span>

1. <span data-ttu-id="ed450-293">على علامة التبويب السريعة **المنتجات**، قم بتعيين حقل **تحديد المنتج** على *محدد*.</span><span class="sxs-lookup"><span data-stu-id="ed450-293">On the **Products** FastTab, set the **Product selection** field to *Selected*.</span></span>
1. <span data-ttu-id="ed450-294">في علامة التبويب السريعة **المنتجات**، حدد **إضافة** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="ed450-294">On the **Products** FastTab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="ed450-295">في الصف الجديد، قم بتعيين الحقل **رقم الصنف** إلى *L0101*.</span><span class="sxs-lookup"><span data-stu-id="ed450-295">In the new row, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="ed450-296">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ed450-296">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-an-output-location"></a><span data-ttu-id="ed450-297">إعداد موقع المخرجات</span><span class="sxs-lookup"><span data-stu-id="ed450-297">Set up an output location</span></span>

1. <span data-ttu-id="ed450-298">انتقل إلى **إدارة المؤسسة \> الموارد \> مجموعات الموارد**.</span><span class="sxs-lookup"><span data-stu-id="ed450-298">Go to **Organization administration \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="ed450-299">في الجزء الأيمن، حدد مجموعة الموارد **5102**.</span><span class="sxs-lookup"><span data-stu-id="ed450-299">In the left pane, select resource group **5102**.</span></span>
1. <span data-ttu-id="ed450-300">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ed450-300">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="ed450-301">**مستودع المخرجات:** *51*</span><span class="sxs-lookup"><span data-stu-id="ed450-301">**Output warehouse:** *51*</span></span>
    - <span data-ttu-id="ed450-302">**موقع المخرجات:** *001*</span><span class="sxs-lookup"><span data-stu-id="ed450-302">**Output location:** *001*</span></span>

1. <span data-ttu-id="ed450-303">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ed450-303">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="ed450-304">الموقع *001* غير خاضع لمراقبة لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="ed450-304">Location *001* isn't a license plate–controlled location.</span></span> <span data-ttu-id="ed450-305">يمكنك إعداد موقع مخرجات غير خاضع لمراقبة لوحة الترخيص فقط في حالة وجود سياسة عمل قابلة للتطبيق للموقع.</span><span class="sxs-lookup"><span data-stu-id="ed450-305">You can set up an output location that isn't license plate–controlled only if an applicable work policy exists for the location.</span></span>

### <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="ed450-306">إنشاء أمر الإنتاج والإبلاغ عنه كمنته</span><span class="sxs-lookup"><span data-stu-id="ed450-306">Create a production order and report it as finished</span></span>

1. <span data-ttu-id="ed450-307">انتقل إلى **التحكم بالإنتاج \> أوامر الإنتاج \> كافة أوامر الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="ed450-307">Go to **Production control \> Production orders \> All production orders**.</span></span>
1. <span data-ttu-id="ed450-308">في جزء الإجراءات، حدد **أمر إنتاج جديد**.</span><span class="sxs-lookup"><span data-stu-id="ed450-308">On the Action Pane, select **New production order**.</span></span>
1. <span data-ttu-id="ed450-309">في مربع الحوار **إنشاء أمر إنتاج**، قم بتعيين حقل **رقم الصنف** إلى *L0101*.</span><span class="sxs-lookup"><span data-stu-id="ed450-309">In the **Create production order** dialog box, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="ed450-310">حدد **إنشاء** لإنشاء الأمر وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="ed450-310">Select **Create** to create the order and close the dialog box.</span></span>

    <span data-ttu-id="ed450-311">يُضاف أمر إنتاج جديد إلى الشبكة في الصفحة **كافة أوامر الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="ed450-311">A new production order is added to the grid on the **All production orders** page.</span></span>

    <span data-ttu-id="ed450-312">حافظ على أمر الإنتاج محددًا.</span><span class="sxs-lookup"><span data-stu-id="ed450-312">Keep the new production order selected.</span></span>

1. <span data-ttu-id="ed450-313">في جزء الإجراءات، في علامة تبويب **أمر الإنتاج** في مجموعة **العملية‏‎‬**، حدد **تقدير**.</span><span class="sxs-lookup"><span data-stu-id="ed450-313">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Estimate**.</span></span>
1. <span data-ttu-id="ed450-314">في مربع الحوار **تقدير**، أقرا التقدير، ثم حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="ed450-314">In the **Estimate** dialog box, read the estimate, and then select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="ed450-315">في جزء الإجراءات، في علامة تبويب **أمر الإنتاج** في مجموعة **العملية‏‎‬**، حدد **بدء**.</span><span class="sxs-lookup"><span data-stu-id="ed450-315">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Start**.</span></span>
1. <span data-ttu-id="ed450-316">في مربع الحوار **بدء**، في علامة التبويب **عام**، قم بتعيين الحقل **استهلاك تلقائي لقائمة مكونات الصنف** إلى *إطلاقًا*.</span><span class="sxs-lookup"><span data-stu-id="ed450-316">In the **Start** dialog box, on the **General** tab, set the **Automatic BOM consumption** field to *Never*.</span></span>
1. <span data-ttu-id="ed450-317">حدد **موافق** لحفظ إعدادك وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="ed450-317">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="ed450-318">في جزء الإجراءات، في علامة تبويب **أمر الإنتاج** في مجموعة **العملية‏‎‬**، حدد **الإبلاغ كمنته**.</span><span class="sxs-lookup"><span data-stu-id="ed450-318">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Report as finished**.</span></span>
1. <span data-ttu-id="ed450-319">في مربع الحوار **الإبلاغ كمنته**، على علامة التبويب **عام**، عيّن الخيار **قبول الخطأ** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="ed450-319">In the **Report as finished** dialog box, on the **General** tab, set the **Accept error** option to *Yes*.</span></span>
1. <span data-ttu-id="ed450-320">حدد **موافق** لحفظ إعدادك وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="ed450-320">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="ed450-321">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، في مجموعة **عام**، حدد **تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="ed450-321">On the Action Pane, on the **Warehouse** tab, in the **General** group, select **Work details**.</span></span>

<span data-ttu-id="ed450-322">عندما يتم الإبلاغ عن أمر الإنتاج كمنته، لا يتم إنشاء عمل للتخزين.</span><span class="sxs-lookup"><span data-stu-id="ed450-322">When the production order is reported as finished, no work is generated for putaway.</span></span> <span data-ttu-id="ed450-323">يحدث هذا السلوك بسبب تعريف سياسة عمل تمنع إنشاء العمل عندما يتم الإبلاغ عن المنتج *L0101* كمنته للموقع *001*.</span><span class="sxs-lookup"><span data-stu-id="ed450-323">This behavior occurs because a work policy is defined that prevents work from being generated when product *L0101* is reported as finished to location *001*.</span></span>

## <a name="more-information"></a><span data-ttu-id="ed450-324">مزيد من المعلومات</span><span class="sxs-lookup"><span data-stu-id="ed450-324">More information</span></span>

<span data-ttu-id="ed450-325">لمزيد من المعلومات حول عناصر قائمة الجهاز المحمول، راجع [إعداد الأجهزة المحمولة لعمل المستودع](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="ed450-325">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

<span data-ttu-id="ed450-326">للحصول على مزيد من المعلومات حول استلام لوحة الترخيص وسياسات العمل، راجع [استلام لوحة الترخيص من خلال تطبيق المستودع](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="ed450-326">For more information about license plate receiving and work policies, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="ed450-327">للحصول على معلومات حول إدارة الأحمال الواردة، راجع [معالجة المستودع للأحمال الواردة لأوامر الشراء‬](inbound-load-handling.md).</span><span class="sxs-lookup"><span data-stu-id="ed450-327">For more information about inbound load management, see [Warehouse handling of inbound loads for purchase orders](inbound-load-handling.md).</span></span>
