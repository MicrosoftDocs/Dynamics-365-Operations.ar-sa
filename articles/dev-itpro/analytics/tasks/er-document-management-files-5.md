--- 
title: "تعديل وتشغيل التنسيقات لاستخدام ملفات إدارة المستندات في مخرجات التقارير الإلكترونية"
description: "تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.openlocfilehash: 5effbecf98e633d07f9e5eb22d3df1a12967c1e4
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---
# <a name="modify-and-run-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="45353-103">تعديل وتشغيل التنسيقات لاستخدام ملفات إدارة المستندات في مخرجات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="45353-103">Modify and run formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="45353-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="45353-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="45353-105">يمكن تنفيذ هذه الخطوات في شركة DEMF.</span><span class="sxs-lookup"><span data-stu-id="45353-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="45353-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 4: تشغيل التنسيق)".</span><span class="sxs-lookup"><span data-stu-id="45353-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="45353-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="45353-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="45353-108">تعديل التنسيق لتعبئة المرفقات في الرسائل الناشئة بتنسيق ثنائي</span><span class="sxs-lookup"><span data-stu-id="45353-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="45353-109">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="45353-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="45353-110">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="45353-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="45353-111">في الشجرة، قم بتوسيع "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="45353-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="45353-112">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)/رسالة نموذج فاتورة إلكترونية."</span><span class="sxs-lookup"><span data-stu-id="45353-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="45353-113">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="45353-113">Click Designer.</span></span>
    * <span data-ttu-id="45353-114">ستقوم بتعبئة رسالة الفاتورة في الإخراج الناشئ كملف XML باستخدام ترميز UNICODE.</span><span class="sxs-lookup"><span data-stu-id="45353-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="45353-115">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="45353-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="45353-116">في الشجرة، حدد "Common\File".</span><span class="sxs-lookup"><span data-stu-id="45353-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="45353-117">في الحقل "الاسم"، اكتب "رسالة Xml".</span><span class="sxs-lookup"><span data-stu-id="45353-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="45353-118">رسالة Xml</span><span class="sxs-lookup"><span data-stu-id="45353-118">Xml message</span></span>  
9. <span data-ttu-id="45353-119">في الحقل"الترميز"، اكتب "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="45353-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="45353-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="45353-120">UTF-8</span></span>  
10. <span data-ttu-id="45353-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="45353-121">Click OK.</span></span>
    * <span data-ttu-id="45353-122">قم بتكوين الإخراج الناشئ كملف مضغوط.</span><span class="sxs-lookup"><span data-stu-id="45353-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="45353-123">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="45353-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="45353-124">في الشجرة، حدد "عام\مجلد".</span><span class="sxs-lookup"><span data-stu-id="45353-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="45353-125">في الحقل "الاسم"، اكتب "إخراج ملف Zip".</span><span class="sxs-lookup"><span data-stu-id="45353-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="45353-126">إخراج ملف Zip</span><span class="sxs-lookup"><span data-stu-id="45353-126">Zip output</span></span>  
14. <span data-ttu-id="45353-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="45353-127">Click OK.</span></span>
15. <span data-ttu-id="45353-128">في الشجرة، حدد "إخراج ملف Zip".</span><span class="sxs-lookup"><span data-stu-id="45353-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="45353-129">أضف المرفقات إلى الملف المضغوط الناشئ كالملفات ذات الأسماء والملحقات الأصلية.</span><span class="sxs-lookup"><span data-stu-id="45353-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="45353-130">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="45353-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="45353-131">في الشجرة، حدد "Common\File".</span><span class="sxs-lookup"><span data-stu-id="45353-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="45353-132">في حقل "الاسم"، اكتب "الملف المرفق".</span><span class="sxs-lookup"><span data-stu-id="45353-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="45353-133">الملف المرفق</span><span class="sxs-lookup"><span data-stu-id="45353-133">Attached file</span></span>  
19. <span data-ttu-id="45353-134">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="45353-134">Click OK.</span></span>
20. <span data-ttu-id="45353-135">في الشجرة، حدد "إخراج ملف Zip\ملف مرفق".</span><span class="sxs-lookup"><span data-stu-id="45353-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="45353-136">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="45353-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="45353-137">في الشجرة، حدد "النص\Base64".</span><span class="sxs-lookup"><span data-stu-id="45353-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="45353-138">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="45353-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="45353-139">تعيين عناصر التنسيق الجديد إلى نموذج بيانات</span><span class="sxs-lookup"><span data-stu-id="45353-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="45353-140">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="45353-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="45353-141">في الشجرة ، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="45353-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="45353-142">في الشجرة، قم بتوسيع "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="45353-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="45353-143">في الشجرة، حدد "إخراج ملف Zip\ملف مرفق\Base64".</span><span class="sxs-lookup"><span data-stu-id="45353-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="45353-144">في الشجرة، حدد "النموذج\مرفقات الفاتورة\محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="45353-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="45353-145">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="45353-145">Click Bind.</span></span>
7. <span data-ttu-id="45353-146">في الشجرة، حدد "إخراج ملف Zip\ملف مرفق".</span><span class="sxs-lookup"><span data-stu-id="45353-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="45353-147">انقر فوق "تحرير اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="45353-147">Click Edit filename.</span></span>
9. <span data-ttu-id="45353-148">في الشجرة، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="45353-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="45353-149">في الشجرة، قم بتوسيع "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="45353-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="45353-150">في الشجرة، حدد "النموذج\مرفقات الفاتورة\اسم الملف‬".</span><span class="sxs-lookup"><span data-stu-id="45353-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="45353-151">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="45353-151">Click Add data source.</span></span>
13. <span data-ttu-id="45353-152">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="45353-152">Click Save.</span></span>
14. <span data-ttu-id="45353-153">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="45353-153">Close the page.</span></span>
15. <span data-ttu-id="45353-154">في الشجرة، حدد "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="45353-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="45353-155">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="45353-155">Click Bind.</span></span>
17. <span data-ttu-id="45353-156">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="45353-156">Click Save.</span></span>
18. <span data-ttu-id="45353-157">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="45353-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="45353-158">تشغيل التقرير المصمم للفاتورة المحددة</span><span class="sxs-lookup"><span data-stu-id="45353-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="45353-159">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="45353-159">Click Run.</span></span>
2. <span data-ttu-id="45353-160">وسّع المقطع "السجلات المطلوب تضمينها‬ ()".</span><span class="sxs-lookup"><span data-stu-id="45353-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="45353-161">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="45353-161">Click Filter.</span></span>
4. <span data-ttu-id="45353-162">حدد الصف لحقل دفتر يومية فاتورة العميل وأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="45353-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="45353-163">في حقل المعايير"، في حقل "أمر المبيعات" للمعايير، اكتب رقم الأمر 000148.</span><span class="sxs-lookup"><span data-stu-id="45353-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="45353-164">000148</span><span class="sxs-lookup"><span data-stu-id="45353-164">000148</span></span>  
6. <span data-ttu-id="45353-165">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="45353-165">Click OK.</span></span>
7. <span data-ttu-id="45353-166">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="45353-166">Click OK.</span></span>
    * <span data-ttu-id="45353-167">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="45353-167">Review the generated output.</span></span> <span data-ttu-id="45353-168">لاحظ أنه تم إنشاء ملف واحد لكل مرفق، بالإضافة إلى رسالة الفاتورة بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="45353-168">Note, in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="45353-169">تتم تعبئة ملفات المرفقات بالإخراج المضغوط بتنسيق ثنائي.</span><span class="sxs-lookup"><span data-stu-id="45353-169">The attachment files are populated with the zipped output in binary format.</span></span>  


