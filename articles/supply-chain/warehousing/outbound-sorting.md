---
title: الفرز الصادر
description: يوفر هذا الموضوع معلومات حول الفرز الخارجي. تسهل هذه الوظيفة معالجة الحاويات الصغيرة، وتساعد موظفي المستودع على تخطيط قدرة البالتات وتنظيمها في الشاحنة بشكل أفضل.
author: Mirzaab
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3c576209a86f776ac424f7fb9f2b606bea774a67
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828384"
---
# <a name="outbound-sorting"></a><span data-ttu-id="c0c91-104">الفرز الصادر</span><span class="sxs-lookup"><span data-stu-id="c0c91-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0c91-105">تسهل هذه الوظيفة معالجة الحاويات الصغيرة وتساعد موظفي المستودع على تخطيط قدرة البالتات وتنظيمها في الشاحنة بشكل أفضل.</span><span class="sxs-lookup"><span data-stu-id="c0c91-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="c0c91-106">عند استخدام الفرز الخارجي، يمكنك فرز الحاويات المُعبأة‬ في البالتة الصحيحة بعد وصولها إلى محطة التعبئة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="c0c91-107">يمكنك أيضًا إنشاء تدرج هرمي للتعبئة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="c0c91-108">تتيح لك هذه الوظيفة إنشاء بالتات من الحاويات التي تتم تعبئتها من خلال وظيفة التعبئة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="c0c91-109">لا يتم إرسال الحاوية إلى موقع الشحن النهائي كما هو الحال في تدفق التعبئة الأصلي.</span><span class="sxs-lookup"><span data-stu-id="c0c91-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="c0c91-110">ويمكن للعاملين بدلاً من ذلك إغلاق الحاوية ونقلها إلى موقع نوع الفرز.</span><span class="sxs-lookup"><span data-stu-id="c0c91-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="c0c91-111">ويمكن عندها فرز الحاويات إلى مواضع، تحتوي كل منها على لوحة ترخيص (LP).</span><span class="sxs-lookup"><span data-stu-id="c0c91-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="c0c91-112">وبعد فرز الحاويات يمكن إنشاء العمل لإرسال لوحات الترخيص بأكملها إلى موقع إرساء الشحن النهائي أو موقع المرحلة، استنادًا إلى توجيهات المواقع أو متطلباتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="c0c91-113">ويمكن بالإضافة إلى ذلك لإجراء إغلاق موضع الفرز نقل المخزون إلى موقع الشحن النهائي فورًا وانتقائه إلى الأمر.</span><span class="sxs-lookup"><span data-stu-id="c0c91-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="c0c91-114">تشغيل ميزة الفرز الخارجي</span><span class="sxs-lookup"><span data-stu-id="c0c91-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="c0c91-115">قبل أن تتمكن من استخدام الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="c0c91-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="c0c91-116">بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="c0c91-117">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c0c91-118">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="c0c91-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c0c91-119">**اسم الميزة:** *الفرز الخارجي*</span><span class="sxs-lookup"><span data-stu-id="c0c91-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="c0c91-120">الإعداد</span><span class="sxs-lookup"><span data-stu-id="c0c91-120">Setup</span></span>

<span data-ttu-id="c0c91-121">بالنسبة لهذا السيناريو، يجب استخدام بيانات العرض التوضيحي القياسية **USMF** والمستودع *62*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="c0c91-122">ويجب أيضًا إكمال الإعداد الموضح في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="c0c91-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="c0c91-123">إعداد قالب موجة</span><span class="sxs-lookup"><span data-stu-id="c0c91-123">Set up a wave template</span></span>

<span data-ttu-id="c0c91-124">يعاج هذا الإعداد الموجة وينشئ العمل تلقائيًا عند تحرير سطر بالمستودع.</span><span class="sxs-lookup"><span data-stu-id="c0c91-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="c0c91-125">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجة**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="c0c91-126">في قائمة القوالب، حدد **المستودع 62**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="c0c91-127">في علامة التبويب السريعة **عام**، تأكد من تعيين الخيار **معالجة الموجة عند الإصدار إلى مستودع** على القيمة *نعم*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="c0c91-128">إعداد عامل</span><span class="sxs-lookup"><span data-stu-id="c0c91-128">Set up a worker</span></span>

<span data-ttu-id="c0c91-129">تعتبر محطة التعبئة موقعًا.</span><span class="sxs-lookup"><span data-stu-id="c0c91-129">The packing station is considered a location.</span></span> <span data-ttu-id="c0c91-130">يراجع موظفو المستودع الذين يسجلون الدخول بمحطة التعبئة ويعملون فقط على الشحنات والحاويات التي يتم تخطيطها في موقع التعبئة المحدد.</span><span class="sxs-lookup"><span data-stu-id="c0c91-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="c0c91-131">ويجب إعداد المستخدم الذي يسجل الدخول إلى Microsoft Dynamics 365 كعامل في إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="c0c91-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="c0c91-132">إذا لم يظهر اسم المستخدم في قائمة مستخدمي العمل، استخدم الإجراء التالي لإضافته.</span><span class="sxs-lookup"><span data-stu-id="c0c91-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="c0c91-133">تفترض هذه الخطوات وجود المستخدم بالفعل في النظام وإقرانه كموظف أو عامل في وحدة **الموارد البشرية** النمطية.</span><span class="sxs-lookup"><span data-stu-id="c0c91-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="c0c91-134">انتقل إلى **إدارة المستودعات \> الإعداد \> العامل**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="c0c91-135">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-135">Select **New**.</span></span>
1. <span data-ttu-id="c0c91-136">في الحقل **العامل**، حدد المستخدم الهدف في قائمة الموظفين.</span><span class="sxs-lookup"><span data-stu-id="c0c91-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="c0c91-137">حدد **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-137">Select **Select**.</span></span>
1. <span data-ttu-id="c0c91-138">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c0c91-139">في علامة التبويب السريعة **المستخدمين**، حدد **جديد** لإنشاء حساب للجهاز المحمول، وعيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="c0c91-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="c0c91-140">**معرف المستخدم:** أدخل معرفًا فريدًا.</span><span class="sxs-lookup"><span data-stu-id="c0c91-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="c0c91-141">**اسم المستخدم:** أدخل اسمًا للمعرف.</span><span class="sxs-lookup"><span data-stu-id="c0c91-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="c0c91-142">**المستودع الافتراضي:** *62*</span><span class="sxs-lookup"><span data-stu-id="c0c91-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="c0c91-143">**اسم القائمة:** *الأساسي*</span><span class="sxs-lookup"><span data-stu-id="c0c91-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="c0c91-144">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c0c91-145">يظهر مربع الحوار **تعيين كلمة المرور**، حيث يمكنك إنشاء كلمة مرور بسيطة يمكن للمستخدم استخدامها لتسجيل الدخول إلى تطبيق الأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="c0c91-146">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-146">Set the following values:</span></span>

    - <span data-ttu-id="c0c91-147">**كلمه المرور:** أدخل كلمة مرور بسيطة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="c0c91-148">**تأكيد كلمة المرور:** أدخل نفس كلمة المرور مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="c0c91-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="c0c91-149">حدد **تعيين كلمة المرور**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-149">Select **Set password**.</span></span>

    <span data-ttu-id="c0c91-150">يعلمك إخطار في مركز الصيانة بتعيين كلمة المرور للمستخدم الذي أنشأته.</span><span class="sxs-lookup"><span data-stu-id="c0c91-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="c0c91-151">إنشاء نوع موقع</span><span class="sxs-lookup"><span data-stu-id="c0c91-151">Create a location type</span></span>

1. <span data-ttu-id="c0c91-152">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> أنواع المواقع**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="c0c91-153">في جزء الإجراءات، حدد **جديد** لإنشاء نوع الموقع وعيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="c0c91-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="c0c91-154">**نوع الموقع:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="c0c91-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="c0c91-155">**الوصف:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="c0c91-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="c0c91-156">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="c0c91-157">إعداد معلمات إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="c0c91-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="c0c91-158">انتقل إلى **إدارة المستودعات‬\> إعداد‬ \> محددات إدارة المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="c0c91-159">في علامة التبويب **عام**، في علامة التبويب السريعة **أنواع المواقع**، عيِّن الحقل **نوع موقع الفرز** على *SORT*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="c0c91-160">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="c0c91-161">إعداد ملف تعريف موقع</span><span class="sxs-lookup"><span data-stu-id="c0c91-161">Set up a location profile</span></span>

