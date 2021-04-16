---
title: خلط أبعاد المنتج في الموقع
description: يوفر هذا الموضوع معلومات حول مزج أبعاد المنتج في الموقع. تساعد وظيفة ملف تعريف الموقع هذه في تحسين إدارة الموقع عند استخدام متغيرات منتجات أو منتجات لها أبعاد، كما هو الحال في صناعة الأزياء. ويتيح لك تحديد ما إذا كان يمكن خلط التكوينات والألوان والأنماط والأحجام لملف تعريف موقع معين، أو ما إذا كان من الممكن وضع إحدى هذه الأبعاد أو توليفة منها فقط في نفس الموقع.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 28f59052a74b6d8b263c7a8a8b6061f2c4b34c89
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831280"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="ef2d6-105">خلط أبعاد المنتج في الموقع</span><span class="sxs-lookup"><span data-stu-id="ef2d6-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef2d6-106">مزج أبعاد المنتج في الموقع هي وظيفة ملف تعريف الموقع التي تساعد في تحسين إدارة الموقع عند استخدام متغيرات منتجات أو منتجات لها أبعاد، كما هو الحال في صناعة الأزياء.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="ef2d6-107">ويتيح لك تحديد ما إذا كان يمكن خلط التكوينات والألوان والأنماط والأحجام لملف تعريف موقع معين، أو ما إذا كان من الممكن وضع إحدى هذه الأبعاد أو توليفة منها فقط في نفس الموقع.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="ef2d6-108">تشغيل ميزة مزج أبعاد المنتج للموقع</span><span class="sxs-lookup"><span data-stu-id="ef2d6-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="ef2d6-109">قبل أن تتمكن من استخدام ميزة مزج أبعاد المنتج للموقع، يجب تشغيلها في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="ef2d6-110">بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="ef2d6-111">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="ef2d6-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ef2d6-112">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ef2d6-113">**اسم الميزة:** *مزج أبعاد المنتج للموقع*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="ef2d6-114">الإعداد</span><span class="sxs-lookup"><span data-stu-id="ef2d6-114">Setup</span></span>

