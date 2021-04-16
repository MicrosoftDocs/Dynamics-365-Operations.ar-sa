---
title: طباعة تسمية الموجة
description: يصف هذا الموضوع طباعة بطاقة تسمية الموجة ويوضح كيفية اعدادها.
author: GarmMSFT
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: fe04b841dbb3bb237de53f74d73f2b3f9162ae6b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840427"
---
# <a name="wave-label-printing"></a><span data-ttu-id="10683-103">طباعة تسمية الموجة</span><span class="sxs-lookup"><span data-stu-id="10683-103">Wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10683-104">تقدم طباعة بطاقات التسمية الموجهة منهجًا بديلاً لتسمية الطباعة من خلال تقديم طريقة جديدة لخطوة الموجة تسمح لك بإنشاء التسميات وطباعتها مباشرة من قالب الموجة أثناء تنفيذ الموجة.</span><span class="sxs-lookup"><span data-stu-id="10683-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="10683-105">التالي، ستكون التسميات متاحة بالفعل قبل قيام العاملين بتشغيل طلب العمل علي جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="10683-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="10683-106">يمكن للعاملين بعد ذلك إرفاق التسميات المطلوبة اثناء الانتقاء بدلا من بعد الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="10683-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="10683-107">تستخدم طباعة بطاقة تسمية الموجات لغة برمجة Zebra Programming Language (ZPL) لإنشاء تخطيطات بطاقات التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="10683-108">ينقسم تخطيط التسمية إلى ثلاثة أقسام (الرأس والنص والتذييل) للسماح بالتسميات التي لها بنية متكررة.</span><span class="sxs-lookup"><span data-stu-id="10683-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="10683-109">تعرف قوالب التسمية الموجهة النظام على تخطيط التسمية المراد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="10683-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="10683-110">يمكن للمستخدمين تحديد الطابعة التي يتم استخدامها.</span><span class="sxs-lookup"><span data-stu-id="10683-110">Users can specify which printer is used.</span></span> <span data-ttu-id="10683-111">كما يمكنهم طباعة تسميات علي العديد من الطابعات في نفس الوقت، حسب احتياجهم.</span><span class="sxs-lookup"><span data-stu-id="10683-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="10683-112">تعرض صفحة **محفوظات تسميات الموجة** سجلاً بكافة التسميات التي تم إنشاؤها باستخدام هذا الاعداد.</span><span class="sxs-lookup"><span data-stu-id="10683-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="10683-113">يمكنك طباعة التسميات وترتيبها استنادا إلى رؤوس العمل، ويمكنك طباعة تسميات فواصل لكل رأس عمل، كما يمكنك طباعة تسميات محتوى الحاوية وتسميات الحالة وتسميات أخرى مشابهة.</span><span class="sxs-lookup"><span data-stu-id="10683-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="10683-114">لا تحل هذه الوظيفة محل وظيفة طباعة التسمية الموجودة والتي تستند إلى توجيه المستند.</span><span class="sxs-lookup"><span data-stu-id="10683-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="10683-115">تعرض طباعة بطاقة تسمية الموجة التحسينات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="10683-116">طباعة التسميات وفقًا لعدد علب الكارتون في سطر عمل واحد، بدون استخدام التعبئة في حاويات.</span><span class="sxs-lookup"><span data-stu-id="10683-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="10683-117">(تمثل "كارتون" وحدة يتم تعيينها على بنود مجموعة تسلسل الوحدات.)</span><span class="sxs-lookup"><span data-stu-id="10683-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="10683-118">طباعة العديد من تسلسلات التسميات المختلفة (علي سبيل المثال ، الكارتون وبطاقات البالتة).</span><span class="sxs-lookup"><span data-stu-id="10683-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="10683-119">تضمين تعداد التسميات (علي سبيل المثال، 1/124 ، 2/124 ،... 124/124)، وحدد نطاق التعداد (علي سبيل المثال، سطر العمل أو بند التحميل أو الشحنة).</span><span class="sxs-lookup"><span data-stu-id="10683-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="10683-120">إنشاء وطباعة معرف بوليصة الشحن على التسميات قبل إنشاء بوليصة الشحن.</span><span class="sxs-lookup"><span data-stu-id="10683-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="10683-121">إنشاء كود مسلسل لحاويه شحن (SSCC) فريد لكل علبة كارتون، وتضمينه في كل بطاقة تسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="10683-122">إنشاء تسلسلات رقمية متوافقة مع GS1 لمعرفات بوليصة الشحن وأكواد SSCC.</span><span class="sxs-lookup"><span data-stu-id="10683-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="10683-123">إعادة طباعة التسميات من كل من الأجهزة المحمولة والعميل الثري.</span><span class="sxs-lookup"><span data-stu-id="10683-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="10683-124">إلغاء التسميات (علي سبيل المثال، في سيناريوهات انتقاء قصيرة)، ثم إعاده طباعتها.</span><span class="sxs-lookup"><span data-stu-id="10683-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="10683-125">تنظيف محفوظات تسميات الموجات.</span><span class="sxs-lookup"><span data-stu-id="10683-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="10683-126">تتم مشاركة التحسينات الخاصة بتخطيطات توجيه المستندات بين تخطيطات توجيه المستندات وتخطيطات بطاقات عنونة الموجة.</span><span class="sxs-lookup"><span data-stu-id="10683-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="10683-127">(لمزيد من المعلومات، راجع [تخطيط توجيه المستند للوحات الترخيص](../warehousing/document-routing-layout-for-license-plates.md).)</span><span class="sxs-lookup"><span data-stu-id="10683-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="10683-128">وتجعل هذه التحسينات تنفيذ الخطوات أكثر فعالية لتسمية علب الكارتون قبل استخدام البالتة.</span><span class="sxs-lookup"><span data-stu-id="10683-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="10683-129">وهي تفيد على وجه الخصوص الشركات التي تقوم بالشحن إلى البائعين الكبيرين الذين يقومون بالتأكيد تلقائيًا على إيصالات الأوامر بمسح كل علبة كارتون بشكل منفصل.</span><span class="sxs-lookup"><span data-stu-id="10683-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="10683-130">يمكنك تنفيذ سيناريوهات التكوين الموضحة في هذا الموضوع إما بشكل منفصل أو بمجموعة، وفقًا لمتطلبات العمل الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="10683-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="10683-131">يمكنك تصميم العديد من قوالب بطاقات التسمية الموجهة التي تعمل بالتسلسل (كما هو موضح في السيناريو 3).</span><span class="sxs-lookup"><span data-stu-id="10683-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="10683-132">علي سبيل المثال، يمكنك استخدام السيناريو 1 لطباعة تسميات علب كارتون والسيناريو 2 لطباعة تسميات البالتات (إذا كانت البالتات في المخزون تختلف في الحجم والتركيب).</span><span class="sxs-lookup"><span data-stu-id="10683-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="10683-133">تشغيل ميزة طباعة بطاقة تسمية الموجة</span><span class="sxs-lookup"><span data-stu-id="10683-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="10683-134">قبل أن تتمكن من استخدام ميزة *طباعة بطاقة تسمية الموجة*، يجب تشغيلها في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="10683-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="10683-135">بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="10683-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="10683-136">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="10683-137">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="10683-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="10683-138">**اسم الميزة:** *طباعه تسمية الموجة*</span><span class="sxs-lookup"><span data-stu-id="10683-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="10683-139">السيناريو 1: تتم طباعة تسمية الموجة حيث يتم إنشاء تسمية واحدة للموجة</span><span class="sxs-lookup"><span data-stu-id="10683-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="10683-140">يوضح هذا السيناريو كيفية قيام إحدى الشركات بطباعة بطاقات الشحن لبائع تجزئة كبير يقوم بتأكيد إيصالات الشراء تلقائيا عن طريق مسح كل علبة كارتون بشكل منفصل.</span><span class="sxs-lookup"><span data-stu-id="10683-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="10683-141">يعرض هذا السيناريو تدفق نهاية إلى نهاية.</span><span class="sxs-lookup"><span data-stu-id="10683-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="10683-142">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="10683-142">Make demo data available</span></span>

<span data-ttu-id="10683-143">لاتباع هذا السيناريو، يجب تثبيت بيانات العرض التوضيحي، ويجب تحديد الكيان القانوني **USMF‎**.</span><span class="sxs-lookup"><span data-stu-id="10683-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="10683-144">تأكد من أن طريقة تسمية الموجة متاحة</span><span class="sxs-lookup"><span data-stu-id="10683-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="10683-145">قد تحتاج إلى إعادة إنشاء أساليب عملية الموجة لجعل أسلوب طباعة بطاقة تسمية الموجة متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="10683-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="10683-146">انتقل إلى **إدارة المستودعات \> إعداد \> الموجات \> أساليب عملي الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="10683-147">تأكد من وجود **waveLabelPrinting** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="10683-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="10683-148">إذا لم يكن موجودًا، فحدد **أساليب إعادة الإنشاء** في جزء الإجراءات لإضافته.</span><span class="sxs-lookup"><span data-stu-id="10683-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="10683-149">قم بتكوين قالب موجة.</span><span class="sxs-lookup"><span data-stu-id="10683-149">Configure a wave template</span></span>

