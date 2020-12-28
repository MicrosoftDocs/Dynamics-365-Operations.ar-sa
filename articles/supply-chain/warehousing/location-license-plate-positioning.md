---
title: ‏‫تحديد موضع لوحة ترخيص الموقع
description: يتيح لك ضبط موضع لوحة الترخيص رؤية أين توجد لوحة الترخيص في موقع متعدد البالتات، مثل الموقع الذي يستخدم رفوف بالتات مزدوجة العمق.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 7b0ebfb965e5a8f1bfe1857a9642d998dac2faf3
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4421690"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="c7917-103">‏‫تحديد موضع لوحة ترخيص الموقع</span><span class="sxs-lookup"><span data-stu-id="c7917-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7917-104">يتيح لك ضبط موضع لوحة الترخيص رؤية أين توجد لوحة الترخيص في موقع متعدد البالتات، مثل الموقع الذي يستخدم رفوف بالتات مزدوجة العمق.</span><span class="sxs-lookup"><span data-stu-id="c7917-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="c7917-105">تضيف الميزة رقمًا تسلسليًا لكل لوحة ترخيص يتم وضعها في موقع تخزين.</span><span class="sxs-lookup"><span data-stu-id="c7917-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="c7917-106">يتم استخدام رقم التسلسل هذا لترتيب لوحات الترخيص في موقع التخزين.</span><span class="sxs-lookup"><span data-stu-id="c7917-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="c7917-107">لذلك، تدعم الميزة بصورة ذكية السيناريوهات التي يستخدم فيها العملاء نظام رفوف الثقل ويجب أن يعرف، لأغراض الانتقاء، ما هي لوح الترخيص المواجهة للأمام.</span><span class="sxs-lookup"><span data-stu-id="c7917-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="c7917-108">يقدم هذا الموضوع سيناريو يوضح كيفية إعداد الميزة واستخدامها.</span><span class="sxs-lookup"><span data-stu-id="c7917-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="c7917-109">تشغيل ميزة ضبط موضع لوحة ترخيص الموقع</span><span class="sxs-lookup"><span data-stu-id="c7917-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="c7917-110">قبل أن تتمكن من استخدام ميزة ضبط موقع لوحة الترخيص، يجب تشغيلها في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c7917-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="c7917-111">بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c7917-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="c7917-112">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="c7917-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c7917-113">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="c7917-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c7917-114">**اسم الميزة:** *ضبط موضع لوحة ترخيص الموقع*</span><span class="sxs-lookup"><span data-stu-id="c7917-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="c7917-115">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="c7917-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="c7917-116">جعل بيانات العينة متاحة</span><span class="sxs-lookup"><span data-stu-id="c7917-116">Make sample data available</span></span>

<span data-ttu-id="c7917-117">للعمل في هذا السيناريو باستخدام القيم المقترحة هنا، يجب أن تعمل على نظام تم تثبيت البيانات عينة عليه.</span><span class="sxs-lookup"><span data-stu-id="c7917-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="c7917-118">بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني **USMF** قبل أن تبدأ.</span><span class="sxs-lookup"><span data-stu-id="c7917-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="c7917-119">إعداد الميزة لهذا السيناريو</span><span class="sxs-lookup"><span data-stu-id="c7917-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="c7917-120">أكمل الإجراءات التالية لإعداد ميزة *ضبط موضع لوحة ترخيص الموقع* للسيناريو الموضح في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="c7917-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="c7917-121">ملفات تعريف الموقع</span><span class="sxs-lookup"><span data-stu-id="c7917-121">Location profiles</span></span>

