---
title: تستخدم التقارير الإلكترونية ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 3 - إنشاء التنسيق)
description: يوضح هذا الموضوع كيفيه تكوين تنسيق التقارير الكترونيه لاستخدام ملفات أداره المستندات في إخراج ER. (جزء 3)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99a286b4e40ddeb7f4ff37c1ece3c678b26c838b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755000"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="822f1-104">تستخدم التقارير الإلكترونية ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 3 - إنشاء التنسيق)</span><span class="sxs-lookup"><span data-stu-id="822f1-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="822f1-105">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="822f1-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="822f1-106">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="822f1-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="822f1-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 2: توسيع نموذج البيانات").</span><span class="sxs-lookup"><span data-stu-id="822f1-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="822f1-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="822f1-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="822f1-109">إنشاء تنسيق لمعالجة الفواتير</span><span class="sxs-lookup"><span data-stu-id="822f1-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="822f1-110">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="822f1-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="822f1-111">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="822f1-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="822f1-112">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="822f1-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="822f1-113">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="822f1-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="822f1-114">ستقوم بإنشاء تنسيق لإنشاء رسائل إلكترونية ذات معلومات حول أي من الملفات التي تم إرفاقها بأمر مبيعات يرتبط بفاتورة تتم معالجتها إلكترونيًا.</span><span class="sxs-lookup"><span data-stu-id="822f1-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="822f1-115">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="822f1-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="822f1-116">في الحقل "جديد"، أدخل 'التنسيق المستند إلى نموذج البيانات نموذج فاتورة العميل (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="822f1-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="822f1-117">في حقل "الاسم"، اكتب "رسالة نموذجية للفاتورة الإلكترونية".</span><span class="sxs-lookup"><span data-stu-id="822f1-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="822f1-118">رسالة نموذجية للفاتورة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="822f1-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="822f1-119">في الحقل "تعريف نموذج البيانات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="822f1-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="822f1-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="822f1-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="822f1-121">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="822f1-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="822f1-122">تصميم تنسيق لتعبئة المرفقات في الرسالة الناشئة بتنسيق MIME</span><span class="sxs-lookup"><span data-stu-id="822f1-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="822f1-123">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="822f1-123">Click Designer.</span></span>
2. <span data-ttu-id="822f1-124">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="822f1-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="822f1-125">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="822f1-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="822f1-126">في حقل "الاسم"، اكتب "الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="822f1-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="822f1-127">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="822f1-127">Invoice</span></span>  
5. <span data-ttu-id="822f1-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="822f1-128">Click OK.</span></span>
6. <span data-ttu-id="822f1-129">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="822f1-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="822f1-130">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="822f1-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="822f1-131">في حقل "الاسم"، اكتب "SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="822f1-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="822f1-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="822f1-132">SalesOrder</span></span>  
9. <span data-ttu-id="822f1-133">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="822f1-133">Click OK.</span></span>
10. <span data-ttu-id="822f1-134">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="822f1-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="822f1-135">في حقل "الاسم"، اكتب "InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="822f1-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="822f1-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="822f1-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="822f1-137">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="822f1-137">Click OK.</span></span>
13. <span data-ttu-id="822f1-138">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="822f1-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="822f1-139">في حقل "الاسم"، اكتب "InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="822f1-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="822f1-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="822f1-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="822f1-141">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="822f1-141">Click OK.</span></span>
16. <span data-ttu-id="822f1-142">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="822f1-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="822f1-143">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="822f1-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="822f1-144">في حقل "الاسم"، اكتب "EnclosedDocs".</span><span class="sxs-lookup"><span data-stu-id="822f1-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="822f1-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="822f1-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="822f1-146">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="822f1-146">Click OK.</span></span>
20. <span data-ttu-id="822f1-147">في الشجرة، حدد "الفاتورة\EnclosedDocs‬".</span><span class="sxs-lookup"><span data-stu-id="822f1-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="822f1-148">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="822f1-148">Click Add Element.</span></span>
22. <span data-ttu-id="822f1-149">في حقل "الاسم"، اكتب "المستند".</span><span class="sxs-lookup"><span data-stu-id="822f1-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="822f1-150">مستند</span><span class="sxs-lookup"><span data-stu-id="822f1-150">Document</span></span>  
23. <span data-ttu-id="822f1-151">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="822f1-151">Click OK.</span></span>
24. <span data-ttu-id="822f1-152">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند".</span><span class="sxs-lookup"><span data-stu-id="822f1-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="822f1-153">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="822f1-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="822f1-154">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="822f1-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="822f1-155">في حقل "الاسم"، اكتب "FileName".</span><span class="sxs-lookup"><span data-stu-id="822f1-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="822f1-156">FileName</span><span class="sxs-lookup"><span data-stu-id="822f1-156">FileName</span></span>  
28. <span data-ttu-id="822f1-157">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="822f1-157">Click OK.</span></span>
29. <span data-ttu-id="822f1-158">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="822f1-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="822f1-159">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="822f1-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="822f1-160">في حقل "الاسم"، اكتب "FileContent".</span><span class="sxs-lookup"><span data-stu-id="822f1-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="822f1-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="822f1-161">FileContent</span></span>  
32. <span data-ttu-id="822f1-162">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="822f1-162">Click OK.</span></span>
33. <span data-ttu-id="822f1-163">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند\FileContent".</span><span class="sxs-lookup"><span data-stu-id="822f1-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="822f1-164">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="822f1-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="822f1-165">في الشجرة، حدد "النص\Base64".</span><span class="sxs-lookup"><span data-stu-id="822f1-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="822f1-166">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="822f1-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="822f1-167">تعيين عناصر التنسيق إلى نموذج بيانات كمصدر بيانات</span><span class="sxs-lookup"><span data-stu-id="822f1-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="822f1-168">في الشجرة، حدد "الفاتورة‬\SalesOrder‬".</span><span class="sxs-lookup"><span data-stu-id="822f1-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="822f1-169">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="822f1-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="822f1-170">في الشجرة، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="822f1-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="822f1-171">في الشجرة، حدد "النموذج\رقم أمر المبيعات(SalesId)".</span><span class="sxs-lookup"><span data-stu-id="822f1-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="822f1-172">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="822f1-172">Click Bind.</span></span>
6. <span data-ttu-id="822f1-173">في الشجرة، حدد "الفاتورة\InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="822f1-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="822f1-174">في الشجرة، قم بتوسيع "النموذج\الفاتورة الأساسية‬(InvoiceBase)".</span><span class="sxs-lookup"><span data-stu-id="822f1-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="822f1-175">في الشجرة، حدد "النموذج\الفاتورة الأساسية(InvoiceBase)\رقم الفاتورة(Id)".</span><span class="sxs-lookup"><span data-stu-id="822f1-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="822f1-176">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="822f1-176">Click Bind.</span></span>
10. <span data-ttu-id="822f1-177">في الشجرة، حدد "الفاتورة\InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="822f1-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="822f1-178">في الشجرة، حدد "النموذج\الفاتورة الأساسية(InvoiceBase)\مبلغ الفاتورة(المبلغ)".</span><span class="sxs-lookup"><span data-stu-id="822f1-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="822f1-179">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="822f1-179">Click Bind.</span></span>
13. <span data-ttu-id="822f1-180">في الشجرة، قم بتوسيع "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="822f1-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="822f1-181">في الشجرة، حدد "النموذج\مرفقات الفاتورة\محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="822f1-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="822f1-182">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند\FileContent\Base64".</span><span class="sxs-lookup"><span data-stu-id="822f1-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="822f1-183">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="822f1-183">Click Bind.</span></span>
17. <span data-ttu-id="822f1-184">في الشجرة، حدد "النموذج\مرفقات الفاتورة\اسم الملف‬".</span><span class="sxs-lookup"><span data-stu-id="822f1-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="822f1-185">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند\FileName".</span><span class="sxs-lookup"><span data-stu-id="822f1-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="822f1-186">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="822f1-186">Click Bind.</span></span>
20. <span data-ttu-id="822f1-187">في الشجرة، حدد "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="822f1-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="822f1-188">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند".</span><span class="sxs-lookup"><span data-stu-id="822f1-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="822f1-189">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="822f1-189">Click Bind.</span></span>
23. <span data-ttu-id="822f1-190">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="822f1-190">Click Save.</span></span>
24. <span data-ttu-id="822f1-191">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="822f1-191">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]