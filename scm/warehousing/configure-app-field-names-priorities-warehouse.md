---
title: "تكوين أسماء حقول حقول التطبيق في تطبيق التخزين"
description: "يوضح هذا الموضوع كيفية تحديد وتكوين أسماء حقول تطبيق المخزن والأولويات في Finance and Operations."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 55c77c5c41b83c6b9d3e04e1e0c6382f23831502
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---

# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="0a547-103">تكوين أسماء حقول حقول التطبيق في تطبيق التخزين</span><span class="sxs-lookup"><span data-stu-id="0a547-103">Configure app field names in Warehousing app</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0a547-104">يوضح هذا الموضوع كيفية تحديد وتكوين أسماء حقول تطبيق المخزن والأولويات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0a547-104">This topic describes how to define and configure warehouse app field names and priorities in Finance and Operations.</span></span> 

<span data-ttu-id="0a547-105">**ملاحظة:** ينطبق هذا الموضوع على الميزات في إدارة المخزن.</span><span class="sxs-lookup"><span data-stu-id="0a547-105">**Note:** This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="0a547-106">ولا ينطبق على الميزات في إدارة المخزون.</span><span class="sxs-lookup"><span data-stu-id="0a547-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="0a547-107">Finance and Operations - التخزين هو تطبيق يمكن استخدامه لتنفيذ مهام المخزن.</span><span class="sxs-lookup"><span data-stu-id="0a547-107">Finance and Operations - Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="0a547-108">يمكن تحديد وتكوين أسماء الحقول المستخدمة في التطبيق، فضلًا عن تكوين الأولوية التي ينبغي تعيين أسماء الحقول على أساسها.</span><span class="sxs-lookup"><span data-stu-id="0a547-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="0a547-109">يوضح هذا الموضوع كيفية تحديد وتكوين أسماء حقول تطبيق التخزين والأولويات هذه، وكيفية استخدامها في Finance and Operations - التخزين.</span><span class="sxs-lookup"><span data-stu-id="0a547-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Finance and Operations - Warehousing.</span></span> <span data-ttu-id="0a547-110">للحصول على معلومات مفصلة حول كيفية تكوين اتصال لـ Finance and Operations -التخزين، يُرجى الرجوع إلى البرنامج التعليمي [تثبيت وتكوين Finance and Operations- التخزين](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="0a547-110">For detailed information about how to configure the connection to Finance and Operations  - Warehousing, refer to the tutorial [Install and configure Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span></span>

<a name="configure-warehouse-app-field-names"></a><span data-ttu-id="0a547-111">تكوين أسماء حقول تطبيق المخزن</span><span class="sxs-lookup"><span data-stu-id="0a547-111">Configure warehouse app field names</span></span>
===================================

