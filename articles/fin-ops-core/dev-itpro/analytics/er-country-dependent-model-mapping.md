---
title: تكوين تعيينات نماذج التقارير الإلكترونية التابعة لسياقات البلدان
description: يشرح هذا الموضوع كيفيه اعداد تعيينات نماذج التقارير الإلكترونية لكي تعتمد علي سياق البلد/المنطقة الخاص بالكيان القانوني الذي يتحكم في استخدامه.
author: NickSelin
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: 6c4b18a3cf2ba313756d5f761ef1beb2c3015516
ms.sourcegitcommit: 56add4c49c35c65a75fa2ca5234927e7f7cd66ef
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/11/2019
ms.locfileid: "2781135"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a><span data-ttu-id="2b36c-103">تكوين تعيينات نماذج التقارير الإلكترونية التابعة لسياقات البلدان</span><span class="sxs-lookup"><span data-stu-id="2b36c-103">Configure country context dependent ER model mappings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2b36c-104">يمكنك تكوين تعيينات نماذج التقارير الكترونيه (ER) بحيث تقوم بتطبيق نموذج بيانات تقارير إلكترونية عام ولكنه خاص بـ Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="2b36c-104">You can configure Electronic reporting (ER) model mappings so that they implement a generic ER data model but are specific to Dynamics 365 Finance.</span></span> <span data-ttu-id="2b36c-105">يشرح هذا الموضوع كيفيه تصميم تعيينات نماذج تقارير إلكترونية متعددة لنموذج بيانات تقرير إلكترونية للتحكم في كيفيه استخدامها بواسطة تنسيقات التقارير الإلكترونية المقابلة التي يتم تشغيلها من الشركات التي لها سياقات بلد/منطقه مختلفه.</span><span class="sxs-lookup"><span data-stu-id="2b36c-105">This topic explains how to design multiple ER model mappings for an ER data model to control how they are used by corresponding ER formats that are run from companies that have different country/region contexts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2b36c-106">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="2b36c-106">Prerequisites</span></span>

<span data-ttu-id="2b36c-107">لإكمال الأمثلة في هذا الموضوع، يجب أن يكون لديك الوصول التالي:</span><span class="sxs-lookup"><span data-stu-id="2b36c-107">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="2b36c-108">الوصول إلى Finance لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="2b36c-108">Access to Finance for one of the following roles:</span></span>
    - <span data-ttu-id="2b36c-109">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="2b36c-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="2b36c-110">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="2b36c-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="2b36c-111">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="2b36c-111">System administrator</span></span>

- <span data-ttu-id="2b36c-112">يمكنك الوصول إلى مثيل خدمات التكوين التنظيمية (RCS) التي تم توفيرها لنفس المستأجر مثل التمويل لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="2b36c-112">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>
    - <span data-ttu-id="2b36c-113">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="2b36c-113">Electronic reporting developer</span></span>
    - <span data-ttu-id="2b36c-114">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="2b36c-114">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="2b36c-115">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="2b36c-115">System administrator</span></span>

<span data-ttu-id="2b36c-116">تتطلب بعض الخطوات الواردة في هذا الموضوع تنفيذ تنسيق تقارير إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2b36c-116">Some steps in this topic require execution of an ER format.</span></span> <span data-ttu-id="2b36c-117">في بعض الحالات، يتاثر تنفيذ التنسيق الخاص بالتقارير الإلكترونية بسياق البلد/المنطقة للشركة التي تقوم بتسجيل الدخول إليها حاليا.</span><span class="sxs-lookup"><span data-stu-id="2b36c-117">In some cases, execution of an ER format is affected by the country/region context of the company that you're currently signed in to.</span></span> <span data-ttu-id="2b36c-118">يمكنك تشغيل تنسيق التقارير الإلكترونية في مثيل RCS الحالي إذا كانت الشركة التي لها سياق البلد/المنطقة المطلوب متوفرة في RCS.</span><span class="sxs-lookup"><span data-stu-id="2b36c-118">You can run an ER format in the current RCS instance if the company that has the required country/region context is available in RCS.</span></span> <span data-ttu-id="2b36c-119">وبخلاف ذلك، يجب تحميل إصدار مكتمل من تعيين نموذج التقارير الإلكترونية وتكوينات تنسيق التقارير الإلكترونية التي تستخدم نموذج البيانات التقارير الإلكترونية إلى مثيل التمويل الخاص بك، ثم قم بتشغيل تنسيق التقارير الإلكترونية في مثيل التمويل هذا.</span><span class="sxs-lookup"><span data-stu-id="2b36c-119">Otherwise, you must upload a completed version of the ER model mapping and ER format configurations that use the ER data model to your Finance instance, and then run the ER format in that Finance instance.</span></span> <span data-ttu-id="2b36c-120">للحصول علي معلومات حول كيفيه استيراد التكوينات التي توجد في RCS إلى مثيل تمويل، راجع [استيراد التكوينات من RCS](rcs-download-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="2b36c-120">For information about how to import configurations that reside in RCS into a Finance instance, see [Import configurations from RCS](rcs-download-configurations.md).</span></span>

## <a name="single-model-mapping-case"></a><span data-ttu-id="2b36c-121">حاله تعيين نموذج واحد</span><span class="sxs-lookup"><span data-stu-id="2b36c-121">Single model mapping case</span></span>

