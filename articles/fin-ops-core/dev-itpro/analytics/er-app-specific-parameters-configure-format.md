---
title: تكوين تنسيقات التقارير الإلكترونية لاستخدام المعلمات المحددة لكل كيان قانوني
description: يوضح هذا الموضوع كيفيه تكوين تنسيقات إعداد التقارير الكترونيه (ER) لاستخدام المعلمات التي تم تحديدها لكل كيان قانوني.
author: NickSelin
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 3802675b2fe0615f4c2ad682462a233c67f18f1a
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853483"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="36d24-103">تكوين تنسيقات التقارير الإلكترونية لاستخدام المعلمات المحددة لكل كيان قانوني</span><span class="sxs-lookup"><span data-stu-id="36d24-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="36d24-104">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="36d24-104">Overview</span></span>

<span data-ttu-id="36d24-105">في العديد من تنسيقات إعداد التقارير الكترونيه (ER) التي ستقوم بتصميمها ، يجب تصفيه البيانات باستخدام مجموعه من القيم الخاصة بكل كيان قانوني من المثيل الخاص بك (علي سبيل المثال ، مجموعه من أكواد الضريبة لتصفيه الحركات الضريبية).</span><span class="sxs-lookup"><span data-stu-id="36d24-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="36d24-106">حاليا ، عند تكوين التصفية من هذا النوع بتنسيق ER ، يتم استخدام القيم التي تعتمد علي الكيان القانوني (علي سبيل المثال ، أكواد الضريبة) في التعبيرات الخاصة بالتنسيق ER لتحديد قواعد تصفيه البيانات.</span><span class="sxs-lookup"><span data-stu-id="36d24-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="36d24-107">التالي ، يتم إنشاء التنسيق القانوني للكيان القانوني الخاص بالكيان القانوني ، ولإنشاء التقارير المطلوبة ، يجب إنشاء نسخ مشتقه من تنسيق ER الأصلي لكل كيان قانوني حيث يتعين عليك تشغيل التنسيق الخاص ب ER.</span><span class="sxs-lookup"><span data-stu-id="36d24-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="36d24-108">يجب تحرير كل تنسيق تقارير إلكترونية مشتق لإحضار قيم خاصة بالكيان القانوني إليها، ويجب إعادة تعيين أساسه كلما تم تحديث الإصدار الأصلي (الأساسي)، وتصديره من بيئة اختبار، واستيراده إلى بيئة إنتاج عندما يجب نشره لاستخدام بيئة الإنتاج، وهكذا.</span><span class="sxs-lookup"><span data-stu-id="36d24-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment, and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="36d24-109">وبالتالي، فإن صيانة هذا النوع من حل التقارير الإلكترونية المكوّن هي معقده وتستهلك الكثير من الوقت لأسباب كثيرة:</span><span class="sxs-lookup"><span data-stu-id="36d24-109">Therefore, maintenance of this type of configured ER solution is complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="36d24-110">وكلما زادت الكيانات القانونية ، يجب الحفاظ علي تكوينات التنسيق الإضافية الخاصة بالتنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="36d24-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="36d24-111">يتطلب صيانة تكوينات ER ان يقوم مستخدمو الاعمال بمعرفه المعارف ل ER.</span><span class="sxs-lookup"><span data-stu-id="36d24-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="36d24-112">ميزه المعلمات الخاصة بالتطبيق الخاص ب ER السماح لمستخدمي الطاقة بتكوين تصفيه البيانات بتنسيق ER بحيث تستند إلى مجموعه من القواعد المجردة.</span><span class="sxs-lookup"><span data-stu-id="36d24-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="36d24-113">يمكن تكوين هذه المجموعة من القواعد لاستخدام مصادر البيانات المتوفرة في التنسيق الخاص ب ER.</span><span class="sxs-lookup"><span data-stu-id="36d24-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="36d24-114">ويمكن بعد ذلك لمستخدمي الاعمال تحديد قواعد حقيقية خارج اطار عمل ER باستخدام واجهه المستخدم (UI) التي يتم إنشاؤها تلقائيا استنادا إلى إعدادات التنسيق المقابل ل ER وبيانات الكيان القانوني الحالية التي سيتم الوصول اليها بواسطة بيانات التنسيق الخاص ب ER مصدر.</span><span class="sxs-lookup"><span data-stu-id="36d24-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="36d24-115">يمكن تصدير مجموعه القواعد المحددة لتنسيق ER من الكيان القانوني الحالي لمثيل Dynamics 365 Finance (المالية).</span><span class="sxs-lookup"><span data-stu-id="36d24-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="36d24-116">ويمكن بعد ذلك استيراده إلى كيان قانوني آخر اما لنفس مثيل التمويل أو لمثيل مختلف كمجموعه من القواعد لنفس تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="36d24-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="36d24-117">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="36d24-117">Prerequisites</span></span>

<span data-ttu-id="36d24-118">لإكمال الأمثلة الواردة في هذا الموضوع، يجب عليك الوصول إلى مثيل خدمات التكوين التنظيمية (RCS) التي تم توفيرها لنفس المستأجر مثل Finance and Operations، لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="36d24-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="36d24-119">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="36d24-119">Electronic reporting developer</span></span>
- <span data-ttu-id="36d24-120">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="36d24-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="36d24-121">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="36d24-121">System administrator</span></span>

