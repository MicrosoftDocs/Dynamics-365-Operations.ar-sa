---
title: تحسينات في تتبع نتائج التقارير الإلكترونية (ER) المنشأة والمقارنة مع القيم الأساسية
description: يوفر هذا الموضوع معلومات حول تم تحسين ميزة ER الأساسية في Microsoft Dynamics 365 for Finance and Operationsالإصدار 10.0.3 (يونيو 2019).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 1e144e2623f3ddfafaee749bb334de40ef5aec1b
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578208"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="29971-103">تحسينات في تتبع نتائج التقارير الإلكترونية (ER) المنشأة والمقارنة مع القيم الأساسية</span><span class="sxs-lookup"><span data-stu-id="29971-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="29971-104">يصف هذا الموضوع مجموعة التحسينات الأولى التي تم إجراؤها للميزة الأساسية في إطار عمل التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="29971-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="29971-105">وتتوفر هذه التحسينات Microsoft Dynamics 365 for Finance and Operationsالإصدار 10.0.3 (يونيو 2019) والإصدارات الأحدث.</span><span class="sxs-lookup"><span data-stu-id="29971-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="29971-106">أتمته إعداد القواعد الأساسية</span><span class="sxs-lookup"><span data-stu-id="29971-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="29971-107">يشرح موضوع [‏‫تتبع نتائج التقارير المنشأة ومقارنتها بالقيم الأساسية‬](er-trace-reports-compare-baseline.md) كيفية تكوين إطار عمل ER لجمع معلومات حول عمليات تنفيذ تنسيق ER وتقييم نتائج عمليات التنفيذ هذه.</span><span class="sxs-lookup"><span data-stu-id="29971-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="29971-108">يوضح المثال الوارد في هذا الموضوع الخطوات التي يجب أن يتم إكمالها.</span><span class="sxs-lookup"><span data-stu-id="29971-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="29971-109">فيما يلي بعض الخطوات:</span><span class="sxs-lookup"><span data-stu-id="29971-109">Here are some of the steps:</span></span>

- <span data-ttu-id="29971-110">تشغيل تنسيق ER لإنشاء ملف صادر، وتخزين الملف محليا.</span><span class="sxs-lookup"><span data-stu-id="29971-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="29971-111">إضافة الملف المخزن محليا كمرفق للأساس الذي تمت إضافته لتنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="29971-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="29971-112">تكوين قاعدة الأساس للأساس المضاف.</span><span class="sxs-lookup"><span data-stu-id="29971-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="29971-113">يتضمن هذا التكوين الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="29971-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="29971-114">تحديد عنصر تنسيق ER الذي تم استخدامه في إنشاء ملف صادر.</span><span class="sxs-lookup"><span data-stu-id="29971-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="29971-115">حدد المرفق الذي يشير إلى الملف الصادر الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="29971-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="29971-116">يجب إجراء هذه الخطوات يدويا، بالرغم من أن إمكانيات ER الجديدة تتيح التنفيذ التلقائي لها.</span><span class="sxs-lookup"><span data-stu-id="29971-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="29971-117">لتعلم المزيد حول هذه الميزة، أكمل المثال التالي.</span><span class="sxs-lookup"><span data-stu-id="29971-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="29971-118">مثال: أتمتة إعداد القواعد الأساسية</span><span class="sxs-lookup"><span data-stu-id="29971-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="29971-119">لإكمال الخطوات الموجودة في هذا المثال، يجب أولا إكمال الخطوات في المثال في الموضوع [‏‫تتبع نتائج التقارير المنشأة ومقارنتها بالقيم الأساسية‬](er-trace-reports-compare-baseline.md)، حتى القسم "إضافة أساس جديد لتنسيق ER المصمم".</span><span class="sxs-lookup"><span data-stu-id="29971-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="29971-120">مراجعة الأساس المضاف</span><span class="sxs-lookup"><span data-stu-id="29971-120">Review added baseline</span></span>