<span data-ttu-id="c7917-122">يجب أن تكون الميزة قيد التشغيل في ملف تعريف الموقع لكل موقع يتم استخدامه.</span><span class="sxs-lookup"><span data-stu-id="c7917-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="c7917-123">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> ملفات تعريف الموقع**.</span><span class="sxs-lookup"><span data-stu-id="c7917-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="c7917-124">في قائمة ملفات تعريف المواقع في الجزء الأيمن، حدد **BULK-06**.</span><span class="sxs-lookup"><span data-stu-id="c7917-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="c7917-125">في علامة التبويب السريعة **عام**، تمت إضافية خيارين جديدين بواسطة الميزة.</span><span class="sxs-lookup"><span data-stu-id="c7917-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="c7917-126">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c7917-126">Set the following values:</span></span>

    - <span data-ttu-id="c7917-127">**تمكين وضع لوح الترخيص:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="c7917-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="c7917-128">عند تعيين هذا الخيار على *نعم*، سيتم الاحتفاظ بموضع لوحة الترخيص للوحات الترخيص في الموقع.</span><span class="sxs-lookup"><span data-stu-id="c7917-128">When this option is set to *Yes*, the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="c7917-129">**عرض موضع LP للجهاز المحمول:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="c7917-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="c7917-130">عند تعيين هذا الخيار على *نعم*، سيتم عرض موضع لوحة الترخيص لمستخدمي الجهاز المحمول أثناء التسوية والجرد.</span><span class="sxs-lookup"><span data-stu-id="c7917-130">When this option is set to *Yes*, the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="c7917-131">يمكنك تغيير إعداد هذا الخيار فقط عند تشغيل الميزة.</span><span class="sxs-lookup"><span data-stu-id="c7917-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="c7917-132">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c7917-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="c7917-133">توجيهات الموقع</span><span class="sxs-lookup"><span data-stu-id="c7917-133">Location directives</span></span>

1. <span data-ttu-id="c7917-134">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="c7917-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="c7917-135">في الجزء الأيمن، تأكد من تعيين حقل **نوع أمر العمل** إلى *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="c7917-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="c7917-136">في قائمه توجيهات الموقع، حدد **أمر انتقاء 61 SO**.</span><span class="sxs-lookup"><span data-stu-id="c7917-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="c7917-137">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="c7917-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c7917-138">في علامة التبويب السريعة **البنود**، حدد البند الذي يحتوي على قيمة **رقم التسلسل** *2*.</span><span class="sxs-lookup"><span data-stu-id="c7917-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="c7917-139">في علامة التبويب السريعة **إجراءات التوجيه للموقع**، حدد البند الذي يحتوي على قيمة **الاسم** *انتقاء لأقل من بالته* (يجب أن يكون البند الوحيد)، وقم بتغيير قيمة **رقم التسلسل** إلى *2*.</span><span class="sxs-lookup"><span data-stu-id="c7917-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="c7917-140">حدد **جديد** أعلى الشبكة لإضافة سطر لإجراء توجيه موقع جديد.</span><span class="sxs-lookup"><span data-stu-id="c7917-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="c7917-141">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c7917-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="c7917-142">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="c7917-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="c7917-143">**الاسم:** *موضع الانتقاء 1*</span><span class="sxs-lookup"><span data-stu-id="c7917-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="c7917-144">في أثناء تحديد السطر الجديد ، حدد **تحرير استعلام** فوق الشبكة.</span><span class="sxs-lookup"><span data-stu-id="c7917-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="c7917-145">في محرر الاستعلام ، حدد علامة التبويب **الصلات**.</span><span class="sxs-lookup"><span data-stu-id="c7917-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="c7917-146">قم بتوسيع جدول **المواقع** لإظهار الصلة بجدول **أبعاد المخزون**.</span><span class="sxs-lookup"><span data-stu-id="c7917-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="c7917-147">قم بتوسيع جدول **أبعاد المخزون** لإظهار الصلة بجدول **المخزون الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="c7917-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="c7917-148">حدد **أبعاد المخزون**، ثم حدد **إضافة صلة جداول**.</span><span class="sxs-lookup"><span data-stu-id="c7917-148">Select **Inventory dimensions**, and then select **Add table join**.</span></span>
1. <span data-ttu-id="c7917-149">في قائمة الجداول التي تظهر، في عمود **العلاقة**، حدد **لوحة الترخيص (لوحة الترخيص)**.</span><span class="sxs-lookup"><span data-stu-id="c7917-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="c7917-150">ثم حدد **تحديد** لإضافة **لوحة ترخيص** إلى صلة جدول **أبعاد المخزون**.</span><span class="sxs-lookup"><span data-stu-id="c7917-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="c7917-151">بينما ما تزال **لوحة الترخيص** محددة، حدد **إضافة صلة جدول**.</span><span class="sxs-lookup"><span data-stu-id="c7917-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="c7917-152">في قائمة الجداول التي تظهر، في عمود **العلاقة**، حدد **ضبط موضع لوحة ترخيص الموقع (لوحة الترخيص)**.</span><span class="sxs-lookup"><span data-stu-id="c7917-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="c7917-153">ثم حدد **تحديد** لإضافة **ضبط موضع لوحة ترخيص الموقع** إلى صلة جدول **أبعاد المخزون**.</span><span class="sxs-lookup"><span data-stu-id="c7917-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="c7917-154">![صلات الجداول](media/LpTableJoin.png "صلات الجداول")</span><span class="sxs-lookup"><span data-stu-id="c7917-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="c7917-155">حدد **موافق** لتأكيد الجداول المرتبطة المحدثة وإغلاق محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="c7917-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="c7917-156">في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **تحرير الاستعلام** مرة أخرى لإعادة فتح محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="c7917-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="c7917-157">في علامة التبويب **النطاق**، حدد **إضافة** لإضافة بند إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="c7917-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="c7917-158">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c7917-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="c7917-159">**الجدول:** *ضبط موضع لوحة ترخيص الموقع*</span><span class="sxs-lookup"><span data-stu-id="c7917-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="c7917-160">**الجدول المشتق:** *ضبط موضع لوحة ترخيص الموقع*</span><span class="sxs-lookup"><span data-stu-id="c7917-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="c7917-161">**الحقل:** *موضع LP*</span><span class="sxs-lookup"><span data-stu-id="c7917-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="c7917-162">**المعايير:** *1*</span><span class="sxs-lookup"><span data-stu-id="c7917-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="c7917-163">![نطاق جديد](media/LpPositionCriteria.png "نطاق جديد")</span><span class="sxs-lookup"><span data-stu-id="c7917-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="c7917-164">حدد **موافق** لتأكيد تغييراتك وإغلاق محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="c7917-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="c7917-165">إعداد بيانات عينة لهذا السيناريو</span><span class="sxs-lookup"><span data-stu-id="c7917-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="c7917-166">بالنسبة لهذا السيناريو، يجب أن يقوم المستخدم بتسجيل الدخول إلى تطبيق الأجهزة المحمولة للمستودع باستخدام العامل الذي تم إعداده للمستودع *61* لتنفيذ العمل.</span><span class="sxs-lookup"><span data-stu-id="c7917-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="c7917-167">يجب أيضًا على المستخدم إكمال الحركات.</span><span class="sxs-lookup"><span data-stu-id="c7917-167">The user must also complete transactions.</span></span>