<span data-ttu-id="36d24-122">ونوصي بإكمال الخطوات الواردة في موضوع [دعم استدعاءات المعلمات لمصادر بيانات التقارير الإلكترونية الخاصة بنوع الحقل المحسوب](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="36d24-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="36d24-123">إذا قمت بالفعل بإكمال الخطوات التالية، فيمكنك تخطي الخطوات الموجودة في قسم **استيراد تكوينات التقارير الإلكترونية إلى RCS** التالي.</span><span class="sxs-lookup"><span data-stu-id="36d24-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="36d24-124">استيراد التقارير الإلكترونية إلى RCS</span><span class="sxs-lookup"><span data-stu-id="36d24-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="36d24-125">قم بتنزيل تكوينات التقارير الإلكترونية التالية وتخزينها محليًا.</span><span class="sxs-lookup"><span data-stu-id="36d24-125">Download and locally store the following ER configurations.</span></span>

| <span data-ttu-id="36d24-126">**وصف المحتوى**</span><span class="sxs-lookup"><span data-stu-id="36d24-126">**Content description**</span></span>                        | <span data-ttu-id="36d24-127">**اسم الملف**</span><span class="sxs-lookup"><span data-stu-id="36d24-127">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="36d24-128">نموذج ملف تكوين **نموذج بيانات التقارير الإلكترونية**</span><span class="sxs-lookup"><span data-stu-id="36d24-128">Sample **ER data model** configuration file</span></span>    | [<span data-ttu-id="36d24-129">Model to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="36d24-129">Model to learn parameterized calls.version.1.xml</span></span>](https://download.microsoft.com/download/2/d/b/2db913a0-3622-494e-91a2-97fc494af9b9/Modeltolearnparameterizedcalls.version.1.xml)     |
| <span data-ttu-id="36d24-130">نموذج ملف تكوين **بيانات تعريف التقارير الإلكترونية**</span><span class="sxs-lookup"><span data-stu-id="36d24-130">Sample **ER metadata** configuration file</span></span>      | [<span data-ttu-id="36d24-131">Metadata to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="36d24-131">Metadata to learn parameterized calls.version.1.xml</span></span>](https://download.microsoft.com/download/1/b/3/1b343968-5a47-4000-b5a8-6487698ef4c0/Metadatatolearnparameterizedcalls.version.1.xml)  |
| <span data-ttu-id="36d24-132">نموذج ملف تكوين **تعيين نماذج التقارير الإلكترونية**</span><span class="sxs-lookup"><span data-stu-id="36d24-132">Sample **ER model mapping** configuration file</span></span> | [<span data-ttu-id="36d24-133">Mapping to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="36d24-133">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://download.microsoft.com/download/8/6/6/866e0ab6-2e05-4d98-9d52-d2da2038f6e4/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| <span data-ttu-id="36d24-134">نموذج تكوين **تنسيق التقارير الإلكترونية**</span><span class="sxs-lookup"><span data-stu-id="36d24-134">Sample **ER format** configuration</span></span>             | [<span data-ttu-id="36d24-135">Format to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="36d24-135">Format to learn parameterized calls.version.1.1.xml</span></span>](https://download.microsoft.com/download/e/3/9/e392eadc-b9b4-4834-95c3-b8066dd00b9c/Formattolearnparameterizedcalls.version.1.1.xml)  |

<span data-ttu-id="36d24-136">في الخطوة التالية، قم بتسجيل الدخول إلى مثيل RCS.</span><span class="sxs-lookup"><span data-stu-id="36d24-136">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="36d24-137">في هذا المثال، ستقوم بإنشاء تكوين لشركة نموذجية، وهي Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="36d24-137">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="36d24-138">قبل أن يمكنك إكمال الخطوات في هذا الإجراء، يجب أولاً إكمال الخطوات الواردة في موضوع [إنشاء موفر تكوين ووضع علامة عليه كنشط](tasks/er-configuration-provider-mark-it-active-2016-11.md) في RCS.</span><span class="sxs-lookup"><span data-stu-id="36d24-138">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="36d24-139">في لوحة المعلومات الافتراضية، حدد **‏‫إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="36d24-139">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="36d24-140">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="36d24-140">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="36d24-141">قم باستيراد تكوينات التقارير الإلكترونية التي قمت بتنزيلها مسبقًا إلى RCS، بالترتيب التالي: نموذج البيانات، وبيانات التعريف، وتعيين النموذج، والتنسيق.</span><span class="sxs-lookup"><span data-stu-id="36d24-141">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="36d24-142">بالنسبة لكل تكوين تقارير إلكترونية، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="36d24-142">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="36d24-143">حدد **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="36d24-143">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="36d24-144">حدد **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="36d24-144">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="36d24-145">حدد **استعراض** لتحديد الملف اللازم لتكوين التقارير الإلكترونية المطلوب بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="36d24-145">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="36d24-146">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="36d24-146">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="36d24-147">مراجعه حل التقارير الإلكترونية المتوفر</span><span class="sxs-lookup"><span data-stu-id="36d24-147">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="36d24-148">في شجرة التكوين، قم بتوسيع محتويات **نموذج للتعرف على الاستدعاءات ذات معلمات‬**.</span><span class="sxs-lookup"><span data-stu-id="36d24-148">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="36d24-149">حدد الصنف **تنسيق للتعرف على الاستدعاءات ذات معلمات**.</span><span class="sxs-lookup"><span data-stu-id="36d24-149">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="36d24-150">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="36d24-150">Select **Designer**.</span></span>
4.  <span data-ttu-id="36d24-151">حدد **التوسيع/الطي**.</span><span class="sxs-lookup"><span data-stu-id="36d24-151">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="36d24-152">تم تصميم تنسيق التقارير الإلكترونية **تنسيق للتعرف على الاستدعاءات ذات معلمات** لإنشاء بيان ضريبة بتنسيق XML الذي يقدم عدة مستويات من الضرائب (العادية، والمخفضة، ولا شيء).</span><span class="sxs-lookup"><span data-stu-id="36d24-152">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="36d24-153">يشتمل كل مستوى على عدد مختلف من التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="36d24-153">Each level has a different number of details.</span></span>

    ![مستويات متعددة من تنسيق التقارير الإلكترونية، تنسيق لمعرفة المكالمات ذات المعلمات](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="36d24-155">في علامة التبويب **تعيين**، قم بتوسيع عناصر **النموذج** و **البيانات** و **الملخص**.</span><span class="sxs-lookup"><span data-stu-id="36d24-155">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="36d24-156">يقوم مصدر البيانات **Model.Data.Summary** بإرجاع قائمة حركات الضريبة.</span><span class="sxs-lookup"><span data-stu-id="36d24-156">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="36d24-157">يتم تلخيص هذه الحركات حسب كود الضريبة.</span><span class="sxs-lookup"><span data-stu-id="36d24-157">These transactions are summarized by tax code.</span></span> <span data-ttu-id="36d24-158">بالنسبة لمصدر البيانات هذا، تم تكوين الحقل المحسوب **Model.Data.Summary.Level** لإرجاع كود مستوي الضرائب لكل سجل ملخص.</span><span class="sxs-lookup"><span data-stu-id="36d24-158">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="36d24-159">بالنسبة لأي كود ضريبة يمكن استرداده من مصدر البيانات **Model.Data.Summary** في وقت التشغيل، يقوم الحقل المحسوب بإرجاع كود مستوى الضرائب (**العادية** أو **المخفضة** أو **لا شيء** أو **آخر**) كقيمة نص.</span><span class="sxs-lookup"><span data-stu-id="36d24-159">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="36d24-160">يتم استخدام الحقل المحسوب **Model.Data.Summary.Level** لتصفية سجلات مصدر بيانات **Model.Data.Summary**، وأدخل البيانات المصفاة في كل عنصر XML يمثل مستوى ضرائب باستخدام حقول **Model.Data2.Level1**، و **Model.Data2.Level2**، و **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="36d24-160">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![قائمة حركات الضريبة لمصدر البيانات Model.Data.Summary](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="36d24-162">تم تكوين الحقل المحسوب **Model.Data.Summary.Level** بحيث يحتوي على تعبير تقارير إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="36d24-162">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="36d24-163">أكواد الضرائب (**VAT19**، و **InVAT19**، و **VAT7**، و **InVAT7**، و **THIRD**، و **InVAT0**) مشفرة في هذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="36d24-163">Tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="36d24-164">وبالتالي، يعتمد تنسيق التقارير الإلكترونية هذا على الكيان القانوني حيث تم تكوين هذه الأكواد الضريبية.</span><span class="sxs-lookup"><span data-stu-id="36d24-164">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![الحقل Model.Data.Summary.Level المحسوب بأكواد الضرائب المشفرة](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="36d24-166">لدعم مجموعة مختلفة من أكواد الضريبة لكل كيان قانوني، يجب اتباع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="36d24-166">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="36d24-167">قم بإنشاء إصدار مشتق من تنسيق التقارير الإلكترونية لكل كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="36d24-167">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="36d24-168">قم بتحديث أكواد الضريبة في الحقل المحسوب **Model.Data.Summary.Level**، استنادا إلى إعداد الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="36d24-168">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="36d24-169">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-169">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="36d24-170">إنشاء تنسيق مشتق</span><span class="sxs-lookup"><span data-stu-id="36d24-170">Create a derived format</span></span>

<span data-ttu-id="36d24-171">بعد ذلك، ستستخدم ميزه المعلمات الخاصة بالتطبيق الخاص بالتقارير الإلكترونية لدعم مجموعه مختلفة من أكواد الضريبة لكل كيان قانوني بتنسيق تقارير إلكترونية مفرد.</span><span class="sxs-lookup"><span data-stu-id="36d24-171">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="36d24-172">في شجرة التكوين، قم بتوسيع محتويات **نموذج للتعرف على الاستدعاءات ذات معلمات‬**.</span><span class="sxs-lookup"><span data-stu-id="36d24-172">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="36d24-173">حدد الصنف **تنسيق للتعرف على الاستدعاءات ذات معلمات**.</span><span class="sxs-lookup"><span data-stu-id="36d24-173">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="36d24-174">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="36d24-174">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="36d24-175">حدد خيار **اشتقاق من الاسم: تنسيق للتعرف على الاستدعاءات ذات معلمات، Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="36d24-175">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="36d24-176">في حقل **الاسم**، أدخل **تنسيق للتعرف على كيفية البحث عن بيانات الكيان القانوني**.</span><span class="sxs-lookup"><span data-stu-id="36d24-176">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="36d24-177">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="36d24-177">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="36d24-178">تكوين تنسيق مشتق</span><span class="sxs-lookup"><span data-stu-id="36d24-178">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="36d24-179">إضافة تعداد التنسيق</span><span class="sxs-lookup"><span data-stu-id="36d24-179">Add a format enumeration</span></span>

<span data-ttu-id="36d24-180">بعد ذلك، ستقوم باضافه تعداد جديد لتنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="36d24-180">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="36d24-181">سيتم تقديم قيم تعداد التعداد هذا لمستخدمي الاعمال ، والذين سيقومون بتحديد المجموعات التابعة للكيان القانوني لأكواد الضريبة لضرائب المختلفة المستخدمة في تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="36d24-181">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="36d24-182">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="36d24-182">Select **Designer**.</span></span>
2.  <span data-ttu-id="36d24-183">حدد **تعدادات التنسيقات**.</span><span class="sxs-lookup"><span data-stu-id="36d24-183">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="36d24-184">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-184">Select **Add**.</span></span>
4.  <span data-ttu-id="36d24-185">في حقل **الاسم**، أدخل **قائمة مستويات الضرائب**.</span><span class="sxs-lookup"><span data-stu-id="36d24-185">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="36d24-186">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="36d24-186">Select **Save**.</span></span>
6.  <span data-ttu-id="36d24-187">في علامة التبويب **قيم تعداد التنسيقات**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-187">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="36d24-188">في حقل **الاسم**، أدخل **الضرائب العادية**.</span><span class="sxs-lookup"><span data-stu-id="36d24-188">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="36d24-189">حدد **إضافة** مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="36d24-189">Select **Add** again.</span></span>
9.  <span data-ttu-id="36d24-190">في حقل **الاسم**، أدخل **الضرائب المخفضة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-190">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="36d24-191">حدد **إضافة** مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="36d24-191">Select **Add** again.</span></span>
11. <span data-ttu-id="36d24-192">في حقل **الاسم**، أدخل **لا ضرائب**.</span><span class="sxs-lookup"><span data-stu-id="36d24-192">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="36d24-193">حدد **إضافة** مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="36d24-193">Select **Add** again.</span></span>
13. <span data-ttu-id="36d24-194">في حقل **الاسم**، أدخل **آخر**.</span><span class="sxs-lookup"><span data-stu-id="36d24-194">In the **Name** field, enter **Other**.</span></span>

    ![سجل جديد في صفحة تعدادات التنسيقات](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="36d24-196">نظرا لان مستخدمي الاعمال قد يستخدمون لغات مختلفة لتحديد المجموعات التابعة للكيان القانوني ، نوصي بترجمة قيم قائمه التعداد هذه إلى اللغات التي تم تكوينها علي انها اللغات المفضلة لهؤلاء المستخدمين في التمويل.</span><span class="sxs-lookup"><span data-stu-id="36d24-196">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="36d24-197">حدد سجل **لا ضرائب**.</span><span class="sxs-lookup"><span data-stu-id="36d24-197">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="36d24-198">انقر في حقل **التسمية**.</span><span class="sxs-lookup"><span data-stu-id="36d24-198">Click in the **Label** field.</span></span>
16. <span data-ttu-id="36d24-199">حدد **ترجمة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-199">Select **Translate**.</span></span>
17. <span data-ttu-id="36d24-200">في جزء **ترجمة النص**، في حقل **معرف التسمية**، أدخل **LBL_LEVELENUM_NO**.</span><span class="sxs-lookup"><span data-stu-id="36d24-200">In the **Text translation** pane, in the **Label ID** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="36d24-201">في حقل **النص باللغة الافتراضية**، أدخل **لا ضرائب**.</span><span class="sxs-lookup"><span data-stu-id="36d24-201">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="36d24-202">في حقل **اللغة**، حدد **DE**.</span><span class="sxs-lookup"><span data-stu-id="36d24-202">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="36d24-203">في حقل **النص المترجم**، أدخل **keine Besteuerung**.</span><span class="sxs-lookup"><span data-stu-id="36d24-203">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="36d24-204">حدد **ترجمة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-204">Select **Translate**.</span></span>

    ![شريحة ترجمة النص](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="36d24-206">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="36d24-206">Select **Save**.</span></span>
23. <span data-ttu-id="36d24-207">أغلق صفحة **تعدادات التنسيقات**.</span><span class="sxs-lookup"><span data-stu-id="36d24-207">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="36d24-208">إضافة مصدر بيانات بحث جديد</span><span class="sxs-lookup"><span data-stu-id="36d24-208">Add a new lookup data source</span></span>

<span data-ttu-id="36d24-209">بعد ذلك ، تتم أضافه مصدر بيانات جديد لتحديد كيفيه قيام مستخدمي الاعمال بتحديد القواعد القانونية التي تعتمد علي الكيان للتعرف علي مستوي الضرائب الصحيح لكل سجل حركه ملخص.</span><span class="sxs-lookup"><span data-stu-id="36d24-209">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="36d24-210">في علامة تبويب **تعيين**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-210">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="36d24-211">حدد **تعداد التنسيق/البحث**.</span><span class="sxs-lookup"><span data-stu-id="36d24-211">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="36d24-212">لقد قمت للتو بالتعرف علي ان كل قاعده يقوم مستخدمو الاعمال بتحديدها لضرائب علي مستوي التقييم سيقوم بإرجاع قيمه لتعداد تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="36d24-212">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="36d24-213">لاحظ أنه يمكن الوصول إلى نوع مصدر بيانات **البحث** ضمن **نموذج البيانات** وكتل **Dynamics 365 for Operations** بالإضافه إلى كتلة **تعداد التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="36d24-213">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="36d24-214">لذلك، يمكن استخدام التعدادات الخاصة بنموذج بيانات التقارير الإلكترونية و تعدادات التطبيق لتحديد نوع القيم المرتجعة لمصادر البيانات من هذا النوع.</span><span class="sxs-lookup"><span data-stu-id="36d24-214">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that are returned for data sources of that type.</span></span> <span data-ttu-id="36d24-215">لمعرفة المزيد حول مصادر بيانات **البحث**، راجع [تكوين مصادر بيانات البحث لاستخدام ميزة المعلمات الخاصة بتطبيق ER‬](er-lookup-data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="36d24-215">To learn more about the **Lookup** data sources, see [Configure Lookup data sources to use the ER application-specific parameters feature](er-lookup-data-sources.md).</span></span>
    
3.  <span data-ttu-id="36d24-216">في الحقل **الاسم**، أدخل **‏محدد**.</span><span class="sxs-lookup"><span data-stu-id="36d24-216">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="36d24-217">في حقل **تعداد التنسيق**، حدد **قائمة مستويات الضرائب**.</span><span class="sxs-lookup"><span data-stu-id="36d24-217">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="36d24-218">لقد حددت، أنه بالنسبة إلى كل قاعدة محددة في مصدر البيانات هذا، يجب أن يحدد مستخدم الأعمال إحدى قيم تعداد التنسيق **قائمة مستويات الضرائب** كقيمة مرتجعة.</span><span class="sxs-lookup"><span data-stu-id="36d24-218">You specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="36d24-219">حدد **تحرير البحث**.</span><span class="sxs-lookup"><span data-stu-id="36d24-219">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="36d24-220">حدد **الأعمدة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-220">Select **Columns**.</span></span>
7.  <span data-ttu-id="36d24-221">قم بتوسيع عنصر **النموذج**.</span><span class="sxs-lookup"><span data-stu-id="36d24-221">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="36d24-222">قم بتوسيع عنصر **البيانات**.</span><span class="sxs-lookup"><span data-stu-id="36d24-222">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="36d24-223">قم بتوسيع عنصر **الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-223">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="36d24-224">حدد عنصر **Model.Data.Tax.Code**.</span><span class="sxs-lookup"><span data-stu-id="36d24-224">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="36d24-225">حدد الزر **إضافة** (السهم الأيمن).</span><span class="sxs-lookup"><span data-stu-id="36d24-225">Select the **Add** button (the right arrow).</span></span>

    ![شريحة الأعمدة](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="36d24-227">لقد حددت للتو أنه لكل قاعدة تم تحديدها في مصدر البيانات هذا للتعرف على مستوى الضرائب ، يجب على مستخدم النشاط التجاري اختيار أحد الرموز الضريبية كشرط.</span><span class="sxs-lookup"><span data-stu-id="36d24-227">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="36d24-228">سيتم إرجاع قائمه أكواد الضريبة التي يمكن للمستخدم التجاري تحديدها بواسطة مصدر بيانات **Model.Data.Tax**.</span><span class="sxs-lookup"><span data-stu-id="36d24-228">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="36d24-229">نظرا لان مصدر البيانات هذا يحتوي علي حقل **الاسم**، سيتم عرض اسم كود الضريبة لكل قيمه من قيم أكواد الضريبة في البحث الذي يتم تقديمه لمستخدم الاعمال.</span><span class="sxs-lookup"><span data-stu-id="36d24-229">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="36d24-230">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="36d24-230">Select **OK**.</span></span>

    ![صفحة مصمم البحث](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="36d24-232">يمكن لمستخدمي الاعمال أضافه قواعد متعددة كسجلات لمصدر البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="36d24-232">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="36d24-233">يتم ترقيم كل سجل حسب كود البند.</span><span class="sxs-lookup"><span data-stu-id="36d24-233">Each record will be numbered by a line code.</span></span> <span data-ttu-id="36d24-234">سيتم تقييم القواعد بترتيب أسطر متزايد.</span><span class="sxs-lookup"><span data-stu-id="36d24-234">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="36d24-235">ونظرًا لقيامك بتحديد حقل **كود الضريبة** كشرط للقواعد في مصدر بيانات البحث هذا، ونظرًا لإعداد **كود الضريبة** كحقل لنوع بيانات **السلسلة**، سيتم تقييم كل قاعده في وقت التشغيل بمقارنه كود الضريبة الذي يتم تمريره إلى مصدر البيانات مع كود الضريبة المحدد في سجل مصدر البيانات.</span><span class="sxs-lookup"><span data-stu-id="36d24-235">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="36d24-236">عند العثور علي قاعده تفي بالشرط الذي تم تكوينه ، يقوم مصدر البيانات هذا بإرجاع قيمه البحث للقاعدة المحددة في حقل **نتيجة البحث**.</span><span class="sxs-lookup"><span data-stu-id="36d24-236">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="36d24-237">في حاله عدم العثور علي قاعده ، يتم طرح استثناء لاعلام المستخدم بان مصدر البيانات الحالي لا يرجع قيمه صحيحه.</span><span class="sxs-lookup"><span data-stu-id="36d24-237">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="36d24-238">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="36d24-238">Select **Save**.</span></span>
14. <span data-ttu-id="36d24-239">أغلق صفحة **مصمم البحث**.</span><span class="sxs-lookup"><span data-stu-id="36d24-239">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="36d24-240">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="36d24-240">Select **OK**.</span></span>

    <span data-ttu-id="36d24-241">لاحظ انك قمت باضافه مصدر بيانات جديد سيقوم بإرجاع مستوي الضرائب كقيمه لتعداد تنسيق **قائمة مستويات الضرائب** لأي كود ضريبة يتم تمريره إلى مصدر البيانات كوسيطة في معلمة **الكود** لنوع بيانات **السلسلة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-241">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![صفحة مصمم التنسيق بمصدر بيانات جديد](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="36d24-243">تقييم القواعد المكوّنة يعتمد علي نوع بيانات الحقول التي تم تحديدها لتعريف شروط هذه القواعد.</span><span class="sxs-lookup"><span data-stu-id="36d24-243">The evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="36d24-244">عند تحديد حقل تم تكوينه كحقل اما لنوع البيانات **رقمي** أو **تاريخ**، فان المعايير ستختلف عن المعايير الموضحة سابقًا لنوع بيانات **السلسلة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-244">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="36d24-245">بالنسبة للحقلين **رقمي** و **التاريخ**، يجب تحديد القاعدة كنطاق من القيم.</span><span class="sxs-lookup"><span data-stu-id="36d24-245">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="36d24-246">سيتم اعتبار شرط القاعدة مستوفيًا عندما تكون القيمة التي يتم تمريرها إلى مصدر البيانات في النطاق المكوّن.</span><span class="sxs-lookup"><span data-stu-id="36d24-246">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="36d24-247">يبين الرسم التوضيحي التالي مثالاً عن هذا النوع من الإعداد.</span><span class="sxs-lookup"><span data-stu-id="36d24-247">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="36d24-248">بالإضافة إلى حقل **Model.Data.Tax.Code** في نوع بيانات **السلسلة**، يتم استخدام حقل **Model.Tax.Summary.Base** من نوع بيانات **Real** لتحديد شروط مصدر بيانات البحث.</span><span class="sxs-lookup"><span data-stu-id="36d24-248">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![صفحه مصمم البحث مع الاعمده الإضافية](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="36d24-250">نظرًا لأنه يتم تحديد حقلي **Model.Data.Tax.Code** و **Model.Tax.Summary.Base** لمصدر بيانات البحث هذا، سيتم تكوين كل قاعدة من مصدر البيانات بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="36d24-250">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="36d24-251">في القائمة التي تم تقديمها، يجب تحديد قيمة تعداد تنسيق **قائمة مستويات الضرائب** كقيمة مرجعة.</span><span class="sxs-lookup"><span data-stu-id="36d24-251">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="36d24-252">يجب إدخال كود الضريبة كشرط لهذه القاعدة.</span><span class="sxs-lookup"><span data-stu-id="36d24-252">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="36d24-253">لا يمكن تطبيق إلا أكواد الضريبة الموفرة بواسطة مصدر بيانات **Model.Data.Tax**.</span><span class="sxs-lookup"><span data-stu-id="36d24-253">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="36d24-254">يجب إدخال الحد الأدنى والحد الأقصى لقيم المبلغ الأساسي للضريبة كشروط لهذه القاعدة.</span><span class="sxs-lookup"><span data-stu-id="36d24-254">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="36d24-255">فيما يلي كيفيه تقييم كل قاعده من مصدر البيانات هذا في وقت التشغيل:</span><span class="sxs-lookup"><span data-stu-id="36d24-255">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="36d24-256">هل الكود الخاص بنوع بيانات **السلسلة** الذي تم تمريره إلى مصدر البيانات هذا يساوي الكود الضريبي لإحدى القواعد؟</span><span class="sxs-lookup"><span data-stu-id="36d24-256">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="36d24-257">هل تقع قيمه نوع البيانات **الحقيقية** التي تم تمريرها إلى مصدر البيانات هذا بين حد ادني وحد اقصي للقيم المحددة؟</span><span class="sxs-lookup"><span data-stu-id="36d24-257">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="36d24-258">سيتم اعتبار القاعدة قابله للتطبيق عند الوفاء بكلٍّ من الشرطين.</span><span class="sxs-lookup"><span data-stu-id="36d24-258">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="36d24-259">ترجمه تسميه مصدر بيانات البحث الذي تمت إضافته</span><span class="sxs-lookup"><span data-stu-id="36d24-259">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="36d24-260">نظرًا لأن مستخدمي الأعمال قد يستخدمون لغات مختلفة لتحديد مجموعات الرموز الضريبية المعتمدة على الكيان القانوني ، فإننا نوصي بترجمة تسمية أي مصدر بيانات بحث تضيفه ، بحيث يتم تقديمه بلغة كل مستخدم المفضلة على الصفحة المقابلة.</span><span class="sxs-lookup"><span data-stu-id="36d24-260">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="36d24-261">حدد مصدر بيانات **Model.Data.Selector**.</span><span class="sxs-lookup"><span data-stu-id="36d24-261">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="36d24-262">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="36d24-262">Select **Edit**.</span></span>
3.  <span data-ttu-id="36d24-263">انقر في حقل **التسمية**.</span><span class="sxs-lookup"><span data-stu-id="36d24-263">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="36d24-264">حدد **ترجمة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-264">Select **Translate**.</span></span>
5.  <span data-ttu-id="36d24-265">في جزء **ترجمة النص**، في حقل **معرف التسمية**، أدخل **LBL_SELECTOR_DS**.</span><span class="sxs-lookup"><span data-stu-id="36d24-265">In the **Text translation** pane, in the **Label ID** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="36d24-266">في حقل **النص باللغة الافتراضية**، أدخل **تحديد مستوي الضريبة حسب كود الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-266">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="36d24-267">في حقل **اللغة**، حدد **DE**.</span><span class="sxs-lookup"><span data-stu-id="36d24-267">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="36d24-268">في حقل **النص المترجم**، أدخل **Steuerebene für Steuerkennzeichen auswählen**.</span><span class="sxs-lookup"><span data-stu-id="36d24-268">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="36d24-269">حدد **ترجمة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-269">Select **Translate**.</span></span>
10. <span data-ttu-id="36d24-270">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="36d24-270">Select **OK**.</span></span>

    ![شريحة خصائص مصدر البيانات](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="36d24-272">إضافة حقل جديد لاستخدام البحث المكون</span><span class="sxs-lookup"><span data-stu-id="36d24-272">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="36d24-273">قم بتوسيع عنصر **Model.Data**.</span><span class="sxs-lookup"><span data-stu-id="36d24-273">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="36d24-274">حدد عنصر **Model.Data.Summary**.</span><span class="sxs-lookup"><span data-stu-id="36d24-274">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="36d24-275">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-275">Select **Add**.</span></span>
4.  <span data-ttu-id="36d24-276">حدد **الوظائف/الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="36d24-276">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="36d24-277">في حقل **الاسم**، أدخل **LevelByLookup**.</span><span class="sxs-lookup"><span data-stu-id="36d24-277">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="36d24-278">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-278">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="36d24-279">في **حقل المعادلة**، أدخل **Model.Selector(Model.Data.Summary.Code)**.</span><span class="sxs-lookup"><span data-stu-id="36d24-279">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="36d24-280">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="36d24-280">Select **Save**.</span></span>

    ![إضافة Model.Selector (Model.Data.Summary.Code) إلى صفحة مصمم الصيغة](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="36d24-282">أغلق صفحة **محرر المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-282">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="36d24-283">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="36d24-283">Select **OK**.</span></span>

    ![تنسيق الصفحة مع إضافة صيغة جديدة](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="36d24-285&quot;>لاحظ أن الحقل المحسوب **LevelByLookup** الذي قمت بإضافته سيقوم بإرجاع مستوى الضرائب باعتباره قيمة تعداد تنسيق **قائمة مستويات الضرائب** لكل سجل حركات ضريبة ملخصة.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-285&quot;>Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id=&quot;36d24-286&quot;>سيتم تمرير كود الضريبة للسجل إلى مصدر بيانات بحث **Model.Selector**، وسيتم استخدام مجموعه القواعد الخاصة بمصدر البيانات هذا لتحديد مستوي الضرائب الصحيح.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-286&quot;>The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name=&quot;add-a-new-format-enumeration-based-data-source&quot;></a><span data-ttu-id=&quot;36d24-287&quot;>إضافة مصدر بيانات جديد مستند إلى تعداد التنسيق</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-287&quot;>Add a new format enumeration-based data source</span></span>

<span data-ttu-id=&quot;36d24-288&quot;>بعد ذلك ، ستقوم باضافه مصدر بيانات جديد يشير إلى تعداد التنسيق الذي قمت بإضافته سابقا.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-288&quot;>Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id=&quot;36d24-289&quot;>سيتم استخدام قيم مصدر البيانات هذا في تعبير تنسيق التقارير الإلكترونية لاحقا.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-289&quot;>Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id=&quot;36d24-290&quot;>حدد **إضافة جذر**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-290&quot;>Select **Add root**.</span></span>
2.  <span data-ttu-id=&quot;36d24-291&quot;>حدد **تعدادات التنسيقات/التعداد**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-291&quot;>Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id=&quot;36d24-292&quot;>في حقل **الاسم**، أدخل **TaxationLevel**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-292&quot;>In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id=&quot;36d24-293&quot;>في حقل **تعداد التنسيق**، حدد **قائمة مستويات الضرائب**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-293&quot;>In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id=&quot;36d24-294&quot;>حدد **حفظ**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-294&quot;>Select **Save**.</span></span>

### <a name=&quot;modify-an-existing-field-to-start-to-use-the-lookup&quot;></a><span data-ttu-id=&quot;36d24-295&quot;>تعديل حقل موجود لبدء استخدام البحث</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-295&quot;>Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id=&quot;36d24-296&quot;>بعد ذلك، ستقوم بتعديل الحقل المحسوب الموجود بحيث يستخدم مصدر بيانات البحث الذي تم تكوينه لإرجاع قيمه مستوي الضرائب الصحيح، وفقا لكود الضريبة.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-296&quot;>Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id=&quot;36d24-297&quot;>حدد عنصر **Model.Data.Summary.Level**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-297&quot;>Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id=&quot;36d24-298&quot;>حدد **تحرير**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-298&quot;>Select **Edit**.</span></span>
3.  <span data-ttu-id=&quot;36d24-299&quot;>حدد **تحرير المعادلة**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-299&quot;>Select **Edit formula**.</span></span>

    <span data-ttu-id=&quot;36d24-300&quot;>لاحظ أن التعبير الحالي الخاص بحقل **Model.Data.Summary.Level** يتضمن أكواد الضريبة التالية المضمنة:</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;36d24-300&quot;>Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id=&quot;36d24-301&quot;>CASE (@.Code، &quot;VAT19&quot;، &quot;العادي&quot;, &quot;InVAT19&quot;، &quot;العادية&quot;, &quot;VAT7&quot;، &quot;المخفضة&quot;, &quot;InVAT7&quot;، &quot;المخفضة&quot;, &quot;THIRD&quot;، &quot;لا شيء&quot;، &quot;InVAT0&quot;، &quot;لا شيء&quot;, &quot;آخر")</span><span class="sxs-lookup"><span data-stu-id="36d24-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="36d24-302">في حقل **المعادلة**، أدخل **CASE(@.LevelByLookup، TaxationLevel.'Regular taxation', "العادية", TaxationLevel.'Reduced taxation'، "المخفضة", TaxationLevel.'No taxation'، "لا شيء", "آخر")**.</span><span class="sxs-lookup"><span data-stu-id="36d24-302">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![صفحة مصمم تشغيل التقارير الإلكترونية](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="36d24-304">لاحظ أن التعبير الخاص بحقل **Model.Data.Summary.Level** سيقوم الآن بإرجاع مستوى الضرائب، استنادًا إلى كود الضريبة الخاص بالسجل الحالي ومجموعة القواعد التي يقوم مستخدم الأعمال بتكوينها في مصدر بيانات البحث **Model.Data.Selector**.</span><span class="sxs-lookup"><span data-stu-id="36d24-304">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="36d24-305">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="36d24-305">Select **Save**.</span></span>
6.  <span data-ttu-id="36d24-306">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-306">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="36d24-307">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="36d24-307">Select **OK**.</span></span>
8.  <span data-ttu-id="36d24-308">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="36d24-308">Select **Save**.</span></span>
9.  <span data-ttu-id="36d24-309">أغلق صفحة **مصمم التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="36d24-309">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="36d24-310">إكمال إصدار المسودة لتنسيق مشتق</span><span class="sxs-lookup"><span data-stu-id="36d24-310">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="36d24-311">في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="36d24-311">On the **Versions** FastTab, select **Change status**.</span></span>
2.  <span data-ttu-id="36d24-312">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="36d24-312">Select **Complete**.</span></span>
3.  <span data-ttu-id="36d24-313">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="36d24-313">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="36d24-314">تصدير الإصدار المكتمل لتنسيق معدل</span><span class="sxs-lookup"><span data-stu-id="36d24-314">Export completed version of modified format</span></span>

1.  <span data-ttu-id="36d24-315">في شجره التكوين، حدد عنصر **تنسيق للتعرف على كيفية البحث عن بيانات الكيان القانوني**.</span><span class="sxs-lookup"><span data-stu-id="36d24-315">In the configuration tree, select the **Format to learn how to look up LE data** item.</span></span>
2.  <span data-ttu-id="36d24-316">في علامة التبويب السريعة **الإصدارات**، حدد السجل الذي بحالة **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="36d24-316">On the **Versions** FastTab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="36d24-317">حدد **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="36d24-317">Select **Exchange**.</span></span>
4.  <span data-ttu-id="36d24-318">حدد **تصدير كملف XML**.</span><span class="sxs-lookup"><span data-stu-id="36d24-318">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="36d24-319">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="36d24-319">Select **OK**.</span></span>
6.  <span data-ttu-id="36d24-320">يقوم مستعرض الويب بتنزيل ملف **تنسيق للتعرف على كيفية البحث عن data.xml للكيان القانوني**.</span><span class="sxs-lookup"><span data-stu-id="36d24-320">The web browser downloads a **Format to learn how to look up LE data.xml** file.</span></span> <span data-ttu-id="36d24-321">قم بتخزين هذا الملف محليا.</span><span class="sxs-lookup"><span data-stu-id="36d24-321">Store this file locally.</span></span>

<span data-ttu-id="36d24-322">كرر الخطوات الموجودة في هذا القسم للعناصر الأصلية لتنسيق **تنسيق للتعرف على كيفية البحث عن بيانات الكيان القانوني**، وقم بتخزين الملفات التالية محليًا:</span><span class="sxs-lookup"><span data-stu-id="36d24-322">Repeat steps in this section for parent items of the **Format to learn how to look up LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="36d24-323">تنسيق للتعرف على الاستدعاءات ذات معلمات.xml</span><span class="sxs-lookup"><span data-stu-id="36d24-323">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="36d24-324">تعيين للتعرف على الاستدعاءات ذات معلمات.xml</span><span class="sxs-lookup"><span data-stu-id="36d24-324">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="36d24-325">النموذج للتعرف على الاستدعاءات ذات معلمات.xml</span><span class="sxs-lookup"><span data-stu-id="36d24-325">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="36d24-326">لمعرفه كيفيه استخدام تنسيق التقارير الإلكترونية المكون **تنسيق للتعرف على كيفية البحث عن بيانات الكيان القانوني** لإعداد المجموعات المعتمدة للكيانات القانونية لتصفيه حركات الضريبة من خلال مستويات ضرائب مختلفة، أكمل الخطوات الواردة في موضوع [إعداد معلمات تنسيق التقارير الإلكترونية للكيان القانوني](er-app-specific-parameters-set-up.md).</span><span class="sxs-lookup"><span data-stu-id="36d24-326">To learn how to use the configured **Format to learn how to look up LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36d24-327">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="36d24-327">Additional resources</span></span>

[<span data-ttu-id="36d24-328">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="36d24-328">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="36d24-329">إعداد معلمات تنسيق التقارير الإلكترونية لكل كيان قانوني</span><span class="sxs-lookup"><span data-stu-id="36d24-329">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)

[<span data-ttu-id="36d24-330">تكوين مصادر بيانات البحث لاستخدام ميزة المعلمات الخاصة بتطبيق ER</span><span class="sxs-lookup"><span data-stu-id="36d24-330">Configure Lookup data sources to use the ER application-specific parameters feature</span></span>](er-lookup-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
