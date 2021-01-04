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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b949c2629df0e9db8c11322c9d0d090b200edc2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681747"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="27c58-103">التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 5 - تعديل التنسيق وتشغيله)</span><span class="sxs-lookup"><span data-stu-id="27c58-103">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27c58-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="27c58-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="27c58-105">يمكن تنفيذ هذه الخطوات في شركة DEMF.</span><span class="sxs-lookup"><span data-stu-id="27c58-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="27c58-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 4: تشغيل التنسيق)".</span><span class="sxs-lookup"><span data-stu-id="27c58-106">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="27c58-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="27c58-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="27c58-108">تعديل التنسيق لتعبئة المرفقات في الرسائل الناشئة بتنسيق ثنائي</span><span class="sxs-lookup"><span data-stu-id="27c58-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="27c58-109">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="27c58-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="27c58-110">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="27c58-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="27c58-111">في الشجرة، قم بتوسيع "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="27c58-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="27c58-112">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)/رسالة نموذج فاتورة إلكترونية."</span><span class="sxs-lookup"><span data-stu-id="27c58-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="27c58-113">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="27c58-113">Click Designer.</span></span>
    * <span data-ttu-id="27c58-114">ستقوم بتعبئة رسالة الفاتورة في الإخراج الناشئ كملف XML باستخدام ترميز UNICODE.</span><span class="sxs-lookup"><span data-stu-id="27c58-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="27c58-115">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="27c58-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="27c58-116">في الشجرة، حدد "Common\File".</span><span class="sxs-lookup"><span data-stu-id="27c58-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="27c58-117">في الحقل "الاسم"، اكتب "رسالة Xml".</span><span class="sxs-lookup"><span data-stu-id="27c58-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="27c58-118">رسالة Xml</span><span class="sxs-lookup"><span data-stu-id="27c58-118">Xml message</span></span>  
9. <span data-ttu-id="27c58-119">في الحقل"الترميز"، اكتب "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="27c58-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="27c58-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="27c58-120">UTF-8</span></span>  
10. <span data-ttu-id="27c58-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="27c58-121">Click OK.</span></span>
    * <span data-ttu-id="27c58-122">قم بتكوين الإخراج الناشئ كملف مضغوط.</span><span class="sxs-lookup"><span data-stu-id="27c58-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="27c58-123">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="27c58-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="27c58-124">في الشجرة، حدد "عام\مجلد".</span><span class="sxs-lookup"><span data-stu-id="27c58-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="27c58-125">في الحقل "الاسم"، اكتب "إخراج ملف Zip".</span><span class="sxs-lookup"><span data-stu-id="27c58-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="27c58-126">إخراج ملف Zip</span><span class="sxs-lookup"><span data-stu-id="27c58-126">Zip output</span></span>  
14. <span data-ttu-id="27c58-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="27c58-127">Click OK.</span></span>
15. <span data-ttu-id="27c58-128">في الشجرة، حدد "إخراج ملف Zip".</span><span class="sxs-lookup"><span data-stu-id="27c58-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="27c58-129">أضف المرفقات إلى الملف المضغوط الناشئ كالملفات ذات الأسماء والملحقات الأصلية.</span><span class="sxs-lookup"><span data-stu-id="27c58-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="27c58-130">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="27c58-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="27c58-131">في الشجرة، حدد "Common\File".</span><span class="sxs-lookup"><span data-stu-id="27c58-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="27c58-132">في حقل "الاسم"، اكتب "الملف المرفق".</span><span class="sxs-lookup"><span data-stu-id="27c58-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="27c58-133">الملف المرفق</span><span class="sxs-lookup"><span data-stu-id="27c58-133">Attached file</span></span>  
19. <span data-ttu-id="27c58-134">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="27c58-134">Click OK.</span></span>
20. <span data-ttu-id="27c58-135">في الشجرة، حدد "إخراج ملف Zip\ملف مرفق".</span><span class="sxs-lookup"><span data-stu-id="27c58-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="27c58-136">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="27c58-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="27c58-137">في الشجرة، حدد "النص\Base64".</span><span class="sxs-lookup"><span data-stu-id="27c58-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="27c58-138">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="27c58-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="27c58-139">تعيين عناصر التنسيق الجديد إلى نموذج بيانات</span><span class="sxs-lookup"><span data-stu-id="27c58-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="27c58-140">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="27c58-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="27c58-141">في الشجرة، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="27c58-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="27c58-142">في الشجرة، قم بتوسيع "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="27c58-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="27c58-143">في الشجرة، حدد "إخراج ملف Zip\ملف مرفق\Base64".</span><span class="sxs-lookup"><span data-stu-id="27c58-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="27c58-144">في الشجرة، حدد "النموذج\مرفقات الفاتورة\محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="27c58-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="27c58-145">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="27c58-145">Click Bind.</span></span>
7. <span data-ttu-id="27c58-146">في الشجرة، حدد "إخراج ملف Zip\ملف مرفق".</span><span class="sxs-lookup"><span data-stu-id="27c58-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="27c58-147">انقر فوق "تحرير اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="27c58-147">Click Edit filename.</span></span>
9. <span data-ttu-id="27c58-148">في الشجرة، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="27c58-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="27c58-149">في الشجرة، قم بتوسيع "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="27c58-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="27c58-150">في الشجرة، حدد "النموذج\مرفقات الفاتورة\اسم الملف‬".</span><span class="sxs-lookup"><span data-stu-id="27c58-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="27c58-151">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="27c58-151">Click Add data source.</span></span>
13. <span data-ttu-id="27c58-152">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="27c58-152">Click Save.</span></span>
14. <span data-ttu-id="27c58-153">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="27c58-153">Close the page.</span></span>
15. <span data-ttu-id="27c58-154">في الشجرة، حدد "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="27c58-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="27c58-155">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="27c58-155">Click Bind.</span></span>
17. <span data-ttu-id="27c58-156">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="27c58-156">Click Save.</span></span>
18. <span data-ttu-id="27c58-157">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="27c58-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="27c58-158">تشغيل التقرير المصمم للفاتورة المحددة</span><span class="sxs-lookup"><span data-stu-id="27c58-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="27c58-159">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="27c58-159">Click Run.</span></span>
2. <span data-ttu-id="27c58-160">وسّع المقطع "السجلات المطلوب تضمينها‬ ()".</span><span class="sxs-lookup"><span data-stu-id="27c58-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="27c58-161">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="27c58-161">Click Filter.</span></span>
4. <span data-ttu-id="27c58-162">حدد الصف لحقل دفتر يومية فاتورة العميل وأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="27c58-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="27c58-163">في حقل المعايير"، في حقل "أمر المبيعات" للمعايير، اكتب رقم الأمر 000148.</span><span class="sxs-lookup"><span data-stu-id="27c58-163">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="27c58-164">000148</span><span class="sxs-lookup"><span data-stu-id="27c58-164">000148</span></span>  
6. <span data-ttu-id="27c58-165">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="27c58-165">Click OK.</span></span>
7. <span data-ttu-id="27c58-166">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="27c58-166">Click OK.</span></span>
    * <span data-ttu-id="27c58-167">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="27c58-167">Review the generated output.</span></span> <span data-ttu-id="27c58-168">لاحظ أنه تم إنشاء ملف واحد لكل مرفق، بالإضافة إلى رسالة الفاتورة بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="27c58-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="27c58-169">تتم تعبئة ملفات المرفقات بالإخراج المضغوط بتنسيق ثنائي.</span><span class="sxs-lookup"><span data-stu-id="27c58-169">The attachment files are populated with the zipped output in binary format.</span></span>  