1. <span data-ttu-id="c0c91-162">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> ملفات تعريف الموقع**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="c0c91-163">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c0c91-164">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="c0c91-165">**معرف ملف تعريف الموقع:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="c0c91-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="c0c91-166">**الاسم:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="c0c91-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="c0c91-167">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c0c91-168">**تنسيق الموقع:** *ASRB* (الممر-الحامل-الرف-السلة)</span><span class="sxs-lookup"><span data-stu-id="c0c91-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="c0c91-169">**نوع الموقع:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="c0c91-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="c0c91-170">**استخدام تعقب لوحة الترخيص:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="c0c91-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="c0c91-171">**السماح بالعناصر المختلطة:** *نعم* (عند تعيين هذا الخيار على القيمة *نعم*، يتم تعيين الخيار **‏‫السماح بدُفعات المخزون المختلطة** تلقائيًا على القيمة *نعم* ولا يمكن تغييره بشكل مستقل).</span><span class="sxs-lookup"><span data-stu-id="c0c91-171">**Allow mixed items:** *Yes* (When you set this option to *Yes*, the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="c0c91-172">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="c0c91-173">إعداد موقع</span><span class="sxs-lookup"><span data-stu-id="c0c91-173">Set up a location</span></span>

1. <span data-ttu-id="c0c91-174">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> المواقع**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="c0c91-175">في الرأس، امسح خانة الاختيار **إنشاء أرقام شيكات للموقع**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="c0c91-176">في جزء الإجراءات، حدد **جديد** لإنشاء موقع وعيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="c0c91-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="c0c91-177">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="c0c91-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="c0c91-178">**الموقع:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="c0c91-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="c0c91-179">**معرف ملف تعريف الموقع:** *SORTING*</span><span class="sxs-lookup"><span data-stu-id="c0c91-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="c0c91-180">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="c0c91-181">إعداد قالب الفرز الخارجي</span><span class="sxs-lookup"><span data-stu-id="c0c91-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="c0c91-182">يحدد قالب الفرز الخارجي ما إذا كان العمل قد تم إنشاؤه خارج موقع الفرز، وما إذا كان قد تم الفرز يدويًا أو تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="c0c91-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="c0c91-183">بالنسبة لهذا السيناريو، ستنشئ قالب الفرز الخارجي لبناء البالتات بعد محطة التعبئة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="c0c91-184">انتقل إلى **إدارة المستودعات \> الإعداد \> التعبئة \> قالب الفرز الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="c0c91-185">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c0c91-186">في رأس القالب الجديد، عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="c0c91-187">**معرف قالب الفرز الخارجي:** *العمل تلقائيًا*</span><span class="sxs-lookup"><span data-stu-id="c0c91-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="c0c91-188">**الوصف:** *إنشاء العمل تلقائيًا*</span><span class="sxs-lookup"><span data-stu-id="c0c91-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="c0c91-189">**نوع قالب الفرز الخارجي:** *حاوية*</span><span class="sxs-lookup"><span data-stu-id="c0c91-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="c0c91-190">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="c0c91-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="c0c91-191">**الموقع:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="c0c91-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="c0c91-192">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c0c91-193">**التحقق من الفرز:** *مسح الموضع*</span><span class="sxs-lookup"><span data-stu-id="c0c91-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="c0c91-194">**إنشاء عمل عند إغلاق الموضع:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="c0c91-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="c0c91-195">عند تحديد هذا الخيار على القيمة *نعم*، سيتم إنشاء عمل عند إغلاق الموضع لنقل المخزون إلى موقع الشحن النهائي.</span><span class="sxs-lookup"><span data-stu-id="c0c91-195">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="c0c91-196">وعند التعيين على القيمة *لا*، سيتم انتقاء المخزون إلى الأمر فورًا عند إغلاق الموضع.</span><span class="sxs-lookup"><span data-stu-id="c0c91-196">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="c0c91-197">**تعيين الموضع:** *تلقائيًا*</span><span class="sxs-lookup"><span data-stu-id="c0c91-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="c0c91-198">عند تعيين هذا الحقل على القيمة *يدويًا*، يجب على المستخدم أن يشير دائمًا إلى موضع فرز المخزون.</span><span class="sxs-lookup"><span data-stu-id="c0c91-198">If this field is set to *Manual*, the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="c0c91-199">عند التعيين على القيمة *تلقائيًا*، سيرشد النظام المخزون تلقائيًا إلى موضع إذا أمكن، استنادًا إلى فواصل قالب الفرز.</span><span class="sxs-lookup"><span data-stu-id="c0c91-199">If it's set to *Automatic*, the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="c0c91-200">حدد **حفظ** لإتاحة الزر **تحرير الاستعلام** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="c0c91-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="c0c91-201">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="c0c91-202">في محرر الاستعلام، في علامة التبويب **فرز**، أضف سطرًا بالقيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="c0c91-203">**الجدول:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="c0c91-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="c0c91-204">**الجدول المشتق:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="c0c91-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="c0c91-205">**الحقل:** *خدمة شركة النقل*</span><span class="sxs-lookup"><span data-stu-id="c0c91-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="c0c91-206">بتحديد هذه القيمة، قد تتلقى الرسالة التالية: "خدمة شركة الشحن الميدانية ليست حقل فهرس.</span><span class="sxs-lookup"><span data-stu-id="c0c91-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="c0c91-207">هل ترغب في إضافة فرز لها؟"</span><span class="sxs-lookup"><span data-stu-id="c0c91-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="c0c91-208">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-208">Select **Yes**.</span></span>

    - <span data-ttu-id="c0c91-209">**اتجاه البحث:** *تصاعدي*</span><span class="sxs-lookup"><span data-stu-id="c0c91-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="c0c91-210">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-210">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-211">قد تتلقى الرسالة التالية: "ستتم إعادة تعيين التجميع، هل تريد المتابعة؟"</span><span class="sxs-lookup"><span data-stu-id="c0c91-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="c0c91-212">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-212">Select **Yes**.</span></span>

    <span data-ttu-id="c0c91-213">يصبح الزر **فواصل قوالب الفرز الخارجي** في جزء الإجراءات متاحًا.</span><span class="sxs-lookup"><span data-stu-id="c0c91-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="c0c91-214">في جزء الإجراءات، حدد **فواصل قوالب الفرز الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="c0c91-215">في مربع الحوار **معايير الفرز الخارجي**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c0c91-216">**اسم الجدول المرجعي:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="c0c91-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="c0c91-217">**اسم الحقل المرجعي:** *خدمة شركة الشحن*</span><span class="sxs-lookup"><span data-stu-id="c0c91-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="c0c91-218">**تجميع حسب الحقل:** حدد خانة الاختيار هذه لتجميع الشحنات حسب خدمة شركة الشحن.</span><span class="sxs-lookup"><span data-stu-id="c0c91-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="c0c91-219">حدد **موافق** لحفظ إعداداتك وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="c0c91-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="c0c91-220">إعداد سياسات تعبئة الحاويات</span><span class="sxs-lookup"><span data-stu-id="c0c91-220">Set up container packing policies</span></span>

1. <span data-ttu-id="c0c91-221">انتقل إلى **إدارة المستودعات \> الإعداد \> الحاويات \> سياسات تعبئة الحاويات**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="c0c91-222">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c0c91-223">في رأس السياسة الجديدة، عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="c0c91-224">**سياسة تعبئة الحاويات:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="c0c91-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="c0c91-225">**الوصف:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="c0c91-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="c0c91-226">في علامة التبويب السريعة **نظرة عامة**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c0c91-227">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="c0c91-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="c0c91-228">**الموقع الافتراضي للفرز:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="c0c91-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="c0c91-229">**وحدة الوزن:** *كجم*</span><span class="sxs-lookup"><span data-stu-id="c0c91-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="c0c91-230">**سياسة إغلاق الحاوية:** *الإصدار التلقائي*</span><span class="sxs-lookup"><span data-stu-id="c0c91-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="c0c91-231">**سياسة إصدار الحاوية:** *تعيين حاوية إلى موضع الفرز الخارجي*</span><span class="sxs-lookup"><span data-stu-id="c0c91-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="c0c91-232">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="c0c91-233">إعداد ملفات تعريف التعبئة</span><span class="sxs-lookup"><span data-stu-id="c0c91-233">Set up packing profiles</span></span>

