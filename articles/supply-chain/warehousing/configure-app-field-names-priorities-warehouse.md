---
title: تكوين الحقول لتطبيق إدارة المستودع للأجهزة المحمولة
description: يصف هذا الموضوع كيفية تحديد أسماء وأولويات الحقول المعروضة في تطبيق إدارة المستودع للأجهزة المحمولة وتكوينها.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6ed726536085b836f4014c59ea8df4755577ab5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808812"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="2a1bb-103">تكوين الحقول لتطبيق إدارة المستودع للأجهزة المحمولة</span><span class="sxs-lookup"><span data-stu-id="2a1bb-103">Configure fields for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a1bb-104">يصف هذا الموضوع كيفية تحديد أسماء وأولويات الحقول المعروضة في تطبيق إدارة المستودع للأجهزة المحمولة وتكوينها.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-104">This topic describes how to define and configure names and priorities of fields shown in the Warehouse Management mobile app.</span></span>

> [!NOTE]
> <span data-ttu-id="2a1bb-105">ينطبق هذا الموضوع على الميزات في إدارة المخزن.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="2a1bb-106">ولا ينطبق على الميزات في إدارة المخزون.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="2a1bb-107">تطبيق إدارة المستودع للأجهزة المحمولة هو تطبيق يمكن استخدامه لتنفيذ مهام المستودع.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-107">The Warehouse Management mobile app is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="2a1bb-108">يمكن تحديد وتكوين أسماء الحقول المستخدمة في التطبيق، فضلًا عن تكوين الأولوية التي ينبغي تعيين أسماء الحقول على أساسها.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="2a1bb-109">يوضح هذا الموضوع كيفية تحديد وتكوين أسماء حقول تطبيق إدارة المستودع للأجهزة المحمولة والأولويات هذه، وكيفية استخدامها في تطبيق التخزين.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-109">This topic explains how to define and configure these Warehouse Management mobile app field names and priorities, and how they are used.</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="2a1bb-110">تكوين أسماء حقول تطبيق المخزن</span><span class="sxs-lookup"><span data-stu-id="2a1bb-110">Configure warehouse app field names</span></span>

<span data-ttu-id="2a1bb-111">عند استخدام تطبيق التخزين، على جهازك المحمول، يمكنك تكوين كيفية عرض بيانات التعريف على جهازك على صفحة **أسماء حقول تطبيق المخزن**.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-111">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="2a1bb-112">في الشركة الجديدة، حدد **إنشاء إعداد افتراضي** لإنشاء كافة أسماء الحقول التي سيتم استخدامها في عمليات سير عمل تطبيق المستودع على الجهاز المحمول، ثم تعيين وضع الإدخال المفضل ونوع الإدخال الخاص بهذه العمليات.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-112">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="2a1bb-113">بعد إنشاء كافة أسماء الحقول، يمكنك تحديد خيارات الإدخال التالية.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-113">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a1bb-114">الخيار</span><span class="sxs-lookup"><span data-stu-id="2a1bb-114">Option</span></span></th>
<th><span data-ttu-id="2a1bb-115">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="2a1bb-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a1bb-116">وضع الإدخال المفضل</span><span class="sxs-lookup"><span data-stu-id="2a1bb-116">Preferred input mode</span></span></td>
<td><span data-ttu-id="2a1bb-117">يحدد هذا الخيار ما إذا كان الحقل الممسوح أو الحقل الذي يتم فيه قيد الإدخال يدويًا ينبغي عرضه لاسم الحقل المحدد.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-117">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="2a1bb-118">ويُعد هذا أمرًا مفيدًا لتمييز الحقول اعتمادًا على إذا ما كانت الرموز الشريطية مستخدمة للحقل.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-118">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="2a1bb-119"><strong>ملاحظة:</strong> لتعيين أسماء الحقول باستخدام وضع الإدخال المفضل على <strong>مسح</strong>، يمكنك إدخال المعلومات يدوياً إذا كان الرمز الشريطي غير قابل للقراءة أو تالف.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-119"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a1bb-120">نوع الإدخال</span><span class="sxs-lookup"><span data-stu-id="2a1bb-120">Input type</span></span></td>
<td><span data-ttu-id="2a1bb-121">يحدد هذا الخيار ما هو نوع الإدخال الذي يتعين استخدامه لاسم الحقل المحدد.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-121">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="2a1bb-122">والأربعة خيارات المتاحة هي:</span><span class="sxs-lookup"><span data-stu-id="2a1bb-122">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="2a1bb-123"><strong>التحديد</strong> - يحتوي على قائمة بالخيارات للاختيار من بينها.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-123"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="2a1bb-124">يتعذر تحرير أسماء الحقول باستخدام هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-124">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="2a1bb-125"><strong>التاريخ</strong> - سوف تعرض أسماء الحقول المحددة كتاريخ تنسيق التاريخ مع التسمية.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-125"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="2a1bb-126">وسوف يساعد هذا عمال المخزن على رؤية ما هو التنسيق اللازم لإدخال التاريخ.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-126">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="2a1bb-127">يتعذر تحرير أسماء الحقول باستخدام هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-127">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="2a1bb-128"><strong>أبجدي</strong> - في حال تحديد هذا الخيار، سيتم استخدام لوحة مفاتيح الجهاز عند إدخال المعلومات يدويًا في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-128"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="2a1bb-129">يمكن تغيير استخدام لوحة المفاتيح بناءً على الجهاز المستخدم.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-129">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="2a1bb-130"><strong>رقمي</strong> - يستخدم هذا الخيار لأسماء الحقول التي تستخدم الإدخال الرقمي فقط، يمكنك تحديد هذا الخيار لعرض لوحة المفاتيح الرقمية المخصصة مع حقل الإدخال بدلًا من لوحة مفاتيح الجهاز.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-130"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="2a1bb-131">تكوين أولوية حقل تطبيق المخزن</span><span class="sxs-lookup"><span data-stu-id="2a1bb-131">Configure warehouse app field priority</span></span>

