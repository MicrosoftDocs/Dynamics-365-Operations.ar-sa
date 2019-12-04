---
title: تكوين أسماء حقول حقول التطبيق في تطبيق التخزين
description: يوضح هذا الموضوع كيفية تحديد وتكوين أسماء حقول تطبيق المستودع والأولويات في Dynamics 365 Supply Chain Management.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 11f6c96cc07c63d2c0c6a94385916b3396a77ed5
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814963"
---
# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="4bb55-103">تكوين أسماء حقول حقول التطبيق في تطبيق التخزين</span><span class="sxs-lookup"><span data-stu-id="4bb55-103">Configure app field names in Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4bb55-104">يوضح هذا الموضوع كيفية تحديد وتكوين أسماء حقول تطبيق المستودع والأولويات في Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4bb55-104">This topic describes how to define and configure warehouse app field names and priorities in Dynamics 365 Supply Chain Management.</span></span> 

> [!NOTE]
> <span data-ttu-id="4bb55-105">ينطبق هذا الموضوع على الميزات في إدارة المخزن.</span><span class="sxs-lookup"><span data-stu-id="4bb55-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="4bb55-106">ولا ينطبق على الميزات في إدارة المخزون.</span><span class="sxs-lookup"><span data-stu-id="4bb55-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="4bb55-107">التخزين هو تطبيق يمكن استخدامه لتنفيذ مهام المستودع.</span><span class="sxs-lookup"><span data-stu-id="4bb55-107">Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="4bb55-108">يمكن تحديد وتكوين أسماء الحقول المستخدمة في التطبيق، فضلًا عن تكوين الأولوية التي ينبغي تعيين أسماء الحقول على أساسها.</span><span class="sxs-lookup"><span data-stu-id="4bb55-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="4bb55-109">يوضح هذا الموضوع كيفية تحديد وتكوين أسماء حقول تطبيق التخزين والأولويات هذه، وكيفية استخدامها في تطبيق التخزين.</span><span class="sxs-lookup"><span data-stu-id="4bb55-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Warehousing.</span></span> <span data-ttu-id="4bb55-110">للحصول على معلومات مفصلة حول كيفية تكوين اتصال بتطبيق التخزين، يُرجى الرجوع إلى البرنامج التعليمي [نظرة عامة على تثبيت وتكوين تطبيق التخزين](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="4bb55-110">For detailed information about how to configure the connection to FWarehousing, refer to the tutorial [Install and configure the Warehousing app overview](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="4bb55-111">تكوين أسماء حقول تطبيق المخزن</span><span class="sxs-lookup"><span data-stu-id="4bb55-111">Configure warehouse app field names</span></span>

<span data-ttu-id="4bb55-112">عند استخدام تطبيق التخزين، على جهازك المحمول، يمكنك تكوين كيفية عرض بيانات التعريف على جهازك على صفحة **أسماء حقول تطبيق المخزن**.</span><span class="sxs-lookup"><span data-stu-id="4bb55-112">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="4bb55-113">في الشركة الجديدة، حدد **إنشاء إعداد افتراضي** لإنشاء كافة أسماء الحقول التي سيتم استخدامها في عمليات سير عمل تطبيق المستودع على الجهاز المحمول، ثم تعيين وضع الإدخال المفضل ونوع الإدخال الخاص بهذه العمليات.</span><span class="sxs-lookup"><span data-stu-id="4bb55-113">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="4bb55-114">بعد إنشاء كافة أسماء الحقول، يمكنك تحديد خيارات الإدخال التالية.</span><span class="sxs-lookup"><span data-stu-id="4bb55-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4bb55-115">الخيار</span><span class="sxs-lookup"><span data-stu-id="4bb55-115">Option</span></span></th>
<th><span data-ttu-id="4bb55-116">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="4bb55-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4bb55-117">وضع الإدخال المفضل</span><span class="sxs-lookup"><span data-stu-id="4bb55-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="4bb55-118">يحدد هذا الخيار ما إذا كان الحقل الممسوح أو الحقل الذي يتم فيه قيد الإدخال يدويًا ينبغي عرضه لاسم الحقل المحدد.</span><span class="sxs-lookup"><span data-stu-id="4bb55-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="4bb55-119">ويُعد هذا أمرًا مفيدًا لتمييز الحقول اعتمادًا على إذا ما كانت الرموز الشريطية مستخدمة للحقل.</span><span class="sxs-lookup"><span data-stu-id="4bb55-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="4bb55-120"><strong>ملاحظة:</strong> لتعيين أسماء الحقول باستخدام وضع الإدخال المفضل على <strong>مسح</strong>، يمكنك إدخال المعلومات يدوياً إذا كان الرمز الشريطي غير قابل للقراءة أو تالف.</span><span class="sxs-lookup"><span data-stu-id="4bb55-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bb55-121">نوع الإدخال</span><span class="sxs-lookup"><span data-stu-id="4bb55-121">Input type</span></span></td>
<td><span data-ttu-id="4bb55-122">يحدد هذا الخيار ما هو نوع الإدخال الذي يتعين استخدامه لاسم الحقل المحدد.</span><span class="sxs-lookup"><span data-stu-id="4bb55-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="4bb55-123">والأربعة خيارات المتاحة هي:</span><span class="sxs-lookup"><span data-stu-id="4bb55-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="4bb55-124"><strong>التحديد</strong> - يحتوي على قائمة بالخيارات للاختيار من بينها.</span><span class="sxs-lookup"><span data-stu-id="4bb55-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="4bb55-125">يتعذر تحرير أسماء الحقول باستخدام هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="4bb55-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="4bb55-126"><strong>التاريخ</strong> - سوف تعرض أسماء الحقول المحددة كتاريخ تنسيق التاريخ مع التسمية.</span><span class="sxs-lookup"><span data-stu-id="4bb55-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="4bb55-127">وسوف يساعد هذا عمال المخزن على رؤية ما هو التنسيق اللازم لإدخال التاريخ.</span><span class="sxs-lookup"><span data-stu-id="4bb55-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="4bb55-128">يتعذر تحرير أسماء الحقول باستخدام هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="4bb55-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="4bb55-129"><strong>أبجدي</strong> - في حال تحديد هذا الخيار، سيتم استخدام لوحة مفاتيح الجهاز عند إدخال المعلومات يدويًا في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="4bb55-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="4bb55-130">يمكن تغيير استخدام لوحة المفاتيح بناءً على الجهاز المستخدم.</span><span class="sxs-lookup"><span data-stu-id="4bb55-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="4bb55-131"><strong>رقمي</strong> - يستخدم هذا الخيار لأسماء الحقول التي تستخدم الإدخال الرقمي فقط، يمكنك تحديد هذا الخيار لعرض لوحة المفاتيح الرقمية المخصصة مع حقل الإدخال بدلًا من لوحة مفاتيح الجهاز.</span><span class="sxs-lookup"><span data-stu-id="4bb55-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="4bb55-132">تكوين أولوية حقل تطبيق المخزن</span><span class="sxs-lookup"><span data-stu-id="4bb55-132">Configure warehouse app field priority</span></span>

<span data-ttu-id="4bb55-133">على صفحة **أولوية حقل تطبيق المخزن**، يمكنك وضع أسماء الحقول في مجموعات مختلفة الأولوية.</span><span class="sxs-lookup"><span data-stu-id="4bb55-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="4bb55-134">وسوف يمكنك هذا من تحديد ما هي المعلومات التي ينبغي عرضها على صفحة المهام الرئيسية عندما يؤدي عمال المخزن مهامهم باستخدام التطبيق.</span><span class="sxs-lookup"><span data-stu-id="4bb55-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="4bb55-135">إذا قمت بالنقر فوق **إنشاء إعداد افتراضي**، فسوف يتم إنشاء مجموعة افتراضية من مجموعات الأولوية.</span><span class="sxs-lookup"><span data-stu-id="4bb55-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="4bb55-136">ويمكنك إنشاء العديد من مجموعات الأولويات بحسب الحاجة، ولكن سوف تظهر ثلاث مجموعات أولوية فقط على صفحة المهمة.</span><span class="sxs-lookup"><span data-stu-id="4bb55-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="4bb55-137">عندما يرسل النظام بيانات التعريف إلى التطبيق، فسوف يقوم بتعيين أولوية الحقل النسبية بناءً على مجموعة الأولوية الخاصة به، وسوف يعرض التطبيق مجموعات الأولوية الثلاث الواردة في بيانات التعريف على صفحة المهمة.</span><span class="sxs-lookup"><span data-stu-id="4bb55-137">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="4bb55-138">وسوف يتم عرض بقية بيانات التعريف الزائدة على صفحة تفاصيل ثانوية.</span><span class="sxs-lookup"><span data-stu-id="4bb55-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="4bb55-139">يعرض الجدول التالي مثالًا على مجموعات الأولوية الخمس.</span><span class="sxs-lookup"><span data-stu-id="4bb55-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4bb55-140">مجموعة الأولوية</span><span class="sxs-lookup"><span data-stu-id="4bb55-140">Priority group</span></span></th>
<th><span data-ttu-id="4bb55-141">الحقول المعيِّنة</span><span class="sxs-lookup"><span data-stu-id="4bb55-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="4bb55-142">الأولوية 10</span><span class="sxs-lookup"><span data-stu-id="4bb55-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="4bb55-143">الصنف</span><span class="sxs-lookup"><span data-stu-id="4bb55-143">Item</span></span></li>
<li><span data-ttu-id="4bb55-144">الكمية</span><span class="sxs-lookup"><span data-stu-id="4bb55-144">Quantity</span></span></li>
<li><span data-ttu-id="4bb55-145">وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="4bb55-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="4bb55-146">الأولوية 20</span><span class="sxs-lookup"><span data-stu-id="4bb55-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="4bb55-147">منصب نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="4bb55-147">Cluster position</span></span></li>
<li><span data-ttu-id="4bb55-148">مجموعة</span><span class="sxs-lookup"><span data-stu-id="4bb55-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="4bb55-149">الأولوية 30</span><span class="sxs-lookup"><span data-stu-id="4bb55-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="4bb55-150">وصف الصنف</span><span class="sxs-lookup"><span data-stu-id="4bb55-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="4bb55-151">الأولوية 40</span><span class="sxs-lookup"><span data-stu-id="4bb55-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="4bb55-152">التكوين</span><span class="sxs-lookup"><span data-stu-id="4bb55-152">Configuration</span></span></li>
<li><span data-ttu-id="4bb55-153">اللون</span><span class="sxs-lookup"><span data-stu-id="4bb55-153">Color</span></span></li>
<li><span data-ttu-id="4bb55-154">الحجم</span><span class="sxs-lookup"><span data-stu-id="4bb55-154">Size</span></span></li>
<li><span data-ttu-id="4bb55-155">نمط</span><span class="sxs-lookup"><span data-stu-id="4bb55-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="4bb55-156">الأولوية 50</span><span class="sxs-lookup"><span data-stu-id="4bb55-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="4bb55-157"> الموق</span><span class="sxs-lookup"><span data-stu-id="4bb55-157">Location</span></span></li>
<li><span data-ttu-id="4bb55-158">لوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="4bb55-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4bb55-159">على سبيل المثال، عندما يقوم أحد عمال المخزن بتنفيذ مهمة على جهاز محمول، إذا كانت بيانات التعريف التي سيتم عرضها في التطبيق تتكون من الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="4bb55-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="4bb55-160">الصنف</span><span class="sxs-lookup"><span data-stu-id="4bb55-160">Item</span></span>
-   <span data-ttu-id="4bb55-161">الكمية</span><span class="sxs-lookup"><span data-stu-id="4bb55-161">Quantity</span></span>
-   <span data-ttu-id="4bb55-162">وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="4bb55-162">Unit of measure</span></span>
-   <span data-ttu-id="4bb55-163">وصف الصنف</span><span class="sxs-lookup"><span data-stu-id="4bb55-163">Item description</span></span>
-   <span data-ttu-id="4bb55-164">الحجم والموقع</span><span class="sxs-lookup"><span data-stu-id="4bb55-164">Size and Location</span></span>

<span data-ttu-id="4bb55-165">بناءً على إعداد أولوية حقل تطبيق المخزن في الجدول أعلاه، فسوف يتم عرض صفوف المعلومات الثلاثة التالية على صفحة المهمة:</span><span class="sxs-lookup"><span data-stu-id="4bb55-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="4bb55-166">الصف الأول: الصنف والكمية ووحدة القياس</span><span class="sxs-lookup"><span data-stu-id="4bb55-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="4bb55-167">الصف 2: وصف الصنف</span><span class="sxs-lookup"><span data-stu-id="4bb55-167">Row 2: Item description</span></span>
-   <span data-ttu-id="4bb55-168">صف 3: الحجم</span><span class="sxs-lookup"><span data-stu-id="4bb55-168">Row 3: Size</span></span>

<span data-ttu-id="4bb55-169">لن يتم عرض بيانات التعريف المتبقية، الموقع على سبيل المثال، على صفحة المهمة، ولكن سيتم عرضها على صفحة التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="4bb55-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="4bb55-170">لمزيد من المعلومات ومشاهدة أمثلة من واجهة المستخدم، راجع منشور مدونة [الإعلان عن Finance and Operations - التخزين](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="4bb55-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="4bb55-171">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4bb55-171">Additional resources</span></span>
--------

[<span data-ttu-id="4bb55-172">نظرة عامة على تثبيت وتكوين تطبيق التخزين</span><span class="sxs-lookup"><span data-stu-id="4bb55-172">Install and configure the Warehousing app overview</span></span>](install-configure-warehousing-app.md)