<span data-ttu-id="c0c91-234">قم بإنشاء ملف تعريف تعبئة جديد لاستخدامه مع وظيفة الفرز.</span><span class="sxs-lookup"><span data-stu-id="c0c91-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="c0c91-235">انتقل إلى **إدارة المستودعات \> الإعداد \> التعبئة \> ملفات تعريف التعبئة**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="c0c91-236">في جزء الإجراءات، حدد **جديد** لإنشاء سطر وعيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="c0c91-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="c0c91-237">**معرف ملف تعريف التعبئة:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="c0c91-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="c0c91-238">**الوصف:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="c0c91-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="c0c91-239">**سياسة تعبئة الحاويات:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="c0c91-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="c0c91-240">**وضع معرف الحاوية:** *تلقائي*</span><span class="sxs-lookup"><span data-stu-id="c0c91-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="c0c91-241">**نوع الحاوية:** *صندوق كبير*</span><span class="sxs-lookup"><span data-stu-id="c0c91-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="c0c91-242">**إنشاء حاوية تلقائيًا عند إغلاق الحاوية:** تم المسح (= *لا*)</span><span class="sxs-lookup"><span data-stu-id="c0c91-242">**Auto create container at container close:** Cleared (= *No*)</span></span>

1. <span data-ttu-id="c0c91-243">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="c0c91-244">إعداد فئات العمل</span><span class="sxs-lookup"><span data-stu-id="c0c91-244">Set up work classes</span></span>

<span data-ttu-id="c0c91-245">قم بإعداد فئة العمل التي سيتم استخدامها مع الفرز.</span><span class="sxs-lookup"><span data-stu-id="c0c91-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="c0c91-246">انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> فئات العمل**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="c0c91-247">في جزء الإجراءات، حدد **جديد** لإنشاء لإنشاء فئة عمل للفرز وعيِّن القيم التالية لها:</span><span class="sxs-lookup"><span data-stu-id="c0c91-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="c0c91-248">**معرف فئة العمل:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="c0c91-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="c0c91-249">**الوصف:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="c0c91-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="c0c91-250">**نوع أمر العمل:** *انتقاء المخزون الذي تم فرزه*</span><span class="sxs-lookup"><span data-stu-id="c0c91-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="c0c91-251">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="c0c91-252">إعداد عناصر القائمة للأجهزة المحمولة</span><span class="sxs-lookup"><span data-stu-id="c0c91-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="c0c91-253">إعداد عنصر قائمة بالتة جديدة</span><span class="sxs-lookup"><span data-stu-id="c0c91-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="c0c91-254">إنشاء عنصر قائمة للجهاز المحمول لإنشاء البالتات اثناء الفرز.</span><span class="sxs-lookup"><span data-stu-id="c0c91-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="c0c91-255">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="c0c91-256">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c0c91-257">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="c0c91-258">**اسم عنصر القائمة:** *بناء بالتة*</span><span class="sxs-lookup"><span data-stu-id="c0c91-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="c0c91-259">**العنوان:** *إنشاء البالتات*</span><span class="sxs-lookup"><span data-stu-id="c0c91-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="c0c91-260">**الوضع:** *غير مباشر*</span><span class="sxs-lookup"><span data-stu-id="c0c91-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="c0c91-261">**استخدام العمل الموجود:** *لا*</span><span class="sxs-lookup"><span data-stu-id="c0c91-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="c0c91-262">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c0c91-263">**رمز النشاط:** *فرز خارجي*</span><span class="sxs-lookup"><span data-stu-id="c0c91-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="c0c91-264">عند تعيين هذا الحقل على *فرز خارجي*، يظهر الحقل **معرف قالب الفرز الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-264">When this field is set to *Outbound sorting*, the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="c0c91-265">**استخدام دليل المعالجة:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="c0c91-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="c0c91-266">عند تعيين الحقل **رمز النشاط** على *فرز خارجي*، يتم تعيين هذا الخيار تلقائيًا على *نعم*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-266">When the **Activity code** field is set to *Outbound sorting*, this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="c0c91-267">**معرف قالب الفرز الخارجي:** *العمل تلقائيًا*</span><span class="sxs-lookup"><span data-stu-id="c0c91-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="c0c91-268">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="c0c91-269">إعداد عنصر قائمة تحميل جديد</span><span class="sxs-lookup"><span data-stu-id="c0c91-269">Set up a new loading menu item</span></span>

<span data-ttu-id="c0c91-270">انشئ بعد ذلك عنصر قائمة يتيح للمستخدمين نقل أصناف المخزون التي تم فرزها إلى موقع الشحن.</span><span class="sxs-lookup"><span data-stu-id="c0c91-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="c0c91-271">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="c0c91-272">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c0c91-273">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="c0c91-274">**اسم عنصر القائمة:** *تحميل من الفرز*</span><span class="sxs-lookup"><span data-stu-id="c0c91-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="c0c91-275">**العنوان:** *تحميل من الفرز*</span><span class="sxs-lookup"><span data-stu-id="c0c91-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="c0c91-276">**الوضع:** *العمل*</span><span class="sxs-lookup"><span data-stu-id="c0c91-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="c0c91-277">**استخدام العمل الموجود:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="c0c91-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="c0c91-278">في علامة التبويب السريعة **عام**، عيِّن الحقل **موجه بواسطة** على *موجه بواسطة المستخدم*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="c0c91-279">في علامة التبويب السريعة **فئات العمل**، حدد **جديد**، ثم عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-279">On the **Work classes** FastTab, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="c0c91-280">**معرف فئة العمل:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="c0c91-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="c0c91-281">**نوع أمر العمل:** *انتقاء المخزون الذي تم فرزه*</span><span class="sxs-lookup"><span data-stu-id="c0c91-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="c0c91-282">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="c0c91-283">إعداد قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="c0c91-283">Set up the mobile device menu</span></span>

<span data-ttu-id="c0c91-284">يجب الآن إضافة عناصر القائمة الجديدة إلى قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="c0c91-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="c0c91-285">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="c0c91-286">حدد قائمة **الصادر**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="c0c91-287">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c0c91-288">في عمود **القوائم المتوفرة وعناصر القائمة**، ابحث عن **بناء بالتة** وحددها.</span><span class="sxs-lookup"><span data-stu-id="c0c91-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="c0c91-289">حدد زر السهم الأيمن لنقل **بناء بالتة** إلى العمود **بنية القائمة**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="c0c91-290">استخدم أزرار السهم لأعلى والسهم لأسفل لوضع عنصر قائمة **بناء بالتة** في الموضع الموضح في قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="c0c91-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="c0c91-291">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-291">Select **Save**.</span></span>
1. <span data-ttu-id="c0c91-292">كرر هذا الإجراء لإضافة عنصر القائمة **تحميل من الفرز** إلى القائمة **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="c0c91-293">إعداد توجيهات الموقع</span><span class="sxs-lookup"><span data-stu-id="c0c91-293">Set up location directives</span></span>

