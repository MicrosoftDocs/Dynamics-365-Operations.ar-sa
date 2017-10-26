--- 
title: "إنشاء تنسيق لاستخدام ملفات إدارة المستندات في مخرجات التنسيق للتقارير الإلكترونية (ER)"
description: "تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 71e40351e8b54092d1bbcbc73c6da69073791b74
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="create-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="83f4d-103">إنشاء تنسيق لاستخدام ملفات إدارة المستندات في مخرجات التنسيق للتقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="83f4d-103">Create format to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="83f4d-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="83f4d-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="83f4d-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="83f4d-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="83f4d-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 2: توسيع نموذج البيانات").</span><span class="sxs-lookup"><span data-stu-id="83f4d-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="83f4d-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="83f4d-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="83f4d-108">إنشاء تنسيق لمعالجة الفواتير</span><span class="sxs-lookup"><span data-stu-id="83f4d-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="83f4d-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="83f4d-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="83f4d-110">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="83f4d-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="83f4d-111">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="83f4d-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="83f4d-112">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="83f4d-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="83f4d-113">ستقوم بإنشاء تنسيق لإنشاء رسائل إلكترونية ذات معلومات حول أي من الملفات التي تم إرفاقها بأمر مبيعات يرتبط بفاتورة تتم معالجتها إلكترونيًا.</span><span class="sxs-lookup"><span data-stu-id="83f4d-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="83f4d-114">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="83f4d-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="83f4d-115">في الحقل "جديد"، أدخل 'التنسيق المستند إلى نموذج البيانات نموذج فاتورة العميل (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="83f4d-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="83f4d-116">في حقل "الاسم"، اكتب "رسالة نموذجية للفاتورة الإلكترونية".</span><span class="sxs-lookup"><span data-stu-id="83f4d-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="83f4d-117">رسالة نموذجية للفاتورة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="83f4d-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="83f4d-118">في الحقل "تعريف نموذج البيانات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="83f4d-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="83f4d-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="83f4d-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="83f4d-120">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="83f4d-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="83f4d-121">تصميم تنسيق لتعبئة المرفقات في الرسالة الناشئة بتنسيق MIME</span><span class="sxs-lookup"><span data-stu-id="83f4d-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="83f4d-122">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="83f4d-122">Click Designer.</span></span>
2. <span data-ttu-id="83f4d-123">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="83f4d-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="83f4d-124">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="83f4d-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="83f4d-125">في حقل "الاسم"، اكتب "الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="83f4d-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="83f4d-126">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="83f4d-126">Invoice</span></span>  
5. <span data-ttu-id="83f4d-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="83f4d-127">Click OK.</span></span>
6. <span data-ttu-id="83f4d-128">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="83f4d-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="83f4d-129">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="83f4d-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="83f4d-130">في حقل "الاسم"، اكتب "SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="83f4d-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="83f4d-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="83f4d-131">SalesOrder</span></span>  
9. <span data-ttu-id="83f4d-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="83f4d-132">Click OK.</span></span>
10. <span data-ttu-id="83f4d-133">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="83f4d-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="83f4d-134">في حقل "الاسم"، اكتب "InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="83f4d-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="83f4d-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="83f4d-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="83f4d-136">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="83f4d-136">Click OK.</span></span>
13. <span data-ttu-id="83f4d-137">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="83f4d-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="83f4d-138">في حقل "الاسم"، اكتب "InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="83f4d-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="83f4d-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="83f4d-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="83f4d-140">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="83f4d-140">Click OK.</span></span>
16. <span data-ttu-id="83f4d-141">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="83f4d-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="83f4d-142">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="83f4d-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="83f4d-143">في حقل "الاسم"، اكتب "EnclosedDocs".</span><span class="sxs-lookup"><span data-stu-id="83f4d-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="83f4d-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="83f4d-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="83f4d-145">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="83f4d-145">Click OK.</span></span>
20. <span data-ttu-id="83f4d-146">في الشجرة، حدد "الفاتورة\EnclosedDocs‬".</span><span class="sxs-lookup"><span data-stu-id="83f4d-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="83f4d-147">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="83f4d-147">Click Add Element.</span></span>
22. <span data-ttu-id="83f4d-148">في حقل "الاسم"، اكتب "المستند".</span><span class="sxs-lookup"><span data-stu-id="83f4d-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="83f4d-149">مستند</span><span class="sxs-lookup"><span data-stu-id="83f4d-149">Document</span></span>  
23. <span data-ttu-id="83f4d-150">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="83f4d-150">Click OK.</span></span>
24. <span data-ttu-id="83f4d-151">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند".</span><span class="sxs-lookup"><span data-stu-id="83f4d-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="83f4d-152">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="83f4d-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="83f4d-153">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="83f4d-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="83f4d-154">في حقل "الاسم"، اكتب "FileName".</span><span class="sxs-lookup"><span data-stu-id="83f4d-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="83f4d-155">FileName</span><span class="sxs-lookup"><span data-stu-id="83f4d-155">FileName</span></span>  
28. <span data-ttu-id="83f4d-156">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="83f4d-156">Click OK.</span></span>
29. <span data-ttu-id="83f4d-157">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="83f4d-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="83f4d-158">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="83f4d-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="83f4d-159">في حقل "الاسم"، اكتب "FileContent".</span><span class="sxs-lookup"><span data-stu-id="83f4d-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="83f4d-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="83f4d-160">FileContent</span></span>  
32. <span data-ttu-id="83f4d-161">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="83f4d-161">Click OK.</span></span>
33. <span data-ttu-id="83f4d-162">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند\FileContent".</span><span class="sxs-lookup"><span data-stu-id="83f4d-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="83f4d-163">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="83f4d-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="83f4d-164">في الشجرة، حدد "النص\Base64".</span><span class="sxs-lookup"><span data-stu-id="83f4d-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="83f4d-165">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="83f4d-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="83f4d-166">تعيين عناصر التنسيق إلى نموذج بيانات كمصدر بيانات</span><span class="sxs-lookup"><span data-stu-id="83f4d-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="83f4d-167">في الشجرة، حدد "الفاتورة‬\SalesOrder‬".</span><span class="sxs-lookup"><span data-stu-id="83f4d-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="83f4d-168">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="83f4d-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="83f4d-169">في الشجرة، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="83f4d-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="83f4d-170">في الشجرة، حدد "النموذج\رقم أمر المبيعات(SalesId)".</span><span class="sxs-lookup"><span data-stu-id="83f4d-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="83f4d-171">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83f4d-171">Click Bind.</span></span>
6. <span data-ttu-id="83f4d-172">في الشجرة، حدد "الفاتورة\InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="83f4d-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="83f4d-173">في الشجرة، قم بتوسيع "النموذج\الفاتورة الأساسية‬(InvoiceBase)".</span><span class="sxs-lookup"><span data-stu-id="83f4d-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="83f4d-174">في الشجرة، حدد "النموذج\الفاتورة الأساسية(InvoiceBase)\رقم الفاتورة(Id)".</span><span class="sxs-lookup"><span data-stu-id="83f4d-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="83f4d-175">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83f4d-175">Click Bind.</span></span>
10. <span data-ttu-id="83f4d-176">في الشجرة، حدد "الفاتورة\InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="83f4d-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="83f4d-177">في الشجرة، حدد "النموذج\الفاتورة الأساسية(InvoiceBase)\مبلغ الفاتورة(المبلغ)".</span><span class="sxs-lookup"><span data-stu-id="83f4d-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="83f4d-178">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83f4d-178">Click Bind.</span></span>
13. <span data-ttu-id="83f4d-179">في الشجرة، قم بتوسيع "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="83f4d-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="83f4d-180">في الشجرة، حدد "النموذج\مرفقات الفاتورة\محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="83f4d-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="83f4d-181">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند\FileContent\Base64".</span><span class="sxs-lookup"><span data-stu-id="83f4d-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="83f4d-182">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83f4d-182">Click Bind.</span></span>
17. <span data-ttu-id="83f4d-183">في الشجرة، حدد "النموذج\مرفقات الفاتورة\اسم الملف‬".</span><span class="sxs-lookup"><span data-stu-id="83f4d-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="83f4d-184">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند\FileName".</span><span class="sxs-lookup"><span data-stu-id="83f4d-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="83f4d-185">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83f4d-185">Click Bind.</span></span>
20. <span data-ttu-id="83f4d-186">في الشجرة، حدد "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="83f4d-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="83f4d-187">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند".</span><span class="sxs-lookup"><span data-stu-id="83f4d-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="83f4d-188">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="83f4d-188">Click Bind.</span></span>
23. <span data-ttu-id="83f4d-189">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="83f4d-189">Click Save.</span></span>
24. <span data-ttu-id="83f4d-190">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="83f4d-190">Close the page.</span></span>

