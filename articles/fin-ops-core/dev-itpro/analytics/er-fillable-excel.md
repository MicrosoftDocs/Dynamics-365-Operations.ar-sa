---
title: تصميم تكوين لإنشاء مستندات بتنسيق Excel
description: يصف هذا الموضوع كيفية تصميم تنسيق التقارير الإلكترونية (ER) لملء قالب Excel، ثم إنشاء مستندات صادرة بتنسيق Excel.
author: NickSelin
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c8d939fef4fd0f9e189ca37318c2c0306511785
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893898"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="92f98-103">تصميم تكوين لإنشاء المستندات بتنسيق Excel</span><span class="sxs-lookup"><span data-stu-id="92f98-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="92f98-104">يمكن تصميم تكوين لتنسيق [التقارير الإلكترونية (ER)](general-electronic-reporting.md) يتضمن [مكون تنسيق](general-electronic-reporting.md#FormatComponentOutbound) ER والذي يمكنك تكوينه لإنشاء مستند صادر بتنسيق مصنف Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="92f98-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="92f98-105">يجب استخدام مكونات تنسيق ER المحددة لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="92f98-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="92f98-106">لمعرفة المزيد حول هذه الميزة، اتبع الخطوات الواردة في موضوع، [تصميم تكوين لإنشاء التقارير بتنسيق OPENXML](tasks/er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="92f98-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="92f98-107">إضافة تنسيق ER جديد</span><span class="sxs-lookup"><span data-stu-id="92f98-107">Add a new ER format</span></span>

<span data-ttu-id="92f98-108">عند إضافة تكوين لتنسيق ER جديد لإنشاء مستند صادر بتنسيق مصنف Excel، يجب عليك إما تحديد قيمة **Excel** لسمة **نوع التنسيق** للتنسيق أو ترك سمة **نوع التنسيق** فارغة.</span><span class="sxs-lookup"><span data-stu-id="92f98-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="92f98-109">إذا قمت بتحديد **Excel**، يمكنك تكوين التنسيق لإنشاء مستند صادر بتنسيق Excel فقط.</span><span class="sxs-lookup"><span data-stu-id="92f98-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="92f98-110">إذا تركت السمة فارغة، يمكنك تكوين التنسيق لإنشاء مستند صادر بأي تنسيق يدعمه إطار عمل ER.</span><span class="sxs-lookup"><span data-stu-id="92f98-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="92f98-111">لتكوين مكون تنسيق ER للتكوين، حدد **المصمم** في جزء الإجراءات، وافتح مكون تنسيق ER للتحرير في مصمم تشغيل التقارير الإلكترونية‬.</span><span class="sxs-lookup"><span data-stu-id="92f98-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![صفحة التكوينات](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="92f98-113">مكون ملف Excel</span><span class="sxs-lookup"><span data-stu-id="92f98-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="92f98-114">إدخال يدوي</span><span class="sxs-lookup"><span data-stu-id="92f98-114">Manual entry</span></span>

<span data-ttu-id="92f98-115">يجب إضافة مكون **ملف\\Excel** إلى تنسيق ER الذي تم تكوينه لإنشاء مستند صادر بتنسيق Excel.</span><span class="sxs-lookup"><span data-stu-id="92f98-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![مكون ملف/ Excel](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="92f98-117">لتحديد مخطط المستند الصادر، قم بإرفاق مصنف Excel يتضمن الملحق .xlsx إلى مكون **ملف\\Excel** كقالب للمستندات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="92f98-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="92f98-118">عندما تقوم بإرفاق قالب يدويًا، يجب عليك استخدام [نوع مستند](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types) تم تكوينه لهذا الغرض في [معلمات ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span><span class="sxs-lookup"><span data-stu-id="92f98-118">When you manually attach a template, you must use a [document type](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![إضافة مرفق إلى مكون ملف/Excel](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="92f98-120">لتحديد كيفية ملء القالب المرفق عند تشغيل تنسيق ER المكون، يجب إضافة مكونات **الورقة** و **النطاق** و **الخلية** المتداخلة إلى مكون **ملف\\Excel**.</span><span class="sxs-lookup"><span data-stu-id="92f98-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="92f98-121">يجب أن يرتبط كل مكون متداخل بعنصر يسمى Excel.</span><span class="sxs-lookup"><span data-stu-id="92f98-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="92f98-122">استيراد القالب</span><span class="sxs-lookup"><span data-stu-id="92f98-122">Template import</span></span>

<span data-ttu-id="92f98-123">يمكنك تحديد **استيراد من Excel** من علامة التبويب **استيراد** من جزء الإجراءات لاستيراد قالب جديد إلى تنسيق ER فارغ.</span><span class="sxs-lookup"><span data-stu-id="92f98-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="92f98-124">في هذا المثال، سيتم إنشاء مكون **ملف\\Excel** تلقائيًا، وسيتم إرفاق القالب المستورد به.</span><span class="sxs-lookup"><span data-stu-id="92f98-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="92f98-125">سيتم أيضًا إنشاء كافة مكونات ER المطلوبة تلقائيًا، وذلك استنادًا إلى قائمة العناصر المسماة Excel التي تم اكتشافها.</span><span class="sxs-lookup"><span data-stu-id="92f98-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![تحديد استيراد من Excel](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="92f98-127">إذا كنت ترغب في إنشاء عنصر **ورقة** اختياري بتنسيق ER القابل للتحرير، قم بتعيين خيار **إنشاء عنصر تنسيق ورقة Excel** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="92f98-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="92f98-128">مكون الورقة</span><span class="sxs-lookup"><span data-stu-id="92f98-128">Sheet component</span></span>

<span data-ttu-id="92f98-129">يشير مكون **الورقة** إلى ورقة عمل من مصنف Excel المرفق الذي يجب تعبئته.</span><span class="sxs-lookup"><span data-stu-id="92f98-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="92f98-130">يتم تعريف اسم ورقه العمل في قالب Excel في خاصية **الورقة** لهذا المكون.</span><span class="sxs-lookup"><span data-stu-id="92f98-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="92f98-131">هذا المكون اختياري لمصنفات Excel التي تحتوي على ورقة عمل واحدة.</span><span class="sxs-lookup"><span data-stu-id="92f98-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="92f98-132">من علامة التبويب **التعيين** بمصمم تشغيل التقارير الإلكترونية، يمكنك تكوين خاصية **ممكّن** لمكون **الورقة** لتحديد ما إذا كان يجب وضع المكون في مستند تم إنشاؤه أم لا:</span><span class="sxs-lookup"><span data-stu-id="92f98-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="92f98-133">إذا تم تكوين تعبير لخاصية **ممكّن** لإرجاع القيمة **صحيح** في وقت التشغيل، أو إذا لم يتم تكوين أي تعبير على الإطلاق، سيتم وضع ورقه العمل المناسبة في المستند الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="92f98-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="92f98-134">إذا تم تكوين تعبير لخاصية **ممكّن** لإرجاع القيمة **خطأ** في وقت التشغيل، لن يحتوي المستند الذي تم إنشاؤه على أي ورقة عمل.</span><span class="sxs-lookup"><span data-stu-id="92f98-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![مثال لمكون الورقة](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="92f98-136">مكون النطاق</span><span class="sxs-lookup"><span data-stu-id="92f98-136">Range component</span></span>

<span data-ttu-id="92f98-137">يشير مكون **النطاق** إلى نطاق Excel الذي يجب أن يتم التحكم فيه بواسطة مكون ER هذا.</span><span class="sxs-lookup"><span data-stu-id="92f98-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="92f98-138">يتم تعريف اسم النطاق في خاصية **نطاق Excel** لهذا المكون.</span><span class="sxs-lookup"><span data-stu-id="92f98-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="92f98-139">تحدد خاصية **اتجاه النسخ المتماثل** ما إذا كان سيتم تكرار النطاق في المستند المنشأ أم لا:</span><span class="sxs-lookup"><span data-stu-id="92f98-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="92f98-140">إذا تم تعيين خاصية **اتجاه النسخ المتماثل** إلى **عدم النسخ المتماثل**، لن يتكرر نطاق Excel المناسب في المستند الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="92f98-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="92f98-141">إذا تم تعيين خاصية **اتجاه النسخ المتماثل** إلى **رأسي**، فسيتم يتكرر نطاق Excel المناسب في المستند الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="92f98-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="92f98-142">يتم وضع كل نطاق منسوخ نسخًا متماثلاً أسفل النطاق الأصلي في قالب Excel.</span><span class="sxs-lookup"><span data-stu-id="92f98-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="92f98-143">يتم تحديد عدد التكرارات حسب عدد السجلات في مصدر بيانات من نوع **قائمة السجلات** المرتبط بمكون ER هذا.</span><span class="sxs-lookup"><span data-stu-id="92f98-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="92f98-144">إذا تم تعيين خاصية **اتجاه النسخ المتماثل** إلى **أفقي**، فسيتم يتكرر نطاق Excel المناسب في المستند الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="92f98-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="92f98-145">يتم وضع كل نطاق منسوخ نسخًا متماثلاً على يمين النطاق الأصلي في قالب Excel.</span><span class="sxs-lookup"><span data-stu-id="92f98-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="92f98-146">يتم تحديد عدد التكرارات حسب عدد السجلات في مصدر بيانات من نوع **قائمة السجلات** المرتبط بمكون ER هذا.</span><span class="sxs-lookup"><span data-stu-id="92f98-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="92f98-147">لمعرفة المزيد عن النسخ المتماثل الأفقي، اتبع الخطوات الموجودة في [استخدام نطاقات قابلة للتوسيع أفقيًا لإضافة أعمدة في تقارير Excel ديناميكيًا](tasks/er-horizontal-1.md).</span><span class="sxs-lookup"><span data-stu-id="92f98-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="92f98-148">يمكن أن يكون لمكون **النطاق** مكونات ER أخرى يتم استخدامها لإدخال القيم في النطاقات المناسبة المسماة Excel.</span><span class="sxs-lookup"><span data-stu-id="92f98-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="92f98-149">في حالة استخدام أي مكون من المجموعة **النصية** لإدخال القيم، يتم إدخال القيمة في نطاق Excel كقيمة نصية.</span><span class="sxs-lookup"><span data-stu-id="92f98-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="92f98-150">استخدم هذا النمط لتنسيق القيم التي تم إدخالها استنادا إلى الإعدادات المحلية التي تم تحديدها في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="92f98-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="92f98-151">إذا تم استخدام مكون **الخلية** الخاص بمجموعة **Excel** لإدخال القيم، يتم إدخال القيمة في نطاق Excel كقيمة لنوع البيانات الذي تم تحديد بواسطة ربط مكون **الخلية** هذا (على سبيل المثال، **سلسة** أو **حقيقي** أو **عدد صحيح**).</span><span class="sxs-lookup"><span data-stu-id="92f98-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="92f98-152">استخدم هذا النمط لتمكين تطبيق Excel من تنسيق القيم المدخلة استنادا إلى الإعدادات المحلية للكمبيوتر المحلي الذي يقوم بفتح المستند الصادر.</span><span class="sxs-lookup"><span data-stu-id="92f98-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="92f98-153">من علامة التبويب **التعيين** بمصمم تشغيل التقارير الإلكترونية، يمكنك تكوين خاصية **ممكّن** لمكون **النطاق** لتحديد ما إذا كان يجب وضع المكون في مستند تم إنشاؤه أم لا:</span><span class="sxs-lookup"><span data-stu-id="92f98-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="92f98-154">إذا تم تكوين تعبير لخاصية **ممكّن** لإرجاع القيمة **صحيح** في وقت التشغيل، أو إذا لم يتم تكوين أي تعبير على الإطلاق، سيتم ملء النطاق المناسب في المستند الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="92f98-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="92f98-155">إذا تم تكوين تعبير لخاصية **ممكّن** لإرجاع القيمة **خطأ** في وقت التشغيل، وإذا كان هذا النطاق لا يمثل الصفوف أو الأعمدة بأكملها، لن يتم ملء النطاق المناسب في المستند الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="92f98-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="92f98-156">إذا تم تكوين تعبير لخاصية **ممكّن** لإرجاع القيمة **خطأ** في وقت التشغيل، وكان هذا النطاق يمثل الصفوف أو الأعمدة بأكملها، فسوف يحتوي المستند الذي تم إنشاؤه على تكل الصفوف والأعمدة كصفوف وأعمدة مخفية.</span><span class="sxs-lookup"><span data-stu-id="92f98-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="92f98-157">مكون الخلية</span><span class="sxs-lookup"><span data-stu-id="92f98-157">Cell component</span></span>

<span data-ttu-id="92f98-158">يتم استخدام مكون **الخلية** لملء الخلايا والأشكال والصور المسماة Excel.</span><span class="sxs-lookup"><span data-stu-id="92f98-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="92f98-159">للإشارة إلى كائن باسم Excel والذي يجب تعبئته بواسطة مكون ER **الخلية**، يجب تحديد اسم ذلك الكائن في خاصية **نطاق Excel** لمكون **الخلية**.</span><span class="sxs-lookup"><span data-stu-id="92f98-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="92f98-160">من علامة التبويب **التعيين** بمصمم تشغيل التقارير الإلكترونية، يمكنك تكوين خاصية **ممكّن** لمكون **الخلية** لتحديد ما إذا كان يجب ملء الكائن في مستند تم إنشاؤه أم لا:</span><span class="sxs-lookup"><span data-stu-id="92f98-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="92f98-161">إذا تم تكوين تعبير لخاصية **ممكّن** لإرجاع القيمة **صحيح** في وقت التشغيل، أو إذا لم يتم تكوين أي تعبير على الإطلاق، سيتم ملء الكائن المناسب في المستند الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="92f98-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="92f98-162">يحدد ربط مكون **الخلية** هذا قيمة يتم وضعها في الكائن المناسب.</span><span class="sxs-lookup"><span data-stu-id="92f98-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="92f98-163">إذا تم تكوين تعبير لخاصية **ممكّن** لإرجاع القيمة **خطأ** في وقت التشغيل، فلن يتم ملء الكائن المناسب في المستند الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="92f98-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="92f98-164">عند تكوين المكون **خلية** لإدخال قيمة في خلية، فمن الممكن ربطه بمصدر بيانات يرجع قيمة نوع بيانات أساسي (على سبيل المثال، **سلسلة** أو **حقيقي** أو **عدد صحيح**).</span><span class="sxs-lookup"><span data-stu-id="92f98-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="92f98-165">في هذه الحالة، يتم إدخال القيمة في الخلية كقيمة من نفس نوع البيانات.</span><span class="sxs-lookup"><span data-stu-id="92f98-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="92f98-166">عند تكوين المكون **خلية** لإدخال قيمة في شكل Excel، فمن الممكن ربطه بمصدر بيانات يرجع قيمة نوع بيانات أساسي (على سبيل المثال، **سلسلة** أو **حقيقي** أو **عدد صحيح**).</span><span class="sxs-lookup"><span data-stu-id="92f98-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="92f98-167">في هذه الحالة، يتم إدخال القيمة في شكل Excel كنص لهذا الشكل.</span><span class="sxs-lookup"><span data-stu-id="92f98-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="92f98-168">بالنسبة لقيم أنواع البيانات التي ليست **سلسلة**، يتم إجراء التحويل إلى نص تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="92f98-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="92f98-169">يمكنك تكوين المكون **خلية** لتعبئة الشكل فقط في الحالات التي تكون فيها خاصية نص الشكل مدعومة.</span><span class="sxs-lookup"><span data-stu-id="92f98-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="92f98-170">عند تكوين المكون **خلية** لإدخال قيمة في صورة Excel، فمن الممكن ربطه بمصدر بيانات يرجع قيمة نوع بيانات **حاوية** والذي يمثل الصورة بتنسيق ثنائي.</span><span class="sxs-lookup"><span data-stu-id="92f98-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="92f98-171">في هذه الحالة، يتم إدخال القيمة في صورة Excel كصورة.</span><span class="sxs-lookup"><span data-stu-id="92f98-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="92f98-172">يتم اعتبار كل صورة وشكل خاص بـ Excel مرتبطًا من الزاوية العلوية اليسرى له في خلية أو نطاق Excel معين.</span><span class="sxs-lookup"><span data-stu-id="92f98-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="92f98-173">إذا أردت إجراء نسخ متماثل لصورة أو شكل خاص بـ Excel، فيجب عليك تكوين الخلية أو النطاق الذي يتم ربطه بالخلية أو النطاق المنسوخ.</span><span class="sxs-lookup"><span data-stu-id="92f98-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="92f98-174">لمعرفة المزيد حول كيفية تضمين الصور والأشكال، راجع [تضمين الصور والأشكال في المستندات التي تنشئها باستخدام ER](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="92f98-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="92f98-175">مكون فاصل الصفحات</span><span class="sxs-lookup"><span data-stu-id="92f98-175">Page break component</span></span>

<span data-ttu-id="92f98-176">يجبر مكون **PageBreak** Excel على بدء صفحة جديدة.</span><span class="sxs-lookup"><span data-stu-id="92f98-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="92f98-177">لا يكون هذا المكون مطلوبًا عندما تريد استخدام ترحيل الصفحات الافتراضي في Excel، ولكن يجب عليك استخدامه عندما تريد أن يتبع Excel تنسيق ER لهيكلة الترحيل.</span><span class="sxs-lookup"><span data-stu-id="92f98-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="footer-component"></a><span data-ttu-id="92f98-178">مكون التذييل</span><span class="sxs-lookup"><span data-stu-id="92f98-178">Footer component</span></span>

<span data-ttu-id="92f98-179">يُستخدم مكون  **التذييل** لملء التذييلات في أسفل ورقة عمل تم إنشاؤها في مصنف Excel.</span><span class="sxs-lookup"><span data-stu-id="92f98-179">The **Footer** component is used to fill in footers at the bottom of a generated worksheet in an Excel workbook.</span></span>

> [!NOTE]
> <span data-ttu-id="92f98-180">يمكنك إضافة هذا المكون لكل مكون **ورقة عمل** لتحديد تذييلات مختلفة لأوراق العمل المختلفة في مصنف Excel الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="92f98-180">You can add this component for every **Sheet** component to specify different footers for different worksheets in a generated Excel workbook.</span></span>

<span data-ttu-id="92f98-181">عند تكوين مكون **تذييل** فردي، يمكنك استخدام خاصية **مظهر الرأس/التذييل** لتحديد الصفحات التي يتم استخدام المكون لها.</span><span class="sxs-lookup"><span data-stu-id="92f98-181">When you configure an individual **Footer** component, you can use the **Header/footer appearance** property to specify the pages that the component is used for.</span></span> <span data-ttu-id="92f98-182">تتوفر القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="92f98-182">The following values are available:</span></span>

- <span data-ttu-id="92f98-183">**أي** - تشغيل مكون **التذييل** الذي تم تكوينه لأي صفحة من ورقة عمل Excel الأصلية.</span><span class="sxs-lookup"><span data-stu-id="92f98-183">**Any** – Run the configured **Footer** component for any page of the parent Excel worksheet.</span></span>
- <span data-ttu-id="92f98-184">**الأولى** - تشغيل مكون **التذييل** الذي تم تكوينه للصفحة الأولى فقط من ورقة عمل Excel الأصلية.</span><span class="sxs-lookup"><span data-stu-id="92f98-184">**First** – Run the configured **Footer** component for only the first page of the parent Excel worksheet.</span></span>
- <span data-ttu-id="92f98-185">**زوجي** - تشغيل مكون **التذييل** الذي تم تكوينه للصفحات الزوجية فقط من ورقة عمل Excel الأصلية.</span><span class="sxs-lookup"><span data-stu-id="92f98-185">**Even** – Run the configured **Footer** component for only the even pages of the parent Excel worksheet.</span></span>
- <span data-ttu-id="92f98-186">**زوجي** فردي - تشغيل مكون **التذييل** الذي تم تكوينه للصفحات الفردية فقط من ورقة عمل Excel الأصلية.</span><span class="sxs-lookup"><span data-stu-id="92f98-186">**Odd** – Run the configured **Footer** component for only the odd pages of the parent Excel worksheet.</span></span>

<span data-ttu-id="92f98-187">مع مكون **ورقة عمل** فردية، يمكنك إضافة عدة مكونات **تذييل**، ولكل واحد قيمة مختلفة لخاصية **مظهر الرأس/التذييل**.</span><span class="sxs-lookup"><span data-stu-id="92f98-187">For a single **Sheet** component, you can add several **Footer** components, each of which has a different value for the **Header/footer appearance** property.</span></span> <span data-ttu-id="92f98-188">بهذه الطريقة، يمكنك إنشاء تذييلات مختلفة لأنواع مختلفة من الصفحات في ورقة عمل Excel.</span><span class="sxs-lookup"><span data-stu-id="92f98-188">In this way, you can generate different footers for different type of pages in an Excel worksheet.</span></span>

> [!NOTE]
> <span data-ttu-id="92f98-189">تأكد من أن كل مكون **تذييل** قمت بإضافته إلى مكون **ورقة** فردي يتضمن قيمة مختلفة لخاصية **مظهر الرأس/التذييل**.</span><span class="sxs-lookup"><span data-stu-id="92f98-189">Make sure that each **Footer** component that you add to a single **Sheet** component has a different value for the **Header/footer appearance** property.</span></span> <span data-ttu-id="92f98-190">خلاف ذلك، سيحدث [خطأ في التحقق من الصحة](er-components-inspections.md#i16).</span><span class="sxs-lookup"><span data-stu-id="92f98-190">Otherwise, a [validation error](er-components-inspections.md#i16) occurs.</span></span> <span data-ttu-id="92f98-191">تقوم رسالة الخطأ التي تلقيتها بإخطارك بشان عدم التوافق.</span><span class="sxs-lookup"><span data-stu-id="92f98-191">The error message that you receive notifies you about the inconsistency.</span></span>

<span data-ttu-id="92f98-192">ضمن مكون **التذييل** المضاف، أضف المكونات المتداخلة المطلوبة من **النص\\السلسلة** أو **النص\\تاريخ/وقت** أو أي نوع آخر.</span><span class="sxs-lookup"><span data-stu-id="92f98-192">Under the added **Footer** component, add the required nested components of the **Text\\String**, **Text\\DateTime**, or other type.</span></span> <span data-ttu-id="92f98-193">قم بتكوين الروابط لهذه المكونات لتحديد كيفية ملء تذييل صفحتك.</span><span class="sxs-lookup"><span data-stu-id="92f98-193">Configure the bindings for those components to specify how your page footer is filled in.</span></span>

<span data-ttu-id="92f98-194">يمكنك أيضا استخدام [أكواد التنسيق](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) لتنسيق محتوي التذييل الذي تم إنشاؤه بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="92f98-194">You can also use special [formatting codes](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) to correctly format the content of a generated footer.</span></span> <span data-ttu-id="92f98-195">لمعرفة كيفية استخدام هذا النهج، اتبع الخطوات الموضحة في [المثال 1](#example-1)، لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="92f98-195">To learn how to use this approach, follow the steps in [Example 1](#example-1), later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="92f98-196">عند تكوين تنسيقات ER، تأكد من مراعاة [حد Excel](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) والحد الأقصى لعدد الأحرف الخاصة برأس أو تذييل الصفحة الفردية.</span><span class="sxs-lookup"><span data-stu-id="92f98-196">When you configure ER formats, be sure to consider the Excel [limit](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) and the maximum number of characters for a single header or footer.</span></span>

## <a name="header-component"></a><span data-ttu-id="92f98-197">مكون الرأس</span><span class="sxs-lookup"><span data-stu-id="92f98-197">Header component</span></span>

<span data-ttu-id="92f98-198">يُستخدم مكون  **الرأس** لملء الرؤوس في أعلى ورقة عمل تم إنشاؤها في مصنف Excel.</span><span class="sxs-lookup"><span data-stu-id="92f98-198">The **Header** component is used to fill in headers at the top of a generated worksheet in an Excel workbook.</span></span> <span data-ttu-id="92f98-199">ويُستخدم مثل مكون **التذييل**.</span><span class="sxs-lookup"><span data-stu-id="92f98-199">It's used like the **Footer** component.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="92f98-200">تحرير تنسيق ER المضاف</span><span class="sxs-lookup"><span data-stu-id="92f98-200">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="92f98-201">تحديث قالب</span><span class="sxs-lookup"><span data-stu-id="92f98-201">Update a template</span></span>

<span data-ttu-id="92f98-202">يمكنك تحديد **تحديث من Excel** من علامة التبويب **استيراد** من جزء الإجراءات لاستيراد قالب محدث إلى تنسيق ER قابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="92f98-202">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="92f98-203">أثناء هذه العملية، يتم استبدال قالب لمكون **ملف\\Excel** المحدد بقالب جديد.</span><span class="sxs-lookup"><span data-stu-id="92f98-203">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="92f98-204">ستتم مزامنة محتوي تنسيق ER القابل للتحرير مع محتوي قالب ER الذي تم تحديثه.</span><span class="sxs-lookup"><span data-stu-id="92f98-204">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="92f98-205">سيتم إنشاء مكون جديد لتنسيق ER تلقائيًا لكل اسم Excel إذا لم يتم العثور على مكون تنسيق ER في التنسيق القابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="92f98-205">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="92f98-206">سيتم حذف كل مكون من مكونات تنسيق ER من تنسيق ER القابل للتحرير إذا لم يتم العثور على اسم Excel المناسب له.</span><span class="sxs-lookup"><span data-stu-id="92f98-206">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="92f98-207">قم بتعيين خيار **إنشاء عنصر تنسيق ورقة Excel** إلى **نعم** إذا كنت ترغب في إنشاء عنصر **ورقة** بتنسيق ER القابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="92f98-207">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="92f98-208">إذا كان تنسيق ER القابل للتحرير مدرج في الأصل في عناصر **الورقة**، فنحن نوصي بتعيين خيار **إنشاء عنصر تنسيق ورقة Excel** إلى **نعم** عند استيراد قالب محدث.</span><span class="sxs-lookup"><span data-stu-id="92f98-208">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="92f98-209">خلاف ذلك، سيتم إنشاء كافة العناصر المتداخلة لعنصر **الورقة** الأصلي من البداية.</span><span class="sxs-lookup"><span data-stu-id="92f98-209">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="92f98-210">بالتالي، سيتم فقدان كافة ارتباطات عناصر التنسيق المعاد إنشائها في تنسيق ER المحدث.</span><span class="sxs-lookup"><span data-stu-id="92f98-210">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![خيار إنشاء عنصر بتنسيق ورقة Excel في مربع الحوار تحديث من Excel](./media/er-excel-format-update-template.png)

<span data-ttu-id="92f98-212">لمعرفة المزيد حول هذه الميزة، اتبع الخطوات الموجودة في [تعديل تنسيقات التقارير الإلكترونية عن طريق إعادة تطبيق قوالب Excel](modify-electronic-reporting-format-reapply-excel-template.md).</span><span class="sxs-lookup"><span data-stu-id="92f98-212">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="92f98-213">التحقق من صحة تنسيق ER</span><span class="sxs-lookup"><span data-stu-id="92f98-213">Validate an ER format</span></span>

<span data-ttu-id="92f98-214">عند التحقق من صحة تنسيق ER الذي يمكن تحريره، يتم التحقق من التناسق للتأكد من وجود اسم Excel في قالب Excel المستخدم حاليًا.</span><span class="sxs-lookup"><span data-stu-id="92f98-214">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="92f98-215">سيتم إعلامك بوجود أي حالات عدم تناسق.</span><span class="sxs-lookup"><span data-stu-id="92f98-215">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="92f98-216">بالنسبة لبعض حالات عدم التناسق، يتم تقديم خيار لإصلاح المشكلات تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="92f98-216">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![رسالة خطأ التحقق من الصحة](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a><span data-ttu-id="92f98-218">التحكم في حساب معادلات Excel</span><span class="sxs-lookup"><span data-stu-id="92f98-218">Control the calculation of Excel formulas</span></span>

<span data-ttu-id="92f98-219">عند إنشاء مستند خارجي في تنسيق مصنف Microsoft Excel، قد تحتوي بعض الخلايا الخاصة بهذا المستند على معادلات Excel.</span><span class="sxs-lookup"><span data-stu-id="92f98-219">When an outbound document in a Microsoft Excel workbook format is generated, some cells of this document might contain Excel formulas.</span></span> <span data-ttu-id="92f98-220">عندما يتم تمكين ميزة **تمكين استخدام لمكتبة EPPlus في إطار عمل التقارير الإلكترونية**، يمكنك التحكم في الوقت الذي يتم فيه حساب المعادلات بتغيير قيمة **معلمة** [خيارات الحساب](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) في قالب Excel الذي يتم استخدامه:</span><span class="sxs-lookup"><span data-stu-id="92f98-220">When the **Enable usage of EPPlus library in Electronic reporting framework** feature is enabled, you can control when the formulas are calculated by changing the value of the **Calculation Options** [parameter](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) in the Excel template that is being used:</span></span>

- <span data-ttu-id="92f98-221">حدد **تلقائي** لإعادة حساب كافة المعادلات التابعة في كل مره يتم فيها إلحاق مستند تم إنشاؤه بنطاقات وخلايا جديدة وغيرها.</span><span class="sxs-lookup"><span data-stu-id="92f98-221">Select **Automatic** to recalculate all dependent formulas every time a generated document is appended by new ranges, cells, etc.</span></span>
    >[!NOTE]
    > <span data-ttu-id="92f98-222">قد يتسبب هذا في حدوث مشكلة في الأداء لقوالب Excel التي تحتوي على عدة صيغ ذات صلة.</span><span class="sxs-lookup"><span data-stu-id="92f98-222">This might cause a performance issue for Excel templates that contain multiple related formulas.</span></span>
- <span data-ttu-id="92f98-223">حدد **يدوي** لتجنب إعادة حساب المعادلة عند إنشاء مستند.</span><span class="sxs-lookup"><span data-stu-id="92f98-223">Select **Manual** to avoid formula recalculation when a document is generated.</span></span>
    >[!NOTE]
    > <span data-ttu-id="92f98-224">يتم فرض إعادة حساب المعادلة يدويًا عند فتح مستند تم إنشاؤه للمعاينة باستخدام Excel.</span><span class="sxs-lookup"><span data-stu-id="92f98-224">Formula recalculation is manually forced when a generated document is opened for preview using Excel.</span></span>
    > <span data-ttu-id="92f98-225">لا تستخدم هذا الخيار إذا قمت بتكوين وجهة إعداد التقارير الإلكترونية التي تفترض استخدام مستند تم إنشاؤه بدون معاينته في Excel (تحويل PDF، وإرسال بريد إلكتروني، وما إلى ذلك) لأن المستند الذي تم إنشاؤه قد لا يحتوي على قيم في الخلايا التي تحتوي على معادلات.</span><span class="sxs-lookup"><span data-stu-id="92f98-225">Don't use this option if you configure an ER destination that assumes the usage of a generated document without its preview in Excel (PDF conversion, emailing, etc.) because the generated document might not contain values in cells that contain formulas.</span></span>

## <a name="example-1-format-footer-content"></a><a name="example-1"></a><span data-ttu-id="92f98-226">مثال رقم 1: تنسيق محتوى التذييل </span><span class="sxs-lookup"><span data-stu-id="92f98-226">Example 1: Format footer content</span></span>

1. <span data-ttu-id="92f98-227">استخدم تكوينات ER المتوفرة [لإنشاء](er-generate-printable-fti-forms.md) مستند فاتورة ذات نص حر قابل للطباعة (FTI).</span><span class="sxs-lookup"><span data-stu-id="92f98-227">Use the provided ER configurations to [generate](er-generate-printable-fti-forms.md) a printable free text invoice (FTI) document.</span></span>
2. <span data-ttu-id="92f98-228">قم بمراجعة تذييل المستند الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="92f98-228">Review the footer of the generated document.</span></span> <span data-ttu-id="92f98-229">لاحظ أنه يحتوي على معلومات حول رقم الصفحة الحالية والعدد الإجمالي للصفحات في المستند.</span><span class="sxs-lookup"><span data-stu-id="92f98-229">Notice that it contains information about the current page number and the total number of pages in the document.</span></span>

    ![مراجعة تذييل المستند الذي تم إنشاؤه بتنسيق Excel](./media/er-fillable-excel-footer-1.gif)

3. <span data-ttu-id="92f98-231">في مصمم تنسيق ER، [افتح](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) نموذج تنسيق ER للمراجعة.</span><span class="sxs-lookup"><span data-stu-id="92f98-231">In the ER format designer, [open](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) the sample ER format for review.</span></span>

    <span data-ttu-id="92f98-232">يتم إنشاء تذييل ورقة عمل **الفاتورة** استنادا إلى إعدادات مكونين من مكونات **السلسلة** الموجودة ضمن مكون **التذييل**:</span><span class="sxs-lookup"><span data-stu-id="92f98-232">The footer of the **Invoice** worksheet is generated based on the settings of two **String** components that reside under the **Footer** component:</span></span>

    - <span data-ttu-id="92f98-233">يقوم مكون **السلسلة** الأول بتعبئة أكواد التنسيق الخاصة التالية لإجبار Excel على تطبيق تنسيق محدد:</span><span class="sxs-lookup"><span data-stu-id="92f98-233">The first **String** component fills in the following special formatting codes to force Excel to apply specific formatting:</span></span>

        - <span data-ttu-id="92f98-234">**&C** - محاذاة نص التذييل إلى الوسط.</span><span class="sxs-lookup"><span data-stu-id="92f98-234">**&C** – Align the footer text in the center.</span></span>
        - <span data-ttu-id="92f98-235">**&"Segoe UI,Regular"&8** – إظهار نص التنسيق بخط "Segoe UI Regular" بحجم 8 نقاط.</span><span class="sxs-lookup"><span data-stu-id="92f98-235">**&"Segoe UI,Regular"&8** – Present the footer text in the "Segoe UI Regular" font at a size of 8 points.</span></span>

    - <span data-ttu-id="92f98-236">يملأ مكون **السلسلة** الثاني النص الذي يحتوي على رقم الصفحة الحالية والعدد الإجمالي للصفحات في المستند الحالي.</span><span class="sxs-lookup"><span data-stu-id="92f98-236">The second **String** component fills in the text that contains the current page number and the total number of pages in the current document.</span></span>

    ![مراجعة مكون تنسيق التقارير الإلكترونية (ER) في صفحة مصمم التنسيق](./media/er-fillable-excel-footer-2.png)

4. <span data-ttu-id="92f98-238">تخصيص تنسيق نموذج ER لتعديل تذييل الصفحة الحالية:</span><span class="sxs-lookup"><span data-stu-id="92f98-238">Customize the sample ER format to modify the current page footer:</span></span>

    1. <span data-ttu-id="92f98-239">قم [بإنشاء](er-quick-start2-customize-report.md#DeriveProvidedFormat) تنسيق **مخصص لفاتورة نص حر (Excel)** مشتق يستند إلى نموذج تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="92f98-239">[Create](er-quick-start2-customize-report.md#DeriveProvidedFormat) a derived **Free text invoice (Excel) custom** ER format that is based on the sample ER format.</span></span>
    2. <span data-ttu-id="92f98-240">أضف الزوج الجديد الأول من مكونات **السلسلة** لمكون **التذييل** لورقة عمل **الفاتورة**:</span><span class="sxs-lookup"><span data-stu-id="92f98-240">Add the first new pair of **String** components for the **Footer** component of the **Invoice** worksheet:</span></span>

        1. <span data-ttu-id="92f98-241">أضف مكون **سلسلة** لمحاذاة اسم الشركة على اليسار وعرضه بخط 8 نقاط من "Segoe UI Regular" (**"&L&"Segoe UI,Regular"&8"**).</span><span class="sxs-lookup"><span data-stu-id="92f98-241">Add a **String** component that aligns the company name on the left and presents it in 8-point "Segoe UI Regular" font (**"&L&"Segoe UI,Regular"&8"**).</span></span>
        2. <span data-ttu-id="92f98-242">إضافة مكون **سلسله** يقوم بتعبئة اسم الشركة (**model.InvoiceBase.CompanyInfo.Name**).</span><span class="sxs-lookup"><span data-stu-id="92f98-242">Add a **String** component that fills in the company name (**model.InvoiceBase.CompanyInfo.Name**).</span></span>

    3. <span data-ttu-id="92f98-243">أضف الزوج الجديد الثاني من مكونات **السلسلة** لمكون **التذييل** لورقة عمل **الفاتورة**:</span><span class="sxs-lookup"><span data-stu-id="92f98-243">Add the second new pair of **String** components for the **Footer** component of the **Invoice** worksheet:</span></span>

        1. <span data-ttu-id="92f98-244">أضف مكون **سلسلة** لمحاذاة تاريخ المعالجة على اليمين وعرضه بخط 8 نقاط من "Segoe UI Regular" (**"&L&"Segoe UI,Regular"&8"**).</span><span class="sxs-lookup"><span data-stu-id="92f98-244">Add a **String** component that aligns the processing date on the right and presents it in 8-point "Segoe UI Regular" font (**"&R&"Segoe UI,Regular"&8"**).</span></span>
        2. <span data-ttu-id="92f98-245">أضف مكون **سلسلة** يقوم بتعبئة تاريخ المعالجة بتنسيق مخصص (**"&nbsp;"&DATEFORMAT(SESSIONTODAY(), "yyyy-MM-dd")**).</span><span class="sxs-lookup"><span data-stu-id="92f98-245">Add a **String** component that fills in the processing date in a custom format (**"&nbsp;"&DATEFORMAT(SESSIONTODAY(), "yyyy-MM-dd")**).</span></span>

        ![مراجعة مكون تنسيق التقارير الإلكترونية (ER) في صفحة مصمم التنسيق](./media/er-fillable-excel-footer-3.png)

    4. <span data-ttu-id="92f98-247">[أكمل](er-quick-start2-customize-report.md#CompleteDerivedFormat) إصدار المسودة من تنسيق ER لـ **فاتورة نص حرة (Excel) مخصصة** مشتقة.</span><span class="sxs-lookup"><span data-stu-id="92f98-247">[Complete](er-quick-start2-customize-report.md#CompleteDerivedFormat) the draft version of the derived **Free text invoice (Excel) custom** ER format.</span></span>

5. <span data-ttu-id="92f98-248">[قم بتكوين](er-generate-printable-fti-forms.md#configure-print-management) إدارة الطباعة لاستخدام تنسيق ER لـ **فاتورة نص حر (Excel) مخصص** المشتقة بدلا من نموذج تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="92f98-248">[Configure](er-generate-printable-fti-forms.md#configure-print-management) Print management to use the derived **Free text invoice (Excel) custom** ER format instead of the sample ER format.</span></span>
6. <span data-ttu-id="92f98-249">قم بإنشاء وثيقة FTI قابلة للطباعة، وقم بمراجعه تذييل الوثيقة التي تم إنشائها.</span><span class="sxs-lookup"><span data-stu-id="92f98-249">Generate a printable FTI document, and review the footer of the generated document.</span></span>

    ![مراجعة تذييل المستند الذي تم إنشاؤه بتنسيق Excel](./media/er-fillable-excel-footer-4.gif)

## <a name="additional-resources"></a><span data-ttu-id="92f98-251">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="92f98-251">Additional resources</span></span>

[<span data-ttu-id="92f98-252">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="92f98-252">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="92f98-253">تصميم تكوين لإنشاء التقارير بتنسيق OPENXML</span><span class="sxs-lookup"><span data-stu-id="92f98-253">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="92f98-254">تعديل تنسيقات التقارير الإلكترونية من خلال إعادة تطبيق قوالب Excel</span><span class="sxs-lookup"><span data-stu-id="92f98-254">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="92f98-255">استخدام النطاقات القابلة للتوسيع أفقيًا لإضافة الأعمدة بشكل حيوي في تقارير Excel</span><span class="sxs-lookup"><span data-stu-id="92f98-255">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="92f98-256">تضمين الصور والأشكال في المستندات التي تقوم بإنشائها باستخدام التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="92f98-256">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="92f98-257">تكوين التقارير الإلكترونية (ER) لسحب البيانات إلى Power BI</span><span class="sxs-lookup"><span data-stu-id="92f98-257">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]