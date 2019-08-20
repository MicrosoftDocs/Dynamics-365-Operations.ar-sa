---
title: التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 5 - تعديل التنسيق وتشغيله)
description: تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba9cc4dcdfcfbc1bdb933336e85da9b4b6d97a40
ms.sourcegitcommit: f5556189a80ad9f23f1af3333837eae034ddb247
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/29/2019
ms.locfileid: "1791846"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5-modify-and-run-format"></a><span data-ttu-id="c7538-103">التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 5: تعديل التنسيق وتشغيله)</span><span class="sxs-lookup"><span data-stu-id="c7538-103">ER Use Document Management files in format outputs (Part 5: Modify and run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c7538-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c7538-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="c7538-105">يمكن تنفيذ هذه الخطوات في شركة DEMF.</span><span class="sxs-lookup"><span data-stu-id="c7538-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="c7538-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 4: تشغيل التنسيق)".</span><span class="sxs-lookup"><span data-stu-id="c7538-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4: Run format)” procedure.</span></span>

<span data-ttu-id="c7538-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="c7538-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="c7538-108">تعديل التنسيق لتعبئة المرفقات في الرسائل الناشئة بتنسيق ثنائي</span><span class="sxs-lookup"><span data-stu-id="c7538-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="c7538-109">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="c7538-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c7538-110">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="c7538-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="c7538-111">في الشجرة، قم بتوسيع "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="c7538-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="c7538-112">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)/رسالة نموذج فاتورة إلكترونية."</span><span class="sxs-lookup"><span data-stu-id="c7538-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="c7538-113">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="c7538-113">Click Designer.</span></span>
    * <span data-ttu-id="c7538-114">ستقوم بتعبئة رسالة الفاتورة في الإخراج الناشئ كملف XML باستخدام ترميز UNICODE.</span><span class="sxs-lookup"><span data-stu-id="c7538-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="c7538-115">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c7538-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="c7538-116">في الشجرة، حدد "Common\File".</span><span class="sxs-lookup"><span data-stu-id="c7538-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="c7538-117">في الحقل "الاسم"، اكتب "رسالة Xml".</span><span class="sxs-lookup"><span data-stu-id="c7538-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="c7538-118">رسالة Xml</span><span class="sxs-lookup"><span data-stu-id="c7538-118">Xml message</span></span>  
9. <span data-ttu-id="c7538-119">في الحقل"الترميز"، اكتب "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="c7538-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="c7538-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="c7538-120">UTF-8</span></span>  
10. <span data-ttu-id="c7538-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c7538-121">Click OK.</span></span>
    * <span data-ttu-id="c7538-122">قم بتكوين الإخراج الناشئ كملف مضغوط.</span><span class="sxs-lookup"><span data-stu-id="c7538-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="c7538-123">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c7538-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="c7538-124">في الشجرة، حدد "عام\مجلد".</span><span class="sxs-lookup"><span data-stu-id="c7538-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="c7538-125">في الحقل "الاسم"، اكتب "إخراج ملف Zip".</span><span class="sxs-lookup"><span data-stu-id="c7538-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="c7538-126">إخراج ملف Zip</span><span class="sxs-lookup"><span data-stu-id="c7538-126">Zip output</span></span>  