<span data-ttu-id="2a1bb-132">على صفحة **أولوية حقل تطبيق المخزن**، يمكنك وضع أسماء الحقول في مجموعات مختلفة الأولوية.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-132">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="2a1bb-133">وسوف يمكنك هذا من تحديد ما هي المعلومات التي ينبغي عرضها على صفحة المهام الرئيسية عندما يؤدي عمال المخزن مهامهم باستخدام التطبيق.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-133">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="2a1bb-134">إذا قمت بالنقر فوق **إنشاء إعداد افتراضي**، فسوف يتم إنشاء مجموعة افتراضية من مجموعات الأولوية.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-134">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="2a1bb-135">ويمكنك إنشاء العديد من مجموعات الأولويات بحسب الحاجة، ولكن سوف تظهر ثلاث مجموعات أولوية فقط على صفحة المهمة.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-135">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="2a1bb-136">عندما يرسل النظام بيانات التعريف إلى التطبيق، فسوف يقوم بتعيين أولوية الحقل النسبية بناءً على مجموعة الأولوية الخاصة به، وسوف يعرض التطبيق مجموعات الأولوية الثلاث الواردة في بيانات التعريف على صفحة المهمة.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-136">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="2a1bb-137">وسوف يتم عرض بقية بيانات التعريف الزائدة على صفحة تفاصيل ثانوية.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-137">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="2a1bb-138">يعرض الجدول التالي مثالًا على مجموعات الأولوية الخمس.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-138">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a1bb-139">مجموعة الأولوية</span><span class="sxs-lookup"><span data-stu-id="2a1bb-139">Priority group</span></span></th>
<th><span data-ttu-id="2a1bb-140">الحقول المعيِّنة</span><span class="sxs-lookup"><span data-stu-id="2a1bb-140">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="2a1bb-141">الأولوية 10</span><span class="sxs-lookup"><span data-stu-id="2a1bb-141">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="2a1bb-142">الصنف</span><span class="sxs-lookup"><span data-stu-id="2a1bb-142">Item</span></span></li>
<li><span data-ttu-id="2a1bb-143">الكمية</span><span class="sxs-lookup"><span data-stu-id="2a1bb-143">Quantity</span></span></li>
<li><span data-ttu-id="2a1bb-144">وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="2a1bb-144">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="2a1bb-145">الأولوية 20</span><span class="sxs-lookup"><span data-stu-id="2a1bb-145">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="2a1bb-146">منصب نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="2a1bb-146">Cluster position</span></span></li>
<li><span data-ttu-id="2a1bb-147">مجموعة</span><span class="sxs-lookup"><span data-stu-id="2a1bb-147">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="2a1bb-148">الأولوية 30</span><span class="sxs-lookup"><span data-stu-id="2a1bb-148">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="2a1bb-149">وصف الصنف</span><span class="sxs-lookup"><span data-stu-id="2a1bb-149">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="2a1bb-150">الأولوية 40</span><span class="sxs-lookup"><span data-stu-id="2a1bb-150">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="2a1bb-151">التكوين</span><span class="sxs-lookup"><span data-stu-id="2a1bb-151">Configuration</span></span></li>
<li><span data-ttu-id="2a1bb-152">اللون</span><span class="sxs-lookup"><span data-stu-id="2a1bb-152">Color</span></span></li>
<li><span data-ttu-id="2a1bb-153">الحجم</span><span class="sxs-lookup"><span data-stu-id="2a1bb-153">Size</span></span></li>
<li><span data-ttu-id="2a1bb-154">نمط</span><span class="sxs-lookup"><span data-stu-id="2a1bb-154">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="2a1bb-155">الأولوية 50</span><span class="sxs-lookup"><span data-stu-id="2a1bb-155">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="2a1bb-156"> الموق</span><span class="sxs-lookup"><span data-stu-id="2a1bb-156">Location</span></span></li>
<li><span data-ttu-id="2a1bb-157">لوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="2a1bb-157">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2a1bb-158">على سبيل المثال، عندما يقوم أحد عمال المخزن بتنفيذ مهمة على جهاز محمول، إذا كانت بيانات التعريف التي سيتم عرضها في التطبيق تتكون من الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="2a1bb-158">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="2a1bb-159">الصنف</span><span class="sxs-lookup"><span data-stu-id="2a1bb-159">Item</span></span>
-   <span data-ttu-id="2a1bb-160">الكمية</span><span class="sxs-lookup"><span data-stu-id="2a1bb-160">Quantity</span></span>
-   <span data-ttu-id="2a1bb-161">وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="2a1bb-161">Unit of measure</span></span>
-   <span data-ttu-id="2a1bb-162">وصف الصنف</span><span class="sxs-lookup"><span data-stu-id="2a1bb-162">Item description</span></span>
-   <span data-ttu-id="2a1bb-163">الحجم والموقع</span><span class="sxs-lookup"><span data-stu-id="2a1bb-163">Size and Location</span></span>