<span data-ttu-id="c0c91-294">*توجيهات الموقع* هي قواعد تساعد في تحديد انتقاء ووضع مواقع لحركة المخزون.</span><span class="sxs-lookup"><span data-stu-id="c0c91-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="c0c91-295">يجب الآن إنشاء قاعدة لإدارة عمل الفرز.</span><span class="sxs-lookup"><span data-stu-id="c0c91-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="c0c91-296">إعداد توجيه بوحدة SKU مفردة</span><span class="sxs-lookup"><span data-stu-id="c0c91-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="c0c91-297">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="c0c91-298">في الجزء الأيمن، غير قيمة الحقل **نوع أمر العمل** إلى *انتقاء المخزون الذي تم فرزه*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="c0c91-299">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c0c91-300">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="c0c91-301">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="c0c91-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="c0c91-302">**الاسم:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="c0c91-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="c0c91-303">في علامة التبويب السريعة **توجيهات الموقع**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c0c91-304">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="c0c91-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="c0c91-305">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="c0c91-305">**Site:** *6*</span></span>
    - <span data-ttu-id="c0c91-306">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="c0c91-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="c0c91-307">**وحدة SKU متعددة:** *لا*</span><span class="sxs-lookup"><span data-stu-id="c0c91-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="c0c91-308">حدد **حفظ** لإتاحة شريط الأدوات في علامة التبويب السريعة **السطور**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="c0c91-309">في علامة التبويب السريعة **السطور**، حدد **جديد**، ثم عيِّن القيم التالية في السطر الجديد.</span><span class="sxs-lookup"><span data-stu-id="c0c91-309">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="c0c91-310">اقبل القيم الافتراضية لكافة الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="c0c91-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="c0c91-311">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="c0c91-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="c0c91-312">**من:** *0*</span><span class="sxs-lookup"><span data-stu-id="c0c91-312">**From:** *0*</span></span>
    - <span data-ttu-id="c0c91-313">**إلى:** *1,000,000*</span><span class="sxs-lookup"><span data-stu-id="c0c91-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="c0c91-314">حدد **حفظ** لإتاحة شريط الأدوات في علامة التبويب السريعة **إجراءات توجيه الموقع**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="c0c91-315">في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **جديد**، ثم عيِّن القيم التالية في السطر الجديد.</span><span class="sxs-lookup"><span data-stu-id="c0c91-315">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="c0c91-316">اقبل القيم الافتراضية لكافة الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="c0c91-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="c0c91-317">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="c0c91-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="c0c91-318">**الاسم:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="c0c91-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="c0c91-319">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-319">Select **Save**.</span></span>
1. <span data-ttu-id="c0c91-320">في علامة التبويب السريعة **إجراءات توجيه المواقع**، حدد **تحرير الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="c0c91-321">في محرر الاستعلام، في علامة التبويب **النطاق**، ابحث عن الصف الذي يحتوي على حقل **المجال** المعين إلى *الموقع*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="c0c91-322">عيِّن حقل **المعايير** لهذا الصف على *Baydoor*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="c0c91-323">حدد **موافق** لحفظ الإعدادات وإغلاق محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="c0c91-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="c0c91-324">إعداد توجيه بوحدة SKU متعددة</span><span class="sxs-lookup"><span data-stu-id="c0c91-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="c0c91-325">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="c0c91-326">في الجزء الأيمن، غير قيمة الحقل **نوع أمر العمل** إلى *انتقاء المخزون الذي تم فرزه*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="c0c91-327">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c0c91-328">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="c0c91-329">**التسلسل:** *2*</span><span class="sxs-lookup"><span data-stu-id="c0c91-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="c0c91-330">**الاسم:** *Baydoor متعدد*</span><span class="sxs-lookup"><span data-stu-id="c0c91-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="c0c91-331">في علامة التبويب السريعة **توجيهات الموقع**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c0c91-332">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="c0c91-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="c0c91-333">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="c0c91-333">**Site:** *6*</span></span>
    - <span data-ttu-id="c0c91-334">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="c0c91-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="c0c91-335">**وحدة SKU متعدد:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="c0c91-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="c0c91-336">حدد **حفظ** لإتاحة شريط الأدوات في علامة التبويب السريعة **السطور**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="c0c91-337">في علامة التبويب السريعة **السطور**، حدد **جديد**، ثم عيِّن القيم التالية في السطر الجديد.</span><span class="sxs-lookup"><span data-stu-id="c0c91-337">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="c0c91-338">اقبل القيم الافتراضية لكافة الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="c0c91-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="c0c91-339">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="c0c91-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="c0c91-340">**من:** *0*</span><span class="sxs-lookup"><span data-stu-id="c0c91-340">**From:** *0*</span></span>
    - <span data-ttu-id="c0c91-341">**إلى:** *1,000,000*</span><span class="sxs-lookup"><span data-stu-id="c0c91-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="c0c91-342">حدد **حفظ** لإتاحة شريط الأدوات في علامة التبويب السريعة **إجراءات توجيه الموقع**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="c0c91-343">في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **جديد**، ثم عيِّن القيم التالية في السطر الجديد.</span><span class="sxs-lookup"><span data-stu-id="c0c91-343">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="c0c91-344">اقبل القيم الافتراضية لكافة الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="c0c91-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="c0c91-345">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="c0c91-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="c0c91-346">**الاسم:** *Baydoor متعدد*</span><span class="sxs-lookup"><span data-stu-id="c0c91-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="c0c91-347">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-347">Select **Save**.</span></span>
1. <span data-ttu-id="c0c91-348">في علامة التبويب السريعة **إجراءات توجيه المواقع**، حدد **تحرير الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="c0c91-349">في محرر الاستعلام، في علامة التبويب **النطاق**، ابحث عن الصف الذي يحتوي على حقل **المجال** المعين إلى *الموقع*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="c0c91-350">عيِّن حقل **المعايير** لهذا الصف على *Baydoor*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="c0c91-351">حدد **موافق** لحفظ الإعدادات وإغلاق محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="c0c91-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="c0c91-352">إعداد قوالب العمل</span><span class="sxs-lookup"><span data-stu-id="c0c91-352">Set up work templates</span></span>

1. <span data-ttu-id="c0c91-353">انتقل إلى **إدارة المستودعات \> إعداد \> عمل \> قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="c0c91-354">غير قيمة الحقل **نوع أمر العمل** إلى *انتقاء المخزون الذي تم فرزه*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="c0c91-355">في جزء الإجراءات، حدد **جديد** لإنشاء قالب عمل.</span><span class="sxs-lookup"><span data-stu-id="c0c91-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="c0c91-356">في علامة التبويب **نظرة عامة**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="c0c91-357">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="c0c91-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="c0c91-358">**قالب العمل:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="c0c91-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="c0c91-359">**وصف قالب العمل:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="c0c91-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="c0c91-360">حدد **حفظ** لجعل علامة التبويب السريعة **تفاصيل قالب العمل** متاحة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="c0c91-361">في علامة التبويب السريعة **تفاصيل قالب العمل**، حدد **جديد** لإضافة سطر، ثم عيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="c0c91-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="c0c91-362">**نوع العمل:** *انتقاء*</span><span class="sxs-lookup"><span data-stu-id="c0c91-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="c0c91-363">**معرف فئة العمل:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="c0c91-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="c0c91-364">حدد **جديد** مرة أخرى لإضافة سطر ثان، ثم عيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="c0c91-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="c0c91-365">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="c0c91-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="c0c91-366">**معرف فئة العمل:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="c0c91-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="c0c91-367">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="c0c91-368">سيناريو</span><span class="sxs-lookup"><span data-stu-id="c0c91-368">Scenario</span></span>

<span data-ttu-id="c0c91-369">يحاكي هذا السيناريو موقفًا حيث ينبغي فرز الحاويات المعبأة تلقائيًا في مواقع (بالتات) مختلفة بعد محطة التعبئة، وذلك وفقًا لخدمة شركة الشحن.</span><span class="sxs-lookup"><span data-stu-id="c0c91-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="c0c91-370">بعد تعبئة كافة الأصناف من التحميل وفرزها حسب العنوان، يتم نقل البالتات إلى باب المرسى.</span><span class="sxs-lookup"><span data-stu-id="c0c91-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="c0c91-371">إنشاء أوامر مبيعات وعمل انتقاء</span><span class="sxs-lookup"><span data-stu-id="c0c91-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="c0c91-372">إنشاء أمر مبيعات 1</span><span class="sxs-lookup"><span data-stu-id="c0c91-372">Create sales order 1</span></span>

