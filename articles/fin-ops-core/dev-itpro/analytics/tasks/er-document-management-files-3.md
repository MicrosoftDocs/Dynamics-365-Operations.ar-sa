---
title: تستخدم التقارير الإلكترونية ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 3 - إنشاء التنسيق)
description: يوضح هذا الموضوع كيفيه تكوين تنسيق التقارير الكترونيه لاستخدام ملفات أداره المستندات في إخراج ER. (جزء 3)
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: 1ec1ebc15cd980734aebec63d6758404868c1e36
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559739"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="217c8-104">تستخدم التقارير الإلكترونية ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 3 - إنشاء التنسيق)</span><span class="sxs-lookup"><span data-stu-id="217c8-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="217c8-105">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="217c8-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="217c8-106">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="217c8-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="217c8-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 2: توسيع نموذج البيانات").</span><span class="sxs-lookup"><span data-stu-id="217c8-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="217c8-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="217c8-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="217c8-109">إنشاء تنسيق لمعالجة الفواتير</span><span class="sxs-lookup"><span data-stu-id="217c8-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="217c8-110">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="217c8-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="217c8-111">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="217c8-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="217c8-112">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="217c8-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="217c8-113">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="217c8-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="217c8-114">ستقوم بإنشاء تنسيق لإنشاء رسائل إلكترونية ذات معلومات حول أي من الملفات التي تم إرفاقها بأمر مبيعات يرتبط بفاتورة تتم معالجتها إلكترونيًا.</span><span class="sxs-lookup"><span data-stu-id="217c8-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="217c8-115">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="217c8-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="217c8-116">في الحقل "جديد"، أدخل 'التنسيق المستند إلى نموذج البيانات نموذج فاتورة العميل (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="217c8-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="217c8-117">في حقل "الاسم"، اكتب "رسالة نموذجية للفاتورة الإلكترونية".</span><span class="sxs-lookup"><span data-stu-id="217c8-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="217c8-118">رسالة نموذجية للفاتورة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="217c8-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="217c8-119">في الحقل "تعريف نموذج البيانات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="217c8-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="217c8-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="217c8-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="217c8-121">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="217c8-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="217c8-122">تصميم تنسيق لتعبئة المرفقات في الرسالة الناشئة بتنسيق MIME</span><span class="sxs-lookup"><span data-stu-id="217c8-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="217c8-123">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="217c8-123">Click Designer.</span></span>
2. <span data-ttu-id="217c8-124">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="217c8-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="217c8-125">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="217c8-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="217c8-126">في حقل "الاسم"، اكتب "الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="217c8-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="217c8-127">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="217c8-127">Invoice</span></span>  
5. <span data-ttu-id="217c8-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="217c8-128">Click OK.</span></span>
6. <span data-ttu-id="217c8-129">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="217c8-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="217c8-130">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="217c8-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="217c8-131">في حقل "الاسم"، اكتب "SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="217c8-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="217c8-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="217c8-132">SalesOrder</span></span>  
9. <span data-ttu-id="217c8-133">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="217c8-133">Click OK.</span></span>
10. <span data-ttu-id="217c8-134">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="217c8-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="217c8-135">في حقل "الاسم"، اكتب "InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="217c8-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="217c8-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="217c8-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="217c8-137">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="217c8-137">Click OK.</span></span>
13. <span data-ttu-id="217c8-138">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="217c8-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="217c8-139">في حقل "الاسم"، اكتب "InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="217c8-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="217c8-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="217c8-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="217c8-141">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="217c8-141">Click OK.</span></span>
16. <span data-ttu-id="217c8-142">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="217c8-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="217c8-143">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="217c8-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="217c8-144">في حقل "الاسم"، اكتب "EnclosedDocs".</span><span class="sxs-lookup"><span data-stu-id="217c8-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="217c8-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="217c8-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="217c8-146">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="217c8-146">Click OK.</span></span>
20. <span data-ttu-id="217c8-147">في الشجرة، حدد "الفاتورة\EnclosedDocs‬".</span><span class="sxs-lookup"><span data-stu-id="217c8-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="217c8-148">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="217c8-148">Click Add Element.</span></span>
22. <span data-ttu-id="217c8-149">في حقل "الاسم"، اكتب "المستند".</span><span class="sxs-lookup"><span data-stu-id="217c8-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="217c8-150">مستند</span><span class="sxs-lookup"><span data-stu-id="217c8-150">Document</span></span>  
23. <span data-ttu-id="217c8-151">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="217c8-151">Click OK.</span></span>
24. <span data-ttu-id="217c8-152">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند".</span><span class="sxs-lookup"><span data-stu-id="217c8-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="217c8-153">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="217c8-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="217c8-154">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="217c8-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="217c8-155">في حقل "الاسم"، اكتب "FileName".</span><span class="sxs-lookup"><span data-stu-id="217c8-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="217c8-156">FileName</span><span class="sxs-lookup"><span data-stu-id="217c8-156">FileName</span></span>  
28. <span data-ttu-id="217c8-157">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="217c8-157">Click OK.</span></span>
29. <span data-ttu-id="217c8-158">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="217c8-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="217c8-159">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="217c8-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="217c8-160">في حقل "الاسم"، اكتب "FileContent".</span><span class="sxs-lookup"><span data-stu-id="217c8-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="217c8-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="217c8-161">FileContent</span></span>  
32. <span data-ttu-id="217c8-162">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="217c8-162">Click OK.</span></span>
33. <span data-ttu-id="217c8-163">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند\FileContent".</span><span class="sxs-lookup"><span data-stu-id="217c8-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="217c8-164">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="217c8-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="217c8-165">في الشجرة، حدد "النص\Base64".</span><span class="sxs-lookup"><span data-stu-id="217c8-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="217c8-166">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="217c8-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="217c8-167">تعيين عناصر التنسيق إلى نموذج بيانات كمصدر بيانات</span><span class="sxs-lookup"><span data-stu-id="217c8-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="217c8-168">في الشجرة، حدد "الفاتورة‬\SalesOrder‬".</span><span class="sxs-lookup"><span data-stu-id="217c8-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="217c8-169">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="217c8-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="217c8-170">في الشجرة، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="217c8-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="217c8-171">في الشجرة، حدد "النموذج\رقم أمر المبيعات(SalesId)".</span><span class="sxs-lookup"><span data-stu-id="217c8-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="217c8-172">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="217c8-172">Click Bind.</span></span>
6. <span data-ttu-id="217c8-173">في الشجرة، حدد "الفاتورة\InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="217c8-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="217c8-174">في الشجرة، قم بتوسيع "النموذج\الفاتورة الأساسية‬(InvoiceBase)".</span><span class="sxs-lookup"><span data-stu-id="217c8-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="217c8-175">في الشجرة، حدد "النموذج\الفاتورة الأساسية(InvoiceBase)\رقم الفاتورة(Id)".</span><span class="sxs-lookup"><span data-stu-id="217c8-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="217c8-176">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="217c8-176">Click Bind.</span></span>
10. <span data-ttu-id="217c8-177">في الشجرة، حدد "الفاتورة\InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="217c8-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="217c8-178">في الشجرة، حدد "النموذج\الفاتورة الأساسية(InvoiceBase)\مبلغ الفاتورة(المبلغ)".</span><span class="sxs-lookup"><span data-stu-id="217c8-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="217c8-179">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="217c8-179">Click Bind.</span></span>
13. <span data-ttu-id="217c8-180">في الشجرة، قم بتوسيع "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="217c8-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="217c8-181">في الشجرة، حدد "النموذج\مرفقات الفاتورة\محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="217c8-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="217c8-182">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند\FileContent\Base64".</span><span class="sxs-lookup"><span data-stu-id="217c8-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="217c8-183">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="217c8-183">Click Bind.</span></span>
17. <span data-ttu-id="217c8-184">في الشجرة، حدد "النموذج\مرفقات الفاتورة\اسم الملف‬".</span><span class="sxs-lookup"><span data-stu-id="217c8-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="217c8-185">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند\FileName".</span><span class="sxs-lookup"><span data-stu-id="217c8-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="217c8-186">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="217c8-186">Click Bind.</span></span>
20. <span data-ttu-id="217c8-187">في الشجرة، حدد "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="217c8-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="217c8-188">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند".</span><span class="sxs-lookup"><span data-stu-id="217c8-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="217c8-189">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="217c8-189">Click Bind.</span></span>
23. <span data-ttu-id="217c8-190">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="217c8-190">Click Save.</span></span>
24. <span data-ttu-id="217c8-191">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="217c8-191">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]