---
title: تكوين تعيينات نماذج التقارير الإلكترونية التابعة لسياقات البلدان
description: يشرح هذا الموضوع كيفيه اعداد تعيينات نماذج التقارير الإلكترونية لكي تعتمد علي سياق البلد/المنطقة الخاص بالكيان القانوني الذي يتحكم في استخدامه.
author: NickSelin
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: 48d2e3c81d038cc55f6f100f3081561506946199
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562276"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a><span data-ttu-id="0dfea-103">تكوين تعيينات نماذج التقارير الإلكترونية التابعة لسياقات البلدان</span><span class="sxs-lookup"><span data-stu-id="0dfea-103">Configure country context dependent ER model mappings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0dfea-104">يمكنك تكوين تعيينات نماذج التقارير الكترونيه (ER) بحيث تقوم بتطبيق نموذج بيانات تقارير إلكترونية عام ولكنه خاص بـ Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="0dfea-104">You can configure Electronic reporting (ER) model mappings so that they implement a generic ER data model but are specific to Dynamics 365 Finance.</span></span> <span data-ttu-id="0dfea-105">يشرح هذا الموضوع كيفيه تصميم تعيينات نماذج تقارير إلكترونية متعددة لنموذج بيانات تقرير إلكترونية للتحكم في كيفيه استخدامها بواسطة تنسيقات التقارير الإلكترونية المقابلة التي يتم تشغيلها من الشركات التي لها سياقات بلد/منطقه مختلفه.</span><span class="sxs-lookup"><span data-stu-id="0dfea-105">This topic explains how to design multiple ER model mappings for an ER data model to control how they are used by corresponding ER formats that are run from companies that have different country/region contexts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0dfea-106">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="0dfea-106">Prerequisites</span></span>

<span data-ttu-id="0dfea-107">لإكمال الأمثلة في هذا الموضوع، يجب أن يكون لديك الوصول التالي:</span><span class="sxs-lookup"><span data-stu-id="0dfea-107">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="0dfea-108">الوصول إلى Finance لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="0dfea-108">Access to Finance for one of the following roles:</span></span>
    - <span data-ttu-id="0dfea-109">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="0dfea-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="0dfea-110">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="0dfea-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="0dfea-111">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="0dfea-111">System administrator</span></span>

- <span data-ttu-id="0dfea-112">يمكنك الوصول إلى مثيل خدمات التكوين التنظيمية (RCS) التي تم توفيرها لنفس المستأجر مثل التمويل لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="0dfea-112">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>
    - <span data-ttu-id="0dfea-113">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="0dfea-113">Electronic reporting developer</span></span>
    - <span data-ttu-id="0dfea-114">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="0dfea-114">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="0dfea-115">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="0dfea-115">System administrator</span></span>

<span data-ttu-id="0dfea-116">تتطلب بعض الخطوات الواردة في هذا الموضوع تنفيذ تنسيق تقارير إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0dfea-116">Some steps in this topic require execution of an ER format.</span></span> <span data-ttu-id="0dfea-117">في بعض الحالات، يتاثر تنفيذ التنسيق الخاص بالتقارير الإلكترونية بسياق البلد/المنطقة للشركة التي تقوم بتسجيل الدخول إليها حاليا.</span><span class="sxs-lookup"><span data-stu-id="0dfea-117">In some cases, execution of an ER format is affected by the country/region context of the company that you're currently signed in to.</span></span> <span data-ttu-id="0dfea-118">يمكنك تشغيل تنسيق التقارير الإلكترونية في مثيل RCS الحالي إذا كانت الشركة التي لها سياق البلد/المنطقة المطلوب متوفرة في RCS.</span><span class="sxs-lookup"><span data-stu-id="0dfea-118">You can run an ER format in the current RCS instance if the company that has the required country/region context is available in RCS.</span></span> <span data-ttu-id="0dfea-119">وبخلاف ذلك، يجب تحميل إصدار مكتمل من تعيين نموذج التقارير الإلكترونية وتكوينات تنسيق التقارير الإلكترونية التي تستخدم نموذج البيانات التقارير الإلكترونية إلى مثيل التمويل الخاص بك، ثم قم بتشغيل تنسيق التقارير الإلكترونية في مثيل التمويل هذا.</span><span class="sxs-lookup"><span data-stu-id="0dfea-119">Otherwise, you must upload a completed version of the ER model mapping and ER format configurations that use the ER data model to your Finance instance, and then run the ER format in that Finance instance.</span></span> <span data-ttu-id="0dfea-120">للحصول علي معلومات حول كيفيه استيراد التكوينات التي توجد في RCS إلى مثيل تمويل، راجع [استيراد التكوينات من RCS](rcs-download-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="0dfea-120">For information about how to import configurations that reside in RCS into a Finance instance, see [Import configurations from RCS](rcs-download-configurations.md).</span></span>

## <a name="single-model-mapping-case"></a><span data-ttu-id="0dfea-121">حاله تعيين نموذج واحد</span><span class="sxs-lookup"><span data-stu-id="0dfea-121">Single model mapping case</span></span>