<span data-ttu-id="ef2d6-115">يحتاج كل موقع في المستودع إلى ملف تعريف موقع يقترن به ويصف خصائص الموقع.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="ef2d6-116">بالتالي، ستتمكن كافة المواقع التي تستخدم نفس ملف التعريف من السماح بمزج أبعاد المنتج بعد إعدادها.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="ef2d6-117">تكوين ملفات تعريف المواقع للسماح بمزج أبعاد المنتج</span><span class="sxs-lookup"><span data-stu-id="ef2d6-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="ef2d6-118">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> ملفات تعريف الموقع**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="ef2d6-119">في قائمه ملفات تعريف المواقع، حدد **مجمع**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="ef2d6-120">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ef2d6-121">في علامة التبويب السريعة **عام**، قم بتعيين خيار **تمكين مزج أبعاد المنتج للموقع** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef2d6-122">يمكنك تعيين هذا الخيار إلى *نعم* فقط إذا تم تعيين خيار **السماح بالعناصر المختلطة** إلى *لا*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="ef2d6-123">في علامة التبويب السريعة **مزج أبعاد المنتج المسموح بها**، قم بتعيين خيار **الحجم** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="ef2d6-124">في السيناريو الموضح في هذا الموضوع، يمكن إجراء المزج فقط للمنتجات التي لها أبعاد **حجم** مختلفة.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="ef2d6-125">مع ذلك، تتوفر أيضًا خيارات أخرى.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-125">However, other options are also available.</span></span>
1. <span data-ttu-id="ef2d6-126">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="ef2d6-127">إنشاء أصل منتج واحد ومتغيرات المنتجات</span><span class="sxs-lookup"><span data-stu-id="ef2d6-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="ef2d6-128">‏‫انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> أصول المنتجات‬‬**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="ef2d6-129">في جزء الإجراءات، حدد **جديد** لإنشاء أصل منتج.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="ef2d6-130">في مربع الحوار **منتج جديد**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ef2d6-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ef2d6-131">**نوع المنتج:** *الصنف*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="ef2d6-132">**النوع الفرعي للمنتج:** *أصل المنتج*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="ef2d6-133">**رقم المنتج:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="ef2d6-134">**اسم المنتج:** *حجم B0001*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="ef2d6-135">**مجموعة أبعاد المنتج:** *الحجم*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="ef2d6-136">**تقنية التكوين:** *متغير محدد مسبقًا*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="ef2d6-137">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-137">Select **OK**.</span></span>
1. <span data-ttu-id="ef2d6-138">في صفحة **تفاصيل المنتج**، ضمن علامة التبويب **عام**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ef2d6-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="ef2d6-139">**إنشاء متغيرات تلقائيًا:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="ef2d6-140">**مجموعة الحجم:** *CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="ef2d6-141">لعرض المتغيرات المعرفة مسبقًا، في جزء الإجراءات، حدد **متغيرات المنتج**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="ef2d6-142">تظهر صفحة **متغيرات المنتج** وتعرض قائمة بالمتغيرات من تكوين مجموعة الحجم.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="ef2d6-143">إصدار المنتجات إلى شركة USMF</span><span class="sxs-lookup"><span data-stu-id="ef2d6-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="ef2d6-144">في جزء الإجراءات، حدد **إصدار المنتج**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="ef2d6-145">في صفحة **تحديد منتجات لإصدارها**، تأكد من وجود رقم المنتج *B0001* في القائمة، ثم حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="ef2d6-146">حدد **التالي** لتأكيد متغيرات المنتج المطلوب إصدارها.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="ef2d6-147">من صفحة **تحديد الشركات للإصدار إليها**، حدد *USMF*، ثم حدد **التالي** لتأكيد التحديد.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-147">On the **Select companies to release to** page, select *USMF*, and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="ef2d6-148">في صفحة **تأكيد التحديد**، حدد **إنهاء** لإكمال الإصدار.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="ef2d6-149">تظهر لك رسالة "اكتملت العملية".</span><span class="sxs-lookup"><span data-stu-id="ef2d6-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="ef2d6-150">تحديث منتج تم إصداره في شركة USMF</span><span class="sxs-lookup"><span data-stu-id="ef2d6-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="ef2d6-151">تأكد من أنك قمت بتسجيل الدخول إلى شركة **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="ef2d6-152">انتقل إلى **إدارة معلومات المنتج \> المنتجات \> المنتجات المُصدرة** لإنهاء إنشاء المنتج المُصدر.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="ef2d6-153">ابحث عن وحدد رقم الصنف *B0001* لفتح صفحة **تفاصيل المنتج التي تم إصدارها**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="ef2d6-154">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ef2d6-155">في علامة التبويب السريعة **عام**، تأكد من تعيين حقل **مجموعة نماذج الأصناف** إلى *FIFO*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="ef2d6-156">في جزء الإجراءات، في علامة تبويب **المنتج** في مجموعة **إعداد‬**، حدد **مجموعات الأبعاد**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="ef2d6-157">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ef2d6-157">Set the following values:</span></span>

    - <span data-ttu-id="ef2d6-158">**مجموعة أبعاد التخزين:** *Ware*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="ef2d6-159">**مجموعة أبعاد التعقب:** *بلا*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="ef2d6-160">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-160">Select **OK**.</span></span>
1. <span data-ttu-id="ef2d6-161">في جزء الإجراءات، في علامة تبويب **المنتج** في مجموعة **إعداد‬**، حدد **‏‫التدرج الهرمي للحجز‬**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="ef2d6-162">قم بتعيين حقل **التدرج الهرمي للحجز** إلى *الافتراضي*، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-162">Set the **Reservation hierarchy** field to *Default*, and then select **OK**.</span></span>
1. <span data-ttu-id="ef2d6-163">في علامة التبويب السريعة **عام**، في قسم **الإدارة**، لاحظ أنه تم تحديث التحديدات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="ef2d6-164">في علامة التبويب السريعة **الشراء**، في حقل **السعر**، أدخل *10*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="ef2d6-165">في علامة التبويب السريعة **إدارة التكاليف**، في حقل **مجموعة الأصناف**، أدخل *صوتيات*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="ef2d6-166">في علامة التبويب السريعة **الشراء**، في حقل **السعر**، أدخل *10*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="ef2d6-167">في علامة التبويب السريعة **المستودع**، في حقل **معرف مجموعة تسلسل الوحدة**، أدخل *ea*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="ef2d6-168">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="ef2d6-169">إنشاء توجيه موقع</span><span class="sxs-lookup"><span data-stu-id="ef2d6-169">Create a location directive</span></span>