<span data-ttu-id="c7917-168">نظرا لأن ميزة *ضبط موضع لوحة الترخيص للموقع* تضيف معرفًا جديدًا لمواضع لوحات الترخيص في الموقع، يجب عليك أولا إنشاء بعض البيانات لدعم السيناريو.</span><span class="sxs-lookup"><span data-stu-id="c7917-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="c7917-169">الجرد الفوري للموقع الأول</span><span class="sxs-lookup"><span data-stu-id="c7917-169">Spot-count the first location</span></span>

1. <span data-ttu-id="c7917-170">افتح تطبيق المستودع للأجهزة المحمولة وسجل الدخول إلى المستودع *61*.</span><span class="sxs-lookup"><span data-stu-id="c7917-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="c7917-171">انتقل إلى **المخزون \> الجرد الفوري**.</span><span class="sxs-lookup"><span data-stu-id="c7917-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="c7917-172">في صفحة **الجرد الفوري**، قم بتعيين **حقل الموقع** إلى *01A01R1S1B*.</span><span class="sxs-lookup"><span data-stu-id="c7917-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="c7917-173">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7917-173">Select **OK**.</span></span>

    <span data-ttu-id="c7917-174">تعرض الصفحة الموقع الذي قمت بإدخاله.</span><span class="sxs-lookup"><span data-stu-id="c7917-174">The page shows the location that you entered.</span></span> <span data-ttu-id="c7917-175">وتوضح أيضًا الرسالة التالية: "اكتمل الموقع، إضافة لوحة ترخيص أو صنف جديد؟"</span><span class="sxs-lookup"><span data-stu-id="c7917-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="c7917-176">حدد **تحديث** لإضافة جرد في الموقع.</span><span class="sxs-lookup"><span data-stu-id="c7917-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="c7917-177">في صفحة **جرد دوري: إضافة لوحة ترخيص أو صنف جديد**، حدد حقل **الصنف** ثم أدخل القيمة *A0001*.</span><span class="sxs-lookup"><span data-stu-id="c7917-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="c7917-178">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7917-178">Select **OK**.</span></span>
