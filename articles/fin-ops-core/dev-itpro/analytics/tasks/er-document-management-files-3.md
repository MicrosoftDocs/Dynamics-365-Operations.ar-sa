---
title: تستخدم التقارير الإلكترونية ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 3 - إنشاء التنسيق)
description: تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات في مخرجات التقارير الإلكترونية.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bfcc03fa7470d4f2fa45ef012e30acef0712bf99
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681843"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="f0ccf-103">تستخدم التقارير الإلكترونية ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 3 - إنشاء التنسيق)</span><span class="sxs-lookup"><span data-stu-id="f0ccf-103">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0ccf-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="f0ccf-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="f0ccf-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 2: توسيع نموذج البيانات").</span><span class="sxs-lookup"><span data-stu-id="f0ccf-106">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="f0ccf-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="f0ccf-108">إنشاء تنسيق لمعالجة الفواتير</span><span class="sxs-lookup"><span data-stu-id="f0ccf-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="f0ccf-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f0ccf-110">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f0ccf-111">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="f0ccf-112">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="f0ccf-113">ستقوم بإنشاء تنسيق لإنشاء رسائل إلكترونية ذات معلومات حول أي من الملفات التي تم إرفاقها بأمر مبيعات يرتبط بفاتورة تتم معالجتها إلكترونيًا.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="f0ccf-114">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="f0ccf-115">في الحقل "جديد"، أدخل 'التنسيق المستند إلى نموذج البيانات نموذج فاتورة العميل (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="f0ccf-116">في حقل "الاسم"، اكتب "رسالة نموذجية للفاتورة الإلكترونية".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="f0ccf-117">رسالة نموذجية للفاتورة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f0ccf-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="f0ccf-118">في الحقل "تعريف نموذج البيانات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="f0ccf-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="f0ccf-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="f0ccf-120">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="f0ccf-121">تصميم تنسيق لتعبئة المرفقات في الرسالة الناشئة بتنسيق MIME</span><span class="sxs-lookup"><span data-stu-id="f0ccf-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="f0ccf-122">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-122">Click Designer.</span></span>
2. <span data-ttu-id="f0ccf-123">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="f0ccf-124">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="f0ccf-125">في حقل "الاسم"، اكتب "الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="f0ccf-126">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="f0ccf-126">Invoice</span></span>  
5. <span data-ttu-id="f0ccf-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-127">Click OK.</span></span>
6. <span data-ttu-id="f0ccf-128">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="f0ccf-129">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="f0ccf-130">في حقل "الاسم"، اكتب "SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="f0ccf-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="f0ccf-131">SalesOrder</span></span>  
9. <span data-ttu-id="f0ccf-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-132">Click OK.</span></span>
10. <span data-ttu-id="f0ccf-133">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="f0ccf-134">في حقل "الاسم"، اكتب "InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="f0ccf-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="f0ccf-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="f0ccf-136">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-136">Click OK.</span></span>
13. <span data-ttu-id="f0ccf-137">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="f0ccf-138">في حقل "الاسم"، اكتب "InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="f0ccf-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="f0ccf-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="f0ccf-140">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-140">Click OK.</span></span>
16. <span data-ttu-id="f0ccf-141">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="f0ccf-142">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="f0ccf-143">في حقل "الاسم"، اكتب "EnclosedDocs".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="f0ccf-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="f0ccf-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="f0ccf-145">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-145">Click OK.</span></span>
20. <span data-ttu-id="f0ccf-146">في الشجرة، حدد "الفاتورة\EnclosedDocs‬".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="f0ccf-147">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-147">Click Add Element.</span></span>
22. <span data-ttu-id="f0ccf-148">في حقل "الاسم"، اكتب "المستند".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="f0ccf-149">مستند</span><span class="sxs-lookup"><span data-stu-id="f0ccf-149">Document</span></span>  
23. <span data-ttu-id="f0ccf-150">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-150">Click OK.</span></span>
24. <span data-ttu-id="f0ccf-151">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="f0ccf-152">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="f0ccf-153">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="f0ccf-154">في حقل "الاسم"، اكتب "FileName".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="f0ccf-155">FileName</span><span class="sxs-lookup"><span data-stu-id="f0ccf-155">FileName</span></span>  
28. <span data-ttu-id="f0ccf-156">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-156">Click OK.</span></span>
29. <span data-ttu-id="f0ccf-157">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="f0ccf-158">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="f0ccf-159">في حقل "الاسم"، اكتب "FileContent".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="f0ccf-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="f0ccf-160">FileContent</span></span>  
32. <span data-ttu-id="f0ccf-161">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-161">Click OK.</span></span>
33. <span data-ttu-id="f0ccf-162">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند\FileContent".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="f0ccf-163">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="f0ccf-164">في الشجرة، حدد "النص\Base64".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="f0ccf-165">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="f0ccf-166">تعيين عناصر التنسيق إلى نموذج بيانات كمصدر بيانات</span><span class="sxs-lookup"><span data-stu-id="f0ccf-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="f0ccf-167">في الشجرة، حدد "الفاتورة‬\SalesOrder‬".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="f0ccf-168">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="f0ccf-169">في الشجرة، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="f0ccf-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="f0ccf-170">في الشجرة، حدد "النموذج\رقم أمر المبيعات(SalesId)".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="f0ccf-171">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-171">Click Bind.</span></span>
6. <span data-ttu-id="f0ccf-172">في الشجرة، حدد "الفاتورة\InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="f0ccf-173">في الشجرة، قم بتوسيع "النموذج\الفاتورة الأساسية‬(InvoiceBase)".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="f0ccf-174">في الشجرة، حدد "النموذج\الفاتورة الأساسية(InvoiceBase)\رقم الفاتورة(Id)".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="f0ccf-175">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-175">Click Bind.</span></span>
10. <span data-ttu-id="f0ccf-176">في الشجرة، حدد "الفاتورة\InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="f0ccf-177">في الشجرة، حدد "النموذج\الفاتورة الأساسية(InvoiceBase)\مبلغ الفاتورة(المبلغ)".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="f0ccf-178">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-178">Click Bind.</span></span>
13. <span data-ttu-id="f0ccf-179">في الشجرة، قم بتوسيع "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="f0ccf-180">في الشجرة، حدد "النموذج\مرفقات الفاتورة\محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="f0ccf-181">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند\FileContent\Base64".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="f0ccf-182">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-182">Click Bind.</span></span>
17. <span data-ttu-id="f0ccf-183">في الشجرة، حدد "النموذج\مرفقات الفاتورة\اسم الملف‬".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="f0ccf-184">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند\FileName".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="f0ccf-185">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-185">Click Bind.</span></span>
20. <span data-ttu-id="f0ccf-186">في الشجرة، حدد "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="f0ccf-187">في الشجرة، حدد "الفاتورة\EnclosedDocs\المستند".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="f0ccf-188">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-188">Click Bind.</span></span>
23. <span data-ttu-id="f0ccf-189">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f0ccf-189">Click Save.</span></span>
24. <span data-ttu-id="f0ccf-190">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f0ccf-190">Close the page.</span></span>

