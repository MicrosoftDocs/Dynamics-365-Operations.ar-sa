---
title: التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 5 - تعديل التنسيق وتشغيله)
description: يوضح هذا الموضوع كيفيه تكوين تنسيق التقارير الكترونيه (ER) لاستخدام ملفات أداره المستندات (المرفقات) في إخراج ER. (جزء 5)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6062945dfea0eec02e5055e9ebe697189267e051
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564800"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="9a792-104">التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 5 - تعديل التنسيق وتشغيله)</span><span class="sxs-lookup"><span data-stu-id="9a792-104">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9a792-105">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9a792-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="9a792-106">يمكن تنفيذ هذه الخطوات في شركة DEMF.</span><span class="sxs-lookup"><span data-stu-id="9a792-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="9a792-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 4: تشغيل التنسيق)".</span><span class="sxs-lookup"><span data-stu-id="9a792-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="9a792-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="9a792-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="9a792-109">تعديل التنسيق لتعبئة المرفقات في الرسائل الناشئة بتنسيق ثنائي</span><span class="sxs-lookup"><span data-stu-id="9a792-109">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="9a792-110">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="9a792-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9a792-111">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="9a792-111">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="9a792-112">في الشجرة، قم بتوسيع "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="9a792-112">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="9a792-113">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)/رسالة نموذج فاتورة إلكترونية."</span><span class="sxs-lookup"><span data-stu-id="9a792-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="9a792-114">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="9a792-114">Click Designer.</span></span>
    * <span data-ttu-id="9a792-115">ستقوم بتعبئة رسالة الفاتورة في الإخراج الناشئ كملف XML باستخدام ترميز UNICODE.</span><span class="sxs-lookup"><span data-stu-id="9a792-115">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="9a792-116">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9a792-116">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="9a792-117">في الشجرة، حدد "Common\File".</span><span class="sxs-lookup"><span data-stu-id="9a792-117">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="9a792-118">في الحقل "الاسم"، اكتب "رسالة Xml".</span><span class="sxs-lookup"><span data-stu-id="9a792-118">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="9a792-119">رسالة Xml</span><span class="sxs-lookup"><span data-stu-id="9a792-119">Xml message</span></span>  
9. <span data-ttu-id="9a792-120">في الحقل"الترميز"، اكتب "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="9a792-120">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="9a792-121">UTF-8</span><span class="sxs-lookup"><span data-stu-id="9a792-121">UTF-8</span></span>  
10. <span data-ttu-id="9a792-122">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9a792-122">Click OK.</span></span>
    * <span data-ttu-id="9a792-123">قم بتكوين الإخراج الناشئ كملف مضغوط.</span><span class="sxs-lookup"><span data-stu-id="9a792-123">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="9a792-124">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9a792-124">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="9a792-125">في الشجرة، حدد "عام\مجلد".</span><span class="sxs-lookup"><span data-stu-id="9a792-125">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="9a792-126">في الحقل "الاسم"، اكتب "إخراج ملف Zip".</span><span class="sxs-lookup"><span data-stu-id="9a792-126">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="9a792-127">إخراج ملف Zip</span><span class="sxs-lookup"><span data-stu-id="9a792-127">Zip output</span></span>  
