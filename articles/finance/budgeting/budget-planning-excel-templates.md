---
title: قوالب تخطيط الموازنة لـ Excel
description: يوضح هذا الموضوع كيفية إنشاء قوالب Microsoft Excel التي يمكن استخدامها مع خطط الموازنة.
author: panolte
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: roschlom
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f7564ea4372e3d5a532daa33ff59802ba7dede6c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210351"
---
# <a name="budget-planning-templates-for-excel"></a><span data-ttu-id="5ab5a-103">قوالب تخطيط الموازنة لـ Excel</span><span class="sxs-lookup"><span data-stu-id="5ab5a-103">Budget planning templates for Excel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ab5a-104">يوضح هذا الموضوع كيفية إنشاء قوالب Microsoft Excel التي يمكن استخدامها مع خطط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-104">This topic describes how to create Microsoft Excel templates that can be used with budget plans.</span></span>

<span data-ttu-id="5ab5a-105">يوضح هذا الموضوع كيفية إنشاء قوالب Excel التي سيتم استخدامها مع خطط الموازنة باستخدام مجموعة بيانات العرض التقديمي القياسية وتسجيل دخول مستخدم "المسؤول".</span><span class="sxs-lookup"><span data-stu-id="5ab5a-105">This topic shows how to create Excel templates that will be used with budget plans using the standard demo data set and the Admin user login.</span></span> <span data-ttu-id="5ab5a-106">لمزيد من المعلومات حول تخطيط الموازنة، راجع [نظرة عامة حول تخطيط الموازنة](budget-planning-overview-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="5ab5a-106">For more information about budget planning, see [Budget planning overview](budget-planning-overview-configuration.md).</span></span> <span data-ttu-id="5ab5a-107">يمكنك أيضًا متابعة البرنامج التعليمي [تخطيط الموازنة](budget-plan.md) لمعرفة تكوين الوحدة الأساسية ومبادئ الاستخدام.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-107">You can also follow the [Budget planning](budget-plan.md) tutorial to learn basic module configuration and usage principles.</span></span>

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a><span data-ttu-id="5ab5a-108">إنشاء ورقة عمل باستخدام تخطيط مستند خطة الموازنة</span><span class="sxs-lookup"><span data-stu-id="5ab5a-108">Generate a worksheet using budget plan document layout</span></span>

<span data-ttu-id="5ab5a-109">يمكن عرض مستندات خطة الموازنة وتحريرها باستخدام تخطيط واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-109">Budget plan documents can be viewed and edited using one or more layouts.</span></span> <span data-ttu-id="5ab5a-110">يمكن أن يكون لكل تخطيط قالب مستند خطة موازنة مقترن لعرض وتحرير بيانات خطة الموازنة في ورقة عمل Excel.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-110">Each layout can have an associated budget plan document template to view and edit the budget plan data in an Excel worksheet.</span></span> <span data-ttu-id="5ab5a-111">في هذا الموضوع، سوف يتم إنشاء قالب مستند خطة الموازنة باستخدام تكون تخطيط موجود.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-111">In this topic, a budget plan document template will be generated using an existing layout configuration.</span></span> 

1. <span data-ttu-id="5ab5a-112">افتح **قائمة خطط الموازنة** (**الموازنة** &gt; **خطط الموازنة**).</span><span class="sxs-lookup"><span data-stu-id="5ab5a-112">Open the **Budget plans list** (**Budgeting** &gt; **Budget plans**).</span></span> 
2. <span data-ttu-id="5ab5a-113">انقر فوق **جديد** لإنشاء مستند خطة موازنة جديد.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-113">Click **New** to create a new budget plan document.</span></span> 

   <span data-ttu-id="5ab5a-114">[![قائمة خطط الموازنة](./media/bpt11-1024x552.png)](./media/bpt11.png)</span><span class="sxs-lookup"><span data-stu-id="5ab5a-114">[![Budget plans list](./media/bpt11-1024x552.png)](./media/bpt11.png)</span></span> 

3. <span data-ttu-id="5ab5a-115">استخدم خيار سطر **إضافة** لإضافة السطور.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-115">Use the **Add** line option to add lines.</span></span> <span data-ttu-id="5ab5a-116">انقر فوق **تخطيطات** لعرض تكوين تخطيط مستند خطة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-116">Click **Layouts** to view the budget plan document layout configuration.</span></span> 

   <span data-ttu-id="5ab5a-117">[![إضافة خطط الموازنة](./media/bpt2-1024x274.png)](./media/bpt2.png)</span><span class="sxs-lookup"><span data-stu-id="5ab5a-117">[![Budget plans add](./media/bpt2-1024x274.png)](./media/bpt2.png)</span></span> 

<span data-ttu-id="5ab5a-118">يمكنك مراجعة تكوين التخطيط وتعديله وفقًا لما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-118">You can review the layout configuration and adjust it as needed.</span></span> 
1. <span data-ttu-id="5ab5a-119">انتقل إلى **قالب** &gt; **إنشاء** لإنشاء ملف Excel لهذا التخطيط.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-119">Go to **Template** &gt; **Generate** to create an Excel file for this layout.</span></span> 
2. <span data-ttu-id="5ab5a-120">بعد إنشاء القالب، انتقل إلى **قالب** &gt; **عرض** لفتح ومراجعة قالب مستند خطة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-120">After the template is generated, go to **Template** &gt; **View** to open and review the budget plan document template.</span></span> <span data-ttu-id="5ab5a-121">يمكنك حفظ ملف الـ Excel في المحرك المحلي.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-121">You can save the Excel file to your local drive.</span></span> 

<span data-ttu-id="5ab5a-122">[![حفظ باسم](./media/bpt3-1024x545.png)](./media/bpt3.png)</span><span class="sxs-lookup"><span data-stu-id="5ab5a-122">[![Save as](./media/bpt3-1024x545.png)](./media/bpt3.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="5ab5a-123">تعذر تحرير تخطيط مستند خطة الموازنة بعد اقتران قالب Excel بالمستند.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-123">The Budget plan document layout cannot be edited after an Excel template is associated with it.</span></span> <span data-ttu-id="5ab5a-124">لتعديل التخطيط، احذف ملف قالب Excel المقترن، وقم بإعادة الإنشاء.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-124">To modify the layout, delete the associated Excel template file and regenerate it.</span></span> <span data-ttu-id="5ab5a-125">يتطلب هذا الاحتفاظ بالحقول في التخطيط، ومزامنة ورقة العمل.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-125">This is required to keep the fields in the layout and the worksheet synchronized.</span></span> 

<span data-ttu-id="5ab5a-126">سوف يحتوي قالب Excel على جميع العناصر من تخطيط مستند خطة الموازنة، عندما يتم تعيين عمود **متوفر في ورقة العمل** على وضع "صواب".</span><span class="sxs-lookup"><span data-stu-id="5ab5a-126">The Excel template will contain all of the elements from the budget plan document layout, where the **Available in Worksheet** column is set to True.</span></span> <span data-ttu-id="5ab5a-127">لا يسمح بعناصر التداخل في قالب Excel.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-127">Overlapping elements are not allowed in the Excel template.</span></span> <span data-ttu-id="5ab5a-128">على سبيل المثال، إذا كان التخطيط يحتوي على أعمدة طلب ربع1، وطلب ربع2، وطلب ربع3 وطلب ربع4، وعمود الطلب الإجمالي والذي يمثل مجموع الأربعة أعمدة الربع سنوية، يتاح استخدام الأعمدة الربع سنوية أو العمود الإجمالي فقط في قالب Excel.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-128">For example, if the layout contains Request Q1, Request Q2, Request Q3, and Request Q4 columns, and a total request column that represents a sum of all 4 quarterly columns, only the quarterly columns or total column is available to be used in the Excel template.</span></span> <span data-ttu-id="5ab5a-129">يتعذر على ملف Excel تحديث أعمدة التداخل أثناء التحديث لأن البيانات في الجدول قد تصبح قديمة وغير دقيقة.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-129">The Excel file cannot update overlapping columns during the update because data in the table could become out of date and inaccurate.</span></span>

> [!NOTE] 
> <span data-ttu-id="5ab5a-130">لتجنب المشاكل المحتملة في عرض وتحرير بيانات خطة الموازنة باستخدام Excel، يجب على المستخدم نفسه تسجيل دخوله إلى كل من Microsoft Dynamics 365 Finance والوظيفة الإضافية موصل البيانات لـ Office في Microsoft Dynamics.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-130">To avoid potential issues with viewing and editing budget plan data using Excel, the same user should be logged into both Microsoft Dynamics 365 Finance and the Microsoft Dynamics Office Add-in Data Connector.</span></span>

## <a name="add-a-header-to-budget-plan-document-template"></a><span data-ttu-id="5ab5a-131">إضافة عنوان إلى قالب مستند خطة الموازنة</span><span class="sxs-lookup"><span data-stu-id="5ab5a-131">Add a header to budget plan document template</span></span>
<span data-ttu-id="5ab5a-132">لإضافة معلومات العنوان، حدد الصف العلوي في ملف Excel، ثم قم بإدراج صفوف فارغة.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-132">To add header information, select the top row in the Excel file and insert empty rows.</span></span> <span data-ttu-id="5ab5a-133">انقر فوق **تصميم** في **موصل البيانات** لإضافة حقول العنوان إلى ملف Excel.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-133">Click **Design** in the **Data Connector** to add header fields to the Excel file.</span></span>

<span data-ttu-id="5ab5a-134">على علامة التبويب **تصميم**، انقر فوق حقول **إضافة**، ثم حدد **BudgetPlanHeader** كمصدر بيانات الكيان.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-134">In the **Design** tab, click **Add** fields, and then select **BudgetPlanHeader** as the entity data source.</span></span>

<span data-ttu-id="5ab5a-135">وجّه المؤشر إلى الموقع المطلوب في ملف Excel.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-135">Point the cursor to the desired location in the Excel file.</span></span> <span data-ttu-id="5ab5a-136">انقر فوق **إضافة تسمية** لإضافة تسمية الحقل إلى الموقع المحدد.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-136">Click **Add label** to add the field label to the selected location.</span></span> <span data-ttu-id="5ab5a-137">حدد **"إضافة قيمة"** لإضافة قيمة الحقل إلى الموضع المحدد.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-137">Select **Add Value** to add the value field to the selected place.</span></span> <span data-ttu-id="5ab5a-138">انقر فوق **تم** لإغلاق المصمم.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-138">Click **Done** to close the designer.</span></span>

## <a name="select-add-valuemediabpt7png"></a><span data-ttu-id="5ab5a-139">[![تحديد إضافة قيمة](./media/bpt7.png)](./media/bpt7.png)</span><span class="sxs-lookup"><span data-stu-id="5ab5a-139">[![Select Add Value](./media/bpt7.png)](./media/bpt7.png)</span></span>

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a><span data-ttu-id="5ab5a-140">إضافة عمود محسوب إلى جدول قالب مستند خطة الموازنة</span><span class="sxs-lookup"><span data-stu-id="5ab5a-140">Add a calculated column to budget plan document template table</span></span>
--------------------------------------------------------------

<span data-ttu-id="5ab5a-141">التالي، سوف تتم إضافة الأعمدة المحسوبة إلى قالب مستند خطة الموازنة الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-141">Next, calculated columns will be added to generated budget plan document template.</span></span> <span data-ttu-id="5ab5a-142">عمود **إجمالي الطلب**، والذي يلخص طلب ربع1: أعمدة طلب ربع4، وعمود **التسوية**، والذي يقوم بإعادة حساب عمود **"إجمالي الطلب"** من خلال عامل محدد مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-142">A **Total request** column, which summarizes Request Q1: Request Q4 columns, and an **Adjustment** column, which recalculates the **Total Request** column by a predefined factor.</span></span>

<span data-ttu-id="5ab5a-143">انقر فوق **تصميم** في **موصل البيانات** لإضافة الأعمدة إلى الجدول.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-143">Click **Design** in the **Data connector** to add columns to the table.</span></span> <span data-ttu-id="5ab5a-144">انقر فوق **تحرير** الموجود بجوار مصدر بيانات **BudgetPlanWorksheet** لبدء إضافة أعمدة.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-144">Click **Edit** next to **BudgetPlanWorksheet** data source to start adding columns.</span></span>

<span data-ttu-id="5ab5a-145">[![بدء إضافة الأعمدة](./media/bpt8-1024x301.png)](./media/bpt8.png)</span><span class="sxs-lookup"><span data-stu-id="5ab5a-145">[![Start adding columns](./media/bpt8-1024x301.png)](./media/bpt8.png)</span></span> 

<span data-ttu-id="5ab5a-146">تعرض مجموعة الحقل المحدد الأعمدة المتوفرة في القالب.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-146">The selected field group displays the columns that are available in the template.</span></span> <span data-ttu-id="5ab5a-147">انقر فوق **معادلة** لإضافة عمود جديد.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-147">Click **Formula** to add a new column.</span></span> <span data-ttu-id="5ab5a-148">قم بتسمية العمود الجديد، ثم قم بلصق المعادلة داخل حقل **المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-148">Name the new column and then paste the formula into the **Formula** field.</span></span> <span data-ttu-id="5ab5a-149">انقر فوق **تحديث** لإدراج عمود.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-149">Click **Update** to insert the column.</span></span>

<span data-ttu-id="5ab5a-150">[![إضافة عمود وإدراجه](./media/bpt12-1024x565.png)](./media/bpt12.png)</span><span class="sxs-lookup"><span data-stu-id="5ab5a-150">[![Add and insert column](./media/bpt12-1024x565.png)](./media/bpt12.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="5ab5a-151">لتحديد المعادلة، قم بإنشاء المعادلة في جدول البيانات، ثم قم بنسخها إلى نافذة **تصميم**.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-151">To define the formula, create the formula in the spreadsheet, and then copy it to the **Design** window.</span></span> <span data-ttu-id="5ab5a-152">عادة ما يتم تسمية جدول العمليات المرتبطة لـ Finance and Operations باسم "AXTable1".</span><span class="sxs-lookup"><span data-stu-id="5ab5a-152">A Finance and Operations bound table will typically be named "AXTable1".</span></span> <span data-ttu-id="5ab5a-153">على سبيل المثال، لتلخيص طلب ربع1: أعمدة طلب ربع4 في جدول البيانات، المعادلة= AxTable1\[طلب ربع1\]+AxTable1\[طلب ربع2\]+AxTable1\[طلب ربع3\]+AxTable1\[طلب ربع4\].</span><span class="sxs-lookup"><span data-stu-id="5ab5a-153">For example, to summarize Request Q1 : Request Q4 columns in the spreadsheet, the formula = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span></span>

<span data-ttu-id="5ab5a-154">كرر هذه الخطوات لإدراج عمود **تسوية**.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-154">Repeat these steps to insert the **Adjustment** column.</span></span> <span data-ttu-id="5ab5a-155">استخدم المعادلة= AxTable1\[طلب إجمالي\]\*$I$1 لهذا العمود.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-155">Use formula = AxTable1\[Total request\]\*$I$1 for this column.</span></span> <span data-ttu-id="5ab5a-156">وسوف تأخذ هذه القيمة في الخلية 1 ومضاعفة القيم في عمود **الطلب الإجمالي** لحساب مبالغ التسوية.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-156">This will take the value in cell I1 and multiply the values in the **Total request** column to calculate adjustment amounts.</span></span>

<span data-ttu-id="5ab5a-157">قم بحفظ ملف Excel وإغلاقه.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-157">Save and close the Excel file.</span></span> <span data-ttu-id="5ab5a-158">في **التخطيطات**، انقر فوق **قالب &gt; تحميل** لتحميل قالب Excel المحفوظ ليتم استخدامه لخطة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-158">In **Layouts**, click **Template &gt; Upload** to upload the saved Excel template to be used for the budget plan.</span></span> 

<span data-ttu-id="5ab5a-159">[![تحميل قالب Excel](./media/bpt10-1024x352.png)](./media/bpt10.png)</span><span class="sxs-lookup"><span data-stu-id="5ab5a-159">[![Upload Excel template](./media/bpt10-1024x352.png)](./media/bpt10.png)</span></span> 

<span data-ttu-id="5ab5a-160">إغلاق شريط تمرير **تخطيطات**.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-160">Close the **Layouts** slider.</span></span> <span data-ttu-id="5ab5a-161">في مستند **خطة الموازنة**، انقر فوق **ورقة عمل** لعرض وتحرير المستند في Excel.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-161">In **Budget plan** document, click **Worksheet** to view and edit the document in Excel.</span></span> <span data-ttu-id="5ab5a-162">لاحظ أنه تم استخدام قالب Excel المعدل لإنشاء ورقة عمل خطة الموازنة هذه، ويتم تحديث الأعمدة المحسوبة باستخدام المعادلات التي تم تحديدها في الخطوات السابقة.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-162">Note that the adjusted Excel template was used to create this budget plan worksheet and calculated columns are updated using the formulas that were defined in the previous steps.</span></span> 

<span data-ttu-id="5ab5a-163">[![عرض المستند وتحريره في Excel](./media/bpt111-1024x431.png)](./media/bpt111.png)</span><span class="sxs-lookup"><span data-stu-id="5ab5a-163">[![View and edit document in Excel](./media/bpt111-1024x431.png)](./media/bpt111.png)</span></span>

## <a name="tips--tricks-for-creating-budget-plan-templates"></a><span data-ttu-id="5ab5a-164">تلميحات ونصائح حول إنشاء قوالب خطة الموازنة</span><span class="sxs-lookup"><span data-stu-id="5ab5a-164">Tips & tricks for creating budget plan templates</span></span>
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a><span data-ttu-id="5ab5a-165">هل يمكنني إضافة واستخدام مصادر بيانات إضافية إلى قالب خطة الموازنة؟</span><span class="sxs-lookup"><span data-stu-id="5ab5a-165">Can I add and use additional data sources to a budget plan template?</span></span>

<span data-ttu-id="5ab5a-166">نعم، يمكنك استخدام قائمة **تصميم** لإضافة كيانات إضافية لنفس الأوراق أو لأوراق أخرى في قالب Excel.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-166">Yes, you can use the **Design** menu to add additional entities to the same or other sheets in the Excel template.</span></span> <span data-ttu-id="5ab5a-167">على سبيل المثال، يمكنك إضافة مصدر بيانات **BudgetPlanProposedProject** لإنشاء والاحتفاظ بقائمة المشاريع المقترحة في نفس الوقت عند العمل مع بيانات خطة الموازنة في Excel.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-167">For example, you can add the **BudgetPlanProposedProject** data source to create and maintain a list of proposed projects at the same time when working with budget plan data in Excel.</span></span> <span data-ttu-id="5ab5a-168">لاحظ أن تضمين مصادر بيانات كبيرة الحجم قد يؤثر على أداء مصنف Excel.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-168">Note that including high-volume data sources might impact performance of the Excel workbook.</span></span> 

<span data-ttu-id="5ab5a-169">يمكنك استخدام خيار **عامل تصفية** الموجود في **"موصل البيانات"** لإضافة عوامل التصفية المطلوبة إلى مصادر البيانات الإضافية.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-169">You can use the **Filter** option in the **Data Connector** to add desired filters to additional data sources.</span></span>

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a><span data-ttu-id="5ab5a-170">هل يمكن إخفاء خيار "تصميم" في "موصل البيانات" للمستخدمين الآخرين؟</span><span class="sxs-lookup"><span data-stu-id="5ab5a-170">Can I hide the Design option in the Data connector for other users?</span></span>

<span data-ttu-id="5ab5a-171">نعم، قم بفتح خيارات **"موصل البيانات"** لإخفاء خيار **تصميم** من مستخدمين آخرين.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-171">Yes, open the **Data Connector** options to hide the **Design** option from other users.</span></span>

<span data-ttu-id="5ab5a-172">[![خيارات موصل البيانات المفتوحة](./media/bpt13-1024x565.png)](./media/bpt13.png)</span><span class="sxs-lookup"><span data-stu-id="5ab5a-172">[![Open Data Connector options](./media/bpt13-1024x565.png)](./media/bpt13.png)</span></span>

<span data-ttu-id="5ab5a-173">قم بتوسيع **خيارات موصل البيانات** ومسح خانة اختيار **تمكين التصميم**.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-173">Expand **Data connector options** and clear the **Enable design** check box.</span></span> <span data-ttu-id="5ab5a-174">وسوف يقوم هذا بإخفاء خيار **التصميم** من **موصل البيانات**.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-174">This will hide the **Design** option from the **Data connector**.</span></span>

<span data-ttu-id="5ab5a-175">[![إخفاء خيار التصميم من موصل البيانات](./media/bpt14-1024x592.png)](./media/bpt14.png)</span><span class="sxs-lookup"><span data-stu-id="5ab5a-175">[![Hide Design option from Data connector](./media/bpt14-1024x592.png)](./media/bpt14.png)</span></span>

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a><span data-ttu-id="5ab5a-176">هل يمكنني منع المستخدمين من إغلاق موصل البيانات عن طريق الخطأ أثناء العمل مع البيانات؟</span><span class="sxs-lookup"><span data-stu-id="5ab5a-176">Can I prevent users from accidently closing the Data connector while working with data?</span></span>

<span data-ttu-id="5ab5a-177">نوصي بغلق القالب لمنع المستخدمين من إغلاقه.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-177">We recommend locking the template to prevent users from closing it.</span></span> <span data-ttu-id="5ab5a-178">لتشغيل خاصية "التأمين"، انقر فوق **موصل البيانات**، سوف يظهر سهم في الزاوية اليمنى العليا.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-178">To turn on the lock, click the **Data connector**, in the top right corner an arrow appears.</span></span> 

<span data-ttu-id="5ab5a-179">[![تشغيل التأمين](./media/bpt15-1024x285.png)](./media/bpt15.png)</span><span class="sxs-lookup"><span data-stu-id="5ab5a-179">[![Turn on the lock](./media/bpt15-1024x285.png)](./media/bpt15.png)</span></span> 

<span data-ttu-id="5ab5a-180">انقر فوق السهم لقائمة إضافية.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-180">Click the arrow for an additional menu.</span></span> <span data-ttu-id="5ab5a-181">حدد **تأمين**.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-181">Select **Lock**.</span></span>

### <a name="select-lockmediabpt16png"></a><span data-ttu-id="5ab5a-182">[![تحديد تأمين](./media/bpt16-1024x614.png)](./media/bpt16.png)</span><span class="sxs-lookup"><span data-stu-id="5ab5a-182">[![Select Lock](./media/bpt16-1024x614.png)](./media/bpt16.png)</span></span>

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a><span data-ttu-id="5ab5a-183">هل يمكنني استخدام ميزات Excel الأخرى، مثل تنسيق الخلايا، والألوان والتنسيق الشرطي والمخططات مع قوالب خطة الموازنة؟</span><span class="sxs-lookup"><span data-stu-id="5ab5a-183">Can I use other Excel features, like cell formatting, colors, conditional formatting, and charts with my budget plan templates?</span></span>

<span data-ttu-id="5ab5a-184">نعم، تعمل معظم إمكانيات Excel القياسية في قوالب خطة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-184">Yes, most of the standard Excel capabilities will work in budget plan templates.</span></span> <span data-ttu-id="5ab5a-185">نوصي باستخدام ترميز الألوان للمستخدمين للتمييز بين أعمدة القراءة فقط والأعمدة التي يمكن تحريرها.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-185">We recommend using color-coding for users to distinguish between read-only and editable columns.</span></span> <span data-ttu-id="5ab5a-186">يمكن استخدام التنسيق الشرطي لتمييز المناطق المثيرة للمشاكل في الموازنة.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-186">Conditional formatting can be used to highlight problematic areas of the budget.</span></span> <span data-ttu-id="5ab5a-187">يمكن بسهولة عرض إجماليات الأعمدة باستخدام معادلات Excel القياسية الموجود أعلى الجدول.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-187">Column totals can easily be presented by using standard Excel formulas above the table.</span></span>

<span data-ttu-id="5ab5a-188">يمكنك أيضا إنشاء واستخدام الرسوم البيانية والجداول المحورية للتجميعات الإضافية والرسوم المرئية لبيانات الموازنة.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-188">You can also create and use pivot tables and charts for additional groupings and visualizations of budget data.</span></span> <span data-ttu-id="5ab5a-189">في علامة تبويب **البيانات**، في مجموعة **اتصالات**، انقر فوق **"تحديث الكل"**، ثم انقر فوق **"خصائص الاتصال"**.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-189">On the **Data** tab, in the **Connections** group, click **Refresh All**, and then click **Connection Properties**.</span></span> <span data-ttu-id="5ab5a-190">انقر فوق علامة تبويب **الاستخدام**. ضمن **تحديث**، حدد خانة الاختيار **تحديث البيانات عند فتح الملف**.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-190">Click the **Usage** tab. Under **Refresh**, select the **Refresh data when opening the file** check box.</span></span> 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]