<span data-ttu-id="10683-150">تتيح لك القوالب الموجهة ربط مثيلات معينة من أساليب الموجة إلى قالب التسمية الموجة المقابل.</span><span class="sxs-lookup"><span data-stu-id="10683-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="10683-151">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="10683-152">حدد قالب مثل **62 إعداد الشحن الافتراضي**.</span><span class="sxs-lookup"><span data-stu-id="10683-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="10683-153">في علامة التبويب السريعة **الأساليب**، قم بنقل طريقة **طباعة تسمية الموجة** إلى العمود **الأساليب المحددة**.</span><span class="sxs-lookup"><span data-stu-id="10683-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="10683-154">في الحقل **الأساليب المحددة**، حدد أسلوب **طباعة تسمية الموجة** وقم بتعيين حقل **كود خطوة الموجة** على *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="10683-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="10683-155">للحصول على مزيد من المعلومات حول أكواد خطوات الموجات، راجع [أكواد خطوات الموجات](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="10683-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="10683-156">إنشاء تخطيط لتسمية موجة</span><span class="sxs-lookup"><span data-stu-id="10683-156">Create a wave label layout</span></span>

<span data-ttu-id="10683-157">يتحكم تخطيط التسمية بالمعلومات التي تتم طباعتها علي التسمية وكيفية تخطيطها. هنا، تقوم بإدخال رمز ZPL الذي يتم إرساله إلى الطابعة.</span><span class="sxs-lookup"><span data-stu-id="10683-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="10683-158">انتقل إلى **إدارة المستودعات \> إعداد \> توجيه المستند \> تخطيطات تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="10683-159">انشئ سجلاً ينطوي على الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="10683-160">**معرف تخطيط التسمية:** *كارتون*</span><span class="sxs-lookup"><span data-stu-id="10683-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="10683-161">**الوصف:** *كارتون (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="10683-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="10683-162">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="10683-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="10683-163">في جزء الاجراء، حدد **إعدادات صف تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="10683-164">تظهر **الصفحة إعدادات صف التسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="10683-165">يمكنك هنا تكوين الجزء الديناميكي من التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="10683-166">أضف صفًا ينطوي على الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-167">**معرف الصف:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="10683-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="10683-168">**اسم جدول الصف:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="10683-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="10683-169">**موضع بدء الصف:** *0*</span><span class="sxs-lookup"><span data-stu-id="10683-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="10683-170">يحدد هذا الحقل الموضع العمودي الذي سيبدأ فيه الصف على التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="10683-171">**ارتفاع الصف:** *0*</span><span class="sxs-lookup"><span data-stu-id="10683-171">**Row height:** *0*</span></span>

        <span data-ttu-id="10683-172">يحدد هذا الحقل ارتفاع كل صف (بالنقاط) ، وفقًا لمعيار ZPL.</span><span class="sxs-lookup"><span data-stu-id="10683-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="10683-173">ويكون ارتفاع الصف موجبًا للتسميات الأفقية وسالبًا للتسميات العمودية.</span><span class="sxs-lookup"><span data-stu-id="10683-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="10683-174">نظرًا لوجود صف واحد فقط في هذا المثال ، يمكنك تعيين القيمة إلى *0* (صفر).</span><span class="sxs-lookup"><span data-stu-id="10683-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="10683-175">**الصفوف لكل صفحة:** *1*</span><span class="sxs-lookup"><span data-stu-id="10683-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="10683-176">يحدد هذا الحقل عدد الصفوف التي يمكن طباعتها علي كل تسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="10683-177">سيؤدي هذا الإعداد إلى طباعة تسمية ZPL منفصلة لكل سجل في جدول تسميات الموجات.</span><span class="sxs-lookup"><span data-stu-id="10683-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="10683-178">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="10683-178">Close the page.</span></span>
1. <span data-ttu-id="10683-179">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="10683-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="10683-180">في محرر الاستعلام، في علامة التبويب **نطاق**، أضف سطرًا بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-181">**الجدول:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-182">**الجدول المشتق:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-183">**الحقل:** *نوع العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="10683-184">**المعايير:** *انتقاء*</span><span class="sxs-lookup"><span data-stu-id="10683-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="10683-185">يضمن هذا الاستعلام أنه ستتم طباعة سطور العمل الخاصة بنوع الانتقاء فقط علي التسمية وليس في النوع الخاص بسطور العمل.</span><span class="sxs-lookup"><span data-stu-id="10683-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="10683-186">إذا كنت ترغب في أن تكون قادرًا على طباعة معرف بوليصة الشحن، في علامة التبويب **الصلات**، حدد جدول **بنود العمل**، وقم بضم جدول **الشحنات** إليه.</span><span class="sxs-lookup"><span data-stu-id="10683-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="10683-187">أغلق مربع حوار محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="10683-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="10683-188">تتضمن علامة التبويب السريعة **تخطيط نص الطابعة** ثلاثة مقاطع حيث يمكنك كتابة التعليمات البرمجية للطابعة: **مقطع رأس الصفحة** و **مقطع النص الأساسي** ومقطع **التذييل**.</span><span class="sxs-lookup"><span data-stu-id="10683-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="10683-189">في **مقطع الرأس**، في الحقل **رأس التسمية**، أدخل كود لرأس الصفحة المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="10683-190">علي سبيل المثال، إذا كنت تستخدم طابعات Zebra، يمكنك استخدام التعليمات البرمجية التالية.</span><span class="sxs-lookup"><span data-stu-id="10683-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="10683-191">في **مقطع النص الأساسي**، في الحقل **النص الأساسي للتسمية**، أدخل كود للنص الأساسي المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="10683-192">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="10683-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="10683-193">في مقطع **النص الأساسي**، في الحقل **تذييل التسمية**، أدخل كود للتذييل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="10683-194">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="10683-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="10683-195">سيقوم هذا الاعداد بطباعة نسخة واحدة من كل تسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="10683-196">إذا كنت بحاجة إلى نسخ إضافية (علي سبيل المثال، نسخة واحدة لكل جانب من البالتة) ، قم بتعيين القيمة **n** لمقطع **\^PQn** في تذييل الصفحة على عدد النسخ المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="10683-197">علي سبيل المثال، لطباعة أربع نسخ من كل تسمية، حدد **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="10683-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="10683-198">التسمية جاهزة الآن للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="10683-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="10683-199">إنشاء نوع لتسمية موجة</span><span class="sxs-lookup"><span data-stu-id="10683-199">Create a wave label type</span></span>

<span data-ttu-id="10683-200">يتم استخدام أنواع تسميات الموجات المستخدمة لربط قوالب تسميه الموجة بوحدة في بنود مجموعة تسلسل وحدة.</span><span class="sxs-lookup"><span data-stu-id="10683-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="10683-201">انتقل إلى **إدارة المستودعات \> إعداد \> توجيه المستند \> أنواع تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="10683-202">أضف نوع تسمية موجة يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="10683-203">**نوع التسمية:** *كارتون*</span><span class="sxs-lookup"><span data-stu-id="10683-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="10683-204">**الوصف:** *كارتون*</span><span class="sxs-lookup"><span data-stu-id="10683-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="10683-205">إعداد مجموعات تسلسل الوحدات</span><span class="sxs-lookup"><span data-stu-id="10683-205">Set up unit sequence groups</span></span>

<span data-ttu-id="10683-206">بعد ذلك، قم بإعداد مجموعة تسلسلات الوحدات لنوع تسمية الموجة.</span><span class="sxs-lookup"><span data-stu-id="10683-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="10683-207">انتقل إلى **إدارة المستودعات \> إعداد \> المستودع \> مجموعات تسلسل الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="10683-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="10683-208">حدد مجموعة **Ea Box PL**.</span><span class="sxs-lookup"><span data-stu-id="10683-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="10683-209">بالنسبة لبند **الصندوق**، قم بتعيين الحقل **نوع مستوى الموجة** إلى *كارتون*.</span><span class="sxs-lookup"><span data-stu-id="10683-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="10683-210">إنشاء قالب لتسمية موجة</span><span class="sxs-lookup"><span data-stu-id="10683-210">Create a wave label template</span></span>

<span data-ttu-id="10683-211">بعد ذلك، قم بإنشاء قالب تسمية الموجة لنوع تسمية الموجة.</span><span class="sxs-lookup"><span data-stu-id="10683-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="10683-212">انتقل إلى **إدارة المستودعات \> إعداد \> توجيه المستند \> قوالب تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="10683-213">أضف قالب مستوى الموجة، ثم قم بتعيين القيم التالية في الرأس:</span><span class="sxs-lookup"><span data-stu-id="10683-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="10683-214">**اسم قالب التسمية:** *تسميات كارتون*</span><span class="sxs-lookup"><span data-stu-id="10683-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="10683-215">**الوصف:** *تسميات كارتون*</span><span class="sxs-lookup"><span data-stu-id="10683-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="10683-216">**كود خطوة الموجة:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="10683-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="10683-217">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="10683-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="10683-218">على علامة التبويب السرعية **عام**، قم بتعيين حقل **نوع تسميه الموجة** إلى *كارتون*.</span><span class="sxs-lookup"><span data-stu-id="10683-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="10683-219">في علامة التبويب السريعة **تفاصيل قالب تسمية الموجة**، أضف صفًا جديدًا له الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="10683-220">**معرف تخطيط التسمية:** *كارتون*</span><span class="sxs-lookup"><span data-stu-id="10683-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="10683-221">**اسم الطابعة:** حدد طابعة ZPL مناسبة.</span><span class="sxs-lookup"><span data-stu-id="10683-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="10683-222">**تشغيل الاستعلام:** *نعم* (هذا الإعداد اختياري، ولكن ينصح به للحصول على الأداء الأمثل.)</span><span class="sxs-lookup"><span data-stu-id="10683-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="10683-223">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="10683-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="10683-224">اختياري: إذا كنت تقوم بإعداد تصميم تسمية خاص بالعميل، فيجب إنشاء استعلام للعثور على حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="10683-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="10683-225">على علامة التبويب السريعة **تفاصيل قالب تسمية الموجة**، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="10683-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="10683-226">بعد ذلك، في محرر الاستعلام، في علامة التبويب **نطاق**، أضف سطرًا بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-227">**الجدول:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="10683-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="10683-228">**الجدول المشتق:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="10683-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="10683-229">**الحقل:** *رقم الحساب*</span><span class="sxs-lookup"><span data-stu-id="10683-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="10683-230">**المعايير:** أدخل رقم حساب العميل ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="10683-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="10683-231">عند الانتهاء، حدد **موافق** لإغلاق مربع حوار محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="10683-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="10683-232">في جزء الإجراءات، حدد **تحرير الاستعلام** لفتح مربع حوار لتحرير الاستعلام لقالب التسمية بالكامل.</span><span class="sxs-lookup"><span data-stu-id="10683-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="10683-233">في مربع حوار محرر الاستعلام، في علامة التبويب **فرز**، أضف صفًا بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-234">**الجدول:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-235">**الجدول المشتق:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-236">**الحقل:** *معرف سطر تحميل المرجع (معرف السجل)*</span><span class="sxs-lookup"><span data-stu-id="10683-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="10683-237">**اتجاه البحث:** *تصاعدي*</span><span class="sxs-lookup"><span data-stu-id="10683-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="10683-238">حدد **موافق** لإغلاق مربع حوار محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="10683-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="10683-239">يطالبك مربع رسالة بتأكيد عملية إعادة تعيين التجميع.</span><span class="sxs-lookup"><span data-stu-id="10683-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="10683-240">للمتابعة، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="10683-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="10683-241">في جزء الإجراءات، حدد **مجموعة قوالب تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="10683-242">في مربع الحوار **مجموعة قوالب تسمية الموجة**، حدد الصف الذي تم فيه تعيين حقل **اسم الحقل المرجع** إلى *معرف بند التحميل المرجعي*، ثم حدد خانه الاختيار **تسمية معرف البنية** لهذا الصف.</span><span class="sxs-lookup"><span data-stu-id="10683-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id*, and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="10683-243">سيقوم هذا الإعداد بإنشاء تسلسل تسمية واحد ("كارتون 1 من X") لكل بند تحميل خلال الموجة، بغض النظر عن إعداد تجميع العمل.</span><span class="sxs-lookup"><span data-stu-id="10683-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="10683-244">يمكن طباعة تسلسل التسميات هذا في تخطيط التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="10683-245">تكوين ملحقات التسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="10683-245">Configure number sequence extensions</span></span>

<span data-ttu-id="10683-246">تتحكم ملحقات التسلسلات الرقمية في التوافق مع GS1 لتسلسلات رقمية معينة.</span><span class="sxs-lookup"><span data-stu-id="10683-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="10683-247">هذا التكوين اختياري للسيناريو الحالي.</span><span class="sxs-lookup"><span data-stu-id="10683-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="10683-248">لمزيد من المعلومات وتعليمات التكوين، راجع [تكوين ملحقات التسلسلات الرقمية](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="10683-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="10683-249">إنشاء أمر مبيعات وإصداره للمستودع</span><span class="sxs-lookup"><span data-stu-id="10683-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="10683-250">انتقل إلى **المبيعات والتسويق \> أمر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="10683-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="10683-251">قم بإنشاء أمر مبيعات يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="10683-252">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="10683-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="10683-253">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="10683-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="10683-254">قم بإضافة أمري مبيعات بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="10683-255">سطر أمر المبيعات 1:</span><span class="sxs-lookup"><span data-stu-id="10683-255">Sales order line 1:</span></span>

        - <span data-ttu-id="10683-256">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="10683-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="10683-257">**الكمية:** *9024*</span><span class="sxs-lookup"><span data-stu-id="10683-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="10683-258">**الوحدة:** *ea* (9024 Ea = 376 صندوق = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="10683-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="10683-259">سطر أمر المبيعات 2:</span><span class="sxs-lookup"><span data-stu-id="10683-259">Sales order line 2:</span></span>

        - <span data-ttu-id="10683-260">**رقم الصنف:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="10683-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="10683-261">**الكمية:** *9016*</span><span class="sxs-lookup"><span data-stu-id="10683-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="10683-262">**الوحدة:** *ea* (9016 Ea = 322 صندوق = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="10683-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="10683-263">الأصناف والكميات المتوفرة هنا هي أمثلة فقط.</span><span class="sxs-lookup"><span data-stu-id="10683-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="10683-264">ويجب أن يستخدم هؤلاء المستخدمين مجموعة تسلسل الوحدات التي قمت بتحديدها مسبقا، كما يجب تحديد تحويلات الوحدة المناسبة من *ea* إلى *صندوق* إلى *PL*، ويجب أن يكون لديهم مخزون في المستودع *62*.</span><span class="sxs-lookup"><span data-stu-id="10683-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="10683-265">لمزيد من المعلومات، راجع [وحدة القياس ونهج المخزون](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="10683-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="10683-266">حدد بند أمر المبيعات 1.</span><span class="sxs-lookup"><span data-stu-id="10683-266">Select sales order line 1.</span></span> <span data-ttu-id="10683-267">بعد ذلك، في قسم **بند أمر المبيعات**، في قائمة **المخزون**، حدد **الحجوزات**.</span><span class="sxs-lookup"><span data-stu-id="10683-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="10683-268">في صفحة **الحجز**، في جزء الإجراءات حدد **حجز لوط** وبعد ذلك أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="10683-268">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="10683-269">كرر الخطوتين 4 و5 لسطر أمر المبيعات 2.</span><span class="sxs-lookup"><span data-stu-id="10683-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="10683-270">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="10683-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="10683-271">تقع الأحداث التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-271">The following events occur:</span></span>

    - <span data-ttu-id="10683-272">يقوم النظام بمعالجة الشحنة التي تم إنشاؤها باستخدام القالب الذي يتضمن خطوة طباعة التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="10683-273">سيتم استخدام تخطيط التسمية لتحديد تنسيق التسمية، ستكون النتيجة تسمية تتم طباعتها على الطابعة المحددة في قالب التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="10683-274">يتم إنشاء تسميات الموجات وطباعتها.</span><span class="sxs-lookup"><span data-stu-id="10683-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="10683-275">سيساوي عدد التسميات عدد علب الكارتون (في هذا المثال، تسميات الصندوق 376 لتسميات الصناديق 1 و 322 للسطر 2).</span><span class="sxs-lookup"><span data-stu-id="10683-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="10683-276">يتم إنشاء معرف بوليصة شحن جديد للشحنات.</span><span class="sxs-lookup"><span data-stu-id="10683-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="10683-277">إذا قمت بتكوين ملحقات التسلسلات الرقمية، ستتبع معرفات تسمية الموجات تنسيق الأرقام **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="10683-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="10683-278">يمكنك عرض تسميات الموجات وإعادة طباعتها من الصفحات التالية.</span><span class="sxs-lookup"><span data-stu-id="10683-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="10683-279">في جزء الإجراءات بكل صفحة، في علامة التبويب **الشحنات**، في مجموعة **‏‫المعلومات ذات الصلة**، حدد **تسميات الموجات**.</span><span class="sxs-lookup"><span data-stu-id="10683-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="10683-280">كل الشحنات \> تفاصيل الشحنة</span><span class="sxs-lookup"><span data-stu-id="10683-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="10683-281">كل الحمولات \> تفاصيل الحِمل</span><span class="sxs-lookup"><span data-stu-id="10683-281">All loads \> Load details</span></span>
- <span data-ttu-id="10683-282">كافة الموجات</span><span class="sxs-lookup"><span data-stu-id="10683-282">All waves</span></span>
- <span data-ttu-id="10683-283">تسميات الموجة</span><span class="sxs-lookup"><span data-stu-id="10683-283">Wave labels</span></span>
- <span data-ttu-id="10683-284">محفوظات تسمية الموجة</span><span class="sxs-lookup"><span data-stu-id="10683-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="10683-285">السيناريو 2: طباعة تسمية الموجة للتعبئة (بدون سجلات تسميات موجات)</span><span class="sxs-lookup"><span data-stu-id="10683-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="10683-286">يتيح لك هذا السيناريو طباعة تسميات الموجات عند استخدام التعبئة لتقسيم العناصر تلقائيًا إلى علب كارتون ولذلك لا تتطلب سجل تسمية موجة.</span><span class="sxs-lookup"><span data-stu-id="10683-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="10683-287">وفي هذه الحالة، يعمل معرف الحاوية كعنصر نائب لـ SSCC.</span><span class="sxs-lookup"><span data-stu-id="10683-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="10683-288">وفيما يلي الاختلافات الأساسية بين هذا السيناريو والسيناريو 1:</span><span class="sxs-lookup"><span data-stu-id="10683-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="10683-289">**قوالب تسميه الموجه:** لن تقوم بتحديد نوع تسمية الموجة على قالب تسمية الموجة، ولن تحتاج إلى تجميع بنية تسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="10683-290">والا، سيتم تكوين قالب تسمية الموجة والارتباط بقالب الموجة بنفس الطريقة الموضحة في السيناريو 1.</span><span class="sxs-lookup"><span data-stu-id="10683-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="10683-291">يجب عليك ترك نوع تسمية الموجه فارغًا لمنع إنشاء تسميات الموجات.</span><span class="sxs-lookup"><span data-stu-id="10683-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="10683-292">**تخطيطات بطاقات العنونة الموجهة:** ستقوم بتكوين إعدادات صف تخطيط تسمية الموجة لأسطر العمل بدلاً من سجلات تسمية الموجة.</span><span class="sxs-lookup"><span data-stu-id="10683-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="10683-293">يجب تكوين إعداد الصف لتخطيط التسمية باستخدام الجدول **WHSWorkLine** بدلاً من الجدول **WHSWaveLabel**.</span><span class="sxs-lookup"><span data-stu-id="10683-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="10683-294">يتحكم الإعداد **الصفوف لكل صفحة** في عدد الصفوف التي سيحتوي عليها مقطع النص الأساسي.</span><span class="sxs-lookup"><span data-stu-id="10683-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="10683-295">كما يتناسب هذا التكوين مع سيناريوهات الأعمال التي يتم فيها تعبئة أصناف متعددة مختلفة في صندوق بتسمية أو في بالتة، ويمكن تحديد عملية التعبئة هذه بواسطة إنشاء العمل (على سبيل المثال، العمل الذي تم تجميعه حسب الشحنة).</span><span class="sxs-lookup"><span data-stu-id="10683-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="10683-296">يعرض هذا السيناريو تدفق نهاية إلى نهاية.</span><span class="sxs-lookup"><span data-stu-id="10683-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="10683-297">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="10683-297">Make demo data available</span></span>

<span data-ttu-id="10683-298">لاتباع هذا السيناريو، يجب تثبيت بيانات العرض التوضيحي، ويجب تحديد الكيان القانوني **USMF‎**.</span><span class="sxs-lookup"><span data-stu-id="10683-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="10683-299">تأكد من أن طريقة تسمية الموجة متاحة</span><span class="sxs-lookup"><span data-stu-id="10683-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="10683-300">قد تحتاج إلى إعادة إنشاء أساليب عملية الموجة لجعل أسلوب طباعة بطاقة تسمية الموجة متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="10683-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="10683-301">انتقل إلى **إدارة المستودعات \> إعداد \> الموجات \> أساليب عملي الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="10683-302">تأكد من وجود **waveLabelPrinting** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="10683-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="10683-303">إذا لم يكن موجودًا، فحدد **أساليب إعادة الإنشاء** في جزء الإجراءات لإضافته.</span><span class="sxs-lookup"><span data-stu-id="10683-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="10683-304">إعداد قالب موجة</span><span class="sxs-lookup"><span data-stu-id="10683-304">Set up a wave template</span></span>

<span data-ttu-id="10683-305">تتيح لك القوالب الموجهة ربط مثيلات معينة من أساليب الموجة إلى قالب التسمية الموجة المقابل.</span><span class="sxs-lookup"><span data-stu-id="10683-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="10683-306">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="10683-307">حدد قالب مثل **63 التعبئة**.</span><span class="sxs-lookup"><span data-stu-id="10683-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="10683-308">في علامة التبويب السريعة **الأساليب**، قم بنقل طريقة **طباعة تسمية الموجة** إلى العمود **الأساليب المحددة**.</span><span class="sxs-lookup"><span data-stu-id="10683-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="10683-309">في الحقل **الأساليب المحددة**، حدد أسلوب **طباعة تسمية الموجة** وقم بتعيين حقل **كود خطوة الموجة** على *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="10683-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="10683-310">للحصول على مزيد من المعلومات حول أكواد خطوات الموجات، راجع [أكواد خطوات الموجات](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="10683-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="10683-311">إنشاء تخطيط لتسمية موجة</span><span class="sxs-lookup"><span data-stu-id="10683-311">Create a wave label layout</span></span>

1. <span data-ttu-id="10683-312">انتقل إلى **إدارة المستودعات \> إعداد \> توجيه المستند \> تخطيطات تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="10683-313">انشئ سجلاً ينطوي على الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="10683-314">**معرف تخطيط التسمية:** *كارتون*</span><span class="sxs-lookup"><span data-stu-id="10683-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="10683-315">**الوصف:** *كارتون (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="10683-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="10683-316">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="10683-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="10683-317">في جزء الاجراء، حدد **إعدادات صف تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="10683-318">تظهر **الصفحة إعدادات صف التسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="10683-319">يمكنك هنا تكوين الجزء الديناميكي من التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="10683-320">أضف صفًا ينطوي على الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-321">**معرف الصف:** *WorkLine*</span><span class="sxs-lookup"><span data-stu-id="10683-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="10683-322">**اسم جدول الصف:** *WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="10683-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="10683-323">**موضع بدء الصف:** *500*</span><span class="sxs-lookup"><span data-stu-id="10683-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="10683-324">يحدد هذا الحقل الموضع العمودي الذي سيبدأ فيه الصف على التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="10683-325">**ارتفاع الصف:** *50*</span><span class="sxs-lookup"><span data-stu-id="10683-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="10683-326">يحدد هذا الحقل ارتفاع كل صف.</span><span class="sxs-lookup"><span data-stu-id="10683-326">This field defines the height of each row.</span></span> <span data-ttu-id="10683-327">ويكون ارتفاع الصف موجبًا للتسميات الأفقية وسالبًا للتسميات العمودية.</span><span class="sxs-lookup"><span data-stu-id="10683-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="10683-328">**الصفوف لكل صفحة:** *5*</span><span class="sxs-lookup"><span data-stu-id="10683-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="10683-329">يحدد هذا الحقل عدد الصفوف التي يمكن طباعتها علي كل تسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="10683-330">سيقوم هذا الإعداد بطباعة العديد من تسميات ZPL لكل عمل، حيث يمكن أن تحتوي كل صفحة على خمسة بنود عمل.</span><span class="sxs-lookup"><span data-stu-id="10683-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="10683-331">على سبيل المثال، إذا كانت التسمية مطبوعة للحاوية التي تحتوي على 12 بندًا، ستتم طباعة ثلاث تسميات.</span><span class="sxs-lookup"><span data-stu-id="10683-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="10683-332">إذا كنت ترغب في طباعة تسمية منفصلة لكل بند من بنود الانتقاء، قم بتعيين هذه القيمة على *1*.</span><span class="sxs-lookup"><span data-stu-id="10683-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="10683-333">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="10683-333">Close the page.</span></span>
1. <span data-ttu-id="10683-334">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="10683-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="10683-335">في محرر الاستعلام، في علامة التبويب **نطاق**، أضف سطرًا بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-336">**الجدول:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-337">**الجدول المشتق:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-338">**الحقل:** *نوع العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="10683-339">**المعايير:** *انتقاء*</span><span class="sxs-lookup"><span data-stu-id="10683-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="10683-340">إذا كنت ترغب في أن تكون قادرًا على طباعة معرف بوليصة الشحن، في علامة التبويب **الصلات**، حدد جدول **بنود العمل**، وقم بضم جدول **الشحنات** إليه.</span><span class="sxs-lookup"><span data-stu-id="10683-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="10683-341">أغلق مربع حوار محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="10683-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="10683-342">تتضمن علامة التبويب السريعة **تخطيط نص الطابعة** ثلاثة مقاطع حيث يمكنك كتابة التعليمات البرمجية للطابعة: **مقطع رأس الصفحة** و **مقطع النص الأساسي** ومقطع **التذييل**.</span><span class="sxs-lookup"><span data-stu-id="10683-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="10683-343">في **مقطع الرأس**، في الحقل **رأس التسمية**، أدخل كود لرأس الصفحة المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="10683-344">علي سبيل المثال، إذا كنت تستخدم طابعات Zebra، يمكنك استخدام التعليمات البرمجية التالية.</span><span class="sxs-lookup"><span data-stu-id="10683-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="10683-345">في **مقطع النص الأساسي**، في الحقل **النص الأساسي للتسمية**، أدخل كود للنص الأساسي المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="10683-346">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="10683-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="10683-347">في مقطع **النص الأساسي**، في الحقل **تذييل التسمية**، أدخل كود للتذييل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="10683-348">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="10683-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="10683-349">سيقوم هذا الاعداد بطباعة نسخة واحدة من كل تسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="10683-350">إذا كنت بحاجة إلى نسخ إضافية (علي سبيل المثال، نسخة واحدة لكل جانب من البالتة) ، قم بتعيين القيمة **n** لمقطع **\^PQn** في تذييل الصفحة على عدد النسخ المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="10683-351">علي سبيل المثال، لطباعة أربع نسخ من كل تسمية، حدد **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="10683-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="10683-352">التسمية جاهزة الآن للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="10683-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="10683-353">إنشاء قالب لتسمية موجة</span><span class="sxs-lookup"><span data-stu-id="10683-353">Create a wave label template</span></span>

1. <span data-ttu-id="10683-354">انتقل إلى **إدارة المستودعات \> إعداد \> توجيه المستند \> قوالب تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="10683-355">أضف قالب مستوى الموجة، ثم قم بتعيين القيم التالية في الرأس:</span><span class="sxs-lookup"><span data-stu-id="10683-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="10683-356">**اسم قالب التسمية:** *تسميات الحاوية*</span><span class="sxs-lookup"><span data-stu-id="10683-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="10683-357">**الوصف:** *تسميات الحاوية*</span><span class="sxs-lookup"><span data-stu-id="10683-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="10683-358">**كود خطوة الموجة:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="10683-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="10683-359">**المستودع:** *63*</span><span class="sxs-lookup"><span data-stu-id="10683-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="10683-360">في علامة التبويب السريعة **تفاصيل قالب تسمية الموجة**، أضف صفًا له الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-361">**معرف تخطيط التسمية:** *الحاوية*</span><span class="sxs-lookup"><span data-stu-id="10683-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="10683-362">**اسم الطابعة:** حدد طابعة ZPL مناسبة.</span><span class="sxs-lookup"><span data-stu-id="10683-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="10683-363">**تشغيل الاستعلام:** *نعم* (هذا الإعداد اختياري، ولكن ينصح به للحصول على الأداء الأمثل.)</span><span class="sxs-lookup"><span data-stu-id="10683-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="10683-364">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="10683-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="10683-365">اختياري: إذا كنت تقوم بإعداد تصميم تسمية خاص بالعميل، فيجب إنشاء استعلام للعثور على حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="10683-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="10683-366">على علامة التبويب السريعة **تفاصيل قالب تسمية الموجة**، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="10683-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="10683-367">بعد ذلك، في محرر الاستعلام، في علامة التبويب **نطاق**، أضف سطرًا بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-368">**الجدول:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="10683-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="10683-369">**الجدول المشتق:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="10683-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="10683-370">**الحقل:** *رقم الحساب*</span><span class="sxs-lookup"><span data-stu-id="10683-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="10683-371">**المعايير:** أدخل رقم حساب العميل ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="10683-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="10683-372">عند الانتهاء، حدد **موافق** لإغلاق مربع حوار محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="10683-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="10683-373">تكوين ملحقات التسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="10683-373">Configure number sequence extensions</span></span>

<span data-ttu-id="10683-374">تتحكم ملحقات التسلسلات الرقمية في التوافق مع GS1 لتسلسلات رقمية معينة.</span><span class="sxs-lookup"><span data-stu-id="10683-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="10683-375">هذا التكوين اختياري للسيناريو الحالي.</span><span class="sxs-lookup"><span data-stu-id="10683-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="10683-376">لمزيد من المعلومات وتعليمات التكوين، راجع [تكوين ملحقات التسلسلات الرقمية](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="10683-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="10683-377">إنشاء أمر مبيعات وإصداره للمستودع</span><span class="sxs-lookup"><span data-stu-id="10683-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="10683-378">انتقل إلى **المبيعات والتسويق \> أمر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="10683-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="10683-379">قم بإنشاء أمر مبيعات يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="10683-380">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="10683-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="10683-381">**المستودع:** *63*</span><span class="sxs-lookup"><span data-stu-id="10683-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="10683-382">إضافة خمسة بنود أمر مبيعات:</span><span class="sxs-lookup"><span data-stu-id="10683-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="10683-383">سطر أمر المبيعات 1:</span><span class="sxs-lookup"><span data-stu-id="10683-383">Sales order line 1:</span></span>

        - <span data-ttu-id="10683-384">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="10683-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="10683-385">**الكمية:** *10*</span><span class="sxs-lookup"><span data-stu-id="10683-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="10683-386">سطر أمر المبيعات 2:</span><span class="sxs-lookup"><span data-stu-id="10683-386">Sales order line 2:</span></span>

        - <span data-ttu-id="10683-387">**رقم الصنف:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="10683-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="10683-388">**الكمية:** *20*</span><span class="sxs-lookup"><span data-stu-id="10683-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="10683-389">سطر أمر المبيعات 3:</span><span class="sxs-lookup"><span data-stu-id="10683-389">Sales order line 3:</span></span>

        - <span data-ttu-id="10683-390">**رقم الصنف:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="10683-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="10683-391">**الكمية:** *20*</span><span class="sxs-lookup"><span data-stu-id="10683-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="10683-392">سطر أمر المبيعات 4:</span><span class="sxs-lookup"><span data-stu-id="10683-392">Sales order line 4:</span></span>

        - <span data-ttu-id="10683-393">**رقم الصنف:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="10683-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="10683-394">**الكمية:** *40*</span><span class="sxs-lookup"><span data-stu-id="10683-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="10683-395">سطر أمر المبيعات 5:</span><span class="sxs-lookup"><span data-stu-id="10683-395">Sales order line 5:</span></span>

        - <span data-ttu-id="10683-396">**رقم الصنف:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="10683-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="10683-397">**الكمية:** *50*</span><span class="sxs-lookup"><span data-stu-id="10683-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="10683-398">الأصناف والكميات المتوفرة هنا هي أمثلة فقط.</span><span class="sxs-lookup"><span data-stu-id="10683-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="10683-399">يجب أن يكون لديهم مخزون في المستودع المحدد.</span><span class="sxs-lookup"><span data-stu-id="10683-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="10683-400">حدد بند أمر المبيعات 1.</span><span class="sxs-lookup"><span data-stu-id="10683-400">Select sales order line 1.</span></span> <span data-ttu-id="10683-401">بعد ذلك، في قسم **بند أمر المبيعات**، في قائمة **المخزون**، حدد **الحجوزات**.</span><span class="sxs-lookup"><span data-stu-id="10683-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="10683-402">في صفحة **الحجز**، في جزء الإجراءات حدد **حجز لوط** وبعد ذلك أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="10683-402">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="10683-403">كرر الخطوتين 4 و5 لكل سطر أمر المبيعات إضافي.</span><span class="sxs-lookup"><span data-stu-id="10683-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="10683-404">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="10683-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="10683-405">تقع الأحداث التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-405">The following events occur:</span></span>

    - <span data-ttu-id="10683-406">يقوم النظام بمعالجة الشحنة التي تم إنشاؤها باستخدام القالب الذي يتضمن خطوة طباعة التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="10683-407">سيتم استخدام تخطيط التسمية لتحديد تنسيق التسمية، ستكون النتيجة تسمية تتضمن خمسة أسطر وتتم طباعتها على الطابعة المحددة في قالب التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="10683-408">يتم إنشاء معرف بوليصة شحن جديد للشحنات.</span><span class="sxs-lookup"><span data-stu-id="10683-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="10683-409">إذا قمت بتكوين ملحقات التسلسلات الرقمية، ستتبع معرفات تسمية الموجات تنسيق الأرقام **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="10683-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="10683-410">يمكنك إعادة طباعة تسميات الموجات هذه بالانتقال إلى **إدارة المستودعات\>استعلامات وبلاغات\>سجل تسميات الموجات**.</span><span class="sxs-lookup"><span data-stu-id="10683-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="10683-411">السيناريو 3: طباعة تسمية الموجة للتسميات متعددة المستويات</span><span class="sxs-lookup"><span data-stu-id="10683-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="10683-412">يوضح هذا السيناريو كيفية استخدام وظيفة طباعة بطاقات الموجة عندما تتطلب عمليات التخزين مستويات متعددة من بطاقات الشحن.</span><span class="sxs-lookup"><span data-stu-id="10683-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="10683-413">على سبيل المثال، قد تتم طباعة تسميات منفصلة لعلب الكارتون و البالتات، وقد يلزم طباعة تسمية الفصل القصير للحصول على شحنة كاملة.</span><span class="sxs-lookup"><span data-stu-id="10683-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="10683-414">تعد تسميات الفصل نوعًا منفصلاً من التسميات التي يمكن استخدامها كمقسم بين الحالات والحاويات، مثل التسميات لمعرف الشحنة والكود الشريطي، بحيث يمكن فرز التسميات بسهولة بعد طباعتها.</span><span class="sxs-lookup"><span data-stu-id="10683-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="10683-415">إن الفرق الرئيسي بين تكوين هذا السيناريو وتكوين السيناريو 1، بالإضافة إلى حقيقة أن التسميات الفاصلة قد تم تمكينها، حيث يجب ان تقترن أنواع التسميات المتعددة لعلامات الموجة بقوالب تسمية الموجة وبنود مجموعة تسلسل الوحدات.</span><span class="sxs-lookup"><span data-stu-id="10683-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="10683-416">لإنجاز هذا التكوين، قم بإعداد العناصر التالية لهذا السيناريو:</span><span class="sxs-lookup"><span data-stu-id="10683-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="10683-417">**أساليب معالجة الموجة**: ستقوم بوضع علامة "قابل للتكرار" على أسلوب تسمية الموجة، أضفه مرتين (أو أكثر) إلى قالب الموجة، وقم بتعيين رموز أخرى لخطوات الموجة.</span><span class="sxs-lookup"><span data-stu-id="10683-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="10683-418">**قوالب تسمية الموجة:** ستقوم بتكوين قوالب تسمية الموجة وربطها بقالب الموجة.</span><span class="sxs-lookup"><span data-stu-id="10683-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="10683-419">كل قالب تسميه موجة صوتية له نوع تسمية موجة خاص به.</span><span class="sxs-lookup"><span data-stu-id="10683-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="10683-420">**تخطيطات تسمية الموجة**: ستقوم بإنشاء تخطيطات تسميات موجة متعددة.</span><span class="sxs-lookup"><span data-stu-id="10683-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="10683-421">سيكون هناك تخطيط تسمية منفصل لكل "مستوى من التسميات"، سيكون هناك أيضًا تخطيط تسمية فاصل.</span><span class="sxs-lookup"><span data-stu-id="10683-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="10683-422">يعرض هذا السيناريو تدفق نهاية إلى نهاية.</span><span class="sxs-lookup"><span data-stu-id="10683-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="10683-423">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="10683-423">Make demo data available</span></span>

<span data-ttu-id="10683-424">لاتباع هذا السيناريو، يجب تثبيت بيانات العرض التوضيحي، ويجب تحديد الكيان القانوني **USMF‎**.</span><span class="sxs-lookup"><span data-stu-id="10683-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="10683-425">إعداد أسلوب معالجة الموجة</span><span class="sxs-lookup"><span data-stu-id="10683-425">Set up a wave process method</span></span>

1. <span data-ttu-id="10683-426">انتقل إلى **إدارة المستودعات \> إعداد \> الموجات \> أساليب عملي الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="10683-427">تأكد من وجود **waveLabelPrinting** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="10683-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="10683-428">إذا لم يكن موجودًا، فحدد **أساليب إعادة الإنشاء** في جزء الإجراءات لإضافته.</span><span class="sxs-lookup"><span data-stu-id="10683-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="10683-429">بالنسبة للأسلوب **waveLabelPrinting**، حدد خانة الاختيار **جعل الأسلوب قابل للتكرار**</span><span class="sxs-lookup"><span data-stu-id="10683-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="10683-430">إعداد قالب موجة</span><span class="sxs-lookup"><span data-stu-id="10683-430">Set up a wave template</span></span>

1. <span data-ttu-id="10683-431">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="10683-432">حدد قالب مثل **62 إعداد الشحن الافتراضي**.</span><span class="sxs-lookup"><span data-stu-id="10683-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="10683-433">في علامة التبويب السريعة **الأساليب**، قم بنقل طريقة **طباعة تسمية الموجة** إلى العمود **الأساليب المحددة**.</span><span class="sxs-lookup"><span data-stu-id="10683-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="10683-434">في العمود **الأساليب المحددة**، قم بتعيين قيمة **رمز خطوة الموجة**، مثل *كارتون*، إلى طريقة **طباعة بطاقات الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton*, to the **Wave label printing** method.</span></span> <span data-ttu-id="10683-435">للحصول على مزيد من المعلومات حول أكواد خطوات الموجات، راجع [أكواد خطوات الموجات](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="10683-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="10683-436">قم بنقل طريقة **طباعة تسمية الموجة** إلى العمود **الأساليب المحددة** مرة ثانية.</span><span class="sxs-lookup"><span data-stu-id="10683-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="10683-437">في العمود **الأساليب المحددة**، قم بتعيين قيمة **رمز خطوة الموجة** مختلفة، مثل *بالتة*، إلى طريقة **طباعة بطاقات الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet*, to the second **Wave label printing** method.</span></span> <span data-ttu-id="10683-438">للحصول على مزيد من المعلومات حول أكواد خطوات الموجات، راجع [أكواد خطوات الموجات](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="10683-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="10683-439">إنشاء تخطيطات لتسمية موجة</span><span class="sxs-lookup"><span data-stu-id="10683-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="10683-440">انتقل إلى **إدارة المستودعات \> إعداد \> توجيه المستند \> تخطيطات تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="10683-441">انشئ سجلاً ينطوي على الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="10683-442">**معرف تخطيط التسمية:** *كارتون*</span><span class="sxs-lookup"><span data-stu-id="10683-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="10683-443">**الوصف:** *كارتون (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="10683-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="10683-444">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="10683-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="10683-445">في جزء الاجراء، حدد **إعدادات صف تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="10683-446">تظهر **الصفحة إعدادات صف التسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="10683-447">يمكنك هنا تكوين الجزء الديناميكي من التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="10683-448">أضف صفًا ينطوي على الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-449">**معرف الصف:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="10683-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="10683-450">**اسم جدول الصف:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="10683-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="10683-451">**موضع بدء الصف:** *0*</span><span class="sxs-lookup"><span data-stu-id="10683-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="10683-452">يحدد هذا الحقل الموضع العمودي الذي سيبدأ فيه الصف على التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="10683-453">**ارتفاع الصف:** *0*</span><span class="sxs-lookup"><span data-stu-id="10683-453">**Row height:** *0*</span></span>

        <span data-ttu-id="10683-454">يحدد هذا الحقل ارتفاع كل صف (بالنقاط) ، وفقًا لمعيار ZPL.</span><span class="sxs-lookup"><span data-stu-id="10683-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="10683-455">ويكون ارتفاع الصف موجبًا للتسميات الأفقية وسالبًا للتسميات العمودية.</span><span class="sxs-lookup"><span data-stu-id="10683-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="10683-456">نظرًا لوجود صف واحد فقط في هذا المثال ، يمكنك تعيين القيمة إلى *0* (صفر).</span><span class="sxs-lookup"><span data-stu-id="10683-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="10683-457">**الصفوف لكل صفحة:** *1*</span><span class="sxs-lookup"><span data-stu-id="10683-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="10683-458">يحدد هذا الحقل عدد الصفوف التي يمكن طباعتها علي كل تسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="10683-459">سيؤدي هذا الإعداد إلى طباعة تسمية ZPL منفصلة لكل سجل في جدول تسميات الموجات.</span><span class="sxs-lookup"><span data-stu-id="10683-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="10683-460">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="10683-460">Close the page.</span></span>
1. <span data-ttu-id="10683-461">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="10683-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="10683-462">في محرر الاستعلام، في علامة التبويب **نطاق**، أضف سطرًا بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-463">**الجدول:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-464">**الجدول المشتق:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-465">**الحقل:** *نوع العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="10683-466">**المعايير:** *انتقاء*</span><span class="sxs-lookup"><span data-stu-id="10683-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="10683-467">يضمن هذا الاستعلام أنه ستتم طباعة سطور العمل الخاصة بنوع الانتقاء فقط علي التسمية وليس في النوع الخاص بسطور العمل.</span><span class="sxs-lookup"><span data-stu-id="10683-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="10683-468">إذا كنت ترغب في أن تكون قادرًا على طباعة معرف بوليصة الشحن، في علامة التبويب **الصلات**، حدد جدول **بنود العمل**، وقم بضم جدول **الشحنات** إليه.</span><span class="sxs-lookup"><span data-stu-id="10683-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="10683-469">أغلق مربع حوار محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="10683-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="10683-470">تتضمن علامة التبويب السريعة **تخطيط نص الطابعة** ثلاثة مقاطع حيث يمكنك كتابة التعليمات البرمجية للطابعة: **مقطع رأس الصفحة** و **مقطع النص الأساسي** ومقطع **التذييل**.</span><span class="sxs-lookup"><span data-stu-id="10683-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="10683-471">في **مقطع الرأس**، في الحقل **رأس التسمية**، أدخل كود لرأس الصفحة المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="10683-472">علي سبيل المثال، إذا كنت تستخدم طابعات Zebra، يمكنك استخدام التعليمات البرمجية التالية.</span><span class="sxs-lookup"><span data-stu-id="10683-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="10683-473">في **مقطع النص الأساسي**، في الحقل **النص الأساسي للتسمية**، أدخل كود للنص الأساسي المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="10683-474">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="10683-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="10683-475">في مقطع **النص الأساسي**، في الحقل **تذييل التسمية**، أدخل كود للتذييل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="10683-476">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="10683-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="10683-477">سيقوم هذا الاعداد بطباعة نسخة واحدة من كل تسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="10683-478">إذا كنت بحاجة إلى نسخ إضافية (علي سبيل المثال، نسخة واحدة لكل جانب من البالتة) ، قم بتعيين القيمة **n** لمقطع **\^PQn** في تذييل الصفحة على عدد النسخ المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="10683-479">علي سبيل المثال، لطباعة أربع نسخ من كل تسمية، حدد **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="10683-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="10683-480">التسمية الأولى جاهزة الآن للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="10683-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="10683-481">قم بإنشاء سجل تخطيط ثان يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="10683-482">**معرف تخطيط التسمية:** *بالتة*</span><span class="sxs-lookup"><span data-stu-id="10683-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="10683-483">**الوصف:** *البالتة*</span><span class="sxs-lookup"><span data-stu-id="10683-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="10683-484">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="10683-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="10683-485">في جزء الاجراء، حدد **إعدادات صف تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="10683-486">تظهر **الصفحة إعدادات صف التسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="10683-487">يمكنك هنا تكوين الجزء الديناميكي من التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="10683-488">أضف صفًا ينطوي على الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-489">**معرف الصف:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="10683-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="10683-490">**اسم جدول الصف:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="10683-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="10683-491">**موضع بدء الصف:** *0*</span><span class="sxs-lookup"><span data-stu-id="10683-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="10683-492">يحدد هذا الحقل الموضع العمودي الذي سيبدأ فيه الصف على التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="10683-493">**ارتفاع الصف:** *0*</span><span class="sxs-lookup"><span data-stu-id="10683-493">**Row height:** *0*</span></span>

        <span data-ttu-id="10683-494">يحدد هذا الحقل ارتفاع كل صف (بالنقاط) ، وفقًا لمعيار ZPL.</span><span class="sxs-lookup"><span data-stu-id="10683-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="10683-495">ويكون ارتفاع الصف موجبًا للتسميات الأفقية وسالبًا للتسميات العمودية.</span><span class="sxs-lookup"><span data-stu-id="10683-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="10683-496">نظرًا لوجود صف واحد فقط في هذا المثال ، يمكنك تعيين القيمة إلى *0* (صفر).</span><span class="sxs-lookup"><span data-stu-id="10683-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="10683-497">**الصفوف لكل صفحة:** *1*</span><span class="sxs-lookup"><span data-stu-id="10683-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="10683-498">يحدد هذا الحقل عدد الصفوف التي يمكن طباعتها علي كل تسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="10683-499">يؤدي هذا الإعداد إلى طباعة تسمية ZPL منفصلة لكل سجل في جدول تسميات الموجات.</span><span class="sxs-lookup"><span data-stu-id="10683-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="10683-500">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="10683-500">Close the page.</span></span>
1. <span data-ttu-id="10683-501">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="10683-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="10683-502">في محرر الاستعلام، في علامة التبويب **نطاق**، أضف سطرًا بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-503">**الجدول:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-504">**الجدول المشتق:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-505">**الحقل:** *نوع العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="10683-506">**المعايير:** *انتقاء*</span><span class="sxs-lookup"><span data-stu-id="10683-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="10683-507">يضمن هذا الاستعلام أنه ستتم طباعة سطور العمل الخاصة بنوع الانتقاء فقط علي التسمية وليس في النوع الخاص بسطور العمل.</span><span class="sxs-lookup"><span data-stu-id="10683-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="10683-508">إذا كنت ترغب في أن تكون قادرًا على طباعة معرف بوليصة الشحن، في علامة التبويب **الصلات**، حدد جدول **بنود العمل**، وقم بضم جدول **الشحنات** إليه.</span><span class="sxs-lookup"><span data-stu-id="10683-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="10683-509">أغلق مربع حوار محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="10683-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="10683-510">تتضمن علامة التبويب السريعة **تخطيط نص الطابعة** ثلاثة مقاطع حيث يمكنك كتابة التعليمات البرمجية للطابعة: **مقطع رأس الصفحة** و **مقطع النص الأساسي** ومقطع **التذييل**.</span><span class="sxs-lookup"><span data-stu-id="10683-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="10683-511">في **مقطع الرأس**، في الحقل **رأس التسمية**، أدخل كود لرأس الصفحة المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="10683-512">علي سبيل المثال، إذا كنت تستخدم طابعات Zebra، يمكنك استخدام التعليمات البرمجية التالية.</span><span class="sxs-lookup"><span data-stu-id="10683-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="10683-513">في **مقطع النص الأساسي**، في الحقل **النص الأساسي للتسمية**، أدخل كود للنص الأساسي المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="10683-514">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="10683-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="10683-515">في مقطع **النص الأساسي**، في الحقل **تذييل التسمية**، أدخل كود للتذييل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="10683-516">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="10683-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="10683-517">سيقوم هذا الاعداد بطباعة نسخة واحدة من كل تسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="10683-518">إذا كنت بحاجة إلى نسخ إضافية (علي سبيل المثال، نسخة واحدة لكل جانب من البالتة) ، قم بتعيين القيمة **n** لمقطع **\^PQn** في تذييل الصفحة على عدد النسخ المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="10683-519">علي سبيل المثال، لطباعة أربع نسخ من كل تسمية، حدد **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="10683-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="10683-520">التسمية الثانية جاهزة الآن للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="10683-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="10683-521">قم بإنشاء سجل تخطيط ثالث يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="10683-522">**معرف تخطيط التسمية:** *فاصل*</span><span class="sxs-lookup"><span data-stu-id="10683-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="10683-523">**الوصف:** *تسمية الفاصل*</span><span class="sxs-lookup"><span data-stu-id="10683-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="10683-524">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="10683-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="10683-525">تتضمن علامة التبويب السريعة **تخطيط نص الطابعة** ثلاثة مقاطع حيث يمكنك كتابة التعليمات البرمجية للطابعة: **مقطع رأس الصفحة** و **مقطع النص الأساسي** ومقطع **التذييل**.</span><span class="sxs-lookup"><span data-stu-id="10683-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="10683-526">في **مقطع الرأس**، في الحقل **رأس التسمية**، أدخل كود ZPL للرأس المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10683-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="10683-527">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="10683-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="10683-528">لا يوجد نص أساسي مطلوب هذه المرة.</span><span class="sxs-lookup"><span data-stu-id="10683-528">This time, no body is required.</span></span> <span data-ttu-id="10683-529">لذلك، قم فقط بإدخال النص المطلوب في المقطع **مقطع التذييل**.</span><span class="sxs-lookup"><span data-stu-id="10683-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="10683-530">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="10683-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="10683-531">التسمية الثالثة جاهزة الآن للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="10683-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="10683-532">هذه التسمية الثالثة هي تسمية فاصل والتي سيتم استخدامها كفاصل بين تسميتين.</span><span class="sxs-lookup"><span data-stu-id="10683-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="10683-533">إنشاء نوعين لتسمية موجة</span><span class="sxs-lookup"><span data-stu-id="10683-533">Create two wave label types</span></span>

1. <span data-ttu-id="10683-534">انتقل إلى **إدارة المستودعات \> إعداد \> توجيه المستند \> أنواع تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="10683-535">انشئ سجلاً ينطوي على الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="10683-536">**نوع التسمية:** *كارتون*</span><span class="sxs-lookup"><span data-stu-id="10683-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="10683-537">**الوصف:** *كارتون*</span><span class="sxs-lookup"><span data-stu-id="10683-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="10683-538">قم بإنشاء سجل ثان يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="10683-539">**نوع التسمية:** *البالتة*</span><span class="sxs-lookup"><span data-stu-id="10683-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="10683-540">**الوصف:** *البالتة*</span><span class="sxs-lookup"><span data-stu-id="10683-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="10683-541">إعداد مجموعات تسلسل الوحدات</span><span class="sxs-lookup"><span data-stu-id="10683-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="10683-542">انتقل إلى **إدارة المستودعات \> إعداد \> المستودع \> مجموعات تسلسل الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="10683-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="10683-543">حدد أو أنشئ مجموعة **Ea صندوق PL**.</span><span class="sxs-lookup"><span data-stu-id="10683-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="10683-544">بالنسبة لبند **الصندوق**، قم بتعيين الحقل **نوع مستوى الموجة** إلى *كارتون*.</span><span class="sxs-lookup"><span data-stu-id="10683-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="10683-545">بالنسبة لسطر **PL**، قم بتعيين الحقل **نوع مستوى الموجة** إلى *بالتة*.</span><span class="sxs-lookup"><span data-stu-id="10683-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="10683-546">إنشاء قوالب لتسمية موجة</span><span class="sxs-lookup"><span data-stu-id="10683-546">Create wave label templates</span></span>

1. <span data-ttu-id="10683-547">انتقل إلى **إدارة المستودعات \> إعداد \> توجيه المستند \> قوالب تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="10683-548">قم بإنشاء قالب تسمية يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="10683-549">**اسم قالب التسمية:** *تسميات كارتون*</span><span class="sxs-lookup"><span data-stu-id="10683-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="10683-550">**الوصف:** *تسميات كارتون*</span><span class="sxs-lookup"><span data-stu-id="10683-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="10683-551">**كود خطوة الموجة:** *كارتون*</span><span class="sxs-lookup"><span data-stu-id="10683-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="10683-552">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="10683-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="10683-553">في علامة التبويب السريعة **عام**، في حقل **نوع تسمية الموجة**، حدد قيمة مثل *‏‫كارتون‬*.</span><span class="sxs-lookup"><span data-stu-id="10683-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="10683-554">في علامة التبويب السريعة **تفاصيل قالب تسمية الموجة**، أضف صفًا له الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-555">**معرف تخطيط التسمية:** *كارتون*</span><span class="sxs-lookup"><span data-stu-id="10683-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="10683-556">**اسم الطابعة:** حدد طابعة ZPL مناسبة.</span><span class="sxs-lookup"><span data-stu-id="10683-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="10683-557">**تشغيل الاستعلام:** *نعم* (هذا الإعداد اختياري، ولكن ينصح به للحصول على الأداء الأمثل.)</span><span class="sxs-lookup"><span data-stu-id="10683-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="10683-558">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="10683-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="10683-559">اختياري: إذا كنت تقوم بإعداد تصميم تسمية خاص بالعميل، فيجب إنشاء استعلام للعثور على حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="10683-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="10683-560">على علامة التبويب السريعة **تفاصيل قالب تسمية الموجة**، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="10683-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="10683-561">بعد ذلك، في محرر الاستعلام، في علامة التبويب **نطاق**، أضف سطرًا بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-562">**الجدول:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="10683-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="10683-563">**الجدول المشتق:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="10683-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="10683-564">**الحقل:** *رقم الحساب*</span><span class="sxs-lookup"><span data-stu-id="10683-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="10683-565">**المعايير:** أدخل رقم حساب العميل ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="10683-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="10683-566">عند الانتهاء، حدد **موافق** لإغلاق مربع حوار محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="10683-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="10683-567">في جزء الإجراءات، حدد **تحرير الاستعلام** لفتح مربع حوار لتحرير الاستعلام لقالب التسمية بالكامل.</span><span class="sxs-lookup"><span data-stu-id="10683-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="10683-568">في مربع حوار محرر الاستعلام، في علامة التبويب **فرز**، أضف صفًا بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-569">**الجدول:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-570">**الجدول المشتق:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-571">**الحقل:** *معرف سطر تحميل المرجع (معرف السجل)*</span><span class="sxs-lookup"><span data-stu-id="10683-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="10683-572">**اتجاه البحث:** *تصاعدي*</span><span class="sxs-lookup"><span data-stu-id="10683-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="10683-573">أضف صفًا ثانيًا ينطوي على الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="10683-574">**الجدول:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-575">**الجدول المشتق:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-576">**الحقل:** *معرف الشحنة*</span><span class="sxs-lookup"><span data-stu-id="10683-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="10683-577">**اتجاه البحث:** *تصاعدي*</span><span class="sxs-lookup"><span data-stu-id="10683-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="10683-578">حدد **موافق** لإغلاق مربع حوار محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="10683-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="10683-579">يطالبك مربع رسالة بتأكيد عملية إعادة تعيين التجميع.</span><span class="sxs-lookup"><span data-stu-id="10683-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="10683-580">للمتابعة، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="10683-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="10683-581">في جزء الإجراءات، حدد **مجموعة قوالب تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="10683-582">في مربع الحوار **مجموعة قوالب تسميات الموجات**، للصف حيث تم تعيين حقل **اسم الحقل المرجعي** إلى *معرف الشحنة*، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="10683-583">**طباعة تسمية فاصل:** حدد خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="10683-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="10683-584">**معرف تخطيط التسمية:** حدد تسمية فاصل.</span><span class="sxs-lookup"><span data-stu-id="10683-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="10683-585">(على سبيل المثال، حدد تخطيط تسمية *فاصل* التي قمت بإنشائها سابقا في هذا السيناريو.)</span><span class="sxs-lookup"><span data-stu-id="10683-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="10683-586">**اسم الطابعة:** حدد الطابعة الخاصة بتسمية الفاصل.</span><span class="sxs-lookup"><span data-stu-id="10683-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="10683-587">(عادة، بالنسبة للغرض من تقسيم التسمية، يجب تحديد نفس الطابعة التي تم تحديدها في علامة التبويب السريعة **تفاصيل قالب تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="10683-588">ومع ذلك، فمن الممكن سيناريوهات أخرى.)</span><span class="sxs-lookup"><span data-stu-id="10683-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="10683-589">بالنسبة للصف الذي تم تعيين حقل **اسم الحقل المرجعي** فيه إلى *معرف بند تحميل المرجع*، حدد خانة الاختيار **معرف بنية التسمية**.</span><span class="sxs-lookup"><span data-stu-id="10683-589">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="10683-590">سيقوم هذا الإعداد بإنشاء تسلسل تسمية واحد ("كارتون 1 من X") لكل بند تحميل خلال الموجة، بغض النظر عن إعداد تجميع العمل.</span><span class="sxs-lookup"><span data-stu-id="10683-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="10683-591">يمكن طباعة تسلسل التسميات هذا في تخطيط التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="10683-592">بالإضافة إلى ذلك، سيتم فصل التسميات الخاصة بالشحنات المختلفة بتسمية الفاصل المحددة.</span><span class="sxs-lookup"><span data-stu-id="10683-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="10683-593">حدد **موافق** لإغلاق مربع الحوار **مجموعة قوالب تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="10683-594">قم بإنشاء قالب تسمية ثانٍ يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="10683-595">**اسم قالب التسمية:** *تسميات بالتة*</span><span class="sxs-lookup"><span data-stu-id="10683-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="10683-596">**الوصف:** *تسميات البالتة*</span><span class="sxs-lookup"><span data-stu-id="10683-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="10683-597">**كود خطوة الموجة:** *بالتة*</span><span class="sxs-lookup"><span data-stu-id="10683-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="10683-598">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="10683-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="10683-599">في علامة التبويب السريعة **عام**، في حقل **نوع تسمية الموجة**، حدد قيمة مثل *‏‫بالتة‬*.</span><span class="sxs-lookup"><span data-stu-id="10683-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="10683-600">في علامة التبويب السريعة **تفاصيل قالب تسمية الموجة**، أضف صفًا له الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-601">**معرف تخطيط التسمية:** *بالتة*</span><span class="sxs-lookup"><span data-stu-id="10683-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="10683-602">**اسم الطابعة:** حدد طابعة ZPL مناسبة.</span><span class="sxs-lookup"><span data-stu-id="10683-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="10683-603">**تشغيل الاستعلام:** *نعم* (هذا الإعداد اختياري، ولكن ينصح به للحصول على الأداء الأمثل.)</span><span class="sxs-lookup"><span data-stu-id="10683-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="10683-604">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="10683-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="10683-605">اختياري: إذا كنت تقوم بإعداد تصميم تسمية خاص بالعميل، فيجب إنشاء استعلام للعثور على حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="10683-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="10683-606">على علامة التبويب السريعة **تفاصيل قالب تسمية الموجة**، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="10683-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="10683-607">بعد ذلك، في محرر الاستعلام، في علامة التبويب **نطاق**، أضف سطرًا بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-608">**الجدول:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="10683-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="10683-609">**الجدول المشتق:** *الشحنات*</span><span class="sxs-lookup"><span data-stu-id="10683-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="10683-610">**الحقل:** *رقم الحساب*</span><span class="sxs-lookup"><span data-stu-id="10683-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="10683-611">**المعايير:** أدخل رقم حساب العميل ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="10683-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="10683-612">عند الانتهاء، حدد **موافق** لإغلاق مربع حوار محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="10683-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="10683-613">في جزء الإجراءات، حدد **تحرير الاستعلام** لفتح مربع حوار لتحرير الاستعلام لقالب التسمية بالكامل.</span><span class="sxs-lookup"><span data-stu-id="10683-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="10683-614">في مربع حوار محرر الاستعلام، في علامة التبويب **فرز**، أضف صفًا بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="10683-615">**الجدول:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-616">**الجدول المشتق:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-617">**الحقل:** *معرف سطر تحميل المرجع (معرف السجل)*</span><span class="sxs-lookup"><span data-stu-id="10683-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="10683-618">**اتجاه البحث:** *تصاعدي*</span><span class="sxs-lookup"><span data-stu-id="10683-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="10683-619">أضف صفًا ثانيًا ينطوي على الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="10683-620">**الجدول:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-621">**الجدول المشتق:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="10683-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="10683-622">**الحقل:** *معرف الشحنة*</span><span class="sxs-lookup"><span data-stu-id="10683-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="10683-623">**اتجاه البحث:** *تصاعدي*</span><span class="sxs-lookup"><span data-stu-id="10683-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="10683-624">حدد **موافق** لإغلاق مربع حوار محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="10683-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="10683-625">يطالبك مربع رسالة بتأكيد عملية إعادة تعيين التجميع.</span><span class="sxs-lookup"><span data-stu-id="10683-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="10683-626">للمتابعة، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="10683-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="10683-627">في جزء الإجراءات، حدد **مجموعة قوالب تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="10683-628">في مربع الحوار **مجموعة قوالب تسميات الموجات**، للصف حيث تم تعيين حقل **اسم الحقل المرجعي** إلى *معرف الشحنة*، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="10683-629">**طباعة تسمية فاصل:** حدد خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="10683-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="10683-630">**معرف تخطيط التسمية:** حدد تسمية فاصل.</span><span class="sxs-lookup"><span data-stu-id="10683-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="10683-631">(على سبيل المثال، حدد تخطيط تسمية *فاصل* التي قمت بإنشائها سابقا في هذا السيناريو.)</span><span class="sxs-lookup"><span data-stu-id="10683-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="10683-632">**اسم الطابعة:** حدد الطابعة الخاصة بتسمية الفاصل.</span><span class="sxs-lookup"><span data-stu-id="10683-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="10683-633">(عادة، بالنسبة للغرض من تقسيم التسمية، يجب تحديد نفس الطابعة التي تم تحديدها في علامة التبويب السريعة **تفاصيل قالب تسمية الموجة**.</span><span class="sxs-lookup"><span data-stu-id="10683-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="10683-634">ومع ذلك، فمن الممكن سيناريوهات أخرى.)</span><span class="sxs-lookup"><span data-stu-id="10683-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="10683-635">بالنسبة للصف الذي تم تعيين حقل **اسم الحقل المرجعي** فيه إلى *معرف بند تحميل المرجع*، حدد خانة الاختيار **معرف بنية التسمية**.</span><span class="sxs-lookup"><span data-stu-id="10683-635">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="10683-636">سيقوم هذا الإعداد بإنشاء تسلسل تسمية واحد ("كارتون 1 من X") لكل بند تحميل خلال الموجة، بغض النظر عن إعداد تجميع العمل.</span><span class="sxs-lookup"><span data-stu-id="10683-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="10683-637">يمكن طباعة تسلسل التسميات هذا في تخطيط التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="10683-638">بالإضافة إلى ذلك، سيتم فصل التسميات الخاصة بالشحنات المختلفة بتسمية الفاصل المحددة.</span><span class="sxs-lookup"><span data-stu-id="10683-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="10683-639">تكوين ملحقات التسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="10683-639">Configure number sequence extensions</span></span>

<span data-ttu-id="10683-640">تتحكم ملحقات التسلسلات الرقمية في التوافق مع GS1 لتسلسلات رقمية معينة.</span><span class="sxs-lookup"><span data-stu-id="10683-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="10683-641">هذا التكوين اختياري للسيناريو الحالي.</span><span class="sxs-lookup"><span data-stu-id="10683-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="10683-642">لمزيد من المعلومات وتعليمات التكوين، راجع [تكوين ملحقات التسلسلات الرقمية](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="10683-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="10683-643">إنشاء أمر مبيعات وإصداره للمستودع</span><span class="sxs-lookup"><span data-stu-id="10683-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="10683-644">انتقل إلى **المبيعات والتسويق \> أمر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="10683-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="10683-645">قم بإنشاء أمر مبيعات يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="10683-646">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="10683-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="10683-647">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="10683-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="10683-648">إضافة بندي أمر مبيعات:</span><span class="sxs-lookup"><span data-stu-id="10683-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="10683-649">سطر أمر المبيعات 1:</span><span class="sxs-lookup"><span data-stu-id="10683-649">Sales order line 1:</span></span>

        - <span data-ttu-id="10683-650">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="10683-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="10683-651">**الكمية:** *9024*</span><span class="sxs-lookup"><span data-stu-id="10683-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="10683-652">**الوحدة:** *ea* (9024 Ea = 376 صندوق = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="10683-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="10683-653">سطر أمر المبيعات 2:</span><span class="sxs-lookup"><span data-stu-id="10683-653">Sales order line 2:</span></span>

        - <span data-ttu-id="10683-654">**رقم الصنف:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="10683-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="10683-655">**الكمية:** *9016*</span><span class="sxs-lookup"><span data-stu-id="10683-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="10683-656">**الوحدة:** *ea* (9016 Ea = 322 صندوق = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="10683-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="10683-657">الأصناف والكميات المتوفرة هنا هي أمثلة فقط.</span><span class="sxs-lookup"><span data-stu-id="10683-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="10683-658">ويجب أن يستخدم هؤلاء المستخدمين مجموعة تسلسل الوحدات التي قمت بتحديدها مسبقا، كما يجب تحديد تحويلات الوحدة المناسبة من *ea* إلى *صندوق* إلى *PL*، ويجب أن يكون لديهم مخزون في المستودع *62*.</span><span class="sxs-lookup"><span data-stu-id="10683-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="10683-659">لمزيد من المعلومات، راجع [وحدة القياس ونهج المخزون](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="10683-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="10683-660">حدد بند أمر المبيعات 1.</span><span class="sxs-lookup"><span data-stu-id="10683-660">Select sales order line 1.</span></span> <span data-ttu-id="10683-661">بعد ذلك، في قسم **بند أمر المبيعات**، في قائمة **المخزون**، حدد **الحجوزات**.</span><span class="sxs-lookup"><span data-stu-id="10683-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="10683-662">في صفحة **الحجز**، في جزء الإجراءات حدد **حجز لوط** وبعد ذلك أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="10683-662">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="10683-663">كرر الخطوتين 4 و5 لسطر أمر المبيعات 2.</span><span class="sxs-lookup"><span data-stu-id="10683-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="10683-664">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="10683-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="10683-665">تقع الأحداث التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-665">The following events occur:</span></span> 

    - <span data-ttu-id="10683-666">يقوم النظام بمعالجة الشحنة التي تم إنشاؤها باستخدام القالب الذي يتضمن خطوة طباعة التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="10683-667">سيتم استخدام تخطيط التسمية لتحديد تنسيق التسمية، ستكون النتيجة تسمية تتم طباعتها على الطابعة المحددة في قالب التسمية.</span><span class="sxs-lookup"><span data-stu-id="10683-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="10683-668">يتم إنشاء تسميات الموجات وطباعتها.</span><span class="sxs-lookup"><span data-stu-id="10683-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="10683-669">وسوف يساوي عدد التسميات عدد علب الكارتون (في هذا المثال، تسميات المربع 376 لتسميات السطر 1، 322 المربعات لتسميات السطر 2، 47 PL 47 تسميات السطر 2، وتسميات الفواصل التي تحتوي علي معرف الشحنة).</span><span class="sxs-lookup"><span data-stu-id="10683-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="10683-670">يتم إنشاء معرف بوليصة شحن جديد للشحنات.</span><span class="sxs-lookup"><span data-stu-id="10683-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="10683-671">إذا قمت بتكوين ملحقات التسلسلات الرقمية، ستتبع معرفات تسمية الموجات تنسيق الأرقام **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="10683-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="10683-672">يمكنك عرض تسميات الموجات وإعادة طباعتها من الصفحات التالية:</span><span class="sxs-lookup"><span data-stu-id="10683-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="10683-673">كل الشحنات \> تفاصيل الشحنة</span><span class="sxs-lookup"><span data-stu-id="10683-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="10683-674">كل الحمولات \> تفاصيل الحِمل</span><span class="sxs-lookup"><span data-stu-id="10683-674">All loads \> Load details</span></span>
- <span data-ttu-id="10683-675">كافة الموجات</span><span class="sxs-lookup"><span data-stu-id="10683-675">All waves</span></span>
- <span data-ttu-id="10683-676">تسميات الموجة</span><span class="sxs-lookup"><span data-stu-id="10683-676">Wave labels</span></span>
- <span data-ttu-id="10683-677">محفوظات تسمية الموجة</span><span class="sxs-lookup"><span data-stu-id="10683-677">Wave label history</span></span>

<span data-ttu-id="10683-678">بالنسبة لمعظم هذه الصفحات، يمكنك العثور علي الوظيفة ذات الصلة وذلك بتحديد **تسميات الموجات** في مجموعة **المعلومات ذات الصلة** في علامة التبويب **الشحنات** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="10683-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10683-679">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="10683-679">Additional resources</span></span>

- [<span data-ttu-id="10683-680">إعادة طباعة تسميات الموجات وإلغاؤها</span><span class="sxs-lookup"><span data-stu-id="10683-680">Reprint and void wave labels</span></span>](reprint-and-void-wave-labels.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]