<span data-ttu-id="0a547-112">عند استخدام Finance and Operations - التخزين، على جهازك المحمول، يمكنك تكوين كيفية عرض بيانات التعريف على جهازك على صفحة **أسماء حقول تطبيق المخزن**.</span><span class="sxs-lookup"><span data-stu-id="0a547-112">When you use Finance and Operations - Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="0a547-113">في الشركة الجديدة، في تطبيق Finance and Operations، حدد **إنشاء إعداد افتراضي** لإنشاء كافة أسماء الحقول التي سيتم استخدامها في عمليات سير عمل تطبيق المخزن على الجهاز المحمول، ثم تعيين وضع الإدخال المفضل ونوع الإدخال الخاص بهذه العمليات.</span><span class="sxs-lookup"><span data-stu-id="0a547-113">In a new company in Finance and Operations, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="0a547-114">بعد إنشاء كافة أسماء الحقول، يمكنك تحديد خيارات الإدخال التالية.</span><span class="sxs-lookup"><span data-stu-id="0a547-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a547-115">الخيار</span><span class="sxs-lookup"><span data-stu-id="0a547-115">Option</span></span></th>
<th><span data-ttu-id="0a547-116">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="0a547-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a547-117">وضع الإدخال المفضل</span><span class="sxs-lookup"><span data-stu-id="0a547-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="0a547-118">يحدد هذا الخيار ما إذا كان الحقل الممسوح أو الحقل الذي يتم فيه قيد الإدخال يدويًا ينبغي عرضه لاسم الحقل المحدد.</span><span class="sxs-lookup"><span data-stu-id="0a547-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="0a547-119">ويُعد هذا أمرًا مفيدًا لتمييز الحقول اعتمادًا على إذا ما كانت الرموز الشريطية مستخدمة للحقل.</span><span class="sxs-lookup"><span data-stu-id="0a547-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="0a547-120"><strong>ملاحظة:</strong> لتعيين أسماء الحقول باستخدام وضع الإدخال المفضل على <strong>مسح</strong>، يمكنك إدخال المعلومات يدوياً إذا كان الرمز الشريطي غير قابل للقراءة أو تالف.</span><span class="sxs-lookup"><span data-stu-id="0a547-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a547-121">نوع الإدخال</span><span class="sxs-lookup"><span data-stu-id="0a547-121">Input type</span></span></td>
<td><span data-ttu-id="0a547-122">يحدد هذا الخيار ما هو نوع الإدخال الذي يتعين استخدامه لاسم الحقل المحدد.</span><span class="sxs-lookup"><span data-stu-id="0a547-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="0a547-123">والأربعة خيارات المتاحة هي:</span><span class="sxs-lookup"><span data-stu-id="0a547-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="0a547-124"><strong>تحديد</strong> - يحتوي على قائمة بالخيارات للاختيار من بينها.</span><span class="sxs-lookup"><span data-stu-id="0a547-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="0a547-125">يتعذر تحرير أسماء الحقول باستخدام هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="0a547-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="0a547-126"><strong>التاريخ</strong> - سوف تعرض أسماء الحقول المحددة كتاريخ تنسيق التاريخ مع التسمية.</span><span class="sxs-lookup"><span data-stu-id="0a547-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="0a547-127">وسوف يساعد هذا عمال المخزن على رؤية ما هو التنسيق اللازم لإدخال التاريخ.</span><span class="sxs-lookup"><span data-stu-id="0a547-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="0a547-128">يتعذر تحرير أسماء الحقول باستخدام هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="0a547-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="0a547-129"><strong>أبجدي</strong> - في حال تحديد هذا الخيار، سوف تستخدم لوحة مفاتيح الجهاز عند إدخال المعلومات يدويًا في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="0a547-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="0a547-130">يمكن تغيير استخدام لوحة المفاتيح بناءً على الجهاز المستخدم.</span><span class="sxs-lookup"><span data-stu-id="0a547-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="0a547-131"><strong>رقمي</strong> - يستخدم هذا الخيار لأسماء الحقول التي تستخدم الإدخال الرقمي فقط، يمكنك تحديد هذا الخيار لعرض لوحة المفاتيح الرقمية المخصصة مع حقل الإدخال بدلًا من لوحة مفاتيح الجهاز.</span><span class="sxs-lookup"><span data-stu-id="0a547-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="0a547-132">تكوين أولوية حقل تطبيق المخزن</span><span class="sxs-lookup"><span data-stu-id="0a547-132">Configure warehouse app field priority</span></span>
======================================

