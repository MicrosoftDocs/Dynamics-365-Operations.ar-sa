---
title: "تعريفات الصفوف في مصمم التقارير المالية"
description: "يُعد تعريف الصف مكون تقرير، أو كتلة إنشاء، يحدد محتويات كل صف في تقرير مالي. ويمكن دمج تعريف الصف مع تعريفات الأعمدة وتعريفات شجرة التقارير وتعريفات التقارير لإنشاء مجموعة من كتل الإنشاء التي يمكن استخدامها من قِبل العديد من الشركات."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 06a75889e62cbba6e47a8543cf663868df5ae2e3
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="76be9-104">تعريفات الصفوف في مصمم التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="76be9-104">Row definitions in financial report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="76be9-105">يُعد تعريف الصف مكون تقرير، أو كتلة إنشاء، يحدد محتويات كل صف في تقرير مالي.</span><span class="sxs-lookup"><span data-stu-id="76be9-105">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="76be9-106">ويمكن دمج تعريف الصف مع تعريفات الأعمدة وتعريفات شجرة التقارير وتعريفات التقارير لإنشاء مجموعة من كتل الإنشاء التي يمكن استخدامها من قِبل العديد من الشركات.</span><span class="sxs-lookup"><span data-stu-id="76be9-106">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

<a name="create-a-row-definition"></a><span data-ttu-id="76be9-107">إنشاء تعريف صف</span><span class="sxs-lookup"><span data-stu-id="76be9-107">Create a row definition</span></span>
-----------------------

