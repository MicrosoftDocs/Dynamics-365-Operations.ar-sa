---
title: الفرز الصادر
description: يوفر هذا الموضوع معلومات حول الفرز الخارجي. تسهل هذه الوظيفة معالجة الحاويات الصغيرة، وتساعد موظفي المستودع على تخطيط قدرة البالتات وتنظيمها في الشاحنة بشكل أفضل.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 84c4ec83ed16762e6c3c1a22425cf60e5b3ae8da
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4421788"
---
# <a name="outbound-sorting"></a><span data-ttu-id="2d9b4-104">الفرز الصادر</span><span class="sxs-lookup"><span data-stu-id="2d9b4-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d9b4-105">تسهل هذه الوظيفة معالجة الحاويات الصغيرة وتساعد موظفي المستودع على تخطيط قدرة البالتات وتنظيمها في الشاحنة بشكل أفضل.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="2d9b4-106">عند استخدام الفرز الخارجي، يمكنك فرز الحاويات المُعبأة‬ في البالتة الصحيحة بعد وصولها إلى محطة التعبئة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="2d9b4-107">يمكنك أيضًا إنشاء تدرج هرمي للتعبئة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="2d9b4-108">تتيح لك هذه الوظيفة إنشاء بالتات من الحاويات التي تتم تعبئتها من خلال وظيفة التعبئة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="2d9b4-109">لا يتم إرسال الحاوية إلى موقع الشحن النهائي كما هو الحال في تدفق التعبئة الأصلي.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="2d9b4-110">ويمكن للعاملين بدلاً من ذلك إغلاق الحاوية ونقلها إلى موقع نوع الفرز.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="2d9b4-111">ويمكن عندها فرز الحاويات إلى مواضع، تحتوي كل منها على لوحة ترخيص (LP).</span><span class="sxs-lookup"><span data-stu-id="2d9b4-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="2d9b4-112">وبعد فرز الحاويات يمكن إنشاء العمل لإرسال لوحات الترخيص بأكملها إلى موقع إرساء الشحن النهائي أو موقع المرحلة، استنادًا إلى توجيهات المواقع أو متطلباتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="2d9b4-113">ويمكن بالإضافة إلى ذلك لإجراء إغلاق موضع الفرز نقل المخزون إلى موقع الشحن النهائي فورًا وانتقائه إلى الأمر.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="2d9b4-114">تشغيل ميزة الفرز الخارجي</span><span class="sxs-lookup"><span data-stu-id="2d9b4-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="2d9b4-115">قبل أن تتمكن من استخدام الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="2d9b4-116">بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="2d9b4-117">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2d9b4-118">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="2d9b4-119">**اسم الميزة:** *الفرز الخارجي*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="2d9b4-120">الإعداد</span><span class="sxs-lookup"><span data-stu-id="2d9b4-120">Setup</span></span>

<span data-ttu-id="2d9b4-121">بالنسبة لهذا السيناريو، يجب استخدام بيانات العرض التوضيحي القياسية **USMF** والمستودع *62*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="2d9b4-122">ويجب أيضًا إكمال الإعداد الموضح في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="2d9b4-123">إعداد قالب موجة</span><span class="sxs-lookup"><span data-stu-id="2d9b4-123">Set up a wave template</span></span>

<span data-ttu-id="2d9b4-124">يعاج هذا الإعداد الموجة وينشئ العمل تلقائيًا عند تحرير سطر بالمستودع.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="2d9b4-125">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجة**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="2d9b4-126">في قائمة القوالب، حدد **المستودع 62**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="2d9b4-127">في علامة التبويب السريعة **عام**، تأكد من تعيين الخيار **معالجة الموجة عند الإصدار إلى مستودع** على القيمة *نعم*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="2d9b4-128">إعداد عامل</span><span class="sxs-lookup"><span data-stu-id="2d9b4-128">Set up a worker</span></span>

<span data-ttu-id="2d9b4-129">تعتبر محطة التعبئة موقعًا.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-129">The packing station is considered a location.</span></span> <span data-ttu-id="2d9b4-130">يراجع موظفو المستودع الذين يسجلون الدخول بمحطة التعبئة ويعملون فقط على الشحنات والحاويات التي يتم تخطيطها في موقع التعبئة المحدد.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="2d9b4-131">ويجب إعداد المستخدم الذي يسجل الدخول إلى Microsoft Dynamics 365 كعامل في إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="2d9b4-132">إذا لم يظهر اسم المستخدم في قائمة مستخدمي العمل، استخدم الإجراء التالي لإضافته.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="2d9b4-133">تفترض هذه الخطوات وجود المستخدم بالفعل في النظام وإقرانه كموظف أو عامل في وحدة **الموارد البشرية** النمطية.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="2d9b4-134">انتقل إلى **إدارة المستودعات \> الإعداد \> العامل**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="2d9b4-135">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-135">Select **New**.</span></span>
1. <span data-ttu-id="2d9b4-136">في الحقل **العامل**، حدد المستخدم الهدف في قائمة الموظفين.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="2d9b4-137">حدد **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-137">Select **Select**.</span></span>
1. <span data-ttu-id="2d9b4-138">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="2d9b4-139">في علامة التبويب السريعة **المستخدمين**، حدد **جديد** لإنشاء حساب للجهاز المحمول، وعيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="2d9b4-140">**معرف المستخدم:** أدخل معرفًا فريدًا.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="2d9b4-141">**اسم المستخدم:** أدخل اسمًا للمعرف.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="2d9b4-142">**المستودع الافتراضي:** *62*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="2d9b4-143">**اسم القائمة:** *الأساسي*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="2d9b4-144">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="2d9b4-145">يظهر مربع الحوار **تعيين كلمة المرور**، حيث يمكنك إنشاء كلمة مرور بسيطة يمكن للمستخدم استخدامها لتسجيل الدخول إلى تطبيق الأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="2d9b4-146">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-146">Set the following values:</span></span>

    - <span data-ttu-id="2d9b4-147">**كلمه المرور:** أدخل كلمة مرور بسيطة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="2d9b4-148">**تأكيد كلمة المرور:** أدخل نفس كلمة المرور مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="2d9b4-149">حدد **تعيين كلمة المرور**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-149">Select **Set password**.</span></span>

    <span data-ttu-id="2d9b4-150">يعلمك إخطار في مركز الصيانة بتعيين كلمة المرور للمستخدم الذي أنشأته.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="2d9b4-151">إنشاء نوع موقع</span><span class="sxs-lookup"><span data-stu-id="2d9b4-151">Create a location type</span></span>