1. <span data-ttu-id="c0c91-373">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="c0c91-374">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c0c91-375">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c0c91-376">**حساب العميل:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="c0c91-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="c0c91-377">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="c0c91-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="c0c91-378">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="c0c91-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="c0c91-379">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="c0c91-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="c0c91-380">قم بالتبديل إلى طريقة عرض **الرأس**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="c0c91-381">في علامة التبويب السريعة **التسليم**، في قسم **النقل**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="c0c91-382">**شركة الشحن:** *Air cargo*</span><span class="sxs-lookup"><span data-stu-id="c0c91-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="c0c91-383">**خدمة شركة النقل:** *Air*</span><span class="sxs-lookup"><span data-stu-id="c0c91-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="c0c91-384">قم بالتبديل إلى طريقة عرض **السطور**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="c0c91-385">في حالة عدم إضافة سطر جديد خالٍ للشبكة تلقائيًا في علامة التبويب السريعة **سطور أمر المبيعات**، حدد **إضافة سطر** لإضافة واحد.</span><span class="sxs-lookup"><span data-stu-id="c0c91-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="c0c91-386">في سطر الأمر الجديد، عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="c0c91-387">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="c0c91-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="c0c91-388">**الكمية:** *2*</span><span class="sxs-lookup"><span data-stu-id="c0c91-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="c0c91-389">أثناء تحديد سطر الأمر الجديد في علامة التبويب السريعة **سطور أمر المبيعات**، في قائمة **المخزون** أعلى الشبكة، حدد **حجز**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="c0c91-390">في صفحة **الحجز**، حدد **حجز دفعة** لحجز الكمية الكاملة للسطر المحدد في المستودع.</span><span class="sxs-lookup"><span data-stu-id="c0c91-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="c0c91-391">قم بإغلاق صفحة **الحجز** للعودة إلى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c0c91-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="c0c91-392">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، في مجموعة **الإجراءات**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="c0c91-393">ستستلم رسالة معلوماتية توضح الشحنة والموجة لهذا الأمر.</span><span class="sxs-lookup"><span data-stu-id="c0c91-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="c0c91-394">قم بتدوين رقم معرف الموجة ورقم معرف الشحنة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="c0c91-395">أمر المبيعات 2</span><span class="sxs-lookup"><span data-stu-id="c0c91-395">Sales order 2</span></span>

1. <span data-ttu-id="c0c91-396">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="c0c91-397">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c0c91-398">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c0c91-399">**حساب العميل:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="c0c91-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="c0c91-400">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="c0c91-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="c0c91-401">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="c0c91-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="c0c91-402">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="c0c91-402">The new sales order is opened.</span></span> <span data-ttu-id="c0c91-403">ويجب أن يتضمن بندًا فارغًا جديدًا في الشبكة في علامة التبويب السريعة **بنود أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="c0c91-404">عيِّن القيم التالية في سطر الأمر:</span><span class="sxs-lookup"><span data-stu-id="c0c91-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="c0c91-405">**الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="c0c91-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="c0c91-406">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="c0c91-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="c0c91-407">في علامة التبويب السريعة **تفاصيل السطر**، في علامة التبويب **التسليم** عيٍّن الحقل **وضع التسليم** على *Flowe-STD*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="c0c91-408">في علامة التبويب السريعة **سطور أمر المبيعات**، حدد **إضافة سطر**، ثم عيِّن القيم التالية في سطر الأمر الثاني:</span><span class="sxs-lookup"><span data-stu-id="c0c91-408">On the **Sales order lines** FastTab, select **Add line**, and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="c0c91-409">**الصنف:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="c0c91-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="c0c91-410">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="c0c91-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="c0c91-411">في علامة التبويب السريعة **تفاصيل السطر**، في علامة التبويب **التسليم** غير قيمة الحقل **وضع التسليم** على *Air C-Air*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="c0c91-412">في علامة التبويب السريعة **سطور أمر المبيعات**، حدد سطر الأمر الأول.</span><span class="sxs-lookup"><span data-stu-id="c0c91-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="c0c91-413">وفي قائمة **المخزون** أعلى الشبكة، حدد **حجز**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="c0c91-414">في صفحة **الحجز**، حدد **حجز دفعة** لحجز الكمية الكاملة للسطر المحدد في المستودع.</span><span class="sxs-lookup"><span data-stu-id="c0c91-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="c0c91-415">قم بإغلاق صفحة **الحجز** للعودة إلى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c0c91-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="c0c91-416">في علامة التبويب السريعة **سطور أمر المبيعات**، حدد سطر الأمر الثاني.</span><span class="sxs-lookup"><span data-stu-id="c0c91-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="c0c91-417">وفي قائمة **المخزون** أعلى الشبكة، حدد **حجز**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="c0c91-418">في صفحة **الحجز**، حدد **حجز دفعة** لحجز الكمية الكاملة للسطر المحدد في المستودع.</span><span class="sxs-lookup"><span data-stu-id="c0c91-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="c0c91-419">قم بإغلاق صفحة **الحجز** للعودة إلى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c0c91-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="c0c91-420">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، في مجموعة **الإجراءات**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="c0c91-421">ستستلم رسالة معلوماتية توضح الشحنة والموجة لهذا الأمر.</span><span class="sxs-lookup"><span data-stu-id="c0c91-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="c0c91-422">لاحظ أنه تم إنشاء رقمين لمعرف الموجة ورقمين لمعرف الشحنة، واحد لكل وضع من أوضاع التسليم لسطور أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c0c91-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="c0c91-423">الحصول على معرفات العمل من تفاصيل العمل</span><span class="sxs-lookup"><span data-stu-id="c0c91-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="c0c91-424">انتقل إلى **إدارة المستودعات \> العمل \> تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="c0c91-425">تعرض الصفحة معرفات العمل التي تم إنشاؤها من أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c0c91-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="c0c91-426">استخدم معرفات الموجات ومعرفات الشحنات من أوامر المبيعات التي أنشأتها للعثور على معرف العمل لكل موجة وشحنة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="c0c91-427">دون معرفات العمل هذة، لأنك ستحتاجها في الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c0c91-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="c0c91-428">لاحظ أنه تم إنشاء معرفي عمل لأمر المبيعات الثاني.</span><span class="sxs-lookup"><span data-stu-id="c0c91-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="c0c91-429">في حالة انتقاء أصناف مختلفة من مواقع مختلفة، يتم إنشاء معرفات بكلمات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="c0c91-430">انتقاء الأصناف لأوامر المبيعات</span><span class="sxs-lookup"><span data-stu-id="c0c91-430">Pick items for the sales orders</span></span>