1.  <span data-ttu-id="76be9-108">في مصمم التقارير، في جزء التنقل، انقر فوق **تعريفات الصفوف**.</span><span class="sxs-lookup"><span data-stu-id="76be9-108">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2.  <span data-ttu-id="76be9-109">في القائمة **ملف**، انقر فوق **جديد**، ثم انقر فوق **تعريف الصف**.</span><span class="sxs-lookup"><span data-stu-id="76be9-109">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="76be9-110">لمزيد من المعلومات حول محتوى كل خلية، راجع [تعديل خلايا تعريف الصف](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="76be9-110">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="76be9-111">فتح تعريف صف</span><span class="sxs-lookup"><span data-stu-id="76be9-111">Open a row definition</span></span>
1.  <span data-ttu-id="76be9-112">في مصمم التقارير، في جزء التنقل، انقر فوق **تعريفات الصفوف**.</span><span class="sxs-lookup"><span data-stu-id="76be9-112">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2.  <span data-ttu-id="76be9-113">انقر نقرًا مزدوجًا فوق تعريف الصف لفتحه.</span><span class="sxs-lookup"><span data-stu-id="76be9-113">Double-click the name of the row definition to open.</span></span>
3.  <span data-ttu-id="76be9-114">لعرض أي كتل إنشاء مقترنة بتعريف الصف، انقر نقراً مزدوجاً فوق تعريف الصف، ثم حدد **الاقترانات**.</span><span class="sxs-lookup"><span data-stu-id="76be9-114">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="76be9-115"> محتويات تعريف صف</span><span class="sxs-lookup"><span data-stu-id="76be9-115">Contents of a row definition</span></span>
<span data-ttu-id="76be9-116">بإمكان تعريف الصف أن يحتوي على ما يصل لغاية 20,000 من صفوف الأبعاد المالية، وبإمكانه أن يحتوي على المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="76be9-116">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

-   <span data-ttu-id="76be9-117">نص وصفي يضيف معنى إلى التقرير عن طريق إنشاء عناوين المقاطع والأسطر والمسافات، مثل **النقد** أو **إجمالي الإيرادات**.</span><span class="sxs-lookup"><span data-stu-id="76be9-117">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
-   <span data-ttu-id="76be9-118">‏‫ارتباطات إلى بيانات مالية يمكنها أن تتضمن قيم الأبعاد في Microsoft Dynamics 365 for Finance and Operations **ملاحظة:** يمكنك إعداد تعريف صف لسحب البيانات من نظام الأبعاد المالية في كل مرة يتم فيها إنشاء التقرير.‬</span><span class="sxs-lookup"><span data-stu-id="76be9-118">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 for Finance and Operations **Note:** You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>
-   <span data-ttu-id="76be9-119">معادلات وإجماليات الصفوف المستندة إلى البيانات المالية المرتبطة</span><span class="sxs-lookup"><span data-stu-id="76be9-119">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="76be9-120">عادةً ما يحتوي كل صف في تعريف صف على أحد الأنواع التالية من المعلومات:</span><span class="sxs-lookup"><span data-stu-id="76be9-120">Usually, each row in a row definition contains one of the following types of information:</span></span>

-   <span data-ttu-id="76be9-121">مراجع إلى نظام الأبعاد المالية</span><span class="sxs-lookup"><span data-stu-id="76be9-121">References to the financial dimensions system</span></span>
-   <span data-ttu-id="76be9-122">الإجماليات أو العمليات الحسابية التي تستند إلى البيانات</span><span class="sxs-lookup"><span data-stu-id="76be9-122">Totals or calculations that are based on the data</span></span>
-   <span data-ttu-id="76be9-123">التنسيق</span><span class="sxs-lookup"><span data-stu-id="76be9-123">Formatting</span></span>

<span data-ttu-id="76be9-124">هناك طريقتان لإدخال المعلومات في تعريف الصف:</span><span class="sxs-lookup"><span data-stu-id="76be9-124">There are two methods for entering information in a row definition:</span></span>

-   <span data-ttu-id="76be9-125">إدخال معلومات الصف يدويًا في تعريف صف جديد.</span><span class="sxs-lookup"><span data-stu-id="76be9-125">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="76be9-126">لمزيد من المعلومات، راجع [تعديل خلايا تعريفات الصفوف](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="76be9-126">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
-   <span data-ttu-id="76be9-127">استخدام مصمم التقارير لسحب معلومات الصف مباشرة من الأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="76be9-127">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="76be9-128">لمزيد من المعلومات، راجع المقطع "المعادلات/الصفوف/الوحدات ذات الصلة‬" في [تعديل خلايا تعريف الصف‬](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="76be9-128">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="76be9-129"> إضافة أبعاد في تعريف صف</span><span class="sxs-lookup"><span data-stu-id="76be9-129">Add dimensions in a row definition</span></span>
<span data-ttu-id="76be9-130">البُعد هو تقاطع للبيانات والقيم.</span><span class="sxs-lookup"><span data-stu-id="76be9-130">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="76be9-131">يمكنك تجميع القيم والبيانات في مصمم التقارير.</span><span class="sxs-lookup"><span data-stu-id="76be9-131">You can group data and values in report designer.</span></span> <span data-ttu-id="76be9-132">ويمكنك عندئذٍ تصنيف الحركات وتحليلها بمزيد من التفصيل.</span><span class="sxs-lookup"><span data-stu-id="76be9-132">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="76be9-133">يمكنك استخدام مربع الحوار **إدراج صفوف من الأبعاد** لإضافة صفوف متعددة إلى تعريف صف في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="76be9-133">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="76be9-134">ويعرض مربع الحوار عمودًا واحدً لكل بُعد.</span><span class="sxs-lookup"><span data-stu-id="76be9-134">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="76be9-135">يصف الجدول التالي المعلومات التي يمكنك تحديدها لكل بُعد.</span><span class="sxs-lookup"><span data-stu-id="76be9-135">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="76be9-136">خيار</span><span class="sxs-lookup"><span data-stu-id="76be9-136">Option</span></span>                | <span data-ttu-id="76be9-137">الوصف</span><span class="sxs-lookup"><span data-stu-id="76be9-137">Description</span></span>                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76be9-138">البعد</span><span class="sxs-lookup"><span data-stu-id="76be9-138">Dimension</span></span>             | <span data-ttu-id="76be9-139">النمط الذي يحدد البُعد المراد إضافته إلى تعريف الصف.</span><span class="sxs-lookup"><span data-stu-id="76be9-139">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="76be9-140">ويحتوي هذا النمط على حرف عطف واحد (\#) أو إشارة رقم (#) لكل منصب في الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="76be9-140">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="76be9-141">بشكل عام، استخدم كافة علامات العطف لبُعد الحساب الرئيسي وجميع علامات الأرقام للأبعاد الأخرى.</span><span class="sxs-lookup"><span data-stu-id="76be9-141">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="76be9-142">بداية نطاق الأبعاد</span><span class="sxs-lookup"><span data-stu-id="76be9-142">Dimension Range Start</span></span> | <span data-ttu-id="76be9-143">هي القيمة الأولى لهذا البُعد لإضافتها إلى تعريف الصف.</span><span class="sxs-lookup"><span data-stu-id="76be9-143">The first value for this dimension to add to the row definition.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="76be9-144">نهاية نطاق الأبعاد</span><span class="sxs-lookup"><span data-stu-id="76be9-144">Dimension Range End</span></span>   | <span data-ttu-id="76be9-145">القيمة الأخيرة لهذا البعد المراد إضافتها إلى تعريف الصف.</span><span class="sxs-lookup"><span data-stu-id="76be9-145">The last value for this dimension to add to the row definition.</span></span>                                                                                                                                                                                                                  |

<span data-ttu-id="76be9-146">لإضافة أبعاد إلى تعريف صف، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="76be9-146">To add dimensions to a row definition, follow these steps.</span></span>

1.  <span data-ttu-id="76be9-147">في مصمم التقارير انقر فوق **تعريفات الصفوف**، ثم افتح تعريف الصف لتعديله.</span><span class="sxs-lookup"><span data-stu-id="76be9-147">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2.  <span data-ttu-id="76be9-148">في القائمة **تحرير**، انقر فوق **إدراج صفوف من الأبعاد**.</span><span class="sxs-lookup"><span data-stu-id="76be9-148">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3.  <span data-ttu-id="76be9-149">في مربع الحوار **إدراج صفوف من الأبعاد**، في صف **الأبعاد**، حدد الخلية للبُعد الذي تريد نقله إلى تعريف الصف، ثم انقر فوق **الكل & & &**.</span><span class="sxs-lookup"><span data-stu-id="76be9-149">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4.  <span data-ttu-id="76be9-150">لتحديد تعريف الصف بحيث يقتصر على نطاق محدد من قيم الأبعاد، أدخل قيمة بُعد البداية في خلية **بداية نطاق الأبعاد**، ثم أدخل قيمة بُعد النهاية في خلية **نهاية نطاق الأبعاد**.</span><span class="sxs-lookup"><span data-stu-id="76be9-150">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="76be9-151">ولتضمين كافة القيم للبُعد المحدد، اترك هذه الخلايا فارغة.</span><span class="sxs-lookup"><span data-stu-id="76be9-151">To include all values for the selected dimension, leave these cells empty.</span></span> <span data-ttu-id="76be9-152">**ملاحظة:** قد لا تُظهر أحرف البدل (\* أو ؟) في نطاقات الأبعاد جميع النتائج التي تريدها، وهذا يتوقف على طريقة ترتيب البيانات بواسطة قاعدة بيانات ERP.</span><span class="sxs-lookup"><span data-stu-id="76be9-152">**Note:** Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>
5.  <span data-ttu-id="76be9-153">في حقل **كود صف البداية**، حدد كود الصف لقيمة البُعد الأول المراد إضافته إلى تعريف الصف.</span><span class="sxs-lookup"><span data-stu-id="76be9-153">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6.  <span data-ttu-id="76be9-154">في حقل **زيادة كل صف بمقدار**، حدد الفجوة بين أكواد الصفوف المتتالية.</span><span class="sxs-lookup"><span data-stu-id="76be9-154">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="76be9-155">على سبيل المثال، إذا كان كود الصف الأول هو 100 وقيمه الزيادة هي 30، فإن الصفوف الجديدة الأولى تشتمل على أكواد 100 و130، و160، و190، و220.</span><span class="sxs-lookup"><span data-stu-id="76be9-155">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="76be9-156">استخدم قيمة زيادة توفر مساحة لإدراج صفوف معادلة وتنسيق جديدة.‬</span><span class="sxs-lookup"><span data-stu-id="76be9-156">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7.  <span data-ttu-id="76be9-157">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="76be9-157">Click **OK**.</span></span> <span data-ttu-id="76be9-158">لكل قيمة من قيم الأبعاد المحددة، تتم إضافة بند واحد إلى تعريف الصف.</span><span class="sxs-lookup"><span data-stu-id="76be9-158">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="76be9-159"> ضبط التقريب في تعريف صف</span><span class="sxs-lookup"><span data-stu-id="76be9-159">Adjust rounding in a row definition</span></span>
<span data-ttu-id="76be9-160">إذا كان لديك ميزانية عمومية تم فيها تقريب المبالغ، فقد تكون المجاميع غير متوازنة.</span><span class="sxs-lookup"><span data-stu-id="76be9-160">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="76be9-161">قد تحدث هذه المشكلة إذا استخدمت خيار التقريب، على سبيل المثال، في تقرير ميزانية عمومية وقام تعريف التقرير هو أيضًا بتحديد التقريب.</span><span class="sxs-lookup"><span data-stu-id="76be9-161">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="76be9-162">يمكنك استخدام خيار **التسوية التقريبية‬** في تعريف الصف لتحقيق التوازن بين المبالغ الواردة في الميزانيات العمومية.</span><span class="sxs-lookup"><span data-stu-id="76be9-162">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="76be9-163">يمكنك إيقاف تشغيل التقريب أو تعديله على علامة تبويب **الإعدادات** في تعريف التقرير.</span><span class="sxs-lookup"><span data-stu-id="76be9-163">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="76be9-164">يعرض الجدول التالي كيفية تقريب المبالغ.</span><span class="sxs-lookup"><span data-stu-id="76be9-164">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="76be9-165">وفي هذا الجدول، تختلف إجماليات الصفين 100 و200 عند تشغيل التقريب.</span><span class="sxs-lookup"><span data-stu-id="76be9-165">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="76be9-166">كود الصف</span><span class="sxs-lookup"><span data-stu-id="76be9-166">Row code</span></span> | <span data-ttu-id="76be9-167">المبالغ دون تقريب</span><span class="sxs-lookup"><span data-stu-id="76be9-167">Amounts without rounding</span></span> | <span data-ttu-id="76be9-168">المبلغ بالتقريب إلى آلاف كاملة</span><span class="sxs-lookup"><span data-stu-id="76be9-168">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="76be9-169">100</span><span class="sxs-lookup"><span data-stu-id="76be9-169">100</span></span>      | <span data-ttu-id="76be9-170">3,600</span><span class="sxs-lookup"><span data-stu-id="76be9-170">3,600</span></span>                    | <span data-ttu-id="76be9-171">4</span><span class="sxs-lookup"><span data-stu-id="76be9-171">4</span></span>                                       |
| <span data-ttu-id="76be9-172">200</span><span class="sxs-lookup"><span data-stu-id="76be9-172">200</span></span>      | <span data-ttu-id="76be9-173">3,700</span><span class="sxs-lookup"><span data-stu-id="76be9-173">3,700</span></span>                    | <span data-ttu-id="76be9-174">4</span><span class="sxs-lookup"><span data-stu-id="76be9-174">4</span></span>                                       |
| <span data-ttu-id="76be9-175">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="76be9-175">Total</span></span>    | <span data-ttu-id="76be9-176">7,300</span><span class="sxs-lookup"><span data-stu-id="76be9-176">7,300</span></span>                    | <span data-ttu-id="76be9-177">8</span><span class="sxs-lookup"><span data-stu-id="76be9-177">8</span></span>                                       |

<span data-ttu-id="76be9-178">لتسوية التقريب في الميزانية العمومية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="76be9-178">To adjust rounding in a balance sheet, follow these steps.</span></span>

1.  <span data-ttu-id="76be9-179">في مصمم التقارير، انقر فوق **تعريفات الصفوف**، ثم افتح تعريف الصف لتعديله.</span><span class="sxs-lookup"><span data-stu-id="76be9-179">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2.  <span data-ttu-id="76be9-180">من قائمة **تحرير**، انقر فوق **تعديل التقريب**.</span><span class="sxs-lookup"><span data-stu-id="76be9-180">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3.  <span data-ttu-id="76be9-181">في مربع الحوار **التسويات التقريبية**، أدخل القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="76be9-181">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>
    -   <span data-ttu-id="76be9-182">**صف التسوية التقريبية** – كود الصف الذي يجب تسويته لموازنة الميزانية العمومية.</span><span class="sxs-lookup"><span data-stu-id="76be9-182">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    -   <span data-ttu-id="76be9-183">**صف إجمالي الأصول** – كود الصف للصف في الميزانية العمومية التي تحتوي على إجمالي الأصول.</span><span class="sxs-lookup"><span data-stu-id="76be9-183">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    -   <span data-ttu-id="76be9-184">**صف إجمالي الالتزامات وحق الملكية** – كود الصف للصف في الميزانية العمومية التي تحتوي على إجمالي الالتزامات وحق الملكية.</span><span class="sxs-lookup"><span data-stu-id="76be9-184">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    -   <span data-ttu-id="76be9-185">**حد مبلغ التسوية** – عدد صحيح موجب يعين الحد على التسويات التلقائية.</span><span class="sxs-lookup"><span data-stu-id="76be9-185">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="76be9-186">وتتم مقارنة هذا المبلغ بالقيمة المطلقة لفرق التقريب الفعلي.</span><span class="sxs-lookup"><span data-stu-id="76be9-186">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    <span data-ttu-id="76be9-187">**ملاحظة:**يجب ربط أكواد الصفوف هذه بالبيانات المالية.</span><span class="sxs-lookup"><span data-stu-id="76be9-187">**Note:** These row codes must be linked to your financial data.</span></span> <span data-ttu-id="76be9-188">وبعبارة أخرى، يجب أن يشتمل الصف على قيمة بُعد في خلية **الارتباط إلى الأبعاد المالية** الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="76be9-188">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="76be9-189">**لا** تشير إلى وصف (**DESC**)، أو صف محسوب (**CALC**)، أو صف تم تجميع إجماله (**TOT**).</span><span class="sxs-lookup"><span data-stu-id="76be9-189">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="76be9-190">ستتم الآن موازنة المبالغ في ميزانيتك العمومية بطريقة متساوية عند تشغيل التقريب.</span><span class="sxs-lookup"><span data-stu-id="76be9-190">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span> <span data-ttu-id="76be9-191">**ملاحظة:**يتم تطبيق حد التسوية استناداً خيار **دقة التقريب** الذي تم تحديده لتعريف التقرير.</span><span class="sxs-lookup"><span data-stu-id="76be9-191">**Note:** The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="76be9-192">على سبيل المثال، إذا قمت بتحديد تقريب التقرير بالآلاف وأدخلت **2** في حقل **حد مبلغ التسوية**، فستتلقى رسالة تحذير عندما تزداد القيمة في حقل **صف التسوية التقريبية** أو تنخفض بأكثر من 2,000 دولار.</span><span class="sxs-lookup"><span data-stu-id="76be9-192">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="76be9-193">تنسيق الصف ونص العمود</span><span class="sxs-lookup"><span data-stu-id="76be9-193">Format row and column text</span></span>
<span data-ttu-id="76be9-194">يمكنك تخصيص مظهر التقارير الخاصة بك بتغيير الخطوط وتنسيق النص.</span><span class="sxs-lookup"><span data-stu-id="76be9-194">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="76be9-195">تشرح الأقسام التالية كيفية تنسيق مظهر الصفوف والأعمدة في التقارير.</span><span class="sxs-lookup"><span data-stu-id="76be9-195">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="76be9-196">إدارة أنماط الخطوط</span><span class="sxs-lookup"><span data-stu-id="76be9-196">Manage font styles</span></span>

<span data-ttu-id="76be9-197">يمكنك إنشاء أنماط الخطوط وتعديلها في تقريرك.</span><span class="sxs-lookup"><span data-stu-id="76be9-197">You can create and modify font styles for your report.</span></span> <span data-ttu-id="76be9-198">ويمكنك بعدئذٍ تطبيق هذه الأنماط على المستند أو على صف أو عمود معين على التقرير.</span><span class="sxs-lookup"><span data-stu-id="76be9-198">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76be9-199">إنشاء نمط خط</span><span class="sxs-lookup"><span data-stu-id="76be9-199">Create a font style</span></span></td>
<td><ol>
<li><span data-ttu-id="76be9-200">في "مصمم التقرير"، في قائمة <strong>التنسيق</strong>، انقر فوق <strong>الأنماط والتنسيقات</strong>.</span><span class="sxs-lookup"><span data-stu-id="76be9-200">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="76be9-201">في مربع الحوار <strong>الأنماط والتنسيقات</strong>، انقر فوق <strong>جديد</strong>، ثم أدخل اسمًا فريدًا للنمط الجديد.</span><span class="sxs-lookup"><span data-stu-id="76be9-201">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="76be9-202">اختر تحديدات النمط، ثم انقر فوق <strong>موافق</strong>.</span><span class="sxs-lookup"><span data-stu-id="76be9-202">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76be9-203">تعديل نمط خط</span><span class="sxs-lookup"><span data-stu-id="76be9-203">Modify a font style</span></span></td>
<td><ol>
<li><span data-ttu-id="76be9-204">في "مصمم التقرير"، في قائمة <strong>التنسيق</strong>، انقر فوق <strong>الأنماط والتنسيقات</strong>.</span><span class="sxs-lookup"><span data-stu-id="76be9-204">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="76be9-205">حدد نمطًا لتعديله من مربع الحوار <strong>الأنماط والتنسيقات</strong>، ثم انقر فوق <strong>تعديل</strong>.</span><span class="sxs-lookup"><span data-stu-id="76be9-205">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="76be9-206">اختر تحديدات النمط، ثم انقر فوق <strong>موافق</strong>.</span><span class="sxs-lookup"><span data-stu-id="76be9-206">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76be9-207">تطبيق نمط خط</span><span class="sxs-lookup"><span data-stu-id="76be9-207">Apply a font style</span></span></td>
<td><ol>
<li><span data-ttu-id="76be9-208">في مصمم التقارير، في تعريف أو تعريف عمود أو في الرؤوس والتذييلات، حدد خلية واحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="76be9-208">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="76be9-209">من قائمة <strong>نمط</strong> في شريط الأدوات، حدد نمط خط.</span><span class="sxs-lookup"><span data-stu-id="76be9-209">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="76be9-210">تنسيق نص الصف</span><span class="sxs-lookup"><span data-stu-id="76be9-210">Format row text</span></span>

<span data-ttu-id="76be9-211">يتجاوز التنسيق المحدد في تعريف الصف أي تنسيق محدد في تعريف العمود وتعريف التقرير.</span><span class="sxs-lookup"><span data-stu-id="76be9-211">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="76be9-212">ويمكنك تعديل تنسيق النص باستخدام عناصر التحكم الموجودة على شريط أدوات التنسيق.</span><span class="sxs-lookup"><span data-stu-id="76be9-212">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="76be9-213">وعناصر التحكم هذه عبارة عن عناصر التحكم القياسية في Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="76be9-213">These controls are standard Microsoft Windows controls.</span></span>

1.  <span data-ttu-id="76be9-214">في مصمم التقارير، افتح تعريف الصف لتعديله.</span><span class="sxs-lookup"><span data-stu-id="76be9-214">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="76be9-215">حدد الخلايا التي تريد تنسيقها.</span><span class="sxs-lookup"><span data-stu-id="76be9-215">Select the cells to format.</span></span> <span data-ttu-id="76be9-216">ولتحديد خلايا متعددة، اضغط مع الاستمرار على المفتاح Ctrl بينما تقوم بتحديد الخلية.</span><span class="sxs-lookup"><span data-stu-id="76be9-216">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3.  <span data-ttu-id="76be9-217">انقر فوق زر شريط الأدوات للتنسيق المراد تطبيقه.</span><span class="sxs-lookup"><span data-stu-id="76be9-217">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="76be9-218">على سبيل المثال، لإنشاء مسافة بادئة لصف، حدد الصف، ثم انقر فوق **زيادة المسافة البادئة** ![زيادة المسافة البادئة](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "زيادة المسافة البادئة") على شريط الأدوات.</span><span class="sxs-lookup"><span data-stu-id="76be9-218">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="76be9-219">ضبط الأعمدة أثناء تصميم التقارير</span><span class="sxs-lookup"><span data-stu-id="76be9-219">Adjust columns while you design reports</span></span>

<span data-ttu-id="76be9-220">لتسهيل عرض الأعمدة التي تعمل فيها في تعريف الصف، يمكنك ضبط عرض العمود، ويمكنك أيضًا إخفاء (تصغير) أو إظهار الأعمدة في جزء طريقة العرض.</span><span class="sxs-lookup"><span data-stu-id="76be9-220">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="76be9-221">تؤثر التعديلات التي تقوم بإجرائها فقط في مظهر الأعمدة على الشاشة.</span><span class="sxs-lookup"><span data-stu-id="76be9-221">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="76be9-222">ولا تؤثر في تنسيق الأعمدة على التقارير.</span><span class="sxs-lookup"><span data-stu-id="76be9-222">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="76be9-223">تغيير عرض عمود في جزء طريقة العرض</span><span class="sxs-lookup"><span data-stu-id="76be9-223">Change the width of a column in the view pane</span></span>

1.  <span data-ttu-id="76be9-224">في مصمم التقارير، افتح تعريف الصف لتعديله.</span><span class="sxs-lookup"><span data-stu-id="76be9-224">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="76be9-225">في قائمة **التنسيق**، حدد **عرض العمود**.</span><span class="sxs-lookup"><span data-stu-id="76be9-225">On the **Format** menu, select **Column Width**.</span></span>
3.  <span data-ttu-id="76be9-226">في مربع حوار **عرض العمود‬**، أدخل قيمة، ثم انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="76be9-226">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="76be9-227">أو، يمكنك سحب الحد الأيمن لخلية عنوان عمود لتغيير عرض العمود.</span><span class="sxs-lookup"><span data-stu-id="76be9-227">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="76be9-228">إخفاء الأعمدة في جزء طريقة العرض</span><span class="sxs-lookup"><span data-stu-id="76be9-228">Hide columns in the view pane</span></span>

1.  <span data-ttu-id="76be9-229">في مصمم التقارير، افتح تعريف الصف لتعديله.</span><span class="sxs-lookup"><span data-stu-id="76be9-229">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="76be9-230">حدد العمود أو الأعمدة التي تريد تصغيرها.</span><span class="sxs-lookup"><span data-stu-id="76be9-230">Select the column or columns to minimize.</span></span>
3.  <span data-ttu-id="76be9-231">انقر بزر الماوس الأيمن، ثم انقر فوق **إخفاء**.</span><span class="sxs-lookup"><span data-stu-id="76be9-231">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="76be9-232">إظهار كافة الأعمدة المخفية في جزء طريقة العرض</span><span class="sxs-lookup"><span data-stu-id="76be9-232">Show all hidden columns in the view pane</span></span>

1.  <span data-ttu-id="76be9-233">في مصمم التقارير، افتح تعريف الصف لتعديله.</span><span class="sxs-lookup"><span data-stu-id="76be9-233">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="76be9-234">انقر بزر الماوس الأيمن فوق العمود المصغر لعرضه، ثم انقر فوق **إظهار**.</span><span class="sxs-lookup"><span data-stu-id="76be9-234">Right-click the minimized column to display, and then click **Unhide**.</span></span>


<a name="see-also"></a><span data-ttu-id="76be9-235">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="76be9-235">See also</span></span>
--------

[<span data-ttu-id="76be9-236">التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="76be9-236">Financial reporting</span></span>](financial-reporting-intro.md)




