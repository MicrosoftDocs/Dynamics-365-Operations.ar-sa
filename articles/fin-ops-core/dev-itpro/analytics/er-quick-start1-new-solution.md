---
title: تصميم حل جديد لإعداد التقارير الإلكترونية لطباعة تقرير مخصص
description: يشرح هذا الموضوع كيفية تصميم حل لإعداد التقارير الإلكترونية لطباعة تقرير مخصص.
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90e5381c2d30753e3ad82a38d7361b411f1d7a87
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304383"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a><span data-ttu-id="f80a9-103">تصميم حل جديد لإعداد التقارير الإلكترونية لطباعة تقرير مخصص</span><span class="sxs-lookup"><span data-stu-id="f80a9-103">Design a new ER solution to print a custom report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f80a9-104">توضح الخطوات التالية كيف يمكن لمستخدم يؤدي دور مسؤول النظام أو مطور إعداد التقارير الإلكترونية أو مستشار وظيفي لإعداد التقارير الإلكترونية تكوين معلمات لاطار عمل إعداد التقارير الإلكترونية وتصميم تكوينات التقارير الإلكترونية المطلوبة الخاصة بحل جديد لإعداد التقارير الإلكترونية للوصول إلى بيانات مجال عمل معين وإنشاء تقرير مخصص بتنسيق Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="f80a9-104">The following steps explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can configure parameters of the ER framework, design the required ER configurations of a new ER solution to access the data of a particular business domain, and generate a custom report in Microsoft Office format.</span></span> <span data-ttu-id="f80a9-105">يمكن تنفيذ هذه الخطوات في شركة **USMF**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-105">These steps can be completed in the **USMF** company.</span></span>