<span data-ttu-id="c0c91-431">أكمل العمل الذي تم إنشاؤه باستخدام الجهاز المحمول لنقل الأصناف إلى محطة التعبئة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="c0c91-432">على الجهاز المحمول، سجِّل الدخول إلى المستودع *62* باستخدام معرف المستخدم الذي أنشأته لهذا السيناريو (أو معرف المستخدم لمستخدم بيانات العرض التوضيحي موجود).</span><span class="sxs-lookup"><span data-stu-id="c0c91-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="c0c91-433">من القائمة الرئيسية، حدد **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="c0c91-434">من القائمة **خارجي**، حدد **انتقاء المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="c0c91-435">في حقل **المعرف**، أدخل معرف العمل الذي تم إنشاؤه لأمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="c0c91-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="c0c91-436">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-436">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-437">في صفحة **أوامر المبيعات - الانتقاء**، أدخل لوحة الترخيص الهدف التي تم إنشاؤها لأمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="c0c91-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="c0c91-438">لاحظ أنه يتم عرض موقع الانتقاء ( *المجموعة-001*) والصنف ( *A0001*) والكمية ( *قطعتين*).</span><span class="sxs-lookup"><span data-stu-id="c0c91-438">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*2 pcs*) are shown.</span></span>
1. <span data-ttu-id="c0c91-439">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-439">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-440">راجع المعلومات الموجودة في صفحة **أوامر المبيعات - وضع**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="c0c91-441">ينبغي أن يشير الحقل **الموقع** إلى انتقال الأصناف المنتقاة إلى موقع *التعبئة*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="c0c91-442">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-442">Select **OK**.</span></span>

    <span data-ttu-id="c0c91-443">تتلقى في صفحة **مسح معرف العمل/معرف لوحة الترخيص** رسالة "اكتمل العمل"، والتي تشير إلى أنه تم إكمال معرف العمل من أمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="c0c91-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="c0c91-444">ستقوم الآن بانتقاء أمر المبيعات رقم 2.</span><span class="sxs-lookup"><span data-stu-id="c0c91-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="c0c91-445">في حقل **المعرف**، أدخل معرف العمل الذي تم إنشاؤه لأمر المبيعات رقم 2 حيث يحتوي السطر رقم 1 على الصنف *A0001*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="c0c91-446">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-446">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-447">في الصفحة **أوامر المبيعات - الانتقاء**، أدخل لوحة ترخيص هدف.</span><span class="sxs-lookup"><span data-stu-id="c0c91-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="c0c91-448">لاحظ أنه يتم عرض موقع الانتقاء ( *المجموعة-001*) والصنف ( *A0001*) والكمية ( *قطعتين*).</span><span class="sxs-lookup"><span data-stu-id="c0c91-448">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="c0c91-449">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-449">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-450">راجع المعلومات الموجودة في صفحة **أوامر المبيعات - وضع**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="c0c91-451">ينبغي أن يشير الحقل **الموقع** إلى انتقال الأصناف المنتقاة إلى موقع *التعبئة*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="c0c91-452">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-452">Select **OK**.</span></span>

    <span data-ttu-id="c0c91-453">في الصفحة **مسح معرف العمل/معرف لوحة الترخيص**، تتلقى رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="c0c91-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="c0c91-454">وتشير هذه الرسالة إلى أنه تم إكمال معرف العمل من السطر 1 لأمر المبيعات 2.</span><span class="sxs-lookup"><span data-stu-id="c0c91-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="c0c91-455">في حقل **المعرف**، أدخل معرف العمل الذي تم إنشاؤه لأمر المبيعات رقم 2 حيث يحتوي السطر رقم 2 على الصنف *A0002*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="c0c91-456">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-456">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-457">في الصفحة **أوامر المبيعات - الانتقاء**، أدخل لوحة ترخيص هدف.</span><span class="sxs-lookup"><span data-stu-id="c0c91-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="c0c91-458">لاحظ أنه يتم عرض موقع الانتقاء ( *المجموعة-002*) والصنف ( *A0001*) والكمية ( *قطعتين*).</span><span class="sxs-lookup"><span data-stu-id="c0c91-458">Notice that the picking location (*bulk-002*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="c0c91-459">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-459">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-460">راجع المعلومات الموجودة في صفحة **أوامر المبيعات - وضع**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="c0c91-461">ينبغي أن يشير الحقل **الموقع** إلى انتقال الأصناف المنتقاة إلى موقع *التعبئة*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="c0c91-462">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-462">Select **OK**.</span></span>

    <span data-ttu-id="c0c91-463">في الصفحة **مسح معرف العمل/معرف لوحة الترخيص**، تتلقى رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="c0c91-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="c0c91-464">وتشير هذه الرسالة إلى أنه تم إكمال معرف العمل من السطر 2 لأمر المبيعات 2.</span><span class="sxs-lookup"><span data-stu-id="c0c91-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="c0c91-465">تعبئة أوامر المبيعات في حاويات</span><span class="sxs-lookup"><span data-stu-id="c0c91-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="c0c91-466">تعبئة أمر المبيعات 1 في حاويات</span><span class="sxs-lookup"><span data-stu-id="c0c91-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="c0c91-467">انتقل إلى **إدارة المستودعات \> التعبئة والتعبئة في حاويات \> التعبئة**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="c0c91-468">يظهر مربع الحوار **تحديد محطة التعبئة**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="c0c91-469">وبشكل افتراضي، ينبغي تعيين الحقل **العامل** على اسم العامل الذي قمت بإعداده مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="c0c91-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="c0c91-470">عيِّن القيم التالية لعرض الشحنات والحاويات التي تم تخطيطها في موقع التعبئة المحدد والتعامل معها:</span><span class="sxs-lookup"><span data-stu-id="c0c91-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="c0c91-471">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="c0c91-471">**Site:** *6*</span></span>
    - <span data-ttu-id="c0c91-472">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="c0c91-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="c0c91-473">**الموقع:** *التعبئة*</span><span class="sxs-lookup"><span data-stu-id="c0c91-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="c0c91-474">**معرف ملف تعريف التعبئة:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="c0c91-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="c0c91-475">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="c0c91-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="c0c91-476">في صفحة **التعبئة**، في الحقل **لوحة الترخيص أو الشحنة**، أدخل لوحة الترخيص الهدف لأمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="c0c91-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="c0c91-477">ثم حدد **علامة التبويب** أو مفتاح **Enter** في لوحة المفاتيح للانتقال خارج الحقل.</span><span class="sxs-lookup"><span data-stu-id="c0c91-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="c0c91-478">في جزء الإجراءات، حدد **حاوية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="c0c91-479">اقبل كافة الإعدادات الافتراضية، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="c0c91-480">دوِّن ملاحظة بمُعرف الحاوية.</span><span class="sxs-lookup"><span data-stu-id="c0c91-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="c0c91-481">في علامة التبويب السريعة **تعبئة الصنف**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c0c91-482">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="c0c91-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="c0c91-483">**المعرف:** الصنف *A0001*</span><span class="sxs-lookup"><span data-stu-id="c0c91-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="c0c91-484">في جزء الإجراءات، حدد **إغلاق الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="c0c91-485">في مربع الحوار **إغلاق الحاوية**، حدد **الحصول على وزن النظام** لتحديث النظام لحقل **الوزن الإجمالي**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="c0c91-486">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-486">Select **OK**.</span></span> <span data-ttu-id="c0c91-487">يتم نقل الحاوية إلى الموقع *SORT* وتكون جاهزة للفرز.</span><span class="sxs-lookup"><span data-stu-id="c0c91-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="c0c91-488">انشئ حاوية ثانية لإضافة الصنف الثاني من لوحة الترخيص لأمر المبيعات 1 إلى حاوية جديدة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="c0c91-489">في جزء الإجراءات، حدد **حاوية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="c0c91-490">اقبل كافة الإعدادات الافتراضية، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="c0c91-491">دوِّن ملاحظة بمُعرف الحاوية.</span><span class="sxs-lookup"><span data-stu-id="c0c91-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="c0c91-492">في علامة التبويب السريعة **تعبئة الصنف**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c0c91-493">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="c0c91-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="c0c91-494">**المعرف:** الصنف *A0001*</span><span class="sxs-lookup"><span data-stu-id="c0c91-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="c0c91-495">في جزء الإجراءات، حدد **إغلاق الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="c0c91-496">في مربع الحوار **إغلاق الحاوية**، حدد **الحصول على وزن النظام** لتحديث النظام لحقل **الوزن الإجمالي**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="c0c91-497">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-497">Select **OK**.</span></span> <span data-ttu-id="c0c91-498">يتم نقل الحاوية إلى الموقع *SORT* وتكون جاهزة للفرز.</span><span class="sxs-lookup"><span data-stu-id="c0c91-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="c0c91-499">تعبئة أمر المبيعات 2 في حاويات</span><span class="sxs-lookup"><span data-stu-id="c0c91-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="c0c91-500">في صفحة **التعبئة**، في الحقل **لوحة الترخيص أو الشحنة**، أدخل لوحة الترخيص الهدف للسطر 1 بأمر المبيعات 2.</span><span class="sxs-lookup"><span data-stu-id="c0c91-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="c0c91-501">ثم حدد **علامة التبويب** أو مفتاح **Enter** في لوحة المفاتيح للانتقال خارج الحقل.</span><span class="sxs-lookup"><span data-stu-id="c0c91-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="c0c91-502">في جزء الإجراءات، حدد **حاوية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="c0c91-503">اقبل كافة الإعدادات الافتراضية، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="c0c91-504">دوِّن ملاحظة بمُعرف الحاوية.</span><span class="sxs-lookup"><span data-stu-id="c0c91-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="c0c91-505">في علامة التبويب السريعة **تعبئة الصنف**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c0c91-506">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="c0c91-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="c0c91-507">**المعرف:** الصنف *A0001*</span><span class="sxs-lookup"><span data-stu-id="c0c91-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="c0c91-508">في جزء الإجراءات، حدد **إغلاق الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="c0c91-509">في مربع الحوار **إغلاق الحاوية**، حدد **الحصول على وزن النظام** لتحديث النظام لحقل **الوزن الإجمالي**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="c0c91-510">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-510">Select **OK**.</span></span> <span data-ttu-id="c0c91-511">يتم نقل الحاوية إلى الموقع *SORT* وتكون جاهزة للفرز.</span><span class="sxs-lookup"><span data-stu-id="c0c91-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="c0c91-512">في الحقل **لوحة الترخيص أو الشحنة**، أدخل لوحة الترخيص الهدف للسطر 2 بأمر المبيعات 2.</span><span class="sxs-lookup"><span data-stu-id="c0c91-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="c0c91-513">ثم حدد **علامة التبويب** أو مفتاح **Enter** في لوحة المفاتيح للانتقال خارج الحقل.</span><span class="sxs-lookup"><span data-stu-id="c0c91-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="c0c91-514">في جزء الإجراءات، حدد **حاوية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="c0c91-515">اقبل كافة الإعدادات الافتراضية، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="c0c91-516">دوِّن ملاحظة بمُعرف الحاوية.</span><span class="sxs-lookup"><span data-stu-id="c0c91-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="c0c91-517">في علامة التبويب السريعة **تعبئة الصنف**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c0c91-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c0c91-518">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="c0c91-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="c0c91-519">**حقل المعرف:** العنصر *A0002*</span><span class="sxs-lookup"><span data-stu-id="c0c91-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="c0c91-520">في جزء الإجراءات، حدد **إغلاق الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="c0c91-521">في مربع الحوار **إغلاق الحاوية**، حدد **الحصول على وزن النظام** لتحديث النظام لحقل **الوزن الإجمالي**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="c0c91-522">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-522">Select **OK**.</span></span> <span data-ttu-id="c0c91-523">يتم نقل الحاوية إلى الموقع *SORT* وتكون جاهزة للفرز.</span><span class="sxs-lookup"><span data-stu-id="c0c91-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="c0c91-524">لعرض تفاصيل الحاوية، انتقل إلى **إدارة المستودعات \> التعبئة والتعبئة في حاويات \> الحاويات** وابحث عن معرفات الحاويات التي تم إنشاؤها أثناء التعبئة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers**, and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="c0c91-525">فرز الحاويات</span><span class="sxs-lookup"><span data-stu-id="c0c91-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0c91-526">عند الوصول إلى عنصر القائمة **بناء بالتة** في تطبيق الأجهزة المحمولة لإجراء الفرز الخارجي، ستشاهد زرًا بالاسم **بالكامل**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="c0c91-527">*لا تستخدم الزر **‎بالكامل** لفرز الموضع أو إغلاقه.*</span><span class="sxs-lookup"><span data-stu-id="c0c91-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="c0c91-528">يتوفر الزر **‎بالكامل** افتراضيًا ولا يمكن تعطيله أو إزالته من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="c0c91-529">ولا يتم استخدامه لميزة *الفرز الخارجي*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="c0c91-530">فرز الحاوية الأولى</span><span class="sxs-lookup"><span data-stu-id="c0c91-530">Sort the first container</span></span>