1. <span data-ttu-id="2d9b4-152">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> أنواع المواقع**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="2d9b4-153">في جزء الإجراءات، حدد **جديد** لإنشاء نوع الموقع وعيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="2d9b4-154">**نوع الموقع:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="2d9b4-155">**الوصف:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="2d9b4-156">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="2d9b4-157">إعداد معلمات إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="2d9b4-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="2d9b4-158">انتقل إلى **إدارة المستودعات‬\> إعداد‬ \> محددات إدارة المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="2d9b4-159">في علامة التبويب **عام**، في علامة التبويب السريعة **أنواع المواقع**، عيِّن الحقل **نوع موقع الفرز** على *SORT*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="2d9b4-160">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="2d9b4-161">إعداد ملف تعريف موقع</span><span class="sxs-lookup"><span data-stu-id="2d9b4-161">Set up a location profile</span></span>

1. <span data-ttu-id="2d9b4-162">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> ملفات تعريف الموقع**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="2d9b4-163">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2d9b4-164">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-165">**معرف ملف تعريف الموقع:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="2d9b4-166">**الاسم:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="2d9b4-167">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-168">**تنسيق الموقع:** *ASRB* (الممر-الحامل-الرف-السلة)</span><span class="sxs-lookup"><span data-stu-id="2d9b4-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="2d9b4-169">**نوع الموقع:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="2d9b4-170">**استخدام تعقب لوحة الترخيص:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="2d9b4-171">**السماح بالعناصر المختلطة:** *نعم* (عند تعيين هذا الخيار على القيمة *نعم*، يتم تعيين الخيار **‏‫السماح بدُفعات المخزون المختلطة** تلقائيًا على القيمة *نعم* ولا يمكن تغييره بشكل مستقل).</span><span class="sxs-lookup"><span data-stu-id="2d9b4-171">**Allow mixed items:** *Yes* (When you set this option to *Yes*, the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="2d9b4-172">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="2d9b4-173">إعداد موقع</span><span class="sxs-lookup"><span data-stu-id="2d9b4-173">Set up a location</span></span>

1. <span data-ttu-id="2d9b4-174">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> المواقع**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="2d9b4-175">في الرأس، امسح خانة الاختيار **إنشاء أرقام شيكات للموقع**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="2d9b4-176">في جزء الإجراءات، حدد **جديد** لإنشاء موقع وعيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="2d9b4-177">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="2d9b4-178">**الموقع:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="2d9b4-179">**معرف ملف تعريف الموقع:** *SORTING*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="2d9b4-180">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="2d9b4-181">إعداد قالب الفرز الخارجي</span><span class="sxs-lookup"><span data-stu-id="2d9b4-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="2d9b4-182">يحدد قالب الفرز الخارجي ما إذا كان العمل قد تم إنشاؤه خارج موقع الفرز، وما إذا كان قد تم الفرز يدويًا أو تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="2d9b4-183">بالنسبة لهذا السيناريو، ستنشئ قالب الفرز الخارجي لبناء البالتات بعد محطة التعبئة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="2d9b4-184">انتقل إلى **إدارة المستودعات \> الإعداد \> التعبئة \> قالب الفرز الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="2d9b4-185">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2d9b4-186">في رأس القالب الجديد، عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-187">**معرف قالب الفرز الخارجي:** *العمل تلقائيًا*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="2d9b4-188">**الوصف:** *إنشاء العمل تلقائيًا*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="2d9b4-189">**نوع قالب الفرز الخارجي:** *حاوية*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="2d9b4-190">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="2d9b4-191">**الموقع:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="2d9b4-192">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-193">**التحقق من الفرز:** *مسح الموضع*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="2d9b4-194">**إنشاء عمل عند إغلاق الموضع:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="2d9b4-195">عند تحديد هذا الخيار على القيمة *نعم*، سيتم إنشاء عمل عند إغلاق الموضع لنقل المخزون إلى موقع الشحن النهائي.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-195">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="2d9b4-196">وعند التعيين على القيمة *لا*، سيتم انتقاء المخزون إلى الأمر فورًا عند إغلاق الموضع.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-196">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="2d9b4-197">**تعيين الموضع:** *تلقائيًا*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="2d9b4-198">عند تعيين هذا الحقل على القيمة *يدويًا*، يجب على المستخدم أن يشير دائمًا إلى موضع فرز المخزون.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-198">If this field is set to *Manual*, the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="2d9b4-199">عند التعيين على القيمة *تلقائيًا*، سيرشد النظام المخزون تلقائيًا إلى موضع إذا أمكن، استنادًا إلى فواصل قالب الفرز.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-199">If it's set to *Automatic*, the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="2d9b4-200">حدد **حفظ** لإتاحة الزر **تحرير الاستعلام** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="2d9b4-201">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="2d9b4-202">في محرر الاستعلام، في علامة التبويب **فرز**، أضف سطرًا بالقيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="2d9b4-203">**الجدول:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="2d9b4-204">**الجدول المشتق:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="2d9b4-205">**الحقل:** *خدمة شركة النقل*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="2d9b4-206">بتحديد هذه القيمة، قد تتلقى الرسالة التالية: "خدمة شركة الشحن الميدانية ليست حقل فهرس.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="2d9b4-207">هل ترغب في إضافة فرز لها؟"</span><span class="sxs-lookup"><span data-stu-id="2d9b4-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="2d9b4-208">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-208">Select **Yes**.</span></span>

    - <span data-ttu-id="2d9b4-209">**اتجاه البحث:** *تصاعدي*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="2d9b4-210">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-210">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-211">قد تتلقى الرسالة التالية: "ستتم إعادة تعيين التجميع، هل تريد المتابعة؟"</span><span class="sxs-lookup"><span data-stu-id="2d9b4-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="2d9b4-212">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-212">Select **Yes**.</span></span>

    <span data-ttu-id="2d9b4-213">يصبح الزر **فواصل قوالب الفرز الخارجي** في جزء الإجراءات متاحًا.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="2d9b4-214">في جزء الإجراءات، حدد **فواصل قوالب الفرز الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="2d9b4-215">في مربع الحوار **معايير الفرز الخارجي**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-216">**اسم الجدول المرجعي:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="2d9b4-217">**اسم الحقل المرجعي:** *خدمة شركة الشحن*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="2d9b4-218">**تجميع حسب الحقل:** حدد خانة الاختيار هذه لتجميع الشحنات حسب خدمة شركة الشحن.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="2d9b4-219">حدد **موافق** لحفظ إعداداتك وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="2d9b4-220">إعداد سياسات تعبئة الحاويات</span><span class="sxs-lookup"><span data-stu-id="2d9b4-220">Set up container packing policies</span></span>

1. <span data-ttu-id="2d9b4-221">انتقل إلى **إدارة المستودعات \> الإعداد \> الحاويات \> سياسات تعبئة الحاويات**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="2d9b4-222">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2d9b4-223">في رأس السياسة الجديدة، عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-224">**سياسة تعبئة الحاويات:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="2d9b4-225">**الوصف:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="2d9b4-226">في علامة التبويب السريعة **نظرة عامة**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-227">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="2d9b4-228">**الموقع الافتراضي للفرز:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="2d9b4-229">**وحدة الوزن:** *كجم*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="2d9b4-230">**سياسة إغلاق الحاوية:** *الإصدار التلقائي*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="2d9b4-231">**سياسة إصدار الحاوية:** *تعيين حاوية إلى موضع الفرز الخارجي*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="2d9b4-232">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="2d9b4-233">إعداد ملفات تعريف التعبئة</span><span class="sxs-lookup"><span data-stu-id="2d9b4-233">Set up packing profiles</span></span>

<span data-ttu-id="2d9b4-234">قم بإنشاء ملف تعريف تعبئة جديد لاستخدامه مع وظيفة الفرز.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="2d9b4-235">انتقل إلى **إدارة المستودعات \> الإعداد \> التعبئة \> ملفات تعريف التعبئة**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="2d9b4-236">في جزء الإجراءات، حدد **جديد** لإنشاء سطر وعيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="2d9b4-237">**معرف ملف تعريف التعبئة:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="2d9b4-238">**الوصف:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="2d9b4-239">**سياسة تعبئة الحاويات:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="2d9b4-240">**وضع معرف الحاوية:** *تلقائي*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="2d9b4-241">**نوع الحاوية:** *صندوق كبير*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="2d9b4-242">**إنشاء حاوية تلقائيًا عند إغلاق الحاوية:** تم المسح (= *لا*)</span><span class="sxs-lookup"><span data-stu-id="2d9b4-242">**Auto create container at container close:** Cleared (= *No*)</span></span>

1. <span data-ttu-id="2d9b4-243">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="2d9b4-244">إعداد فئات العمل</span><span class="sxs-lookup"><span data-stu-id="2d9b4-244">Set up work classes</span></span>

<span data-ttu-id="2d9b4-245">قم بإعداد فئة العمل التي سيتم استخدامها مع الفرز.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="2d9b4-246">انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> فئات العمل**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="2d9b4-247">في جزء الإجراءات، حدد **جديد** لإنشاء لإنشاء فئة عمل للفرز وعيِّن القيم التالية لها:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="2d9b4-248">**معرف فئة العمل:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="2d9b4-249">**الوصف:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="2d9b4-250">**نوع أمر العمل:** *انتقاء المخزون الذي تم فرزه*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="2d9b4-251">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="2d9b4-252">إعداد عناصر القائمة للأجهزة المحمولة</span><span class="sxs-lookup"><span data-stu-id="2d9b4-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="2d9b4-253">إعداد عنصر قائمة بالتة جديدة</span><span class="sxs-lookup"><span data-stu-id="2d9b4-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="2d9b4-254">إنشاء عنصر قائمة للجهاز المحمول لإنشاء البالتات اثناء الفرز.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="2d9b4-255">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="2d9b4-256">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2d9b4-257">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-258">**اسم عنصر القائمة:** *بناء بالتة*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="2d9b4-259">**العنوان:** *إنشاء البالتات*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="2d9b4-260">**الوضع:** *غير مباشر*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="2d9b4-261">**استخدام العمل الموجود:** *لا*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="2d9b4-262">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-263">**رمز النشاط:** *فرز خارجي*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="2d9b4-264">عند تعيين هذا الحقل على *فرز خارجي*، يظهر الحقل **معرف قالب الفرز الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-264">When this field is set to *Outbound sorting*, the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="2d9b4-265">**استخدام دليل المعالجة:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="2d9b4-266">عند تعيين الحقل **رمز النشاط** على *فرز خارجي*، يتم تعيين هذا الخيار تلقائيًا على *نعم*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-266">When the **Activity code** field is set to *Outbound sorting*, this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="2d9b4-267">**معرف قالب الفرز الخارجي:** *العمل تلقائيًا*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="2d9b4-268">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="2d9b4-269">إعداد عنصر قائمة تحميل جديد</span><span class="sxs-lookup"><span data-stu-id="2d9b4-269">Set up a new loading menu item</span></span>

<span data-ttu-id="2d9b4-270">انشئ بعد ذلك عنصر قائمة يتيح للمستخدمين نقل أصناف المخزون التي تم فرزها إلى موقع الشحن.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="2d9b4-271">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="2d9b4-272">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2d9b4-273">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-274">**اسم عنصر القائمة:** *تحميل من الفرز*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="2d9b4-275">**العنوان:** *تحميل من الفرز*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="2d9b4-276">**الوضع:** *العمل*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="2d9b4-277">**استخدام العمل الموجود:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="2d9b4-278">في علامة التبويب السريعة **عام**، عيِّن الحقل **موجه بواسطة** على *موجه بواسطة المستخدم*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="2d9b4-279">في علامة التبويب السريعة **فئات العمل**، حدد **جديد**، ثم عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-279">On the **Work classes** FastTab, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="2d9b4-280">**معرف فئة العمل:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="2d9b4-281">**نوع أمر العمل:** *انتقاء المخزون الذي تم فرزه*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="2d9b4-282">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="2d9b4-283">إعداد قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="2d9b4-283">Set up the mobile device menu</span></span>

<span data-ttu-id="2d9b4-284">يجب الآن إضافة عناصر القائمة الجديدة إلى قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="2d9b4-285">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="2d9b4-286">حدد قائمة **الصادر**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="2d9b4-287">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2d9b4-288">في عمود **القوائم المتوفرة وعناصر القائمة**، ابحث عن **بناء بالتة** وحددها.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="2d9b4-289">حدد زر السهم الأيمن لنقل **بناء بالتة** إلى العمود **بنية القائمة**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="2d9b4-290">استخدم أزرار السهم لأعلى والسهم لأسفل لوضع عنصر قائمة **بناء بالتة** في الموضع الموضح في قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="2d9b4-291">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-291">Select **Save**.</span></span>
1. <span data-ttu-id="2d9b4-292">كرر هذا الإجراء لإضافة عنصر القائمة **تحميل من الفرز** إلى القائمة **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="2d9b4-293">إعداد توجيهات الموقع</span><span class="sxs-lookup"><span data-stu-id="2d9b4-293">Set up location directives</span></span>

<span data-ttu-id="2d9b4-294">*توجيهات الموقع* هي قواعد تساعد في تحديد انتقاء ووضع مواقع لحركة المخزون.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="2d9b4-295">يجب الآن إنشاء قاعدة لإدارة عمل الفرز.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="2d9b4-296">إعداد توجيه بوحدة SKU مفردة</span><span class="sxs-lookup"><span data-stu-id="2d9b4-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="2d9b4-297">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="2d9b4-298">في الجزء الأيمن، غير قيمة الحقل **نوع أمر العمل** إلى *انتقاء المخزون الذي تم فرزه*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="2d9b4-299">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2d9b4-300">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-301">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="2d9b4-302">**الاسم:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="2d9b4-303">في علامة التبويب السريعة **توجيهات الموقع**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-304">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="2d9b4-305">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-305">**Site:** *6*</span></span>
    - <span data-ttu-id="2d9b4-306">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="2d9b4-307">**وحدة SKU متعددة:** *لا*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="2d9b4-308">حدد **حفظ** لإتاحة شريط الأدوات في علامة التبويب السريعة **السطور**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="2d9b4-309">في علامة التبويب السريعة **السطور**، حدد **جديد**، ثم عيِّن القيم التالية في السطر الجديد.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-309">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="2d9b4-310">اقبل القيم الافتراضية لكافة الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="2d9b4-311">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="2d9b4-312">**من:** *0*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-312">**From:** *0*</span></span>
    - <span data-ttu-id="2d9b4-313">**إلى:** *1,000,000*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="2d9b4-314">حدد **حفظ** لإتاحة شريط الأدوات في علامة التبويب السريعة **إجراءات توجيه الموقع**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="2d9b4-315">في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **جديد**، ثم عيِّن القيم التالية في السطر الجديد.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-315">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="2d9b4-316">اقبل القيم الافتراضية لكافة الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="2d9b4-317">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="2d9b4-318">**الاسم:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="2d9b4-319">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-319">Select **Save**.</span></span>
1. <span data-ttu-id="2d9b4-320">في علامة التبويب السريعة **إجراءات توجيه المواقع**، حدد **تحرير الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="2d9b4-321">في محرر الاستعلام، في علامة التبويب **النطاق**، ابحث عن الصف الذي يحتوي على حقل **المجال** المعين إلى *الموقع*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="2d9b4-322">عيِّن حقل **المعايير** لهذا الصف على *Baydoor*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="2d9b4-323">حدد **موافق** لحفظ الإعدادات وإغلاق محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="2d9b4-324">إعداد توجيه بوحدة SKU متعددة</span><span class="sxs-lookup"><span data-stu-id="2d9b4-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="2d9b4-325">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="2d9b4-326">في الجزء الأيمن، غير قيمة الحقل **نوع أمر العمل** إلى *انتقاء المخزون الذي تم فرزه*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="2d9b4-327">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2d9b4-328">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-329">**التسلسل:** *2*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="2d9b4-330">**الاسم:** *Baydoor متعدد*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="2d9b4-331">في علامة التبويب السريعة **توجيهات الموقع**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-332">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="2d9b4-333">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-333">**Site:** *6*</span></span>
    - <span data-ttu-id="2d9b4-334">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="2d9b4-335">**وحدة SKU متعدد:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="2d9b4-336">حدد **حفظ** لإتاحة شريط الأدوات في علامة التبويب السريعة **السطور**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="2d9b4-337">في علامة التبويب السريعة **السطور**، حدد **جديد**، ثم عيِّن القيم التالية في السطر الجديد.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-337">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="2d9b4-338">اقبل القيم الافتراضية لكافة الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="2d9b4-339">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="2d9b4-340">**من:** *0*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-340">**From:** *0*</span></span>
    - <span data-ttu-id="2d9b4-341">**إلى:** *1,000,000*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="2d9b4-342">حدد **حفظ** لإتاحة شريط الأدوات في علامة التبويب السريعة **إجراءات توجيه الموقع**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="2d9b4-343">في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **جديد**، ثم عيِّن القيم التالية في السطر الجديد.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-343">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="2d9b4-344">اقبل القيم الافتراضية لكافة الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="2d9b4-345">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="2d9b4-346">**الاسم:** *Baydoor متعدد*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="2d9b4-347">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-347">Select **Save**.</span></span>
1. <span data-ttu-id="2d9b4-348">في علامة التبويب السريعة **إجراءات توجيه المواقع**، حدد **تحرير الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="2d9b4-349">في محرر الاستعلام، في علامة التبويب **النطاق**، ابحث عن الصف الذي يحتوي على حقل **المجال** المعين إلى *الموقع*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="2d9b4-350">عيِّن حقل **المعايير** لهذا الصف على *Baydoor*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="2d9b4-351">حدد **موافق** لحفظ الإعدادات وإغلاق محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="2d9b4-352">إعداد قوالب العمل</span><span class="sxs-lookup"><span data-stu-id="2d9b4-352">Set up work templates</span></span>

1. <span data-ttu-id="2d9b4-353">انتقل إلى **إدارة المستودعات \> إعداد \> عمل \> قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="2d9b4-354">غير قيمة الحقل **نوع أمر العمل** إلى *انتقاء المخزون الذي تم فرزه*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="2d9b4-355">في جزء الإجراءات، حدد **جديد** لإنشاء قالب عمل.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="2d9b4-356">في علامة التبويب **نظرة عامة**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-357">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="2d9b4-358">**قالب العمل:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="2d9b4-359">**وصف قالب العمل:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="2d9b4-360">حدد **حفظ** لجعل علامة التبويب السريعة **تفاصيل قالب العمل** متاحة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="2d9b4-361">في علامة التبويب السريعة **تفاصيل قالب العمل**، حدد **جديد** لإضافة سطر، ثم عيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="2d9b4-362">**نوع العمل:** *انتقاء*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="2d9b4-363">**معرف فئة العمل:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="2d9b4-364">حدد **جديد** مرة أخرى لإضافة سطر ثان، ثم عيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="2d9b4-365">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="2d9b4-366">**معرف فئة العمل:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="2d9b4-367">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="2d9b4-368">سيناريو</span><span class="sxs-lookup"><span data-stu-id="2d9b4-368">Scenario</span></span>

<span data-ttu-id="2d9b4-369">يحاكي هذا السيناريو موقفًا حيث ينبغي فرز الحاويات المعبأة تلقائيًا في مواقع (بالتات) مختلفة بعد محطة التعبئة، وذلك وفقًا لخدمة شركة الشحن.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="2d9b4-370">بعد تعبئة كافة الأصناف من التحميل وفرزها حسب العنوان، يتم نقل البالتات إلى باب المرسى.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="2d9b4-371">إنشاء أوامر مبيعات وعمل انتقاء</span><span class="sxs-lookup"><span data-stu-id="2d9b4-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="2d9b4-372">إنشاء أمر مبيعات 1</span><span class="sxs-lookup"><span data-stu-id="2d9b4-372">Create sales order 1</span></span>

1. <span data-ttu-id="2d9b4-373">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="2d9b4-374">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2d9b4-375">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-376">**حساب العميل:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="2d9b4-377">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="2d9b4-378">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="2d9b4-379">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="2d9b4-380">قم بالتبديل إلى طريقة عرض **الرأس**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="2d9b4-381">في علامة التبويب السريعة **التسليم**، في قسم **النقل**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-382">**شركة الشحن:** *Air cargo*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="2d9b4-383">**خدمة شركة النقل:** *Air*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="2d9b4-384">قم بالتبديل إلى طريقة عرض **السطور**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="2d9b4-385">في حالة عدم إضافة سطر جديد خالٍ للشبكة تلقائيًا في علامة التبويب السريعة **سطور أمر المبيعات**، حدد **إضافة سطر** لإضافة واحد.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="2d9b4-386">في سطر الأمر الجديد، عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-387">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="2d9b4-388">**الكمية:** *2*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="2d9b4-389">أثناء تحديد سطر الأمر الجديد في علامة التبويب السريعة **سطور أمر المبيعات**، في قائمة **المخزون** أعلى الشبكة، حدد **حجز**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="2d9b4-390">في صفحة **الحجز**، حدد **حجز دفعة** لحجز الكمية الكاملة للسطر المحدد في المستودع.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="2d9b4-391">قم بإغلاق صفحة **الحجز** للعودة إلى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="2d9b4-392">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، في مجموعة **الإجراءات**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="2d9b4-393">ستستلم رسالة معلوماتية توضح الشحنة والموجة لهذا الأمر.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="2d9b4-394">قم بتدوين رقم معرف الموجة ورقم معرف الشحنة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="2d9b4-395">أمر المبيعات 2</span><span class="sxs-lookup"><span data-stu-id="2d9b4-395">Sales order 2</span></span>

1. <span data-ttu-id="2d9b4-396">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="2d9b4-397">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2d9b4-398">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-399">**حساب العميل:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="2d9b4-400">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="2d9b4-401">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="2d9b4-402">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-402">The new sales order is opened.</span></span> <span data-ttu-id="2d9b4-403">ويجب أن يتضمن بندًا فارغًا جديدًا في الشبكة في علامة التبويب السريعة **بنود أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="2d9b4-404">عيِّن القيم التالية في سطر الأمر:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="2d9b4-405">**الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="2d9b4-406">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="2d9b4-407">في علامة التبويب السريعة **تفاصيل السطر**، في علامة التبويب **التسليم** عيٍّن الحقل **وضع التسليم** على *Flowe-STD*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="2d9b4-408">في علامة التبويب السريعة **سطور أمر المبيعات**، حدد **إضافة سطر**، ثم عيِّن القيم التالية في سطر الأمر الثاني:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-408">On the **Sales order lines** FastTab, select **Add line**, and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="2d9b4-409">**الصنف:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="2d9b4-410">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="2d9b4-411">في علامة التبويب السريعة **تفاصيل السطر**، في علامة التبويب **التسليم** غير قيمة الحقل **وضع التسليم** على *Air C-Air*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="2d9b4-412">في علامة التبويب السريعة **سطور أمر المبيعات**، حدد سطر الأمر الأول.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="2d9b4-413">وفي قائمة **المخزون** أعلى الشبكة، حدد **حجز**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="2d9b4-414">في صفحة **الحجز**، حدد **حجز دفعة** لحجز الكمية الكاملة للسطر المحدد في المستودع.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="2d9b4-415">قم بإغلاق صفحة **الحجز** للعودة إلى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="2d9b4-416">في علامة التبويب السريعة **سطور أمر المبيعات**، حدد سطر الأمر الثاني.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="2d9b4-417">وفي قائمة **المخزون** أعلى الشبكة، حدد **حجز**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="2d9b4-418">في صفحة **الحجز**، حدد **حجز دفعة** لحجز الكمية الكاملة للسطر المحدد في المستودع.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="2d9b4-419">قم بإغلاق صفحة **الحجز** للعودة إلى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="2d9b4-420">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، في مجموعة **الإجراءات**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="2d9b4-421">ستستلم رسالة معلوماتية توضح الشحنة والموجة لهذا الأمر.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="2d9b4-422">لاحظ أنه تم إنشاء رقمين لمعرف الموجة ورقمين لمعرف الشحنة، واحد لكل وضع من أوضاع التسليم لسطور أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="2d9b4-423">الحصول على معرفات العمل من تفاصيل العمل</span><span class="sxs-lookup"><span data-stu-id="2d9b4-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="2d9b4-424">انتقل إلى **إدارة المستودعات \> العمل \> تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="2d9b4-425">تعرض الصفحة معرفات العمل التي تم إنشاؤها من أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="2d9b4-426">استخدم معرفات الموجات ومعرفات الشحنات من أوامر المبيعات التي أنشأتها للعثور على معرف العمل لكل موجة وشحنة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="2d9b4-427">دون معرفات العمل هذة، لأنك ستحتاجها في الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="2d9b4-428">لاحظ أنه تم إنشاء معرفي عمل لأمر المبيعات الثاني.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="2d9b4-429">في حالة انتقاء أصناف مختلفة من مواقع مختلفة، يتم إنشاء معرفات بكلمات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="2d9b4-430">انتقاء الأصناف لأوامر المبيعات</span><span class="sxs-lookup"><span data-stu-id="2d9b4-430">Pick items for the sales orders</span></span>

<span data-ttu-id="2d9b4-431">أكمل العمل الذي تم إنشاؤه باستخدام الجهاز المحمول لنقل الأصناف إلى محطة التعبئة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="2d9b4-432">على الجهاز المحمول، سجِّل الدخول إلى المستودع *62* باستخدام معرف المستخدم الذي أنشأته لهذا السيناريو (أو معرف المستخدم لمستخدم بيانات العرض التوضيحي موجود).</span><span class="sxs-lookup"><span data-stu-id="2d9b4-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="2d9b4-433">من القائمة الرئيسية، حدد **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="2d9b4-434">من القائمة **خارجي**، حدد **انتقاء المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="2d9b4-435">في حقل **المعرف**، أدخل معرف العمل الذي تم إنشاؤه لأمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="2d9b4-436">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-436">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-437">في صفحة **أوامر المبيعات - الانتقاء**، أدخل لوحة الترخيص الهدف التي تم إنشاؤها لأمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="2d9b4-438">لاحظ أنه يتم عرض موقع الانتقاء ( *المجموعة-001*) والصنف ( *A0001*) والكمية ( *قطعتين*).</span><span class="sxs-lookup"><span data-stu-id="2d9b4-438">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*2 pcs*) are shown.</span></span>
1. <span data-ttu-id="2d9b4-439">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-439">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-440">راجع المعلومات الموجودة في صفحة **أوامر المبيعات - وضع**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="2d9b4-441">ينبغي أن يشير الحقل **الموقع** إلى انتقال الأصناف المنتقاة إلى موقع *التعبئة*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="2d9b4-442">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-442">Select **OK**.</span></span>

    <span data-ttu-id="2d9b4-443">تتلقى في صفحة **مسح معرف العمل/معرف لوحة الترخيص** رسالة "اكتمل العمل"، والتي تشير إلى أنه تم إكمال معرف العمل من أمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="2d9b4-444">ستقوم الآن بانتقاء أمر المبيعات رقم 2.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="2d9b4-445">في حقل **المعرف**، أدخل معرف العمل الذي تم إنشاؤه لأمر المبيعات رقم 2 حيث يحتوي السطر رقم 1 على الصنف *A0001*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="2d9b4-446">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-446">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-447">في الصفحة **أوامر المبيعات - الانتقاء**، أدخل لوحة ترخيص هدف.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="2d9b4-448">لاحظ أنه يتم عرض موقع الانتقاء ( *المجموعة-001*) والصنف ( *A0001*) والكمية ( *قطعتين*).</span><span class="sxs-lookup"><span data-stu-id="2d9b4-448">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="2d9b4-449">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-449">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-450">راجع المعلومات الموجودة في صفحة **أوامر المبيعات - وضع**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="2d9b4-451">ينبغي أن يشير الحقل **الموقع** إلى انتقال الأصناف المنتقاة إلى موقع *التعبئة*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="2d9b4-452">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-452">Select **OK**.</span></span>

    <span data-ttu-id="2d9b4-453">في الصفحة **مسح معرف العمل/معرف لوحة الترخيص**، تتلقى رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="2d9b4-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="2d9b4-454">وتشير هذه الرسالة إلى أنه تم إكمال معرف العمل من السطر 1 لأمر المبيعات 2.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="2d9b4-455">في حقل **المعرف**، أدخل معرف العمل الذي تم إنشاؤه لأمر المبيعات رقم 2 حيث يحتوي السطر رقم 2 على الصنف *A0002*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="2d9b4-456">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-456">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-457">في الصفحة **أوامر المبيعات - الانتقاء**، أدخل لوحة ترخيص هدف.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="2d9b4-458">لاحظ أنه يتم عرض موقع الانتقاء ( *المجموعة-002*) والصنف ( *A0001*) والكمية ( *قطعتين*).</span><span class="sxs-lookup"><span data-stu-id="2d9b4-458">Notice that the picking location (*bulk-002*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="2d9b4-459">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-459">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-460">راجع المعلومات الموجودة في صفحة **أوامر المبيعات - وضع**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="2d9b4-461">ينبغي أن يشير الحقل **الموقع** إلى انتقال الأصناف المنتقاة إلى موقع *التعبئة*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="2d9b4-462">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-462">Select **OK**.</span></span>

    <span data-ttu-id="2d9b4-463">في الصفحة **مسح معرف العمل/معرف لوحة الترخيص**، تتلقى رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="2d9b4-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="2d9b4-464">وتشير هذه الرسالة إلى أنه تم إكمال معرف العمل من السطر 2 لأمر المبيعات 2.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="2d9b4-465">تعبئة أوامر المبيعات في حاويات</span><span class="sxs-lookup"><span data-stu-id="2d9b4-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="2d9b4-466">تعبئة أمر المبيعات 1 في حاويات</span><span class="sxs-lookup"><span data-stu-id="2d9b4-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="2d9b4-467">انتقل إلى **إدارة المستودعات \> التعبئة والتعبئة في حاويات \> التعبئة**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="2d9b4-468">يظهر مربع الحوار **تحديد محطة التعبئة**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="2d9b4-469">وبشكل افتراضي، ينبغي تعيين الحقل **العامل** على اسم العامل الذي قمت بإعداده مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="2d9b4-470">عيِّن القيم التالية لعرض الشحنات والحاويات التي تم تخطيطها في موقع التعبئة المحدد والتعامل معها:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="2d9b4-471">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-471">**Site:** *6*</span></span>
    - <span data-ttu-id="2d9b4-472">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="2d9b4-473">**الموقع:** *التعبئة*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="2d9b4-474">**معرف ملف تعريف التعبئة:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="2d9b4-475">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="2d9b4-476">في صفحة **التعبئة**، في الحقل **لوحة الترخيص أو الشحنة**، أدخل لوحة الترخيص الهدف لأمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="2d9b4-477">ثم حدد **علامة التبويب** أو مفتاح **Enter** في لوحة المفاتيح للانتقال خارج الحقل.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="2d9b4-478">في جزء الإجراءات، حدد **حاوية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="2d9b4-479">اقبل كافة الإعدادات الافتراضية، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="2d9b4-480">دوِّن ملاحظة بمُعرف الحاوية.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="2d9b4-481">في علامة التبويب السريعة **تعبئة الصنف**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-482">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="2d9b4-483">**المعرف:** الصنف *A0001*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="2d9b4-484">في جزء الإجراءات، حدد **إغلاق الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="2d9b4-485">في مربع الحوار **إغلاق الحاوية**، حدد **الحصول على وزن النظام** لتحديث النظام لحقل **الوزن الإجمالي**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="2d9b4-486">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-486">Select **OK**.</span></span> <span data-ttu-id="2d9b4-487">يتم نقل الحاوية إلى الموقع *SORT* وتكون جاهزة للفرز.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="2d9b4-488">انشئ حاوية ثانية لإضافة الصنف الثاني من لوحة الترخيص لأمر المبيعات 1 إلى حاوية جديدة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="2d9b4-489">في جزء الإجراءات، حدد **حاوية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="2d9b4-490">اقبل كافة الإعدادات الافتراضية، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="2d9b4-491">دوِّن ملاحظة بمُعرف الحاوية.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="2d9b4-492">في علامة التبويب السريعة **تعبئة الصنف**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-493">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="2d9b4-494">**المعرف:** الصنف *A0001*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="2d9b4-495">في جزء الإجراءات، حدد **إغلاق الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="2d9b4-496">في مربع الحوار **إغلاق الحاوية**، حدد **الحصول على وزن النظام** لتحديث النظام لحقل **الوزن الإجمالي**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="2d9b4-497">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-497">Select **OK**.</span></span> <span data-ttu-id="2d9b4-498">يتم نقل الحاوية إلى الموقع *SORT* وتكون جاهزة للفرز.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="2d9b4-499">تعبئة أمر المبيعات 2 في حاويات</span><span class="sxs-lookup"><span data-stu-id="2d9b4-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="2d9b4-500">في صفحة **التعبئة**، في الحقل **لوحة الترخيص أو الشحنة**، أدخل لوحة الترخيص الهدف للسطر 1 بأمر المبيعات 2.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="2d9b4-501">ثم حدد **علامة التبويب** أو مفتاح **Enter** في لوحة المفاتيح للانتقال خارج الحقل.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="2d9b4-502">في جزء الإجراءات، حدد **حاوية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="2d9b4-503">اقبل كافة الإعدادات الافتراضية، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="2d9b4-504">دوِّن ملاحظة بمُعرف الحاوية.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="2d9b4-505">في علامة التبويب السريعة **تعبئة الصنف**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-506">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="2d9b4-507">**المعرف:** الصنف *A0001*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="2d9b4-508">في جزء الإجراءات، حدد **إغلاق الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="2d9b4-509">في مربع الحوار **إغلاق الحاوية**، حدد **الحصول على وزن النظام** لتحديث النظام لحقل **الوزن الإجمالي**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="2d9b4-510">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-510">Select **OK**.</span></span> <span data-ttu-id="2d9b4-511">يتم نقل الحاوية إلى الموقع *SORT* وتكون جاهزة للفرز.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="2d9b4-512">في الحقل **لوحة الترخيص أو الشحنة**، أدخل لوحة الترخيص الهدف للسطر 2 بأمر المبيعات 2.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="2d9b4-513">ثم حدد **علامة التبويب** أو مفتاح **Enter** في لوحة المفاتيح للانتقال خارج الحقل.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="2d9b4-514">في جزء الإجراءات، حدد **حاوية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="2d9b4-515">اقبل كافة الإعدادات الافتراضية، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="2d9b4-516">دوِّن ملاحظة بمُعرف الحاوية.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="2d9b4-517">في علامة التبويب السريعة **تعبئة الصنف**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="2d9b4-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2d9b4-518">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="2d9b4-519">**حقل المعرف:** العنصر *A0002*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="2d9b4-520">في جزء الإجراءات، حدد **إغلاق الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="2d9b4-521">في مربع الحوار **إغلاق الحاوية**، حدد **الحصول على وزن النظام** لتحديث النظام لحقل **الوزن الإجمالي**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="2d9b4-522">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-522">Select **OK**.</span></span> <span data-ttu-id="2d9b4-523">يتم نقل الحاوية إلى الموقع *SORT* وتكون جاهزة للفرز.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="2d9b4-524">لعرض تفاصيل الحاوية، انتقل إلى **إدارة المستودعات \> التعبئة والتعبئة في حاويات \> الحاويات** وابحث عن معرفات الحاويات التي تم إنشاؤها أثناء التعبئة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers**, and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="2d9b4-525">فرز الحاويات</span><span class="sxs-lookup"><span data-stu-id="2d9b4-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d9b4-526">عند الوصول إلى عنصر القائمة **بناء بالتة** في تطبيق الأجهزة المحمولة لإجراء الفرز الخارجي، ستشاهد زرًا بالاسم **بالكامل**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="2d9b4-527">*لا تستخدم الزر **‎بالكامل** لفرز الموضع أو إغلاقه.*</span><span class="sxs-lookup"><span data-stu-id="2d9b4-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="2d9b4-528">يتوفر الزر **‎بالكامل** افتراضيًا ولا يمكن تعطيله أو إزالته من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="2d9b4-529">ولا يتم استخدامه لميزة *الفرز الخارجي*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="2d9b4-530">فرز الحاوية الأولى</span><span class="sxs-lookup"><span data-stu-id="2d9b4-530">Sort the first container</span></span>

1. <span data-ttu-id="2d9b4-531">على الجهاز المحمول، سجِّل الدخول إلى المستودع *62* باستخدام معرف المستخدم الذي أنشأته لهذا السيناريو (أو معرف المستخدم لمستخدم بيانات العرض التوضيحي موجود).</span><span class="sxs-lookup"><span data-stu-id="2d9b4-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="2d9b4-532">من القائمة الرئيسية، حدد **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="2d9b4-533">من القائمة **خارجي**، حدد **بناء بالتة**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="2d9b4-534">في الحقل **لوحة الترخيص/الحاوية**، أدخل معرف الحاوية الأولى المقترن بأمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="2d9b4-535">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-535">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-536">نظرًا لعدم وجود مواضع فرز حاليًا، يجب تحديد واحدًا.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="2d9b4-537">في الحقل **معرف موضع الفرز**، أدخل *SP01*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="2d9b4-538">نظرًا لعدم اقتران لوحة ترخيص حاليًا بموضع الفرز *SP01*، يجب تحديد واحدة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-538">Because no LP is currently associated with sort position *SP01*, you must specify one.</span></span> <span data-ttu-id="2d9b4-539">في الحقل **لوحة الترخيص**، أدخل *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="2d9b4-540">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-540">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-541">نظرًا لاًن عملية التحقق من صحة موضع الفرز قيد التشغيل، يجب إدخال معرف موضع الفرز مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="2d9b4-542">في الحقل **معرف موضع الفرز**، أدخل *SP01*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="2d9b4-543">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-543">Select **OK**.</span></span>

    <span data-ttu-id="2d9b4-544">ستتلقى رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="2d9b4-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="2d9b4-545">لعرض موضع الفرز ولوحة الترخيص فيه، انتقل إلى **إدارة المستودعات \> التعبئة والتعبئة في حاويات \> تعيينات موضع الفرز الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="2d9b4-546">تظهر صفحة **تعيينات موضع الفرز الخارجي** كافة مواضع الفرز النشطة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="2d9b4-547">يظهر الحقل **حركات موضع الفرز** لوحة الترخيص المقترنة بكل موضع فرز والحاويات الموجودة في موضع الفرز.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="2d9b4-548">لاحظ وجود موضع فرز واحد حاليًا، وأن علامة التبويب السريعة **معايير موضع الفرز** تظهر معيار **الشحنة - خدمة شركة الشحن - جوًا**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="2d9b4-549">فرز الحاويات المتبقية</span><span class="sxs-lookup"><span data-stu-id="2d9b4-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="2d9b4-550">على الجهاز المحمول، سجِّل الدخول إلى المستودع *62* باستخدام معرف المستخدم الذي أنشأته لهذا السيناريو (أو معرف المستخدم لمستخدم بيانات العرض التوضيحي موجود).</span><span class="sxs-lookup"><span data-stu-id="2d9b4-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="2d9b4-551">من القائمة الرئيسية، حدد **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="2d9b4-552">من القائمة **خارجي**، حدد **بناء بالتة**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="2d9b4-553">في الحقل **لوحة الترخيص/الحاوية**، أدخل معرف الحاوية الثانية المقترن بأمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="2d9b4-554">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-554">Select **OK**.</span></span> <span data-ttu-id="2d9b4-555">نظرًا لإعداد قالب الفرز على الفرز تلقائيًا، ووجود موضع فرز له معايير مطابقه بالفعل، سيتم توجيهك تلقائيًا إلى موضع الفرز الصحيح.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="2d9b4-556">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-556">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-557">قم بتأكيد معرف موضع الفرز للإشارة إلى وجود المخزون في المكان الصحيح.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="2d9b4-558">في الحقل **معرف موضع الفرز**، أدخل *SP01*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="2d9b4-559">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-559">Select **OK**.</span></span>

    <span data-ttu-id="2d9b4-560">اكتمل العمل في الحاوية الثانية من أمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="2d9b4-561">ستقوم الآن بفرز الحاويات المتبقية من أمر المبيعات 2.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="2d9b4-562">في الحقل **لوحة الترخيص/الحاوية**، أدخل معرف الحاوية للحاوية من أمر المبيعات 2 الذي يحتوي على الصنف *A0001*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="2d9b4-563">نظرًا لاختلاف خدمة شركة الشحن، فإنك مطالب بإدخال موضع فرز جديد وتعيين لوحة ترخيص لذلك الموضع.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="2d9b4-564">استخدم موضع الفرز *SP02* ولوحة الترخيص *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="2d9b4-565">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-565">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-566">قم بتأكيد موضع الفرز بإدخال *SP02* في الحقل **معرف موضع الفرز**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="2d9b4-567">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-567">Select **OK**.</span></span>

    <span data-ttu-id="2d9b4-568">اكتمل العمل في الحاوية.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="2d9b4-569">في الحقل **لوحة الترخيص/الحاوية**، أدخل معرف الحاوية للحاوية المتبقية من أمر المبيعات 2 الذي يحتوي على الصنف *A0002*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="2d9b4-570">ونظرًا لأن خدمة شركة الشحن هي نفسها لأمر المبيعات رقم 1، فإن النظام يعرض موضع الفرز الموجود الذي له معايير مطابقة.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="2d9b4-571">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-571">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-572">قم بتأكيد موضع الفرز بإدخال *SP01* في الحقل **معرف موضع الفرز**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="2d9b4-573">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-573">Select **OK**.</span></span>

    <span data-ttu-id="2d9b4-574">اكتمل العمل في الحاوية.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="2d9b4-575">إغلاق مواضع الفرز الخارجي</span><span class="sxs-lookup"><span data-stu-id="2d9b4-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="2d9b4-576">بمجرد فرز كل المخزون، يجب إغلاق الموضع قبل التمكن من إنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="2d9b4-577">سيتم إنشاء عمل انتقاء المخزون الذي تم فرزه لحمل المخزون إلى باب المرسى.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="2d9b4-578">إغلاق موضع من الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="2d9b4-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="2d9b4-579">على الجهاز المحمول، سجِّل الدخول إلى المستودع *62* باستخدام معرف المستخدم الذي أنشأته لهذا السيناريو (أو معرف المستخدم لمستخدم بيانات العرض التوضيحي موجود).</span><span class="sxs-lookup"><span data-stu-id="2d9b4-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="2d9b4-580">من القائمة الرئيسية، حدد **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="2d9b4-581">من القائمة **خارجي**، حدد **بناء بالتة**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="2d9b4-582">في الحقل **لوحة الترخيص/الحاوية**، أدخل معرف حاوية تم فرزها في موضع الفرز *SP01*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="2d9b4-583">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-583">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-584">ستتلقى الرسالة التالية: "تم بالفعل فرز الحاوية بالموضع SP01.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="2d9b4-585">هل تريد إغلاق الموضع؟؟</span><span class="sxs-lookup"><span data-stu-id="2d9b4-585">Close the position?"</span></span> <span data-ttu-id="2d9b4-586">حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-586">Select **Close**.</span></span>

    <span data-ttu-id="2d9b4-587">اكتمل العمل.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="2d9b4-588">إغلاق موضع من تعيينات موضع الفرز الخارجي</span><span class="sxs-lookup"><span data-stu-id="2d9b4-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="2d9b4-589">انتقل إلى **إدارة المستودعات \> التعبئة والتعبئة في حاويات \> تعيينات موضع الفرز الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="2d9b4-590">في العمود الأيمن، حدد **SP02**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="2d9b4-591">صف موضع الفرز الخارجي هذا هو الصف الوحيد الذي ستغلقه.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="2d9b4-592">في جزء الإجراءات، حدد **فتح موضع**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="2d9b4-593">سجل موضع الفرز مغلق ولم يعد ظاهرًا.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="2d9b4-594">لإظهار كافة سجلات الموضع المغلقة، حدد خانة الاختيار **إظهار المغلق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="2d9b4-595">انتقاء المخزون الذي تم فرزه</span><span class="sxs-lookup"><span data-stu-id="2d9b4-595">Sorted inventory picking</span></span>

<span data-ttu-id="2d9b4-596">يجب إكمال عمل انتقاء المخزون الذي تم فرزه.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="2d9b4-597">وعند الانتهاء من ذلك، سيتم انتقاء المخزون لأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="2d9b4-598">وعندها، يتم تطبيق كافة عمليات المستودع الأخرى.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="2d9b4-599">على الجهاز المحمول، سجِّل الدخول إلى المستودع *62* باستخدام معرف المستخدم الذي أنشأته لهذا السيناريو (أو معرف المستخدم لمستخدم بيانات العرض التوضيحي موجود).</span><span class="sxs-lookup"><span data-stu-id="2d9b4-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="2d9b4-600">من القائمة الرئيسية، حدد **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="2d9b4-601">في القائمة **خارجي**، حدد **تحميل من الفرز**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="2d9b4-602">أدخل معرف لوحة الترخيص الهدف من موضع الفرز الأول، *SP01*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="2d9b4-603">عيِّن الحقل **المعرف** على *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="2d9b4-604">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-604">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-605">تظهر صفحة **انتقاء المخزون الذي تم فرزه: الانتقاء** عمل الانتقاء الذي يجب إنجازه.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="2d9b4-606">انتقِ من الموقع *SORT* ولوحة الترخيص الهدف *PLP01*، والذي يحتوي على أصناف متعددة وكمية بالقيمة *3*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-606">Pick from the *SORT* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="2d9b4-607">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-607">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-608">تظهر صفحة **انتقاء المخزون الذي تم فرزه: وضع** عمل الوضع الذي يجب إنجازه.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="2d9b4-609">ضع الموقع *Baydoor* ولوحة الترخيص الهدف *PLP01*، والذي يحتوي على أصناف متعددة وكمية بالقيمة *3*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-609">Put to the *Baydoor* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="2d9b4-610">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-610">Select **OK**.</span></span>

    <span data-ttu-id="2d9b4-611">اكتمل العمل.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-611">Work is completed.</span></span>

1. <span data-ttu-id="2d9b4-612">أدخل معرف لوحة الترخيص الهدف من موضع الفرز الثاني، *SP02*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="2d9b4-613">عيِّن الحقل **المعرف** على *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="2d9b4-614">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-614">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-615">تظهر صفحة **انتقاء المخزون الذي تم فرزه: الانتقاء** عمل الانتقاء الذي يجب إنجازه.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="2d9b4-616">انتقِ من الموقع *SORT* ولوحة الترخيص الهدف *PLP02*، والذي يحتوي على أصناف متعددة وكمية بالقيمة *1*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-616">Pick from the *SORT* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="2d9b4-617">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-617">Select **OK**.</span></span>
1. <span data-ttu-id="2d9b4-618">تظهر صفحة **انتقاء المخزون الذي تم فرزه: وضع** عمل الوضع الذي يجب إنجازه.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="2d9b4-619">ضع الموقع *Baydoor* ولوحة الترخيص الهدف *PLP02*، والذي يحتوي على أصناف متعددة وكمية بالقيمة *1*.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-619">Put to the *Baydoor* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="2d9b4-620">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-620">Select **OK**.</span></span>

    <span data-ttu-id="2d9b4-621">اكتمل العمل.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-621">Work is completed.</span></span>

<span data-ttu-id="2d9b4-622">من الآن فصاعدًا، يتم تطبيق كافة عمليات المستودع الأخرى.</span><span class="sxs-lookup"><span data-stu-id="2d9b4-622">From this point forward, all other warehouse processes apply.</span></span>