1. <span data-ttu-id="29971-121">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="29971-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="29971-122">حدد **الأسس**.</span><span class="sxs-lookup"><span data-stu-id="29971-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="29971-123">يتوفر زر **الأسس** في جزء الإجراء فقط عند تشغيل معلمة مستخدم ER **تشغيل في وضع التصحيح** للشركة الحالية.</span><span class="sxs-lookup"><span data-stu-id="29971-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="29971-124">تمت إضافة الأساس لـ **تنسيق لمعرفة أسس ER** المحدد، ولكن لم تتم إضافة قواعد الأساس لهذا الأساس بعد.</span><span class="sxs-lookup"><span data-stu-id="29971-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="29971-125">![صفحة أسس تنسيق التقارير الإلكترونية](media/GER-BaselineSample-AddBaseline2.PNG "لقطة شاشة لصفحة أسس تنسيق التقارير الإلكترونية")</span><span class="sxs-lookup"><span data-stu-id="29971-125">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="29971-126">إنشاء قاعدة أساس جديدة</span><span class="sxs-lookup"><span data-stu-id="29971-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="29971-127">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="29971-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="29971-128">في الشجرة، قم بتوسيع **النموذج لتعلم أسس ER**.</span><span class="sxs-lookup"><span data-stu-id="29971-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="29971-129">في الشجرة ، حدد **النموذج لتعلم أسس ER\\التنسيق لتعلم أسس ER**.</span><span class="sxs-lookup"><span data-stu-id="29971-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="29971-130">في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="29971-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="29971-131">في حقل **معرف الإدخال**، أدخل **1**.</span><span class="sxs-lookup"><span data-stu-id="29971-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="29971-132">قم بتعيين خيار **إنشاء ملفات أساس** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="29971-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="29971-133">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="29971-133">Select **OK**.</span></span>
8. <span data-ttu-id="29971-134">حدد **الأسس**.</span><span class="sxs-lookup"><span data-stu-id="29971-134">Select **Baselines**.</span></span>

    <span data-ttu-id="29971-135">![صفحة أسس تنسيق التقارير الإلكترونية](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "لقطة شاشة لصفحة أسس تنسيق التقارير الإلكترونية")</span><span class="sxs-lookup"><span data-stu-id="29971-135">![Electronic reporting format baselines page](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="29971-136">تم تلقائيًا إرفاق الملف الصادر المنشأ بالأساس الخاص بتنسيق ER الذي تم تنفيذه.</span><span class="sxs-lookup"><span data-stu-id="29971-136">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="29971-137">تمت إضافة قاعدة الأساس تلقائيا إلى هذا الأساس وتحتوي أيضًا على مرجع للملف المرفق.</span><span class="sxs-lookup"><span data-stu-id="29971-137">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="29971-138">في حقل **الاسم**، أدخل **الأساس 1**.</span><span class="sxs-lookup"><span data-stu-id="29971-138">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="29971-139">في حقل **قناع اسم الملف**، أدخل **.xml**.</span><span class="sxs-lookup"><span data-stu-id="29971-139">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="29971-140">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="29971-140">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="29971-141">شغل التنسيق</span><span class="sxs-lookup"><span data-stu-id="29971-141">Run the format</span></span>

<span data-ttu-id="29971-142">أنت الآن جاهز لإكمال الخطوات المتبقية في المثال الموجود في موضوع [تتبع نتائج التقارير المنشأة ومقارنتها بالقيم الأساسية](er-trace-reports-compare-baseline.md)، بدءا من القسم "تشغيل تنسيق ER المصمم ومراجعة السجل لتحليل النتائج".</span><span class="sxs-lookup"><span data-stu-id="29971-142">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="29971-143">عند حذف قاعدة الأساس المضافة تلقائيا في علامة التبويب السريع **الأسس**، لا يتم حذف المرفق المشار إليه تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="29971-143">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="29971-144">تكوين الأساس بحيث يتجاهل الأجزاء المتغيرة باستمرار في إخراج ER</span><span class="sxs-lookup"><span data-stu-id="29971-144">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="29971-145">عندما يتم تصميم تنسيق ER ليحتوي على المعلومات التي تغيرت عند تشغيل التنسيق، عندئذ يلزم أن يستخدم التنسيق ميزة ER الأساسية لمقارنه النتائج التي تم إنشاؤها بقيم الأساس.</span><span class="sxs-lookup"><span data-stu-id="29971-145">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="29971-146">علي سبيل المثال، قد تكون المعلومات هي تاريخ المعالجة ووقتها أو المعرف الفريد للمستند الذي تم إنشاؤه بتنسيقات مختلفة (المعرف الفريد العمومي \[ (GUID\]، وهكذا).</span><span class="sxs-lookup"><span data-stu-id="29971-146">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="29971-147">تسمح لك إمكانات ER الجديدة بتكوين قاعدة الأساس بحيث تتجاهل العناصر القابلة للتغيير الخاصة بتنسيق ER عند تشغيل التنسيق بغرض مقارنة قيم الأساس بنتائج تنفيذ التنسيق.</span><span class="sxs-lookup"><span data-stu-id="29971-147">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="29971-148">لتعلم المزيد حول هذه الميزة، أكمل المثال التالي.</span><span class="sxs-lookup"><span data-stu-id="29971-148">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="29971-149">مثال: تكوين الأساس بحيث يتجاهل الأجزاء المتغيرة باستمرار في إخراج ER</span><span class="sxs-lookup"><span data-stu-id="29971-149">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="29971-150">لإكمال الخطوات الموجودة في هذا المثال، يجب أولا إكمال الخطوات في المثال في الموضوع [‏‫تتبع نتائج التقارير المنشأة ومقارنتها بالقيم الأساسية‬](er-trace-reports-compare-baseline.md).</span><span class="sxs-lookup"><span data-stu-id="29971-150">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="29971-151">تعديل تنسيق ER المكوّن</span><span class="sxs-lookup"><span data-stu-id="29971-151">Modify a configured ER format</span></span>

1. <span data-ttu-id="29971-152">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="29971-152">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="29971-153">في الشجرة، قم بتوسيع **النموذج لتعلم أسس ER**.</span><span class="sxs-lookup"><span data-stu-id="29971-153">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="29971-154">في الشجرة ، حدد **النموذج لتعلم أسس ER\\التنسيق لتعلم أسس ER**.</span><span class="sxs-lookup"><span data-stu-id="29971-154">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="29971-155">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="29971-155">Select **Designer**.</span></span>
5. <span data-ttu-id="29971-156">في الشجرة، حدد **إخراج\\مستند**.</span><span class="sxs-lookup"><span data-stu-id="29971-156">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="29971-157">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="29971-157">Select **Add**.</span></span>
7. <span data-ttu-id="29971-158">في مربع الحوار المنسدل، في الشجرة، حدد **XML\\سمة**.</span><span class="sxs-lookup"><span data-stu-id="29971-158">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="29971-159">في حقل **الاسم**، أدخل **ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="29971-159">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="29971-160">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="29971-160">Select **OK**.</span></span>
10. <span data-ttu-id="29971-161">في علامة تبويب **التعيين**في الشرجة، حدد **إخراج\\مستند\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="29971-161">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="29971-162">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="29971-162">Select **Edit formula**.</span></span>
12. <span data-ttu-id="29971-163">في حقل **المعادلة**، أدخل العبارة التالية: **DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="29971-163">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="29971-164">حدد **حفظ**، ثم قم بتحديد **اختبار**.</span><span class="sxs-lookup"><span data-stu-id="29971-164">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="29971-165">حدد **اختبار** مرة أخرى لإعادة اختبار التعبير المكون.</span><span class="sxs-lookup"><span data-stu-id="29971-165">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="29971-166">![صفحة مصمم المعادلة](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "لقطة شاشة لصفحة مصمم المعادلة")</span><span class="sxs-lookup"><span data-stu-id="29971-166">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="29971-167">تعرض علامة التبويب **نتيجة الاختبار** أن التعبير المكون يقوم بإرجاع قيمة وقت وتاريخ مختلفة عندما يتم استدعاؤه.</span><span class="sxs-lookup"><span data-stu-id="29971-167">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="29971-168">أغلق صفحة **مصمم المعادلة**، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="29971-168">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="29971-169">![صفحة مصمم التنسيق](media/GER-BaselineSample-FormatMappingDesign2.PNG "لقطة شاشة لصفحة مصمم التنسيق")</span><span class="sxs-lookup"><span data-stu-id="29971-169">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="29971-170">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="29971-170">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="29971-171">إزالة قاعدة أساس موجودة</span><span class="sxs-lookup"><span data-stu-id="29971-171">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="29971-172">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="29971-172">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="29971-173">حدد **الأسس**.</span><span class="sxs-lookup"><span data-stu-id="29971-173">Select **Baselines**.</span></span>
3. <span data-ttu-id="29971-174">في قائمه الأسس، حدد الأساس الذي تم تكوينه لـ **تنسيق لمعرفة أسس ER**.</span><span class="sxs-lookup"><span data-stu-id="29971-174">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="29971-175">في علامة التبويب السريع **الأسس**، حدد **حذف** لإزالة قاعدة الأساس التي قمت بتكوينها مسبقا.</span><span class="sxs-lookup"><span data-stu-id="29971-175">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="29971-176">![صفحة أسس تنسيق التقارير الإلكترونية](media/GER-BaselineSample-AddBaseline3.PNG "لقطة شاشة لصفحة أسس تنسيق التقارير الإلكترونية")</span><span class="sxs-lookup"><span data-stu-id="29971-176">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="29971-177">تعريف عمليات الاستبدال لروابط تنسيق ER المصمم</span><span class="sxs-lookup"><span data-stu-id="29971-177">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="29971-178">في صفحة **التكوينات**، في علامة التبويب السريع **الاستبدالات**، حدد **تحديد المكونات**.</span><span class="sxs-lookup"><span data-stu-id="29971-178">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="29971-179">في شجرة مكونات التنسيق، قم بتوسيع **الإخراج**، وقم بتوسيع **الإخراج\\المستند**، ثم حدد خانة الاختيار **الإخراج\\المستند\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="29971-179">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>
3. <span data-ttu-id="29971-180">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="29971-180">Select **OK**.</span></span>

<span data-ttu-id="29971-181">![صفحة أسس تنسيق التقارير الإلكترونية](media/GER-BaselineSample-AddBaseline4.PNG "لقطة شاشة لصفحة أسس تنسيق التقارير الإلكترونية")</span><span class="sxs-lookup"><span data-stu-id="29971-181">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="29971-182">تمت إضافة مكون التنسيق ER المحدد إلى قائمة المكونات في علامة التبويب السريع **الاستبدالات**.</span><span class="sxs-lookup"><span data-stu-id="29971-182">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="29971-183">عند تشغيل تنسيق ER الأساس في وضع التصحيح، فإن ربط التنسيق لكل مكون سيتم استبداله بالربط الموضح في عمود **الربط**.</span><span class="sxs-lookup"><span data-stu-id="29971-183">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="29971-184">لتغيير الربط الافتراضي لمكون مسرد في علامة التبويب السريع **الاستبدالات**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="29971-184">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="29971-185">إنشاء قاعدة أساس جديدة</span><span class="sxs-lookup"><span data-stu-id="29971-185">Make a new baseline rule</span></span>

<span data-ttu-id="29971-186">اتبع الخطوات الموجودة في قسم "مثال: أتمته إعداد القواعد الأساسية‬" الموجود سابقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="29971-186">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="29971-187">يحذرك الإخطار من أنه تم إنشاء الملف الصادر باستخدام إعدادات الأساس، وأن الاستبدال الإجباري لروابط التنسيق قد حدث.</span><span class="sxs-lookup"><span data-stu-id="29971-187">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="29971-188">![إخطار على صفحة التكوينات](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "لقطة شاشة لإخطار على صفحة التكوينات")</span><span class="sxs-lookup"><span data-stu-id="29971-188">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="29971-189">منع التحذيرات حول استبدال روابط التنسيق</span><span class="sxs-lookup"><span data-stu-id="29971-189">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="29971-190">من خلال تعيين معلمات ER محددة، يمكنك منع الإخطارات التي تحذر من استبدال روابط التنسيق.</span><span class="sxs-lookup"><span data-stu-id="29971-190">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="29971-191">يمكن أن يكون هذا المنع مفيدا عند استبدال روابط التنسيق في وضع غير مراقب باستخدام Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="29971-191">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="29971-192">في هذه الحالة، يمكن اعتبار التحذير فشلا لحالة الاختبار التي يتم تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="29971-192">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="29971-193">في صفحة **التكوينات**، في جزء الإجراء، في علامة التبويب **التكوينات**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="29971-193">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="29971-194">قم بتعيين خيار **منع تحذيرات الأساس** على **نعم**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="29971-194">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="29971-195">مراجعة ملف الأساس المنشأ</span><span class="sxs-lookup"><span data-stu-id="29971-195">Review the generated baseline file</span></span>

1. <span data-ttu-id="29971-196">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="29971-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="29971-197">حدد **الأسس**.</span><span class="sxs-lookup"><span data-stu-id="29971-197">Select **Baselines**.</span></span>
3. <span data-ttu-id="29971-198">حدد **المرفقات**.</span><span class="sxs-lookup"><span data-stu-id="29971-198">Select **Attachments**.</span></span>
    > [!NOTE]
    > <span data-ttu-id="29971-199">يحتوي الملف الذي تم إنشاؤه على نص تاريخ ووقت المعالجة (**"#"**) من الربط الذي تم تكوينه في قاعدة الأساس المضافة، وليس من ربط التنسيق.</span><span class="sxs-lookup"><span data-stu-id="29971-199">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>
    
4. <span data-ttu-id="29971-200">أغلق صفحة**المرفقات**.</span><span class="sxs-lookup"><span data-stu-id="29971-200">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="29971-201">تشغيل تنسيق ER المصمم ومراجعة السجل لتحليل النتائج</span><span class="sxs-lookup"><span data-stu-id="29971-201">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="29971-202">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="29971-202">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="29971-203">في الشجرة، قم بتوسيع **النموذج لتعلم أسس ER**.</span><span class="sxs-lookup"><span data-stu-id="29971-203">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="29971-204">في الشجرة ، حدد **النموذج لتعلم أسس ER\\التنسيق لتعلم أسس ER**.</span><span class="sxs-lookup"><span data-stu-id="29971-204">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="29971-205">في علامة التبويب السريعة **الإصدارات** حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="29971-205">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="29971-206">في حقل **معرف الإدخال**، اكتب **1**.</span><span class="sxs-lookup"><span data-stu-id="29971-206">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="29971-207">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="29971-207">Select **OK**.</span></span>
7. <span data-ttu-id="29971-208">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **سجلات تصحيح التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="29971-208">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="29971-209">يحتوي سجل التنفيذ هذا على معلومات حول نتائج مقارنة الملف الذي تم إنشاؤه مع الأساس المكون.</span><span class="sxs-lookup"><span data-stu-id="29971-209">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="29971-210">ويشير السجل إلى أن الملف الذي تم إنشاؤه والأساس متساويان، حتى وإن كان التنسيق الذي تم تنفيذه يحتوي على الربط لإدخال قيمة تاريخ ووقت التغيير باستمرار في الملف الصادر.</span><span class="sxs-lookup"><span data-stu-id="29971-210">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="29971-211">على الرغم من أنه تم إنشاء الملف الصادر باستخدام إعدادات الأساس التي تفرض استبدال روابط التنسيق، لكنك لن تتلقى أي تحذيرات حول الاستبدال.</span><span class="sxs-lookup"><span data-stu-id="29971-211">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="29971-212">تبادل إعدادات الأساس بين البيئات</span><span class="sxs-lookup"><span data-stu-id="29971-212">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="29971-213">تصدير إعدادات الأساس</span><span class="sxs-lookup"><span data-stu-id="29971-213">Export baseline settings</span></span>

<span data-ttu-id="29971-214">تتيح إمكانات التقارير الإلكترونية الجديدة لك تصدير إعدادات الأساس لتنسيق التقارير الإلكترونية المحدد من البيئة الحالية وتخزينها كملفات XML.</span><span class="sxs-lookup"><span data-stu-id="29971-214">The new ER capabilities let you export baseline settings for the selected ER format from the current environment and store them as XML files.</span></span> 

<span data-ttu-id="29971-215">لتصدير إعدادات الأساس، من صفحة **أسس التنسيق للتقارير الإلكترونية**، حدد **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="29971-215">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="29971-216">استيراد إعدادات الأساس</span><span class="sxs-lookup"><span data-stu-id="29971-216">Import baseline settings</span></span>

<span data-ttu-id="29971-217">يمكن استيراد إعدادات الأساس التي تم تصديرها إلى بيئة مختلفة.</span><span class="sxs-lookup"><span data-stu-id="29971-217">Exported baseline settings can be imported into a different environment.</span></span> <span data-ttu-id="29971-218">يجب استيراد البيئة أولا كتنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="29971-218">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="29971-219">بعد ذلك يمكنك استيراد إعدادات الأساس.</span><span class="sxs-lookup"><span data-stu-id="29971-219">You can then import the baseline settings.</span></span>

<span data-ttu-id="29971-220">لاستيراد إعدادات الأساس من ملف XML مخزن محليا، في صفحة **أسس تنسيق التقارير الإلكترونية**، حدد **استيراد**، ثم حدد **استعراض** لتحديد ملف XML.</span><span class="sxs-lookup"><span data-stu-id="29971-220">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="29971-221">![مربع حوار استيراد إعدادات الأساس](media/GER-BaselineSample-ImportBaseline1.PNG "لقطة شاشة لمربع حوار استيراد إعدادات الأساس")</span><span class="sxs-lookup"><span data-stu-id="29971-221">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="29971-222">لاستيراد إعدادات الأساس من ملف XML المخزن في خادم Microsoft SharePoint، استنادا إلى إعدادات إدارة المستندات الحالية ونوع المستند المحدد، في صفحة **أسس تنسيق التقارير الإلكترونية**، حدد **استيراد من المصدر**.</span><span class="sxs-lookup"><span data-stu-id="29971-222">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="29971-223">ثم حدد نوع المستند وملف XML.</span><span class="sxs-lookup"><span data-stu-id="29971-223">Then select the document type and the XML file.</span></span> <span data-ttu-id="29971-224">يجب تكوين نوع المستند المطلوب للوصول إلى مجلد SharePoint مقدما.</span><span class="sxs-lookup"><span data-stu-id="29971-224">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="29971-225">![مربع حوار الاستيراد من المصدر](media/GER-BaselineSample-ImportBaseline2.PNG "لقطة شاشة لمربع حوار الاستيراد من المصدر")</span><span class="sxs-lookup"><span data-stu-id="29971-225">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="29971-226">يمكنك استخدام مسجل المهام لتسجيل خطوات تحديد نوع المستند المطلوب واسم الملف في مربع الحوار **استيراد من المصدر**.</span><span class="sxs-lookup"><span data-stu-id="29971-226">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="29971-227">بهذه الطريقة، يمكنك الاحتفاظ بإعدادات الأساس المطلوبة على خادم SharePoint ثم استيرادها تلقائيا من خلال تشغيل تسجيل المهام عند تشغيل الاختبارات المؤتمتة باستخدام Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="29971-227">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="29971-228">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="29971-228">Additional resources</span></span>

- [<span data-ttu-id="29971-229">تتبع نتائج التقارير المنشأة ومقارنتها بقيم الأساس</span><span class="sxs-lookup"><span data-stu-id="29971-229">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="29971-230">مسجل المهام</span><span class="sxs-lookup"><span data-stu-id="29971-230">Task recorder</span></span>](../user-interface/task-recorder.md)
