---
title: التقارير الإلكترونية - استخدام النطاقات القابلة للتوسيع أفقيًا لإضافة الأعمدة بشكل حيوي في تقارير Excel (الجزء 1 - تصميم التنسيق)
description: يوضح هذا الموضوع كيفيه تكوين تنسيق اعداد التقارير الكترونيه (ER) لإنشاء تقارير كملفات أوبينكسمل (Excel). (جزء 1)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9eef9ffaadbd7010129cc9850ded1ba67bc281d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745001"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a><span data-ttu-id="63d59-104">التقارير الإلكترونية - استخدام النطاقات القابلة للتوسيع أفقيًا لإضافة الأعمدة بشكل حيوي في تقارير Excel (الجزء 1 - تصميم التنسيق)</span><span class="sxs-lookup"><span data-stu-id="63d59-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1 - Design format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="63d59-105">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق التقارير الإلكترونية لإنشاء التقارير كملفات أوراق عمل (Excel) تنسيق OPENXML حيث يمكن إنشاء الأعمدة المطلوبة بطريقة ديناميكية كنطاقات قابلة للتوسيع أفقيًا.</span><span class="sxs-lookup"><span data-stu-id="63d59-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="63d59-106">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="63d59-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="63d59-107">لإكمال هذه الخطوات، يجب عليك أولاً إكمال خطوط دلائل المهام الثلاث التالية:</span><span class="sxs-lookup"><span data-stu-id="63d59-107">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="63d59-108">"التقارير الإلكترونية- إنشاء موفر تكوين ووضع علامة عليه على أنه نشط"</span><span class="sxs-lookup"><span data-stu-id="63d59-108">"ER Create a configuration provider and mark it as active"</span></span>

<span data-ttu-id="63d59-109">"التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 1 - تصميم نموذج البيانات):</span><span class="sxs-lookup"><span data-stu-id="63d59-109">"ER Use financial dimensions as a data source (Part 1: Design data model)"</span></span>

<span data-ttu-id="63d59-110">"التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 2 - تعيين النموذج)"</span><span class="sxs-lookup"><span data-stu-id="63d59-110">"ER Use financial dimensions as a data source (Part 2: Model mapping)"</span></span>