1. <span data-ttu-id="c7917-179">في صفحة **جرد دوري: إضافة لوحة ترخيص أو صنف جديد**، حدد حقل **لوحة الترخيص**، ثم أدخل القيمة *LP1001* (أو أي رقم لوحة ترخيص أخرى من اختيارك).</span><span class="sxs-lookup"><span data-stu-id="c7917-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="c7917-180">تُظهر صفحة **جرد دوري: إضافة لوحة ترخيص أو صنف جديد** **موضع لوحة الترخيص 1**.</span><span class="sxs-lookup"><span data-stu-id="c7917-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="c7917-181">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7917-181">Select **OK**.</span></span>

    <span data-ttu-id="c7917-182">يجب الآن تحديد كمية الصنف التي تم جردها على لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="c7917-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="c7917-183">قم بتعيين حقل **الكمية** إلى *10*.</span><span class="sxs-lookup"><span data-stu-id="c7917-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="c7917-184">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7917-184">Select **OK**.</span></span>

    <span data-ttu-id="c7917-185">تعرض الصفحة الموقع الذي قمت بإدخاله.</span><span class="sxs-lookup"><span data-stu-id="c7917-185">The page shows the location that you entered.</span></span> <span data-ttu-id="c7917-186">وتوضح أيضًا الرسالة التالية: "اكتمل الموقع، إضافة لوحة ترخيص أو صنف جديد؟"</span><span class="sxs-lookup"><span data-stu-id="c7917-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="c7917-187">حدد **تحديث** لإضافة جرد آخر في الموقع.</span><span class="sxs-lookup"><span data-stu-id="c7917-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="c7917-188">في صفحة **جرد دوري: إضافة لوحة ترخيص أو صنف جديد**، حدد حقل **الصنف** ثم أدخل القيمة *A0002*.</span><span class="sxs-lookup"><span data-stu-id="c7917-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="c7917-189">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7917-189">Select **OK**.</span></span>
1. <span data-ttu-id="c7917-190">في صفحة **جرد دوري: إضافة لوحة ترخيص أو صنف جديد**، حدد حقل **لوحة الترخيص**، ثم أدخل القيمة *LP1002* (أو أي رقم لوحة ترخيص آخر من اختيارك، بشرط أن يختلف ذلك عن رقم لوحة الترخيص الذي قمت بتحديده سابقًا).</span><span class="sxs-lookup"><span data-stu-id="c7917-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="c7917-191">قم بتغيير موضع لوحة الترخيص بتعيين الحقل **موضع لوحة الترخيص** إلى *2*.</span><span class="sxs-lookup"><span data-stu-id="c7917-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="c7917-192">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7917-192">Select **OK**.</span></span>
1. <span data-ttu-id="c7917-193">حدد كمية الصنف التي يتم جردها في لوحة الترخيص من خلال تعيين حقل **الكمية** إلى *10*.</span><span class="sxs-lookup"><span data-stu-id="c7917-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="c7917-194">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7917-194">Select **OK**.</span></span>

    <span data-ttu-id="c7917-195">تعرض الصفحة الموقع الذي قمت بإدخاله.</span><span class="sxs-lookup"><span data-stu-id="c7917-195">The page shows the location that you entered.</span></span> <span data-ttu-id="c7917-196">وتوضح أيضًا الرسالة التالية: "اكتمل الموقع، إضافة لوحة ترخيص أو صنف جديد؟"</span><span class="sxs-lookup"><span data-stu-id="c7917-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="c7917-197">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7917-197">Select **OK**.</span></span>

<span data-ttu-id="c7917-198">العمل مكتمل الآن.</span><span class="sxs-lookup"><span data-stu-id="c7917-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="c7917-199">الجرد الفوري للموقع الثاني</span><span class="sxs-lookup"><span data-stu-id="c7917-199">Spot-count the second location</span></span>

1. <span data-ttu-id="c7917-200">في صفحة **الجرد الفوري**، قم بتعيين **حقل الموقع** إلى *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="c7917-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="c7917-201">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7917-201">Select **OK**.</span></span>

    <span data-ttu-id="c7917-202">تعرض الصفحة الموقع الذي قمت بإدخاله.</span><span class="sxs-lookup"><span data-stu-id="c7917-202">The page shows the location that you entered.</span></span> <span data-ttu-id="c7917-203">وتوضح أيضًا الرسالة التالية: "اكتمل الموقع، إضافة لوحة ترخيص أو صنف جديد؟"</span><span class="sxs-lookup"><span data-stu-id="c7917-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="c7917-204">حدد **تحديث** لإضافة جرد في الموقع.</span><span class="sxs-lookup"><span data-stu-id="c7917-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="c7917-205">في صفحة **جرد دوري: إضافة لوحة ترخيص أو صنف جديد**، حدد حقل **الصنف** ثم أدخل القيمة *A0002*.</span><span class="sxs-lookup"><span data-stu-id="c7917-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="c7917-206">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7917-206">Select **OK**.</span></span>