<span data-ttu-id="0a547-133">على صفحة **أولوية حقل تطبيق المخزن**، يمكنك وضع أسماء الحقول في مجموعات مختلفة الأولوية.</span><span class="sxs-lookup"><span data-stu-id="0a547-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="0a547-134">وسوف يمكنك هذا من تحديد ما هي المعلومات التي ينبغي عرضها على صفحة المهام الرئيسية عندما يؤدي عمال المخزن مهامهم باستخدام التطبيق.</span><span class="sxs-lookup"><span data-stu-id="0a547-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="0a547-135">إذا قمت بالنقر فوق **إنشاء إعداد افتراضي**، فسوف يتم إنشاء مجموعة افتراضية من مجموعات الأولوية.</span><span class="sxs-lookup"><span data-stu-id="0a547-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="0a547-136">ويمكنك إنشاء العديد من مجموعات الأولويات بحسب الحاجة، ولكن سوف تظهر ثلاث مجموعات أولوية فقط على صفحة المهمة.</span><span class="sxs-lookup"><span data-stu-id="0a547-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="0a547-137">عندما يرسل Finance and Operations بيانات التعريف إلى التطبيق، فسوف يقوم بتعيين أولوية الحقل النسبية بناءً على مجموعة الأولوية الخاصة به، وسوف يعرض التطبيق مجموعات الأولوية الثلاث الواردة في بيانات التعريف على صفحة المهمة.</span><span class="sxs-lookup"><span data-stu-id="0a547-137">When Finance and Operations sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="0a547-138">وسوف يتم عرض بقية بيانات التعريف الزائدة على صفحة تفاصيل ثانوية.</span><span class="sxs-lookup"><span data-stu-id="0a547-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="0a547-139">يعرض الجدول التالي مثالًا على مجموعات الأولوية الخمس.</span><span class="sxs-lookup"><span data-stu-id="0a547-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a547-140">مجموعة الأولوية</span><span class="sxs-lookup"><span data-stu-id="0a547-140">Priority group</span></span></th>
<th><span data-ttu-id="0a547-141">الحقول المعيِّنة</span><span class="sxs-lookup"><span data-stu-id="0a547-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="0a547-142">الأولوية 10</span><span class="sxs-lookup"><span data-stu-id="0a547-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="0a547-143">الصنف</span><span class="sxs-lookup"><span data-stu-id="0a547-143">Item</span></span></li>
<li><span data-ttu-id="0a547-144">الكمية</span><span class="sxs-lookup"><span data-stu-id="0a547-144">Quantity</span></span></li>
<li><span data-ttu-id="0a547-145">وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="0a547-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="0a547-146">الأولوية 20</span><span class="sxs-lookup"><span data-stu-id="0a547-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="0a547-147">منصب نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="0a547-147">Cluster position</span></span></li>
<li><span data-ttu-id="0a547-148">مجموعة</span><span class="sxs-lookup"><span data-stu-id="0a547-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="0a547-149">الأولوية 30</span><span class="sxs-lookup"><span data-stu-id="0a547-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="0a547-150">وصف الصنف</span><span class="sxs-lookup"><span data-stu-id="0a547-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="0a547-151">الأولوية 40</span><span class="sxs-lookup"><span data-stu-id="0a547-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="0a547-152">التكوين</span><span class="sxs-lookup"><span data-stu-id="0a547-152">Configuration</span></span></li>
<li><span data-ttu-id="0a547-153">اللون</span><span class="sxs-lookup"><span data-stu-id="0a547-153">Color</span></span></li>
<li><span data-ttu-id="0a547-154">الحجم</span><span class="sxs-lookup"><span data-stu-id="0a547-154">Size</span></span></li>
<li><span data-ttu-id="0a547-155">نمط</span><span class="sxs-lookup"><span data-stu-id="0a547-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="0a547-156">الأولوية 50</span><span class="sxs-lookup"><span data-stu-id="0a547-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="0a547-157"> الموق</span><span class="sxs-lookup"><span data-stu-id="0a547-157">Location</span></span></li>
<li><span data-ttu-id="0a547-158">لوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="0a547-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0a547-159">على سبيل المثال، عندما يقوم أحد عمال المخزن بتنفيذ مهمة على جهاز محمول، إذا كانت بيانات التعريف التي سيتم عرضها في التطبيق تتكون من الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="0a547-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="0a547-160">الصنف</span><span class="sxs-lookup"><span data-stu-id="0a547-160">Item</span></span>
-   <span data-ttu-id="0a547-161">الكمية</span><span class="sxs-lookup"><span data-stu-id="0a547-161">Quantity</span></span>
-   <span data-ttu-id="0a547-162">وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="0a547-162">Unit of measure</span></span>
-   <span data-ttu-id="0a547-163">وصف الصنف</span><span class="sxs-lookup"><span data-stu-id="0a547-163">Item description</span></span>
-   <span data-ttu-id="0a547-164">الحجم والموقع</span><span class="sxs-lookup"><span data-stu-id="0a547-164">Size and Location</span></span>

<span data-ttu-id="0a547-165">بناءً على إعداد أولوية حقل تطبيق المخزن في الجدول أعلاه، فسوف يتم عرض صفوف المعلومات الثلاثة التالية على صفحة المهمة:</span><span class="sxs-lookup"><span data-stu-id="0a547-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="0a547-166">الصف الأول: الصنف والكمية ووحدة القياس</span><span class="sxs-lookup"><span data-stu-id="0a547-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="0a547-167">الصف 2: وصف الصنف</span><span class="sxs-lookup"><span data-stu-id="0a547-167">Row 2: Item description</span></span>
-   <span data-ttu-id="0a547-168">صف 3: الحجم</span><span class="sxs-lookup"><span data-stu-id="0a547-168">Row 3: Size</span></span>

<span data-ttu-id="0a547-169">لن يتم عرض بيانات التعريف المتبقية، الموقع على سبيل المثال، على صفحة المهمة، ولكن سيتم عرضها على صفحة التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="0a547-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="0a547-170">لمزيد من المعلومات ومشاهدة أمثلة من واجهة المستخدم، راجع منشور مدونة [الإعلان عن Finance and Operations - التخزين](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="0a547-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="see-also"></a><span data-ttu-id="0a547-171">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="0a547-171">See also</span></span>
--------

[<span data-ttu-id="0a547-172">تثبيت وتكوين Microsoft Dynamics 365 for Finance and Operations – التخزين</span><span class="sxs-lookup"><span data-stu-id="0a547-172">Install and configure Microsoft Dynamics 365 for Finance and Operations – Warehousing</span></span>](install-configure-warehousing-app.md)