<span data-ttu-id="0dfea-122">اتبع الخطوات الواردة في [الملحق 1](#appendix1) من هذا الموضوع لتصميم مكونات التقارير الإلكترونية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-122">Follow the steps in [Appendix 1](#appendix1) of this topic to design the required ER components.</span></span> <span data-ttu-id="0dfea-123">لديك الآن تكوين تعيين نموذج **التعيين (عام)** الذي يحتوي على تعيين النموذج لتعريف **نقطة الإدخال 1**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-123">You now have the **Mapping (General)** model mapping configuration that contains the model mapping for the **Entry point 1** definition.</span></span>

![صفحة تكوينات التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="0dfea-125">تشغيل التنسيق المكوَّن</span><span class="sxs-lookup"><span data-stu-id="0dfea-125">Run the configured format</span></span>

1.  <span data-ttu-id="0dfea-126">في **صفحة التكوينات**، في علامة التبويب السريع **الإصدارات**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-126">On the **Configurations page**, on the **Versions** FastTab, select **Run**.</span></span>
2.  <span data-ttu-id="0dfea-127">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-127">Select **OK**.</span></span>

<span data-ttu-id="0dfea-128">لاحظ أن مستعرض الويب يعرض تنزيل الملف النصي الذي تم إنشاؤه بواسطة تنسيق التقارير الإلكترونية الذي تم تنفيذه.</span><span class="sxs-lookup"><span data-stu-id="0dfea-128">Notice that the web browser offers to download the text file that was generated by executed ER format.</span></span> <span data-ttu-id="0dfea-129">بسبب تكوين هذا التنسيق لاستخدام **تعريف نقطه الإدخال 1**، وتعيين نموذج واحد فقط متوفر حاليا للنموذج الأساسي الذي يحتوي علي تعيين لهذا التعريف ، فان تنسيق التقارير الإلكترونية الذي تم تنفيذه استخدم تعيين نموذج **التعيين (عام)** لتكوين **التعيين (عام)** كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="0dfea-129">Because this format was configured to use the **Entry point 1** definition, and only a single model mapping is currently available for the base model that contains a mapping for this definition, the executed ER format used the **Mapping (General)** model mapping of the **Mapping (General)** configuration as a data source.</span></span> <span data-ttu-id="0dfea-130">لذلك ، يحتوي الملف الذي تم تنزيله علي **نص الوظيفة العامة 1**</span><span class="sxs-lookup"><span data-stu-id="0dfea-130">Therefore, the downloaded file contains the **Generic functionality 1** text.</span></span>

## <a name="multiple-shared-model-mappings-case"></a><span data-ttu-id="0dfea-131">حاله تعيينات متعددة النماذج المشتركة</span><span class="sxs-lookup"><span data-stu-id="0dfea-131">Multiple shared model mappings case</span></span>

<span data-ttu-id="0dfea-132">اتبع الخطوات الواردة في [الملحق 2](#appendix2) من هذا الموضوع لتصميم مكونات التقارير الإلكترونية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-132">Follow the steps in [Appendix 2](#appendix2) of this topic to design the required ER components.</span></span> <span data-ttu-id="0dfea-133">لديك الآن تكوينات تعيين نموذج **التعيين (عام)** و **التعيين المخصص (عام)**، والتي يحتوي كل منها على تعيين النموذج لتعريف **نقطة الإدخال 1**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-133">You now have **Mapping (General)** and **Mapping (General) custom** model mapping configurations, each of which contains the model mapping for the **Entry point 1** definition.</span></span>

![صفحة تكوينات التقارير الإلكترونية](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="0dfea-135">تشغيل التنسيق المكوَّن</span><span class="sxs-lookup"><span data-stu-id="0dfea-135">Run the configured format</span></span>

1.  <span data-ttu-id="0dfea-136">في صفحة **التكوينات**، في شجرة التكوينات، حدد عنصر **التنسيق للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-136">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="0dfea-137">في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-137">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="0dfea-138">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-138">Select **OK**.</span></span>

<span data-ttu-id="0dfea-139">لاحظ ان تنفيذ تنسيق التقارير الإلكترونية المحدد غير ناجح.</span><span class="sxs-lookup"><span data-stu-id="0dfea-139">Notice that execution of the selected ER format is unsuccessful.</span></span> <span data-ttu-id="0dfea-140">تظهر رسالة خطا لاعلامك بوجود أكثر من تعيين نموذج واحد لنموذج **النموذج للتعرف على التعيينات** وتعريف **نقطة الإخال 1** في **التعيين (عام)** وتكوينات تعيين نموذج **التعيين المخصص (عام)**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-140">An error message informs you that more than one model mapping exists for the **Model to learn mappings** model and the **Entry point 1** definition in the **Mapping (General)** and **Mapping (General) custom** model mapping configurations.</span></span> <span data-ttu-id="0dfea-141">وتوصي الرسالة أيضا بتحديد أحد هذه التكوينات كتكوين افتراضي.</span><span class="sxs-lookup"><span data-stu-id="0dfea-141">The message also recommends that you select one of those configurations as the default configuration.</span></span>

![صفحة تكوينات التقارير الإلكترونية](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a><span data-ttu-id="0dfea-143">تحديد تكوين افتراضي للتعيين</span><span class="sxs-lookup"><span data-stu-id="0dfea-143">Define a default mapping configuration</span></span>

<span data-ttu-id="0dfea-144">اتبع الخطوات التالية **لتعريف تكوين تعيين** نموذج مخصص (عام) كتكوين افتراضي ، بحيث يمكن استخدام التعيينات الخاصة بها كمصادر بيانات للتنسيق الذي يمكن من خلاله **التعرف علي تنسيق التعيينات** ل ER.</span><span class="sxs-lookup"><span data-stu-id="0dfea-144">Follow these steps to define the **Mapping (General) custom** model mapping configuration as the default configuration, so that its mappings can be used as data sources for the **Format to learn mappings** ER format.</span></span>

1.  <span data-ttu-id="0dfea-145">في صفحة **التكوينات**، في شجرة التكوينات، حدد **التعيين المخصص (عام)**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-145">On the **Configurations** page, in the configurations tree, select **Mapping (General) custom**.</span></span>
2.  <span data-ttu-id="0dfea-146">حسب الحاجة، حدد **تحرير** لتجعل الصفحة الحالية جاهزه للتحرير.</span><span class="sxs-lookup"><span data-stu-id="0dfea-146">As required, select **Edit** to make the current page ready for editing.</span></span>
3.  <span data-ttu-id="0dfea-147">قم بتعيين الخيار **الاعداد الافتراضي لتعيين النموذج** إلى **نعم.**</span><span class="sxs-lookup"><span data-stu-id="0dfea-147">Set the **Default for model mapping** option to **Yes**.</span></span>
4.  <span data-ttu-id="0dfea-148">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-148">Select **Save**.</span></span>

![صفحة تكوينات التقارير الإلكترونية](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="0dfea-150">تشغيل التنسيق المكوَّن</span><span class="sxs-lookup"><span data-stu-id="0dfea-150">Run the configured format</span></span>

1.  <span data-ttu-id="0dfea-151">في صفحة **التكوينات**، في شجرة التكوينات، حدد عنصر **التنسيق للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-151">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="0dfea-152">في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-152">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="0dfea-153">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-153">Select **OK**.</span></span>

<span data-ttu-id="0dfea-154">لاحظ ان تنفيذ تنسيق التقارير الإلكترونية المحدد ناجح.</span><span class="sxs-lookup"><span data-stu-id="0dfea-154">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="0dfea-155">مستعرض الويب يعرض تنزيل الملف النصي الذي تم إنشاؤه بواسطة تنسيق التقارير الإلكترونية الذي تم تنفيذه.</span><span class="sxs-lookup"><span data-stu-id="0dfea-155">The web browser offers to download the text file that was generated by executed ER format.</span></span> <span data-ttu-id="0dfea-156">بسبب تكوين هذا التنسيق لاستخدام تعريف **نقطة الإدخال 1**، تم تحديد تكوين تعيين نموذج **التعيين المخصص (عام)** باعتباره التكوين الافتراضي، واستخدم تنسيق التقارير الإلكترونية المنفذ تعيين نموذج **نسخة التعيين (عام)** لتكوين **التعيين المخصص** كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="0dfea-156">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (General) custom** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (General) copy** model mapping of the **Mapping (General) custom** configuration as a data source.</span></span> <span data-ttu-id="0dfea-157">لذلك، يحتوي الملف الذي تم تنزيله على **الوظيفة العامة المخصصة 1**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-157">Therefore, the downloaded file contains the **Generic functionality 1 custom** text.</span></span>

> [!NOTE]
> <span data-ttu-id="0dfea-158">إذا قمت بتغيير الشركة التي قمت بتسجيل الدخول اليها حاليا وتشغيل تنسيق التقارير الإلكترونية هذا مره أخرى ، ستحصل علي نفس المحتوي في الملف الذي تم إنشاؤه ، لان تكوين تعيين نموذج التقارير الإكترونية الافتراضي لا يحتوي علي إيه قيود تعتمد علي الشركة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-158">If you change the company that you're currently signed in to and run this ER format again, you get the same content in the generated file, because the default ER model mapping configuration doesn't contain any company-dependent restrictions.</span></span>

## <a name="multiple-mixed-model-mappings-case"></a><span data-ttu-id="0dfea-159">حاله تعيينات متعددة النماذج المختلطة</span><span class="sxs-lookup"><span data-stu-id="0dfea-159">Multiple mixed model mappings case</span></span>

<span data-ttu-id="0dfea-160">اتبع الخطوات الواردة في [الملحق 3](#appendix3) من هذا الموضوع لتصميم مكونات التقارير الإلكترونية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-160">Follow the steps in [Appendix 3](#appendix3) of this topic to design the required ER components.</span></span> <span data-ttu-id="0dfea-161">لديك الآن تكوينات **التعيين (عام)**، و **التعيين المخصص (عام)**، و **تعيين نموذج التعيين (FR)** التي تحتوي على تعيين النموذج لتعريف **نقطة الإدخال 1**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-161">You now have **Mapping (General)**, **Mapping (General) custom**, and **Mapping (FR) model mapping** configurations that contain the model mapping for the **Entry point 1** definition.</span></span>

<span data-ttu-id="0dfea-162">لاحظ ان الإصدار 1 من تكوين تعيين النموذج **التعيين (FR)** تم تكوينه بحيث يتم تطبيقه فقط علي تنسيقات التقارير الإلكترونية لنموذج **النموذج للتعرف على التعيينات** الذي يعمل في شركات Finance التي لها سياق بلد/منطقه فرنسية.</span><span class="sxs-lookup"><span data-stu-id="0dfea-162">Notice that version 1 of the **Mapping (FR)** model mapping configuration is configured so that it applies only to ER formats of the **Model to learn mappings** model that are run in Finance companies that have French country/region context.</span></span>

![صفحة تكوينات التقارير الإلكترونية](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="0dfea-164">تشغيل التنسيق المكوَّن</span><span class="sxs-lookup"><span data-stu-id="0dfea-164">Run the configured format</span></span>

1.  <span data-ttu-id="0dfea-165">قم بتغيير الشركة إلى **FRSI**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-165">Change the company to **FRSI**.</span></span>
2.  <span data-ttu-id="0dfea-166">في صفحة **التكوينات**، في شجرة التكوينات، حدد عنصر **التنسيق للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-166">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
3.  <span data-ttu-id="0dfea-167">في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-167">On the **Versions** FastTab, select **Run**.</span></span>
4.  <span data-ttu-id="0dfea-168">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-168">Select **OK**.</span></span>

<span data-ttu-id="0dfea-169">لاحظ ان تنفيذ تنسيق التقارير الإلكترونية المحدد ناجح.</span><span class="sxs-lookup"><span data-stu-id="0dfea-169">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="0dfea-170">مستعرض الويب يعرض تنزيل الملف النصي الذي تم إنشاؤه بواسطة تنسيق التقارير الإلكترونية الذي تم تنفيذه.</span><span class="sxs-lookup"><span data-stu-id="0dfea-170">The web browser offers to download the text file that was generated by the executed ER format.</span></span> <span data-ttu-id="0dfea-171">بسبب تكوين هذا التنسيق لاستخدام تعريف **نقطة الإدخال 1**، تم تحديد تكوين تعيين نموذج **التعيين المخصص (عام)** باعتباره التكوين الافتراضي، واستخدم تنسيق التقارير الإلكترونية المنفذ تعيين نموذج **نسخة التعيين (عام)** لتكوين **التعيين المخصص** كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="0dfea-171">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (General) custom** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (General) copy** model mapping of the **Mapping (General) custom** configuration as a data source.</span></span> <span data-ttu-id="0dfea-172">لذلك، يحتوي الملف الذي تم تنزيله على **الوظيفة العامة المخصصة 1**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-172">Therefore, the downloaded file contains the **Generic functionality 1 custom** text.</span></span>

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a><span data-ttu-id="0dfea-173">حدد تكوين التعيين الخاص بفرنسا كتكوين افتراضي</span><span class="sxs-lookup"><span data-stu-id="0dfea-173">Define the France-specific mapping configuration as the default configuration</span></span>

<span data-ttu-id="0dfea-174">اتبع الخطوات التالية لتحديد تكوين تعيين نموذج **التعيين (FR)** باعتباره التكوين الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="0dfea-174">Follow these steps to define the custom **Mapping (FR)** model mapping configuration as the default configuration.</span></span> <span data-ttu-id="0dfea-175">لاحظ انه نظرا لان هذا التعيين مخصص لفرنسا، فانه سيتم اعتباره التعيين الافتراضي بين كافة تكوينات تعيينات النماذج التي تشتمل على كود البلد **FR** في حقل **أكواد البلد/المنطقة ISO**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-175">Note that, because this mapping is specific to France, it will be considered the default mapping between all model mapping configurations that have the **FR** country code specified in the **ISO country/region codes** field.</span></span>

1.  <span data-ttu-id="0dfea-176">في صفحة **التكوينات**، في شجرة التكوينات، حدد **التعيين (FR)**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-176">On the **Configurations** page, in the configurations tree, select **Mapping (FR)**.</span></span>
2.  <span data-ttu-id="0dfea-177">حسب الحاجة، حدد **تحرير** لتجعل الصفحة الحالية جاهزه للتحرير.</span><span class="sxs-lookup"><span data-stu-id="0dfea-177">As required, select **Edit** to make the current page ready for editing.</span></span>
3.  <span data-ttu-id="0dfea-178">قم بتعيين الخيار **الاعداد الافتراضي لتعيين النموذج** إلى **نعم.**</span><span class="sxs-lookup"><span data-stu-id="0dfea-178">Set the **Default for model mapping** option to **Yes**.</span></span>
4.  <span data-ttu-id="0dfea-179">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-179">Select **Save**.</span></span>

![صفحة تكوينات التقارير الإلكترونية](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="0dfea-181">تشغيل التنسيق المكوَّن</span><span class="sxs-lookup"><span data-stu-id="0dfea-181">Run the configured format</span></span>

1.  <span data-ttu-id="0dfea-182">في صفحة **التكوينات**، في شجرة التكوينات، حدد عنصر **التنسيق للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-182">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="0dfea-183">في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-183">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="0dfea-184">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-184">Select **OK**.</span></span>

<span data-ttu-id="0dfea-185">لاحظ ان تنفيذ تنسيق التقارير الإلكترونية المحدد ناجح.</span><span class="sxs-lookup"><span data-stu-id="0dfea-185">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="0dfea-186">مستعرض الويب يعرض تنزيل الملف النصي الذي تم إنشاؤه بواسطة تنسيق التقارير الإلكترونية الذي تم تنفيذه.</span><span class="sxs-lookup"><span data-stu-id="0dfea-186">The web browser offers to download the text file that was generated by the executed ER format.</span></span> <span data-ttu-id="0dfea-187">بسبب تكوين هذا التنسيق لاستخدام تعريف **نقطة الإدخال 1**، تم تحديد تكوين تعيين نموذج **التعيين (FR)** باعتباره التكوين الافتراضي، واستخدم تنسيق التقارير الإلكترونية المنفذ تعيين نموذج **التعيين (FR)** لتكوين **التعيين (FR)** كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="0dfea-187">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (FR)** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (FR)** model mapping of the **Mapping (FR)** configuration as a data source.</span></span> <span data-ttu-id="0dfea-188">لذلك ، يحتوي الملف الذي تم تنزيله علي **وظيفة FR 1**</span><span class="sxs-lookup"><span data-stu-id="0dfea-188">Therefore, the downloaded file contains the **FR functionality 1** text.</span></span>

> [!NOTE]
> <span data-ttu-id="0dfea-189">في حاله تغيير الشركة التي قمت بتسجيل الدخول اليها حاليا وتشغيل تنسيق التقارير الإلكترونية هذا مره أخرى ، سيعتمد الإخراج علي سياق البلد/المنطقة الخاص بالشركة المحددة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-189">If you change the company that you're currently signed in to and run this ER format again, the output will depend on the country/region context of the selected company.</span></span>

## <a name="other-model-mapping-cases"></a><span data-ttu-id="0dfea-190">حاله تعيينات النماذج الأخرى</span><span class="sxs-lookup"><span data-stu-id="0dfea-190">Other model mapping cases</span></span>

<span data-ttu-id="0dfea-191">وكما شاهدت، فان تحديد تعيين النموذج لتنفيذ تنسيق التقارير الإلكترونية يعمل بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="0dfea-191">As you've seen, the selection of a model mapping for the execution of an ER format works in the following way:</span></span>

- <span data-ttu-id="0dfea-192">يتم تحديد تعريف تعيين النموذج الذي يستخدمه تنسيق التقارير الإلكترونية **(نقطه الإدخال 1** في الأمثله الموجودة في هذا الموضوع).</span><span class="sxs-lookup"><span data-stu-id="0dfea-192">The model mapping definition that an ER format uses is specified (**Entry point 1** in the examples in this topic).</span></span>
- <span data-ttu-id="0dfea-193">يمكن استخدام كافة تكوينات التعيين التي تحتوي على تعيين لديه التعريف المحدد، والتي تفي بقيود سياق البلد/المنطقة التي تم تكوينها لتشغيل تنسيق التقارير الإلكترونية (**التعيين (عام)**، و **التعيين المخصص (عام)**، و **التعيين (FR)** في الأمثله الواردة في هذا الموضوع).</span><span class="sxs-lookup"><span data-stu-id="0dfea-193">All mapping configurations that contain a mapping that has the specified definition, and that satisfy any country/region context restrictions that are configured, can potentially be used to run the ER format (**Mapping (General)**, **Mapping (General) custom**, and **Mapping (FR)** in the examples in this topic).</span></span>
- <span data-ttu-id="0dfea-194">ويكون لأي تعيين نموذج افتراضي له قيود علي سياق البلد/المنطقة أعلى أولوية للتحديد (**التعيين (FR)** في الأمثله الموجودة في هذا الموضوع).</span><span class="sxs-lookup"><span data-stu-id="0dfea-194">Any default model mapping that has country/region context restrictions has the highest priority for selection (**Mapping (FR)** in the examples in this topic).</span></span>
- <span data-ttu-id="0dfea-195">ويكون لأي تعيين نموذج افتراضي لا يشتمل على قيود سياق البلد/المنطقة الأولوية الأعلى التالية (**التعيين المخصص (عام)** في الأمثله الموجودة في هذا الموضوع).</span><span class="sxs-lookup"><span data-stu-id="0dfea-195">Any default model mapping that doesn't have country/region context restrictions has the next higher priority for selection  (**Mapping (General) custom** in the examples in this topic).</span></span>
- <span data-ttu-id="0dfea-196">ان اي تعيين نموذج له قيود علي سياق البلد/المنطقة له اولويه اعلي للتحديد مقارنةً بتعيين نموذج ليس له قيود علي سياق البلد/المنطقة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-196">Any model mapping that has country/region context restrictions has higher priority for selection than a model mapping that doesn't have country/region context restrictions.</span></span>

<span data-ttu-id="0dfea-197">يوفر الجدول التالي معلومات حول نتائج تحديد تعيين النماذج لكافة الحالات المحتملة لإعدادات تعيين النماذج:</span><span class="sxs-lookup"><span data-stu-id="0dfea-197">The following table provides information about the results of model mapping selection for all possible cases for model mapping settings:</span></span>

- <span data-ttu-id="0dfea-198">يشير العمود 1 إلى ما إذا كان التعيين الأول للنموذج الذي ليس له قيود على سياق البلد/المنطقة (على سبيل المثال، تعيين **التعيين (عام)**) موجودًا، وإذا كان الأمر كذلك، وما إذا كان تم تعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم** له.</span><span class="sxs-lookup"><span data-stu-id="0dfea-198">Column 1 indicates whether the first model mapping that doesn't have country/region context restrictions (for example, the shared **Mapping (General)** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="0dfea-199">يشير العمود 2 إلى ما إذا كان التعيين الثاني للنموذج الذي ليس له قيود على سياق البلد/المنطقة (على سبيل المثال، تعيين **التعيين المخصص (عام)**) موجودًا، وإذا كان الأمر كذلك، وما إذا كان تم تعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم** له.</span><span class="sxs-lookup"><span data-stu-id="0dfea-199">Column 2 indicates whether the second model mapping that doesn't have country/region context restrictions (for example, the shared **Mapping (General) custom** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="0dfea-200">يشير العمود 3 إلى ما إذا كان التعيين الأول للنموذج يشتمل على قيود على سياق البلد/المنطقة A (على سبيل المثال، تعيين **التعيين (FR)** الخاص بفرنسا) موجودًا، وإذا كان الأمر كذلك، وما إذا كان تم تعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم** له.</span><span class="sxs-lookup"><span data-stu-id="0dfea-200">Column 3 indicates whether the first model mapping that has country/region A context restrictions (for example, the France-specific **Mapping (FR)** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="0dfea-201">يشير العمود 4 إلى ما إذا كان التعيين الثاني للنموذج يشتمل على قيود على سياق البلد/المنطقة A موجودًا، وإذا كان الأمر كذلك، وما إذا كان تم تعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم** له.</span><span class="sxs-lookup"><span data-stu-id="0dfea-201">Column 4 indicates whether the second model mapping that has country/region A context restrictions is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="0dfea-202">يقدم العمود رقم 5 النتيجة الخاصة بتحديد تعيين النموذج لتنفيذ أحد تنسيقات التقارير الإلكترونية ضمن التحكم في الشركة التي لها سياق A للمنطقه/البلد.</span><span class="sxs-lookup"><span data-stu-id="0dfea-202">Column 5 presents the result of a model mapping selection for execution of an ER format under the control of a company that has country/region A context.</span></span>
- <span data-ttu-id="0dfea-203">يقدم العمود رقم 6 النتيجة الخاصة بتحديد تعيين النموذج لتنفيذ أحد تنسيقات التقارير الإلكترونية ضمن التحكم في الشركة التي لها سياق B للمنطقه/البلد.</span><span class="sxs-lookup"><span data-stu-id="0dfea-203">Column 6 presents the result of a model mapping selection for execution of an ER format under the control of a company that has country/region B context.</span></span>

<span data-ttu-id="0dfea-204">وتشير علامة الجمع (+) في الجدول إلى وجود تكوين تعيين النموذج في المثيل الحالي لخدمة Microsoft Azure المستخدمة لتشغيل تنسيق التقارير الإلكترونية (إما Finance أو RCS).</span><span class="sxs-lookup"><span data-stu-id="0dfea-204">In the table, a plus sign (+) indicates the presence of a model mapping configuration in the current instance of the Microsoft Azure service that is used to run an ER format (either Finance or RCS).</span></span>

| <span data-ttu-id="0dfea-205">الحالة</span><span class="sxs-lookup"><span data-stu-id="0dfea-205">Case</span></span> | <span data-ttu-id="0dfea-206">تعيين النموذج 1 دون سياق البلد/المنطقة (MM1)</span><span class="sxs-lookup"><span data-stu-id="0dfea-206">Model mapping 1 without country/region context (MM1)</span></span> | <span data-ttu-id="0dfea-207">تعيين النموذج 2 دون سياق البلد/المنطقة (MM2)</span><span class="sxs-lookup"><span data-stu-id="0dfea-207">Model mapping 2 without country/region context (MM2)</span></span> | <span data-ttu-id="0dfea-208">تعيين النموذج 1 مع سياق البلد/المنطقة A (MM1A)</span><span class="sxs-lookup"><span data-stu-id="0dfea-208">Model mapping 1 with country/region A context (MM1A)</span></span> | <span data-ttu-id="0dfea-209">تعيين النموذج 2 مع سياق البلد/المنطقة A (MM2A)</span><span class="sxs-lookup"><span data-stu-id="0dfea-209">Model mapping 2 with country/region A context (MM2A)</span></span> | <span data-ttu-id="0dfea-210">تشغيل ضمن عنصر التحكم في شركه لها سياق منطقه/البلد A</span><span class="sxs-lookup"><span data-stu-id="0dfea-210">Run under control of a company that has country/region A context</span></span> | <span data-ttu-id="0dfea-211">تشغيل ضمن عنصر التحكم في شركه لها سياق منطقه/البلد B</span><span class="sxs-lookup"><span data-stu-id="0dfea-211">Run under the control of a company that has country/region B context</span></span> |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     <span data-ttu-id="0dfea-212">1</span><span class="sxs-lookup"><span data-stu-id="0dfea-212">1</span></span>   |     <span data-ttu-id="0dfea-213">2</span><span class="sxs-lookup"><span data-stu-id="0dfea-213">2</span></span>   |    <span data-ttu-id="0dfea-214">3</span><span class="sxs-lookup"><span data-stu-id="0dfea-214">3</span></span>    |    <span data-ttu-id="0dfea-215">4</span><span class="sxs-lookup"><span data-stu-id="0dfea-215">4</span></span>    |           <span data-ttu-id="0dfea-216">5</span><span class="sxs-lookup"><span data-stu-id="0dfea-216">5</span></span>               |            <span data-ttu-id="0dfea-217">6</span><span class="sxs-lookup"><span data-stu-id="0dfea-217">6</span></span>               |
|     <span data-ttu-id="0dfea-218">1</span><span class="sxs-lookup"><span data-stu-id="0dfea-218">1</span></span>   |         |         |         |         | <span data-ttu-id="0dfea-219">خطأ (تعيين مفقود)</span><span class="sxs-lookup"><span data-stu-id="0dfea-219">Error (missing mapping)</span></span>   | <span data-ttu-id="0dfea-220">خطأ (تعيين مفقود)</span><span class="sxs-lookup"><span data-stu-id="0dfea-220">Error (missing mapping)</span></span>    |
|     <span data-ttu-id="0dfea-221">2</span><span class="sxs-lookup"><span data-stu-id="0dfea-221">2</span></span>   |     +   |         |         |         | <span data-ttu-id="0dfea-222">MM1</span><span class="sxs-lookup"><span data-stu-id="0dfea-222">MM1</span></span>                       | <span data-ttu-id="0dfea-223">MM1</span><span class="sxs-lookup"><span data-stu-id="0dfea-223">MM1</span></span>                        |
|     <span data-ttu-id="0dfea-224">3</span><span class="sxs-lookup"><span data-stu-id="0dfea-224">3</span></span>   |     +   |     +   |         |         | <span data-ttu-id="0dfea-225">خطأ (تعيينات متعددة)</span><span class="sxs-lookup"><span data-stu-id="0dfea-225">Error (multiple mappings)</span></span> | <span data-ttu-id="0dfea-226">خطأ (تعيينات متعددة)</span><span class="sxs-lookup"><span data-stu-id="0dfea-226">Error (multiple mappings)</span></span>  |
|     <span data-ttu-id="0dfea-227">4</span><span class="sxs-lookup"><span data-stu-id="0dfea-227">4</span></span>   |     +   |         |    +    |         | <span data-ttu-id="0dfea-228">MM1A</span><span class="sxs-lookup"><span data-stu-id="0dfea-228">MM1A</span></span>                      | <span data-ttu-id="0dfea-229">MM1</span><span class="sxs-lookup"><span data-stu-id="0dfea-229">MM1</span></span>                        |
|     <span data-ttu-id="0dfea-230">5</span><span class="sxs-lookup"><span data-stu-id="0dfea-230">5</span></span>   |     +   |         |    +    |    +    | <span data-ttu-id="0dfea-231">خطأ (تعيينات متعددة)</span><span class="sxs-lookup"><span data-stu-id="0dfea-231">Error (multiple mappings)</span></span> | <span data-ttu-id="0dfea-232">MM1</span><span class="sxs-lookup"><span data-stu-id="0dfea-232">MM1</span></span>                        |
|     <span data-ttu-id="0dfea-233">6</span><span class="sxs-lookup"><span data-stu-id="0dfea-233">6</span></span>   |     +   | <span data-ttu-id="0dfea-234">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-234">default</span></span> |    +    |    +    | <span data-ttu-id="0dfea-235">MM2</span><span class="sxs-lookup"><span data-stu-id="0dfea-235">MM2</span></span>                       | <span data-ttu-id="0dfea-236">MM2</span><span class="sxs-lookup"><span data-stu-id="0dfea-236">MM2</span></span>                        |
|     <span data-ttu-id="0dfea-237">7</span><span class="sxs-lookup"><span data-stu-id="0dfea-237">7</span></span>   |     +   |         | <span data-ttu-id="0dfea-238">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-238">default</span></span> |         | <span data-ttu-id="0dfea-239">MM1A</span><span class="sxs-lookup"><span data-stu-id="0dfea-239">MM1A</span></span>                      | <span data-ttu-id="0dfea-240">MM1</span><span class="sxs-lookup"><span data-stu-id="0dfea-240">MM1</span></span>                        |
|     <span data-ttu-id="0dfea-241">8</span><span class="sxs-lookup"><span data-stu-id="0dfea-241">8</span></span>   |     +   |         | <span data-ttu-id="0dfea-242">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-242">default</span></span> |    +    | <span data-ttu-id="0dfea-243">MM1A</span><span class="sxs-lookup"><span data-stu-id="0dfea-243">MM1A</span></span>                      | <span data-ttu-id="0dfea-244">MM1</span><span class="sxs-lookup"><span data-stu-id="0dfea-244">MM1</span></span>                        |
|     <span data-ttu-id="0dfea-245">9</span><span class="sxs-lookup"><span data-stu-id="0dfea-245">9</span></span>   |     +   |         | <span data-ttu-id="0dfea-246">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-246">default</span></span> | <span data-ttu-id="0dfea-247">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-247">default</span></span> | <span data-ttu-id="0dfea-248">خطأ (تعيينات متعددة)</span><span class="sxs-lookup"><span data-stu-id="0dfea-248">Error (multiple mappings)</span></span> | <span data-ttu-id="0dfea-249">MM1</span><span class="sxs-lookup"><span data-stu-id="0dfea-249">MM1</span></span>                        |
|    <span data-ttu-id="0dfea-250">10</span><span class="sxs-lookup"><span data-stu-id="0dfea-250">10</span></span>   | <span data-ttu-id="0dfea-251">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-251">default</span></span> |         |         |         | <span data-ttu-id="0dfea-252">MM1</span><span class="sxs-lookup"><span data-stu-id="0dfea-252">MM1</span></span>                       | <span data-ttu-id="0dfea-253">MM1</span><span class="sxs-lookup"><span data-stu-id="0dfea-253">MM1</span></span>                        |
|    <span data-ttu-id="0dfea-254">11</span><span class="sxs-lookup"><span data-stu-id="0dfea-254">11</span></span>   | <span data-ttu-id="0dfea-255">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-255">default</span></span> |    +    |         |         | <span data-ttu-id="0dfea-256">MM1</span><span class="sxs-lookup"><span data-stu-id="0dfea-256">MM1</span></span>                       | <span data-ttu-id="0dfea-257">MM1</span><span class="sxs-lookup"><span data-stu-id="0dfea-257">MM1</span></span>                        |
|    <span data-ttu-id="0dfea-258">12</span><span class="sxs-lookup"><span data-stu-id="0dfea-258">12</span></span>   | <span data-ttu-id="0dfea-259">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-259">default</span></span> |         |    +    |         | <span data-ttu-id="0dfea-260">MM1</span><span class="sxs-lookup"><span data-stu-id="0dfea-260">MM1</span></span>                       | <span data-ttu-id="0dfea-261">MM1</span><span class="sxs-lookup"><span data-stu-id="0dfea-261">MM1</span></span>                        |
|    <span data-ttu-id="0dfea-262">13</span><span class="sxs-lookup"><span data-stu-id="0dfea-262">13</span></span>   | <span data-ttu-id="0dfea-263">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-263">default</span></span> | <span data-ttu-id="0dfea-264">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-264">default</span></span> |         |         | <span data-ttu-id="0dfea-265">خطأ (تعيينات متعددة)</span><span class="sxs-lookup"><span data-stu-id="0dfea-265">Error (multiple mappings)</span></span> | <span data-ttu-id="0dfea-266">خطأ (تعيينات متعددة)</span><span class="sxs-lookup"><span data-stu-id="0dfea-266">Error (multiple mappings)</span></span>  |
|    <span data-ttu-id="0dfea-267">14</span><span class="sxs-lookup"><span data-stu-id="0dfea-267">14</span></span>   | <span data-ttu-id="0dfea-268">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-268">default</span></span> |         | <span data-ttu-id="0dfea-269">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-269">default</span></span> |         | <span data-ttu-id="0dfea-270">MM1A</span><span class="sxs-lookup"><span data-stu-id="0dfea-270">MM1A</span></span>                      | <span data-ttu-id="0dfea-271">MM1</span><span class="sxs-lookup"><span data-stu-id="0dfea-271">MM1</span></span>                        |
|    <span data-ttu-id="0dfea-272">15</span><span class="sxs-lookup"><span data-stu-id="0dfea-272">15</span></span>   | <span data-ttu-id="0dfea-273">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-273">default</span></span> |         | <span data-ttu-id="0dfea-274">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-274">default</span></span> | <span data-ttu-id="0dfea-275">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-275">default</span></span> | <span data-ttu-id="0dfea-276">MM1A</span><span class="sxs-lookup"><span data-stu-id="0dfea-276">MM1A</span></span>                      | <span data-ttu-id="0dfea-277">MM2A</span><span class="sxs-lookup"><span data-stu-id="0dfea-277">MM2A</span></span>                       |
|    <span data-ttu-id="0dfea-278">16</span><span class="sxs-lookup"><span data-stu-id="0dfea-278">16</span></span>   |         |         |    +    |    +    | <span data-ttu-id="0dfea-279">MM1A</span><span class="sxs-lookup"><span data-stu-id="0dfea-279">MM1A</span></span>                      | <span data-ttu-id="0dfea-280">MM2A</span><span class="sxs-lookup"><span data-stu-id="0dfea-280">MM2A</span></span>                       |
|    <span data-ttu-id="0dfea-281">17</span><span class="sxs-lookup"><span data-stu-id="0dfea-281">17</span></span>   |         |         | <span data-ttu-id="0dfea-282">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-282">default</span></span> | <span data-ttu-id="0dfea-283">افتراضية</span><span class="sxs-lookup"><span data-stu-id="0dfea-283">default</span></span> | <span data-ttu-id="0dfea-284">MM1A</span><span class="sxs-lookup"><span data-stu-id="0dfea-284">MM1A</span></span>                      | <span data-ttu-id="0dfea-285">MM2A</span><span class="sxs-lookup"><span data-stu-id="0dfea-285">MM2A</span></span>                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a><span data-ttu-id="0dfea-286">التعرف على التعيين الذي تم استخدامه في تنفيذ أحد تنسيقات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="0dfea-286">Learn what mapping was used in the execution of an ER format</span></span>

### <a name="configure-er-user-parameters"></a><span data-ttu-id="0dfea-287">تكوين معلمات مستخدم التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="0dfea-287">Configure ER user parameters</span></span>

1.  <span data-ttu-id="0dfea-288">في صفحة **التكوينات**، في جزء الإجراء، في علامة التبويب **التكوينات**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-288">On the **Configurations** page, on the Action Pane, on the **CONFIGURATIONS** tab, select **User parameters**.</span></span>
2.  <span data-ttu-id="0dfea-289">قم بتعيين خيار **تشغيل في وضع التصحيح** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-289">Set the **Run in debug mode** option to **Yes**.</span></span>
4.  <span data-ttu-id="0dfea-290">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-290">Select **Ok**.</span></span>

### <a name="run-the-configured-format"></a><span data-ttu-id="0dfea-291">تشغيل التنسيق المكوَّن</span><span class="sxs-lookup"><span data-stu-id="0dfea-291">Run the configured format</span></span>

1.  <span data-ttu-id="0dfea-292">في صفحة **التكوينات**، في شجرة التكوينات، حدد عنصر **التنسيق للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-292">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="0dfea-293">في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-293">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="0dfea-294">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-294">Select **Ok**.</span></span>

### <a name="review-the-er-debug-log"></a><span data-ttu-id="0dfea-295">مراجعة سجل تصحيح التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="0dfea-295">Review the ER debug log</span></span>

1.  <span data-ttu-id="0dfea-296">في جزء التنقل، انتقل إلى **الوحدات \> إدارة المؤسسة \> التقارير الإلكترونية \> سجل تصحيح التكوين**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-296">In the navigation pane, go to **Modules \> Organization administration \> Electronic reporting \> Configuration debug log**.</span></span>
2.  <span data-ttu-id="0dfea-297">حدد الزر **إعادة تحميل هذه الصفحة**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-297">Select the **Reload this page** button.</span></span>

![صفحه سجلات تشغيل التقارير الإلكترونية](./media/RCS-Context-specific-mapping-DebugLog.PNG)

<span data-ttu-id="0dfea-299">لاحظ انه تمت أضافه سجل جديد إلى سجل تصحيح التقارير الإلكترونية لتنسيق التقارير الإلكترونية الذي تم تنفيذه.</span><span class="sxs-lookup"><span data-stu-id="0dfea-299">Notice that a new record has been added to the ER debug log for the executed ER format.</span></span> <span data-ttu-id="0dfea-300">ونظرا لأنه يتم تعيين حقل **المستوى** لهذا السجل إلى **معلومات**، يكون السجل معلوماتيًا.</span><span class="sxs-lookup"><span data-stu-id="0dfea-300">Because the **Level** field of this record is set to **Info**, the record is informational.</span></span> <span data-ttu-id="0dfea-301">نظرًا لتعيين حقل مكون التنسيق إلى **تكوين التعيين**، يقوم السجل باعلامك عن تعيين النموذج الذي تم استخدامه أثناء تنفيذ تنسيق التقارير الإلكترونية **التنسيق للتعرف على التعيينات** (المحدد في حقل **اسم التكوين**).</span><span class="sxs-lookup"><span data-stu-id="0dfea-301">Because the Format component field is set to **Mapping configuration**, the record informs you about a model mapping that was used during execution of the **Format to learn mappings** ER format (selected in the **Configuration name** field).</span></span> <span data-ttu-id="0dfea-302">ويعلمك محتوى حقل **النص الذي تم إنشاؤه** بأن مكون تعيين **التعيين (FR)** الموجود في تكوين **التعيين (FR)** تم استخدامه لتشغيل هذا التقرير.</span><span class="sxs-lookup"><span data-stu-id="0dfea-302">The content of the **Generated text** field informs you that the **Mapping (FR)** mapping component that resides in the **Mapping (FR)** configuration has been used to run this report.</span></span>

## <a name="appendix-1"></a><a name="appendix1"></a> <span data-ttu-id="0dfea-303">الملحق 1</span><span class="sxs-lookup"><span data-stu-id="0dfea-303">Appendix 1</span></span>

### <a name="configure-a-sample-data-model"></a><span data-ttu-id="0dfea-304">تكوين نموذج بيانات النموذج</span><span class="sxs-lookup"><span data-stu-id="0dfea-304">Configure a sample data model</span></span>

<span data-ttu-id="0dfea-305">سجل الدخول إلى مثيل RCS.</span><span class="sxs-lookup"><span data-stu-id="0dfea-305">Sign in to your RCS instance.</span></span>

<span data-ttu-id="0dfea-306">في هذا المثال، سوف تنشئ تكوينًا للشركة النموذجية Litware, Inc. ولإكمال هذه الخطوات، يجب عليك أولاً في RCS إكمال الخطوات الموجودة في الإجراء [‏‫إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="0dfea-306">In this example, you will create a configuration for sample company, Litware, Inc. To complete these steps, you must first complete, in RCS, the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

#### <a name="create-an-er-data-model-configuration"></a><span data-ttu-id="0dfea-307">إنشاء تكوين نموذج بيانات تقارير إلكترونية</span><span class="sxs-lookup"><span data-stu-id="0dfea-307">Create an ER data model configuration</span></span>

1.  <span data-ttu-id="0dfea-308">في لوحة المعلومات الافتراضية، حدد **‏‫إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-308">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="0dfea-309">حدد تجانب **تكوينات التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-309">Select the **Reporting configurations** tile.</span></span>
3.  <span data-ttu-id="0dfea-310">في صفحة **التكوينات**، حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-310">On the **Configurations** page, select **Create configuration**.</span></span>
4.  <span data-ttu-id="0dfea-311">في مربع الحوار المنسدل، في حقل **الاسم**، أدخل **النموذج للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-311">In the drop-down dialog box, in the **Name** field, enter **Model to learn mappings**.</span></span>
5.  <span data-ttu-id="0dfea-312">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-312">Select **Create configuration**.</span></span>
6.  <span data-ttu-id="0dfea-313">حدد علامة التبويب السريعة **مكونات التكوين**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-313">Select the **Configuration components** FastTab.</span></span>

<span data-ttu-id="0dfea-314">لاحظ أن إصدار المسودة 1 لتكوين التقارير الإلكترونية هذا جاهز للتحرير.</span><span class="sxs-lookup"><span data-stu-id="0dfea-314">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="0dfea-315">يحتوي هذا الإصدار على مكون نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="0dfea-315">This version contains the data model component.</span></span>

#### <a name="design-a-sample-data-model"></a><span data-ttu-id="0dfea-316">تصميم نموذج بيانات النموذج</span><span class="sxs-lookup"><span data-stu-id="0dfea-316">Design a sample data model</span></span>

1.  <span data-ttu-id="0dfea-317">في **صفحة التكوينات**، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-317">On the **Configurations page**, select **Designer**.</span></span>
2.  <span data-ttu-id="0dfea-318">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-318">Select **New**.</span></span>
3.  <span data-ttu-id="0dfea-319">في مربع الحوار المنسدل، في حقل **الاسم**، أدخل **نقطة الإدخال 1**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-319">In the drop-down dialog box, in the **Name** field, enter **Entry point 1**.</span></span>
4.  <span data-ttu-id="0dfea-320">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-320">Select **Add**.</span></span>
5.  <span data-ttu-id="0dfea-321">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-321">Select **New**.</span></span>
6.  <span data-ttu-id="0dfea-322">في مربع الحوار المنسدل، في حقل **الاسم**، أدخل **وصف الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-322">In the drop-down dialog box, in the **Name** field, enter **Functionality description**.</span></span>
7.  <span data-ttu-id="0dfea-323">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-323">Select **Add**.</span></span>
8.  <span data-ttu-id="0dfea-324">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-324">Select **New**.</span></span>
9.  <span data-ttu-id="0dfea-325">في مربع الحوار المنسدل، في مجموعة حقول **العقدة الجديدة**، حدد **جذر النموذج**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-325">In the drop-down dialog box, in the **New node** field group, select **Model root**.</span></span>
10. <span data-ttu-id="0dfea-326">في حقل **الاسم**، أدخل **نقطة الإدخال 2**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-326">In the **Name** field, enter **Entry point 2**.</span></span>
11. <span data-ttu-id="0dfea-327">حدد **نقطه الإدخال 2**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-327">Select **Entry point 2**.</span></span>
12. <span data-ttu-id="0dfea-328">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-328">Select **Add**.</span></span>
13. <span data-ttu-id="0dfea-329">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-329">Select **New**.</span></span>
14. <span data-ttu-id="0dfea-330">في مربع الحوار المنسدل، في حقل **الاسم**، أدخل **وصف الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-330">In the drop-down dialog box, in the **Name** field, enter **Functionality description**.</span></span>
15. <span data-ttu-id="0dfea-331">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-331">Select **Add**.</span></span>

    ![صفحة مصمم نموذج بيانات التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Model.PNG)

16. <span data-ttu-id="0dfea-333">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-333">Select **Save**.</span></span>
17. <span data-ttu-id="0dfea-334">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-334">Close the page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-configuration"></a><span data-ttu-id="0dfea-335">إكمال الإصدار المعدل من تكوين النموذج</span><span class="sxs-lookup"><span data-stu-id="0dfea-335">Complete the modified version of the model configuration</span></span>

1.  <span data-ttu-id="0dfea-336">في صفحة **التكوينات**، في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-336">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="0dfea-337">قم بتغيير حالة تكوين النموذج المصمم من **مسودة** إلى **مكتمل**، بحيث يمكن استخدامه لتصميم تنسيقات وتعيينات النماذج المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-337">Change the status of designed model configuration from **Draft** to **Completed**, so that it can be used to design the required model mappings and formats.</span></span>

2.  <span data-ttu-id="0dfea-338">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-338">Select **Complete**.</span></span>
3.  <span data-ttu-id="0dfea-339">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-339">Select **OK**.</span></span>

<span data-ttu-id="0dfea-340">لاحظ أن التكوين الذي قمت بإنشائه تم حفظه باعتباره الإصدار المكتمل 1.</span><span class="sxs-lookup"><span data-stu-id="0dfea-340">Notice that the configuration that you created is saved as completed version 1.</span></span>

### <a name="configure-a-sample-model-mapping"></a><span data-ttu-id="0dfea-341">تكوين تعيين نموذج عينة</span><span class="sxs-lookup"><span data-stu-id="0dfea-341">Configure a sample model mapping</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="0dfea-342">إنشاء تكوين تعيين نموذج التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="0dfea-342">Create an ER model mapping configuration</span></span>

1.  <span data-ttu-id="0dfea-343">في صفحة **التكوينات**، حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-343">On the **Configurations** page, select **Create configuration**.</span></span>
2.  <span data-ttu-id="0dfea-344">في مربع الحوار المنسدل، في مجموعة الحقل **جديد**، حدد **تعيين النموذج استنادًا إلى نموذج نموذج البيانات للتعرف إلى التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-344">In the drop-down dialog box, in the **New** field group, select **Model mapping based on data model Model to learn mappings**.</span></span>
3.  <span data-ttu-id="0dfea-345">في حقل **الاسم**، أدخل **التعيين (عام)**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-345">In the **Name** field, enter **Mapping (General)**.</span></span>
4.  <span data-ttu-id="0dfea-346">في حقل **تعريف نموذج البيانات**، حدد **نقطة الإدخال 1**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-346">In the **Data model definition** field, select **Entry point 1**.</span></span>
5.  <span data-ttu-id="0dfea-347">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-347">Select **Create configuration**.</span></span>

<span data-ttu-id="0dfea-348">لاحظ أن إصدار المسودة 1 لتكوين التقارير الإلكترونية هذا جاهز للتحرير.</span><span class="sxs-lookup"><span data-stu-id="0dfea-348">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="0dfea-349">يحتوي هذا الإصدار على مكون تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="0dfea-349">This version contains the model mapping component.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="0dfea-350">تصميم تعيين نموذج عينة</span><span class="sxs-lookup"><span data-stu-id="0dfea-350">Design a sample model mapping</span></span>

1.  <span data-ttu-id="0dfea-351">في صفحة **التكوينات**، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-351">On the **Configurations** page, select **Designer**.</span></span>

    <span data-ttu-id="0dfea-352">لاحظ انه تمت أضافه تعيين النموذج من نوع اتجاه **إلى النموذج** تلقائيًا إلى هذا المكون لتعريف **نقطة الإدخال 1**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-352">Notice that the model mapping of the **To model** direction type has been automatically added to this component for the **Entry point 1** definition.</span></span>
    
2.  <span data-ttu-id="0dfea-353">حدد **المصمم** للبدء في تحرير تعيين النموذج المضاف.</span><span class="sxs-lookup"><span data-stu-id="0dfea-353">Select **Designer** to start editing the added model mapping.</span></span>
3.  <span data-ttu-id="0dfea-354">في قسم **نموذج البيانات**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-354">In the **Data model** section, select **Edit**.</span></span>
4.  <span data-ttu-id="0dfea-355">في حقل **المعادلة**، أدخل **"الوظيفة العامة 1"**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-355">In the **Formula** field, enter **"Generic functionality 1"**.</span></span>
5.  <span data-ttu-id="0dfea-356">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-356">Select **Save**.</span></span>
6.  <span data-ttu-id="0dfea-357">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-357">Close the **Formula designer** page.</span></span>

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  <span data-ttu-id="0dfea-359">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-359">Select **Save**.</span></span>
8.  <span data-ttu-id="0dfea-360">أغلق صفحة **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-360">Close the **Model mapping designer** page.</span></span>
9.  <span data-ttu-id="0dfea-361">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-361">Select **New**.</span></span>
10. <span data-ttu-id="0dfea-362">في حقل **التعريف**، حدد **نقطة الإدخال 2**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-362">In the **Definition** field, select **Entry point 2**.</span></span>
11. <span data-ttu-id="0dfea-363">في حقل **الاسم**، أدخل **التعيين (عام) 2**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-363">In the **Name** field, enter **Mapping (General) 2**.</span></span>
12. <span data-ttu-id="0dfea-364">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-364">Select **Designer**.</span></span>
13. <span data-ttu-id="0dfea-365">في قسم **نموذج البيانات**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-365">In the **Data model** section, select **Edit**.</span></span>
14. <span data-ttu-id="0dfea-366">في حقل **المعادلة**، أدخل **"الوظيفة العامة 2"**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-366">In the **Formula** field, enter **"Generic functionality 2"**.</span></span>
15. <span data-ttu-id="0dfea-367">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-367">Select **Save**.</span></span>
16. <span data-ttu-id="0dfea-368">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-368">Close the **Formula designer** page.</span></span>

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. <span data-ttu-id="0dfea-370">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-370">Select **Save**.</span></span>
18. <span data-ttu-id="0dfea-371">أغلق صفحة **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-371">Close the **Model mapping designer** page.</span></span>

    ![صفحة تعيينات نماذج التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. <span data-ttu-id="0dfea-373">أغلق صفحة **تعيينات النماذج**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-373">Close the **Model mappings** page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="0dfea-374">إكمال الإصدار المعدل من تكوين تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="0dfea-374">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="0dfea-375">في **صفحة التكوينات**، في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-375">On the **Configurations page**, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="0dfea-376">قم بتغيير حالة تكوين تعيين النموذج المصمم من **مسودة** إلى **مكتمل**، بحيث يمكن استخدامه بواسطة تنسيقات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0dfea-376">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="0dfea-377">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-377">Select **Complete**.</span></span>
3.  <span data-ttu-id="0dfea-378">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-378">Select **OK**.</span></span>

<span data-ttu-id="0dfea-379">لاحظ أن التكوين الذي تم إنشاؤه تم حفظه باعتباره الإصدار المكتمل 1.</span><span class="sxs-lookup"><span data-stu-id="0dfea-379">Notice that the configuration that is created is saved as completed version 1.</span></span>

### <a name="configure-a-sample-format"></a><span data-ttu-id="0dfea-380">تكوين تنسيق نموذج</span><span class="sxs-lookup"><span data-stu-id="0dfea-380">Configure a sample format</span></span>

#### <a name="create-an-er-format-configuration"></a><span data-ttu-id="0dfea-381">إنشاء تكوين تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="0dfea-381">Create an ER format configuration</span></span>

1.  <span data-ttu-id="0dfea-382">في صفحة **التكوينات**، في شجرة التكوينات، حدد **النموذج للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-382">On the **Configurations** page, in the configurations tree, select **Model to learn mappings**.</span></span>
2.  <span data-ttu-id="0dfea-383">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-383">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="0dfea-384">في مربع الحوار المنسدل، في مجموعة الحقل **جديد**، حدد **التنسيق استنادًا إلى نموذج نموذج البيانات للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-384">In the drop-down dialog box, in the **New** field group, select **Format based on data model Model to learn mappings**.</span></span>
4.  <span data-ttu-id="0dfea-385">في حقل **الاسم**، أدخل **التنسيق للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-385">In the **Name** field, enter **Format to learn mappings**.</span></span>
5.  <span data-ttu-id="0dfea-386">في حقل **تعريف نموذج البيانات**، حدد **نقطة الإدخال 1**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-386">In the **Data model definition** field, select **Entry point 1**.</span></span>
6.  <span data-ttu-id="0dfea-387">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-387">Select **Create configuration**.</span></span>

<span data-ttu-id="0dfea-388">لاحظ أن إصدار المسودة 1 لتكوين التقارير الإلكترونية هذا جاهز للتحرير.</span><span class="sxs-lookup"><span data-stu-id="0dfea-388">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="0dfea-389">يحتوي هذا الإصدار على مكون التنسيق.</span><span class="sxs-lookup"><span data-stu-id="0dfea-389">This version contains the format component.</span></span>

#### <a name="design-a-sample-format"></a><span data-ttu-id="0dfea-390">تصميم تنسيق نموذج</span><span class="sxs-lookup"><span data-stu-id="0dfea-390">Design a sample format</span></span>

1.  <span data-ttu-id="0dfea-391">في صفحة **التكوينات**، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-391">On the **Configurations** page, select **Designer**.</span></span>
2.  <span data-ttu-id="0dfea-392">حدد **إضافة جذر**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-392">Select **Add root**.</span></span>
3.  <span data-ttu-id="0dfea-393">في مجموعة **النص**، حدد عنصر **السلسلة**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-393">In the **Text** group, select the **String** item.</span></span>
4.  <span data-ttu-id="0dfea-394">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-394">Select **OK**.</span></span>

#### <a name="bind-format-elements-to-a-data-source"></a><span data-ttu-id="0dfea-395">ربط عناصر التنسيق بمصدر بيانات</span><span class="sxs-lookup"><span data-stu-id="0dfea-395">Bind format elements to a data source</span></span>

1.  <span data-ttu-id="0dfea-396">في صفحة **مصمم التنسيق**، في علامة التبويب **تعيين**، قم بتوسيع مصدر بيانات النموذج.</span><span class="sxs-lookup"><span data-stu-id="0dfea-396">On the **Format designer** page, on the **Mapping** tab, expand the model data source.</span></span>
2.  <span data-ttu-id="0dfea-397">حدد حقل **وصف الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-397">Select the **Functionality description** field.</span></span>
3.  <span data-ttu-id="0dfea-398">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-398">Select **Bind**.</span></span>

    ![صفحة مصمم تنسيق‬ التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Format.PNG)

4.  <span data-ttu-id="0dfea-400">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-400">Select **Save**.</span></span>
5.  <span data-ttu-id="0dfea-401">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-401">Close the page.</span></span>

## <a name="appendix-2"></a><a name="appendix2"></a> <span data-ttu-id="0dfea-402">الملحق 2</span><span class="sxs-lookup"><span data-stu-id="0dfea-402">Appendix 2</span></span>

### <a name="configure-a-sample-model-mapping-for-general-customization"></a><span data-ttu-id="0dfea-403">تكوين تعيين نموذج عينة للتخصيص العام</span><span class="sxs-lookup"><span data-stu-id="0dfea-403">Configure a sample model mapping for general customization</span></span>

<span data-ttu-id="0dfea-404">قد تحتاج إلى تخصيص تعيين نموذج تم توفيره من قبل موفر التكوين (الشريك)، ثم استخدام الإصدار المخصص كمصدر بيانات لتنسيقات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0dfea-404">You might want to customize a model mapping that a configuration provider (partner) provided to you, and then use the customized version as a data source for your ER formats.</span></span> <span data-ttu-id="0dfea-405">في هذه الحالة، يجب إنشاء تكوين تعيين نموذج تقارير إلكترونية (ER) مخصص لاجراء التغييرات المطلوبة في تعيينات النماذج الموجودة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-405">In this case, you must create a custom ER model mapping configuration to make the required changes in existing model mappings.</span></span> <span data-ttu-id="0dfea-406">تستخدم الإجراءات الموجودة في هذا الملحق تعيين نموذج **التعيين (عام)** كمثال.</span><span class="sxs-lookup"><span data-stu-id="0dfea-406">The procedures in this appendix use the **Mapping (General)** model mapping as an example.</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="0dfea-407">إنشاء تكوين تعيين نموذج التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="0dfea-407">Create an ER model mapping configuration</span></span>

1.  <span data-ttu-id="0dfea-408">في صفحة **التكوينات**، في شجرة التكوينات، حدد **التعيين (عام)**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-408">On the **Configurations** page, in the configurations tree, select **Mapping (General)**.</span></span>
2.  <span data-ttu-id="0dfea-409">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-409">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="0dfea-410">في مربع الحوار المنسدل ، في مجموعه الحقل **جديد**، حدد **الاشتقاق من الاسم: التعيين (عام)، شركة Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-410">In the drop-down dialog box, in the **New** field group, select **Derive from Name: Mapping (General), Litware, Inc.**.</span></span>
4.  <span data-ttu-id="0dfea-411">في حقل **الاسم**، أدخل **التعيين المخصص (عام)**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-411">In the **Name** field, enter **Mapping (General) custom**.</span></span>
5.  <span data-ttu-id="0dfea-412">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-412">Select **Create configuration**.</span></span>

<span data-ttu-id="0dfea-413">لاحظ أن إصدار المسودة 1 لتكوين التقارير الإلكترونية هذا جاهز للتحرير.</span><span class="sxs-lookup"><span data-stu-id="0dfea-413">Notice that draft version 1 of this ER configuration is ready for editing.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="0dfea-414">تصميم تعيين نموذج عينة</span><span class="sxs-lookup"><span data-stu-id="0dfea-414">Design a sample model mapping</span></span>

1.  <span data-ttu-id="0dfea-415">في صفحة **التكوينات**، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-415">On the **Configurations** page, select **Designer**.</span></span>

    > <span data-ttu-id="0dfea-416">لاحظ أنه تم نسخ تعيينات النماذج الخاصة بالتكوين الأساسي تلقائيًا إلى هذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="0dfea-416">Notice that the model mappings of the base configuration have been automatically copied to this configuration.</span></span>

2.  <span data-ttu-id="0dfea-417">حدد تعيين **نسخ التعيين (عام)**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-417">Select the **Mapping (General) Copy** mapping.</span></span>
3.  <span data-ttu-id="0dfea-418">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-418">Select **Designer**.</span></span>
4.  <span data-ttu-id="0dfea-419">في قسم **نموذج البيانات**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-419">In the **Data model** section, select **Edit**.</span></span>
5.  <span data-ttu-id="0dfea-420">في حقل **المعادلة**، أدخل **"الوظيفة العامة المخصصة 1"**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-420">In the **Formula** field, enter **"Generic functionality 1 custom"**.</span></span>
6.  <span data-ttu-id="0dfea-421">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-421">Select **Save**.</span></span>
7.  <span data-ttu-id="0dfea-422">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-422">Close the page.</span></span>

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  <span data-ttu-id="0dfea-424">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-424">Select **Save**.</span></span>
9.  <span data-ttu-id="0dfea-425">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-425">Close the page.</span></span>
10. <span data-ttu-id="0dfea-426">حدد تعيين **نسخة التعيين (عام) 2**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-426">Select the **Mapping (General) 2 Copy** mapping.</span></span>
11. <span data-ttu-id="0dfea-427">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-427">Select **Designer**.</span></span>
12. <span data-ttu-id="0dfea-428">في قسم **نموذج البيانات**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-428">In the **Data model** section, select **Edit**.</span></span>
13. <span data-ttu-id="0dfea-429">في حقل **المعادلة**، أدخل **"الوظيفة العامة المخصصة 2"**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-429">In the **Formula** field, enter **"Generic functionality 2 custom"**.</span></span>
14. <span data-ttu-id="0dfea-430">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-430">Select **Save**.</span></span>
15. <span data-ttu-id="0dfea-431">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-431">Close the page.</span></span>

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. <span data-ttu-id="0dfea-433">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-433">Select **Save**.</span></span>
17. <span data-ttu-id="0dfea-434">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-434">Close the page.</span></span>

    ![صفحة تعيينات نماذج التقارير الإلكترونية](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. <span data-ttu-id="0dfea-436">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-436">Close the page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="0dfea-437">إكمال الإصدار المعدل من تكوين تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="0dfea-437">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="0dfea-438">في صفحة **التكوينات**، في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-438">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="0dfea-439">قم بتغيير حالة تكوين تعيين النموذج المصمم من **مسودة** إلى **مكتمل**، بحيث يمكن استخدامه بواسطة تنسيقات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0dfea-439">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="0dfea-440">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-440">Select **Complete**.</span></span>
3.  <span data-ttu-id="0dfea-441">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-441">Select **OK**.</span></span>

<span data-ttu-id="0dfea-442">لاحظ أن التكوين الذي تم إنشاؤه تم حفظه باعتباره الإصدار المكتمل 1.</span><span class="sxs-lookup"><span data-stu-id="0dfea-442">Notice that the configuration that is created is saved as completed version 1.</span></span>

## <a name="appendix-3"></a><a name="appendix3"></a> <span data-ttu-id="0dfea-443">الملحق 3</span><span class="sxs-lookup"><span data-stu-id="0dfea-443">Appendix 3</span></span>

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a><span data-ttu-id="0dfea-444">تكوين تعيين نموذج عينة للتخصيص الخاص بالبلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="0dfea-444">Configure a sample model mapping for country/region-specific customization</span></span>

<span data-ttu-id="0dfea-445">بالنسبة لبعض تنسيقات التقارير الإلكترونية، قد تكون هناك متطلبات خاصة بالبلد/المنطقة لإعداد البيانات.</span><span class="sxs-lookup"><span data-stu-id="0dfea-445">For some ER formats, there might be country/region-specific requirements for data preparation.</span></span> <span data-ttu-id="0dfea-446">في هذه الحالة، يمكنك أداره تكوين تعيين نموذج تقارير إلكترونية وعزل تنفيذ هذه المتطلبات الخاصة بالبلد/المنطقة عن التنفيذ العام.</span><span class="sxs-lookup"><span data-stu-id="0dfea-446">In this case, you can manage a separate ER model mapping configuration and isolate the implementation of these country/region-specific requirements from the general implementation.</span></span> <span data-ttu-id="0dfea-447">تستخدم الإجراءات الموجودة في هذا الملحق تنسيق التقارير الإلكترونية **التنسيق للتعرف على التعيينات** والمتطلبات الخاصة بالفرنسية كمثال.</span><span class="sxs-lookup"><span data-stu-id="0dfea-447">The procedures in this appendix use the **Format to learn mappings** ER format and French-specific requirements as an example.</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="0dfea-448">إنشاء تكوين تعيين نموذج التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="0dfea-448">Create an ER model mapping configuration</span></span>

<span data-ttu-id="0dfea-449">أولاً، قم بإنشاء تكوين تعيين نموذج تقارير إلكترونية (ER) جديد لتنفيذ المتطلبات الخاصة بالبلد/المنطقة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-449">First, create a new ER model mapping configuration to implement the country/region-specific requirements.</span></span> <span data-ttu-id="0dfea-450">استخدم تكوين تعيين نموذج تقارير إلكترونية مخصص كأساس.</span><span class="sxs-lookup"><span data-stu-id="0dfea-450">Use your custom ER model mapping configuration as a base.</span></span>

1.  <span data-ttu-id="0dfea-451">في صفحة **التكوينات**، في شجرة التكوينات، حدد **التعيين المخصص (عام)**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-451">On the **Configurations** page, in the configurations tree, select **Mapping (General) custom**.</span></span>
2.  <span data-ttu-id="0dfea-452">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-452">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="0dfea-453">في مربع الحوار المنسدل، في مجموعه الحقل **جديد**، حدد **الاشتقاق من الاسم: التعيين المخصص (عام)، شركة Litware, Inc**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-453">In the drop-down dialog box, in the **New** field group, select **Derive from Name: Mapping (General) custom, Litware, Inc**.</span></span>
4.  <span data-ttu-id="0dfea-454">في حقل **الاسم**، أدخل **التعيين (FR)**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-454">In the **Name** field, enter **Mapping (FR)**.</span></span>
5.  <span data-ttu-id="0dfea-455">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-455">Select **Create configuration**.</span></span>

<span data-ttu-id="0dfea-456">لاحظ أن إصدار المسودة 1 لتكوين التقارير الإلكترونية هذا جاهز للتحرير.</span><span class="sxs-lookup"><span data-stu-id="0dfea-456">Notice that draft version 1 of this ER configuration is ready for editing.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="0dfea-457">تصميم تعيين نموذج عينة</span><span class="sxs-lookup"><span data-stu-id="0dfea-457">Design a sample model mapping</span></span>

1.  <span data-ttu-id="0dfea-458">في صفحة **التكوينات**، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-458">On the **Configurations** page, select **Designer**.</span></span>

    > <span data-ttu-id="0dfea-459">لاحظ أنه تم نسخ تعيينات النماذج الخاصة بالتكوين الأساسي تلقائيًا إلى هذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="0dfea-459">Notice that model mappings of the base configuration have been automatically copied to this configuration.</span></span>

2.  <span data-ttu-id="0dfea-460">حدد تعيين **نسخ نسخة التعيين (عام)**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-460">Select the **Mapping (General) Copy Copy** mapping.</span></span>
3.  <span data-ttu-id="0dfea-461">أعد تسميتها بـ **التعيين (FR)**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-461">Rename it **Mapping (FR)**.</span></span>
4.  <span data-ttu-id="0dfea-462">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-462">Select **Designer**.</span></span>
5.  <span data-ttu-id="0dfea-463">في قسم **نموذج البيانات**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-463">In the **Data model** section, select **Edit**.</span></span>
6.  <span data-ttu-id="0dfea-464">في حقل **المعادلة**، أدخل **"وظيفة FR رقم 1"**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-464">In the **Formula** field, enter **"FR functionality 1"**.</span></span>
7.  <span data-ttu-id="0dfea-465">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-465">Select **Save**.</span></span>
8.  <span data-ttu-id="0dfea-466">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-466">Close the page.</span></span>

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  <span data-ttu-id="0dfea-468">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-468">Select **Save**.</span></span>
10. <span data-ttu-id="0dfea-469">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-469">Close the page.</span></span>
11. <span data-ttu-id="0dfea-470">حدد تعيين **نسخ نسخة التعيين (عام) 2**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-470">Select the **Mapping (General) 2 Copy Copy** mapping.</span></span>
12. <span data-ttu-id="0dfea-471">أعد تسميتها بـ **التعيين (FR) 2**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-471">Rename it **Mapping (FR) 2**.</span></span>
13. <span data-ttu-id="0dfea-472">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-472">Select **Designer**.</span></span>
14. <span data-ttu-id="0dfea-473">في قسم **نموذج البيانات**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-473">In the **Data model** section, select **Edit**.</span></span>
15. <span data-ttu-id="0dfea-474">في حقل **المعادلة**، أدخل **"وظيفة FR رقم 2"**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-474">In the **Formula** field, enter **"FR functionality 2"**.</span></span>
16. <span data-ttu-id="0dfea-475">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-475">Select **Save**.</span></span>
17. <span data-ttu-id="0dfea-476">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-476">Close the page.</span></span>

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. <span data-ttu-id="0dfea-478">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-478">Select **Save**.</span></span>
19. <span data-ttu-id="0dfea-479">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-479">Close the page.</span></span>

    ![صفحة تعيينات نماذج التقارير الإلكترونية](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. <span data-ttu-id="0dfea-481">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-481">Close the page.</span></span>

#### <a name="specify-countryregion-context-restrictions-for-use"></a><span data-ttu-id="0dfea-482">تحديد قيود سياق البلد/المنطقة للاستخدام</span><span class="sxs-lookup"><span data-stu-id="0dfea-482">Specify country/region context restrictions for use</span></span>

1.  <span data-ttu-id="0dfea-483">في صفحة **التكوينات**، في علامة التبويب السريع **أكواد البلد/المنطقة ISO**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-483">On the **Configurations** page, on the **ISO Country/region codes** FastTab, select **New**.</span></span>
2.  <span data-ttu-id="0dfea-484">في حقل **ISO**، حدد **FR**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-484">In the **ISO** field, select **FR**.</span></span>
3.  <span data-ttu-id="0dfea-485">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-485">Select **Save**.</span></span>

<span data-ttu-id="0dfea-486">لاحظ انه يجب عليك تسجيل الدخول إلى شركه معينه في Finance لتشغيل تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0dfea-486">Note that you must sign in to a specific company in Finance to run an ER format.</span></span> <span data-ttu-id="0dfea-487">وبالتالي ، يمكن اعتبار هذه الشركة جهة تحكم في تنفيذ تنسيق التقارير الإلكترونية وتحديد تعيين نموذج التقارير الإلكترونية الصحيح لنموذج البيانات الأساسي للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0dfea-487">Therefore, this company can be considered a party that controls both ER format execution and selection of the correct ER model mapping of the base ER data model.</span></span> <span data-ttu-id="0dfea-488">عن طريق أضافه كود البلد **FR**، فانك تحدد أن تعيين النموذج هذا متوفر للتحديد بواسطة تنسيق التقارير الإلكترونية الخاص بنموذج البيانات الأساسي فقط عند تشغيل هذا التنسيق ضمن عنصر تحكم شركه لها سياق بلد/منطقه فرنسية.</span><span class="sxs-lookup"><span data-stu-id="0dfea-488">By adding the **FR** country code, you specify that this model mapping is available for selection by an ER format of the base data model only when that format is run under the control of a company that has French country/region context.</span></span>

<span data-ttu-id="0dfea-489">يمكنك أضافه العديد من أكواد البلد/المنطقة لإصدار واحد من تكوين تعيين نموذج التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="0dfea-489">You can add multiple country/region codes for a single version of an ER model mapping configuration.</span></span> <span data-ttu-id="0dfea-490">وبهذه الطريقة، يمكن استخدام تعيينات النماذج الموجودة في تكوين تعيين النموذج لتنسيق تقارير إلكترونية يتم تشغيله ضمن التحكم في الشركات التي لها سياق بلد/منطقه مختلف.</span><span class="sxs-lookup"><span data-stu-id="0dfea-490">In this way, model mappings that reside in that model mapping configuration can be used for an ER format that is run under the control of companies that have a different country/region context.</span></span>

<span data-ttu-id="0dfea-491">لاحظ انه تم تحديد قائمه أكواد البلد/المنطقة لكل إصدار من تكوين تعيين نموذج تقارير إلكترونية ويمكن ان تختلف من إصدار إلى إصدار.</span><span class="sxs-lookup"><span data-stu-id="0dfea-491">Note that the list of country/region codes is specified for each version of an ER model mapping configuration and can vary from version to version.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="0dfea-492">إكمال الإصدار المعدل من تكوين تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="0dfea-492">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="0dfea-493">في صفحة **التكوينات**، في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-493">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="0dfea-494">قم بتغيير حالة تكوين تعيين النموذج المصمم من **مسودة** إلى **مكتمل**، بحيث يمكن استخدامه بواسطة تنسيقات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0dfea-494">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="0dfea-495">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-495">Select **Complete**.</span></span>
3.  <span data-ttu-id="0dfea-496">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-496">Select **OK**.</span></span>

<span data-ttu-id="0dfea-497">لاحظ أن التكوين الذي تم إنشاؤه تم حفظه باعتباره الإصدار المكتمل 1.</span><span class="sxs-lookup"><span data-stu-id="0dfea-497">Notice that the configuration that is created is saved as completed version 1.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0dfea-498">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0dfea-498">Additional resources</span></span>

[<span data-ttu-id="0dfea-499">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="0dfea-499">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="0dfea-500">إدارة تعيين نموذج ER (تقارير إلكترونية) في تكوينات ER (تقارير إلكترونية) منفصلة</span><span class="sxs-lookup"><span data-stu-id="0dfea-500">Manage ER model mapping in separate ER configurations</span></span>](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[<span data-ttu-id="0dfea-501">تطبيق سياق البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="0dfea-501">Apply country/region context</span></span>](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="0dfea-502">الأسئلة المتداولة</span><span class="sxs-lookup"><span data-stu-id="0dfea-502">Frequently asked questions</span></span>

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a><span data-ttu-id="0dfea-503">لقد قمت بتكوين اثنين من تكوينات تعيين نموذج تقارير إلكترونية مشترك في RCS وتم وضع علامة علي أحدهما كتكوين تعيين للنموذج الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="0dfea-503">I configured two shared ER model mapping configurations in RCS and marked one of them as the default model mapping configuration.</span></span> <span data-ttu-id="0dfea-504">لقد قمت بنجاح بتشغيل تنسيق تقارير إلكترونية تم إنشاؤه لنفس التكوين الأساسي لنموذج بيانات التقارير الإلكترونية، لاختبار تعيينات النماذج.</span><span class="sxs-lookup"><span data-stu-id="0dfea-504">I successfully ran an ER format that was created for the same base ER data model configuration, to test model mappings.</span></span> <span data-ttu-id="0dfea-505">ثم قمت بعد ذلك باستيراد حل التقارير الإلكترونية الكامل (نموذج بيانات التقارير الإلكترونية، وتكوينا تعيين نموذج التقارير الإلكترونية، وتكوين تنسيق التقارير الإلكترونية) إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="0dfea-505">I then imported the whole ER solution (ER data model, two ER model mapping configurations, and ER format configuration) into Finance.</span></span> <span data-ttu-id="0dfea-506">لماذا أتلقى رسالة خطا عند محاولة تشغيل نفس تنسيق التقارير الإلكترونية في Finance؟</span><span class="sxs-lookup"><span data-stu-id="0dfea-506">Why do I receive an error message when I try to run the same ER format in Finance?</span></span>
<span data-ttu-id="0dfea-507">إعداد تعيين النموذج الافتراضي خاص بالبيئة.</span><span class="sxs-lookup"><span data-stu-id="0dfea-507">The default model mapping setting is environment-specific.</span></span> <span data-ttu-id="0dfea-508">تم تكوينه في RCS ولكن لم يتم تصديره إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="0dfea-508">It's configured in RCS but isn't exported to Finance.</span></span> <span data-ttu-id="0dfea-509">لتشغيل تنسيق التقارير الإلكترونية بنجاح، يجب عليك وضع علامة على أحد تكوينات تعيين نموذج التقارير الإلكترونية كتكوين تعيين النموذج الافتراضي في Finance أيضا.</span><span class="sxs-lookup"><span data-stu-id="0dfea-509">To successfully run this ER format, you must mark one of ER model mapping configurations as the default model mapping configuration in Finance too.</span></span>

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a><span data-ttu-id="0dfea-510">لقد قمت بتكوين تعيين نموذج واحد كتعيين نموذج مشترك وأكملت إصدار المسودة له.</span><span class="sxs-lookup"><span data-stu-id="0dfea-510">I configured one model mapping as a shared model mapping and completed the draft version of it.</span></span> <span data-ttu-id="0dfea-511">بعد ذلك قمت باضافه تكوين تعيين نموذج جديد لنفس نموذج البيانات وتكوينه كخاص بالفرنسية.</span><span class="sxs-lookup"><span data-stu-id="0dfea-511">I then added a new model mapping configuration for same data model and configured it as French-specific.</span></span> <span data-ttu-id="0dfea-512">لماذا يتم تحديد تعيين النموذج المشترك عند تشغيل تنسيق التقارير الإلكترونية، حتى إذا كان هذا التنسيق للتقارير الإلكترونية يستخدم تعريف الجذر الصحيح وتم اجراء التنفيذ ضمن التحكم في الشركة التي لها سياق بلد/منطقه فرنسية؟</span><span class="sxs-lookup"><span data-stu-id="0dfea-512">Why is the shared model mapping selected when I run an ER format, even though this ER format uses the correct root definition and execution is done under the control of the company that has French country/region context?</span></span>
<span data-ttu-id="0dfea-513">تأكد من أن تكوين تعيين النموذج المشترك لم يتم وضع علامة عليه علي أنه تكوين تعيين النموذج الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="0dfea-513">Make sure that the shared model mapping configuration isn't marked as the default model mapping configuration.</span></span> <span data-ttu-id="0dfea-514">والا سيكون له اولويه أعلى أثناء تحديد التعيين.</span><span class="sxs-lookup"><span data-stu-id="0dfea-514">Otherwise, it will have higher priority during mapping selection.</span></span> <span data-ttu-id="0dfea-515">وتأكد أيضا من مراعاه تكوين تعيين النموذج الخاص بالفرنسية عند تحديد تعيين أثناء تنفيذ تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0dfea-515">Also make sure that the French-specific model mapping configuration is considered when a mapping is selected during ER format execution.</span></span> <span data-ttu-id="0dfea-516">يتوفر تكوين لتعيين نموذج تقارير إلكترونية للتحديد فقط في حاله تحقق أحد الشروط التالية على الأقل:</span><span class="sxs-lookup"><span data-stu-id="0dfea-516">An ER model mapping configuration is available for selection only if at least one of the following conditions is met:</span></span>
- <span data-ttu-id="0dfea-517">إصدار واحد على الأقل من تكوين تعيين نموذج التقارير الإلكترونية بالحالة **مكتمل** أو **مشترك**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-517">At least one version of the ER model mapping configuration has either **Completed** or **Shared** status.</span></span> <span data-ttu-id="0dfea-518">في هذه الحالة، سيتم استخدام الإصدار الذي يحتوي على رقم الإصدار الأعلى لتنفيذ تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0dfea-518">In this case, the version that has the highest version number will be used for ER format execution.</span></span>
- <span data-ttu-id="0dfea-519">تم تشغيل خيار **تشغيل المسودة** لتكوين تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0dfea-519">The **Run draft** option for the ER model mapping configuration is turned on.</span></span> <span data-ttu-id="0dfea-520">في هذه الحالة، سيتم استخدام الإصدار الذي له حالة **المسودة** لتنفيذ تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0dfea-520">In this case, the version that has **Draft** status will be used for ER format execution.</span></span>
> <span data-ttu-id="0dfea-521">يتوفر خيار **تشغيل المسودة** في صفحة **التكوينات** لكل تكوين تعيين نموذج تقارير إلكترونية عند تشغيل معلمة مستخدم التقارير الإلكترونية **تشغيل الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="0dfea-521">The **Run draft** option becomes available on the **Configurations** page for each ER model mapping configuration when the **Run setting** ER user parameter is turned on.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]