1. <span data-ttu-id="c0c91-531">على الجهاز المحمول، سجِّل الدخول إلى المستودع *62* باستخدام معرف المستخدم الذي أنشأته لهذا السيناريو (أو معرف المستخدم لمستخدم بيانات العرض التوضيحي موجود).</span><span class="sxs-lookup"><span data-stu-id="c0c91-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="c0c91-532">من القائمة الرئيسية، حدد **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="c0c91-533">من القائمة **خارجي**، حدد **بناء بالتة**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="c0c91-534">في الحقل **لوحة الترخيص/الحاوية**، أدخل معرف الحاوية الأولى المقترن بأمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="c0c91-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="c0c91-535">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-535">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-536">نظرًا لعدم وجود مواضع فرز حاليًا، يجب تحديد واحدًا.</span><span class="sxs-lookup"><span data-stu-id="c0c91-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="c0c91-537">في الحقل **معرف موضع الفرز**، أدخل *SP01*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="c0c91-538">نظرًا لعدم اقتران لوحة ترخيص حاليًا بموضع الفرز *SP01*، يجب تحديد واحدة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-538">Because no LP is currently associated with sort position *SP01*, you must specify one.</span></span> <span data-ttu-id="c0c91-539">في الحقل **لوحة الترخيص**، أدخل *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="c0c91-540">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-540">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-541">نظرًا لاًن عملية التحقق من صحة موضع الفرز قيد التشغيل، يجب إدخال معرف موضع الفرز مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="c0c91-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="c0c91-542">في الحقل **معرف موضع الفرز**، أدخل *SP01*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="c0c91-543">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-543">Select **OK**.</span></span>

    <span data-ttu-id="c0c91-544">ستتلقى رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="c0c91-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="c0c91-545">لعرض موضع الفرز ولوحة الترخيص فيه، انتقل إلى **إدارة المستودعات \> التعبئة والتعبئة في حاويات \> تعيينات موضع الفرز الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="c0c91-546">تظهر صفحة **تعيينات موضع الفرز الخارجي** كافة مواضع الفرز النشطة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="c0c91-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="c0c91-547">يظهر الحقل **حركات موضع الفرز** لوحة الترخيص المقترنة بكل موضع فرز والحاويات الموجودة في موضع الفرز.</span><span class="sxs-lookup"><span data-stu-id="c0c91-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="c0c91-548">لاحظ وجود موضع فرز واحد حاليًا، وأن علامة التبويب السريعة **معايير موضع الفرز** تظهر معيار **الشحنة - خدمة شركة الشحن - جوًا**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="c0c91-549">فرز الحاويات المتبقية</span><span class="sxs-lookup"><span data-stu-id="c0c91-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="c0c91-550">على الجهاز المحمول، سجِّل الدخول إلى المستودع *62* باستخدام معرف المستخدم الذي أنشأته لهذا السيناريو (أو معرف المستخدم لمستخدم بيانات العرض التوضيحي موجود).</span><span class="sxs-lookup"><span data-stu-id="c0c91-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="c0c91-551">من القائمة الرئيسية، حدد **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="c0c91-552">من القائمة **خارجي**، حدد **بناء بالتة**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="c0c91-553">في الحقل **لوحة الترخيص/الحاوية**، أدخل معرف الحاوية الثانية المقترن بأمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="c0c91-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="c0c91-554">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-554">Select **OK**.</span></span> <span data-ttu-id="c0c91-555">نظرًا لإعداد قالب الفرز على الفرز تلقائيًا، ووجود موضع فرز له معايير مطابقه بالفعل، سيتم توجيهك تلقائيًا إلى موضع الفرز الصحيح.</span><span class="sxs-lookup"><span data-stu-id="c0c91-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="c0c91-556">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-556">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-557">قم بتأكيد معرف موضع الفرز للإشارة إلى وجود المخزون في المكان الصحيح.</span><span class="sxs-lookup"><span data-stu-id="c0c91-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="c0c91-558">في الحقل **معرف موضع الفرز**، أدخل *SP01*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="c0c91-559">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-559">Select **OK**.</span></span>

    <span data-ttu-id="c0c91-560">اكتمل العمل في الحاوية الثانية من أمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="c0c91-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="c0c91-561">ستقوم الآن بفرز الحاويات المتبقية من أمر المبيعات 2.</span><span class="sxs-lookup"><span data-stu-id="c0c91-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="c0c91-562">في الحقل **لوحة الترخيص/الحاوية**، أدخل معرف الحاوية للحاوية من أمر المبيعات 2 الذي يحتوي على الصنف *A0001*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="c0c91-563">نظرًا لاختلاف خدمة شركة الشحن، فإنك مطالب بإدخال موضع فرز جديد وتعيين لوحة ترخيص لذلك الموضع.</span><span class="sxs-lookup"><span data-stu-id="c0c91-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="c0c91-564">استخدم موضع الفرز *SP02* ولوحة الترخيص *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="c0c91-565">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-565">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-566">قم بتأكيد موضع الفرز بإدخال *SP02* في الحقل **معرف موضع الفرز**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="c0c91-567">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-567">Select **OK**.</span></span>

    <span data-ttu-id="c0c91-568">اكتمل العمل في الحاوية.</span><span class="sxs-lookup"><span data-stu-id="c0c91-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="c0c91-569">في الحقل **لوحة الترخيص/الحاوية**، أدخل معرف الحاوية للحاوية المتبقية من أمر المبيعات 2 الذي يحتوي على الصنف *A0002*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="c0c91-570">ونظرًا لأن خدمة شركة الشحن هي نفسها لأمر المبيعات رقم 1، فإن النظام يعرض موضع الفرز الموجود الذي له معايير مطابقة.</span><span class="sxs-lookup"><span data-stu-id="c0c91-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="c0c91-571">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-571">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-572">قم بتأكيد موضع الفرز بإدخال *SP01* في الحقل **معرف موضع الفرز**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="c0c91-573">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-573">Select **OK**.</span></span>

    <span data-ttu-id="c0c91-574">اكتمل العمل في الحاوية.</span><span class="sxs-lookup"><span data-stu-id="c0c91-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="c0c91-575">إغلاق مواضع الفرز الخارجي</span><span class="sxs-lookup"><span data-stu-id="c0c91-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="c0c91-576">بمجرد فرز كل المخزون، يجب إغلاق الموضع قبل التمكن من إنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="c0c91-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="c0c91-577">سيتم إنشاء عمل انتقاء المخزون الذي تم فرزه لحمل المخزون إلى باب المرسى.</span><span class="sxs-lookup"><span data-stu-id="c0c91-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="c0c91-578">إغلاق موضع من الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="c0c91-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="c0c91-579">على الجهاز المحمول، سجِّل الدخول إلى المستودع *62* باستخدام معرف المستخدم الذي أنشأته لهذا السيناريو (أو معرف المستخدم لمستخدم بيانات العرض التوضيحي موجود).</span><span class="sxs-lookup"><span data-stu-id="c0c91-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="c0c91-580">من القائمة الرئيسية، حدد **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="c0c91-581">من القائمة **خارجي**، حدد **بناء بالتة**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="c0c91-582">في الحقل **لوحة الترخيص/الحاوية**، أدخل معرف حاوية تم فرزها في موضع الفرز *SP01*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="c0c91-583">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-583">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-584">ستتلقى الرسالة التالية: "تم بالفعل فرز الحاوية بالموضع SP01.</span><span class="sxs-lookup"><span data-stu-id="c0c91-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="c0c91-585">هل تريد إغلاق الموضع؟؟</span><span class="sxs-lookup"><span data-stu-id="c0c91-585">Close the position?"</span></span> <span data-ttu-id="c0c91-586">حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-586">Select **Close**.</span></span>

    <span data-ttu-id="c0c91-587">اكتمل العمل.</span><span class="sxs-lookup"><span data-stu-id="c0c91-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="c0c91-588">إغلاق موضع من تعيينات موضع الفرز الخارجي</span><span class="sxs-lookup"><span data-stu-id="c0c91-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="c0c91-589">انتقل إلى **إدارة المستودعات \> التعبئة والتعبئة في حاويات \> تعيينات موضع الفرز الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="c0c91-590">في العمود الأيمن، حدد **SP02**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="c0c91-591">صف موضع الفرز الخارجي هذا هو الصف الوحيد الذي ستغلقه.</span><span class="sxs-lookup"><span data-stu-id="c0c91-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="c0c91-592">في جزء الإجراءات، حدد **فتح موضع**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="c0c91-593">سجل موضع الفرز مغلق ولم يعد ظاهرًا.</span><span class="sxs-lookup"><span data-stu-id="c0c91-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="c0c91-594">لإظهار كافة سجلات الموضع المغلقة، حدد خانة الاختيار **إظهار المغلق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="c0c91-595">انتقاء المخزون الذي تم فرزه</span><span class="sxs-lookup"><span data-stu-id="c0c91-595">Sorted inventory picking</span></span>