1. <span data-ttu-id="ef2d6-170">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="ef2d6-171">في الجزء الأيسر في حقل **نوع أمر العمل**، حدد *أوامر الشراء*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="ef2d6-172">في القائمة، حدد توجيه الموقع الذي يسمي *24 أمر شراء مباشر*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="ef2d6-173">في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **جديد** لإضافة سطر إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="ef2d6-174">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ef2d6-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ef2d6-175">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="ef2d6-176">يجب أن يكون البند الجديد أالبند الموجود سابقا.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="ef2d6-177">لإجراء التغيير، استخدم الزرين **تحريك لأعلى** و **تحريك لأسفل** على شريط الأدوات، أو قم بتغيير قيمة **رقم التسلسل** للبند الموجود إلى *2*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="ef2d6-178">**الاسم:** *الوضع في ملف تعريف الموقع BULK*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="ef2d6-179">**استخدام الموقع الثابت:** *المواقع الثابتة وغير الثابتة*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="ef2d6-180">**السماح بالمخزون السالب:** *قم بإلغاء تحديد خانة الاختيار هذه (= لا)*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="ef2d6-181">**تمكين الدفعة:** *قم بإلغاء تحديد خانة الاختيار هذه (= لا)*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="ef2d6-182">**الاستراتيجية:** *بلا*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="ef2d6-183">في أثناء تحديد السطر الجديد ، حدد **تحرير استعلام** فوق الشبكة.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="ef2d6-184">في مربع حوار الاستعلام، ضمن علامة التبويب **النطاق**، حدد **إضافة** لإضافة بند إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="ef2d6-185">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ef2d6-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ef2d6-186">**الجدول:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="ef2d6-187">**الجدول المشتق:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="ef2d6-188">**الحقل:** *معرف ملف الموقع*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="ef2d6-189">**المعايير:** *BULK*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="ef2d6-190">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-190">Select **OK**.</span></span>
1. <span data-ttu-id="ef2d6-191">في صفحة **توجيهات الموقع**، في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="ef2d6-192">في علامة التبويب السريعة **إجراءات توجيه المواقع** حقل **الاستراتيجية**، إذا كنت تستخدم استراتيجية الموقع *دمج*، فإن إعداد **مزج أبعاد المنتج المسموح به** في **ملفات تعريف الموقع**، سيتم تجاوزه وسيتم وضع الأصناف في نفس الموقع حتى وإن كان هذا السلوك غير مسموح به بواسطة الإعداد.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="ef2d6-193">إنشاء عنصر قائمة جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="ef2d6-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="ef2d6-194">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ef2d6-195">في جزء الإجراءات، حدد **جديد** لإنشاء عنصر قائمة لاستخدامه في الفرز.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="ef2d6-196">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ef2d6-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="ef2d6-197">**اسم عنصر القائمة:** *استلام سطر أمر الشراء*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="ef2d6-198">**العنوان:** *استلام سطر أمر الشراء*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="ef2d6-199">**الوضع:** *العمل*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="ef2d6-200">**استخدام العمل الموجود:** *لا*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="ef2d6-201">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ef2d6-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="ef2d6-202">**عملية إنشاء العمل:** *استلام سطر أمر الشراء وتخزينه*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="ef2d6-203">**إنشاء لوحة الترخيص:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="ef2d6-204">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="ef2d6-205">تكوين قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="ef2d6-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="ef2d6-206">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="ef2d6-207">في قائمة القوائم، حدد **وارد**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="ef2d6-208">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ef2d6-209">في قائمة **القوائم المتوفرة وعناصر القائمة**، ابحث عن عنصر القائمة **الاستلام سطر أمر الشراء** وحدده.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="ef2d6-210">حدد الزر سهم لليمين لنقل عنصر قائمة **استلام سطر أمر الشراء** إلى قائمة **بنية القائمة**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="ef2d6-211">بهذه الطريقة، تضيف عنصر القائمة الجديد إلى القائمة المحددة.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="ef2d6-212">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="ef2d6-213">سيناريو</span><span class="sxs-lookup"><span data-stu-id="ef2d6-213">Scenario</span></span>

