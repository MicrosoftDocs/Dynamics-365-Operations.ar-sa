--- 
title: "إنشاء تنسيقات لاستخدام ملفات إدارة المستندات في مخرجات التقارير الإلكترونية"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 934775bbdda13238e16fba91dcb90d6d3249e812
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---
# <a name="create-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="7b0b6-103">إنشاء تنسيقات لاستخدام ملفات إدارة المستندات في مخرجات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="7b0b6-103">Create formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b0b6-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="7b0b6-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="7b0b6-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 2: توسيع نموذج البيانات").</span><span class="sxs-lookup"><span data-stu-id="7b0b6-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="7b0b6-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="7b0b6-108">إنشاء تنسيق لمعالجة الفواتير</span><span class="sxs-lookup"><span data-stu-id="7b0b6-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="7b0b6-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7b0b6-110">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="7b0b6-111">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="7b0b6-112">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="7b0b6-113">ستقوم بإنشاء تنسيق لإنشاء رسائل إلكترونية ذات معلومات حول أي من الملفات التي تم إرفاقها بأمر مبيعات يرتبط بفاتورة تتم معالجتها إلكترونيًا.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="7b0b6-114">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="7b0b6-115">في الحقل "جديد"، أدخل 'التنسيق المستند إلى نموذج البيانات نموذج فاتورة العميل (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="7b0b6-116">في حقل "الاسم"، اكتب "رسالة نموذجية للفاتورة الإلكترونية".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="7b0b6-117">رسالة نموذجية للفاتورة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="7b0b6-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="7b0b6-118">في الحقل "تعريف نموذج البيانات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="7b0b6-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="7b0b6-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="7b0b6-120">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="7b0b6-121">تصميم تنسيق لتعبئة المرفقات في الرسالة الناشئة بتنسيق MIME</span><span class="sxs-lookup"><span data-stu-id="7b0b6-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="7b0b6-122">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-122">Click Designer.</span></span>
2. <span data-ttu-id="7b0b6-123">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="7b0b6-124">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="7b0b6-125">في حقل "الاسم"، اكتب "الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="7b0b6-126">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="7b0b6-126">Invoice</span></span>  
5. <span data-ttu-id="7b0b6-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-127">Click OK.</span></span>
6. <span data-ttu-id="7b0b6-128">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="7b0b6-129">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="7b0b6-130">في حقل "الاسم"، اكتب "SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="7b0b6-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="7b0b6-131">SalesOrder</span></span>  
9. <span data-ttu-id="7b0b6-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-132">Click OK.</span></span>
10. <span data-ttu-id="7b0b6-133">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="7b0b6-134">في حقل "الاسم"، اكتب "InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="7b0b6-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="7b0b6-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="7b0b6-136">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-136">Click OK.</span></span>
13. <span data-ttu-id="7b0b6-137">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="7b0b6-138">في حقل "الاسم"، اكتب "InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="7b0b6-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="7b0b6-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="7b0b6-140">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-140">Click OK.</span></span>
16. <span data-ttu-id="7b0b6-141">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="7b0b6-142">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="7b0b6-143">في حقل "الاسم"، اكتب "EnclosedDocs".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="7b0b6-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="7b0b6-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="7b0b6-145">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-145">Click OK.</span></span>
20. <span data-ttu-id="7b0b6-146">في الشجرة، حدد "الفاتورة\EnclosedDocs‬".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="7b0b6-147">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-147">Click Add Element.</span></span>
22. <span data-ttu-id="7b0b6-148">في حقل "الاسم"، اكتب "المستند".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="7b0b6-149">مستند</span><span class="sxs-lookup"><span data-stu-id="7b0b6-149">Document</span></span>  
23. <span data-ttu-id="7b0b6-150">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-150">Click OK.</span></span>
24. <span data-ttu-id="7b0b6-151">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="7b0b6-152">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="7b0b6-153">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="7b0b6-154">في حقل "الاسم"، اكتب "FileName".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="7b0b6-155">FileName</span><span class="sxs-lookup"><span data-stu-id="7b0b6-155">FileName</span></span>  
28. <span data-ttu-id="7b0b6-156">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-156">Click OK.</span></span>
29. <span data-ttu-id="7b0b6-157">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="7b0b6-158">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="7b0b6-159">في حقل "الاسم"، اكتب "FileContent".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="7b0b6-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="7b0b6-160">FileContent</span></span>  
32. <span data-ttu-id="7b0b6-161">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-161">Click OK.</span></span>
33. <span data-ttu-id="7b0b6-162">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند\FileContent".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="7b0b6-163">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="7b0b6-164">في الشجرة، حدد "النص\Base64".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="7b0b6-165">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="7b0b6-166">تعيين عناصر التنسيق إلى نموذج بيانات كمصدر بيانات</span><span class="sxs-lookup"><span data-stu-id="7b0b6-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="7b0b6-167">في الشجرة، حدد "الفاتورة‬\SalesOrder‬".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="7b0b6-168">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="7b0b6-169">في الشجرة، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="7b0b6-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="7b0b6-170">في الشجرة، حدد "النموذج\رقم أمر المبيعات(SalesId)".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="7b0b6-171">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-171">Click Bind.</span></span>
6. <span data-ttu-id="7b0b6-172">في الشجرة، حدد "الفاتورة\InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="7b0b6-173">في الشجرة، قم بتوسيع "النموذج\الفاتورة الأساسية‬(InvoiceBase)".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="7b0b6-174">في الشجرة، حدد "النموذج\الفاتورة الأساسية(InvoiceBase)\رقم الفاتورة(Id)".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="7b0b6-175">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-175">Click Bind.</span></span>
10. <span data-ttu-id="7b0b6-176">في الشجرة، حدد "الفاتورة\InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="7b0b6-177">في الشجرة، حدد "النموذج\الفاتورة الأساسية(InvoiceBase)\مبلغ الفاتورة(المبلغ)".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="7b0b6-178">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-178">Click Bind.</span></span>
13. <span data-ttu-id="7b0b6-179">في الشجرة، قم بتوسيع "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="7b0b6-180">في الشجرة، حدد "النموذج\مرفقات الفاتورة\محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="7b0b6-181">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند\FileContent\Base64".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="7b0b6-182">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-182">Click Bind.</span></span>
17. <span data-ttu-id="7b0b6-183">في الشجرة، حدد "النموذج\مرفقات الفاتورة\اسم الملف‬".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="7b0b6-184">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند\FileName".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="7b0b6-185">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-185">Click Bind.</span></span>
20. <span data-ttu-id="7b0b6-186">في الشجرة، حدد "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="7b0b6-187">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="7b0b6-188">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-188">Click Bind.</span></span>
23. <span data-ttu-id="7b0b6-189">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7b0b6-189">Click Save.</span></span>
24. <span data-ttu-id="7b0b6-190">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7b0b6-190">Close the page.</span></span>