1. <span data-ttu-id="c7917-207">في صفحة **جرد دوري: إضافة لوحة ترخيص أو صنف جديد**، حدد حقل **لوحة الترخيص**، ثم أدخل القيمة *LP1003* (أو أي رقم لوحة ترخيص آخر من اختيارك، بشرط أن يختلف ذلك عن كلا من رقمي لوحة الترخيص اللذين حددتها في الإجراء السابق).</span><span class="sxs-lookup"><span data-stu-id="c7917-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="c7917-208">تُظهر صفحة **جرد دوري: إضافة لوحة ترخيص أو صنف جديد** **موضع لوحة الترخيص 1**.</span><span class="sxs-lookup"><span data-stu-id="c7917-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="c7917-209">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7917-209">Select **OK**.</span></span>
1. <span data-ttu-id="c7917-210">حدد كمية الصنف التي يتم جردها في لوحة الترخيص من خلال تعيين حقل **الكمية** إلى *10*.</span><span class="sxs-lookup"><span data-stu-id="c7917-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="c7917-211">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7917-211">Select **OK**.</span></span>

    <span data-ttu-id="c7917-212">تعرض الصفحة الموقع الذي قمت بإدخاله.</span><span class="sxs-lookup"><span data-stu-id="c7917-212">The page shows the location that you entered.</span></span> <span data-ttu-id="c7917-213">وتوضح أيضًا الرسالة التالية: "اكتمل الموقع، إضافة لوحة ترخيص أو صنف جديد؟"</span><span class="sxs-lookup"><span data-stu-id="c7917-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="c7917-214">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7917-214">Select **OK**.</span></span>

