---
title: التقارير الإلكترونية - استخدام النطاقات القابلة للتوسيع أفقيًا لإضافة الأعمدة بشكل حيوي في تقارير Excel (الجزء 1 - تصميم التنسيق)
description: تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق التقارير الإلكترونية لإنشاء التقارير كملفات أوراق عمل (Excel) تنسيق OPENXML حيث يمكن إنشاء الأعمدة المطلوبة بطريقة ديناميكية كنطاقات قابلة للتوسيع أفقيًا.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b616998738d6b6986f157d136fc56e061900ef41
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550522"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a><span data-ttu-id="1d9df-103">التقارير الإلكترونية - استخدام النطاقات القابلة للتوسيع أفقيًا لإضافة الأعمدة بشكل حيوي في تقارير Excel (الجزء 1 - تصميم التنسيق)</span><span class="sxs-lookup"><span data-stu-id="1d9df-103">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1 - Design format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d9df-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق التقارير الإلكترونية لإنشاء التقارير كملفات أوراق عمل (Excel) تنسيق OPENXML حيث يمكن إنشاء الأعمدة المطلوبة بطريقة ديناميكية كنطاقات قابلة للتوسيع أفقيًا.</span><span class="sxs-lookup"><span data-stu-id="1d9df-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="1d9df-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="1d9df-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="1d9df-106">لإكمال هذه الخطوات، يجب عليك أولاً إكمال خطوط دلائل المهام الثلاث التالية:</span><span class="sxs-lookup"><span data-stu-id="1d9df-106">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="1d9df-107">"التقارير الإلكترونية - إنشاء موفر تكوين ووضع علامة عليه على أنه نشط"</span><span class="sxs-lookup"><span data-stu-id="1d9df-107">“ER Create a configuration provider and mark it as active”</span></span>

<span data-ttu-id="1d9df-108">"التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 1: تصميم نموذج البيانات)"</span><span class="sxs-lookup"><span data-stu-id="1d9df-108">“ER Use financial dimensions as a data source (Part 1: Design data model)”</span></span>

<span data-ttu-id="1d9df-109">"التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 2: تعيين النموذج)"</span><span class="sxs-lookup"><span data-stu-id="1d9df-109">“ER Use financial dimensions as a data source (Part 2: Model mapping)”</span></span>