<span data-ttu-id="2b36c-122">اتبع الخطوات الواردة في [الملحق 1](#appendix1) من هذا الموضوع لتصميم مكونات التقارير الإلكترونية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-122">Follow the steps in [Appendix 1](#appendix1) of this topic to design the required ER components.</span></span> <span data-ttu-id="2b36c-123">لديك الآن تكوين تعيين نموذج **التعيين (عام)** الذي يحتوي على تعيين النموذج لتعريف **نقطة الإدخال 1**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-123">You now have the **Mapping (General)** model mapping configuration that contains the model mapping for the **Entry point 1** definition.</span></span>

![صفحة تكوينات التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="2b36c-125">تشغيل التنسيق المكوَّن</span><span class="sxs-lookup"><span data-stu-id="2b36c-125">Run the configured format</span></span>

1.  <span data-ttu-id="2b36c-126">في **صفحة التكوينات**، في علامة التبويب السريع **الإصدارات**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-126">On the **Configurations page**, on the **Versions** FastTab, select **Run**.</span></span>
2.  <span data-ttu-id="2b36c-127">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-127">Select **OK**.</span></span>

<span data-ttu-id="2b36c-128">لاحظ أن مستعرض الويب يعرض تنزيل الملف النصي الذي تم إنشاؤه بواسطة تنسيق التقارير الإلكترونية الذي تم تنفيذه.</span><span class="sxs-lookup"><span data-stu-id="2b36c-128">Notice that the web browser offers to download the text file that was generated by executed ER format.</span></span> <span data-ttu-id="2b36c-129">بسبب تكوين هذا التنسيق لاستخدام **تعريف نقطه الإدخال 1**، وتعيين نموذج واحد فقط متوفر حاليا للنموذج الأساسي الذي يحتوي علي تعيين لهذا التعريف ، فان تنسيق التقارير الإلكترونية الذي تم تنفيذه استخدم تعيين نموذج **التعيين (عام)** لتكوين **التعيين (عام)** كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="2b36c-129">Because this format was configured to use the **Entry point 1** definition, and only a single model mapping is currently available for the base model that contains a mapping for this definition, the executed ER format used the **Mapping (General)** model mapping of the **Mapping (General)** configuration as a data source.</span></span> <span data-ttu-id="2b36c-130">لذلك ، يحتوي الملف الذي تم تنزيله علي **نص الوظيفة العامة 1**</span><span class="sxs-lookup"><span data-stu-id="2b36c-130">Therefore, the downloaded file contains the **Generic functionality 1** text.</span></span>

## <a name="multiple-shared-model-mappings-case"></a><span data-ttu-id="2b36c-131">حاله تعيينات متعددة النماذج المشتركة</span><span class="sxs-lookup"><span data-stu-id="2b36c-131">Multiple shared model mappings case</span></span>

<span data-ttu-id="2b36c-132">اتبع الخطوات الواردة في [الملحق 2](#appendix2) من هذا الموضوع لتصميم مكونات التقارير الإلكترونية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-132">Follow the steps in [Appendix 2](#appendix2) of this topic to design the required ER components.</span></span> <span data-ttu-id="2b36c-133">لديك الآن تكوينات تعيين نموذج **التعيين (عام)** و**التعيين المخصص (عام)**، والتي يحتوي كل منها على تعيين النموذج لتعريف **نقطة الإدخال 1**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-133">You now have **Mapping (General)** and **Mapping (General) custom** model mapping configurations, each of which contains the model mapping for the **Entry point 1** definition.</span></span>

![صفحة تكوينات التقارير الإلكترونية](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="2b36c-135">تشغيل التنسيق المكوَّن</span><span class="sxs-lookup"><span data-stu-id="2b36c-135">Run the configured format</span></span>

1.  <span data-ttu-id="2b36c-136">في صفحة **التكوينات**، في شجرة التكوينات، حدد عنصر **التنسيق للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-136">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="2b36c-137">في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-137">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="2b36c-138">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-138">Select **OK**.</span></span>

<span data-ttu-id="2b36c-139">لاحظ ان تنفيذ تنسيق التقارير الإلكترونية المحدد غير ناجح.</span><span class="sxs-lookup"><span data-stu-id="2b36c-139">Notice that execution of the selected ER format is unsuccessful.</span></span> <span data-ttu-id="2b36c-140">تظهر رسالة خطا لاعلامك بوجود أكثر من تعيين نموذج واحد لنموذج **النموذج للتعرف على التعيينات** وتعريف **نقطة الإخال 1** في **التعيين (عام)** وتكوينات تعيين نموذج **التعيين المخصص (عام)**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-140">An error message informs you that more than one model mapping exists for the **Model to learn mappings** model and the **Entry point 1** definition in the **Mapping (General)** and **Mapping (General) custom** model mapping configurations.</span></span> <span data-ttu-id="2b36c-141">وتوصي الرسالة أيضا بتحديد أحد هذه التكوينات كتكوين افتراضي.</span><span class="sxs-lookup"><span data-stu-id="2b36c-141">The message also recommends that you select one of those configurations as the default configuration.</span></span>

![صفحة تكوينات التقارير الإلكترونية](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a><span data-ttu-id="2b36c-143">تحديد تكوين افتراضي للتعيين</span><span class="sxs-lookup"><span data-stu-id="2b36c-143">Define a default mapping configuration</span></span>

<span data-ttu-id="2b36c-144">اتبع الخطوات التالية **لتعريف تكوين تعيين** نموذج مخصص (عام) كتكوين افتراضي ، بحيث يمكن استخدام التعيينات الخاصة بها كمصادر بيانات للتنسيق الذي يمكن من خلاله **التعرف علي تنسيق التعيينات** ل ER.</span><span class="sxs-lookup"><span data-stu-id="2b36c-144">Follow these steps to define the **Mapping (General) custom** model mapping configuration as the default configuration, so that its mappings can be used as data sources for the **Format to learn mappings** ER format.</span></span>

1.  <span data-ttu-id="2b36c-145">في صفحة **التكوينات**، في شجرة التكوينات، حدد **التعيين المخصص (عام)**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-145">On the **Configurations** page, in the configurations tree, select **Mapping (General) custom**.</span></span>
2.  <span data-ttu-id="2b36c-146">حسب الحاجة، حدد **تحرير** لتجعل الصفحة الحالية جاهزه للتحرير.</span><span class="sxs-lookup"><span data-stu-id="2b36c-146">As required, select **Edit** to make the current page ready for editing.</span></span>
3.  <span data-ttu-id="2b36c-147">قم بتعيين الخيار **الاعداد الافتراضي لتعيين النموذج** إلى **نعم.**</span><span class="sxs-lookup"><span data-stu-id="2b36c-147">Set the **Default for model mapping** option to **Yes**.</span></span>
4.  <span data-ttu-id="2b36c-148">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-148">Select **Save**.</span></span>

![صفحة تكوينات التقارير الإلكترونية](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="2b36c-150">تشغيل التنسيق المكوَّن</span><span class="sxs-lookup"><span data-stu-id="2b36c-150">Run the configured format</span></span>

1.  <span data-ttu-id="2b36c-151">في صفحة **التكوينات**، في شجرة التكوينات، حدد عنصر **التنسيق للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-151">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="2b36c-152">في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-152">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="2b36c-153">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-153">Select **OK**.</span></span>

<span data-ttu-id="2b36c-154">لاحظ ان تنفيذ تنسيق التقارير الإلكترونية المحدد ناجح.</span><span class="sxs-lookup"><span data-stu-id="2b36c-154">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="2b36c-155">مستعرض الويب يعرض تنزيل الملف النصي الذي تم إنشاؤه بواسطة تنسيق التقارير الإلكترونية الذي تم تنفيذه.</span><span class="sxs-lookup"><span data-stu-id="2b36c-155">The web browser offers to download the text file that was generated by executed ER format.</span></span> <span data-ttu-id="2b36c-156">بسبب تكوين هذا التنسيق لاستخدام تعريف **نقطة الإدخال 1**، تم تحديد تكوين تعيين نموذج **التعيين المخصص (عام)** باعتباره التكوين الافتراضي، واستخدم تنسيق التقارير الإلكترونية المنفذ تعيين نموذج **نسخة التعيين (عام)** لتكوين **التعيين المخصص** كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="2b36c-156">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (General) custom** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (General) copy** model mapping of the **Mapping (General) custom** configuration as a data source.</span></span> <span data-ttu-id="2b36c-157">لذلك، يحتوي الملف الذي تم تنزيله على **الوظيفة العامة المخصصة 1**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-157">Therefore, the downloaded file contains the **Generic functionality 1 custom** text.</span></span>

> [!NOTE]
> <span data-ttu-id="2b36c-158">إذا قمت بتغيير الشركة التي قمت بتسجيل الدخول اليها حاليا وتشغيل تنسيق التقارير الإلكترونية هذا مره أخرى ، ستحصل علي نفس المحتوي في الملف الذي تم إنشاؤه ، لان تكوين تعيين نموذج التقارير الإكترونية الافتراضي لا يحتوي علي إيه قيود تعتمد علي الشركة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-158">If you change the company that you're currently signed in to and run this ER format again, you get the same content in the generated file, because the default ER model mapping configuration doesn't contain any company-dependent restrictions.</span></span>

## <a name="multiple-mixed-model-mappings-case"></a><span data-ttu-id="2b36c-159">حاله تعيينات متعددة النماذج المختلطة</span><span class="sxs-lookup"><span data-stu-id="2b36c-159">Multiple mixed model mappings case</span></span>

<span data-ttu-id="2b36c-160">اتبع الخطوات الواردة في [الملحق 3](#appendix3) من هذا الموضوع لتصميم مكونات التقارير الإلكترونية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-160">Follow the steps in [Appendix 3](#appendix3) of this topic to design the required ER components.</span></span> <span data-ttu-id="2b36c-161">لديك الآن تكوينات **التعيين (عام)**، و**التعيين المخصص (عام)**، و**تعيين نموذج التعيين (FR)** التي تحتوي على تعيين النموذج لتعريف **نقطة الإدخال 1**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-161">You now have **Mapping (General)**, **Mapping (General) custom**, and **Mapping (FR) model mapping** configurations that contain the model mapping for the **Entry point 1** definition.</span></span>

<span data-ttu-id="2b36c-162">لاحظ ان الإصدار 1 من تكوين تعيين النموذج **التعيين (FR)** تم تكوينه بحيث يتم تطبيقه فقط علي تنسيقات التقارير الإلكترونية لنموذج **النموذج للتعرف على التعيينات** الذي يعمل في شركات Finance التي لها سياق بلد/منطقه فرنسية.</span><span class="sxs-lookup"><span data-stu-id="2b36c-162">Notice that version 1 of the **Mapping (FR)** model mapping configuration is configured so that it applies only to ER formats of the **Model to learn mappings** model that are run in Finance companies that have French country/region context.</span></span>

![صفحة تكوينات التقارير الإلكترونية](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="2b36c-164">تشغيل التنسيق المكوَّن</span><span class="sxs-lookup"><span data-stu-id="2b36c-164">Run the configured format</span></span>

1.  <span data-ttu-id="2b36c-165">قم بتغيير الشركة إلى **FRSI**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-165">Change the company to **FRSI**.</span></span>
2.  <span data-ttu-id="2b36c-166">في صفحة **التكوينات**، في شجرة التكوينات، حدد عنصر **التنسيق للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-166">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
3.  <span data-ttu-id="2b36c-167">في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-167">On the **Versions** FastTab, select **Run**.</span></span>
4.  <span data-ttu-id="2b36c-168">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-168">Select **OK**.</span></span>

<span data-ttu-id="2b36c-169">لاحظ ان تنفيذ تنسيق التقارير الإلكترونية المحدد ناجح.</span><span class="sxs-lookup"><span data-stu-id="2b36c-169">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="2b36c-170">مستعرض الويب يعرض تنزيل الملف النصي الذي تم إنشاؤه بواسطة تنسيق التقارير الإلكترونية الذي تم تنفيذه.</span><span class="sxs-lookup"><span data-stu-id="2b36c-170">The web browser offers to download the text file that was generated by the executed ER format.</span></span> <span data-ttu-id="2b36c-171">بسبب تكوين هذا التنسيق لاستخدام تعريف **نقطة الإدخال 1**، تم تحديد تكوين تعيين نموذج **التعيين المخصص (عام)** باعتباره التكوين الافتراضي، واستخدم تنسيق التقارير الإلكترونية المنفذ تعيين نموذج **نسخة التعيين (عام)** لتكوين **التعيين المخصص** كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="2b36c-171">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (General) custom** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (General) copy** model mapping of the **Mapping (General) custom** configuration as a data source.</span></span> <span data-ttu-id="2b36c-172">لذلك، يحتوي الملف الذي تم تنزيله على **الوظيفة العامة المخصصة 1**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-172">Therefore, the downloaded file contains the **Generic functionality 1 custom** text.</span></span>

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a><span data-ttu-id="2b36c-173">حدد تكوين التعيين الخاص بفرنسا كتكوين افتراضي</span><span class="sxs-lookup"><span data-stu-id="2b36c-173">Define the France-specific mapping configuration as the default configuration</span></span>

<span data-ttu-id="2b36c-174">اتبع الخطوات التالية لتحديد تكوين تعيين نموذج **التعيين (FR)** باعتباره التكوين الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="2b36c-174">Follow these steps to define the custom **Mapping (FR)** model mapping configuration as the default configuration.</span></span> <span data-ttu-id="2b36c-175">لاحظ انه نظرا لان هذا التعيين مخصص لفرنسا، فانه سيتم اعتباره التعيين الافتراضي بين كافة تكوينات تعيينات النماذج التي تشتمل على كود البلد **FR** في حقل **أكواد البلد/المنطقة ISO**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-175">Note that, because this mapping is specific to France, it will be considered the default mapping between all model mapping configurations that have the **FR** country code specified in the **ISO country/region codes** field.</span></span>

1.  <span data-ttu-id="2b36c-176">في صفحة **التكوينات**، في شجرة التكوينات، حدد **التعيين (FR)**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-176">On the **Configurations** page, in the configurations tree, select **Mapping (FR)**.</span></span>
2.  <span data-ttu-id="2b36c-177">حسب الحاجة، حدد **تحرير** لتجعل الصفحة الحالية جاهزه للتحرير.</span><span class="sxs-lookup"><span data-stu-id="2b36c-177">As required, select **Edit** to make the current page ready for editing.</span></span>
3.  <span data-ttu-id="2b36c-178">قم بتعيين الخيار **الاعداد الافتراضي لتعيين النموذج** إلى **نعم.**</span><span class="sxs-lookup"><span data-stu-id="2b36c-178">Set the **Default for model mapping** option to **Yes**.</span></span>
4.  <span data-ttu-id="2b36c-179">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-179">Select **Save**.</span></span>

![صفحة تكوينات التقارير الإلكترونية](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="2b36c-181">تشغيل التنسيق المكوَّن</span><span class="sxs-lookup"><span data-stu-id="2b36c-181">Run the configured format</span></span>

1.  <span data-ttu-id="2b36c-182">في صفحة **التكوينات**، في شجرة التكوينات، حدد عنصر **التنسيق للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-182">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="2b36c-183">في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-183">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="2b36c-184">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-184">Select **OK**.</span></span>

<span data-ttu-id="2b36c-185">لاحظ ان تنفيذ تنسيق التقارير الإلكترونية المحدد ناجح.</span><span class="sxs-lookup"><span data-stu-id="2b36c-185">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="2b36c-186">مستعرض الويب يعرض تنزيل الملف النصي الذي تم إنشاؤه بواسطة تنسيق التقارير الإلكترونية الذي تم تنفيذه.</span><span class="sxs-lookup"><span data-stu-id="2b36c-186">The web browser offers to download the text file that was generated by the executed ER format.</span></span> <span data-ttu-id="2b36c-187">بسبب تكوين هذا التنسيق لاستخدام تعريف **نقطة الإدخال 1**، تم تحديد تكوين تعيين نموذج **التعيين (FR)** باعتباره التكوين الافتراضي، واستخدم تنسيق التقارير الإلكترونية المنفذ تعيين نموذج **التعيين (FR)** لتكوين **التعيين (FR)** كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="2b36c-187">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (FR)** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (FR)** model mapping of the **Mapping (FR)** configuration as a data source.</span></span> <span data-ttu-id="2b36c-188">لذلك ، يحتوي الملف الذي تم تنزيله علي **وظيفة FR 1**</span><span class="sxs-lookup"><span data-stu-id="2b36c-188">Therefore, the downloaded file contains the **FR functionality 1** text.</span></span>

> [!NOTE]
> <span data-ttu-id="2b36c-189">في حاله تغيير الشركة التي قمت بتسجيل الدخول اليها حاليا وتشغيل تنسيق التقارير الإلكترونية هذا مره أخرى ، سيعتمد الإخراج علي سياق البلد/المنطقة الخاص بالشركة المحددة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-189">If you change the company that you're currently signed in to and run this ER format again, the output will depend on the country/region context of the selected company.</span></span>

## <a name="other-model-mapping-cases"></a><span data-ttu-id="2b36c-190">حاله تعيينات النماذج الأخرى</span><span class="sxs-lookup"><span data-stu-id="2b36c-190">Other model mapping cases</span></span>

<span data-ttu-id="2b36c-191">وكما شاهدت، فان تحديد تعيين النموذج لتنفيذ تنسيق التقارير الإلكترونية يعمل بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="2b36c-191">As you've seen, the selection of a model mapping for the execution of an ER format works in the following way:</span></span>

- <span data-ttu-id="2b36c-192">يتم تحديد تعريف تعيين النموذج الذي يستخدمه تنسيق التقارير الإلكترونية **(نقطه الإدخال 1** في الأمثله الموجودة في هذا الموضوع).</span><span class="sxs-lookup"><span data-stu-id="2b36c-192">The model mapping definition that an ER format uses is specified (**Entry point 1** in the examples in this topic).</span></span>
- <span data-ttu-id="2b36c-193">يمكن استخدام كافة تكوينات التعيين التي تحتوي على تعيين لديه التعريف المحدد، والتي تفي بقيود سياق البلد/المنطقة التي تم تكوينها لتشغيل تنسيق التقارير الإلكترونية (**التعيين (عام)**، و**التعيين المخصص (عام)**، و**التعيين (FR)** في الأمثله الواردة في هذا الموضوع).</span><span class="sxs-lookup"><span data-stu-id="2b36c-193">All mapping configurations that contain a mapping that has the specified definition, and that satisfy any country/region context restrictions that are configured, can potentially be used to run the ER format (**Mapping (General)**, **Mapping (General) custom**, and **Mapping (FR)** in the examples in this topic).</span></span>
- <span data-ttu-id="2b36c-194">ويكون لأي تعيين نموذج افتراضي له قيود علي سياق البلد/المنطقة أعلى أولوية للتحديد (**التعيين (FR)** في الأمثله الموجودة في هذا الموضوع).</span><span class="sxs-lookup"><span data-stu-id="2b36c-194">Any default model mapping that has country/region context restrictions has the highest priority for selection (**Mapping (FR)** in the examples in this topic).</span></span>
- <span data-ttu-id="2b36c-195">ويكون لأي تعيين نموذج افتراضي لا يشتمل على قيود سياق البلد/المنطقة الأولوية الأعلى التالية (**التعيين المخصص (عام)** في الأمثله الموجودة في هذا الموضوع).</span><span class="sxs-lookup"><span data-stu-id="2b36c-195">Any default model mapping that doesn't have country/region context restrictions has the next higher priority for selection  (**Mapping (General) custom** in the examples in this topic).</span></span>
- <span data-ttu-id="2b36c-196">ان اي تعيين نموذج له قيود علي سياق البلد/المنطقة له اولويه اعلي للتحديد مقارنةً بتعيين نموذج ليس له قيود علي سياق البلد/المنطقة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-196">Any model mapping that has country/region context restrictions has higher priority for selection than a model mapping that doesn't have country/region context restrictions.</span></span>

<span data-ttu-id="2b36c-197">يوفر الجدول التالي معلومات حول نتائج تحديد تعيين النماذج لكافة الحالات المحتملة لإعدادات تعيين النماذج:</span><span class="sxs-lookup"><span data-stu-id="2b36c-197">The following table provides information about the results of model mapping selection for all possible cases for model mapping settings:</span></span>

- <span data-ttu-id="2b36c-198">يشير العمود 1 إلى ما إذا كان التعيين الأول للنموذج الذي ليس له قيود على سياق البلد/المنطقة (على سبيل المثال، تعيين **التعيين (عام)**) موجودًا، وإذا كان الأمر كذلك، وما إذا كان تم تعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم** له.</span><span class="sxs-lookup"><span data-stu-id="2b36c-198">Column 1 indicates whether the first model mapping that doesn't have country/region context restrictions (for example, the shared **Mapping (General)** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="2b36c-199">يشير العمود 2 إلى ما إذا كان التعيين الثاني للنموذج الذي ليس له قيود على سياق البلد/المنطقة (على سبيل المثال، تعيين **التعيين المخصص (عام)**) موجودًا، وإذا كان الأمر كذلك، وما إذا كان تم تعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم** له.</span><span class="sxs-lookup"><span data-stu-id="2b36c-199">Column 2 indicates whether the second model mapping that doesn't have country/region context restrictions (for example, the shared **Mapping (General) custom** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="2b36c-200">يشير العمود 3 إلى ما إذا كان التعيين الأول للنموذج يشتمل على قيود على سياق البلد/المنطقة A (على سبيل المثال، تعيين **التعيين (FR)** الخاص بفرنسا) موجودًا، وإذا كان الأمر كذلك، وما إذا كان تم تعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم** له.</span><span class="sxs-lookup"><span data-stu-id="2b36c-200">Column 3 indicates whether the first model mapping that has country/region A context restrictions (for example, the France-specific **Mapping (FR)** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="2b36c-201">يشير العمود 4 إلى ما إذا كان التعيين الثاني للنموذج يشتمل على قيود على سياق البلد/المنطقة A موجودًا، وإذا كان الأمر كذلك، وما إذا كان تم تعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم** له.</span><span class="sxs-lookup"><span data-stu-id="2b36c-201">Column 4 indicates whether the second model mapping that has country/region A context restrictions is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="2b36c-202">يقدم العمود رقم 5 النتيجة الخاصة بتحديد تعيين النموذج لتنفيذ أحد تنسيقات التقارير الإلكترونية ضمن التحكم في الشركة التي لها سياق A للمنطقه/البلد.</span><span class="sxs-lookup"><span data-stu-id="2b36c-202">Column 5 presents the result of a model mapping selection for execution of an ER format under the control of a company that has country/region A context.</span></span>
- <span data-ttu-id="2b36c-203">يقدم العمود رقم 6 النتيجة الخاصة بتحديد تعيين النموذج لتنفيذ أحد تنسيقات التقارير الإلكترونية ضمن التحكم في الشركة التي لها سياق B للمنطقه/البلد.</span><span class="sxs-lookup"><span data-stu-id="2b36c-203">Column 6 presents the result of a model mapping selection for execution of an ER format under the control of a company that has country/region B context.</span></span>

<span data-ttu-id="2b36c-204">وتشير علامة الجمع (+) في الجدول إلى وجود تكوين تعيين النموذج في المثيل الحالي لخدمة Microsoft Azure المستخدمة لتشغيل تنسيق التقارير الإلكترونية (إما Finance أو RCS).</span><span class="sxs-lookup"><span data-stu-id="2b36c-204">In the table, a plus sign (+) indicates the presence of a model mapping configuration in the current instance of the Microsoft Azure service that is used to run an ER format (either Finance or RCS).</span></span>

| <span data-ttu-id="2b36c-205">الحالة</span><span class="sxs-lookup"><span data-stu-id="2b36c-205">Case</span></span> | <span data-ttu-id="2b36c-206">تعيين النموذج 1 دون سياق البلد/المنطقة (MM1)</span><span class="sxs-lookup"><span data-stu-id="2b36c-206">Model mapping 1 without country/region context (MM1)</span></span> | <span data-ttu-id="2b36c-207">تعيين النموذج 2 دون سياق البلد/المنطقة (MM2)</span><span class="sxs-lookup"><span data-stu-id="2b36c-207">Model mapping 2 without country/region context (MM2)</span></span> | <span data-ttu-id="2b36c-208">تعيين النموذج 1 مع سياق البلد/المنطقة A (MM1A)</span><span class="sxs-lookup"><span data-stu-id="2b36c-208">Model mapping 1 with country/region A context (MM1A)</span></span> | <span data-ttu-id="2b36c-209">تعيين النموذج 2 مع سياق البلد/المنطقة A (MM2A)</span><span class="sxs-lookup"><span data-stu-id="2b36c-209">Model mapping 2 with country/region A context (MM2A)</span></span> | <span data-ttu-id="2b36c-210">تشغيل ضمن عنصر التحكم في شركه لها سياق منطقه/البلد A</span><span class="sxs-lookup"><span data-stu-id="2b36c-210">Run under control of a company that has country/region A context</span></span> | <span data-ttu-id="2b36c-211">تشغيل ضمن عنصر التحكم في شركه لها سياق منطقه/البلد B</span><span class="sxs-lookup"><span data-stu-id="2b36c-211">Run under the control of a company that has country/region B context</span></span> |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     <span data-ttu-id="2b36c-212">1</span><span class="sxs-lookup"><span data-stu-id="2b36c-212">1</span></span>   |     <span data-ttu-id="2b36c-213">2</span><span class="sxs-lookup"><span data-stu-id="2b36c-213">2</span></span>   |    <span data-ttu-id="2b36c-214">3</span><span class="sxs-lookup"><span data-stu-id="2b36c-214">3</span></span>    |    <span data-ttu-id="2b36c-215">4</span><span class="sxs-lookup"><span data-stu-id="2b36c-215">4</span></span>    |           <span data-ttu-id="2b36c-216">5</span><span class="sxs-lookup"><span data-stu-id="2b36c-216">5</span></span>               |            <span data-ttu-id="2b36c-217">6</span><span class="sxs-lookup"><span data-stu-id="2b36c-217">6</span></span>               |
|     <span data-ttu-id="2b36c-218">1</span><span class="sxs-lookup"><span data-stu-id="2b36c-218">1</span></span>   |         |         |         |         | <span data-ttu-id="2b36c-219">خطأ (تعيين مفقود)</span><span class="sxs-lookup"><span data-stu-id="2b36c-219">Error (missing mapping)</span></span>   | <span data-ttu-id="2b36c-220">خطأ (تعيين مفقود)</span><span class="sxs-lookup"><span data-stu-id="2b36c-220">Error (missing mapping)</span></span>    |
|     <span data-ttu-id="2b36c-221">2</span><span class="sxs-lookup"><span data-stu-id="2b36c-221">2</span></span>   |     +   |         |         |         | <span data-ttu-id="2b36c-222">MM1</span><span class="sxs-lookup"><span data-stu-id="2b36c-222">MM1</span></span>                       | <span data-ttu-id="2b36c-223">MM1</span><span class="sxs-lookup"><span data-stu-id="2b36c-223">MM1</span></span>                        |
|     <span data-ttu-id="2b36c-224">3</span><span class="sxs-lookup"><span data-stu-id="2b36c-224">3</span></span>   |     +   |     +   |         |         | <span data-ttu-id="2b36c-225">خطأ (تعيينات متعددة)</span><span class="sxs-lookup"><span data-stu-id="2b36c-225">Error (multiple mappings)</span></span> | <span data-ttu-id="2b36c-226">خطأ (تعيينات متعددة)</span><span class="sxs-lookup"><span data-stu-id="2b36c-226">Error (multiple mappings)</span></span>  |
|     <span data-ttu-id="2b36c-227">4</span><span class="sxs-lookup"><span data-stu-id="2b36c-227">4</span></span>   |     +   |         |    +    |         | <span data-ttu-id="2b36c-228">MM1A</span><span class="sxs-lookup"><span data-stu-id="2b36c-228">MM1A</span></span>                      | <span data-ttu-id="2b36c-229">MM1</span><span class="sxs-lookup"><span data-stu-id="2b36c-229">MM1</span></span>                        |
|     <span data-ttu-id="2b36c-230">5</span><span class="sxs-lookup"><span data-stu-id="2b36c-230">5</span></span>   |     +   |         |    +    |    +    | <span data-ttu-id="2b36c-231">خطأ (تعيينات متعددة)</span><span class="sxs-lookup"><span data-stu-id="2b36c-231">Error (multiple mappings)</span></span> | <span data-ttu-id="2b36c-232">MM1</span><span class="sxs-lookup"><span data-stu-id="2b36c-232">MM1</span></span>                        |
|     <span data-ttu-id="2b36c-233">6</span><span class="sxs-lookup"><span data-stu-id="2b36c-233">6</span></span>   |     +   | <span data-ttu-id="2b36c-234">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-234">default</span></span> |    +    |    +    | <span data-ttu-id="2b36c-235">MM2</span><span class="sxs-lookup"><span data-stu-id="2b36c-235">MM2</span></span>                       | <span data-ttu-id="2b36c-236">MM2</span><span class="sxs-lookup"><span data-stu-id="2b36c-236">MM2</span></span>                        |
|     <span data-ttu-id="2b36c-237">7</span><span class="sxs-lookup"><span data-stu-id="2b36c-237">7</span></span>   |     +   |         | <span data-ttu-id="2b36c-238">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-238">default</span></span> |         | <span data-ttu-id="2b36c-239">MM1A</span><span class="sxs-lookup"><span data-stu-id="2b36c-239">MM1A</span></span>                      | <span data-ttu-id="2b36c-240">MM1</span><span class="sxs-lookup"><span data-stu-id="2b36c-240">MM1</span></span>                        |
|     <span data-ttu-id="2b36c-241">8</span><span class="sxs-lookup"><span data-stu-id="2b36c-241">8</span></span>   |     +   |         | <span data-ttu-id="2b36c-242">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-242">default</span></span> |    +    | <span data-ttu-id="2b36c-243">MM1A</span><span class="sxs-lookup"><span data-stu-id="2b36c-243">MM1A</span></span>                      | <span data-ttu-id="2b36c-244">MM1</span><span class="sxs-lookup"><span data-stu-id="2b36c-244">MM1</span></span>                        |
|     <span data-ttu-id="2b36c-245">9</span><span class="sxs-lookup"><span data-stu-id="2b36c-245">9</span></span>   |     +   |         | <span data-ttu-id="2b36c-246">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-246">default</span></span> | <span data-ttu-id="2b36c-247">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-247">default</span></span> | <span data-ttu-id="2b36c-248">خطأ (تعيينات متعددة)</span><span class="sxs-lookup"><span data-stu-id="2b36c-248">Error (multiple mappings)</span></span> | <span data-ttu-id="2b36c-249">MM1</span><span class="sxs-lookup"><span data-stu-id="2b36c-249">MM1</span></span>                        |
|    <span data-ttu-id="2b36c-250">10</span><span class="sxs-lookup"><span data-stu-id="2b36c-250">10</span></span>   | <span data-ttu-id="2b36c-251">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-251">default</span></span> |         |         |         | <span data-ttu-id="2b36c-252">MM1</span><span class="sxs-lookup"><span data-stu-id="2b36c-252">MM1</span></span>                       | <span data-ttu-id="2b36c-253">MM1</span><span class="sxs-lookup"><span data-stu-id="2b36c-253">MM1</span></span>                        |
|    <span data-ttu-id="2b36c-254">11</span><span class="sxs-lookup"><span data-stu-id="2b36c-254">11</span></span>   | <span data-ttu-id="2b36c-255">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-255">default</span></span> |    +    |         |         | <span data-ttu-id="2b36c-256">MM1</span><span class="sxs-lookup"><span data-stu-id="2b36c-256">MM1</span></span>                       | <span data-ttu-id="2b36c-257">MM1</span><span class="sxs-lookup"><span data-stu-id="2b36c-257">MM1</span></span>                        |
|    <span data-ttu-id="2b36c-258">12</span><span class="sxs-lookup"><span data-stu-id="2b36c-258">12</span></span>   | <span data-ttu-id="2b36c-259">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-259">default</span></span> |         |    +    |         | <span data-ttu-id="2b36c-260">MM1</span><span class="sxs-lookup"><span data-stu-id="2b36c-260">MM1</span></span>                       | <span data-ttu-id="2b36c-261">MM1</span><span class="sxs-lookup"><span data-stu-id="2b36c-261">MM1</span></span>                        |
|    <span data-ttu-id="2b36c-262">13</span><span class="sxs-lookup"><span data-stu-id="2b36c-262">13</span></span>   | <span data-ttu-id="2b36c-263">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-263">default</span></span> | <span data-ttu-id="2b36c-264">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-264">default</span></span> |         |         | <span data-ttu-id="2b36c-265">خطأ (تعيينات متعددة)</span><span class="sxs-lookup"><span data-stu-id="2b36c-265">Error (multiple mappings)</span></span> | <span data-ttu-id="2b36c-266">خطأ (تعيينات متعددة)</span><span class="sxs-lookup"><span data-stu-id="2b36c-266">Error (multiple mappings)</span></span>  |
|    <span data-ttu-id="2b36c-267">14</span><span class="sxs-lookup"><span data-stu-id="2b36c-267">14</span></span>   | <span data-ttu-id="2b36c-268">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-268">default</span></span> |         | <span data-ttu-id="2b36c-269">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-269">default</span></span> |         | <span data-ttu-id="2b36c-270">MM1A</span><span class="sxs-lookup"><span data-stu-id="2b36c-270">MM1A</span></span>                      | <span data-ttu-id="2b36c-271">MM1</span><span class="sxs-lookup"><span data-stu-id="2b36c-271">MM1</span></span>                        |
|    <span data-ttu-id="2b36c-272">15</span><span class="sxs-lookup"><span data-stu-id="2b36c-272">15</span></span>   | <span data-ttu-id="2b36c-273">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-273">default</span></span> |         | <span data-ttu-id="2b36c-274">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-274">default</span></span> | <span data-ttu-id="2b36c-275">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-275">default</span></span> | <span data-ttu-id="2b36c-276">MM1A</span><span class="sxs-lookup"><span data-stu-id="2b36c-276">MM1A</span></span>                      | <span data-ttu-id="2b36c-277">MM2A</span><span class="sxs-lookup"><span data-stu-id="2b36c-277">MM2A</span></span>                       |
|    <span data-ttu-id="2b36c-278">16</span><span class="sxs-lookup"><span data-stu-id="2b36c-278">16</span></span>   |         |         |    +    |    +    | <span data-ttu-id="2b36c-279">MM1A</span><span class="sxs-lookup"><span data-stu-id="2b36c-279">MM1A</span></span>                      | <span data-ttu-id="2b36c-280">MM2A</span><span class="sxs-lookup"><span data-stu-id="2b36c-280">MM2A</span></span>                       |
|    <span data-ttu-id="2b36c-281">17</span><span class="sxs-lookup"><span data-stu-id="2b36c-281">17</span></span>   |         |         | <span data-ttu-id="2b36c-282">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-282">default</span></span> | <span data-ttu-id="2b36c-283">افتراضية</span><span class="sxs-lookup"><span data-stu-id="2b36c-283">default</span></span> | <span data-ttu-id="2b36c-284">MM1A</span><span class="sxs-lookup"><span data-stu-id="2b36c-284">MM1A</span></span>                      | <span data-ttu-id="2b36c-285">MM2A</span><span class="sxs-lookup"><span data-stu-id="2b36c-285">MM2A</span></span>                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a><span data-ttu-id="2b36c-286">التعرف على التعيين الذي تم استخدامه في تنفيذ أحد تنسيقات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2b36c-286">Learn what mapping was used in the execution of an ER format</span></span>

### <a name="configure-er-user-parameters"></a><span data-ttu-id="2b36c-287">تكوين معلمات مستخدم التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2b36c-287">Configure ER user parameters</span></span>

1.  <span data-ttu-id="2b36c-288">في صفحة **التكوينات**، في جزء الإجراء، في علامة التبويب **التكوينات**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-288">On the **Configurations** page, on the Action Pane, on the **CONFIGURATIONS** tab, select **User parameters**.</span></span>
2.  <span data-ttu-id="2b36c-289">قم بتعيين خيار **تشغيل في وضع التصحيح** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-289">Set the **Run in debug mode** option to **Yes**.</span></span>
4.  <span data-ttu-id="2b36c-290">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-290">Select **Ok**.</span></span>

### <a name="run-the-configured-format"></a><span data-ttu-id="2b36c-291">تشغيل التنسيق المكوَّن</span><span class="sxs-lookup"><span data-stu-id="2b36c-291">Run the configured format</span></span>

1.  <span data-ttu-id="2b36c-292">في صفحة **التكوينات**، في شجرة التكوينات، حدد عنصر **التنسيق للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-292">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="2b36c-293">في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-293">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="2b36c-294">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-294">Select **Ok**.</span></span>

### <a name="review-the-er-debug-log"></a><span data-ttu-id="2b36c-295">مراجعة سجل تصحيح التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2b36c-295">Review the ER debug log</span></span>

1.  <span data-ttu-id="2b36c-296">في جزء التنقل، انتقل إلى **الوحدات \> إدارة المؤسسة \> التقارير الإلكترونية \> سجل تصحيح التكوين**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-296">In the navigation pane, go to **Modules \> Organization administration \> Electronic reporting \> Configuration debug log**.</span></span>
2.  <span data-ttu-id="2b36c-297">حدد الزر **إعادة تحميل هذه الصفحة**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-297">Select the **Reload this page** button.</span></span>

![صفحه سجلات تشغيل التقارير الإلكترونية](./media/RCS-Context-specific-mapping-DebugLog.PNG)

<span data-ttu-id="2b36c-299">لاحظ انه تمت أضافه سجل جديد إلى سجل تصحيح التقارير الإلكترونية لتنسيق التقارير الإلكترونية الذي تم تنفيذه.</span><span class="sxs-lookup"><span data-stu-id="2b36c-299">Notice that a new record has been added to the ER debug log for the executed ER format.</span></span> <span data-ttu-id="2b36c-300">ونظرا لأنه يتم تعيين حقل **المستوى** لهذا السجل إلى **معلومات**، يكون السجل معلوماتيًا.</span><span class="sxs-lookup"><span data-stu-id="2b36c-300">Because the **Level** field of this record is set to **Info**, the record is informational.</span></span> <span data-ttu-id="2b36c-301">نظرًا لتعيين حقل مكون التنسيق إلى **تكوين التعيين**، يقوم السجل باعلامك عن تعيين النموذج الذي تم استخدامه أثناء تنفيذ تنسيق التقارير الإلكترونية **التنسيق للتعرف على التعيينات** (المحدد في حقل **اسم التكوين**).</span><span class="sxs-lookup"><span data-stu-id="2b36c-301">Because the Format component field is set to **Mapping configuration**, the record informs you about a model mapping that was used during execution of the **Format to learn mappings** ER format (selected in the **Configuration name** field).</span></span> <span data-ttu-id="2b36c-302">ويعلمك محتوى حقل **النص الذي تم إنشاؤه** بأن مكون تعيين **التعيين (FR)** الموجود في تكوين **التعيين (FR)** تم استخدامه لتشغيل هذا التقرير.</span><span class="sxs-lookup"><span data-stu-id="2b36c-302">The content of the **Generated text** field informs you that the **Mapping (FR)** mapping component that resides in the **Mapping (FR)** configuration has been used to run this report.</span></span>

## <a name="appendix1"></a> <span data-ttu-id="2b36c-303">الملحق 1</span><span class="sxs-lookup"><span data-stu-id="2b36c-303">Appendix 1</span></span>

### <a name="configure-a-sample-data-model"></a><span data-ttu-id="2b36c-304">تكوين نموذج بيانات النموذج</span><span class="sxs-lookup"><span data-stu-id="2b36c-304">Configure a sample data model</span></span>

<span data-ttu-id="2b36c-305">سجل الدخول إلى مثيل RCS.</span><span class="sxs-lookup"><span data-stu-id="2b36c-305">Sign in to your RCS instance.</span></span>

<span data-ttu-id="2b36c-306">في هذا المثال، سوف تنشئ تكوينًا للشركة النموذجية Litware, Inc. ولإكمال هذه الخطوات، يجب عليك أولاً في RCS إكمال الخطوات الموجودة في الإجراء [‏‫إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="2b36c-306">In this example, you will create a configuration for sample company, Litware, Inc. To complete these steps, you must first complete, in RCS, the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

#### <a name="create-an-er-data-model-configuration"></a><span data-ttu-id="2b36c-307">إنشاء تكوين نموذج بيانات تقارير إلكترونية</span><span class="sxs-lookup"><span data-stu-id="2b36c-307">Create an ER data model configuration</span></span>

1.  <span data-ttu-id="2b36c-308">في لوحة المعلومات الافتراضية، حدد **‏‫إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-308">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="2b36c-309">حدد تجانب **تكوينات التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-309">Select the **Reporting configurations** tile.</span></span>
3.  <span data-ttu-id="2b36c-310">في صفحة **التكوينات**، حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-310">On the **Configurations** page, select **Create configuration**.</span></span>
4.  <span data-ttu-id="2b36c-311">في مربع الحوار المنسدل، في حقل **الاسم**، أدخل **النموذج للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-311">In the drop-down dialog box, in the **Name** field, enter **Model to learn mappings**.</span></span>
5.  <span data-ttu-id="2b36c-312">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-312">Select **Create configuration**.</span></span>
6.  <span data-ttu-id="2b36c-313">حدد علامة التبويب السريعة **مكونات التكوين**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-313">Select the **Configuration components** FastTab.</span></span>

<span data-ttu-id="2b36c-314">لاحظ أن إصدار المسودة 1 لتكوين التقارير الإلكترونية هذا جاهز للتحرير.</span><span class="sxs-lookup"><span data-stu-id="2b36c-314">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="2b36c-315">يحتوي هذا الإصدار على مكون نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="2b36c-315">This version contains the data model component.</span></span>

#### <a name="design-a-sample-data-model"></a><span data-ttu-id="2b36c-316">تصميم نموذج بيانات النموذج</span><span class="sxs-lookup"><span data-stu-id="2b36c-316">Design a sample data model</span></span>

1.  <span data-ttu-id="2b36c-317">في **صفحة التكوينات**، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-317">On the **Configurations page**, select **Designer**.</span></span>
2.  <span data-ttu-id="2b36c-318">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-318">Select **New**.</span></span>
3.  <span data-ttu-id="2b36c-319">في مربع الحوار المنسدل، في حقل **الاسم**، أدخل **نقطة الإدخال 1**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-319">In the drop-down dialog box, in the **Name** field, enter **Entry point 1**.</span></span>
4.  <span data-ttu-id="2b36c-320">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-320">Select **Add**.</span></span>
5.  <span data-ttu-id="2b36c-321">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-321">Select **New**.</span></span>
6.  <span data-ttu-id="2b36c-322">في مربع الحوار المنسدل، في حقل **الاسم**، أدخل **وصف الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-322">In the drop-down dialog box, in the **Name** field, enter **Functionality description**.</span></span>
7.  <span data-ttu-id="2b36c-323">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-323">Select **Add**.</span></span>
8.  <span data-ttu-id="2b36c-324">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-324">Select **New**.</span></span>
9.  <span data-ttu-id="2b36c-325">في مربع الحوار المنسدل، في مجموعة حقول **العقدة الجديدة**، حدد **جذر النموذج**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-325">In the drop-down dialog box, in the **New node** field group, select **Model root**.</span></span>
10. <span data-ttu-id="2b36c-326">في حقل **الاسم**، أدخل **نقطة الإدخال 2**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-326">In the **Name** field, enter **Entry point 2**.</span></span>
11. <span data-ttu-id="2b36c-327">حدد **نقطه الإدخال 2**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-327">Select **Entry point 2**.</span></span>
12. <span data-ttu-id="2b36c-328">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-328">Select **Add**.</span></span>
13. <span data-ttu-id="2b36c-329">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-329">Select **New**.</span></span>
14. <span data-ttu-id="2b36c-330">في مربع الحوار المنسدل، في حقل **الاسم**، أدخل **وصف الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-330">In the drop-down dialog box, in the **Name** field, enter **Functionality description**.</span></span>
15. <span data-ttu-id="2b36c-331">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-331">Select **Add**.</span></span>

    ![صفحة مصمم نموذج بيانات التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Model.PNG)

16. <span data-ttu-id="2b36c-333">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-333">Select **Save**.</span></span>
17. <span data-ttu-id="2b36c-334">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-334">Close the page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-configuration"></a><span data-ttu-id="2b36c-335">إكمال الإصدار المعدل من تكوين النموذج</span><span class="sxs-lookup"><span data-stu-id="2b36c-335">Complete the modified version of the model configuration</span></span>

1.  <span data-ttu-id="2b36c-336">في صفحة **التكوينات**، في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-336">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="2b36c-337">قم بتغيير حالة تكوين النموذج المصمم من **مسودة** إلى **مكتمل**، بحيث يمكن استخدامه لتصميم تنسيقات وتعيينات النماذج المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-337">Change the status of designed model configuration from **Draft** to **Completed**, so that it can be used to design the required model mappings and formats.</span></span>

2.  <span data-ttu-id="2b36c-338">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-338">Select **Complete**.</span></span>
3.  <span data-ttu-id="2b36c-339">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-339">Select **OK**.</span></span>

<span data-ttu-id="2b36c-340">لاحظ أن التكوين الذي قمت بإنشائه تم حفظه باعتباره الإصدار المكتمل 1.</span><span class="sxs-lookup"><span data-stu-id="2b36c-340">Notice that the configuration that you created is saved as completed version 1.</span></span>

### <a name="configure-a-sample-model-mapping"></a><span data-ttu-id="2b36c-341">تكوين تعيين نموذج عينة</span><span class="sxs-lookup"><span data-stu-id="2b36c-341">Configure a sample model mapping</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="2b36c-342">إنشاء تكوين تعيين نموذج التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2b36c-342">Create an ER model mapping configuration</span></span>

1.  <span data-ttu-id="2b36c-343">في صفحة **التكوينات**، حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-343">On the **Configurations** page, select **Create configuration**.</span></span>
2.  <span data-ttu-id="2b36c-344">في مربع الحوار المنسدل، في مجموعة الحقل **جديد**، حدد **تعيين النموذج استنادًا إلى نموذج نموذج البيانات للتعرف إلى التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-344">In the drop-down dialog box, in the **New** field group, select **Model mapping based on data model Model to learn mappings**.</span></span>
3.  <span data-ttu-id="2b36c-345">في حقل **الاسم**، أدخل **التعيين (عام)**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-345">In the **Name** field, enter **Mapping (General)**.</span></span>
4.  <span data-ttu-id="2b36c-346">في حقل **تعريف نموذج البيانات**، حدد **نقطة الإدخال 1**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-346">In the **Data model definition** field, select **Entry point 1**.</span></span>
5.  <span data-ttu-id="2b36c-347">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-347">Select **Create configuration**.</span></span>

<span data-ttu-id="2b36c-348">لاحظ أن إصدار المسودة 1 لتكوين التقارير الإلكترونية هذا جاهز للتحرير.</span><span class="sxs-lookup"><span data-stu-id="2b36c-348">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="2b36c-349">يحتوي هذا الإصدار على مكون تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="2b36c-349">This version contains the model mapping component.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="2b36c-350">تصميم تعيين نموذج عينة</span><span class="sxs-lookup"><span data-stu-id="2b36c-350">Design a sample model mapping</span></span>

1.  <span data-ttu-id="2b36c-351">في صفحة **التكوينات**، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-351">On the **Configurations** page, select **Designer**.</span></span>

    <span data-ttu-id="2b36c-352">لاحظ انه تمت أضافه تعيين النموذج من نوع اتجاه **إلى النموذج** تلقائيًا إلى هذا المكون لتعريف **نقطة الإدخال 1**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-352">Notice that the model mapping of the **To model** direction type has been automatically added to this component for the **Entry point 1** definition.</span></span>
    
2.  <span data-ttu-id="2b36c-353">حدد **المصمم** للبدء في تحرير تعيين النموذج المضاف.</span><span class="sxs-lookup"><span data-stu-id="2b36c-353">Select **Designer** to start editing the added model mapping.</span></span>
3.  <span data-ttu-id="2b36c-354">في قسم **نموذج البيانات**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-354">In the **Data model** section, select **Edit**.</span></span>
4.  <span data-ttu-id="2b36c-355">في حقل **المعادلة**، أدخل **"الوظيفة العامة 1"**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-355">In the **Formula** field, enter **"Generic functionality 1"**.</span></span>
5.  <span data-ttu-id="2b36c-356">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-356">Select **Save**.</span></span>
6.  <span data-ttu-id="2b36c-357">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-357">Close the **Formula designer** page.</span></span>

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  <span data-ttu-id="2b36c-359">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-359">Select **Save**.</span></span>
8.  <span data-ttu-id="2b36c-360">أغلق صفحة **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-360">Close the **Model mapping designer** page.</span></span>
9.  <span data-ttu-id="2b36c-361">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-361">Select **New**.</span></span>
10. <span data-ttu-id="2b36c-362">في حقل **التعريف**، حدد **نقطة الإدخال 2**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-362">In the **Definition** field, select **Entry point 2**.</span></span>
11. <span data-ttu-id="2b36c-363">في حقل **الاسم**، أدخل **التعيين (عام) 2**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-363">In the **Name** field, enter **Mapping (General) 2**.</span></span>
12. <span data-ttu-id="2b36c-364">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-364">Select **Designer**.</span></span>
13. <span data-ttu-id="2b36c-365">في قسم **نموذج البيانات**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-365">In the **Data model** section, select **Edit**.</span></span>
14. <span data-ttu-id="2b36c-366">في حقل **المعادلة**، أدخل **"الوظيفة العامة 2"**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-366">In the **Formula** field, enter **"Generic functionality 2"**.</span></span>
15. <span data-ttu-id="2b36c-367">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-367">Select **Save**.</span></span>
16. <span data-ttu-id="2b36c-368">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-368">Close the **Formula designer** page.</span></span>

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. <span data-ttu-id="2b36c-370">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-370">Select **Save**.</span></span>
18. <span data-ttu-id="2b36c-371">أغلق صفحة **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-371">Close the **Model mapping designer** page.</span></span>

    ![صفحة تعيينات نماذج التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. <span data-ttu-id="2b36c-373">أغلق صفحة **تعيينات النماذج**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-373">Close the **Model mappings** page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="2b36c-374">إكمال الإصدار المعدل من تكوين تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="2b36c-374">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="2b36c-375">في **صفحة التكوينات**، في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-375">On the **Configurations page**, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="2b36c-376">قم بتغيير حالة تكوين تعيين النموذج المصمم من **مسودة** إلى **مكتمل**، بحيث يمكن استخدامه بواسطة تنسيقات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2b36c-376">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="2b36c-377">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-377">Select **Complete**.</span></span>
3.  <span data-ttu-id="2b36c-378">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-378">Select **OK**.</span></span>

<span data-ttu-id="2b36c-379">لاحظ أن التكوين الذي تم إنشاؤه تم حفظه باعتباره الإصدار المكتمل 1.</span><span class="sxs-lookup"><span data-stu-id="2b36c-379">Notice that the configuration that is created is saved as completed version 1.</span></span>

### <a name="configure-a-sample-format"></a><span data-ttu-id="2b36c-380">تكوين تنسيق نموذج</span><span class="sxs-lookup"><span data-stu-id="2b36c-380">Configure a sample format</span></span>

#### <a name="create-an-er-format-configuration"></a><span data-ttu-id="2b36c-381">إنشاء تكوين تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2b36c-381">Create an ER format configuration</span></span>

1.  <span data-ttu-id="2b36c-382">في صفحة **التكوينات**، في شجرة التكوينات، حدد **النموذج للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-382">On the **Configurations** page, in the configurations tree, select **Model to learn mappings**.</span></span>
2.  <span data-ttu-id="2b36c-383">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-383">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="2b36c-384">في مربع الحوار المنسدل، في مجموعة الحقل **جديد**، حدد **التنسيق استنادًا إلى نموذج نموذج البيانات للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-384">In the drop-down dialog box, in the **New** field group, select **Format based on data model Model to learn mappings**.</span></span>
4.  <span data-ttu-id="2b36c-385">في حقل **الاسم**، أدخل **التنسيق للتعرف على التعيينات**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-385">In the **Name** field, enter **Format to learn mappings**.</span></span>
5.  <span data-ttu-id="2b36c-386">في حقل **تعريف نموذج البيانات**، حدد **نقطة الإدخال 1**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-386">In the **Data model definition** field, select **Entry point 1**.</span></span>
6.  <span data-ttu-id="2b36c-387">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-387">Select **Create configuration**.</span></span>

<span data-ttu-id="2b36c-388">لاحظ أن إصدار المسودة 1 لتكوين التقارير الإلكترونية هذا جاهز للتحرير.</span><span class="sxs-lookup"><span data-stu-id="2b36c-388">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="2b36c-389">يحتوي هذا الإصدار على مكون التنسيق.</span><span class="sxs-lookup"><span data-stu-id="2b36c-389">This version contains the format component.</span></span>

#### <a name="design-a-sample-format"></a><span data-ttu-id="2b36c-390">تصميم تنسيق نموذج</span><span class="sxs-lookup"><span data-stu-id="2b36c-390">Design a sample format</span></span>

1.  <span data-ttu-id="2b36c-391">في صفحة **التكوينات**، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-391">On the **Configurations** page, select **Designer**.</span></span>
2.  <span data-ttu-id="2b36c-392">حدد **إضافة جذر**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-392">Select **Add root**.</span></span>
3.  <span data-ttu-id="2b36c-393">في مجموعة **النص**، حدد عنصر **السلسلة**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-393">In the **Text** group, select the **String** item.</span></span>
4.  <span data-ttu-id="2b36c-394">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-394">Select **OK**.</span></span>

#### <a name="bind-format-elements-to-a-data-source"></a><span data-ttu-id="2b36c-395">ربط عناصر التنسيق بمصدر بيانات</span><span class="sxs-lookup"><span data-stu-id="2b36c-395">Bind format elements to a data source</span></span>

1.  <span data-ttu-id="2b36c-396">في صفحة **مصمم التنسيق**، في علامة التبويب **تعيين**، قم بتوسيع مصدر بيانات النموذج.</span><span class="sxs-lookup"><span data-stu-id="2b36c-396">On the **Format designer** page, on the **Mapping** tab, expand the model data source.</span></span>
2.  <span data-ttu-id="2b36c-397">حدد حقل **وصف الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-397">Select the **Functionality description** field.</span></span>
3.  <span data-ttu-id="2b36c-398">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-398">Select **Bind**.</span></span>

    ![صفحة مصمم تنسيق‬ التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Format.PNG)

4.  <span data-ttu-id="2b36c-400">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-400">Select **Save**.</span></span>
5.  <span data-ttu-id="2b36c-401">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-401">Close the page.</span></span>

## <a name="appendix2"></a> <span data-ttu-id="2b36c-402">الملحق 2</span><span class="sxs-lookup"><span data-stu-id="2b36c-402">Appendix 2</span></span>

### <a name="configure-a-sample-model-mapping-for-general-customization"></a><span data-ttu-id="2b36c-403">تكوين تعيين نموذج عينة للتخصيص العام</span><span class="sxs-lookup"><span data-stu-id="2b36c-403">Configure a sample model mapping for general customization</span></span>

<span data-ttu-id="2b36c-404">قد تحتاج إلى تخصيص تعيين نموذج تم توفيره من قبل موفر التكوين (الشريك)، ثم استخدام الإصدار المخصص كمصدر بيانات لتنسيقات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2b36c-404">You might want to customize a model mapping that a configuration provider (partner) provided to you, and then use the customized version as a data source for your ER formats.</span></span> <span data-ttu-id="2b36c-405">في هذه الحالة، يجب إنشاء تكوين تعيين نموذج تقارير إلكترونية (ER) مخصص لاجراء التغييرات المطلوبة في تعيينات النماذج الموجودة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-405">In this case, you must create a custom ER model mapping configuration to make the required changes in existing model mappings.</span></span> <span data-ttu-id="2b36c-406">تستخدم الإجراءات الموجودة في هذا الملحق تعيين نموذج **التعيين (عام)** كمثال.</span><span class="sxs-lookup"><span data-stu-id="2b36c-406">The procedures in this appendix use the **Mapping (General)** model mapping as an example.</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="2b36c-407">إنشاء تكوين تعيين نموذج التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2b36c-407">Create an ER model mapping configuration</span></span>

1.  <span data-ttu-id="2b36c-408">في صفحة **التكوينات**، في شجرة التكوينات، حدد **التعيين (عام)**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-408">On the **Configurations** page, in the configurations tree, select **Mapping (General)**.</span></span>
2.  <span data-ttu-id="2b36c-409">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-409">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="2b36c-410">في مربع الحوار المنسدل ، في مجموعه الحقل **جديد**، حدد **الاشتقاق من الاسم: التعيين (عام)، شركة Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-410">In the drop-down dialog box, in the **New** field group, select **Derive from Name: Mapping (General), Litware, Inc.**.</span></span>
4.  <span data-ttu-id="2b36c-411">في حقل **الاسم**، أدخل **التعيين المخصص (عام)**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-411">In the **Name** field, enter **Mapping (General) custom**.</span></span>
5.  <span data-ttu-id="2b36c-412">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-412">Select **Create configuration**.</span></span>

<span data-ttu-id="2b36c-413">لاحظ أن إصدار المسودة 1 لتكوين التقارير الإلكترونية هذا جاهز للتحرير.</span><span class="sxs-lookup"><span data-stu-id="2b36c-413">Notice that draft version 1 of this ER configuration is ready for editing.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="2b36c-414">تصميم تعيين نموذج عينة</span><span class="sxs-lookup"><span data-stu-id="2b36c-414">Design a sample model mapping</span></span>

1.  <span data-ttu-id="2b36c-415">في صفحة **التكوينات**، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-415">On the **Configurations** page, select **Designer**.</span></span>

    > <span data-ttu-id="2b36c-416">لاحظ أنه تم نسخ تعيينات النماذج الخاصة بالتكوين الأساسي تلقائيًا إلى هذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="2b36c-416">Notice that the model mappings of the base configuration have been automatically copied to this configuration.</span></span>

2.  <span data-ttu-id="2b36c-417">حدد تعيين **نسخ التعيين (عام)**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-417">Select the **Mapping (General) Copy** mapping.</span></span>
3.  <span data-ttu-id="2b36c-418">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-418">Select **Designer**.</span></span>
4.  <span data-ttu-id="2b36c-419">في قسم **نموذج البيانات**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-419">In the **Data model** section, select **Edit**.</span></span>
5.  <span data-ttu-id="2b36c-420">في حقل **المعادلة**، أدخل **"الوظيفة العامة المخصصة 1"**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-420">In the **Formula** field, enter **"Generic functionality 1 custom"**.</span></span>
6.  <span data-ttu-id="2b36c-421">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-421">Select **Save**.</span></span>
7.  <span data-ttu-id="2b36c-422">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-422">Close the page.</span></span>

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  <span data-ttu-id="2b36c-424">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-424">Select **Save**.</span></span>
9.  <span data-ttu-id="2b36c-425">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-425">Close the page.</span></span>
10. <span data-ttu-id="2b36c-426">حدد تعيين **نسخة التعيين (عام) 2**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-426">Select the **Mapping (General) 2 Copy** mapping.</span></span>
11. <span data-ttu-id="2b36c-427">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-427">Select **Designer**.</span></span>
12. <span data-ttu-id="2b36c-428">في قسم **نموذج البيانات**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-428">In the **Data model** section, select **Edit**.</span></span>
13. <span data-ttu-id="2b36c-429">في حقل **المعادلة**، أدخل **"الوظيفة العامة المخصصة 2"**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-429">In the **Formula** field, enter **"Generic functionality 2 custom"**.</span></span>
14. <span data-ttu-id="2b36c-430">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-430">Select **Save**.</span></span>
15. <span data-ttu-id="2b36c-431">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-431">Close the page.</span></span>

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. <span data-ttu-id="2b36c-433">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-433">Select **Save**.</span></span>
17. <span data-ttu-id="2b36c-434">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-434">Close the page.</span></span>

    ![صفحة تعيينات نماذج التقارير الإلكترونية](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. <span data-ttu-id="2b36c-436">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-436">Close the page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="2b36c-437">إكمال الإصدار المعدل من تكوين تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="2b36c-437">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="2b36c-438">في صفحة **التكوينات**، في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-438">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="2b36c-439">قم بتغيير حالة تكوين تعيين النموذج المصمم من **مسودة** إلى **مكتمل**، بحيث يمكن استخدامه بواسطة تنسيقات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2b36c-439">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="2b36c-440">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-440">Select **Complete**.</span></span>
3.  <span data-ttu-id="2b36c-441">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-441">Select **OK**.</span></span>

<span data-ttu-id="2b36c-442">لاحظ أن التكوين الذي تم إنشاؤه تم حفظه باعتباره الإصدار المكتمل 1.</span><span class="sxs-lookup"><span data-stu-id="2b36c-442">Notice that the configuration that is created is saved as completed version 1.</span></span>

## <a name="appendix3"></a> <span data-ttu-id="2b36c-443">الملحق 3</span><span class="sxs-lookup"><span data-stu-id="2b36c-443">Appendix 3</span></span>

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a><span data-ttu-id="2b36c-444">تكوين تعيين نموذج عينة للتخصيص الخاص بالبلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="2b36c-444">Configure a sample model mapping for country/region-specific customization</span></span>

<span data-ttu-id="2b36c-445">بالنسبة لبعض تنسيقات التقارير الإلكترونية، قد تكون هناك متطلبات خاصة بالبلد/المنطقة لإعداد البيانات.</span><span class="sxs-lookup"><span data-stu-id="2b36c-445">For some ER formats, there might be country/region-specific requirements for data preparation.</span></span> <span data-ttu-id="2b36c-446">في هذه الحالة، يمكنك أداره تكوين تعيين نموذج تقارير إلكترونية وعزل تنفيذ هذه المتطلبات الخاصة بالبلد/المنطقة عن التنفيذ العام.</span><span class="sxs-lookup"><span data-stu-id="2b36c-446">In this case, you can manage a separate ER model mapping configuration and isolate the implementation of these country/region-specific requirements from the general implementation.</span></span> <span data-ttu-id="2b36c-447">تستخدم الإجراءات الموجودة في هذا الملحق تنسيق التقارير الإلكترونية **التنسيق للتعرف على التعيينات** والمتطلبات الخاصة بالفرنسية كمثال.</span><span class="sxs-lookup"><span data-stu-id="2b36c-447">The procedures in this appendix use the **Format to learn mappings** ER format and French-specific requirements as an example.</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="2b36c-448">إنشاء تكوين تعيين نموذج التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2b36c-448">Create an ER model mapping configuration</span></span>

<span data-ttu-id="2b36c-449">أولاً، قم بإنشاء تكوين تعيين نموذج تقارير إلكترونية (ER) جديد لتنفيذ المتطلبات الخاصة بالبلد/المنطقة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-449">First, create a new ER model mapping configuration to implement the country/region-specific requirements.</span></span> <span data-ttu-id="2b36c-450">استخدم تكوين تعيين نموذج تقارير إلكترونية مخصص كأساس.</span><span class="sxs-lookup"><span data-stu-id="2b36c-450">Use your custom ER model mapping configuration as a base.</span></span>

1.  <span data-ttu-id="2b36c-451">في صفحة **التكوينات**، في شجرة التكوينات، حدد **التعيين المخصص (عام)**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-451">On the **Configurations** page, in the configurations tree, select **Mapping (General) custom**.</span></span>
2.  <span data-ttu-id="2b36c-452">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-452">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="2b36c-453">في مربع الحوار المنسدل، في مجموعه الحقل **جديد**، حدد **الاشتقاق من الاسم: التعيين المخصص (عام)، شركة Litware, Inc**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-453">In the drop-down dialog box, in the **New** field group, select **Derive from Name: Mapping (General) custom, Litware, Inc**.</span></span>
4.  <span data-ttu-id="2b36c-454">في حقل **الاسم**، أدخل **التعيين (FR)**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-454">In the **Name** field, enter **Mapping (FR)**.</span></span>
5.  <span data-ttu-id="2b36c-455">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-455">Select **Create configuration**.</span></span>

<span data-ttu-id="2b36c-456">لاحظ أن إصدار المسودة 1 لتكوين التقارير الإلكترونية هذا جاهز للتحرير.</span><span class="sxs-lookup"><span data-stu-id="2b36c-456">Notice that draft version 1 of this ER configuration is ready for editing.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="2b36c-457">تصميم تعيين نموذج عينة</span><span class="sxs-lookup"><span data-stu-id="2b36c-457">Design a sample model mapping</span></span>

1.  <span data-ttu-id="2b36c-458">في صفحة **التكوينات**، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-458">On the **Configurations** page, select **Designer**.</span></span>

    > <span data-ttu-id="2b36c-459">لاحظ أنه تم نسخ تعيينات النماذج الخاصة بالتكوين الأساسي تلقائيًا إلى هذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="2b36c-459">Notice that model mappings of the base configuration have been automatically copied to this configuration.</span></span>

2.  <span data-ttu-id="2b36c-460">حدد تعيين **نسخ نسخة التعيين (عام)**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-460">Select the **Mapping (General) Copy Copy** mapping.</span></span>
3.  <span data-ttu-id="2b36c-461">أعد تسميتها بـ **التعيين (FR)**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-461">Rename it **Mapping (FR)**.</span></span>
4.  <span data-ttu-id="2b36c-462">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-462">Select **Designer**.</span></span>
5.  <span data-ttu-id="2b36c-463">في قسم **نموذج البيانات**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-463">In the **Data model** section, select **Edit**.</span></span>
6.  <span data-ttu-id="2b36c-464">في حقل **المعادلة**، أدخل **"وظيفة FR رقم 1"**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-464">In the **Formula** field, enter **"FR functionality 1"**.</span></span>
7.  <span data-ttu-id="2b36c-465">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-465">Select **Save**.</span></span>
8.  <span data-ttu-id="2b36c-466">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-466">Close the page.</span></span>

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  <span data-ttu-id="2b36c-468">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-468">Select **Save**.</span></span>
10. <span data-ttu-id="2b36c-469">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-469">Close the page.</span></span>
11. <span data-ttu-id="2b36c-470">حدد تعيين **نسخ نسخة التعيين (عام) 2**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-470">Select the **Mapping (General) 2 Copy Copy** mapping.</span></span>
12. <span data-ttu-id="2b36c-471">أعد تسميتها بـ **التعيين (FR) 2**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-471">Rename it **Mapping (FR) 2**.</span></span>
13. <span data-ttu-id="2b36c-472">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-472">Select **Designer**.</span></span>
14. <span data-ttu-id="2b36c-473">في قسم **نموذج البيانات**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-473">In the **Data model** section, select **Edit**.</span></span>
15. <span data-ttu-id="2b36c-474">في حقل **المعادلة**، أدخل **"وظيفة FR رقم 2"**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-474">In the **Formula** field, enter **"FR functionality 2"**.</span></span>
16. <span data-ttu-id="2b36c-475">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-475">Select **Save**.</span></span>
17. <span data-ttu-id="2b36c-476">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-476">Close the page.</span></span>

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. <span data-ttu-id="2b36c-478">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-478">Select **Save**.</span></span>
19. <span data-ttu-id="2b36c-479">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-479">Close the page.</span></span>

    ![صفحة تعيينات نماذج التقارير الإلكترونية](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. <span data-ttu-id="2b36c-481">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-481">Close the page.</span></span>

#### <a name="specify-countryregion-context-restrictions-for-use"></a><span data-ttu-id="2b36c-482">تحديد قيود سياق البلد/المنطقة للاستخدام</span><span class="sxs-lookup"><span data-stu-id="2b36c-482">Specify country/region context restrictions for use</span></span>

1.  <span data-ttu-id="2b36c-483">في صفحة **التكوينات**، في علامة التبويب السريع **أكواد البلد/المنطقة ISO**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-483">On the **Configurations** page, on the **ISO Country/region codes** FastTab, select **New**.</span></span>
2.  <span data-ttu-id="2b36c-484">في حقل **ISO**، حدد **FR**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-484">In the **ISO** field, select **FR**.</span></span>
3.  <span data-ttu-id="2b36c-485">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-485">Select **Save**.</span></span>

<span data-ttu-id="2b36c-486">لاحظ انه يجب عليك تسجيل الدخول إلى شركه معينه في Finance لتشغيل تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2b36c-486">Note that you must sign in to a specific company in Finance to run an ER format.</span></span> <span data-ttu-id="2b36c-487">وبالتالي ، يمكن اعتبار هذه الشركة جهة تحكم في تنفيذ تنسيق التقارير الإلكترونية وتحديد تعيين نموذج التقارير الإلكترونية الصحيح لنموذج البيانات الأساسي للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2b36c-487">Therefore, this company can be considered a party that controls both ER format execution and selection of the correct ER model mapping of the base ER data model.</span></span> <span data-ttu-id="2b36c-488">عن طريق أضافه كود البلد **FR**، فانك تحدد أن تعيين النموذج هذا متوفر للتحديد بواسطة تنسيق التقارير الإلكترونية الخاص بنموذج البيانات الأساسي فقط عند تشغيل هذا التنسيق ضمن عنصر تحكم شركه لها سياق بلد/منطقه فرنسية.</span><span class="sxs-lookup"><span data-stu-id="2b36c-488">By adding the **FR** country code, you specify that this model mapping is available for selection by an ER format of the base data model only when that format is run under the control of a company that has French country/region context.</span></span>

<span data-ttu-id="2b36c-489">يمكنك أضافه العديد من أكواد البلد/المنطقة لإصدار واحد من تكوين تعيين نموذج التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="2b36c-489">You can add multiple country/region codes for a single version of an ER model mapping configuration.</span></span> <span data-ttu-id="2b36c-490">وبهذه الطريقة، يمكن استخدام تعيينات النماذج الموجودة في تكوين تعيين النموذج لتنسيق تقارير إلكترونية يتم تشغيله ضمن التحكم في الشركات التي لها سياق بلد/منطقه مختلف.</span><span class="sxs-lookup"><span data-stu-id="2b36c-490">In this way, model mappings that reside in that model mapping configuration can be used for an ER format that is run under the control of companies that have a different country/region context.</span></span>

<span data-ttu-id="2b36c-491">لاحظ انه تم تحديد قائمه أكواد البلد/المنطقة لكل إصدار من تكوين تعيين نموذج تقارير إلكترونية ويمكن ان تختلف من إصدار إلى إصدار.</span><span class="sxs-lookup"><span data-stu-id="2b36c-491">Note that the list of country/region codes is specified for each version of an ER model mapping configuration and can vary from version to version.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="2b36c-492">إكمال الإصدار المعدل من تكوين تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="2b36c-492">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="2b36c-493">في صفحة **التكوينات**، في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-493">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="2b36c-494">قم بتغيير حالة تكوين تعيين النموذج المصمم من **مسودة** إلى **مكتمل**، بحيث يمكن استخدامه بواسطة تنسيقات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2b36c-494">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="2b36c-495">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-495">Select **Complete**.</span></span>
3.  <span data-ttu-id="2b36c-496">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-496">Select **OK**.</span></span>

<span data-ttu-id="2b36c-497">لاحظ أن التكوين الذي تم إنشاؤه تم حفظه باعتباره الإصدار المكتمل 1.</span><span class="sxs-lookup"><span data-stu-id="2b36c-497">Notice that the configuration that is created is saved as completed version 1.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b36c-498">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2b36c-498">Additional resources</span></span>

[<span data-ttu-id="2b36c-499">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2b36c-499">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="2b36c-500">إدارة تعيين نموذج ER (تقارير إلكترونية) في تكوينات ER (تقارير إلكترونية) منفصلة</span><span class="sxs-lookup"><span data-stu-id="2b36c-500">Manage ER model mapping in separate ER configurations</span></span>](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[<span data-ttu-id="2b36c-501">تطبيق سياق البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="2b36c-501">Apply country/region context</span></span>](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="2b36c-502">الأسئلة المتداولة</span><span class="sxs-lookup"><span data-stu-id="2b36c-502">Frequently asked questions</span></span>

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a><span data-ttu-id="2b36c-503">لقد قمت بتكوين اثنين من تكوينات تعيين نموذج تقارير إلكترونية مشترك في RCS وتم وضع علامة علي أحدهما كتكوين تعيين للنموذج الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="2b36c-503">I configured two shared ER model mapping configurations in RCS and marked one of them as the default model mapping configuration.</span></span> <span data-ttu-id="2b36c-504">لقد قمت بنجاح بتشغيل تنسيق تقارير إلكترونية تم إنشاؤه لنفس التكوين الأساسي لنموذج بيانات التقارير الإلكترونية، لاختبار تعيينات النماذج.</span><span class="sxs-lookup"><span data-stu-id="2b36c-504">I successfully ran an ER format that was created for the same base ER data model configuration, to test model mappings.</span></span> <span data-ttu-id="2b36c-505">ثم قمت بعد ذلك باستيراد حل التقارير الإلكترونية الكامل (نموذج بيانات التقارير الإلكترونية، وتكوينا تعيين نموذج التقارير الإلكترونية، وتكوين تنسيق التقارير الإلكترونية) إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="2b36c-505">I then imported the whole ER solution (ER data model, two ER model mapping configurations, and ER format configuration) into Finance.</span></span> <span data-ttu-id="2b36c-506">لماذا أتلقى رسالة خطا عند محاولة تشغيل نفس تنسيق التقارير الإلكترونية في Finance؟</span><span class="sxs-lookup"><span data-stu-id="2b36c-506">Why do I receive an error message when I try to run the same ER format in Finance?</span></span>
<span data-ttu-id="2b36c-507">إعداد تعيين النموذج الافتراضي خاص بالبيئة.</span><span class="sxs-lookup"><span data-stu-id="2b36c-507">The default model mapping setting is environment-specific.</span></span> <span data-ttu-id="2b36c-508">تم تكوينه في RCS ولكن لم يتم تصديره إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="2b36c-508">It's configured in RCS but isn't exported to Finance.</span></span> <span data-ttu-id="2b36c-509">لتشغيل تنسيق التقارير الإلكترونية بنجاح، يجب عليك وضع علامة على أحد تكوينات تعيين نموذج التقارير الإلكترونية كتكوين تعيين النموذج الافتراضي في Finance أيضا.</span><span class="sxs-lookup"><span data-stu-id="2b36c-509">To successfully run this ER format, you must mark one of ER model mapping configurations as the default model mapping configuration in Finance too.</span></span>

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a><span data-ttu-id="2b36c-510">لقد قمت بتكوين تعيين نموذج واحد كتعيين نموذج مشترك وأكملت إصدار المسودة له.</span><span class="sxs-lookup"><span data-stu-id="2b36c-510">I configured one model mapping as a shared model mapping and completed the draft version of it.</span></span> <span data-ttu-id="2b36c-511">بعد ذلك قمت باضافه تكوين تعيين نموذج جديد لنفس نموذج البيانات وتكوينه كخاص بالفرنسية.</span><span class="sxs-lookup"><span data-stu-id="2b36c-511">I then added a new model mapping configuration for same data model and configured it as French-specific.</span></span> <span data-ttu-id="2b36c-512">لماذا يتم تحديد تعيين النموذج المشترك عند تشغيل تنسيق التقارير الإلكترونية، حتى إذا كان هذا التنسيق للتقارير الإلكترونية يستخدم تعريف الجذر الصحيح وتم اجراء التنفيذ ضمن التحكم في الشركة التي لها سياق بلد/منطقه فرنسية؟</span><span class="sxs-lookup"><span data-stu-id="2b36c-512">Why is the shared model mapping selected when I run an ER format, even though this ER format uses the correct root definition and execution is done under the control of the company that has French country/region context?</span></span>
<span data-ttu-id="2b36c-513">تأكد من أن تكوين تعيين النموذج المشترك لم يتم وضع علامة عليه علي أنه تكوين تعيين النموذج الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="2b36c-513">Make sure that the shared model mapping configuration isn't marked as the default model mapping configuration.</span></span> <span data-ttu-id="2b36c-514">والا سيكون له اولويه أعلى أثناء تحديد التعيين.</span><span class="sxs-lookup"><span data-stu-id="2b36c-514">Otherwise, it will have higher priority during mapping selection.</span></span> <span data-ttu-id="2b36c-515">وتأكد أيضا من مراعاه تكوين تعيين النموذج الخاص بالفرنسية عند تحديد تعيين أثناء تنفيذ تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2b36c-515">Also make sure that the French-specific model mapping configuration is considered when a mapping is selected during ER format execution.</span></span> <span data-ttu-id="2b36c-516">يتوفر تكوين لتعيين نموذج تقارير إلكترونية للتحديد فقط في حاله تحقق أحد الشروط التالية على الأقل:</span><span class="sxs-lookup"><span data-stu-id="2b36c-516">An ER model mapping configuration is available for selection only if at least one of the following conditions is met:</span></span>
- <span data-ttu-id="2b36c-517">إصدار واحد على الأقل من تكوين تعيين نموذج التقارير الإلكترونية بالحالة **مكتمل** أو **مشترك**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-517">At least one version of the ER model mapping configuration has either **Completed** or **Shared** status.</span></span> <span data-ttu-id="2b36c-518">في هذه الحالة، سيتم استخدام الإصدار الذي يحتوي على رقم الإصدار الأعلى لتنفيذ تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2b36c-518">In this case, the version that has the highest version number will be used for ER format execution.</span></span>
- <span data-ttu-id="2b36c-519">تم تشغيل خيار **تشغيل المسودة** لتكوين تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2b36c-519">The **Run draft** option for the ER model mapping configuration is turned on.</span></span> <span data-ttu-id="2b36c-520">في هذه الحالة، سيتم استخدام الإصدار الذي له حالة **المسودة** لتنفيذ تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2b36c-520">In this case, the version that has **Draft** status will be used for ER format execution.</span></span>
> <span data-ttu-id="2b36c-521">يتوفر خيار **تشغيل المسودة** في صفحة **التكوينات** لكل تكوين تعيين نموذج تقارير إلكترونية عند تشغيل معلمة مستخدم التقارير الإلكترونية **تشغيل الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="2b36c-521">The **Run draft** option becomes available on the **Configurations** page for each ER model mapping configuration when the **Run setting** ER user parameter is turned on.</span></span>