<span data-ttu-id="c7917-215">العمل مكتمل الآن.</span><span class="sxs-lookup"><span data-stu-id="c7917-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="c7917-216">تفاصيل العمل</span><span class="sxs-lookup"><span data-stu-id="c7917-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="c7917-217">الجرد الفوري من تطبيق الأجهزة المحمولة ينشئ عمل جرد دوري في Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c7917-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="c7917-218">ويتطلب العمل أن يتم قبول الجرد قبل ترحيله إلى المخزون.</span><span class="sxs-lookup"><span data-stu-id="c7917-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="c7917-219">سجل دخولك إلى Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c7917-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="c7917-220">انتقل إلى **إدارة المستودعات \> العمل \> تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="c7917-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="c7917-221">في علامة التبويب **نظرة عامة**، ابحث عن البنود التي لها القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c7917-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="c7917-222">**نوع أمر العمل:** *جرد دوري*</span><span class="sxs-lookup"><span data-stu-id="c7917-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="c7917-223">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="c7917-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="c7917-224">**حالة العمل:** *مراجعة معلقة*</span><span class="sxs-lookup"><span data-stu-id="c7917-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="c7917-225">ويجب أن يكون قد تم إنشاء معرفي عمل لهذه البنود.</span><span class="sxs-lookup"><span data-stu-id="c7917-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="c7917-226">يجب قبول الجرد لكل من معرفات العمل هذه.</span><span class="sxs-lookup"><span data-stu-id="c7917-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="c7917-227">في الشبكة، حدد أول معرف عمل لنوع أمر العمل *الجرد الدوري*.</span><span class="sxs-lookup"><span data-stu-id="c7917-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="c7917-228">في جزء الإجراءات، ضمن علامة التبويب **العمل**، في مجموعة **العمل**، حدد **جرد دوري**.</span><span class="sxs-lookup"><span data-stu-id="c7917-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="c7917-229">يتم عرض بندين، واحد لكل صنف ولوحة ترخيص.</span><span class="sxs-lookup"><span data-stu-id="c7917-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="c7917-230">يجب أن تتطابق القيم الموجودة في حقول **الكمية المجرودة** و **الموقع** و **لوحة الترخيص** و **الصنف** مع إدخالات الجرد التي قمت بإنشائها على الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="c7917-230">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="c7917-231">إذا لم يكن أي من هذه الحقول مرئيًا، فحدد **أبعاد العرض** في جزء الإجراءات لإضافتها إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="c7917-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="c7917-232">حدد كلا البندين.</span><span class="sxs-lookup"><span data-stu-id="c7917-232">Select both lines.</span></span>
1. <span data-ttu-id="c7917-233">في جزء الإجراءات، حدد **قبول الجرد**.</span><span class="sxs-lookup"><span data-stu-id="c7917-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="c7917-234">ستستلم رسالة "ترحيل - دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="c7917-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="c7917-235">حدد **تفاصيل الرسالة** لعرض رقم دفتر اليومية الذي تم ترحيله.</span><span class="sxs-lookup"><span data-stu-id="c7917-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="c7917-236">أغلق تفاصيل الرسالة.</span><span class="sxs-lookup"><span data-stu-id="c7917-236">Close the message details.</span></span>
1. <span data-ttu-id="c7917-237">قم بتحديث صفحة **العمل**.</span><span class="sxs-lookup"><span data-stu-id="c7917-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="c7917-238">تم إغلاق معرف العمل الأول ولم يعد ظاهرًا.</span><span class="sxs-lookup"><span data-stu-id="c7917-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="c7917-239">لعرض العمل المغلق، حدد خانة الاختيار **إظهار المغلق** أعلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="c7917-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="c7917-240">يمكنك الآن قبول العمل للوحة الترخيص في الموقع *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="c7917-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="c7917-241">في علامة التبويب **نظرة عامة**، حدد معرف العمل الثاني لنوع أمر العمل *الجرد الدوري*.</span><span class="sxs-lookup"><span data-stu-id="c7917-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="c7917-242">في جزء الإجراءات، ضمن علامة التبويب **العمل**، في مجموعة **العمل**، حدد **جرد دوري**.</span><span class="sxs-lookup"><span data-stu-id="c7917-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="c7917-243">يتم عرض بند واحد، للصنف ولوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="c7917-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="c7917-244">يجب أن تتطابق القيم الموجودة في حقول **الكمية المجرودة** و **الموقع** و **لوحة الترخيص** و **الصنف** مع إدخالات الجرد التي قمت بإنشائها على الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="c7917-244">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="c7917-245">حدد البند.</span><span class="sxs-lookup"><span data-stu-id="c7917-245">Select the line.</span></span>
1. <span data-ttu-id="c7917-246">في جزء الإجراءات، حدد **قبول الجرد**.</span><span class="sxs-lookup"><span data-stu-id="c7917-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="c7917-247">ستستلم رسالة "ترحيل - دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="c7917-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="c7917-248">حدد **تفاصيل الرسالة** لعرض رقم دفتر اليومية الذي تم ترحيله.</span><span class="sxs-lookup"><span data-stu-id="c7917-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="c7917-249">أغلق تفاصيل الرسالة.</span><span class="sxs-lookup"><span data-stu-id="c7917-249">Close the message details.</span></span>
1. <span data-ttu-id="c7917-250">قم بتحديث صفحة **العمل**.</span><span class="sxs-lookup"><span data-stu-id="c7917-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="c7917-251">تم إغلاق معرف العمل الثاني ولم يعد ظاهرًا.</span><span class="sxs-lookup"><span data-stu-id="c7917-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="c7917-252">لعرض العمل المغلق، حدد خانة الاختيار **إظهار المغلق** أعلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="c7917-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="c7917-253">الفعلي حسب الموقع</span><span class="sxs-lookup"><span data-stu-id="c7917-253">On-hand by location</span></span>

1. <span data-ttu-id="c7917-254">انتقل إلى **إدارة المستودعات‬ \> الاستعلامات والتقارير‬ \> الفعلي حسب الموقع‬**.</span><span class="sxs-lookup"><span data-stu-id="c7917-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="c7917-255">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c7917-255">Set the following values:</span></span>

    - <span data-ttu-id="c7917-256">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="c7917-256">**Site:** *6*</span></span>
    - <span data-ttu-id="c7917-257">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="c7917-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="c7917-258">**التحديث عبر المواقع:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="c7917-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="c7917-259">لاحظ أن الموقع *01A01R1S1B* يتضمن لوحتي ترخيص:</span><span class="sxs-lookup"><span data-stu-id="c7917-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="c7917-260">**A0001**، حيث يتم تعيين حقل **موضع لوحة الترخيص** إلى *1*</span><span class="sxs-lookup"><span data-stu-id="c7917-260">**A0001**, where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="c7917-261">**A0002**، حيث يتم تعيين حقل **موضع لوحة الترخيص** إلى *2*</span><span class="sxs-lookup"><span data-stu-id="c7917-261">**A0002**, where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="c7917-262">لاحظ أن الموقع *01A01R1S2B* يتضمن لوحة ترخيص واحدة:</span><span class="sxs-lookup"><span data-stu-id="c7917-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="c7917-263">**A0002**، حيث يتم تعيين حقل **موضع لوحة الترخيص** إلى *1*</span><span class="sxs-lookup"><span data-stu-id="c7917-263">**A0002**, where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="c7917-264">سيناريو أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="c7917-264">Sales order scenario</span></span>