<span data-ttu-id="1d9df-110">يجب أيضًا تنزيل نسخة محلية من القالب وحفظها مع نموذج التقرير الموجود هنا، [عينة تقرير خدمة ويب للأبعاد المالية](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="1d9df-110">You must also download and save a local copy of the template with a sample report found here, [Sample Financial Dimensions Web Service Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>

<span data-ttu-id="1d9df-111">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="1d9df-111">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="1d9df-112">إنشاء تكوين تقرير جديد</span><span class="sxs-lookup"><span data-stu-id="1d9df-112">Create a new report configuration</span></span>
1. <span data-ttu-id="1d9df-113">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="1d9df-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="1d9df-114">في الشجرة، حدد "نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="1d9df-114">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="1d9df-115">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="1d9df-115">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="1d9df-116">في الحقل "جديد"، أدخل "التنسيق المستند إلى نموذج البيانات نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="1d9df-116">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="1d9df-117">استخدم النموذج الذي تم إنشاؤه مسبقًا كمصدر بيانات للتقرير الجديد.</span><span class="sxs-lookup"><span data-stu-id="1d9df-117">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="1d9df-118">في حقل "الاسم"، اكتب "نموذج تقرير مع نطاقات قابلة للتوسيع أفقيًا".</span><span class="sxs-lookup"><span data-stu-id="1d9df-118">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="1d9df-119">نموذج تقرير مع نطاقات قابلة للتوسيع أفقيًا</span><span class="sxs-lookup"><span data-stu-id="1d9df-119">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="1d9df-120">في حقل "الوصف"، اكتب "لإنشاء مخرجات Excel من خلال إضافة الأعمدة بشكل حيوي‬".</span><span class="sxs-lookup"><span data-stu-id="1d9df-120">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="1d9df-121">لإنشاء مخرجات Excel من خلال إضافة الأعمدة بشكل حيوي</span><span class="sxs-lookup"><span data-stu-id="1d9df-121">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="1d9df-122">في الحقل "تعريف نموذج البيانات"، حدد "الإدخال".</span><span class="sxs-lookup"><span data-stu-id="1d9df-122">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="1d9df-123">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="1d9df-123">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="1d9df-124">تصميم تنسيق التقرير</span><span class="sxs-lookup"><span data-stu-id="1d9df-124">Design the report format</span></span>
1. <span data-ttu-id="1d9df-125">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="1d9df-125">Click Designer.</span></span>
2. <span data-ttu-id="1d9df-126">قم بتشغيل زر التبديل "إظهار التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="1d9df-126">Turn on the ‘Show details’ toggle button.</span></span>
3. <span data-ttu-id="1d9df-127">في جزء الإجراءات، انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="1d9df-127">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="1d9df-128">انقر فوق استيراد من "Excel".</span><span class="sxs-lookup"><span data-stu-id="1d9df-128">Click Import from Excel.</span></span>
5. <span data-ttu-id="1d9df-129">انقر فوق "المرفقات".</span><span class="sxs-lookup"><span data-stu-id="1d9df-129">Click Attachments.</span></span>
    * <span data-ttu-id="1d9df-130">استورد قالب التقرير.</span><span class="sxs-lookup"><span data-stu-id="1d9df-130">Import the report’s template.</span></span> <span data-ttu-id="1d9df-131">استخدم ملف Excel الذي قمت بتحميله لذلك.</span><span class="sxs-lookup"><span data-stu-id="1d9df-131">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="1d9df-132">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1d9df-132">Click New.</span></span>
7. <span data-ttu-id="1d9df-133">انقر فوق "ملف".</span><span class="sxs-lookup"><span data-stu-id="1d9df-133">Click File.</span></span>
8. <span data-ttu-id="1d9df-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1d9df-134">Close the page.</span></span>
9. <span data-ttu-id="1d9df-135">في حقل "القالب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1d9df-135">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="1d9df-136">حدد القالب الذي تم تنزيله.</span><span class="sxs-lookup"><span data-stu-id="1d9df-136">Select the downloaded template.</span></span>  
10. <span data-ttu-id="1d9df-137">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="1d9df-137">Click OK.</span></span>
    * <span data-ttu-id="1d9df-138">أضف مجموعة جديدة لإنشاء مخرجات Excel بطريقة ديناميكية باستخدام العدد الذي حددته من الأعمدة (في نموذج حوار المستخدم) للأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="1d9df-138">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="1d9df-139">ستمثل كل خلية لكل عمود اسم بُعد مالي واحد.</span><span class="sxs-lookup"><span data-stu-id="1d9df-139">Each cell for every column will represent a single financial dimension’s name.</span></span>  
11. <span data-ttu-id="1d9df-140">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="1d9df-140">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="1d9df-141">في الشجرة، حدد "Excel\نطاق".</span><span class="sxs-lookup"><span data-stu-id="1d9df-141">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="1d9df-142">في الحقل "نطاق Excel"، اكتب "DimNames".</span><span class="sxs-lookup"><span data-stu-id="1d9df-142">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="1d9df-143">DimNames</span><span class="sxs-lookup"><span data-stu-id="1d9df-143">DimNames</span></span>  
14. <span data-ttu-id="1d9df-144">في الحقل "اتجاه النسخ المتماثل"، حدد "أفقي".</span><span class="sxs-lookup"><span data-stu-id="1d9df-144">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="1d9df-145">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="1d9df-145">Click OK.</span></span>
16. <span data-ttu-id="1d9df-146">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<DimNames>: أفقي".</span><span class="sxs-lookup"><span data-stu-id="1d9df-146">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="1d9df-147">انقر فوق "تحريك لأعلى".</span><span class="sxs-lookup"><span data-stu-id="1d9df-147">Click Move up.</span></span>
18. <span data-ttu-id="1d9df-148">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\خلية<DimNames>".</span><span class="sxs-lookup"><span data-stu-id="1d9df-148">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="1d9df-149">انقر فوق "قص".</span><span class="sxs-lookup"><span data-stu-id="1d9df-149">Click Cut.</span></span>
20. <span data-ttu-id="1d9df-150">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<DimNames>: أفقي".</span><span class="sxs-lookup"><span data-stu-id="1d9df-150">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="1d9df-151">انقر فوق "لصق".</span><span class="sxs-lookup"><span data-stu-id="1d9df-151">Click Paste.</span></span>
22. <span data-ttu-id="1d9df-152">في الشجرة، قم بتوسيع "Excel = "SampleFinDimWsReport"\نطاق<DimNames>: أفقي".</span><span class="sxs-lookup"><span data-stu-id="1d9df-152">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="1d9df-153">في الشجرة، قم بتوسيع "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي".</span><span class="sxs-lookup"><span data-stu-id="1d9df-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="1d9df-154">في الشجرة، قم بتوسيع "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي".</span><span class="sxs-lookup"><span data-stu-id="1d9df-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="1d9df-155">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي".</span><span class="sxs-lookup"><span data-stu-id="1d9df-155">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="1d9df-156">أضف مجموعة جديدة لإنشاء مخرجات Excel بطريقة ديناميكية باستخدام العدد الذي حددته من الأعمدة (في نموذج حوار المستخدم) للأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="1d9df-156">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="1d9df-157">ستمثل كل خلية لكل عمود قيمة بُعد مالي واحدة لكل حركة تقرير.</span><span class="sxs-lookup"><span data-stu-id="1d9df-157">Each cell for every column will represent a single financial dimension’s value for each reporting transaction.</span></span>  
26. <span data-ttu-id="1d9df-158">انقر فوق "إضافة نطاق".</span><span class="sxs-lookup"><span data-stu-id="1d9df-158">Click Add Range.</span></span>
27. <span data-ttu-id="1d9df-159">في الحقل "نطاق Excel"، اكتب "DimValues".</span><span class="sxs-lookup"><span data-stu-id="1d9df-159">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="1d9df-160">DimValues</span><span class="sxs-lookup"><span data-stu-id="1d9df-160">DimValues</span></span>  
28. <span data-ttu-id="1d9df-161">في الحقل "اتجاه النسخ المتماثل"، حدد "أفقي".</span><span class="sxs-lookup"><span data-stu-id="1d9df-161">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="1d9df-162">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="1d9df-162">Click OK.</span></span>
30. <span data-ttu-id="1d9df-163">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\خلية<DimValues>".</span><span class="sxs-lookup"><span data-stu-id="1d9df-163">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="1d9df-164">انقر فوق "قص".</span><span class="sxs-lookup"><span data-stu-id="1d9df-164">Click Cut.</span></span>
32. <span data-ttu-id="1d9df-165">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق‏‎<JournalLine>: عمودي\نطاق‏‎<TransactionLine>: عمودي\نطاق<DimValues>: أفقي".</span><span class="sxs-lookup"><span data-stu-id="1d9df-165">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="1d9df-166">انقر فوق "لصق".</span><span class="sxs-lookup"><span data-stu-id="1d9df-166">Click Paste.</span></span>
34. <span data-ttu-id="1d9df-167">في الشجرة، قم بتوسيع "Excel = "SampleFinDimWsReport"\نطاق‏‎<JournalLine>: عمودي\نطاق‏‎<TransactionLine>: عمودي\نطاق<DimValues>: أفقي".</span><span class="sxs-lookup"><span data-stu-id="1d9df-167">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="1d9df-168">تعيين عناصر التنسيق إلى مصادر بيانات</span><span class="sxs-lookup"><span data-stu-id="1d9df-168">Map format elements to data sources</span></span>
1. <span data-ttu-id="1d9df-169">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="1d9df-169">Click the Mapping tab.</span></span>
2. <span data-ttu-id="1d9df-170">في الشجرة، قم بتوسيع "النموذج: نموذج البيانات نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="1d9df-170">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="1d9df-171">في الشجرة، قم بتوسيع "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="1d9df-171">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="1d9df-172">في الشجرة، قم بتوسيع "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="1d9df-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="1d9df-173">في الشجرة، قم بتوسيع "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="1d9df-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="1d9df-174">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\Range<DimValues>: أفقي\خلية<DimValues>".</span><span class="sxs-lookup"><span data-stu-id="1d9df-174">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="1d9df-175">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات\الكود: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="1d9df-175">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="1d9df-176">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="1d9df-176">Click Bind.</span></span>
9. <span data-ttu-id="1d9df-177">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق‏‎<JournalLine>: عمودي\نطاق‏‎<TransactionLine>: عمودي\نطاق<DimValues>: أفقي".</span><span class="sxs-lookup"><span data-stu-id="1d9df-177">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="1d9df-178">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="1d9df-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="1d9df-179">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="1d9df-179">Click Bind.</span></span>
12. <span data-ttu-id="1d9df-180">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\خلية<Credit>".</span><span class="sxs-lookup"><span data-stu-id="1d9df-180">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="1d9df-181">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\الائتمان: حقيقي‬".</span><span class="sxs-lookup"><span data-stu-id="1d9df-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="1d9df-182">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="1d9df-182">Click Bind.</span></span>
15. <span data-ttu-id="1d9df-183">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\خلية<Debit>".</span><span class="sxs-lookup"><span data-stu-id="1d9df-183">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="1d9df-184">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\الدين: حقيقي‬".</span><span class="sxs-lookup"><span data-stu-id="1d9df-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="1d9df-185">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="1d9df-185">Click Bind.</span></span>
18. <span data-ttu-id="1d9df-186">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\خلية<Currency>".</span><span class="sxs-lookup"><span data-stu-id="1d9df-186">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="1d9df-187">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\العملة: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="1d9df-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="1d9df-188">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="1d9df-188">Click Bind.</span></span>
21. <span data-ttu-id="1d9df-189">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\خلية<TransDate>".</span><span class="sxs-lookup"><span data-stu-id="1d9df-189">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="1d9df-190">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\التاريخ: التاريخ".</span><span class="sxs-lookup"><span data-stu-id="1d9df-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="1d9df-191">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="1d9df-191">Click Bind.</span></span>
24. <span data-ttu-id="1d9df-192">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\خلية<TransVoucher>".</span><span class="sxs-lookup"><span data-stu-id="1d9df-192">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="1d9df-193">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\الإيصال: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="1d9df-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="1d9df-194">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="1d9df-194">Click Bind.</span></span>
27. <span data-ttu-id="1d9df-195">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي\خلية<TransBatch>".</span><span class="sxs-lookup"><span data-stu-id="1d9df-195">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="1d9df-196">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الدُفعة: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="1d9df-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="1d9df-197">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="1d9df-197">Click Bind.</span></span>
30. <span data-ttu-id="1d9df-198">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\نطاق<TransactionLine>: عمودي".</span><span class="sxs-lookup"><span data-stu-id="1d9df-198">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="1d9df-199">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="1d9df-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="1d9df-200">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="1d9df-200">Click Bind.</span></span>
33. <span data-ttu-id="1d9df-201">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي\خلية<Batch>".</span><span class="sxs-lookup"><span data-stu-id="1d9df-201">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="1d9df-202">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الدُفعة: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="1d9df-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="1d9df-203">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="1d9df-203">Click Bind.</span></span>
36. <span data-ttu-id="1d9df-204">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<JournalLine>: عمودي".</span><span class="sxs-lookup"><span data-stu-id="1d9df-204">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="1d9df-205">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="1d9df-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="1d9df-206">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="1d9df-206">Click Bind.</span></span>
39. <span data-ttu-id="1d9df-207">في الشجرة، قم بتوسيع "النموذج: نموذج الأبعاد المالية لنموذج البيانات\إعداد الأبعاد: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="1d9df-207">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="1d9df-208">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\إعداد الأبعاد: قائمة السجلات\الكود: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="1d9df-208">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="1d9df-209">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<DimNames>: أفقي\خلية<DimNames>".</span><span class="sxs-lookup"><span data-stu-id="1d9df-209">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="1d9df-210">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="1d9df-210">Click Bind.</span></span>
43. <span data-ttu-id="1d9df-211">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\إعداد الأبعاد: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="1d9df-211">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="1d9df-212">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\نطاق<DimNames>: أفقي".</span><span class="sxs-lookup"><span data-stu-id="1d9df-212">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="1d9df-213">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="1d9df-213">Click Bind.</span></span>
46. <span data-ttu-id="1d9df-214">في الشجرة، حدد "Excel = "SampleFinDimWsReport"\خلية<CompanyName>".</span><span class="sxs-lookup"><span data-stu-id="1d9df-214">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="1d9df-215">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\الشركة: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="1d9df-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="1d9df-216">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="1d9df-216">Click Bind.</span></span>
49. <span data-ttu-id="1d9df-217">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1d9df-217">Click Save.</span></span>
50. <span data-ttu-id="1d9df-218">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1d9df-218">Close the page.</span></span>