- [<span data-ttu-id="f80a9-106">تكوين إطار عمل ER</span><span class="sxs-lookup"><span data-stu-id="f80a9-106">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="f80a9-107">تكوين معلمات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f80a9-107">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="f80a9-108">تنشيط موفر تكوين ER</span><span class="sxs-lookup"><span data-stu-id="f80a9-108">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="f80a9-109">مراجعة قائمة موفري تكوين ER</span><span class="sxs-lookup"><span data-stu-id="f80a9-109">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="f80a9-110">إضافة موفر تكوين ER جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-110">Add a new ER configuration provider</span></span>](#AddProvider)
        - [<span data-ttu-id="f80a9-111">تنشيط موفر تكوين ER</span><span class="sxs-lookup"><span data-stu-id="f80a9-111">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="f80a9-112">تصميم نموذج بيانات خاص بالمجال</span><span class="sxs-lookup"><span data-stu-id="f80a9-112">Design a domain-specific data model</span></span>](#DesignModel)

    - [<span data-ttu-id="f80a9-113">استيراد تكوين نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-113">Import a new data model configuration</span></span>](#ImportDataModel)
    - [<span data-ttu-id="f80a9-114">إنشاء تكوين نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-114">Create a new data model configuration</span></span>](#DesignDataModel)

        - [<span data-ttu-id="f80a9-115">تسمية نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-115">Name the data model</span></span>](#NameDataModel)
        - [<span data-ttu-id="f80a9-116">إضافة حقول نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-116">Add data model fields</span></span>](#FieldsEntry)
        - [<span data-ttu-id="f80a9-117">إكمال تصميم نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-117">Complete the design of the data model</span></span>](#CompleteDataModel)

- [<span data-ttu-id="f80a9-118">تصميم تعيين نموذج لنموذج البيانات المكوّن</span><span class="sxs-lookup"><span data-stu-id="f80a9-118">Design a model mapping for the configured data model</span></span>](#DesignMapping)

    - [<span data-ttu-id="f80a9-119">استيراد تكوين تعيين نموذج جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-119">Import a new model mapping configuration</span></span>](#ImportModelMapping)
    - [<span data-ttu-id="f80a9-120">إنشاء تكوين تعيين نموذج جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-120">Create a new model mapping configuration</span></span>](#CreateModelMapping)

        - [<span data-ttu-id="f80a9-121">تصميم مكون تعيين نموذج جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-121">Design a new model mapping component</span></span>](#DesignMappingComponent)
        - [<span data-ttu-id="f80a9-122">إضافة مصادر بيانات للوصول إلى جداول التطبيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-122">Add data sources to access application tables</span></span>](#AddMmDataSource1)
        - [<span data-ttu-id="f80a9-123">إضافة مصادر بيانات للوصول إلى عمليات تعداد التطبيقات</span><span class="sxs-lookup"><span data-stu-id="f80a9-123">Add data sources to access application enumerations</span></span>](#AddMmDataSource2)
        - [<span data-ttu-id="f80a9-124">إضافة تسميات التقارير الإلكترونية لإنشاء تقرير بلغة محددة</span><span class="sxs-lookup"><span data-stu-id="f80a9-124">Add ER labels to generate a report in a specified language</span></span>](#AddMmLabels)
        - [<span data-ttu-id="f80a9-125">إضافة مصدر بيانات لتحويل نتائج مقارنة قيم التعداد بقيمة نصية</span><span class="sxs-lookup"><span data-stu-id="f80a9-125">Add a data source to transform the results of comparing enumeration values to a text value</span></span>](#AddMmDataSource3)
        - [<span data-ttu-id="f80a9-126">ربط مصادر البيانات بحقول نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-126">Bind data sources to data model fields</span></span>](#AddMmBindings1)
        - [<span data-ttu-id="f80a9-127">إكمال تصميم تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="f80a9-127">Complete the design of the model mapping</span></span>](#CompleteModelMapping)

- [<span data-ttu-id="f80a9-128">تصميم قالب لتقرير مخصص</span><span class="sxs-lookup"><span data-stu-id="f80a9-128">Design a template for a custom report</span></span>](#DesignReportTemplate)
- [<span data-ttu-id="f80a9-129">تصميم تنسيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-129">Design a format</span></span>](#DesignFormat)

    - [<span data-ttu-id="f80a9-130">استيراد تكوين تنسيق مصمّم</span><span class="sxs-lookup"><span data-stu-id="f80a9-130">Import a designed format configuration</span></span>](#FormatImport)
    - [<span data-ttu-id="f80a9-131">قم بإنشاء تكوين تنسيق جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-131">Create a new format configuration</span></span>](#FormatCreate)

        - [<span data-ttu-id="f80a9-132">استيراد قالب تقرير</span><span class="sxs-lookup"><span data-stu-id="f80a9-132">Import a report template</span></span>](#ImportReportTemplate)
        - [<span data-ttu-id="f80a9-133">تكوين تنسيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-133">Configure a format</span></span>](#ConfigureFormat)
        - [<span data-ttu-id="f80a9-134">تعريف ربط البيانات لعنوان التقرير</span><span class="sxs-lookup"><span data-stu-id="f80a9-134">Define the data binding for a report title</span></span>](#DefineFormatBindings)
        - [<span data-ttu-id="f80a9-135">مراجعة مصدر بيانات النموذج</span><span class="sxs-lookup"><span data-stu-id="f80a9-135">Review the model data source</span></span>](#ReviewModelDataSource)
        - [<span data-ttu-id="f80a9-136">ربط عناصر التنسيق بحقول مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-136">Bind format elements to data source fields</span></span>](#BindFormatElements)

    - [<span data-ttu-id="f80a9-137">تشغيل تنسيق مصمّم من التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f80a9-137">Run a designed format from ER</span></span>](#RunFormatFromER)

- [<span data-ttu-id="f80a9-138">ضبط تنسيق مصمّم</span><span class="sxs-lookup"><span data-stu-id="f80a9-138">Tune a designed format</span></span>](#TuneFormat)

    - [<span data-ttu-id="f80a9-139">تعديل تنسيق لتغيير اسم مستند تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="f80a9-139">Modify a format to change the name of a generated document</span></span>](#ModifyToChangeName)
    - [<span data-ttu-id="f80a9-140">تعديل تنسيق لتغيير ترتيب الأسئلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-140">Modify a format to change the order of questions</span></span>](#ModifyToOrder)
    - [<span data-ttu-id="f80a9-141">تشغيل تنسيق معدّل من التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f80a9-141">Run a modified format from ER</span></span>](#RunFormatFromER2)
    - [<span data-ttu-id="f80a9-142">إكمال تصميم التنسيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-142">Complete the format design</span></span>](#CompleteFormat)

- [<span data-ttu-id="f80a9-143">تطوير بيانات اصطناعية للتطبيق لاستدعاء التقرير المصمّم</span><span class="sxs-lookup"><span data-stu-id="f80a9-143">Develop application artefacts to call the designed report</span></span>](#DevelopCustomCode)

    - [<span data-ttu-id="f80a9-144">تعديل التعليمات البرمجية المصدر</span><span class="sxs-lookup"><span data-stu-id="f80a9-144">Modify source code</span></span>](#ModifySourceCode)

        - [<span data-ttu-id="f80a9-145">إضافة فئة عقد بيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-145">Add a data contract class</span></span>](#DataContractClass)
        - [<span data-ttu-id="f80a9-146">إضافة فئة منشئ واجهة المستخدم</span><span class="sxs-lookup"><span data-stu-id="f80a9-146">Add a UI builder class</span></span>](#UIBuilderClass)
        - [<span data-ttu-id="f80a9-147">إضافة فئة موفر بيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-147">Add a data provider class</span></span>](#DataProviderClass)
        - [<span data-ttu-id="f80a9-148">إضافة ملف تسميات</span><span class="sxs-lookup"><span data-stu-id="f80a9-148">Add a labels file</span></span>](#LabelsFile)
        - [<span data-ttu-id="f80a9-149">إضافة فئة خدمة تقرير</span><span class="sxs-lookup"><span data-stu-id="f80a9-149">Add a report service class</span></span>](#ServiceClass)
        - [<span data-ttu-id="f80a9-150">إضافة فئة مراقب التقارير</span><span class="sxs-lookup"><span data-stu-id="f80a9-150">Add a report controller class</span></span>](#ControllerClass)
        - [<span data-ttu-id="f80a9-151">إضافة عنصر قائمة</span><span class="sxs-lookup"><span data-stu-id="f80a9-151">Add a menu item</span></span>](#MenuItem)
        - [<span data-ttu-id="f80a9-152">إضافة عنصر قائمة إلى قائمة</span><span class="sxs-lookup"><span data-stu-id="f80a9-152">Add a menu item to a menu</span></span>](#Menu)
        - [<span data-ttu-id="f80a9-153">إنشاء مشروع Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f80a9-153">Build a Visual Studio project</span></span>](#BuildVSProject)

    - [<span data-ttu-id="f80a9-154">تشغيل تنسيق من التطبيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-154">Run a format from the application</span></span>](#RunFormatFromApp)

- [<span data-ttu-id="f80a9-155">ضبط حل إعداد التقارير الإلكترونية المصمّم</span><span class="sxs-lookup"><span data-stu-id="f80a9-155">Tune a designed ER solution</span></span>](#TuneSolution)

    - [<span data-ttu-id="f80a9-156">تعديل تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="f80a9-156">Modify a model mapping</span></span>](#ModifyModelMapping)

        - [<span data-ttu-id="f80a9-157">إضافة مصادر بيانات للوصول إلى كائن عقد البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-157">Add data sources to access a data contract object</span></span>](#AddDataSource1)
        - [<span data-ttu-id="f80a9-158">إضافة مصدر بيانات للوصول إلى سجلات تعيين تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f80a9-158">Add a data source to access ER format mapping records</span></span>](#AddDataSource2)
        - [<span data-ttu-id="f80a9-159">إضافة مصدر بيانات للوصول إلى سجل تعيين التنسيق لتنسيق تقارير إلكترونية قيد التشغيل</span><span class="sxs-lookup"><span data-stu-id="f80a9-159">Add a data source to access a format mapping record of a running ER format</span></span>](#AddDataSource3)
        - [<span data-ttu-id="f80a9-160">إدخال اسم تنسيق تقارير إلكترونية قيد التشغيل في نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-160">Enter the name of the running ER format in the data model</span></span>](#AddBinding)
        - [<span data-ttu-id="f80a9-161">إكمال تصميم تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="f80a9-161">Complete the design of the model mapping</span></span>](#CompleteModelMapping2)

    - [<span data-ttu-id="f80a9-162">تعديل تنسيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-162">Modify a format</span></span>](#ModifyFormat)

        - [<span data-ttu-id="f80a9-163">إضافة عنصر تنسيق جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-163">Add a new format element</span></span>](#AddFormatElement)
        - [<span data-ttu-id="f80a9-164">ربط عنصر التنسيق المضاف</span><span class="sxs-lookup"><span data-stu-id="f80a9-164">Bind the added format element</span></span>](#BindAddedFormatElement)
        - [<span data-ttu-id="f80a9-165">إكمال تصميم التنسيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-165">Complete the format design</span></span>](#CompleteFormat2)

    - [<span data-ttu-id="f80a9-166">تشغيل تنسيق من التطبيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-166">Run a format from the application</span></span>](#RunFormatFromApp2)
    - [<span data-ttu-id="f80a9-167">تشغيل تنسيق من التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f80a9-167">Run a format from ER</span></span>](#RunFormatFromER3)
    - [<span data-ttu-id="f80a9-168">تكوين وجهة التنسيق للمعاينة على الشاشة</span><span class="sxs-lookup"><span data-stu-id="f80a9-168">Configure a format destination for on-screen preview</span></span>](#ConfigureDestination)
    - [<span data-ttu-id="f80a9-169">تشغيل تنسيق من التطبيق لمعاينته كمستند PDF</span><span class="sxs-lookup"><span data-stu-id="f80a9-169">Run a format from the application to preview it as a PDF document</span></span>](#RunFormatFromApp3)

- [<span data-ttu-id="f80a9-170">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f80a9-170">Additional resources</span></span>](#References)

<span data-ttu-id="f80a9-171">في هذا المثال، ستقوم بإنشاء حل جديد لإعداد التقارير الإلكترونية للوحدة النمطية [الاستبيان](../../../human-resources/hr-learning-questionnaires.md).</span><span class="sxs-lookup"><span data-stu-id="f80a9-171">In this example, you will create a new ER solution for the [Questionnaire](../../../human-resources/hr-learning-questionnaires.md) module.</span></span> <span data-ttu-id="f80a9-172">يتيح لك هذا الحل الجديد لإعداد التقارير الإلكترونية بتصميم تقرير باستخدام ورقه عمل Microsoft Excel كقالب.</span><span class="sxs-lookup"><span data-stu-id="f80a9-172">This new ER solution lets you design a report by using a Microsoft Excel worksheet as a template.</span></span> <span data-ttu-id="f80a9-173">يمكنك بعد ذلك إنشاء تقرير **الاستبيان** بتنسيق Excel أو PDF، بالإضافة إلى إنشاء تقرير SQL Server Reporting Services (SSRS) الموجود.</span><span class="sxs-lookup"><span data-stu-id="f80a9-173">You can then generate the **Questionnaire** report in Excel or PDF format, in addition to generating the existing SQL Server Reporting Services (SSRS) report.</span></span> <span data-ttu-id="f80a9-174">يمكنك أيضًا تعديل التقرير الجديد لاحقًا، عند الطلب.</span><span class="sxs-lookup"><span data-stu-id="f80a9-174">You can also modify the new report later, upon request.</span></span> <span data-ttu-id="f80a9-175">الترميز غير مطلوب.</span><span class="sxs-lookup"><span data-stu-id="f80a9-175">No coding is required.</span></span>

1. <span data-ttu-id="f80a9-176">لتشغيل التقرير الموجود، انتقل إلى **الاستبيان** \> **تصميم** \> **تقرير الاستبيانات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-176">To run the existing report, go to **Questionnaire** \> **Design** \> **Questionnaires report**.</span></span>

    ![تحديد عنصر قائمة تقرير الاستبيانات في الوحدة النمطية للاستبيان لتشغيل تقرير SSRS الموجود](./media/er-quick-start1-application-menu-origin.png)

2. <span data-ttu-id="f80a9-178">في مربع الحوار **تقرير الاستبيانات**، حدد معايير التحديد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-178">In the **Questionnaires report** dialog box, specify selection criteria.</span></span> <span data-ttu-id="f80a9-179">طبّق عامل تصفية بحيث يتضمن التقرير الاستبيان **SBCCrsExam** فقط.</span><span class="sxs-lookup"><span data-stu-id="f80a9-179">Apply a filter so that the report includes only the **SBCCrsExam** questionnaire.</span></span>

    ![تحديد معايير التحديد. في مربع الحوار "تقرير الاستبيانات"](./media/er-quick-start1-ssrs-report-dialog.png)

<span data-ttu-id="f80a9-181">يبين الرسم التوضيحي التالي الإصدار الذي تم إنشاؤه من تقرير SSRS للاستبيان ‎**SBCCrsExam**</span><span class="sxs-lookup"><span data-stu-id="f80a9-181">The following illustration shows the generated version of the SSRS report for the **SBCCrsExam** questionnaire.</span></span>

![تقرير SSRS المُنشأ](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a><span data-ttu-id="f80a9-183">تكوين إطار عمل ER</span><span class="sxs-lookup"><span data-stu-id="f80a9-183">Configure the ER framework</span></span>

<span data-ttu-id="f80a9-184">كمستخدم يؤدي دور مطور إعداد التقارير الإلكترونية، يجب عليك تكوين مجموعة صغيرة من معلمات التقارير الإلكترونية قبل بدء استخدام إطار عمل إعداد التقارير الإلكترونية لتصميم الحل الجديد لإعداد التقارير الإلكترونية..</span><span class="sxs-lookup"><span data-stu-id="f80a9-184">As a user in the Electronic Reporting Developer role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design your new ER solution.</span></span>

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a><span data-ttu-id="f80a9-185">تكوين معلمات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f80a9-185">Configure ER parameters</span></span>

1. <span data-ttu-id="f80a9-186">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-186">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f80a9-187">في مساحة عمل **إعداد التقارير الإلكترونية**، حدد **معلمات ‏‫إعداد التقارير الإلكترونية‬**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-187">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="f80a9-188">في صفحة **معلمات التقارير الإلكترونية**، على علامة التبويب **عام**، عيّن الخيار **تمكين وضع التصميم** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-188">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="f80a9-189">في علامة التبويب **المرفقات**، عيّن المعلمات التالية:</span><span class="sxs-lookup"><span data-stu-id="f80a9-189">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="f80a9-190">قم بتعيين حقل **التكوينات** إلى **الملف** لشركة **USMF**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-190">Set the **Configurations** field to **File** for the **USMF** company.</span></span>
    - <span data-ttu-id="f80a9-191">قم بتعيين حقول **أرشيف الوظيفة** و **المؤقت** و **الأساس** و **أخرى** إلى **الملف**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-191">Set **Job archive**, **Temporary**, **Baseline**, and **Others** fields to **File**.</span></span>

<span data-ttu-id="f80a9-192">لمزيد من المعلومات حول معلمات ER، راجع [تكوين إطار عمل ER](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f80a9-192">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a><span data-ttu-id="f80a9-193">تنشيط موفر تكوين ER</span><span class="sxs-lookup"><span data-stu-id="f80a9-193">Activate an ER configuration provider</span></span>

<span data-ttu-id="f80a9-194">يتم تمييز كل تكوين لإعداد التقارير الإلكترونية كمملوك من موفر تكوين التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-194">Every ER configuration is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="f80a9-195">بالتالي، يجب عليك تنشيط موفر تكوين التقارير الإلكترونية في مساحة عمل **إعداد التقارير الإلكترونية** قبل البدء في إضافة تكوينات التقارير الإلكترونية وتحريرها.</span><span class="sxs-lookup"><span data-stu-id="f80a9-195">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit any ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="f80a9-196">يمكن لمالك تكوين ER فقط تحريره.</span><span class="sxs-lookup"><span data-stu-id="f80a9-196">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="f80a9-197">بالتالي، قبل تحرير تكوين ER، يجب تنشيط موفر تكوين ER المناسب في مساحة عمل **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-197">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a><span data-ttu-id="f80a9-198">مراجعة قائمة موفري تكوين ER</span><span class="sxs-lookup"><span data-stu-id="f80a9-198">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="f80a9-199">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-199">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f80a9-200">في مساحة عمل **إعداد التقارير الإلكترونية**، في قسم **الارتباطات‬ ذات الصلة**، حدد **موفرو التكوين**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-200">In the **Electronic reporting** workspace, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="f80a9-201">في صفحة **موفرو التكوين**، يتضمن كل سجل موفر تكوين اسمًا وعنوان URL فريدين.</span><span class="sxs-lookup"><span data-stu-id="f80a9-201">On the **Configuration providers** page, each configuration provider record has a unique name and URL.</span></span> <span data-ttu-id="f80a9-202">راجع محتويات هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-202">Review the contents of this page.</span></span> <span data-ttu-id="f80a9-203">في حالة وجود سجل لـ **Litware, Inc.** (`https://www.litware.com`) بالفعل، فتخطي الإجراء التالي، [إضافة موفر تكوين ER جديد](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="f80a9-203">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a><span data-ttu-id="f80a9-204">إضافة موفر تكوين ER جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-204">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="f80a9-205">في صفحة **موفري التكوين**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-205">On the **Configuration providers** page, select **New**.</span></span>
2. <span data-ttu-id="f80a9-206">في حقل **الاسم**، أدخل **Litware, Inc**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-206">In the **Name** field, enter **Litware, Inc.**</span></span>
3. <span data-ttu-id="f80a9-207">في الحقل **عنوان الإنترنت**، أدخل `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="f80a9-207">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
4. <span data-ttu-id="f80a9-208">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-208">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a><span data-ttu-id="f80a9-209">تنشيط موفر تكوين ER</span><span class="sxs-lookup"><span data-stu-id="f80a9-209">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="f80a9-210">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-210">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f80a9-211">في مساحة عمل **إعداد التقارير الإلكترونية**، حدد موفر التكوين **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-211">In the **Electronic reporting** workspace, select the **Litware, Inc.** configuration provider.</span></span>
3. <span data-ttu-id="f80a9-212">حدد **تعيين كنشط**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-212">Select **Set active**.</span></span>

<span data-ttu-id="f80a9-213">لمزيد من المعلومات حول موفري تكوين ER، راجع [إنشاء موفري التكوين ووضع علامة عليهم كنشطين](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f80a9-213">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a><span data-ttu-id="f80a9-214">تصميم نموذج بيانات خاص بالمجال</span><span class="sxs-lookup"><span data-stu-id="f80a9-214">Design a domain-specific data model</span></span>

<span data-ttu-id="f80a9-215">يجب إنشاء تكوين جديد للتقارير الإلكترونية يحتوي على مكون [نموذج بيانات](general-electronic-reporting.md#data-model-and-model-mapping-components) لمجال عمل **الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-215">You must create a new ER configuration that contains a [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** business domain.</span></span> <span data-ttu-id="f80a9-216">سيتم استخدام نموذج البيانات هذا لاحقًا كمصدر بيانات عند تصميم تنسيق التقارير الإلكترونية لإنشاء تقرير **الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-216">This data model will later be used as a data source when you design an ER format to generate the **Questionnaire** report.</span></span>

<span data-ttu-id="f80a9-217">ومن خلال إكمال الخطوات الواردة في القسم [استيراد تكوين نموذج بيانات جديد](#ImportDataModel)، يمكنك استيراد نموذج البيانات المطلوب من ملف XML الذي تم توفيره.</span><span class="sxs-lookup"><span data-stu-id="f80a9-217">By completing the steps in the [Import a new data model configuration](#ImportDataModel) section, you can import the required data model from the provided XML file.</span></span> <span data-ttu-id="f80a9-218">أو يمكنك إكمال الخطوات الواردة في القسم [إنشاء تكوين نموذج بيانات جديد](#DesignDataModel) لتصميم نموذج البيانات هذا من البداية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-218">Alternatively, you can complete the steps in the [Create a new data model configuration](#DesignDataModel) section to design this data model from scratch.</span></span>

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a><span data-ttu-id="f80a9-219">استيراد تكوين نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-219">Import a new data model configuration</span></span>

1. <span data-ttu-id="f80a9-220">قم بتنزيل الملف [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) واحفظه في جهاز الكمبيوتر المحلي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-220">Download the [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="f80a9-221">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-221">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="f80a9-222">في مساحة عمل **إعداد التقارير الإلكترونية**، حدد **تكوينات إعداد التقارير**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-222">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="f80a9-223">في جزء الإجراءات، حدد **التبادل** \> **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-223">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="f80a9-224">حدد **استعراض** ثم ابحث عن الملف **Questionnaires model.version.1.xml** وحدده.</span><span class="sxs-lookup"><span data-stu-id="f80a9-224">Select **Browse**, and then find and select the **Questionnaires model.version.1.xml** file.</span></span>
6. <span data-ttu-id="f80a9-225">حدد **موافق** لاستيراد التكوين.</span><span class="sxs-lookup"><span data-stu-id="f80a9-225">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="f80a9-226">للمتابعة، انتقل إلى الاجراء التالي، [إنشاء تكوين نموذج بيانات جديد](#DesignDataModel).</span><span class="sxs-lookup"><span data-stu-id="f80a9-226">To continue, skip the next procedure, [Create a new data model configuration](#DesignDataModel).</span></span>

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a><span data-ttu-id="f80a9-227">إنشاء تكوين نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-227">Create a new data model configuration</span></span>

1. <span data-ttu-id="f80a9-228">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-228">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f80a9-229">في مساحة عمل **إعداد التقارير الإلكترونية**، حدد **تكوينات إعداد التقارير**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-229">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="f80a9-230">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-230">Select **Create configuration**.</span></span>
4. <span data-ttu-id="f80a9-231">في مربع الحوار المنسدل، في الحقل **الاسم**، أدخل **نموذج الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-231">In the drop-down dialog box, in the **Name** field, enter **Questionnaire model**.</span></span>
5. <span data-ttu-id="f80a9-232">حدد **إنشاء تكوين** لإنشاء التكوين.</span><span class="sxs-lookup"><span data-stu-id="f80a9-232">Select **Create configuration** to create the configuration.</span></span>

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a><span data-ttu-id="f80a9-233">تسمية نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-233">Name the data model</span></span>

1. <span data-ttu-id="f80a9-234">في صفحة **التكوينات**، في شجرة التكوين، حدد **نموذج الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-234">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
2. <span data-ttu-id="f80a9-235">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-235">Select **Designer**.</span></span>
3. <span data-ttu-id="f80a9-236">في الصفحة **مصمم نموذج البيانات**، على علامة التبويب السريعة **عام**، في حقل **الاسم**، أدخل <a name="DataModeName"></a>**الاستبيانات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-236">On the **Data model designer** page, on the **General** FastTab, in the **Name** field, enter <a name="DataModeName"></a>**Questionnaires**.</span></span>

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a><span data-ttu-id="f80a9-237">إضافة حقول نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-237">Add new data model fields</span></span>

1. <span data-ttu-id="f80a9-238">في صفحة **مصمم نموذج البيانات**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-238">On the **Data model designer** page, select **New**.</span></span>
2. <span data-ttu-id="f80a9-239">في مربع الحوار المنسدل لإضافة عقدة نموذج بيانات، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f80a9-239">In the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="f80a9-240">حدد **جذر النموذج** لنوع العقدة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-240">Select **Model root** as the type of the new node.</span></span>
    2. <span data-ttu-id="f80a9-241">في الحقل **الاسم**، أدخل <a name="RootDefinitionName"></a>**جذر**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-241">In the **Name** field, enter <a name="RootDefinitionName"></a>**Root**.</span></span>
    3. <span data-ttu-id="f80a9-242">حدد **إضافة** لإضافة عقدة جديدة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-242">Select **Add** to add the new node.</span></span>

    <span data-ttu-id="f80a9-243">سيتم استخدام واصف الجذر هذا لتوفير بيانات لتقرير **الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-243">This root descriptor will be used to provide data for the **Questionnaire** report.</span></span> <span data-ttu-id="f80a9-244">يمكن وجود واصفات متعددة لنموذج بيانات واحد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-244">A single data model can have multiple descriptors.</span></span> <span data-ttu-id="f80a9-245">يمكن تحديد كل واصف لتنسيق تقارير إلكترونية واحد، لتعريف البيانات المطلوبة لإنشاء التقرير.</span><span class="sxs-lookup"><span data-stu-id="f80a9-245">Each descriptor can be specified for a single ER format, to identify data that is required to generate the report.</span></span>

3. <span data-ttu-id="f80a9-246">حدد **جديد** مرة أخرى، ثم في مربع الحوار المنسدل لإضافة عقدة نموذج بيانات، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f80a9-246">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="f80a9-247">حدد **تابع لعقدة نشطة** كنوع العقدة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-247">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="f80a9-248">في الحقل **الاسم**، أدخل **‏‫CompanyName‬**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-248">In the **Name** field, enter **CompanyName**.</span></span>
    3. <span data-ttu-id="f80a9-249">في الحقل **نوع الصنف**، حدد **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-249">In the **Item type** field, select **String**.</span></span>
    4. <span data-ttu-id="f80a9-250">حدد **إضافة** لإضافة الحقل الجديد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-250">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="f80a9-251">هذا الحقل مطلوب لتمرير اسم الشركة الحالية إلى تقرير إعداد التقارير الإلكترونية الذي يستهلك نموذج البيانات هذا كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-251">This field is required to pass the name of the current company to an ER report that consumes this data model as a data source.</span></span>

4. <span data-ttu-id="f80a9-252">حدد **جديد** مرة أخرى، ثم في مربع الحوار المنسدل لإضافة عقدة نموذج بيانات، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f80a9-252">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="f80a9-253">حدد **تابع لعقدة نشطة** كنوع العقدة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-253">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="f80a9-254">في الحقل **الاسم**، أدخل **‏‫الاستبيان‬**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-254">In the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="f80a9-255">في حقل **نوع الصنف**، حدد **قائمة سجلات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-255">In the **Item type** field, select **Record list**.</span></span>
    4. <span data-ttu-id="f80a9-256">حدد **إضافة** لإضافة الحقل الجديد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-256">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="f80a9-257">سيتم استخدام هذا الحقل لتمرير قائمة الاستبيانات لتقرير إعداد التقارير الإلكترونية الذي يستهلك نموذج البيانات هذا كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-257">This field will be used to pass the list of questionnaires to an ER report that consumes this data model as a data source.</span></span>

5. <span data-ttu-id="f80a9-258">حدد عقدة **الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-258">Select the **Questionnaire** node.</span></span>
6. <span data-ttu-id="f80a9-259">تابع إضافة الحقول المطلوبة لنموذج البيانات القابل للتحرير بنفس الطريقة حتى إكمال بنية نموذج البيانات التالية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-259">Continue to add the required fields of the editable data model in the same manner until you complete the following data model structure.</span></span>

    | <span data-ttu-id="f80a9-260">مسار حقل</span><span class="sxs-lookup"><span data-stu-id="f80a9-260">Field path</span></span>                                                    | <span data-ttu-id="f80a9-261">نوع البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-261">Data type</span></span>   | <span data-ttu-id="f80a9-262">تعيين الحقل/القيمة المرتجعة</span><span class="sxs-lookup"><span data-stu-id="f80a9-262">Field designation/returned value</span></span> |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | <span data-ttu-id="f80a9-263">Root</span><span class="sxs-lookup"><span data-stu-id="f80a9-263">Root</span></span>                                                          |             | <span data-ttu-id="f80a9-264">النقطة المرجعية لطلب بيانات الاستبيان.</span><span class="sxs-lookup"><span data-stu-id="f80a9-264">The reference point to request questionnaire data.</span></span> |
    | <span data-ttu-id="f80a9-265">Root\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="f80a9-265">Root\\CompanyName</span></span>                                             | <span data-ttu-id="f80a9-266">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-266">String</span></span>      | <span data-ttu-id="f80a9-267">اسم الشركة الحالية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-267">The name of the current company.</span></span> |
    | <span data-ttu-id="f80a9-268">Root\\ExecutionContext</span><span class="sxs-lookup"><span data-stu-id="f80a9-268">Root\\ExecutionContext</span></span>                                        | <span data-ttu-id="f80a9-269">تسجيل</span><span class="sxs-lookup"><span data-stu-id="f80a9-269">Record</span></span>      | <span data-ttu-id="f80a9-270">تفاصيل تنفيذ التنسيق.</span><span class="sxs-lookup"><span data-stu-id="f80a9-270">Format execution details.</span></span> |
    | <span data-ttu-id="f80a9-271">Root\\ExecutionContext\\FormatName</span><span class="sxs-lookup"><span data-stu-id="f80a9-271">Root\\ExecutionContext\\FormatName</span></span>                            | <span data-ttu-id="f80a9-272">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-272">String</span></span>      | <span data-ttu-id="f80a9-273">اسم تنسيق التقارير الإلكترونية الذي يجري تشغيله.</span><span class="sxs-lookup"><span data-stu-id="f80a9-273">The name of the ER format that is being run.</span></span> |
    | <span data-ttu-id="f80a9-274">Root\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="f80a9-274">Root\\Questionnaire</span></span>                                           | <span data-ttu-id="f80a9-275">قائمة السجلات</span><span class="sxs-lookup"><span data-stu-id="f80a9-275">Record list</span></span> | <span data-ttu-id="f80a9-276">قائمة الاستبيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-276">The list of questionnaires</span></span> |
    | <span data-ttu-id="f80a9-277">Root\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="f80a9-277">Root\\Questionnaire\\Active</span></span>                                   | <span data-ttu-id="f80a9-278">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-278">String</span></span>      | <span data-ttu-id="f80a9-279">حالة الاستبيان الحالي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-279">The status of the current questionnaire.</span></span> |
    | <span data-ttu-id="f80a9-280">Root\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="f80a9-280">Root\\Questionnaire\\Code</span></span>                                     | <span data-ttu-id="f80a9-281">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-281">String</span></span>      | <span data-ttu-id="f80a9-282">كود الاستبيان الحالي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-282">The code of the current questionnaire.</span></span> |
    | <span data-ttu-id="f80a9-283">Root\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="f80a9-283">Root\\Questionnaire\\Description</span></span>                              | <span data-ttu-id="f80a9-284">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-284">String</span></span>      | <span data-ttu-id="f80a9-285">وصف الاستبيان الحالي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-285">The description of the current questionnaire.</span></span> |
    | <span data-ttu-id="f80a9-286">Root\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="f80a9-286">Root\\Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="f80a9-287">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-287">String</span></span>      | <span data-ttu-id="f80a9-288">نوع الاستبيان الحالي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-288">The type of the current questionnaire.</span></span> |
    | <span data-ttu-id="f80a9-289">Root\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="f80a9-289">Root\\Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="f80a9-290">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-290">String</span></span>      | <span data-ttu-id="f80a9-291">الترتيب الرقمي للاستبيان الحالي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-291">The numerical order of the current questionnaire.</span></span> |
    | <span data-ttu-id="f80a9-292">Root\\Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="f80a9-292">Root\\Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="f80a9-293">تسجيل</span><span class="sxs-lookup"><span data-stu-id="f80a9-293">Record</span></span>      | <span data-ttu-id="f80a9-294">معلمات نتيجة الاستبيان الحالي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-294">The result parameters of the current questionnaire.</span></span> |
    | <span data-ttu-id="f80a9-295">Root\\Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="f80a9-295">Root\\Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="f80a9-296">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-296">String</span></span>      | <span data-ttu-id="f80a9-297">كود تعريف مجموعة النتائج الحالية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-297">The identification code of the current result group.</span></span> |
    | <span data-ttu-id="f80a9-298">Root\\Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="f80a9-298">Root\\Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="f80a9-299">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-299">String</span></span>      | <span data-ttu-id="f80a9-300">وصف مجموعة النتائج الحالية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-300">The description of the current result group.</span></span> |
    | <span data-ttu-id="f80a9-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="f80a9-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="f80a9-302">حقيقي</span><span class="sxs-lookup"><span data-stu-id="f80a9-302">Real</span></span>        | <span data-ttu-id="f80a9-303">الحد الأقصى لعدد النقاط التي يمكن كسبها.</span><span class="sxs-lookup"><span data-stu-id="f80a9-303">The maximum number of points that could be earned.</span></span> |
    | <span data-ttu-id="f80a9-304">Root\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="f80a9-304">Root\\Questionnaire\\Question</span></span>                                 | <span data-ttu-id="f80a9-305">قائمة السجلات</span><span class="sxs-lookup"><span data-stu-id="f80a9-305">Record list</span></span> | <span data-ttu-id="f80a9-306">قائمة الأسئلة الخاصة بالاستبيان الحالي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-306">The list of questions for the current questionnaire.</span></span> |
    | <span data-ttu-id="f80a9-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="f80a9-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="f80a9-308">عدد صحيح</span><span class="sxs-lookup"><span data-stu-id="f80a9-308">Integer</span></span>     | <span data-ttu-id="f80a9-309">الرقم التسلسلي لمجموعة الإجابات الحالية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-309">The sequence number of the current answer collection.</span></span> |
    | <span data-ttu-id="f80a9-310">Root\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="f80a9-310">Root\\Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="f80a9-311">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-311">String</span></span>      | <span data-ttu-id="f80a9-312">كود تعريف السؤال الحالي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-312">The identification code of the current question.</span></span> |
    | <span data-ttu-id="f80a9-313">Root\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="f80a9-313">Root\\Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="f80a9-314">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-314">String</span></span>      | <span data-ttu-id="f80a9-315">علامة تشير إلى ما إذا كان يجب الإجابة على السؤال الحالي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-315">A flag that indicates whether the current question must be answered.</span></span> |
    | <span data-ttu-id="f80a9-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="f80a9-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="f80a9-317">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-317">String</span></span>      | <span data-ttu-id="f80a9-318">علامة تشير إلى ما إذا كان السؤال الحالي عبارة عن سؤال أساسي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-318">A flag that indicates whether the current question is primary.</span></span> |
    | <span data-ttu-id="f80a9-319">Root\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="f80a9-319">Root\\Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="f80a9-320">عدد صحيح</span><span class="sxs-lookup"><span data-stu-id="f80a9-320">Integer</span></span>     | <span data-ttu-id="f80a9-321">الرقم التسلسلي للسؤال الحالي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-321">The sequence number of the current question.</span></span> |
    | <span data-ttu-id="f80a9-322">Root\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="f80a9-322">Root\\Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="f80a9-323">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-323">String</span></span>      | <span data-ttu-id="f80a9-324">نص السؤال الحالي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-324">The text of the current question.</span></span> |
    | <span data-ttu-id="f80a9-325">Root\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="f80a9-325">Root\\Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="f80a9-326">قائمة السجلات</span><span class="sxs-lookup"><span data-stu-id="f80a9-326">Record list</span></span> | <span data-ttu-id="f80a9-327">قائمة الإجابات على السؤال الحالي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-327">The list of answers for the current question.</span></span> |
    | <span data-ttu-id="f80a9-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="f80a9-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="f80a9-329">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-329">String</span></span>      | <span data-ttu-id="f80a9-330">علامة تشير إلى ما إذا كانت الإجابة الحالية صحيحة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-330">A flag that indicates whether the current answer is correct.</span></span> |
    | <span data-ttu-id="f80a9-331">Root\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="f80a9-331">Root\\Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="f80a9-332">حقيقي</span><span class="sxs-lookup"><span data-stu-id="f80a9-332">Real</span></span>        | <span data-ttu-id="f80a9-333">النقاط التي تم اكتسابها عند تحديد الإجابة الحالية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-333">The points that are earned when the current answer is selected.</span></span> |
    | <span data-ttu-id="f80a9-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="f80a9-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="f80a9-335">عدد صحيح</span><span class="sxs-lookup"><span data-stu-id="f80a9-335">Integer</span></span>     | <span data-ttu-id="f80a9-336">الرقم التسلسلي للإجابة الحالية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-336">The sequence number of the current answer.</span></span> |
    | <span data-ttu-id="f80a9-337">Root\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="f80a9-337">Root\\Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="f80a9-338">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-338">String</span></span>      | <span data-ttu-id="f80a9-339">نص الإجابة الحالية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-339">The text of the current answer.</span></span> |

    <span data-ttu-id="f80a9-340">يبين الرسم التوضيحي التالي نموذج البيانات المكتمل القابل للتحرير في صفحة **مصمم نموذج البيانات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-340">The following illustration shows the completed editable data model on the **Data model designer** page.</span></span>

    ![نموذج بيانات مكوّن في مصمم نموذج بيانات إعداد التقارير الإلكترونية](./media/er-quick-start1-model2.png)

7. <span data-ttu-id="f80a9-342">‏‏قم بحفظ التغييرات التي قمت بإجرائها.</span><span class="sxs-lookup"><span data-stu-id="f80a9-342">Save your changes.</span></span>
8. <span data-ttu-id="f80a9-343">أغلق صفحة **مصمم نموذج البيانات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-343">Close the **Data model designer** page.</span></span>

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a><span data-ttu-id="f80a9-344">إكمال تصميم نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-344">Complete the design of the data model</span></span>

1. <span data-ttu-id="f80a9-345">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-345">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f80a9-346">في صفحة **التكوينات**، في شجرة التكوين، حدد **نموذج الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-346">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="f80a9-347">في علامة التبويب السريعة **الإصدارات**، حدد إصدار التكوين بحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-347">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="f80a9-348">حدد **تغيير الحالة** \> **مكتمل‏‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-348">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="f80a9-349">تم تغيير حالة الإصدار 1 من هذا التكوين من **مسودة** إلى **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-349">The status of version 1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="f80a9-350">لم يعد من الممكن تغيير الإصدار 1.</span><span class="sxs-lookup"><span data-stu-id="f80a9-350">Version 1 can no longer be changed.</span></span> <span data-ttu-id="f80a9-351">يحتوي هذا الإصدار على نموذج البيانات الذي تم تكوينه ويمكن استخدامه كأساس لتكوينات إعداد التقارير الإلكترونية الأخرى.</span><span class="sxs-lookup"><span data-stu-id="f80a9-351">This version contains the configured data model and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="f80a9-352">تم إنشاء الإصدار 2 من هذا التكوين وهو بالحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-352">Version 2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="f80a9-353">يمكنك تحرير هذا الإصدار لتعديل نموذج بيانات **الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-353">You can edit this version to adjust the **Questionnaire** data model.</span></span>

![إصدارات التكوين القابل للتعديل في صفحة التكوينات](./media/er-quick-start1-model-configuration.png)

<span data-ttu-id="f80a9-355">لمزيد من المعلومات حول تعيين إصدار تكوينات إعداد التقارير الإلكترونية، راجع [نظرة عامة حول إعداد التقارير الإلكترونية](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="f80a9-355">For more information about versioning for ER configurations, see [Electronic reporting (ER) overview](general-electronic-reporting.md#component-versioning).</span></span>

> [!NOTE]
> <span data-ttu-id="f80a9-356">يعتبر نموذج البيانات الذي تم تكوينه التمثيل المجرد لمجال عمل **الاستبيان** ولا يحتوي على أي علاقات بالبيانات الاصطناعية الخاصة بتطبيق Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="f80a9-356">The configured data model is your abstract representation of the **Questionnaire** business domain and contains no relations to artefacts that are specific to Microsoft Dynamics 365 Finance.</span></span>

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a><span data-ttu-id="f80a9-357">تصميم تعيين نموذج لنموذج البيانات المكوّن</span><span class="sxs-lookup"><span data-stu-id="f80a9-357">Design a model mapping for the configured data model</span></span>

<span data-ttu-id="f80a9-358">كمستخدم يؤدي دور مطور إعداد التقارير الإلكترونية، يجب عليك إنشاء تكوين جديد لإعداد التقارير الإلكترونية يحتوي على مكون [تعيين نموذج](general-electronic-reporting.md#data-model-and-model-mapping-components) لنموذج بيانات **الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-358">As a user in the Electronic Reporting Developer role, you must create a new ER configuration that contains a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** data model.</span></span> <span data-ttu-id="f80a9-359">لأن هذا المكون يقوم بتطبيق نموذج البيانات الذي تم تكوينه لتطبيق Finance، فهو خاص بتطبيق Finance.</span><span class="sxs-lookup"><span data-stu-id="f80a9-359">Because this component implements the configured data model for Finance, it's Finance-specific.</span></span> <span data-ttu-id="f80a9-360">يجب تكوين مكون تعيين النموذج لتحديد كائنات التطبيق التي يجب استخدامها لتعبئة نموذج البيانات الذي تم تكوينه بواسطة بيانات التطبيق في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="f80a9-360">You must configure the model mapping component to specify the application objects that must be used to fill in the configured data model with application data at runtime.</span></span> <span data-ttu-id="f80a9-361">لإكمال هذه المهمة، يجب أن تكون على علم بتفاصيل التنفيذ لبنية البيانات لمجال عمل **الاستبيان** في Finance.</span><span class="sxs-lookup"><span data-stu-id="f80a9-361">To complete this task, you must be aware of the implementation details of the data structure of the **Questionnaire** business domain in Finance.</span></span>

<span data-ttu-id="f80a9-362">ومن خلال إكمال الخطوات الواردة في القسم [استيراد تكوين تعيين نموذج جديد](#ImportModelMapping)، يمكنك استيراد تكوين تعيين النموذج من ملف XML الذي تم توفيره.</span><span class="sxs-lookup"><span data-stu-id="f80a9-362">By completing the steps in the [Import a new model mapping configuration](#ImportModelMapping) section that follows, you can import the required model mapping configuration from the provided XML file.</span></span> <span data-ttu-id="f80a9-363">أو يمكنك إكمال الخطوات الواردة في القسم [إنشاء تكوين تعيين نموذج جديد](#CreateModelMapping) لتصميم تعيين النموذج هذا من البداية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-363">Alternatively, you can complete the steps in the [Create a new model mapping configuration](#CreateModelMapping) section to design this model mapping from scratch.</span></span>

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a><span data-ttu-id="f80a9-364">استيراد تكوين تعيين نموذج جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-364">Import a new model mapping configuration</span></span>

1. <span data-ttu-id="f80a9-365">قم بتنزيل الملف [Questionnaires mapping.version.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) واحفظه في جهاز الكمبيوتر المحلي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-365">Download the [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="f80a9-366">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-366">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="f80a9-367">في مساحة عمل **إعداد التقارير الإلكترونية**، حدد **تكوينات إعداد التقارير**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-367">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="f80a9-368">في جزء الإجراءات، حدد **التبادل** \> **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-368">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="f80a9-369">حدد **استعراض** ثم ابحث عن الملف **Questionnaires mapping.version.1.xml** وحدده.</span><span class="sxs-lookup"><span data-stu-id="f80a9-369">Select **Browse**, and then find and select the **Questionnaires mapping.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="f80a9-370">حدد **موافق** لاستيراد التكوين.</span><span class="sxs-lookup"><span data-stu-id="f80a9-370">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="f80a9-371">للمتابعة، انتقل إلى الاجراء التالي، [إنشاء تكوين تعيين نموذج جديد](#CreateModelMapping).</span><span class="sxs-lookup"><span data-stu-id="f80a9-371">To continue, skip the next procedure, [Create a new model mapping configuration](#CreateModelMapping).</span></span>

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a><span data-ttu-id="f80a9-372">إنشاء تكوين تعيين نموذج جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-372">Create a new model mapping configuration</span></span>

1. <span data-ttu-id="f80a9-373">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-373">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f80a9-374">في صفحة **التكوينات**، في شجرة التكوين، حدد **نموذج الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-374">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="f80a9-375">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-375">Select **Create configuration**.</span></span>
4. <span data-ttu-id="f80a9-376">في مربع الحوار المنسدل، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f80a9-376">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="f80a9-377">في الحقل **جديد**، حدد **تعيين النموذج استنادًا إلى استبيانات نموذج بيانات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="f80a9-378">في حقل **الاسم**، أدخل **تعيين الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-378">In the **Name** field, enter **Questionnaire mapping**.</span></span>
    3. <span data-ttu-id="f80a9-379">في الحقل **تعريف نموذج البيانات**، حدد تعريف **الجذر**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-379">In the **Data model definition** field, select the **Root** definition.</span></span>
    4. <span data-ttu-id="f80a9-380">حدد **إنشاء تكوين** لإنشاء التكوين.</span><span class="sxs-lookup"><span data-stu-id="f80a9-380">Select **Create configuration** to create the configuration.</span></span>

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a><span data-ttu-id="f80a9-381">تصميم مكون تعيين نموذج جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-381">Design a new model mapping component</span></span>

1. <span data-ttu-id="f80a9-382">في صفحة **التكوينات**، في شجرة التكوين، حدد **تعيين الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-382">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
2. <span data-ttu-id="f80a9-383">حدد **المصمم** لفتح قائمة التعيينات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-383">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="f80a9-384">حدد التعيين **تعيين الاستبيان** المضاف تلقائيًا لتعريف **الجذر**</span><span class="sxs-lookup"><span data-stu-id="f80a9-384">Select the **Questionnaires mapping** mapping that was automatically added for the **Root** definition</span></span>
4. <span data-ttu-id="f80a9-385">حدد **المصمم** لبدء تكوين التعيين المحدد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-385">Select **Designer** to start to configure the selected mapping.</span></span>

<span data-ttu-id="f80a9-386">يُضاف تعيين جديد بشكل تلقائي لتعريف **الجذر**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-386">A new mapping is automatically added for the **Root** definition.</span></span> <span data-ttu-id="f80a9-387">اتجاه هذا التعيين هو **إلى النموذج**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-387">This mapping has the **To model** direction.</span></span> <span data-ttu-id="f80a9-388">وبالتالي، يمكن استخدام هذا التعيين لتعبئة نموذج بيانات يحتوي على البيانات المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-388">Therefore, this mapping can be used to fill in a data model with required data.</span></span>

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a><span data-ttu-id="f80a9-389">إضافة مصادر بيانات للوصول إلى جداول التطبيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-389">Add data sources to access application tables</span></span>

<span data-ttu-id="f80a9-390">يجب تكوين مصادر البيانات للوصول إلى جداول التطبيق التي تحتوي على تفاصيل الاستبيان.</span><span class="sxs-lookup"><span data-stu-id="f80a9-390">You must configure data sources to access the application tables that contain questionnaire details.</span></span>

1. <span data-ttu-id="f80a9-391">في صفحة **مصمم تعيين النموذج**، في جزء **أنواع مصادر البيانات**، حدد **Dynamics 365 for Operations\\Table records**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-391">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="f80a9-392">أضف مصدر بيانات جديدًا سيتم استخدامه للوصول إلى الجدول KMCollection، حيث يمثل كل سجل استبيانًا واحدًا:</span><span class="sxs-lookup"><span data-stu-id="f80a9-392">Add a new data source that will be used to access the KMCollection table, where every record represents a single questionnaire:</span></span>

    1. <span data-ttu-id="f80a9-393">حدد **إضافة جذر** في جزء **مصادر البيانات** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-393">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="f80a9-394">في مربع الحوار، في الحقل **الاسم**، أدخل **الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-394">In dialog box, in the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="f80a9-395">في حقل **الجدول**، أدخل **KMCollection‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-395">In the **Table** field, enter **KMCollection**.</span></span>
    4. <span data-ttu-id="f80a9-396">عيّن الخيار **طلب الاستعلام** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-396">Set the **Ask for query** option to **Yes**.</span></span> <span data-ttu-id="f80a9-397">ستتمكن عندئذٍ من تحديد خيارات [التصفية](../../fin-ops/get-started/advanced-filtering-query-options.md) لهذا الجدول في مربع حوار استعلام النظام في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="f80a9-397">You will then be able to specify [filtering](../../fin-ops/get-started/advanced-filtering-query-options.md) options for this table in the system query dialog box at runtime.</span></span>
    5. <span data-ttu-id="f80a9-398">حدد **موافق** لإضافة مصدر البيانات الجديد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-398">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="f80a9-399">في الجزء **أنواع مصادر البيانات**، حدد **Dynamics 365 for Operations\\Table records**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-399">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
4. <span data-ttu-id="f80a9-400">أضف مصدر بيانات جديدًا سيتم استخدامه للوصول إلى الجدول KMQuestion، حيث يمثل كل سجل سؤالاً واحدًا في استبيان:</span><span class="sxs-lookup"><span data-stu-id="f80a9-400">Add a new data source that will be used to access the KMQuestion table, where every record represents a single question in a questionnaire:</span></span>

    1. <span data-ttu-id="f80a9-401">حدد **إضافة جذر** في جزء **مصادر البيانات** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-401">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="f80a9-402">في مربع الحوار، في الحقل **الاسم**، أدخل **السؤال**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-402">In the dialog box, in the **Name** field, enter **Question**.</span></span>
    3. <span data-ttu-id="f80a9-403">في حقل **الجدول**، أدخل **KMQuestion‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-403">In the **Table** field, enter **KMQuestion**.</span></span>
    4. <span data-ttu-id="f80a9-404">حدد **موافق** لإضافة مصدر البيانات الجديد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-404">Select **OK** to add the new data source.</span></span>

5. <span data-ttu-id="f80a9-405">في الجزء **أنواع مصادر البيانات**، حدد **Dynamics 365 for Operations\\Table records**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-405">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
6. <span data-ttu-id="f80a9-406">أضف مصدر بيانات جديدًا سيتم استخدامه للوصول إلى الجدول KMAnswer، حيث يمثل كل سجل إجابة واحدة على سؤال في استبيان:</span><span class="sxs-lookup"><span data-stu-id="f80a9-406">Add a new data source try that will be used to access the KMAnswer table, where every record represents a single answer to a question in a questionnaire:</span></span>

    1. <span data-ttu-id="f80a9-407">حدد **إضافة جذر** في جزء **مصادر البيانات** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-407">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="f80a9-408">في الحقل **الاسم**، أدخل **الإجابة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-408">In the **Name** field, enter **Answer**.</span></span>
    3. <span data-ttu-id="f80a9-409">في حقل **الجدول**، أدخل **KMAnswer‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-409">In the **Table** field, enter **KMAnswer**.</span></span>
    4. <span data-ttu-id="f80a9-410">حدد **موافق** لإضافة مصدر البيانات الجديد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-410">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="f80a9-411">في الجزء **أنواع مصادر البيانات**، حدد **الدالات\\الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-411">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="f80a9-412">أضف حقلاً محسوبًا جديدًا سيتم استخدامه للوصول إلى سجل من الجدول KMQuestionResultGroup من كل سجل لجدول KMCollection الأصل:</span><span class="sxs-lookup"><span data-stu-id="f80a9-412">Add a new calculated field that will be used to access a record of the KMQuestionResultGroup table from every record of the parent KMCollection table:</span></span>

    1. <span data-ttu-id="f80a9-413">حدد **الاستبيان** في جزء **مصادر البيانات** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-413">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="f80a9-414">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-414">Select **Add**.</span></span>
    3. <span data-ttu-id="f80a9-415">في مربع الحوار، في الحقل **الاسم‏‎**، أدخل **\$ResultGroup**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-415">In the dialog box, in the **Name** field, enter **\$ResultGroup**.</span></span>
    4. <span data-ttu-id="f80a9-416">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-416">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="f80a9-417">في [محرر معادلات إعداد التقارير الإلكترونية](general-electronic-reporting-formula-designer.md)، في حقل **المعادلة**، أدخل **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** لاستخدام [المسار](er-formula-language.md#Paths) لعلاقة واحد إلى واحد بين الجدولين KMCollection وKMQuestionResultGroup.</span><span class="sxs-lookup"><span data-stu-id="f80a9-417">In the [ER formula editor](general-electronic-reporting-formula-designer.md), in the **Formula** field, enter **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** to use the [path](er-formula-language.md#Paths) of the one-to-many relation between the KMCollection and KMQuestionResultGroup tables.</span></span>
    6. <span data-ttu-id="f80a9-418">حدد **حفظ** ثم قم بإغلاق محرر المعادلات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-418">Select **Save**, and close the formula editor.</span></span>
    7. <span data-ttu-id="f80a9-419">حدد **موافق** لإضافة الحقل المحسوب الجديد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-419">Select **OK** to add the new calculated field.</span></span>

9. <span data-ttu-id="f80a9-420">في الجزء **أنواع مصادر البيانات**، حدد **الدالات\\الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-420">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
10. <span data-ttu-id="f80a9-421">أضف حقلاً محسوبًا جديدًا سيتم استخدامه للوصول إلى سجلات السؤال من الجدول KMQuestion من كل سجل لجدول KMCollectionQuestion الأصل:</span><span class="sxs-lookup"><span data-stu-id="f80a9-421">Add a new calculated field that will be used to access question records of the KMQuestion table from every record of the parent KMCollectionQuestion table:</span></span>

    1. <span data-ttu-id="f80a9-422">حدد **الاستبيان** في جزء **مصادر البيانات** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-422">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="f80a9-423">قم بتوسيع عقدة **\<العلاقات** التي تحتوي على علاقات واحد إلى متعدد لجدول KMCollection.</span><span class="sxs-lookup"><span data-stu-id="f80a9-423">Expand the **\<Relations** node that contains one-to-many relations of the KMCollection table.</span></span>
    3. <span data-ttu-id="f80a9-424">حدد الجدول ذا الصلة **KMCollectionQuestion** ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-424">Select the related **KMCollectionQuestion** table, and then select **Add**.</span></span>
    4. <span data-ttu-id="f80a9-425">في مربع الحوار، في الحقل **الاسم‏‎**، أدخل **\$Question**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-425">In the dialog box, in the **Name** field, enter **\$Question**.</span></span>
    5. <span data-ttu-id="f80a9-426">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-426">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="f80a9-427">في محرر المعادلات، في حقل **المعادلة**، أدخل **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** لإرجاع سجلات السؤال المناسب من جدول KMQuestion.</span><span class="sxs-lookup"><span data-stu-id="f80a9-427">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** to return the appropriate question records from the KMQuestion table.</span></span>
    7. <span data-ttu-id="f80a9-428">حدد **حفظ** ثم قم بإغلاق محرر المعادلات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-428">Select **Save**, and close the formula editor.</span></span>
    8. <span data-ttu-id="f80a9-429">حدد **موافق** لإضافة الحقل المحسوب الجديد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-429">Select **OK** to add the new calculated field.</span></span>

11. <span data-ttu-id="f80a9-430">في الجزء **أنواع مصادر البيانات**، حدد **الدالات\\الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-430">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
12. <span data-ttu-id="f80a9-431">أضف حقلاً محسوبًا جديدًا سيتم استخدامه للوصول إلى سجلات الإجابة من الجدول KMAnswer من كل سجل لجدول KMAnswer الأصل:</span><span class="sxs-lookup"><span data-stu-id="f80a9-431">Add a new calculated field that will be used to access answer records of the KMAnswer table from every record of the parent KMQuestion table:</span></span>

    1. <span data-ttu-id="f80a9-432">في جزء **مصادر البيانات**، حدد **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-432">In the **Data sources** pane, select **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, and then select **Add**.</span></span>
    2. <span data-ttu-id="f80a9-433">في مربع الحوار، في الحقل **الاسم‏‎‏‎**، أدخل **\$Answer**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-433">In the dialog box, in the **Name** field, enter **\$Answer**.</span></span>
    3. <span data-ttu-id="f80a9-434">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-434">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="f80a9-435">في محرر المعادلات، في حقل **المعادلة‏‎**، أدخل **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** لإرجاع سجلات السؤال المناسب من جدول KMAnswer.</span><span class="sxs-lookup"><span data-stu-id="f80a9-435">In the formula editor, in the **Formula** field, enter **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** to return the appropriate answer records from the KMAnswer table.</span></span>
    5. <span data-ttu-id="f80a9-436">حدد **حفظ** ثم قم بإغلاق محرر المعادلات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-436">Select **Save**, and close the formula editor.</span></span>
    6. <span data-ttu-id="f80a9-437">حدد **موافق** لإضافة الحقل المحسوب الجديد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-437">Select **OK** to add the new calculated field.</span></span>

13. <span data-ttu-id="f80a9-438">في الجزء **أنواع مصادر البيانات**، حدد **Dynamics 365 for Operations\\الجدول**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-438">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table**.</span></span>
14. <span data-ttu-id="f80a9-439">أضف مصدر بيانات جديدًا سيتم استخدامه للوصول إلى أساليب الجدول معلومات الشركة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-439">Add a new data source that will be used to access methods of the CompanyInfo table.</span></span> <span data-ttu-id="f80a9-440">لاحظ أن أسلوب **find()** الخاص بهذا الجدول يرجع سجلاً يمثل شركة من مثيل Finance الحالي الذي تم استدعاء هذا التعيين في سياقه.</span><span class="sxs-lookup"><span data-stu-id="f80a9-440">Note that the **find()** method of this table returns a record that represents a company of the current Finance instance that this mapping is called in the context of.</span></span>

    1. <span data-ttu-id="f80a9-441">حدد **إضافة جذر** في جزء **مصادر البيانات** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-441">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="f80a9-442">في مربع الحوار، في الحقل **الاسم**، أدخل **معلومات الشركة‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-442">In the dialog box, in the **Name** field, enter **CompanyInfo**.</span></span>
    3. <span data-ttu-id="f80a9-443">في حقل **الجدول**، أدخل **معلومات الشركة‎‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-443">In the **Table** field, enter **CompanyInfo**.</span></span>
    4. <span data-ttu-id="f80a9-444">حدد **موافق** لإضافة مصدر البيانات الجديد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-444">Select **OK** to add the new data source.</span></span>

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a><span data-ttu-id="f80a9-445">إضافة مصادر بيانات للوصول إلى عمليات تعداد التطبيقات</span><span class="sxs-lookup"><span data-stu-id="f80a9-445">Add data sources to access application enumerations</span></span>

<span data-ttu-id="f80a9-446">يجب عليك تكوين مصادر البيانات للوصول إلى تعدادات التطبيقات ومقارنة قيمها مع قيم حقول من نوع **التعداد** في جداول التطبيق.</span><span class="sxs-lookup"><span data-stu-id="f80a9-446">You must configure data sources to access application enumerations and compare their values with values of fields of the **Enumeration** type in the application tables.</span></span> <span data-ttu-id="f80a9-447">يجب استخدام نتيجة المقارنة لملء الحقول المناسبة لنموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-447">You must use the result of the comparison to fill in appropriate fields of the data model.</span></span>

1. <span data-ttu-id="f80a9-448">في صفحة **مصمم تعيين النموذج**، في جزء **أنواع مصادر البيانات**، حدد **Dynamics 365 for Operations\\تعداد‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-448">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
2. <span data-ttu-id="f80a9-449">أضف مصدر بيانات جديدًا سيتم استخدامه للوصول إلى قيم التعداد **EnumAppNoYes‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-449">Add a new data source that will be used to access values of the **EnumAppNoYes** enumeration:</span></span>

    1. <span data-ttu-id="f80a9-450">حدد **إضافة جذر** في جزء **مصادر البيانات** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-450">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="f80a9-451">في مربع الحوار، في الحقل **الاسم**، أدخل **EnumAppNoYes‎‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-451">In the dialog box, in the **Name** field, enter **EnumAppNoYes**.</span></span>
    3. <span data-ttu-id="f80a9-452">في الحقل **التعداد**، أدخل **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-452">In the **Enumeration** field, enter **NoYes**.</span></span>
    4. <span data-ttu-id="f80a9-453">حدد **موافق** لإضافة مصدر البيانات الجديد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-453">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="f80a9-454">في الجزء **أنواع مصادر البيانات**، حدد **Dynamics 365 for Operations\\Enumeration‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-454">In the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
4. <span data-ttu-id="f80a9-455">أضف مصدر بيانات جديدًا سيتم استخدامه للوصول إلى قيم التعداد **KMCollectionQuestionMode‎‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-455">Add a new data source that will be used to access the values of the **KMCollectionQuestionMode** enumeration:</span></span>

    1. <span data-ttu-id="f80a9-456">حدد **إضافة جذر** في جزء **مصادر البيانات** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-456">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="f80a9-457">في مربع الحوار، في حقل **الاسم**، أدخل **EnumAppQuestionOrder**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-457">In the dialog box, in the **Name** field, enter **EnumAppQuestionOrder**.</span></span>
    3. <span data-ttu-id="f80a9-458">في الحقل **التعداد**، أدخل **KMCollectionQuestionMode**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-458">In the **Enumeration** field, enter **KMCollectionQuestionMode**.</span></span>
    4. <span data-ttu-id="f80a9-459">حدد **موافق** لإضافة مصدر البيانات الجديد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-459">Select **OK** to add the new data source.</span></span>

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a><span data-ttu-id="f80a9-460">إضافة تسميات التقارير الإلكترونية لإنشاء تقرير بلغة محددة</span><span class="sxs-lookup"><span data-stu-id="f80a9-460">Add ER labels to generate a report in a specified language</span></span>

<span data-ttu-id="f80a9-461">يمكنك إضافة تسميات التقارير الإلكترونية لتكوين بعض مصادر البيانات لإرجاع القيم التي تعتمد على اللغة التي تم تعريفها في سياق استدعاء تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="f80a9-461">You can add ER labels to configure some of your data sources to return values that depend on the language that is defined in the context of the model mapping's call.</span></span>

1. <span data-ttu-id="f80a9-462">في صفحة **مصمم تعيين النموذج**، في جزء **مصادر البيانات**، حدد **إجابة**، ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-462">On the **Model mapping designer** page, in the **Data sources** pane, select **Answer**, and then select **Edit**.</span></span>
2. <span data-ttu-id="f80a9-463">قم بتنشيط حقل **التسمية**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-463">Activate the **Label** field.</span></span>
3. <span data-ttu-id="f80a9-464">حدد **ترجمة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-464">Select **Translate**.</span></span>
4. <span data-ttu-id="f80a9-465">في مربع الحوار **نص الترجمة**، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f80a9-465">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="f80a9-466">في حقل **معرف التسمية**، أدخل **PositiveAnswer**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-466">In the **Label Id** field, enter **PositiveAnswer**.</span></span>
    2. <span data-ttu-id="f80a9-467">في حقل **النص باللغة الافتراضية**، أدخل **نعم**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-467">In the **Text in default language** field, enter **Yes**.</span></span>
    3. <span data-ttu-id="f80a9-468">حدد **ترجمة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-468">Select **Translate**.</span></span>
    4. <span data-ttu-id="f80a9-469">في حقل **معرف التسمية**، أدخل **NegativeAnswer**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-469">In the **Label Id** field, enter **NegativeAnswer**.</span></span>
    5. <span data-ttu-id="f80a9-470">في حقل **النص باللغة الافتراضية**، أدخل **لا**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-470">In the **Text in default language** field, enter **No**.</span></span>
    6. <span data-ttu-id="f80a9-471">حدد **ترجمة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-471">Select **Translate**.</span></span>

5. <span data-ttu-id="f80a9-472">قم بإغلاق مربع الحوار **ترجمة النص**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-472">Close the **Text translation** dialog box.</span></span>
6. <span data-ttu-id="f80a9-473">حدد **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-473">Select **Cancel**.</span></span>

![إضافة تسميات التقارير الإلكترونية لتعيين النموذج القابل للتحرير](./media/er-quick-start1-adding-labels.png)

<span data-ttu-id="f80a9-475">لقد قمت بإدخال تسميات التقارير الإلكترونية للغة الافتراضية فقط.</span><span class="sxs-lookup"><span data-stu-id="f80a9-475">You've entered ER labels only for the default language.</span></span> <span data-ttu-id="f80a9-476">لمزيد من المعلومات حول كيفية ترجمة تسميات التقارير الإلكترونية إلى لغات أخرى، راجع [تصميم تقارير متعددة اللغات](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="f80a9-476">For information about how ER labels can be translated into other languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a><span data-ttu-id="f80a9-477">إضافة مصدر بيانات لتحويل نتائج مقارنة قيم التعداد بقيمة نصية</span><span class="sxs-lookup"><span data-stu-id="f80a9-477">Add a data source to transform the results of comparing enumeration values to a text value</span></span>

<span data-ttu-id="f80a9-478">لأنه يجب عليك تحويل نتائج المقارنة بين قيم التعداد والقيم النصية عدة مرات بسبب اختلاف المصادر، من المستحسن تكوين هذا المنطق كمصدر بيانات واحد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-478">Because you must transform the results of the comparison between enumeration values and text values several times for difference sources, it's a good idea to configure this logic as a single data source.</span></span> <span data-ttu-id="f80a9-479">ومع ذلك، ولجعل مصدر البيانات هذا قابلاً لإعادة الاستخدام، يجب عليك عندئذٍ تكوينه كمصدر بيانات يتضمن معلمات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-479">However, to make this data source reusable, you must then configure it as the parametrized data source.</span></span> <span data-ttu-id="f80a9-480">لمزيد من المعلومات، راجع [اعتماد استدعاءات ذات معلمات لمصادر بيانات التقارير الإلكترونية لنوع الحقل المحسوب](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="f80a9-480">For more information, see [Support parameterized calls of ER data sources of the Calculated field type](er-calculated-field-type.md).</span></span>

1. <span data-ttu-id="f80a9-481">في صفحة **مصمم تعيين النموذج**، في جزء **أنواع مصادر البيانات**، حدد **General\\Empty container**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-481">On the **Model mapping designer** page, in the **Data source types** pane, select **General\\Empty container**.</span></span>
2. <span data-ttu-id="f80a9-482">إضافة مصدر بيانات حاوية جديد:</span><span class="sxs-lookup"><span data-stu-id="f80a9-482">Add a new container data source:</span></span>

    1. <span data-ttu-id="f80a9-483">حدد **إضافة جذر** في جزء **مصادر البيانات** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-483">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="f80a9-484">في مربع الحوار، في الحقل **الاسم**، أدخل **المساعد**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-484">In the dialog box, in the **Name** field, enter **Helper**.</span></span>
    3. <span data-ttu-id="f80a9-485">حدد **موافق** لإضافة مصدر البيانات الحاوية الجديد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-485">Select **OK** to add the new container data source.</span></span>

3. <span data-ttu-id="f80a9-486">في الجزء **أنواع مصادر البيانات**، حدد **الدالات\\الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-486">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="f80a9-487">إضافة مصدر بيانات جديد:</span><span class="sxs-lookup"><span data-stu-id="f80a9-487">Add a new data source:</span></span>

    1. <span data-ttu-id="f80a9-488">في جزء **مصادر البيانات**، حدد **المساعد** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-488">In the **Data sources** pane, select **Helper**.</span></span>
    2. <span data-ttu-id="f80a9-489">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-489">Select **Add**.</span></span>
    3. <span data-ttu-id="f80a9-490">في مربع الحوار، في حقل **الاسم**، أدخل **NoYesEnumToString**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-490">In the dialog box, in the **Name** field, enter **NoYesEnumToString**.</span></span>
    4. <span data-ttu-id="f80a9-491">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-491">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="f80a9-492">في محرر الصيغة، حدد **المعلمات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-492">In the formula editor, select **Parameters**.</span></span>
    6. <span data-ttu-id="f80a9-493">اتبع الخطوات التالية لتحديد معلمات للتعبير المكوّن:</span><span class="sxs-lookup"><span data-stu-id="f80a9-493">Follow these steps to specify parameters for the configured expression:</span></span>

        1. <span data-ttu-id="f80a9-494">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-494">Select **New**.</span></span>
        2. <span data-ttu-id="f80a9-495">في مربع الحوار، في الحقل **الاسم**، أدخل **الوسيطة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-495">In the dialog box, in the **Name** field, enter **Argument**.</span></span>
        3. <span data-ttu-id="f80a9-496">في الحقل **النوع**، حدد نوع البيانات **منطقي**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-496">In the **Type** field, select the **Boolean** data type.</span></span>
        4. <span data-ttu-id="f80a9-497">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-497">Select **OK**.</span></span>

    7. <span data-ttu-id="f80a9-498">في حقل **المعادلة**، أدخل **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** لإرجاع نص تسمية التقارير الإلكترونية المناسبة، بحسب لغة سياق التنفيذ وقيمة المعلمة المحددة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-498">In the **Formula** field, enter **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** to return the text of the appropriate ER label, depending on the language of the execution context and value of the specified parameter.</span></span>
    8. <span data-ttu-id="f80a9-499">حدد **حفظ** ثم قم بإغلاق محرر المعادلات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-499">Select **Save**, and close the formula editor.</span></span>
    9. <span data-ttu-id="f80a9-500">حدد **موافق** لإضافة مصدر البيانات الجديد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-500">Select **OK** to add the new data source.</span></span>

![تعيين نموذج مكوّن في مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a><span data-ttu-id="f80a9-502">ربط مصادر البيانات بحقول نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-502">Bind data sources to data model fields</span></span>

<span data-ttu-id="f80a9-503">يجب ربط مصادر البيانات التي تم تكوينها بحقول نموذج البيانات لتحديد كيف سيتم ملء نموذج البيانات ببيانات التطبيق في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="f80a9-503">You must bind the configured data sources to the fields of the data model to specify how the data model will by filled in with application data at runtime.</span></span>

1. <span data-ttu-id="f80a9-504">في صفحة **مصمم تعيين النموذج**، في جزء **نموذج البيانات**، حدد **اسم الشركة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-504">On the **Model mapping designer** page, in the **Data model** pane, select **CompanyName**.</span></span>
2. <span data-ttu-id="f80a9-505">في جزء **مصادر البيانات**، قم بتوسيع **معلومات الشركة**، ثم اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f80a9-505">In the **Data sources** pane, expand **CompanyInfo**, and then follow these steps:</span></span>

    1. <span data-ttu-id="f80a9-506">قم بتوسيع العقدة **CompanyInfo.find()** التي تمثل الأسلوب **find()** في جدول معلومات الشركة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-506">Expand the **CompanyInfo.find()** node that represents the **find()** method of the CompanyInfo table.</span></span>
    2. <span data-ttu-id="f80a9-507">حدد **CompanyInfo.find().Name**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-507">Select **CompanyInfo.find().Name**.</span></span>
    3. <span data-ttu-id="f80a9-508">حدد **ربط** لملء اسم الشركة الذي يتم استدعاء تعيين النموذج المكوّن لها في سياق وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="f80a9-508">Select **Bind** to fill in the name of the company that the configured model mapping is called in the context of at runtime.</span></span>

3. <span data-ttu-id="f80a9-509">حدد **الاستبيان** في جزء **نموذج البيانات** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-509">In the **Data model** pane, select **Questionnaire**.</span></span>
4. <span data-ttu-id="f80a9-510">في جزء **مصادر البيانات**، حدد **الاستبيان**، ثم حدد **ربط** لملء سجلات الاستبيان.</span><span class="sxs-lookup"><span data-stu-id="f80a9-510">In the **Data sources** pane, select **Questionnaire**, and then select **Bind** to fill in questionnaire records.</span></span>
5. <span data-ttu-id="f80a9-511">في جزء **نموذج البيانات**، قم بتوسيع **الاستبيان**، ثم اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f80a9-511">In the **Data model** pane, expand **Questionnaire**, and then follow these steps:</span></span>

    1. <span data-ttu-id="f80a9-512">حدد **نشط** في جزء **نموذج البيانات** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-512">In the **Data model** pane, select **Active**.</span></span>
    2. <span data-ttu-id="f80a9-513">حدد **تحرير** في جزء **نموذج البيانات** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-513">In the **Data model** pane, select **Edit**.</span></span>
    3. <span data-ttu-id="f80a9-514">في حقل **المعادلة**، أدخل **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** لملء النتيجة التي تعتمد على النص وعلى اللغة للمقارنة بين قيم التعداد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-514">In the **Formula** field, enter **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** to fill the text-dependent and language-dependent result of the comparison between enumeration values.</span></span>

6. <span data-ttu-id="f80a9-515">تابع لربط مصادر البيانات بحقول نموذج البيانات بنفس الطريقة حتى تحقق النتيجة التالية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-515">Continue to bind data sources to data model fields in the same manner until you achieve the following result.</span></span>

    | <span data-ttu-id="f80a9-516">مسار حقل</span><span class="sxs-lookup"><span data-stu-id="f80a9-516">Field path</span></span>                                              | <span data-ttu-id="f80a9-517">نوع البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-517">Data type</span></span>   | <span data-ttu-id="f80a9-518">الإجراء</span><span class="sxs-lookup"><span data-stu-id="f80a9-518">Action</span></span> | <span data-ttu-id="f80a9-519">تعبير الربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-519">Binding expression</span></span> |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | <span data-ttu-id="f80a9-520">اسم الشركة</span><span class="sxs-lookup"><span data-stu-id="f80a9-520">CompanyName</span></span>                                             | <span data-ttu-id="f80a9-521">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-521">String</span></span>      | <span data-ttu-id="f80a9-522">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-522">Bind</span></span>   | <span data-ttu-id="f80a9-523">CompanyInfo.'find()'.Name</span><span class="sxs-lookup"><span data-stu-id="f80a9-523">CompanyInfo.'find()'.Name</span></span> |
    | <span data-ttu-id="f80a9-524">الاستبيان</span><span class="sxs-lookup"><span data-stu-id="f80a9-524">Questionnaire</span></span>                                           | <span data-ttu-id="f80a9-525">قائمة السجلات</span><span class="sxs-lookup"><span data-stu-id="f80a9-525">Record list</span></span> | <span data-ttu-id="f80a9-526">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-526">Bind</span></span>   | <span data-ttu-id="f80a9-527">الاستبيان</span><span class="sxs-lookup"><span data-stu-id="f80a9-527">Questionnaire</span></span> |
    | <span data-ttu-id="f80a9-528">Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="f80a9-528">Questionnaire\\Active</span></span>                                   | <span data-ttu-id="f80a9-529">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-529">String</span></span>      | <span data-ttu-id="f80a9-530">تحرير</span><span class="sxs-lookup"><span data-stu-id="f80a9-530">Edit</span></span>   | <span data-ttu-id="f80a9-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="f80a9-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="f80a9-532">Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="f80a9-532">Questionnaire\\Code</span></span>                                     | <span data-ttu-id="f80a9-533">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-533">String</span></span>      | <span data-ttu-id="f80a9-534">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-534">Bind</span></span>   | <span data-ttu-id="f80a9-535">\@.kmCollectionId</span><span class="sxs-lookup"><span data-stu-id="f80a9-535">\@.kmCollectionId</span></span> |
    | <span data-ttu-id="f80a9-536">Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="f80a9-536">Questionnaire\\Description</span></span>                              | <span data-ttu-id="f80a9-537">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-537">String</span></span>      | <span data-ttu-id="f80a9-538">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-538">Bind</span></span>   | <span data-ttu-id="f80a9-539">\@.Description</span><span class="sxs-lookup"><span data-stu-id="f80a9-539">\@.Description</span></span> |
    | <span data-ttu-id="f80a9-540">Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="f80a9-540">Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="f80a9-541">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-541">String</span></span>      | <span data-ttu-id="f80a9-542">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-542">Bind</span></span>   | <span data-ttu-id="f80a9-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span><span class="sxs-lookup"><span data-stu-id="f80a9-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span></span> |
    | <span data-ttu-id="f80a9-544">Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="f80a9-544">Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="f80a9-545">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-545">String</span></span>      | <span data-ttu-id="f80a9-546">تحرير</span><span class="sxs-lookup"><span data-stu-id="f80a9-546">Edit</span></span>   | <span data-ttu-id="f80a9-547">CASE (\@.questionMode,</span><span class="sxs-lookup"><span data-stu-id="f80a9-547">CASE (\@.questionMode,</span></span><br><span data-ttu-id="f80a9-548">EnumAppQuestionOrder.Conditional, "Conditional",</span><span class="sxs-lookup"><span data-stu-id="f80a9-548">EnumAppQuestionOrder.Conditional, "Conditional",</span></span><br><span data-ttu-id="f80a9-549">EnumAppQuestionOrder.Random، "عشوائي (النسبة المئوية في الاستبيان)"،</span><span class="sxs-lookup"><span data-stu-id="f80a9-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span></span><br><span data-ttu-id="f80a9-550">EnumAppQuestionOrder.RandomGroup، "عشوائي (النسبة المئوية في مجموعات النتائج)"،</span><span class="sxs-lookup"><span data-stu-id="f80a9-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span></span><br><span data-ttu-id="f80a9-551">EnumAppQuestionOrder.Sequence، "تسلسلي"،</span><span class="sxs-lookup"><span data-stu-id="f80a9-551">EnumAppQuestionOrder.Sequence, "Sequential",</span></span><br><span data-ttu-id="f80a9-552">"")</span><span class="sxs-lookup"><span data-stu-id="f80a9-552">"")</span></span> |
    | <span data-ttu-id="f80a9-553">Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="f80a9-553">Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="f80a9-554">تسجيل</span><span class="sxs-lookup"><span data-stu-id="f80a9-554">Record</span></span>      |        | |
    | <span data-ttu-id="f80a9-555">Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="f80a9-555">Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="f80a9-556">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-556">String</span></span>      | <span data-ttu-id="f80a9-557">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-557">Bind</span></span>   | <span data-ttu-id="f80a9-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span><span class="sxs-lookup"><span data-stu-id="f80a9-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span></span> |
    | <span data-ttu-id="f80a9-559">Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="f80a9-559">Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="f80a9-560">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-560">String</span></span>      | <span data-ttu-id="f80a9-561">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-561">Bind</span></span>   | <span data-ttu-id="f80a9-562">\@.'\$ResultGroup'.description</span><span class="sxs-lookup"><span data-stu-id="f80a9-562">\@.'\$ResultGroup'.description</span></span> |
    | <span data-ttu-id="f80a9-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="f80a9-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="f80a9-564">حقيقي</span><span class="sxs-lookup"><span data-stu-id="f80a9-564">Real</span></span>        | <span data-ttu-id="f80a9-565">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-565">Bind</span></span>   | <span data-ttu-id="f80a9-566">\@.'\$ResultGroup'.maxPoint</span><span class="sxs-lookup"><span data-stu-id="f80a9-566">\@.'\$ResultGroup'.maxPoint</span></span> |
    | <span data-ttu-id="f80a9-567">Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="f80a9-567">Questionnaire\\Question</span></span>                                 | <span data-ttu-id="f80a9-568">قائمة السجلات</span><span class="sxs-lookup"><span data-stu-id="f80a9-568">Record list</span></span> | <span data-ttu-id="f80a9-569">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-569">Bind</span></span>   | <span data-ttu-id="f80a9-570">\@.'&lt;Relations'.KMCollectionQuestion</span><span class="sxs-lookup"><span data-stu-id="f80a9-570">\@.'&lt;Relations'.KMCollectionQuestion</span></span> |
    | <span data-ttu-id="f80a9-571">Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="f80a9-571">Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="f80a9-572">عدد صحيح</span><span class="sxs-lookup"><span data-stu-id="f80a9-572">Integer</span></span>     | <span data-ttu-id="f80a9-573">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-573">Bind</span></span>   | <span data-ttu-id="f80a9-574">\@.answerCollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="f80a9-574">\@.answerCollectionSequenceNumber</span></span> |
    | <span data-ttu-id="f80a9-575">Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="f80a9-575">Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="f80a9-576">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-576">String</span></span>      | <span data-ttu-id="f80a9-577">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-577">Bind</span></span>   | <span data-ttu-id="f80a9-578">\@.kmQuestionId</span><span class="sxs-lookup"><span data-stu-id="f80a9-578">\@.kmQuestionId</span></span> |
    | <span data-ttu-id="f80a9-579">Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="f80a9-579">Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="f80a9-580">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-580">String</span></span>      | <span data-ttu-id="f80a9-581">تحرير</span><span class="sxs-lookup"><span data-stu-id="f80a9-581">Edit</span></span>   | <span data-ttu-id="f80a9-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="f80a9-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="f80a9-583">Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="f80a9-583">Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="f80a9-584">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-584">String</span></span>      | <span data-ttu-id="f80a9-585">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-585">Bind</span></span>   | <span data-ttu-id="f80a9-586">\@.parentQuestionId</span><span class="sxs-lookup"><span data-stu-id="f80a9-586">\@.parentQuestionId</span></span> |
    | <span data-ttu-id="f80a9-587">Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="f80a9-587">Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="f80a9-588">عدد صحيح</span><span class="sxs-lookup"><span data-stu-id="f80a9-588">Integer</span></span>     | <span data-ttu-id="f80a9-589">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-589">Bind</span></span>   | <span data-ttu-id="f80a9-590">\@.SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="f80a9-590">\@.SequenceNumber</span></span> |
    | <span data-ttu-id="f80a9-591">Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="f80a9-591">Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="f80a9-592">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-592">String</span></span>      | <span data-ttu-id="f80a9-593">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-593">Bind</span></span>   | <span data-ttu-id="f80a9-594">\@.'\$Question'.text</span><span class="sxs-lookup"><span data-stu-id="f80a9-594">\@.'\$Question'.text</span></span> |
    | <span data-ttu-id="f80a9-595">Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="f80a9-595">Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="f80a9-596">قائمة السجلات</span><span class="sxs-lookup"><span data-stu-id="f80a9-596">Record list</span></span> | <span data-ttu-id="f80a9-597">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-597">Bind</span></span>   | <span data-ttu-id="f80a9-598">\@.'\$Question'.'\$Answer'</span><span class="sxs-lookup"><span data-stu-id="f80a9-598">\@.'\$Question'.'\$Answer'</span></span> |
    | <span data-ttu-id="f80a9-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="f80a9-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="f80a9-600">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-600">String</span></span>      | <span data-ttu-id="f80a9-601">تحرير</span><span class="sxs-lookup"><span data-stu-id="f80a9-601">Edit</span></span>   | <span data-ttu-id="f80a9-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="f80a9-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="f80a9-603">Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="f80a9-603">Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="f80a9-604">حقيقي</span><span class="sxs-lookup"><span data-stu-id="f80a9-604">Real</span></span>        | <span data-ttu-id="f80a9-605">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-605">Bind</span></span>   | <span data-ttu-id="f80a9-606">\@.point</span><span class="sxs-lookup"><span data-stu-id="f80a9-606">\@.point</span></span> |
    | <span data-ttu-id="f80a9-607">Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="f80a9-607">Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="f80a9-608">عدد صحيح</span><span class="sxs-lookup"><span data-stu-id="f80a9-608">Integer</span></span>     | <span data-ttu-id="f80a9-609">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-609">Bind</span></span>   | <span data-ttu-id="f80a9-610">\@.sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="f80a9-610">\@.sequenceNumber</span></span> |
    | <span data-ttu-id="f80a9-611">Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="f80a9-611">Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="f80a9-612">السلسلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-612">String</span></span>      | <span data-ttu-id="f80a9-613">ربط</span><span class="sxs-lookup"><span data-stu-id="f80a9-613">Bind</span></span>   | <span data-ttu-id="f80a9-614">\@.text</span><span class="sxs-lookup"><span data-stu-id="f80a9-614">\@.text</span></span> |

    <span data-ttu-id="f80a9-615">يبين الرسم التوضيحي التالي الحالة النهائية لتعيين النموذج الذي تم تكوينه على صفحة **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-615">The following illustration shows the final state of the configured model mapping on the **Model mapping designer** page.</span></span>

    ![تعيين نموذج مكوّن بشكل كامل في مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/er-quick-start1-mapping2.png)

7. <span data-ttu-id="f80a9-617">‏‏قم بحفظ التغييرات التي قمت بإجرائها.</span><span class="sxs-lookup"><span data-stu-id="f80a9-617">Save your changes.</span></span>
8. <span data-ttu-id="f80a9-618">أغلق صفحة **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-618">Close the **Model mapping designer** page.</span></span>

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a><span data-ttu-id="f80a9-619">إكمال تصميم تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="f80a9-619">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="f80a9-620">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-620">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f80a9-621">في صفحة **التكوينات**، في شجرة التكوين، حدد **تعيين الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-621">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="f80a9-622">في علامة التبويب السريعة **الإصدارات**، حدد إصدار التكوين بحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-622">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="f80a9-623">حدد **تغيير الحالة** \> **مكتمل‏‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-623">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="f80a9-624">تم تغيير حالة الإصدار 1.1 من هذا التكوين من **مسودة** إلى **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-624">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="f80a9-625">لم يعد من الممكن تغيير الإصدار 1.1.</span><span class="sxs-lookup"><span data-stu-id="f80a9-625">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="f80a9-626">يحتوي هذا الإصدار على تعيين النموذج الذي تم تكوينه ويمكن استخدامه كأساس لتكوينات إعداد التقارير الإلكترونية الأخرى.</span><span class="sxs-lookup"><span data-stu-id="f80a9-626">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="f80a9-627">تم إنشاء الإصدار 1.2 من هذا التكوين وهو بالحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-627">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="f80a9-628">يمكنك تحرير هذا الإصدار لتعديل تكوين **تعيين الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-628">You can edit this version to adjust the **Questionnaire mapping** configuration.</span></span>

![إصدارات تكوين تنسيق إعداد التقارير الإلكترونية في صفحة التكوينات](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> <span data-ttu-id="f80a9-630">يعد تعيين النموذج الذي تم تكوينه بمثابة تنفيذ خاص بتطبيق Finance لنموذج البيانات المجرد الذي يمثل مجال عمل **الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-630">The configured model mapping is your Finance-specific implementation of the abstract data model that represents the **Questionnaire** business domain.</span></span>

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a><span data-ttu-id="f80a9-631">تصميم قالب لتقرير مخصص</span><span class="sxs-lookup"><span data-stu-id="f80a9-631">Design a template for a custom report</span></span>

<span data-ttu-id="f80a9-632">يستخدم إطار عمل إعداد التقارير الإلكترونية قوالب معرّفة مسبقًا لإنشاء تقارير بتنسيقات Microsoft Office (مصنفات Excel أو مستندات Word).</span><span class="sxs-lookup"><span data-stu-id="f80a9-632">The ER framework uses predefined templates to generate reports in Microsoft Office formats (Excel workbooks or Word documents).</span></span> <span data-ttu-id="f80a9-633">بينما يتم إنشاء التقرير المطلوب، يتم ملء القالب بالبيانات المطلوبة وفقًا لتدفق البيانات الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="f80a9-633">While the required report is being generated, a template is filled in with required data according to the configured dataflow.</span></span> <span data-ttu-id="f80a9-634">وبالتالي، يجب أولاً تصميم قالب للتقرير المخصص.</span><span class="sxs-lookup"><span data-stu-id="f80a9-634">Therefore, you must first design a template for your custom report.</span></span> <span data-ttu-id="f80a9-635">يجب تصميم هذا القالب كمصنف Excel، ويمثل البنية التي تمثل تخطيط تقرير مخصص.</span><span class="sxs-lookup"><span data-stu-id="f80a9-635">This template must be designed as an Excel workbook, the structure of which represents the layout of a custom report.</span></span> <span data-ttu-id="f80a9-636">يجب عليك تسمية كل عنصر من عناصر Excel التي تخطط لتعبئتها بالبيانات المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-636">You must name every Excel item that you plan to fill in with required data.</span></span>

1. <span data-ttu-id="f80a9-637">قم بتنزيل الملف [Questionnaires report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx)، واحفظه في جهاز الكمبيوتر المحلي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-637">Download the [Questionnaires report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="f80a9-638">افتح الملف في Excel، وراجع بنية المصنف.</span><span class="sxs-lookup"><span data-stu-id="f80a9-638">Open the file in Excel, and review the structure of the workbook.</span></span>

<span data-ttu-id="f80a9-639">كما يوضح الرسم التوضيحي التالي، تم تصميم القالب الذي تم تنزيله لطباعة الاستبيانات المحددة التي تقدم أسئلة الاستبيان مع الإجابات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-639">As the following illustration shows, the downloaded template has been designed to print specified questionnaires that present a questionnaire's questions together with appropriate answers.</span></span>

![قالب Excel لطباعة الاستبيانات المحددة](./media/er-quick-start1-template-layout.png)

<span data-ttu-id="f80a9-641">تمت إضافة أسماء Excel إلى هذا القالب لملء تفاصيل الاستبيان.</span><span class="sxs-lookup"><span data-stu-id="f80a9-641">Excel names have been added to this template to fill in the questionnaire details.</span></span> <span data-ttu-id="f80a9-642">يمكنك استخدام إدارة الأسماء لمراجعه أسماء Excel.</span><span class="sxs-lookup"><span data-stu-id="f80a9-642">You can use Name Manager to review the Excel names.</span></span>

![استخدام إدارة الأسماء لمراجعة أسماء Excel في قالب Excel المتوفر](./media/er-quick-start1-template-names.png)

<span data-ttu-id="f80a9-644">تمت إضافة تسميات التقارير كنص ثابت باللغة الإنجليزية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-644">Report labels have been added as fixed text in the English language.</span></span> <span data-ttu-id="f80a9-645">يمكنك استبدال تسميات التقارير بأسماء Excel جديدة تقوم بملء التسميات بواسط نص يعتمد على اللغة باستخدام [تسميات](#AddMmLabels) تنسيقات التقارير الإلكتروني، كما فعلت بالتعبيرات التي تعتمد على اللغة في تعيين النموذج الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="f80a9-645">You can replace the report labels with new Excel names that fill in the labels with language-dependent text by using the ER format [labels](#AddMmLabels), as you did for language-dependent expressions in the configured model mapping.</span></span> <span data-ttu-id="f80a9-646">في هذه الحالة، يجب إضافة تسميات التقارير الإلكترونية في تنسيق التقارير الإلكترونية القابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="f80a9-646">In this case, ER labels must be added in the editable ER format.</span></span>

<span data-ttu-id="f80a9-647">كما يبين الشكل التوضيحي التالي، تم تعيين رأس التقرير المخصص لتمكين Excel من إجراء ترحيل الصفحات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-647">As the following illustration shows, the custom report header has been specified to enable Excel to do paging.</span></span>

![رأس التقرير المخصص في قالب Excel المتوفر](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a><span data-ttu-id="f80a9-649">تصميم تنسيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-649">Design a format</span></span>

<span data-ttu-id="f80a9-650">كمستخدم في دور المستشار الوظيفي للتقارير الإلكترونية، يجب عليك إنشاء تكوين تقارير إلكترونية جديد يحتوي على مكون [التنسيق](general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="f80a9-650">As a user in the Electronic Reporting Functional Consultant role, you must create a new ER configuration that contains a [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="f80a9-651">يجب تكوين مكون التنسيق لتحديد كيفية ملء قالب التقرير بالبيانات المطلوبة في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="f80a9-651">You must configure the format component to specify how a report template will be filled in with required data at runtime.</span></span>

<span data-ttu-id="f80a9-652">ومن خلال إكمال الخطوات الواردة في القسم [استيراد تكوين تنسيق مصمّم](#FormatImport)، يمكنك استيراد التنسيق المطلوب من ملف XML الذي تم توفيره.</span><span class="sxs-lookup"><span data-stu-id="f80a9-652">By completing the steps in the [Import a designed format configuration](#FormatImport) section, you can import the required format from the provided XML file.</span></span> <span data-ttu-id="f80a9-653">أو يمكنك إكمال الخطوات الواردة في القسم [إنشاء تكوين تنسيق جديد](#FormatCreate) لتصميم هذا التنسيق من البداية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-653">Alternatively, you can complete the steps in the [Create a new format configuration](#FormatCreate) section to design this format from scratch.</span></span>

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a><span data-ttu-id="f80a9-654">استيراد تكوين تنسيق مصمّم</span><span class="sxs-lookup"><span data-stu-id="f80a9-654">Import a designed format configuration</span></span>

1. <span data-ttu-id="f80a9-655">قم بتنزيل الملف [Questionnaires format.version.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) واحفظه في جهاز الكمبيوتر المحلي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-655">Download the [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="f80a9-656">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-656">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="f80a9-657">في مساحة عمل **إعداد التقارير الإلكترونية**، حدد **تكوينات إعداد التقارير**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-657">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="f80a9-658">في جزء الإجراءات، حدد **التبادل** \> **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-658">On the Action pane, Select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="f80a9-659">حدد **استعراض** ثم ابحث عن الملف **Questionnaires format.version.1.xml** وحدده.</span><span class="sxs-lookup"><span data-stu-id="f80a9-659">Select **Browse**, and then find and select the **Questionnaires format.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="f80a9-660">حدد **موافق** لاستيراد التكوين.</span><span class="sxs-lookup"><span data-stu-id="f80a9-660">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="f80a9-661">للمتابعة، انتقل إلى الاجراء التالي، [إنشاء تكوين تنسيق جديد](#FormatCreate).</span><span class="sxs-lookup"><span data-stu-id="f80a9-661">To continue, skip the next procedure, [Create a new format configuration](#FormatCreate).</span></span>

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a><span data-ttu-id="f80a9-662">قم بإنشاء تكوين تنسيق جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-662">Create a new format configuration</span></span>
 
1. <span data-ttu-id="f80a9-663">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-663">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f80a9-664">في صفحة **التكوينات**، في شجرة التكوين، حدد **نموذج الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-664">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="f80a9-665">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-665">Select **Create configuration**.</span></span>
4. <span data-ttu-id="f80a9-666">في مربع الحوار المنسدل، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f80a9-666">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="f80a9-667">في الحقل **جديد**، حدد **تنسيق يستند إلى استبيانات نموذج بيانات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-667">In the **New** field, select **Format based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="f80a9-668">في حقل **الاسم**، أدخل **تقرير الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-668">In the **Name** field, enter **Questionnaire report**.</span></span>
    3. <span data-ttu-id="f80a9-669">في الحقل **إصدار نموذج البيانات**، حدد **1**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-669">In the **Data model version** field, select **1**.</span></span>

        > [!NOTE]
        > - <span data-ttu-id="f80a9-670">إذا قمت بتحديد إصدار محدد من نموذج البيانات الأساسي، فستُقدم لك بنية الإصدار المقابل لنموذج البيانات كبنية مصدر بيانات **النموذج** بالتنسيق الذي يتم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="f80a9-670">If you select a specific version of the base data model, the structure of the corresponding version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span>
        > - <span data-ttu-id="f80a9-671">يمكنك ترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="f80a9-671">You can leave this field blank.</span></span> <span data-ttu-id="f80a9-672">في هذه الحالة، ستُقدم لك بنية إصدار **المسودة** لنموذج البيانات كبنية مصدر بيانات ‬‏‫**النموذج** بالتنسيق الذي يتم إنشاؤه.‬</span><span class="sxs-lookup"><span data-stu-id="f80a9-672">In that case, the structure of the **Draft** version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span> <span data-ttu-id="f80a9-673">يمكنك بعد ذلك تعديل النموذج ورؤية هذه التعديلات في التنسيق على الفور.</span><span class="sxs-lookup"><span data-stu-id="f80a9-673">You can then adjust your model and immediately see those adjustments in your format.</span></span> <span data-ttu-id="f80a9-674">وقد يؤدي هذا الأسلوب إلى تحسين فعالية تصميم حل إعداد التقارير الإلكترونية عند تكوين نموذج البيانات وتعيين النموذج والتنسيق في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="f80a9-674">This approach might improve the efficiency of ER solution design when you configure your data model, model mapping, and format simultaneously.</span></span>
        > - <span data-ttu-id="f80a9-675">إذا قمت بتحديد إصدار محدد من نموذج البيانات الأساسي، يمكنك التبديل إلى استخدام إصدار **المسودة** لاحقًا، عند بدء تحرير تنسيق.</span><span class="sxs-lookup"><span data-stu-id="f80a9-675">If you select a specific version of the base data model, you can switch to using the **Draft** version later, when you start to edit a format.</span></span>

    4. <span data-ttu-id="f80a9-676">في الحقل **تعريف نموذج البيانات**، حدد تعريف **الجذر**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-676">In the **Data model definition** field, select the **Root** definition.</span></span>

5. <span data-ttu-id="f80a9-677">حدد **إنشاء تكوين** لإنشاء التكوين.</span><span class="sxs-lookup"><span data-stu-id="f80a9-677">Select **Create configuration** to create the configuration.</span></span>

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a><span data-ttu-id="f80a9-678">استيراد قالب تقرير</span><span class="sxs-lookup"><span data-stu-id="f80a9-678">Import a report template</span></span>

1. <span data-ttu-id="f80a9-679">في صفحة **التكوينات**، في شجرة التكوين، حدد **تقرير الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-679">On the **Configurations** page, in the configuration tree, select **Questionnaire report**.</span></span>
2. <span data-ttu-id="f80a9-680">حدد **المصمم** لبدء تكوين تنسيق مخصص.</span><span class="sxs-lookup"><span data-stu-id="f80a9-680">Select **Designer** to start to configure a custom format.</span></span>
3. <span data-ttu-id="f80a9-681">في صفحة **مصمم التنسيق** في جزء الإجراءات، حدد **استيراد** \> **استيراد من Excel**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-681">On the **Format designer** page, on the Action Pane, select **Import** \> **Import from Excel**.</span></span>
4. <span data-ttu-id="f80a9-682">في مربع الحوار، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f80a9-682">In the dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="f80a9-683">حدد **إضافة قالب**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-683">Select **Add template**.</span></span>
    2. <span data-ttu-id="f80a9-684">ابحث عن الملف المحفوظ محليًا **Questionnaires report template.xslx** وحدده، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-684">Find and select the locally saved **Questionnaires report template.xslx** file, and then select **Open**.</span></span>
    3. <span data-ttu-id="f80a9-685">حدد **موافق** لاستيراد القالب.</span><span class="sxs-lookup"><span data-stu-id="f80a9-685">Select **OK** to import the template.</span></span>

    ![استيراد قالب تقرير](./media/er-quick-start1-template-import.png)

<span data-ttu-id="f80a9-687">يُضاف عنصر التنسيق **Excel\\File** بشكل تلقائي إلى التنسيق القابل للتحرير كعنصر جذر.</span><span class="sxs-lookup"><span data-stu-id="f80a9-687">The **Excel\\File** format element is automatically added to the editable format as a root element.</span></span> <span data-ttu-id="f80a9-688">علاوةً على ذلك، يُضاف عنصر تنسيق **Excel\\نطاق** أو عنصر تنسيق **Excel\\خلية** بشكل تلقائي لكل اسم Excel للقالب المستورد يتم التعرّف عليه.</span><span class="sxs-lookup"><span data-stu-id="f80a9-688">Additionally, either the **Excel\\Range** format element or the **Excel\\Cell** format element is automatically added for every recognized Excel name of the imported template.</span></span> <span data-ttu-id="f80a9-689">يُضاف تنسيق **Excel\\الرأس** الذي يتضمن عنصر **السلسلة** المتداخل بشكل تلقائي لعكس إعدادات الرأس للقالب المستورد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-689">The **Excel\\Header** format that has the nested **String** element is automatically added to reflect the header settings of the imported template.</span></span>

![تنسيق البنية الذي يتضمن العناصر المضافة تلقائيًا في مصمم عمليات التقارير الإلكترونية](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a><span data-ttu-id="f80a9-691">تكوين تنسيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-691">Configure a format</span></span>

1. <span data-ttu-id="f80a9-692">في الصفحة **مصمم التنسيق**، في شجرة التنسيق، حدد عنصر الجذر **Excel‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-692">On the **Format designer** page, in the format tree, select the **Excel** root element.</span></span>
2. <span data-ttu-id="f80a9-693">على علامة التبويب **تنسيق** على الجانب الأيسر من الصفحة، في حقل **الاسم**، أدخل <a name="AddFormatRootElement"></a>**تقرير**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-693">On the **Format** tab on the right side of the page, in the **Name** field, enter <a name="AddFormatRootElement"></a>**Report**.</span></span>
3. <span data-ttu-id="f80a9-694">في الحقل **تفضيلات اللغة**، حدد **تفضيلات المستخدم** لتشغيل التقرير بلغة المستخدم المفضلة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-694">In the **Language preference** field, select **User preference** to run the report in the user's preferred language.</span></span>
4. <span data-ttu-id="f80a9-695">في الحقل **تفضيلات الثقافة**، حدد **تفضيلات المستخدم** لتشغيل التقرير بثقافة المستخدم المفضلة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-695">In the **Culture preference** field, select **User preference** to run the report in the user's preferred culture.</span></span>

    <span data-ttu-id="f80a9-696">للحصول على معلومات حول كيفية تحديد سياقات اللغة والثقافة لعملية التقارير الإلكترونية، راجع [تصميم تقارير متعددة اللغات](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="f80a9-696">For information about how to specify the language and culture contexts for an ER process, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

    ![تكوين إعدادات اللغة والثقافة للتقرير المصمم في مصمم عمليات التقارير الإلكترونية](./media/er-quick-start1-template-format-structure1.png)

5. <span data-ttu-id="f80a9-698">في شجرة التنسيق، قم بتوسيع العقدة الجذر، ثم حدد **ResultsGroup**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-698">In the format tree, expand the root node, and then select **ResultsGroup**.</span></span>
6. <span data-ttu-id="f80a9-699">ضمن علامة التبويب **تنسيق**، في حقل **اتجاه النسخ المتماثل**، حدد **بلا نسخ متماثل**، لأنك لا تتوقع أن يكون لديك مجموعات نتائج متعددة لاستبيان واحد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-699">On the **Format** tab, in the **Replication direction** field, select **No replication**, because you don't expect to have multiple result groups for a single questionnaire.</span></span>

    ![تعريف اتجاه النسخ المتماثل لعناصر تنسيق النطاق في مصمم عمليات التقارير الإلكترونية](./media/er-quick-start1-template-format-structure2.png)

7. <span data-ttu-id="f80a9-701">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-701">Select **Save**.</span></span>

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a><span data-ttu-id="f80a9-702">تعريف ربط البيانات لعنوان التقرير</span><span class="sxs-lookup"><span data-stu-id="f80a9-702">Define the data binding for a report title</span></span>

<span data-ttu-id="f80a9-703">يجب تحديد ربط بيانات لعنصر التنسيق المستخدم لملء عنوان التقرير الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="f80a9-703">You must specify a data binding for a format element that is used to fill in the title of a generated report.</span></span>

1. <span data-ttu-id="f80a9-704">في صفحة **مصمم التنسيق**، على علامة تبويب **التعيين** إلى اليسار، حدد العنصر **التقرير\\عنوان التقرير**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-704">On the **Format designer** page, on the **Mapping** tab on the right, select the **Report\\ReportTitle** element.</span></span>
2. <span data-ttu-id="f80a9-705">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-705">Select **Edit formula**.</span></span>
3. <span data-ttu-id="f80a9-706">في محرر المعادلة، حدد **ترجمة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-706">In the formula editor, select **Translate**.</span></span>
4. <span data-ttu-id="f80a9-707">في مربع الحوار **نص الترجمة**، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f80a9-707">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="f80a9-708">في حقل **معرف التسمية**، أدخل **عنوان التقرير**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-708">In the **Label ID** field, enter **ReportTitle**.</span></span>
    2. <span data-ttu-id="f80a9-709">في حقل **النص باللغة الافتراضية**، أدخل **تقرير الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-709">In the **Text in default language** field, enter **Questionnaires report**.</span></span>
    3. <span data-ttu-id="f80a9-710">حدد **ترجمة**، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-710">Select **Translate**, and then select **Save**.</span></span>
    4. <span data-ttu-id="f80a9-711">حدد **ترجمة** لإغلاق مربع الحوار **ترجمة النص**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-711">Select **Translate** to close the **Text translation** dialog box.</span></span>

5. <span data-ttu-id="f80a9-712">أغلق محرر المعادلة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-712">Close the formula editor.</span></span>

    ![تكوين الربط لملء العنوان في تقرير منشأ](./media/er-quick-start1-add-report-title-label.png)

<span data-ttu-id="f80a9-714">يمكنك استخدام هذا الأسلوب لجعل كافة التسميات الأخرى للقالب الحالي تعتمد على اللغة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-714">You can use this technique to make all other labels of the current template language-dependent.</span></span> <span data-ttu-id="f80a9-715">لمزيد من المعلومات حول كيفية ترجمة التسميات المضافة لتكوين تقارير إلكترونية واحد إلى كافة اللغات المدعومة، راجع [تصميم تقارير متعددة اللغات](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="f80a9-715">For information about how the added labels of a single ER configuration can be translated into all supported languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a><span data-ttu-id="f80a9-716">مراجعة مصدر بيانات النموذج</span><span class="sxs-lookup"><span data-stu-id="f80a9-716">Review model data source</span></span>

1. <span data-ttu-id="f80a9-717">في صفحة **مصمم التنسيق**، على علامة تبويب **التعيين**، حدد مصدر بيانات <a name="ModelDSName"></a>**النموذج** الذي يمثل نموذج البيانات الأساسي لتنسيق التقارير الإلكترونية هذا.</span><span class="sxs-lookup"><span data-stu-id="f80a9-717">On the **Format designer** page, on the **Mapping** tab, select the <a name="ModelDSName"></a>**model** data source that represents the base data model of this ER format.</span></span>
2. <span data-ttu-id="f80a9-718">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-718">Select **Edit**.</span></span>
3. <span data-ttu-id="f80a9-719">راجع المعلومات الموجودة في مربع الحوار **خصائص مصدر البيانات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-719">Review the information in the **Data source properties** dialog box.</span></span> <span data-ttu-id="f80a9-720">ويمثل مصدر البيانات هذا الإصدار 1 من مكون نموذج البيانات **الاستبيانات** في تكوين التقارير الإلكترونية **نموذج الاستبيانات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-720">This data source represents version 1 of the **Questionnaires** data model component that resides in the **Questionnaires model** ER configuration.</span></span>

![خصائص مصدر بيانات النموذج في مصمم عمليات التقارير الإلكترونية](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a><span data-ttu-id="f80a9-722">ربط عناصر التنسيق بحقول مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-722">Bind format elements to data source fields</span></span>

<span data-ttu-id="f80a9-723">لتحديد كيفية ملء قالب في وقت التشغيل، يجب أن تقوم بربط كل عنصر تنسيق مقترن باسم Excel مناسب بحقل واحد في مصدر بيانات التنسيق هذا.</span><span class="sxs-lookup"><span data-stu-id="f80a9-723">To specify how a template is filled in at runtime, you must bind every format element that is associated with an appropriate Excel name to a single field of this format's data source.</span></span>

1. <span data-ttu-id="f80a9-724">في الصفحة **مصمم التنسيق** في شجرة التنسيق، حدد عنصر التنسيق **التقرير\\اسم الشركة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-724">On the **Format designer** page, in the format tree, select the **Report\\CompanyName** format element.</span></span>
2. <span data-ttu-id="f80a9-725">على علامة تبويب **التعيين**، حدد حقل مصدر البيانات **model.CompanyName** لنوع **السلسلة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-725">On the **Mapping** tab, select the **model.CompanyName** data source field of the **String** type.</span></span>
3. <span data-ttu-id="f80a9-726">حدد **ربط** لإدخال اسم شركة في قالب.</span><span class="sxs-lookup"><span data-stu-id="f80a9-726">Select **Bind** to enter a company name in a template.</span></span>
4. <span data-ttu-id="f80a9-727">في شجرة التنسيق، حدد العنصر **التقرير\\الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-727">In the format tree, select the **Report\\Questionnaire** element.</span></span>
5. <span data-ttu-id="f80a9-728">على علامة تبويب **التنسيق**، حدد حقل مصدر البيانات **model.Questionnaire** لنوع **قائمة السجلات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-728">On the **Mapping** tab, select the **model.Questionnaire** data source field of the **Record list** type.</span></span>
6. <span data-ttu-id="f80a9-729">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-729">Select **Bind**.</span></span>
7. <span data-ttu-id="f80a9-730">حدد **إظهار التفاصيل** لعرض مزيد من التفاصيل لتنسيق العناصر.</span><span class="sxs-lookup"><span data-stu-id="f80a9-730">Select **Show details** to see more details for format elements.</span></span>

    <span data-ttu-id="f80a9-731">يتم تكوين تنسيق نطاق **الاستبيان‏‎** كمنسوخ عموديًا.</span><span class="sxs-lookup"><span data-stu-id="f80a9-731">The **Questionnaire** range format element is configured as vertically replicated.</span></span> <span data-ttu-id="f80a9-732">عند ربطه بمصدر بيانات من النوع **قائمة السجلات**، يتم تكرار نطاق **الاستبيان** المناسب لقالب Excel لكل سجل من سجلات مصدر البيانات المرتبط.</span><span class="sxs-lookup"><span data-stu-id="f80a9-732">When it's bound to a data source of the **Record list** type, the appropriate **Questionnaire** range of the Excel template is repeated for every record of the bound data source.</span></span>
 
    ![ربط عنصر تنسيق نطاق الاستبيان إلى مصادر بيانات قائمة السجلات المناسبة في مصمم عمليات التقارير الإلكترونية](./media/er-quick-start1-bindings1.png)

    <span data-ttu-id="f80a9-734">بسبب تحديد نطاق **الاستبيان** لقالب Excel بين الصفوف من 5 إلى 14، يتم تكرار هذه الصفوف لكل استبيان تم الإبلاغ عنه.</span><span class="sxs-lookup"><span data-stu-id="f80a9-734">Because the **Questionnaire** range of the Excel template is defined between rows 5 through 14, these rows are repeated for every reported questionnaire.</span></span>

    ![صفوف في قالب Excel سيتم تكرارها في تقرير يتم إنشاؤه لكل سجل من مصادر بيانات قائمة السجلات](./media/er-quick-start1-template-questionnaire-range.png)

8. <span data-ttu-id="f80a9-736">قم بتكوين روابط مماثلة لعناصر التنسيق المتبقية، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-736">Configure similar bindings for the remaining format elements, as described in the following table.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f80a9-737">في هذا الجدول، تفترض المعلومات الموجودة في العمود "مسار مصدر البيانات" أن ميزة [المسار النسبي](relative-path-data-bindings-er-models-format.md)لإعداد التقارير الإلكترونية هي قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="f80a9-737">In this table, the information in the "Data source path" column assumes that the [relative path](relative-path-data-bindings-er-models-format.md) ER feature is turned on.</span></span>

    | <span data-ttu-id="f80a9-738">مسار عنصر التنسيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-738">Format element path</span></span>                                      | <span data-ttu-id="f80a9-739">مسار مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-739">Data source path</span></span> |
    |----------------------------------------------------------|------------------|
    | <span data-ttu-id="f80a9-740">Excel\\عنوان التقرير</span><span class="sxs-lookup"><span data-stu-id="f80a9-740">Excel\\ReportTitle</span></span>                                       | <span data-ttu-id="f80a9-741">**\@"GER\_LABEL:ReportTitle"**</span><span class="sxs-lookup"><span data-stu-id="f80a9-741">**\@"GER\_LABEL:ReportTitle"**</span></span> |
    | <span data-ttu-id="f80a9-742">Excel\\اسم الشركة</span><span class="sxs-lookup"><span data-stu-id="f80a9-742">Excel\\CompanyName</span></span>                                       | <span data-ttu-id="f80a9-743">**model.CompanyName**</span><span class="sxs-lookup"><span data-stu-id="f80a9-743">**model.CompanyName**</span></span> |
    | <span data-ttu-id="f80a9-744">Excel\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="f80a9-744">Excel\\Questionnaire</span></span>                                     | <span data-ttu-id="f80a9-745">**model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="f80a9-745">**model.Questionnaire**</span></span> |
    | <span data-ttu-id="f80a9-746">Excel\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="f80a9-746">Excel\\Questionnaire\\Active</span></span>                             | <span data-ttu-id="f80a9-747">**\@.Active**، حيث **\@** هو **model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="f80a9-747">**\@.Active**, where **\@** is **model.Questionnaire**</span></span> |
    | <span data-ttu-id="f80a9-748">Excel\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="f80a9-748">Excel\\Questionnaire\\Code</span></span>                               | <span data-ttu-id="f80a9-749">**\@.Code**</span><span class="sxs-lookup"><span data-stu-id="f80a9-749">**\@.Code**</span></span> |
    | <span data-ttu-id="f80a9-750">Excel\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="f80a9-750">Excel\\Questionnaire\\Description</span></span>                        | <span data-ttu-id="f80a9-751">**\@.Description**</span><span class="sxs-lookup"><span data-stu-id="f80a9-751">**\@.Description**</span></span> |
    | <span data-ttu-id="f80a9-752">Excel\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="f80a9-752">Excel\\Questionnaire\\QuestionnaireType</span></span>                  | <span data-ttu-id="f80a9-753">**\@.QuestionnaireType**</span><span class="sxs-lookup"><span data-stu-id="f80a9-753">**\@.QuestionnaireType**</span></span> |
    | <span data-ttu-id="f80a9-754">Excel\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="f80a9-754">Excel\\Questionnaire\\QuestionOrder</span></span>                      | <span data-ttu-id="f80a9-755">**\@.QuestionOrder**</span><span class="sxs-lookup"><span data-stu-id="f80a9-755">**\@.QuestionOrder**</span></span> |
    | <span data-ttu-id="f80a9-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span><span class="sxs-lookup"><span data-stu-id="f80a9-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span></span>               | <span data-ttu-id="f80a9-757">**\@.ResultsGroup.Code**</span><span class="sxs-lookup"><span data-stu-id="f80a9-757">**\@.ResultsGroup.Code**</span></span> |
    | <span data-ttu-id="f80a9-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span><span class="sxs-lookup"><span data-stu-id="f80a9-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span></span>        | <span data-ttu-id="f80a9-759">**\@.ResultsGroup.Description**</span><span class="sxs-lookup"><span data-stu-id="f80a9-759">**\@.ResultsGroup.Description**</span></span> |
    | <span data-ttu-id="f80a9-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="f80a9-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>    | <span data-ttu-id="f80a9-761">**\@.ResultsGroup.MaxNumberOfPoint**</span><span class="sxs-lookup"><span data-stu-id="f80a9-761">**\@.ResultsGroup.MaxNumberOfPoint**</span></span> |
    | <span data-ttu-id="f80a9-762">Excel\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="f80a9-762">Excel\\Questionnaire\\Question</span></span>                           | <span data-ttu-id="f80a9-763">**\@.Question**</span><span class="sxs-lookup"><span data-stu-id="f80a9-763">**\@.Question**</span></span> |
    | <span data-ttu-id="f80a9-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="f80a9-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span></span> | <span data-ttu-id="f80a9-765">**\@.CollectionSequenceNumber**، حيث **\@** هو **model.Questionnaire.Question**</span><span class="sxs-lookup"><span data-stu-id="f80a9-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span></span> |
    | <span data-ttu-id="f80a9-766">Excel\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="f80a9-766">Excel\\Questionnaire\\Question\\Id</span></span>                       | <span data-ttu-id="f80a9-767">**\@.Id**</span><span class="sxs-lookup"><span data-stu-id="f80a9-767">**\@.Id**</span></span> |
    | <span data-ttu-id="f80a9-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="f80a9-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span></span>          | <span data-ttu-id="f80a9-769">**\@.MustBeCompleted**</span><span class="sxs-lookup"><span data-stu-id="f80a9-769">**\@.MustBeCompleted**</span></span> |
    | <span data-ttu-id="f80a9-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="f80a9-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span></span>          | <span data-ttu-id="f80a9-771">**\@.PrimaryQuestion**</span><span class="sxs-lookup"><span data-stu-id="f80a9-771">**\@.PrimaryQuestion**</span></span> |
    | <span data-ttu-id="f80a9-772">Excel\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="f80a9-772">Excel\\Questionnaire\\Question\\SequenceNumber</span></span>           | <span data-ttu-id="f80a9-773">**\@.SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="f80a9-773">**\@.SequenceNumber**</span></span> |
    | <span data-ttu-id="f80a9-774">Excel\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="f80a9-774">Excel\\Questionnaire\\Question\\Text</span></span>                     | <span data-ttu-id="f80a9-775">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="f80a9-775">**\@.Text**</span></span> |
    | <span data-ttu-id="f80a9-776">Excel\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="f80a9-776">Excel\\Questionnaire\\Question\\Answer</span></span>                   | <span data-ttu-id="f80a9-777">**\@.Answer**</span><span class="sxs-lookup"><span data-stu-id="f80a9-777">**\@.Answer**</span></span> |
    | <span data-ttu-id="f80a9-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="f80a9-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>    | <span data-ttu-id="f80a9-779">**\@.CorrectAnswer**، حيث **\@** هو **model.Questionnaire.Answer**</span><span class="sxs-lookup"><span data-stu-id="f80a9-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span></span> |
    | <span data-ttu-id="f80a9-780">Excel\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="f80a9-780">Excel\\Questionnaire\\Question\\Answer\\Points</span></span>           | <span data-ttu-id="f80a9-781">**\@.Points**</span><span class="sxs-lookup"><span data-stu-id="f80a9-781">**\@.Points**</span></span> |
    | <span data-ttu-id="f80a9-782">Excel\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="f80a9-782">Excel\\Questionnaire\\Question\\Answer\\Text</span></span>             | <span data-ttu-id="f80a9-783">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="f80a9-783">**\@.Text**</span></span> |

9. <span data-ttu-id="f80a9-784">عند الانتهاء، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-784">When you've finished, select **Save**.</span></span>

<span data-ttu-id="f80a9-785">يبين الرسم التوضيحي التالي الحالة النهائية لروابط البيانات المكوّنة في صفحة **مصمم التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-785">The following illustration shows the final state of the configured data bindings on the **Format designer** page.</span></span>

![روابط البيانات المكوّنة في مصمم عمليات التقارير الإلكترونية](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> <span data-ttu-id="f80a9-787">تمثل المجموعة الكاملة من مصادر البيانات والروابط المحدد مكون تعيين التنسيق للتنسيق المكوّن.</span><span class="sxs-lookup"><span data-stu-id="f80a9-787">The whole collection of specified data sources and bindings represents a format mapping component of the configured format.</span></span> <span data-ttu-id="f80a9-788">يتم استدعاء تعيين التنسيق هذا عند تشغيل التنسيق المكوّن لإنشاء التقارير.</span><span class="sxs-lookup"><span data-stu-id="f80a9-788">This format mapping is called when you run the configured format for report generation.</span></span>

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a><span data-ttu-id="f80a9-789">تشغيل تنسيق مصمّم من التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f80a9-789">Run a designed format from ER</span></span>

<span data-ttu-id="f80a9-790">يمكنك الآن تشغيل تنسيق مصمّم لأغراض الاختبار من صفحة **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-790">You can now run a designed format for testing purposes from the **Configurations** page.</span></span>

1. <span data-ttu-id="f80a9-791">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-791">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f80a9-792">في صفحة **التكوين**، في شجرة التكوين، وسَّع **نموذج الاستبيان**، ثم حدد **تقرير الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-792">On the **Configuration** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="f80a9-793">حدد **المصمم** لإصدار التنسيق بحالة **المسودة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-793">Select **Designer** for the format version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="f80a9-794">في صفحة **مصمم التنسيق**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-794">On the **Format designer** page, select **Run**.</span></span>
5. <span data-ttu-id="f80a9-795">في مربع الحوار **معلمات التقارير الإلكترونية‬**، على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**، قم بتكوين خيار التصفية بحيث يتم تضمين الاستبيان **SBCCrsExam** فقط,</span><span class="sxs-lookup"><span data-stu-id="f80a9-795">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
6. <span data-ttu-id="f80a9-796">حدد **موافق** لتأكيد خيار التصفية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-796">Select **OK** to confirm the filtering option.</span></span>
7. <span data-ttu-id="f80a9-797">حدد **موافق** لتشغيل التقرير.</span><span class="sxs-lookup"><span data-stu-id="f80a9-797">Select **OK** to run the report.</span></span>
8. <span data-ttu-id="f80a9-798">راجع التقرير المُنشأ.</span><span class="sxs-lookup"><span data-stu-id="f80a9-798">Review the generated report.</span></span>

<span data-ttu-id="f80a9-799">بشكل [افتراضي](electronic-reporting-destinations.md#default-behavior)، يتم تسليم تقرير مُنشأ كملف Excel يمكنك تنزيله.</span><span class="sxs-lookup"><span data-stu-id="f80a9-799">By [default](electronic-reporting-destinations.md#default-behavior), a generated report is delivered as an Excel file that you can download.</span></span> <span data-ttu-id="f80a9-800">تظهر الأشكال التوضيحية التالية صفحتين للتقرير الذي تم إنشاؤه بتنسيق Excel.</span><span class="sxs-lookup"><span data-stu-id="f80a9-800">The following illustrations show two pages of the generated report in Excel format.</span></span>

![مثال لتقرير تم إنشاؤه بتنسيق Excel، الصفحة رقم 1](./media/er-quick-start1-report1a.png)

![مثال لتقرير تم إنشاؤه بتنسيق Excel، الصفحة رقم 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a><span data-ttu-id="f80a9-803">ضبط تنسيق مصمّم</span><span class="sxs-lookup"><span data-stu-id="f80a9-803">Tune a designed format</span></span>

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a><span data-ttu-id="f80a9-804">تعديل تنسيق لتغيير اسم مستند تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="f80a9-804">Modify a format to change the name of a generated document</span></span>

<span data-ttu-id="f80a9-805">بشكل افتراضي، تتم تسمية مستند تم إنشاؤه باستخدام الاسم المستعار للمستخدم الحالي.</span><span class="sxs-lookup"><span data-stu-id="f80a9-805">By default, a generated document is named by using the alias of the current user.</span></span> <span data-ttu-id="f80a9-806">ومن خلال تعديل التنسيق، يمكنك تغيير هذا السلوك بحيث تتم تسمية مستند تم إنشاؤه استنادًا إلى المنطق المخصص.</span><span class="sxs-lookup"><span data-stu-id="f80a9-806">By modifying the format, you can change this behavior so that a generated document is named based on your custom logic.</span></span> <span data-ttu-id="f80a9-807">على سبيل المثال، يمكنك إسناد مستند مُنشـأ إلى تاريخ ووقت جلسة العمل الحالية وإلى عنوان التقرير.</span><span class="sxs-lookup"><span data-stu-id="f80a9-807">For example, the name of a generated document can be based on the current session date and time, and on the report's title.</span></span>

1. <span data-ttu-id="f80a9-808">في الصفحة **مصمم التنسيق**، حدد عنصر الجذر **التقرير**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-808">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="f80a9-809">في علامة التبويب **التعيين**، حدد **تحرير اسم الملف**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-809">On the **Mapping** tab, select **Edit file name**.</span></span>
3. <span data-ttu-id="f80a9-810">في حقل **المعادلة**، أدخل **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-810">In the **Formula** field, enter **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span></span>
4. <span data-ttu-id="f80a9-811">حدد **حفظ** ثم قم بإغلاق محرر المعادلات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-811">Select **Save**, and close the formula editor.</span></span>
5. <span data-ttu-id="f80a9-812">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-812">Select **Save**.</span></span>

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a><span data-ttu-id="f80a9-813">تعديل تنسيق لتغيير ترتيب الأسئلة</span><span class="sxs-lookup"><span data-stu-id="f80a9-813">Modify a format to change the order of questions</span></span>

<span data-ttu-id="f80a9-814">لا يتم ترتيب الأسئلة بشكل صحيح في تقرير تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="f80a9-814">The questions aren't correctly ordered in a generated report.</span></span> <span data-ttu-id="f80a9-815">يمكنك تغيير الترتيب عن طريق تعديل التنسيق.</span><span class="sxs-lookup"><span data-stu-id="f80a9-815">You can change the order by modifying the format.</span></span>

1. <span data-ttu-id="f80a9-816">في الصفحة **مصمم التنسيق**، حدد عنصر الجذر **التقرير**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-816">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="f80a9-817">على علامة التبويب **التعيين** في شجرة التنسيق، وسّع **التقرير\\الاستبيان\\السؤال**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-817">On the **Mapping** tab, in the format tree, expand **Report\\Questionnaire\\Question**.</span></span>

    ![عنصر تنسيق السؤال لنوع النطاق في مصمم عمليات التقارير الإلكترونية](./media/er-quick-start1-bindings3.png)

3. <span data-ttu-id="f80a9-819">في علامة التبويب **التعيين**، حدد **model.Questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-819">On the **Mapping** tab, select **model.Questionnaire**.</span></span>
4. <span data-ttu-id="f80a9-820">حدد **إضافة** \> **Functions\\Calculated field**، ثم في حقل **الاسم**، أدخل **OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-820">Select **Add** \> **Functions\\Calculated field**, and then, in the **Name** field, enter **OrderedQuestions**.</span></span>
5. <span data-ttu-id="f80a9-821">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-821">Select **Edit formula**.</span></span>
6. <span data-ttu-id="f80a9-822">في محرر المعادلات، في حقل **المعادلة**، أدخل **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** لترتيب قائمة أسئلة الاستبيان الحالي بواسطة رقم ترتيب التسلسل.</span><span class="sxs-lookup"><span data-stu-id="f80a9-822">In the formula editor, in the **Formula** field, enter **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** to order the list of questions of the current questionnaire by the sequence order number.</span></span>
7. <span data-ttu-id="f80a9-823">حدد **حفظ** ثم قم بإغلاق محرر المعادلات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-823">Select **Save**, and close the formula editor.</span></span>
8. <span data-ttu-id="f80a9-824">حدد **موافق** لإكمال إدخال حقل محسوب جديد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-824">Select **OK** to complete the entry of a new calculated field.</span></span>
9. <span data-ttu-id="f80a9-825">في علامة التبويب **التعيين**، حدد **model.Questionnaire.OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-825">On the **Mapping** tab, select **model.Questionnaire.OrderedQuestions**.</span></span>
10. <span data-ttu-id="f80a9-826">في شجرة التنسيق، حدد **Excel\\Questionnaire\\Question**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-826">In the format tree, select **Excel\\Questionnaire\\Question**.</span></span>
11. <span data-ttu-id="f80a9-827">حدد **ربط**، ثم أكد أن مسار **model.Questionnaire.Questions** الحالي تم استبداله بمسار **model.Questionnaire.OrderedQuestions** الجديد في جميع روابط العناصر المتداخلة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-827">Select **Bind**, and then confirm that the current **model.Questionnaire.Questions** path is replaced by the new **model.Questionnaire.OrderedQuestions** path in all bindings of nested elements.</span></span>
12. <span data-ttu-id="f80a9-828">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-828">Select **Save**.</span></span>

![ربط عنصر تنسيق السؤال بمصدر بيانات OrderedQuestions الذي تم تكوينه في مصمم عمليات التقارير الإلكترونية](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a><span data-ttu-id="f80a9-830">تشغيل تنسيق معدّل من التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f80a9-830">Run a modified format from ER</span></span>

<span data-ttu-id="f80a9-831">يمكنك الآن تشغيل تنسيق معدل لأغراض الاختبار من إطار عمل إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-831">You can now run a modified format for testing purposes from the ER framework.</span></span>

1. <span data-ttu-id="f80a9-832">في صفحة **مصمم التنسيق**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-832">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="f80a9-833">في مربع الحوار **معلمات التقارير الإلكترونية‬**، على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**، قم بتكوين خيار التصفية بحيث يتم تضمين الاستبيان **SBCCrsExam** فقط,</span><span class="sxs-lookup"><span data-stu-id="f80a9-833">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
3. <span data-ttu-id="f80a9-834">حدد **موافق** لتأكيد خيار التصفية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-834">Select **OK** to confirm the filtering option.</span></span>
4. <span data-ttu-id="f80a9-835">حدد **موافق** لتشغيل التقرير.</span><span class="sxs-lookup"><span data-stu-id="f80a9-835">Select **OK** to run the report.</span></span>
5. <span data-ttu-id="f80a9-836">راجع التقرير المُنشأ.</span><span class="sxs-lookup"><span data-stu-id="f80a9-836">Review the generated report.</span></span>

<span data-ttu-id="f80a9-837">يوضح الرسم التوضيحي التالي التقرير الذي تم إنشاؤه بتنسيق Excel حيث يتم ترتيب الأسئلة بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="f80a9-837">The following illustration shows a generated report in Excel format where the questions are correctly ordered.</span></span>

![تقرير مُنشأ بتنسيق Excel يحتوي على أسئلة تم ترتيبها بشكل صحيح](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a><span data-ttu-id="f80a9-839">إكمال تصميم التنسيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-839">Complete the format design</span></span>

1. <span data-ttu-id="f80a9-840">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-840">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f80a9-841">في صفحة **التكوينات**، في شجرة التكوين، وسَّع **نموذج الاستبيان**، ثم حدد **تقرير الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-841">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="f80a9-842">في علامة التبويب السريعة **الإصدارات**، حدد إصدار التكوين بحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-842">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="f80a9-843">حدد **تغيير الحالة** \> **مكتمل‏‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-843">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="f80a9-844">تم تغيير حالة الإصدار 1.1 من هذا التكوين من **مسودة** إلى **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-844">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="f80a9-845">لم يعد من الممكن تغيير الإصدار 1.1.</span><span class="sxs-lookup"><span data-stu-id="f80a9-845">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="f80a9-846">يحتوي هذا الإصدار على التنسيق المكوّن ويمكن استخدامه لطباعة التقرير المخصص.</span><span class="sxs-lookup"><span data-stu-id="f80a9-846">This version contains the configured format and can be used to print your custom report.</span></span> <span data-ttu-id="f80a9-847">تم إنشاء الإصدار 1.2 من هذا التكوين وهو بالحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-847">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="f80a9-848">يمكنك تحرير هذا الإصدار لتعديل تنسيق تقرير **الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-848">You can edit this version to adjust the format of your **Questionnaire** report.</span></span>

![تكوين إعداد التقارير الإلكترونية القابلة للتعديل في صفحة التكوينات](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> <span data-ttu-id="f80a9-850">التنسيق المكوّن هو تصميم تقرير **الاستبيان** ولا يحتوي علي أي علاقات ببيانات اصطناعية خاصة بـ Finance.</span><span class="sxs-lookup"><span data-stu-id="f80a9-850">The configured format is your design of the **Questionnaire** report and contains no relations to the Finance-specific artefacts.</span></span>

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a><span data-ttu-id="f80a9-851">تطوير بيانات اصطناعية للتطبيق لاستدعاء التقرير المصمّم</span><span class="sxs-lookup"><span data-stu-id="f80a9-851">Develop application artefacts to call the designed report</span></span>

<span data-ttu-id="f80a9-852">كمستخدم لديه دور مسؤول النظام، يجب تطوير منطق جديد بحيث يمكن استدعاء التنسيق المكوّن للتقارير الإلكترونية من واجهة مستخدم التطبيق (UI) لإنشاء التقرير المخصص.</span><span class="sxs-lookup"><span data-stu-id="f80a9-852">As a user in the System Administrator role, you must develop new logic so that the configured ER format can be called from the application user interface (UI) to generate your custom report.</span></span> <span data-ttu-id="f80a9-853">في الوقت الحالي، لا تقدم التقارير الإلكترونية أي إمكانية لتكوين نوع المنطق هذا.</span><span class="sxs-lookup"><span data-stu-id="f80a9-853">Currently, ER doesn't offer any capability for configuring this type of logic.</span></span> <span data-ttu-id="f80a9-854">وبالتالي، هناك بعض الأعمال الهندسية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-854">Therefore, some engineering work is required.</span></span> 

<span data-ttu-id="f80a9-855">لتطوير المنطق الجديد، يجب نشر مخطط يدعم البناء المستمر.</span><span class="sxs-lookup"><span data-stu-id="f80a9-855">To develop the new logic, you must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="f80a9-856">لمزيد من المعلومات ، راجع [نشر مخططات تدعم البناء المستمر والتنفيذ التلقائي للاختبار‬ات](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="f80a9-856">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="f80a9-857">يجب أن يكون لديك أيضًأ حق الوصول إلى بيئة التطوير لهذا المخطط.</span><span class="sxs-lookup"><span data-stu-id="f80a9-857">You must also have access to the development environment for this topology.</span></span> <span data-ttu-id="f80a9-858">لمزيد من المعلومات حول واجهة API للتقارير الإلكترونية، راجع [واجهة API لإطار عمل إعداد التقارير الإلكترونية](er-apis-app73.md).</span><span class="sxs-lookup"><span data-stu-id="f80a9-858">For more information about the available ER API, see [ER framework API](er-apis-app73.md).</span></span>

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a><span data-ttu-id="f80a9-859">تعديل التعليمات البرمجية المصدر</span><span class="sxs-lookup"><span data-stu-id="f80a9-859">Modify source code</span></span>

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a><span data-ttu-id="f80a9-860">إضافة فئة عقد بيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-860">Add a data contract class</span></span>

<span data-ttu-id="f80a9-861">أضف الفئة الجديدة **QuestionnairesErReportContract** إلى مشروع Microsoft Visual Studio، واكتب التعليمات البرمجية التي تحدد عقد البيانات الذي يجب استخدامه لتشغيل تنسيق التقارير الإلكترونية المكوّن.</span><span class="sxs-lookup"><span data-stu-id="f80a9-861">Add the new **QuestionnairesErReportContract** class to your Microsoft Visual Studio project, and write code that specifies the data contract that should be used to run the configured ER format.</span></span>

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a><span data-ttu-id="f80a9-862">إضافة فئة منشئ واجهة المستخدم</span><span class="sxs-lookup"><span data-stu-id="f80a9-862">Add a UI builder class</span></span>

<span data-ttu-id="f80a9-863">أضف الفئة الجديدة **QuestionnairesErReportUIBuilder** إلى مشروع Visual Studio، واكتب التعليمات البرمجية لإنشاء مربع حوار وقت التشغيل الذي سيتم استخدامه للبحث عن معرف تعين التنسيق لتنسيق التقارير الإلكترونية الذي يجب تشغيله.</span><span class="sxs-lookup"><span data-stu-id="f80a9-863">Add the new **QuestionnairesErReportUIBuilder** class to your Visual Studio project, and write code to generate a runtime dialog box that will be used to look up the format mapping ID of the ER format that must be run.</span></span> <span data-ttu-id="f80a9-864">التعليمات البرمجية المتوفرة تبحث فقط عن تنسيقات التقارير الإلكترونية التي تحتوي على مصدر بيانات من النوع **نموذج البيانات** الذي يشير إلى نموذج البيانات **[الاستبيانات](#DataModeName)** باستخدام تعريف **[الجذر](#RootDefinitionName)**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-864">The provided code looks up only ER formats that contain a data source of the **Data model** type that refers to the **[Questionnaires](#DataModeName)** data model by using the **[Root](#RootDefinitionName)** definition.</span></span>

> [!NOTE]
> <span data-ttu-id="f80a9-865">بدلاً من ذلك، يمكنك استخدام نقاط تكامل التقارير الإلكترونية لتصفية تنسيقات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-865">Alternatively, you can use ER integration points to filter ER formats.</span></span> <span data-ttu-id="f80a9-866">لمزيد من المعلومات، راجع [واجهة API لإظهار بحث تعيين التنسيق](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span><span class="sxs-lookup"><span data-stu-id="f80a9-866">For more information, see [API to show a format mapping lookup](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span></span>

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a><span data-ttu-id="f80a9-867">إضافة فئة موفر بيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-867">Add a data provider class</span></span>

<span data-ttu-id="f80a9-868">أضف الفئة الجديدة **QuestionnairesErReportDP** إلى مشروع Visual Studio، واكتب التعليمات البرمجية التي تقدم موفر البيانات الذي يجب استخدامه لتشغيل تنسيق التقارير الإلكترونية المكوّن.</span><span class="sxs-lookup"><span data-stu-id="f80a9-868">Add the new **QuestionnairesErReportDP** class to your Visual Studio project, and write code that introduces the data provider that should used to run the configured ER format.</span></span> <span data-ttu-id="f80a9-869">تشتمل التعليمات البرمجية المتوفرة علي عقد البيانات الخاص بموفر البيانات هذا فقط.</span><span class="sxs-lookup"><span data-stu-id="f80a9-869">The provided code includes only the data contract for this data provider.</span></span>

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a><span data-ttu-id="f80a9-870">إضافة ملف تسميات</span><span class="sxs-lookup"><span data-stu-id="f80a9-870">Add a labels file</span></span>

<span data-ttu-id="f80a9-871">أضف ملف التسميات الجديد **QuestionnairesErReportLabels\_en-US** إلى مشروع Visual Studio، وحدد التسميات التالية لموارد واجهة المستخدم التالية:</span><span class="sxs-lookup"><span data-stu-id="f80a9-871">Add the new **QuestionnairesErReportLabels\_en-US** labels file to your Visual Studio project, and specify the following labels for new UI resources:</span></span>

- <span data-ttu-id="f80a9-872">أضف تسمية **\@QuestionnairesReport** لعنصر قائمة جديد يحتوي على النص التالي باللغة US English (en-US): **تقرير الاستبيانات (مشغّل بواسطة التقارير الإلكترونية)**</span><span class="sxs-lookup"><span data-stu-id="f80a9-872">The **\@QuestionnairesReport** label for a new menu item that contains the following text in US English (en-US): **Questionnaires report (powered by ER)**</span></span>
- <span data-ttu-id="f80a9-873">التسمية **\@QuestionnairesReportBatchJobDescription** لعنوان وظيفة دُفعية إذا تمت جدولة تنسيق التقارير الإلكترونية لتنفيذه كوظيفة دُفعية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-873">The **\@QuestionnairesReportBatchJobDescription** label for a batch job title if a selected ER format is scheduled for execution as a batch job</span></span>

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a><span data-ttu-id="f80a9-874">إضافة فئة خدمة تقرير</span><span class="sxs-lookup"><span data-stu-id="f80a9-874">Add a report service class</span></span>

<span data-ttu-id="f80a9-875">أضف الفئة الجديدة **QuestionnairesErReportService** إلى مشروع Visual Studio واكتب تعليمات برمجية تستدعي تنسيق تقارير إلكترونية، ويحدده بواسطة معرف تعيين التنسيق، ويوفر عقد بيانات كمعلمة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-875">Add the new **QuestionnairesErReportService** class to your Visual Studio project, and write code that calls an ER format, identifies it by a format mapping ID, and provides a data contract as a parameter.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

<span data-ttu-id="f80a9-876">عندما يجب استخدام تنسيق التقارير الإلكترونية الذي يقوم بتشغيل بيانات التطبيق، يجب عليك تكوين مصدر بيانات من النوع **نموذج بيانات** في تعيين التنسيق.</span><span class="sxs-lookup"><span data-stu-id="f80a9-876">When you must use an ER format that runs application data, you must configure a data source of the **Data model** type in the format mapping.</span></span> <span data-ttu-id="f80a9-877">يشير مصدر البيانات هذا إلى جزء معين من نموذج البيانات المحدد باستخدام تعريف جذر مفرد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-877">This data source refers to a specific part of the specified data model by using a single root definition.</span></span> <span data-ttu-id="f80a9-878">يستدعي تنسيق التقارير الإلكترونية، عند تشغيله، مصدر البيانات هذا للوصول إلى تعيين تنسيق التقارير الإلكترونية المناسب الذي تم تكوينه لنموذج محدد وتعريف جذر.</span><span class="sxs-lookup"><span data-stu-id="f80a9-878">When the ER format is run, it calls this data source to access the appropriate ER model mapping that is configured for a given model and root definition.</span></span>

<span data-ttu-id="f80a9-879">يمكن تمرير كافة المعلومات التي قد تعمل على تحضيرها في التعليمات البرمجية المصدر وتخزينها كجزء من عقد البيانات إلى تنسيق التقارير الإلكترونية قيد التشغيل باستخدام تعيين نموذج تقارير إلكترونية من هذا النوع.</span><span class="sxs-lookup"><span data-stu-id="f80a9-879">All the information that you might prepare in the source code and store as part of the data contract can be passed to the running ER format by using an ER model mapping of this type.</span></span> <span data-ttu-id="f80a9-880">في تعيين نموذج التقارير الإلكترونية، يجب تكوين مصدر بيانات من نوع **الكائن** يشير إلى فئة **[QuestionnairesErReportContract](#DataContractClass)**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-880">In the ER model mapping, you must configure a data source of the **Object** type that refers to the **[QuestionnairesErReportContract](#DataContractClass)** class.</span></span> <span data-ttu-id="f80a9-881">لتحديد تعيين نموذج، يجب تحديد مصدر بيانات يستدعي تعيين النموذج هذا.</span><span class="sxs-lookup"><span data-stu-id="f80a9-881">To identify a model mapping, you must specify a data source that calls this model mapping.</span></span> <span data-ttu-id="f80a9-882">في التعليمات البرمجية المتوفرة، يتم تحديد مصدر البيانات هذا بواسطة الثابت **ERModelDataSourceName** الذي لديه قيمة **[النموذج](#ModelDSName)**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-882">In the provided code, this data source specified by the **ERModelDataSourceName** constant that has the **[model](#ModelDSName)** value.</span></span> <span data-ttu-id="f80a9-883">لتحديد مصدر البيانات المستخدم لعرض عقد البيانات في تعيين النموذج، يجب تحديد اسم مصدر البيانات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-883">To identify which data source is used to expose the data contract in the model mapping, you must specify a data source name.</span></span> <span data-ttu-id="f80a9-884">في التعليمات البرمجية المتوفرة، يتم تحديد هذا الاسم بواسطة الثابت **ParametersDataSourceName** الذي لديه قيمة <a name="DataContractDSName"></a>**RunTimeParameters**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-884">In the provided code, this name is specified by the **ParametersDataSourceName** constant that has <a name="DataContractDSName"></a>**RunTimeParameters** value.</span></span>

> [!NOTE]
> <span data-ttu-id="f80a9-885">في بيئة جديدة، قد يلزم تحديث بيانات تعريف التقارير الإلكترونية بحيث يتوفر هذا النوع من الفئات في مصمم تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-885">In a new environment, you might have to refresh the ER metadata so that this type of class is available in the ER model mapping designer.</span></span> <span data-ttu-id="f80a9-886">لمزيد من المعلومات، راجع [تكوين إطار عمل إعداد التقارير الإلكترونية](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="f80a9-886">For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span></span>

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a><span data-ttu-id="f80a9-887">إضافة فئة مراقب التقارير</span><span class="sxs-lookup"><span data-stu-id="f80a9-887">Add a report controller class</span></span>

<span data-ttu-id="f80a9-888">أضف الفئة **QuestionnairesErReportController** إلى مشروع Visual Studio واكتب التعليمات البرمجية التي يتم تشغيلها على تنسيق التقارير الإلكترونية في الوضع المتزامن أو وضع الدُفعة، كما تفضل، في مربع الحوار المبني بالاستناد إلى منطق فئة **QuestionnairesErReportUIBuilder** المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-888">Add the new **QuestionnairesErReportController** class to your Visual Studio project, and write code that runs an ER format in either synchronous mode or batch mode, as you prefer, in the dialog box that is built based on the logic of the provided **QuestionnairesErReportUIBuilder** class.</span></span>

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a><span data-ttu-id="f80a9-889">إضافة عنصر قائمة</span><span class="sxs-lookup"><span data-stu-id="f80a9-889">Add a menu item</span></span>

<span data-ttu-id="f80a9-890">أضف عنصر قائمة **QuestionnairesErReport** الجديد إلى مشروع Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f80a9-890">Add the new **QuestionnairesErReport** menu item to your Visual Studio project.</span></span> <span data-ttu-id="f80a9-891">في خاصية **الكائن**، يشير عنصر القائمة هذا إلى فئة **QuestionnairesErReportController**، ويتم استخدامه لتحديد إذن المستخدم لتحديده وتشغيل تنسيق تقارير إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-891">In the **Object** property, this menu item refers to the **QuestionnairesErReportController** class, and it's used to specify a user permission to select and run an ER format.</span></span> <span data-ttu-id="f80a9-892">في خاصية **التسمية**، يشير عنصر القائمة هذا إلى تسمية **\@QuestionnairesReport** التي أنشأتها في وقت سابق، بحيث يتم تقديم النص الصحيح في واجهة برمجة تطبيقات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="f80a9-892">In the **Label** property, this menu item refers to the **\@QuestionnairesReport** label that you created earlier, so that correct text is presented in the application UI.</span></span>

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a><span data-ttu-id="f80a9-893">إضافة عنصر قائمة إلى قائمة</span><span class="sxs-lookup"><span data-stu-id="f80a9-893">Add a menu item to a menu</span></span>

<span data-ttu-id="f80a9-894">أضف قائمة **KM** الموجودة إلى مشروع Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f80a9-894">Add the existing **KM** menu to your Visual Studio project.</span></span> <span data-ttu-id="f80a9-895">يجب إضافة عنصر **QuestionnairesErReport** جديد من النوع **إخراج** إلى هذه القائمة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-895">You must add a new **QuestionnairesErReport** item of the **Output** type to this menu.</span></span> <span data-ttu-id="f80a9-896">يجب أن يشير هذا العنصر إلى عنصر قائمة **QuestionnairesErReport** الذي ورد وصفه في القسم السابق.</span><span class="sxs-lookup"><span data-stu-id="f80a9-896">This item must refer to the **QuestionnairesErReport** menu item that is described in the previous section.</span></span>

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a><span data-ttu-id="f80a9-897">إنشاء مشروع Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f80a9-897">Build a Visual Studio project</span></span>

<span data-ttu-id="f80a9-898">قم بإنشاء مشروع لجعل عنصر قائمة جديد متوفرًا للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="f80a9-898">Build your project to make a new menu item available to users.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a><span data-ttu-id="f80a9-899">تشغيل تنسيق من التطبيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-899">Run a format from the application</span></span>

1. <span data-ttu-id="f80a9-900">انتقل إلى **الاستبيان** \> **تصميم** \> **تقرير الاستبيانات (مشغّل بواسطة التقارير الإلكترونية)‬**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-900">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>

    ![تحديد عنصر قائمة الاستبيانات (مشغّل بواسطة التقارير الإلكترونية)‬‏‫ في الوحدة النمطية للاستبيان لتشغيل التقارير الإلكترونية المكوّن](./media/er-quick-start1-application-menu-modified.png)

2. <span data-ttu-id="f80a9-902">في مربع الحوار، في حقل **تعيين التنسيق**، حدد **تقرير الاستبيانات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-902">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="f80a9-903">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-903">Select **OK**.</span></span>
4. <span data-ttu-id="f80a9-904">في مربع الحوار **معلمات التقارير الإلكترونية‬**، على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**، قم بتكوين خيار التصفية بحيث يتم تضمين الاستبيان **SBCCrsExam** فقط,</span><span class="sxs-lookup"><span data-stu-id="f80a9-904">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="f80a9-905">حدد **موافق** لتأكيد خيار التصفية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-905">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="f80a9-906">حدد **موافق** لتشغيل التقرير.</span><span class="sxs-lookup"><span data-stu-id="f80a9-906">Select **OK** to run the report.</span></span>

    ![تحديد معايير التحديد في مربع حوار التقارير الإلكترونية](./media/er-quick-start1-report-run-dialog-page.png)

7. <span data-ttu-id="f80a9-908">راجع التقرير المُنشأ.</span><span class="sxs-lookup"><span data-stu-id="f80a9-908">Review the generated report.</span></span>

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a><span data-ttu-id="f80a9-909">ضبط حل إعداد التقارير الإلكترونية المصمّم</span><span class="sxs-lookup"><span data-stu-id="f80a9-909">Tune a designed ER solution</span></span>

<span data-ttu-id="f80a9-910">يمكنك تعديل حل التقارير الإلكترونية المكوّن بحيث يستخدم فئة موفر البيانات التي تم تطويرها للوصول إلى تفاصيل تنسيق تقارير إلكترونية قيد التشغيل، بحيث يدخل اسم تنسيق التقارير الإلكترونية هذا في تقرير بتم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="f80a9-910">You can modify the configured ER solution so that it uses the data provider class that you developed to access details of the running ER format, and so that it enters the name of this ER format in a generated report.</span></span>

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a><span data-ttu-id="f80a9-911">تعديل تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="f80a9-911">Modify a model mapping</span></span>

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a><span data-ttu-id="f80a9-912">إضافة مصادر بيانات للوصول إلى كائن عقد البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-912">Add data sources to access a data contract object</span></span>

1. <span data-ttu-id="f80a9-913">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-913">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f80a9-914">في صفحة **التكوينات**، في شجرة التكوين، وسَّع **نموذج الاستبيان**، ثم حدد **تعيين الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-914">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="f80a9-915">Select **الصمم** لفتح صحة **تعيين النموذج إلى مصدر البيانات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-915">Select **Designer** to open the **Model to datasource mapping** page.</span></span>
4. <span data-ttu-id="f80a9-916">حدد **المصمم** لفتح التعيين المحدد في مصمم تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="f80a9-916">Select **Designer** to open the selected mapping in the model mapping designer.</span></span>
5. <span data-ttu-id="f80a9-917">في صفحة **مصمم تعيين النموذج**، في جزء **أنواع مصادر البيانات**، حدد **Dynamics 365 for Operations\\كائن‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-917">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Object**.</span></span>
6. <span data-ttu-id="f80a9-918">حدد **إضافة جذر** في جزء **مصادر البيانات** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-918">In the **Data sources** pane, select **Add root**.</span></span>
7. <span data-ttu-id="f80a9-919">في مربع الحوار، في حقل **الاسم**، أدخل **[RunTimeParameters](#DataContractDSName)**، كما هو محدد في التعليمات البرمجية المصدر في الفئة **QuestionnairesErReportService**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-919">In the dialog box, in the **Name** field, enter **[RunTimeParameters](#DataContractDSName)**, as defined in the source code of the **QuestionnairesErReportService** class.</span></span>
8. <span data-ttu-id="f80a9-920">في حقل **الفئة**، أدخل **[QuestionnairesErReportContract](#DataContractClass)**، الذي تم ترميزه في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="f80a9-920">In the **Class** field, enter **[QuestionnairesErReportContract](#DataContractClass)**, which was coded earlier.</span></span>
9. <span data-ttu-id="f80a9-921">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-921">Select **OK**.</span></span>
10. <span data-ttu-id="f80a9-922">قم بتوسيع **RunTimeParameters**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-922">Expand **RunTimeParameters**.</span></span>

<span data-ttu-id="f80a9-923">يوفر مصدر البيانات المضاف معلومات حول معرف السجل الخاص بتعيين تنسيق التقارير الإلكترونية قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="f80a9-923">The added data source provides information about the record ID of the running ER format mapping.</span></span>

![مصدر بيانات مضاف في مصمم تعيين نموذج التقارير الإلكترونية](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a><span data-ttu-id="f80a9-925">إضافة مصدر بيانات للوصول إلى سجلات تعيين تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f80a9-925">Add a data source to access ER format mapping records</span></span>

<span data-ttu-id="f80a9-926">تابع تحرير تعيين النموذج المحدد عن طريق إضافة مصدر بيانات للوصول إلى سجلات تعيين تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-926">Continue to edit the selected model mapping by adding a data source to access ER format mapping records.</span></span>

1. <span data-ttu-id="f80a9-927">في صفحة **مصمم تعيين النموذج**، في جزء **أنواع مصادر البيانات**، حدد **Dynamics 365 for Operations\\Table records**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-927">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="f80a9-928">حدد **إضافة جذر** في جزء **مصادر البيانات** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-928">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="f80a9-929">في مربع الحوار، في الحقل **الاسم**، أدخل **ER1**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-929">In the dialog box, in the **Name** field, enter **ER1**.</span></span>
4. <span data-ttu-id="f80a9-930">في حقل **الجدول**، أدخل **ERFormatMappingTable‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-930">In the **Table** field, enter **ERFormatMappingTable**.</span></span>
5. <span data-ttu-id="f80a9-931">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-931">Select **OK**.</span></span>

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a><span data-ttu-id="f80a9-932">إضافة مصدر بيانات للوصول إلى سجل تعيين التنسيق لتنسيق تقارير إلكترونية قيد التشغيل</span><span class="sxs-lookup"><span data-stu-id="f80a9-932">Add a data source to access a format mapping record of a running ER format</span></span>

<span data-ttu-id="f80a9-933">تابع تحرير تعيين النموذج المحدد عن طريق إضافة مصدر بيانات للوصول إلى سجل تعيين تنسيق التقارير الإلكترونية قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="f80a9-933">Continue to edit the selected model mapping by adding a data source to access the format mapping record of the running ER format.</span></span>

1. <span data-ttu-id="f80a9-934">في صفحة **مصمم تعيين النموذج**، في جزء **أنواع مصادر البيانات**، حدد **الدالات\\الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-934">On the **Model mapping designer** page, in the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
2. <span data-ttu-id="f80a9-935">حدد **إضافة جذر** في جزء **مصادر البيانات** .</span><span class="sxs-lookup"><span data-stu-id="f80a9-935">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="f80a9-936">في مربع الحوار، في الحقل **الاسم**، أدخل **ER2**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-936">In the dialog box, in the **Name** field, enter **ER2**.</span></span>
4. <span data-ttu-id="f80a9-937">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-937">Select **Edit formula**.</span></span>
5. <span data-ttu-id="f80a9-938">في محرر المعادلة، في حقل **المعادلة**، أدخل **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-938">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span></span>
6. <span data-ttu-id="f80a9-939">حدد **حفظ** ثم قم بإغلاق محرر المعادلات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-939">Select **Save**, and close the formula editor.</span></span>
7. <span data-ttu-id="f80a9-940">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-940">Select **OK**.</span></span>

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a><span data-ttu-id="f80a9-941">إدخال اسم تنسيق تقارير إلكترونية قيد التشغيل في نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="f80a9-941">Enter the name of the running ER format in the data model</span></span>

<span data-ttu-id="f80a9-942">تابع تحرير تعيين النموذج المحدد بحيث يتم إدخال اسم تنسيق التقارير الإلكترونية قيد التشغيل في نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-942">Continue to edit the selected model mapping so that the name of the running ER format is entered in the data model.</span></span>

1. <span data-ttu-id="f80a9-943">في صفحة **مصمم تعيين النموذج**، في جزء **نموذج البيانات** قم بتوسيع **ExecutionContext**، ثم حدد **ExecutionContext\\FormatName**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-943">On the **Model mapping designer** page, in the **Data model** pane, expand **ExecutionContext**, and then select **ExecutionContext\\FormatName**.</span></span>
2. <span data-ttu-id="f80a9-944">في جزء **نموذج البيانات**، حدد **تحرير** لتكوين ربط البيانات لحقل نموذج البيانات المحدد.</span><span class="sxs-lookup"><span data-stu-id="f80a9-944">In the **Data model** pane, select **Edit** to configure a data binding for the selected data model's field.</span></span>
3. <span data-ttu-id="f80a9-945">في محرر المعادلة، في حقل **المعادلة**، أدخل **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-945">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span></span>
4. <span data-ttu-id="f80a9-946">حدد **حفظ** ثم قم بإغلاق محرر المعادلات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-946">Select **Save**, and close the formula editor.</span></span>

<span data-ttu-id="f80a9-947">لأنك استخدمت الحقل **FormatName**، يقوم تعيين النموذج المكوّن الآن بكشف اسم تنسيق التقارير الإلكترونية الذي يستدعي تعيين هذا النموذج أثناء التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="f80a9-947">Because you used the **FormatName** field, the configured model mapping now exposes the name of an ER format that calls this model mapping during execution.</span></span>

![ربط حقل نموذج البيانات بأسلوب مصدر البيانات المضاف في مصمم تعيين نموذج التقارير الإلكترونية](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a><span data-ttu-id="f80a9-949">إكمال تصميم تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="f80a9-949">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="f80a9-950">في صفحة **مصمم تعيين النموذج**، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-950">On the **Model mapping designer** page, select **Save**.</span></span>
2. <span data-ttu-id="f80a9-951">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f80a9-951">Close the page.</span></span>
3. <span data-ttu-id="f80a9-952">أغلق صفحة تعيينات النماذج.</span><span class="sxs-lookup"><span data-stu-id="f80a9-952">Close the model mappings page.</span></span>
4. <span data-ttu-id="f80a9-953">في صفحة **التكوينات**، في شجرة التكوين، تأكد من استمرار تحديد تكوين **تعيين الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-953">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire mapping** configuration is still selected.</span></span> <span data-ttu-id="f80a9-954">بعد ذلك، على علامة التبويب السريعة **الإصدارات**، حدد إصدار التكوين بحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-954">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
5. <span data-ttu-id="f80a9-955">حدد **تغيير الحالة** \> **مكتمل‏‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-955">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="f80a9-956">تم تغيير حالة الإصدار 1.2 من هذا التكوين من **مسودة** إلى **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-956">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="f80a9-957">لم يعد من الممكن تغيير الإصدار 1.2.</span><span class="sxs-lookup"><span data-stu-id="f80a9-957">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="f80a9-958">يحتوي هذا الإصدار على تعيين النموذج الذي تم تكوينه ويمكن استخدامه كأساس لتكوينات إعداد التقارير الإلكترونية الأخرى.</span><span class="sxs-lookup"><span data-stu-id="f80a9-958">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="f80a9-959">تم إنشاء الإصدار 1.3 من هذا التكوين وهو بالحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-959">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="f80a9-960">يمكنك تحرير هذا الإصدار لتعديل تعيين نموذج **الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-960">You can edit this version to adjust the **Questionnaire** model mapping.</span></span>

### <a name="modify-a-format"></a><a name="ModifyFormat"></a><span data-ttu-id="f80a9-961">تعديل تنسيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-961">Modify a format</span></span>

<span data-ttu-id="f80a9-962">يمكنك تعديل تنسيق التقارير الإلكترونية المكوّن بحيث يتم عرض اسمه في تذييل التقرير الذي يتم إنشاؤه عند تشغيل تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-962">You can modify the configured ER format so that its name is shown in the footer of a report that is generated when the ER format is run.</span></span>

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a><span data-ttu-id="f80a9-963">إضافة عنصر تنسيق جديد</span><span class="sxs-lookup"><span data-stu-id="f80a9-963">Add a new format element</span></span>

1. <span data-ttu-id="f80a9-964">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-964">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f80a9-965">في صفحة **التكوينات**، في شجرة التكوين، وسَّع **نموذج الاستبيان**، ثم حدد **تقرير الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-965">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="f80a9-966">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-966">Select **Designer**.</span></span>
4. <span data-ttu-id="f80a9-967">في الصفحة **مصمم التنسيق**، حدد عنصر الجذر **التقرير**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-967">On the **Format designer** page, select the **Report** root item.</span></span>
5. <span data-ttu-id="f80a9-968">حدد **إضافة** لإضافة‏‎ عنصر تنسيق متداخل عنصر جذر **التقرير**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-968">Select **Add** to add a new nested format element for the selected **Report** root item.</span></span>
6. <span data-ttu-id="f80a9-969">حدد **Excel\\تذييل**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-969">Select **Excel\\Footer**.</span></span>
7. <span data-ttu-id="f80a9-970">في الحقل **الاسم**، أدخل **التذييل**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-970">In the **Name** field, enter **Footer**.</span></span>
8. <span data-ttu-id="f80a9-971">حدد **التقرير\التذييل**، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-971">Select **Report\Footer**, and then select **Add**.</span></span>
9. <span data-ttu-id="f80a9-972">حدد **نص\\سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-972">Select **Text\\String**.</span></span>

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a><span data-ttu-id="f80a9-973">ربط عنصر التنسيق المضاف</span><span class="sxs-lookup"><span data-stu-id="f80a9-973">Bind the added format element</span></span>

1. <span data-ttu-id="f80a9-974">في صفحة **مصمم التنسيق**، على علامة التبويب **التعيين** في شجرة التنسيق، لعنصر **تذييل\\سلسلة** النشط، حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-974">On the **Format designer** page, on the **Mapping** tab, in the format tree, for the active **Footer\\String** element, select **Edit formula**.</span></span>
2. <span data-ttu-id="f80a9-975">في محرر المعادلة، في حقل **المعادلة**، أدخل **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-975">In the formula editor, in the **Formula** field, enter **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span></span>
3. <span data-ttu-id="f80a9-976">حدد **حفظ** ثم قم بإغلاق محرر المعادلات.</span><span class="sxs-lookup"><span data-stu-id="f80a9-976">Select **Save**, and close the formula editor.</span></span>
4. <span data-ttu-id="f80a9-977">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-977">Select **Save**.</span></span>

<span data-ttu-id="f80a9-978">لقد تم الآن تعديل التنسيق المكوّن بحيث يتم إدخال اسمه في تذييل التقرير الذي تم إنشاؤه باستخدام العنصر **تذييل\\سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-978">The configured format has now been modified so that its name will be entered in the footer of a generated report by using the **Footer\\String** element.</span></span>

![أضافه عنصر تنسيق التذييل إلى التنسيق الذي تم تكوينه في مصمم عمليات التقارير الإلكترونية‬](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a><span data-ttu-id="f80a9-980">إكمال تصميم التنسيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-980">Complete the format design</span></span>

1. <span data-ttu-id="f80a9-981">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-981">Close the **Format designer** page.</span></span>
2. <span data-ttu-id="f80a9-982">في صفحة **التكوينات**، في شجرة التكوين، تأكد من استمرار تحديد تكوين **تقرير الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-982">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire report** configuration is still selected.</span></span> <span data-ttu-id="f80a9-983">بعد ذلك، على علامة التبويب السريعة **الإصدارات**، حدد إصدار التكوين بحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-983">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
3. <span data-ttu-id="f80a9-984">حدد **تغيير الحالة** \> **مكتمل‏‎**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-984">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="f80a9-985">تم تغيير حالة الإصدار 1.2 من هذا التكوين من **مسودة** إلى **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-985">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="f80a9-986">لم يعد من الممكن تغيير الإصدار 1.2.</span><span class="sxs-lookup"><span data-stu-id="f80a9-986">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="f80a9-987">يحتوي هذا الإصدار على التنسيق المكوّن ويمكن استخدامه كأساس لتكوينات إعداد التقارير الإلكترونية الأخرى.</span><span class="sxs-lookup"><span data-stu-id="f80a9-987">This version contains the configured format and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="f80a9-988">تم إنشاء الإصدار 1.3 من هذا التكوين وهو بالحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-988">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="f80a9-989">يمكنك تحرير هذا الإصدار لتعديل تقرير **الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-989">You can edit this version to adjust the **Questionnaire** report.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a><span data-ttu-id="f80a9-990">تشغيل تنسيق من التطبيق</span><span class="sxs-lookup"><span data-stu-id="f80a9-990">Run a format from the application</span></span>

1. <span data-ttu-id="f80a9-991">انتقل إلى **الاستبيان** \> **تصميم** \> **تقرير الاستبيانات (مشغّل بواسطة التقارير الإلكترونية)‬**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-991">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="f80a9-992">في مربع الحوار، في حقل **تعيين التنسيق**، حدد **تقرير الاستبيانات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-992">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="f80a9-993">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-993">Select **OK**.</span></span>
4. <span data-ttu-id="f80a9-994">في مربع الحوار **معلمات التقارير الإلكترونية‬**، على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**، قم بتكوين خيار التصفية بحيث يتم تضمين الاستبيان **SBCCrsExam** فقط,</span><span class="sxs-lookup"><span data-stu-id="f80a9-994">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="f80a9-995">حدد **موافق** لتأكيد خيار التصفية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-995">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="f80a9-996">حدد **موافق** لتشغيل التقرير.</span><span class="sxs-lookup"><span data-stu-id="f80a9-996">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="f80a9-997">راجع التقرير الذي تم إنشاؤه بتنسيق Excel.</span><span class="sxs-lookup"><span data-stu-id="f80a9-997">Review the generated report in Excel format.</span></span>

<span data-ttu-id="f80a9-998">لاحظ أن تذييل التقرير الذي تم إنشاؤه يحتوي على اسم تنسيق التقارير الإلكترونية الذي تم استخدامه لإنشائه.</span><span class="sxs-lookup"><span data-stu-id="f80a9-998">Notice that the footer of the generated report contains the name of the ER format that was used to generate it.</span></span>

![التقرير الذي تم إنشاؤه بتنسيق Excel](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a><span data-ttu-id="f80a9-1000">تشغيل تنسيق من التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f80a9-1000">Run a format from ER</span></span>

1. <span data-ttu-id="f80a9-1001">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1001">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f80a9-1002">في صفحة **التكوينات**، في شجرة التكوين، وسَّع **نموذج الاستبيان**، ثم حدد **تقرير الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1002">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="f80a9-1003">في جزء الإجراءات، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1003">On the Action Pane, select **Run**.</span></span>
4. <span data-ttu-id="f80a9-1004">في مربع الحوار **معلمات التقارير الإلكترونية‬**، على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**، قم بتكوين خيار التصفية بحيث يتم تضمين الاستبيان **SBCCrsExam** فقط,</span><span class="sxs-lookup"><span data-stu-id="f80a9-1004">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="f80a9-1005">حدد **موافق** لتأكيد خيار التصفية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1005">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="f80a9-1006">حدد **موافق** لتشغيل التقرير.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1006">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="f80a9-1007">راجع التقرير الذي تم إنشاؤه بتنسيق Excel.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1007">Review the generated report in Excel format.</span></span>

<span data-ttu-id="f80a9-1008">لاحظ أن تذييل التقرير الذي تم إنشاؤه لا يحتوي على اسم تنسيق التقارير الإلكترونية الذي تم استخدامه لإنشائها، بسبب عدم تمرير كائن عقد البيانات إلى تعيين النموذج قيد التشغيل عند استدعائه بواسطة تنسيق التقارير الإلكترونية لذي تم تشغيله من التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1008">Notice that the footer of the generated report doesn't contain the name of ER format that was used to generate it, because the data contract object wasn't passed to the running model mapping when it was called by the ER format that was run from ER.</span></span>

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a><span data-ttu-id="f80a9-1009">تكوين وجهة التنسيق للمعاينة على الشاشة</span><span class="sxs-lookup"><span data-stu-id="f80a9-1009">Configure a format destination for on-screen preview</span></span>

1. <span data-ttu-id="f80a9-1010">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **وجهة إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1010">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting destination**.</span></span>
2. <span data-ttu-id="f80a9-1011">في صفحة **وجهة إعداد التقارير الإلكترونية**، أضف سجل وجهة لتنسيق التقارير الإلكترونية **تقرير الاستبيان** المكوّن.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1011">On the **Electronic reporting destination** page, add a destination record for the configured **Questionnaire report** ER format.</span></span>
3. <span data-ttu-id="f80a9-1012">على علامة التبويب **وجهة الملف**، قم بإعداد **وجهة** [الشاشة](er-destination-type-screen.md) لمكون تنسيق **التقرير** الذي تمت [إضافته](#AddFormatRootElement) كعنصر جذر لتنسيق التقارير الإلكترونية المكوّن **تقرير الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1012">On the **File destination** FastTab, set up the **Screen** [destination](er-destination-type-screen.md) for the **Report** format component that has been [added](#AddFormatRootElement) as the root element of the configured **Questionnaire report** ER format.</span></span>
4. <span data-ttu-id="f80a9-1013">على علامة التبويب السريعة **إعدادات تحويل PDF**، قم بتكوين الوجهة لتحويل تقرير إلى [تنسيق PDF](electronic-reporting-destinations.md#OutputConversionToPDF) يستخدم اتجاه الصفحة **أفقي**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1013">On the **PDF conversion settings** FastTab, configure the destination to convert a report to [PDF format](electronic-reporting-destinations.md#OutputConversionToPDF) that uses the **Landscape** page orientation.</span></span>

![تكوين وجهة الشاشة المخصصة لتنسيق التقارير الإلكترونية على صفحة وجهة التقارير الإلكترونية](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a><span data-ttu-id="f80a9-1015">تشغيل تنسيق من التطبيق لمعاينته كمستند PDF</span><span class="sxs-lookup"><span data-stu-id="f80a9-1015">Run a format from the application to preview it as a PDF document</span></span>

1. <span data-ttu-id="f80a9-1016">انتقل إلى **الاستبيان** \> **تصميم** \> **تقرير الاستبيانات (مشغّل بواسطة التقارير الإلكترونية)‬**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1016">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="f80a9-1017">في مربع الحوار، في حقل **تعيين التنسيق**، حدد **تقرير الاستبيانات**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1017">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="f80a9-1018">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1018">Select **OK**.</span></span>
4. <span data-ttu-id="f80a9-1019">في مربع الحوار **معلمات التقارير الإلكترونية‬**، على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**، قم بتكوين خيار التصفية بحيث يتم تضمين الاستبيان **SBCCrsExam** فقط,</span><span class="sxs-lookup"><span data-stu-id="f80a9-1019">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="f80a9-1020">حدد **موافق** لتأكيد خيار التصفية.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1020">Select **OK** to confirm the filtering option.</span></span>

    <span data-ttu-id="f80a9-1021">على علامة التبويب **الوجهات**، لاحظ تعيين حقل **الإخراج** إلى **الشاشة**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1021">On the **Destinations** FastTab, notice that the **Output** field is set to **Screen**.</span></span> <span data-ttu-id="f80a9-1022">إذا كنت ترغب في تغيير الوجهة المكونة، حدد **تغيير**.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1022">If you want to change the configured destination, select **Change**.</span></span>

    ![مربع الحوار وقت تشغيل التقارير الإلكترونية حيث يمكنك تغيير الوجهة المكونة](./media/er-quick-start1-run-settings.png)

6. <span data-ttu-id="f80a9-1024">حدد **موافق** لتشغيل التقرير.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1024">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="f80a9-1025">راجع التقرير الذي تم إنشاؤه بتنسيق PDF.</span><span class="sxs-lookup"><span data-stu-id="f80a9-1025">Review the generated report in PDF format.</span></span>

    ![معاينة على الشاشة للتقرير الذي تم إنشاؤه بتنسيق PDF](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a><span data-ttu-id="f80a9-1027">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f80a9-1027">Additional resources</span></span>

- [<span data-ttu-id="f80a9-1028">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f80a9-1028">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="f80a9-1029">لغة تركيبة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f80a9-1029">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="f80a9-1030">تصميم تقارير متعددة اللغات</span><span class="sxs-lookup"><span data-stu-id="f80a9-1030">Design multilingual reports</span></span>](er-design-multilingual-reports.md)
- [<span data-ttu-id="f80a9-1031">API إطار عمل التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f80a9-1031">ER framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="f80a9-1032">الدالة CASE</span><span class="sxs-lookup"><span data-stu-id="f80a9-1032">CASE function</span></span>](er-functions-logical-case.md)
- [<span data-ttu-id="f80a9-1033">الدالة CONCATENATE</span><span class="sxs-lookup"><span data-stu-id="f80a9-1033">CONCATENATE function</span></span>](er-functions-text-concatenate.md)
- [<span data-ttu-id="f80a9-1034">الدالة DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="f80a9-1034">DATETIMEFORMAT function</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="f80a9-1035">الدالة FILTER</span><span class="sxs-lookup"><span data-stu-id="f80a9-1035">FILTER function</span></span>](er-functions-list-filter.md)
- [<span data-ttu-id="f80a9-1036">الدالة FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="f80a9-1036">FIRSTORNULL function</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="f80a9-1037">الدالة FORMAT</span><span class="sxs-lookup"><span data-stu-id="f80a9-1037">FORMAT function</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="f80a9-1038">الدالة IF</span><span class="sxs-lookup"><span data-stu-id="f80a9-1038">IF function</span></span>](er-functions-logical-if.md)
- [<span data-ttu-id="f80a9-1039">الدالة ORDERBY</span><span class="sxs-lookup"><span data-stu-id="f80a9-1039">ORDERBY function</span></span>](er-functions-list-orderby.md)
- [<span data-ttu-id="f80a9-1040">الدالة SESSIONNOW</span><span class="sxs-lookup"><span data-stu-id="f80a9-1040">SESSIONNOW function</span></span>](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