<span data-ttu-id="c7917-265">والآن بعد إعداد ميزة *ضبط موضع لوحة الترخيص للموقع*، وتم تقسيم المخزون، يجب إنشاء أمر مبيعات لإنشاء عمل الانتقاء الذي سيقوم بتوجيه عامل المستودع لانتقاء الصنف *A0002* من موقع المخزون الذي يوجد به معرف البالتة في الموضع *1*.</span><span class="sxs-lookup"><span data-stu-id="c7917-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="c7917-266">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="c7917-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="c7917-267">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c7917-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c7917-268">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c7917-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c7917-269">**حساب العميل:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="c7917-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="c7917-270">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="c7917-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="c7917-271">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7917-271">Select **OK**.</span></span>
1. <span data-ttu-id="c7917-272">تتم إضافة بند جديد إلى الشبكة في علامة التبويب السريعة **بنود أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="c7917-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="c7917-273">في هذا البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="c7917-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="c7917-274">**رقم الصنف:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="c7917-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="c7917-275">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="c7917-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="c7917-276">في قائمة **المخزون** أعلى الشبكة، حدد **حجز**.</span><span class="sxs-lookup"><span data-stu-id="c7917-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="c7917-277">في صفحة **الحجز**، في جزء الإجراءات حدد **حجز لوط** لحجز المخزون لبند الأمر.</span><span class="sxs-lookup"><span data-stu-id="c7917-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="c7917-278">أغلق صفحة **الحجز**.</span><span class="sxs-lookup"><span data-stu-id="c7917-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="c7917-279">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، في مجموعة **الإجراءات**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="c7917-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="c7917-280">سوف تستلم رسالة معلوماتية تشير إلى معرف الموجة ومعرف الشحنة التي تم إنشاؤها لهذا الأمر.</span><span class="sxs-lookup"><span data-stu-id="c7917-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="c7917-281">في علامة التبويب السريعة **بنود أمر المبيعات**، في قائمة **المستودع** فوق الشبكة، حدد **تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="c7917-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="c7917-282">تظهر صفحة **العمل** وتظهر العمل الذي تم إنشاؤه لبند المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c7917-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="c7917-283">قم بتدوين معرف العمل الذي يظهر.</span><span class="sxs-lookup"><span data-stu-id="c7917-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="c7917-284">سيناريو انتقاء المبيعات</span><span class="sxs-lookup"><span data-stu-id="c7917-284">Sales picking scenario</span></span>

1. <span data-ttu-id="c7917-285">افتح تطبيق الأجهزة المحمولة وسجل الدخول إلى المستودع *61*.</span><span class="sxs-lookup"><span data-stu-id="c7917-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="c7917-286">انتقل إلى **الصادر \> انتقاء المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="c7917-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="c7917-287">في صفحة **مسح معرف العمل / معرف لوحة الترخيص**، حدد حقل **المعرف**، ثم أدخل معرف العمل من بند المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c7917-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="c7917-288">لاحظ أن عمل الانتقاء يوجك لانتقاء الصنف *A0002* من الموقع *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="c7917-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="c7917-289">تتلقي هذا التعليمات نظرا لأن الصنف *A0002* موجود على لوحة ترخيص في الموضع *1* في ذلك الموقع.</span><span class="sxs-lookup"><span data-stu-id="c7917-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="c7917-290">![الموضع 1](media/LocationLicensePlatePositioning.png "الموضع 1")</span><span class="sxs-lookup"><span data-stu-id="c7917-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="c7917-291">أدخل معرف لوحة الترخيص الذي قمت بإنشائه للموقع، ثم اتبع المطالبات لانتقاء أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c7917-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>