<span data-ttu-id="c0c91-596">يجب إكمال عمل انتقاء المخزون الذي تم فرزه.</span><span class="sxs-lookup"><span data-stu-id="c0c91-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="c0c91-597">وعند الانتهاء من ذلك، سيتم انتقاء المخزون لأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c0c91-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="c0c91-598">وعندها، يتم تطبيق كافة عمليات المستودع الأخرى.</span><span class="sxs-lookup"><span data-stu-id="c0c91-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="c0c91-599">على الجهاز المحمول، سجِّل الدخول إلى المستودع *62* باستخدام معرف المستخدم الذي أنشأته لهذا السيناريو (أو معرف المستخدم لمستخدم بيانات العرض التوضيحي موجود).</span><span class="sxs-lookup"><span data-stu-id="c0c91-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="c0c91-600">من القائمة الرئيسية، حدد **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="c0c91-601">في القائمة **خارجي**، حدد **تحميل من الفرز**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="c0c91-602">أدخل معرف لوحة الترخيص الهدف من موضع الفرز الأول، *SP01*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="c0c91-603">عيِّن الحقل **المعرف** على *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="c0c91-604">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-604">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-605">تظهر صفحة **انتقاء المخزون الذي تم فرزه: الانتقاء** عمل الانتقاء الذي يجب إنجازه.</span><span class="sxs-lookup"><span data-stu-id="c0c91-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="c0c91-606">انتقِ من الموقع *SORT* ولوحة الترخيص الهدف *PLP01*، والذي يحتوي على أصناف متعددة وكمية بالقيمة *3*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-606">Pick from the *SORT* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="c0c91-607">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-607">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-608">تظهر صفحة **انتقاء المخزون الذي تم فرزه: وضع** عمل الوضع الذي يجب إنجازه.</span><span class="sxs-lookup"><span data-stu-id="c0c91-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="c0c91-609">ضع الموقع *Baydoor* ولوحة الترخيص الهدف *PLP01*، والذي يحتوي على أصناف متعددة وكمية بالقيمة *3*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-609">Put to the *Baydoor* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="c0c91-610">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-610">Select **OK**.</span></span>

    <span data-ttu-id="c0c91-611">اكتمل العمل.</span><span class="sxs-lookup"><span data-stu-id="c0c91-611">Work is completed.</span></span>

1. <span data-ttu-id="c0c91-612">أدخل معرف لوحة الترخيص الهدف من موضع الفرز الثاني، *SP02*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="c0c91-613">عيِّن الحقل **المعرف** على *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="c0c91-614">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-614">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-615">تظهر صفحة **انتقاء المخزون الذي تم فرزه: الانتقاء** عمل الانتقاء الذي يجب إنجازه.</span><span class="sxs-lookup"><span data-stu-id="c0c91-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="c0c91-616">انتقِ من الموقع *SORT* ولوحة الترخيص الهدف *PLP02*، والذي يحتوي على أصناف متعددة وكمية بالقيمة *1*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-616">Pick from the *SORT* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="c0c91-617">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-617">Select **OK**.</span></span>
1. <span data-ttu-id="c0c91-618">تظهر صفحة **انتقاء المخزون الذي تم فرزه: وضع** عمل الوضع الذي يجب إنجازه.</span><span class="sxs-lookup"><span data-stu-id="c0c91-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="c0c91-619">ضع الموقع *Baydoor* ولوحة الترخيص الهدف *PLP02*، والذي يحتوي على أصناف متعددة وكمية بالقيمة *1*.</span><span class="sxs-lookup"><span data-stu-id="c0c91-619">Put to the *Baydoor* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="c0c91-620">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0c91-620">Select **OK**.</span></span>

    <span data-ttu-id="c0c91-621">اكتمل العمل.</span><span class="sxs-lookup"><span data-stu-id="c0c91-621">Work is completed.</span></span>

<span data-ttu-id="c0c91-622">من الآن فصاعدًا، يتم تطبيق كافة عمليات المستودع الأخرى.</span><span class="sxs-lookup"><span data-stu-id="c0c91-622">From this point forward, all other warehouse processes apply.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]