<span data-ttu-id="ef2d6-214">يعرض سيناريو العرض التوضيحي هذا كيف يمكن وضع متغيرين مختلفين للمنتج في نفس الموقع عند عدم سماح ملف تعريف الموقع بالأصناف المختلطة، ولكن يتم تمكين *ميزة مزج أبعاد المنتج للموقع*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="ef2d6-215">في هذه الحالة، ستستخدم متغير **الحجم** كمعيار.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="ef2d6-216">قبل البدء، تأكد من وجود مواقع فارغة في المستودع *24* الذي يستخدم ملف تعريف الموقع *BULK*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="ef2d6-217">إنشاء أمر شراء</span><span class="sxs-lookup"><span data-stu-id="ef2d6-217">Create a purchase order</span></span>

<span data-ttu-id="ef2d6-218">ستقوم بإنشاء أمر شراء يحتوي على ثلاثة سطور: سطرين لنفس رقم المنتج ولكن بمتغيرات **حجم** مختلفة، وسطر ثالث لمنتج مختلف ليس له متغيرات.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="ef2d6-219">انتقل إلى **الحسابات الدائنة \> أوامر الشراء \> جميع أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="ef2d6-220">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ef2d6-221">في مربع الحوار **إنشاء أمر شراء**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ef2d6-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ef2d6-222">**حساب المورّد:** *1001*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="ef2d6-223">**المستودع:** *24*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="ef2d6-224">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-224">Select **OK**.</span></span>
1. <span data-ttu-id="ef2d6-225">يتم إنشاء أمر الشراء، وتتم إضافة سطر جديد في علامة التبويب السريعة **سطور أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="ef2d6-226">تدوين ملاحظة برقم أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="ef2d6-227">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ef2d6-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ef2d6-228">**رقم الصنف:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="ef2d6-229">**الحجم** *L*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-229">**Size** *L*</span></span>
    - <span data-ttu-id="ef2d6-230">**الكمية:** *2*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="ef2d6-231">حدد **إضافة سطر** أعلى الشبكة لإضافة سطر أمر شراء ثان، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ef2d6-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="ef2d6-232">**رقم الصنف:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="ef2d6-233">**الحجم** *XL*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-233">**Size** *XL*</span></span>
    - <span data-ttu-id="ef2d6-234">**الكمية:** *2*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="ef2d6-235">حدد **إضافة سطر** لإضافة سطر أمر شراء ثالث، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ef2d6-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="ef2d6-236">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="ef2d6-237">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="ef2d6-237">**Quantity:** *1*</span></span>

<span data-ttu-id="ef2d6-238">1.حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="ef2d6-239">استلام سطور أوامر الشراء في تطبيق إدارة المستودع للأجهزة المحمولة</span><span class="sxs-lookup"><span data-stu-id="ef2d6-239">Receive purchase order lines in the Warehouse Management mobile app</span></span>