14. <span data-ttu-id="9a792-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9a792-128">Click OK.</span></span>
15. <span data-ttu-id="9a792-129">في الشجرة، حدد "إخراج ملف Zip".</span><span class="sxs-lookup"><span data-stu-id="9a792-129">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="9a792-130">أضف المرفقات إلى الملف المضغوط الناشئ كالملفات ذات الأسماء والملحقات الأصلية.</span><span class="sxs-lookup"><span data-stu-id="9a792-130">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="9a792-131">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9a792-131">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="9a792-132">في الشجرة، حدد "Common\File".</span><span class="sxs-lookup"><span data-stu-id="9a792-132">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="9a792-133">في حقل "الاسم"، اكتب "الملف المرفق".</span><span class="sxs-lookup"><span data-stu-id="9a792-133">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="9a792-134">الملف المرفق</span><span class="sxs-lookup"><span data-stu-id="9a792-134">Attached file</span></span>  
19. <span data-ttu-id="9a792-135">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9a792-135">Click OK.</span></span>
20. <span data-ttu-id="9a792-136">في الشجرة، حدد "إخراج ملف Zip\ملف مرفق".</span><span class="sxs-lookup"><span data-stu-id="9a792-136">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="9a792-137">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9a792-137">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="9a792-138">في الشجرة، حدد "النص\Base64".</span><span class="sxs-lookup"><span data-stu-id="9a792-138">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="9a792-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9a792-139">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="9a792-140">تعيين عناصر التنسيق الجديد إلى نموذج بيانات</span><span class="sxs-lookup"><span data-stu-id="9a792-140">Map new format elements to data model</span></span>
1. <span data-ttu-id="9a792-141">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="9a792-141">Click the Mapping tab.</span></span>
2. <span data-ttu-id="9a792-142">في الشجرة، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="9a792-142">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="9a792-143">في الشجرة، قم بتوسيع "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="9a792-143">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="9a792-144">في الشجرة، حدد "إخراج ملف Zip\ملف مرفق\Base64".</span><span class="sxs-lookup"><span data-stu-id="9a792-144">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="9a792-145">في الشجرة، حدد "النموذج\مرفقات الفاتورة\محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="9a792-145">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="9a792-146">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="9a792-146">Click Bind.</span></span>
7. <span data-ttu-id="9a792-147">في الشجرة، حدد "إخراج ملف Zip\ملف مرفق".</span><span class="sxs-lookup"><span data-stu-id="9a792-147">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="9a792-148">انقر فوق "تحرير اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="9a792-148">Click Edit filename.</span></span>
9. <span data-ttu-id="9a792-149">في الشجرة، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="9a792-149">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="9a792-150">في الشجرة، قم بتوسيع "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="9a792-150">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="9a792-151">في الشجرة، حدد "النموذج\مرفقات الفاتورة\اسم الملف‬".</span><span class="sxs-lookup"><span data-stu-id="9a792-151">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="9a792-152">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="9a792-152">Click Add data source.</span></span>
13. <span data-ttu-id="9a792-153">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="9a792-153">Click Save.</span></span>
14. <span data-ttu-id="9a792-154">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9a792-154">Close the page.</span></span>
15. <span data-ttu-id="9a792-155">في الشجرة، حدد "النموذج\مرفقات الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="9a792-155">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="9a792-156">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="9a792-156">Click Bind.</span></span>
17. <span data-ttu-id="9a792-157">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9a792-157">Click Save.</span></span>
18. <span data-ttu-id="9a792-158">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9a792-158">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="9a792-159">تشغيل التقرير المصمم للفاتورة المحددة</span><span class="sxs-lookup"><span data-stu-id="9a792-159">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="9a792-160">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="9a792-160">Click Run.</span></span>
2. <span data-ttu-id="9a792-161">وسّع المقطع "السجلات المطلوب تضمينها‬ ()".</span><span class="sxs-lookup"><span data-stu-id="9a792-161">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="9a792-162">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="9a792-162">Click Filter.</span></span>
4. <span data-ttu-id="9a792-163">حدد الصف لحقل دفتر يومية فاتورة العميل وأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="9a792-163">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="9a792-164">في حقل المعايير"، في حقل "أمر المبيعات" للمعايير، اكتب رقم الأمر 000148.</span><span class="sxs-lookup"><span data-stu-id="9a792-164">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="9a792-165">000148</span><span class="sxs-lookup"><span data-stu-id="9a792-165">000148</span></span>  
6. <span data-ttu-id="9a792-166">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="9a792-166">Click OK.</span></span>
7. <span data-ttu-id="9a792-167">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="9a792-167">Click OK.</span></span>
    * <span data-ttu-id="9a792-168">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="9a792-168">Review the generated output.</span></span> <span data-ttu-id="9a792-169">لاحظ أنه تم إنشاء ملف واحد لكل مرفق، بالإضافة إلى رسالة الفاتورة بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="9a792-169">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="9a792-170">تتم تعبئة ملفات المرفقات بالإخراج المضغوط بتنسيق ثنائي.</span><span class="sxs-lookup"><span data-stu-id="9a792-170">The attachment files are populated with the zipped output in binary format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]