<span data-ttu-id="63d59-111">يجب أيضًا تنزيل نسخة محلية من القالب وحفظها مع نموذج التقرير الموجود هنا، [عينة تقرير خدمة ويب للأبعاد المالية](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="63d59-111">You must also download and save a local copy of the template with a sample report found here, [Sample Financial Dimensions Web Service Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>

<span data-ttu-id="63d59-112">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="63d59-112">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="63d59-113">إنشاء تكوين تقرير جديد</span><span class="sxs-lookup"><span data-stu-id="63d59-113">Create a new report configuration</span></span>
1. <span data-ttu-id="63d59-114">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="63d59-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="63d59-115">في الشجرة، حدد "نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="63d59-115">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="63d59-116">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="63d59-116">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="63d59-117">في الحقل "جديد"، أدخل "التنسيق المستند إلى نموذج البيانات نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="63d59-117">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="63d59-118">استخدم النموذج الذي تم إنشاؤه مسبقًا كمصدر بيانات للتقرير الجديد.</span><span class="sxs-lookup"><span data-stu-id="63d59-118">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="63d59-119">في حقل "الاسم"، اكتب "نموذج تقرير مع نطاقات قابلة للتوسيع أفقيًا".</span><span class="sxs-lookup"><span data-stu-id="63d59-119">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="63d59-120">نموذج تقرير مع نطاقات قابلة للتوسيع أفقيًا</span><span class="sxs-lookup"><span data-stu-id="63d59-120">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="63d59-121">في حقل "الوصف"، اكتب "لإنشاء مخرجات Excel من خلال إضافة الأعمدة بشكل حيوي‬".</span><span class="sxs-lookup"><span data-stu-id="63d59-121">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="63d59-122">لإنشاء مخرجات Excel من خلال إضافة الأعمدة بشكل حيوي</span><span class="sxs-lookup"><span data-stu-id="63d59-122">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="63d59-123">في الحقل "تعريف نموذج البيانات"، حدد "الإدخال".</span><span class="sxs-lookup"><span data-stu-id="63d59-123">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="63d59-124">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="63d59-124">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="63d59-125">تصميم تنسيق التقرير</span><span class="sxs-lookup"><span data-stu-id="63d59-125">Design the report format</span></span>
1. <span data-ttu-id="63d59-126">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="63d59-126">Click Designer.</span></span>
2. <span data-ttu-id="63d59-127">قم بتشغيل زر التبديل "إظهار التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="63d59-127">Turn on the 'Show details' toggle button.</span></span>
3. <span data-ttu-id="63d59-128">في جزء الإجراءات، انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="63d59-128">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="63d59-129">انقر فوق استيراد من "Excel".</span><span class="sxs-lookup"><span data-stu-id="63d59-129">Click Import from Excel.</span></span>
5. <span data-ttu-id="63d59-130">انقر فوق "المرفقات".</span><span class="sxs-lookup"><span data-stu-id="63d59-130">Click Attachments.</span></span>
    * <span data-ttu-id="63d59-131">استورد قالب التقرير.</span><span class="sxs-lookup"><span data-stu-id="63d59-131">Import the report's template.</span></span> <span data-ttu-id="63d59-132">استخدم ملف Excel الذي قمت بتحميله لذلك.</span><span class="sxs-lookup"><span data-stu-id="63d59-132">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="63d59-133">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="63d59-133">Click New.</span></span>
7. <span data-ttu-id="63d59-134">انقر فوق "ملف".</span><span class="sxs-lookup"><span data-stu-id="63d59-134">Click File.</span></span>
8. <span data-ttu-id="63d59-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="63d59-135">Close the page.</span></span>
9. <span data-ttu-id="63d59-136">في حقل "القالب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="63d59-136">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="63d59-137">حدد القالب الذي تم تنزيله.</span><span class="sxs-lookup"><span data-stu-id="63d59-137">Select the downloaded template.</span></span>  
10. <span data-ttu-id="63d59-138">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="63d59-138">Click OK.</span></span>
    * <span data-ttu-id="63d59-139">أضف مجموعة جديدة لإنشاء مخرجات Excel بطريقة ديناميكية باستخدام العدد الذي حددته من الأعمدة (في نموذج حوار المستخدم) للأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="63d59-139">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="63d59-140">ستمثل كل خلية لكل عمود اسم بُعد مالي واحد.</span><span class="sxs-lookup"><span data-stu-id="63d59-140">Each cell for every column will represent a single financial dimension's name.</span></span>  
11. <span data-ttu-id="63d59-141">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="63d59-141">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="63d59-142">في الشجرة، حدد "Excel\نطاق".</span><span class="sxs-lookup"><span data-stu-id="63d59-142">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="63d59-143">في الحقل "نطاق Excel"، اكتب "DimNames".</span><span class="sxs-lookup"><span data-stu-id="63d59-143">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="63d59-144">DimNames</span><span class="sxs-lookup"><span data-stu-id="63d59-144">DimNames</span></span>  
14. <span data-ttu-id="63d59-145">في الحقل "اتجاه النسخ المتماثل"، حدد "أفقي".</span><span class="sxs-lookup"><span data-stu-id="63d59-145">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="63d59-146">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="63d59-146">Click OK.</span></span>
16. <span data-ttu-id="63d59-147">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<DimNames>: أفقي".</span><span class="sxs-lookup"><span data-stu-id="63d59-147">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="63d59-148">انقر فوق "تحريك لأعلى".</span><span class="sxs-lookup"><span data-stu-id="63d59-148">Click Move up.</span></span>
18. <span data-ttu-id="63d59-149">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\خلية<DimNames>".</span><span class="sxs-lookup"><span data-stu-id="63d59-149">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="63d59-150">انقر فوق "قص".</span><span class="sxs-lookup"><span data-stu-id="63d59-150">Click Cut.</span></span>
20. <span data-ttu-id="63d59-151">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<DimNames>: أفقي".</span><span class="sxs-lookup"><span data-stu-id="63d59-151">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="63d59-152">انقر فوق "لصق".</span><span class="sxs-lookup"><span data-stu-id="63d59-152">Click Paste.</span></span>
22. <span data-ttu-id="63d59-153">في الشجرة، قم بتوسيع "Excel = "SampleFinDimWsReport"\نطاق<DimNames>: أفقي".</span><span class="sxs-lookup"><span data-stu-id="63d59-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="63d59-154">في الشجرة، قم بتوسيع "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي".</span><span class="sxs-lookup"><span data-stu-id="63d59-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="63d59-155">في الشجرة، قم بتوسيع "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي".</span><span class="sxs-lookup"><span data-stu-id="63d59-155">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="63d59-156">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي".</span><span class="sxs-lookup"><span data-stu-id="63d59-156">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="63d59-157">أضف مجموعة جديدة لإنشاء مخرجات Excel بطريقة ديناميكية باستخدام العدد الذي حددته من الأعمدة (في نموذج حوار المستخدم) للأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="63d59-157">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="63d59-158">ستمثل كل خلية لكل عمود قيمة بُعد مالي واحدة لكل حركة تقرير.</span><span class="sxs-lookup"><span data-stu-id="63d59-158">Each cell for every column will represent a single financial dimension's value for each reporting transaction.</span></span>  
26. <span data-ttu-id="63d59-159">انقر فوق "إضافة نطاق".</span><span class="sxs-lookup"><span data-stu-id="63d59-159">Click Add Range.</span></span>
27. <span data-ttu-id="63d59-160">في الحقل "نطاق Excel"، اكتب "DimValues".</span><span class="sxs-lookup"><span data-stu-id="63d59-160">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="63d59-161">DimValues</span><span class="sxs-lookup"><span data-stu-id="63d59-161">DimValues</span></span>  
28. <span data-ttu-id="63d59-162">في الحقل "اتجاه النسخ المتماثل"، حدد "أفقي".</span><span class="sxs-lookup"><span data-stu-id="63d59-162">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="63d59-163">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="63d59-163">Click OK.</span></span>
30. <span data-ttu-id="63d59-164">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\خلية<DimValues>".</span><span class="sxs-lookup"><span data-stu-id="63d59-164">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="63d59-165">انقر فوق "قص".</span><span class="sxs-lookup"><span data-stu-id="63d59-165">Click Cut.</span></span>
32. <span data-ttu-id="63d59-166">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق‏‎<JournalLine>: عمودي\نطاق‏‎<TransactionLine>: عمودي\نطاق<DimValues>: أفقي".</span><span class="sxs-lookup"><span data-stu-id="63d59-166">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="63d59-167">انقر فوق "لصق".</span><span class="sxs-lookup"><span data-stu-id="63d59-167">Click Paste.</span></span>
34. <span data-ttu-id="63d59-168">في الشجرة، قم بتوسيع "Excel = "SampleFinDimWsReport"\نطاق‏‎<JournalLine>: عمودي\نطاق‏‎<TransactionLine>: عمودي\نطاق<DimValues>: أفقي".</span><span class="sxs-lookup"><span data-stu-id="63d59-168">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="63d59-169">تعيين عناصر التنسيق إلى مصادر بيانات</span><span class="sxs-lookup"><span data-stu-id="63d59-169">Map format elements to data sources</span></span>
1. <span data-ttu-id="63d59-170">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="63d59-170">Click the Mapping tab.</span></span>
2. <span data-ttu-id="63d59-171">في الشجرة، قم بتوسيع "النموذج: نموذج البيانات نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="63d59-171">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="63d59-172">في الشجرة، قم بتوسيع "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="63d59-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="63d59-173">في الشجرة، قم بتوسيع "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="63d59-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="63d59-174">في الشجرة، قم بتوسيع "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="63d59-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="63d59-175">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\Range<DimValues>: أفقي\خلية<DimValues>".</span><span class="sxs-lookup"><span data-stu-id="63d59-175">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="63d59-176">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات\الكود: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="63d59-176">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="63d59-177">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="63d59-177">Click Bind.</span></span>
9. <span data-ttu-id="63d59-178">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق‏‎<JournalLine>: عمودي\نطاق‏‎<TransactionLine>: عمودي\نطاق<DimValues>: أفقي".</span><span class="sxs-lookup"><span data-stu-id="63d59-178">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="63d59-179">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="63d59-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="63d59-180">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="63d59-180">Click Bind.</span></span>
12. <span data-ttu-id="63d59-181">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\خلية<Credit>".</span><span class="sxs-lookup"><span data-stu-id="63d59-181">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="63d59-182">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\الائتمان: حقيقي‬".</span><span class="sxs-lookup"><span data-stu-id="63d59-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="63d59-183">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="63d59-183">Click Bind.</span></span>
15. <span data-ttu-id="63d59-184">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\خلية<Debit>".</span><span class="sxs-lookup"><span data-stu-id="63d59-184">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="63d59-185">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\الدين: حقيقي‬".</span><span class="sxs-lookup"><span data-stu-id="63d59-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="63d59-186">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="63d59-186">Click Bind.</span></span>
18. <span data-ttu-id="63d59-187">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\خلية<Currency>".</span><span class="sxs-lookup"><span data-stu-id="63d59-187">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="63d59-188">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\العملة: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="63d59-188">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="63d59-189">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="63d59-189">Click Bind.</span></span>
21. <span data-ttu-id="63d59-190">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\خلية<TransDate>".</span><span class="sxs-lookup"><span data-stu-id="63d59-190">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="63d59-191">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\التاريخ: التاريخ".</span><span class="sxs-lookup"><span data-stu-id="63d59-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="63d59-192">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="63d59-192">Click Bind.</span></span>
24. <span data-ttu-id="63d59-193">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\خلية<TransVoucher>".</span><span class="sxs-lookup"><span data-stu-id="63d59-193">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="63d59-194">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\الإيصال: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="63d59-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="63d59-195">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="63d59-195">Click Bind.</span></span>
27. <span data-ttu-id="63d59-196">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\خلية<TransBatch>".</span><span class="sxs-lookup"><span data-stu-id="63d59-196">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="63d59-197">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الدُفعة: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="63d59-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="63d59-198">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="63d59-198">Click Bind.</span></span>
30. <span data-ttu-id="63d59-199">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي".</span><span class="sxs-lookup"><span data-stu-id="63d59-199">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="63d59-200">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="63d59-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="63d59-201">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="63d59-201">Click Bind.</span></span>
33. <span data-ttu-id="63d59-202">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\خلية<Batch>".</span><span class="sxs-lookup"><span data-stu-id="63d59-202">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="63d59-203">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الدُفعة: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="63d59-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="63d59-204">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="63d59-204">Click Bind.</span></span>
36. <span data-ttu-id="63d59-205">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي".</span><span class="sxs-lookup"><span data-stu-id="63d59-205">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="63d59-206">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="63d59-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="63d59-207">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="63d59-207">Click Bind.</span></span>
39. <span data-ttu-id="63d59-208">في الشجرة، قم بتوسيع "النموذج: نموذج الأبعاد المالية لنموذج البيانات\إعداد الأبعاد: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="63d59-208">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="63d59-209">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\إعداد الأبعاد: قائمة السجلات\الكود: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="63d59-209">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="63d59-210">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<DimNames>: أفقي\خلية<DimNames>".</span><span class="sxs-lookup"><span data-stu-id="63d59-210">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="63d59-211">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="63d59-211">Click Bind.</span></span>
43. <span data-ttu-id="63d59-212">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\إعداد الأبعاد: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="63d59-212">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="63d59-213">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<DimNames>: أفقي".</span><span class="sxs-lookup"><span data-stu-id="63d59-213">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="63d59-214">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="63d59-214">Click Bind.</span></span>
46. <span data-ttu-id="63d59-215">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\خلية<CompanyName>".</span><span class="sxs-lookup"><span data-stu-id="63d59-215">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="63d59-216">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\الشركة: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="63d59-216">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="63d59-217">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="63d59-217">Click Bind.</span></span>
49. <span data-ttu-id="63d59-218">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="63d59-218">Click Save.</span></span>
50. <span data-ttu-id="63d59-219">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="63d59-219">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]