1. <span data-ttu-id="ef2d6-240">سجل الدخول إلى تطبيق إدارة المستودع للأجهزة المحمولة كمستخدم ممكّن للمستودع *24*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-240">Sign in to the Warehouse Management mobile app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="ef2d6-241">حدد قائمة **الوارد**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="ef2d6-242">حدد **استلام سطر أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="ef2d6-243">حدد حقل **رقك أمر الشراء**، ثم أدخل رقم أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="ef2d6-244">قم بتأكيد الإدخال بتحديد زر التأكيد (✔) في أسفل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="ef2d6-245">أدخل رقم السطر من أمر الشراء الذي يجري استلامه.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="ef2d6-246">حدد حقل **رقم البند**، ثم استخدم لوحة الأرقام لإدخال القيمة *1*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="ef2d6-247">قم بتأكيد الإدخال.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-247">Confirm your entry.</span></span>
1. <span data-ttu-id="ef2d6-248">أدخل الكمية المطلوب استلامها.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-248">Enter the quantity to receive.</span></span> <span data-ttu-id="ef2d6-249">حدد زر علامة زائد (**+**) مرتين لزيادة القيمة في حقل **الكمية** إلى *2*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-249">Select the plus sign (**+**) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="ef2d6-250">سجل الإدخال الخاص بك وذلك بتحديد الزر (✔) الموجود أسفل الصفحة، ثم قم بتأكيد الإدخال بتحديد الزر (✔) مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="ef2d6-251">اعرض المعلومات الموجودة في صفحة **أوامر الشراء: وضع**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="ef2d6-252">تعرض هذه الصفحة العمل الذي تم إنشاؤه لحالة التخزين (العمل 1).</span><span class="sxs-lookup"><span data-stu-id="ef2d6-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="ef2d6-253">يتم عرض الموقع الذي سيتم فيه تخزين الصنف المستلم وكذلك لوحة الترخيص والصنف والحجم والكمية الخاصة مهمة **استلام سطر أمر الشراء** التي قمت بإكمالها للتو.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="ef2d6-254">قم بتأكيد عمل التخزين.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="ef2d6-255">قم بتكرار الخطوات من 4 إلى 11 لسطر أمر الشراء 2.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="ef2d6-256">مع ذلك، في الخطوة 8، حدد الكمية *1*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="ef2d6-257">يتم إنشاء عمل تخزين (العمل 2) جديد لنفس الموقع مثل العمل 1.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="ef2d6-258">قم بتكرار الخطوات من 4 إلى 11 مرة أخرى أمر الشراء 2.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="ef2d6-259">في الخطوة 8، حدد الكمية المتبقية *1*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="ef2d6-260">يتم إنشاء عمل تخزين (العمل 3) جديد لنفس الموقع مثل العمل 1 والعمل 2.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="ef2d6-261">يحدث هذا السلوك بسبب استخدام استراتيجية التوجيه لموقع *الدمج*، وعلامة التبويب السريعة **مزج أبعاد المنتج المسموح به** في إعداد *ملفات تعريف الموقع* بالقيمة **Bulk** تسمح بمزج متغير **الحجم** في الموقع.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="ef2d6-262">قم بتكرار الخطوات من 4 إلى 11 لسطر أمر الشراء 3.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="ef2d6-263">في الخطوة 8، حدد الكمية *1* لرقم الصنف *A0001*.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="ef2d6-264">يتم إنشاء عمل تخزين (العمل 4) جديد لموقع مختلف عن الموقع المستخدم لبنود أمر الشراء 1 و 2.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="ef2d6-265">يحدث هذا السلوك بسبب عدم سماح ملف تعريف الموقع بالمنتجات الممزوجة، ولكنه يسمح بأبعاد ممزوجة لنفس أصل المنتج.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="ef2d6-266">حدد زر القائمة أعلى الصفحة (أحيانًا يُشار إليه بهامبورجير أو الزر هامبورجير)، ثم حدد **إلغاء** لإنهاء **استلام سطر أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="ef2d6-267">يمكنك تكرار هذا السيناريو، ولكن في هذه المرة، قم بتعيين **الحجم** - *لا* ضمن علامة التبويب السريعة **السماح بمزج أبعاد المنتج** في *BULK* **ملفات تعريف الموقع**، بحيث لا يمكن مزج أي أبعاد للمنتج.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles**, so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="ef2d6-268">في هذه الحالة، عند استلام أمر الشراء، سيتم وضع كل متغير منتج في موقع جديد.</span><span class="sxs-lookup"><span data-stu-id="ef2d6-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]