14. <span data-ttu-id="c7538-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c7538-127">Click OK.</span></span>
15. <span data-ttu-id="c7538-128">في الشجرة، حدد "إخراج ملف Zip".</span><span class="sxs-lookup"><span data-stu-id="c7538-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="c7538-129">أضف المرفقات إلى الملف المضغوط الناشئ كالملفات ذات الأسماء والملحقات الأصلية.</span><span class="sxs-lookup"><span data-stu-id="c7538-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="c7538-130">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c7538-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="c7538-131">في الشجرة، حدد "Common\File".</span><span class="sxs-lookup"><span data-stu-id="c7538-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="c7538-132">في حقل "الاسم"، اكتب "الملف المرفق".</span><span class="sxs-lookup"><span data-stu-id="c7538-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="c7538-133">الملف المرفق</span><span class="sxs-lookup"><span data-stu-id="c7538-133">Attached file</span></span>  
19. <span data-ttu-id="c7538-134">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c7538-134">Click OK.</span></span>
20. <span data-ttu-id="c7538-135">في الشجرة، حدد "إخراج ملف Zip\ملف مرفق".</span><span class="sxs-lookup"><span data-stu-id="c7538-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="c7538-136">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c7538-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="c7538-137">في الشجرة، حدد "النص\Base64".</span><span class="sxs-lookup"><span data-stu-id="c7538-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="c7538-138">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c7538-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="c7538-139">تعيين عناصر التنسيق الجديد إلى نموذج بيانات</span><span class="sxs-lookup"><span data-stu-id="c7538-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="c7538-140">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="c7538-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="c7538-141">في الشجرة، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="c7538-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="c7538-142">في الشجرة، قم بتوسيع "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="c7538-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="c7538-143">في الشجرة، حدد "إخراج ملف Zip\ملف مرفق\Base64".</span><span class="sxs-lookup"><span data-stu-id="c7538-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="c7538-144">في الشجرة، حدد "النموذج\مرفقات الفاتورة\محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="c7538-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="c7538-145">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="c7538-145">Click Bind.</span></span>
7. <span data-ttu-id="c7538-146">في الشجرة، حدد "إخراج ملف Zip\ملف مرفق".</span><span class="sxs-lookup"><span data-stu-id="c7538-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="c7538-147">انقر فوق "تحرير اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="c7538-147">Click Edit filename.</span></span>
9. <span data-ttu-id="c7538-148">في الشجرة، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="c7538-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="c7538-149">في الشجرة، قم بتوسيع "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="c7538-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="c7538-150">في الشجرة، حدد "النموذج\مرفقات الفاتورة\اسم الملف‬".</span><span class="sxs-lookup"><span data-stu-id="c7538-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="c7538-151">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="c7538-151">Click Add data source.</span></span>
13. <span data-ttu-id="c7538-152">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="c7538-152">Click Save.</span></span>
14. <span data-ttu-id="c7538-153">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c7538-153">Close the page.</span></span>
15. <span data-ttu-id="c7538-154">في الشجرة، حدد "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="c7538-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="c7538-155">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="c7538-155">Click Bind.</span></span>
17. <span data-ttu-id="c7538-156">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c7538-156">Click Save.</span></span>
18. <span data-ttu-id="c7538-157">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c7538-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="c7538-158">تشغيل التقرير المصمم للفاتورة المحددة</span><span class="sxs-lookup"><span data-stu-id="c7538-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="c7538-159">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="c7538-159">Click Run.</span></span>
2. <span data-ttu-id="c7538-160">وسّع المقطع "السجلات المطلوب تضمينها‬ ()".</span><span class="sxs-lookup"><span data-stu-id="c7538-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="c7538-161">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="c7538-161">Click Filter.</span></span>
4. <span data-ttu-id="c7538-162">حدد الصف لحقل دفتر يومية فاتورة العميل وأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c7538-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="c7538-163">في حقل المعايير"، في حقل "أمر المبيعات" للمعايير، اكتب رقم الأمر 000148.</span><span class="sxs-lookup"><span data-stu-id="c7538-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="c7538-164">000148</span><span class="sxs-lookup"><span data-stu-id="c7538-164">000148</span></span>  
6. <span data-ttu-id="c7538-165">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c7538-165">Click OK.</span></span>
7. <span data-ttu-id="c7538-166">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c7538-166">Click OK.</span></span>
    * <span data-ttu-id="c7538-167">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="c7538-167">Review the generated output.</span></span> <span data-ttu-id="c7538-168">لاحظ أنه تم إنشاء ملف واحد لكل مرفق، بالإضافة إلى رسالة الفاتورة بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="c7538-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="c7538-169">تتم تعبئة ملفات المرفقات بالإخراج المضغوط بتنسيق ثنائي.</span><span class="sxs-lookup"><span data-stu-id="c7538-169">The attachment files are populated with the zipped output in binary format.</span></span>  