<span data-ttu-id="2a1bb-164">بناءً على إعداد أولوية حقل تطبيق المخزن في الجدول أعلاه، فسوف يتم عرض صفوف المعلومات الثلاثة التالية على صفحة المهمة:</span><span class="sxs-lookup"><span data-stu-id="2a1bb-164">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="2a1bb-165">الصف الأول: الصنف والكمية ووحدة القياس</span><span class="sxs-lookup"><span data-stu-id="2a1bb-165">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="2a1bb-166">الصف 2: وصف الصنف</span><span class="sxs-lookup"><span data-stu-id="2a1bb-166">Row 2: Item description</span></span>
-   <span data-ttu-id="2a1bb-167">صف 3: الحجم</span><span class="sxs-lookup"><span data-stu-id="2a1bb-167">Row 3: Size</span></span>

<span data-ttu-id="2a1bb-168">لن يتم عرض بيانات التعريف المتبقية، الموقع على سبيل المثال، على صفحة المهمة، ولكن سيتم عرضها على صفحة التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="2a1bb-168">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="2a1bb-169">لمزيد من المعلومات ومشاهدة أمثلة من واجهة المستخدم، راجع منشور المدونة [الإعلان عن Finance and Operations - التخزين](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="2a1bb-169">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="2a1bb-170">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2a1bb-170">Additional resources</span></span>
--------

[<span data-ttu-id="2a1bb-171">تثبيت تطبيق إدارة المستودع للأجهزة المحمولة والاتصال به</span><span class="sxs-lookup"><span data-stu-id="2a1bb-171">Install and connect the Warehouse Management mobile app</span></span>](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]