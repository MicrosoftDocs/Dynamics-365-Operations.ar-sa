---
title: أتمته الاختبار باستخدام التقارير الإلكترونية
description: يشرح هذا الموضوع كيفية استخدام الميزة الأساسية في إطار عمل التقارير الإلكترونية (ER) لأتمتة اختبار الوظائف.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 6da9447386e8e56e20507d985ebcdbfce934debd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181601"
---
# <a name="automate-testing-with-electronic-reporting"></a><span data-ttu-id="f0c61-103">التشغيل التلقائي للاختبارات باستخدام التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f0c61-103">Automate testing with Electronic reporting</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f0c61-104">يشرح هذا الموضوع كيفية استخدام إطار عمل التقارير الإلكترونية (ER) لأتمتة اختبار بعض الوظائف.</span><span class="sxs-lookup"><span data-stu-id="f0c61-104">This topic explains how you can use the Electronic reporting (ER) framework to automate testing of some functionality.</span></span> <span data-ttu-id="f0c61-105">يوضح المثال الموجود في هذا الموضوع كيفية تنفيذ اختبار معالجة دفع المورد تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="f0c61-105">The example in this topic shows how to automate the testing of vendor payment processing.</span></span>

<span data-ttu-id="f0c61-106">يستخدم التطبيق إطار عمل التقارير الإلكترونية لإنشاء ملفات الدفع والمستندات المقابلة أثناء معالجة دفع المورّد.</span><span class="sxs-lookup"><span data-stu-id="f0c61-106">The application uses the ER framework to generate payment files and corresponding documents during vendor payment processing.</span></span> <span data-ttu-id="f0c61-107">يتألف إطار عمل ER من نموذج بيانات وتعيينات نماذج ومكونات تنسيق تدعم معالجة الدفع لأنواع دفع مختلفة وإنشاء المستندات بتنسيقات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="f0c61-107">The ER framework consists of a data model, model mappings, and format components that support payment processing for different payment types and the generation of documents in different formats.</span></span> <span data-ttu-id="f0c61-108">يمكن تنزيل هذه المكونات من Microsoft Dynamics Lifecycle Services (LCS) واستيرادها إلى المثيل.</span><span class="sxs-lookup"><span data-stu-id="f0c61-108">These components can be downloaded from Microsoft Dynamics Lifecycle Services (LCS) and imported into the instance.</span></span>

<span data-ttu-id="f0c61-109">كما يمكنك تخصيص كل مكون من مكونات Microsoft واستخدامه كأساس للمكون المخصص الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="f0c61-109">You also can customize each Microsoft component and use it as the basis of your own custom component.</span></span> <span data-ttu-id="f0c61-110">من خلال إنشاء إصدار مخصص، يمكنك إجراء تغييرات تدعم متطلبات معينة.</span><span class="sxs-lookup"><span data-stu-id="f0c61-110">By creating a custom version, you can make changes that support specific requirements.</span></span> <span data-ttu-id="f0c61-111">على سبيل المثال، يمكنك ضبط نموذج بيانات ER وتعيين نموذج ER للوصول إلى بيانات التطبيقات الخاصة بالعميل، أو يمكنك تغيير تنسيق ER لتعديل تخطيط المستند الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="f0c61-111">For example, you can adjust the ER data model and ER model mapping to access customer-specific application data, or you can change an ER format to modify the layout of a generated document.</span></span>

<span data-ttu-id="f0c61-112">يمكنك استخدام تنسيقات التقارير الإلكترونية المخصصة لمعالجة ملفات الدفع التي تقوم بإنشاء مدفوعات المورّد وكذلك لمعالجة تقارير المراقبة.</span><span class="sxs-lookup"><span data-stu-id="f0c61-112">You can use customized ER formats to process payment files that generate vendor payments and also to process control reports.</span></span> <span data-ttu-id="f0c61-113">يتم دعم تعيين الإصدار لمكونات التقارير الإلكترونية ER.</span><span class="sxs-lookup"><span data-stu-id="f0c61-113">Versioning is supported in ER components.</span></span> <span data-ttu-id="f0c61-114">بالتالي، يمكن أن توفر Microsoft إصدارات محدثة لحلول ER الخاصة بمعالجة دفع المورد، ويمكنك دمج الإصدار المحدث تلقائيا مع المكون المخصص عن طريق إعادة تعيين الأساس له.</span><span class="sxs-lookup"><span data-stu-id="f0c61-114">Therefore, Microsoft can provide updated versions of ER solutions for vendor payment processing, and you can automatically merge the updated version with your customized component by rebasing it.</span></span> <span data-ttu-id="f0c61-115">ومع ذلك، يجب عليك اختبار الإصدار الذي تمت إعادة تعيين الأساس له للتأكد من أنه يعمل كما هو متوقع.</span><span class="sxs-lookup"><span data-stu-id="f0c61-115">However, you must test the rebased version to make sure that it works as you expect.</span></span>

<span data-ttu-id="f0c61-116">تعتبر نماذج البيانات الخاصة بـ ER وتعيينات نماذج ER شائعه للعديد من تنسيقات ER المستخدمة لمعالجة المدفوعات الخاصة بأنواع مختلفة ولإنشاء مستندات الدفع الخاصة بالبلد/المنطقة.</span><span class="sxs-lookup"><span data-stu-id="f0c61-116">ER data models and ER model mappings are common for many ER formats that are used to process payments of different types and to generate country/region-specific payment documents.</span></span> <span data-ttu-id="f0c61-117">والتالي، من المستحسن أتمتة قبول المستخدم واختبار التكامل لكي يتم تنفيذه تلقائيا في العديد من الشركات ولكن مع الأخذ في الاعتبار سياق البلد/المنطقة لكل شركة مستهدفة واستخدام مجموعات بيانات مختلفة وغير ذلك.</span><span class="sxs-lookup"><span data-stu-id="f0c61-117">Therefore, it's highly desirable to automate user acceptance and integration testing so that it's automatically done in multiple companies but considers the country/region context of each target company, uses different datasets, and so on.</span></span>

<span data-ttu-id="f0c61-118">للحصول على مزيد من المعلومات حول كيفية إنشاء إصدار مخصص لتنسيق يستند إلى التنسيق الذي تلقيته من موفر التكوين، راجع  [ترقية التنسيق باعتماد إصدار أساسي جديد لهذا التنسيق في ER‬](./tasks/er-upgrade-format.md).</span><span class="sxs-lookup"><span data-stu-id="f0c61-118">For more information about how to create a custom version of a format that is based on the format that you received from a configuration provider, see [ER Upgrade your format by adopting a new, base version of that format](./tasks/er-upgrade-format.md).</span></span>

## <a name="key-concepts"></a><span data-ttu-id="f0c61-119">المفاهيم الأساسية</span><span class="sxs-lookup"><span data-stu-id="f0c61-119">Key concepts</span></span>

<span data-ttu-id="f0c61-120">يمكن لمستخدمي power الوظيفيين كتابه قبول المستخدم واختبار التكامل دون الحاجة إلى كتابه التعليمات البرمجية المصدر.</span><span class="sxs-lookup"><span data-stu-id="f0c61-120">Functional power users can author user acceptance and integration testing without having to write source code.</span></span>

- <span data-ttu-id="f0c61-121">استخدم الميزة الأساسية في ER لمقارنة المستندات التي تم إنشاؤها بالنسخ الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="f0c61-121">Use the ER baseline feature to compare generated documents to master copies.</span></span> <span data-ttu-id="f0c61-122">لمزيد من المعلومات، راجع [تتبع نتائج التقارير المنشأة ومقارنتها بالقيم الأساسية](er-trace-reports-compare-baseline.md).</span><span class="sxs-lookup"><span data-stu-id="f0c61-122">For more information, see [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md).</span></span>
- <span data-ttu-id="f0c61-123">استخدم مسجل المهام لتسجيل حالات الاختبار، وتضمين التقييم الأساسي.</span><span class="sxs-lookup"><span data-stu-id="f0c61-123">Use Task recorder to record test cases, and include baseline assessment.</span></span> <span data-ttu-id="f0c61-124">لمزيد من المعلومات، راجع [مسجل المهام](../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="f0c61-124">For more information, see [Task recorder](../user-interface/task-recorder.md).</span></span>
- <span data-ttu-id="f0c61-125">تجميع حالات الاختبار لسيناريوهات الاختبار المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="f0c61-125">Group test cases for required test scenarios.</span></span> <span data-ttu-id="f0c61-126">لمزيد من المعلومات ، راجع [إنشاء مكتبات اختبار قبول المستخدم باستخدام تسجيلات المهام وBPM.](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)</span><span class="sxs-lookup"><span data-stu-id="f0c61-126">For more information, see [Create user acceptance test libraries by using task recordings and BPM](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span></span>

    - <span data-ttu-id="f0c61-127">استخدم أداة تكوين عمليات الأعمال (BPM) في LCS لإنشاء مكتبات لاختبارات قبول المستخدم.</span><span class="sxs-lookup"><span data-stu-id="f0c61-127">Use Business process modeler (BPM) in LCS to make libraries for user acceptance tests.</span></span>
    - <span data-ttu-id="f0c61-128">استخدم مكتبات اختبار BPM لإنشاء خطة اختبار ومجموعات اختبار في Microsoft Azure DevOps Services (Azure DevOps).</span><span class="sxs-lookup"><span data-stu-id="f0c61-128">Use BPM test libraries to create a test plan and test suites in Microsoft Azure DevOps Services (Azure DevOps).</span></span>

<span data-ttu-id="f0c61-129">يمكن لمستخدمي power الوظيفيين تشغيل اختبارات قبول المستخدم والتكامل.</span><span class="sxs-lookup"><span data-stu-id="f0c61-129">Functional power users can run user acceptance and integration tests.</span></span>

- <span data-ttu-id="f0c61-130">استخدم Regression suite automation tool (RSAT) لتشغيل حالات الاختبار لمجموعة الاختبار المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="f0c61-130">Use Regression suite automation tool (RSAT) to run test cases of the desired test suite.</span></span>
- <span data-ttu-id="f0c61-131">قم بالإبلاغ عن نتائج الاختبار إلى Azure DevOps، واستخدم هذه الخدمة للاستقصاء عن تلك النتائج.</span><span class="sxs-lookup"><span data-stu-id="f0c61-131">Report the results of the testing to Azure DevOps, and use this service to investigate those results.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f0c61-132">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="f0c61-132">Prerequisites</span></span>

<span data-ttu-id="f0c61-133">قبل أن تتمكن من استكمال المهام في هذا الموضوع، يجب إتمام المهام اللازمة التالية:</span><span class="sxs-lookup"><span data-stu-id="f0c61-133">Before you can complete the tasks in this topic, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="f0c61-134">نشر مخطط يدعم التنفيذ التلقائي للاختبار.</span><span class="sxs-lookup"><span data-stu-id="f0c61-134">Deploy a topology that supports test automation.</span></span> <span data-ttu-id="f0c61-135">يجب أن يكون لديك حق الوصول إلى مثيل هذا المخطط لدور **مسؤول النظام**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-135">You must have access to the instance of this topology for the **System administrator** role.</span></span> <span data-ttu-id="f0c61-136">يجب أن يحتوي هذا المخطط على بيانات العرض التوضيحي التي سيتم استخدامها في هذا المثال.</span><span class="sxs-lookup"><span data-stu-id="f0c61-136">This topology must contain the demo data that will be used in this example.</span></span> <span data-ttu-id="f0c61-137">لمزيد من المعلومات ، راجع [نشر مخططات تدعم البناء المستمر والتنفيذ التلقائي للاختبار‬ات](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="f0c61-137">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span>
- <span data-ttu-id="f0c61-138">لتشغيل اختبارات قبول المستخدم والتكامل تلقائيا، يجب عليك تثبيت RSAT في المخطط الذي تستخدمه وتكوينه بالطريقة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="f0c61-138">To run user acceptance and integration tests automatically, you must install RSAT in the topology that you're using and configure it in the appropriate manner.</span></span> <span data-ttu-id="f0c61-139">للحصول على معلومات حول كيفية تثبيت وتكوين RSAT للعمل مع تطبيقات Finance and Operations وAzure DevOps، راجع [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span><span class="sxs-lookup"><span data-stu-id="f0c61-139">For information about how to install and configure RSAT and configure it to work with Finance and Operations apps and Azure DevOps, see [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span></span> <span data-ttu-id="f0c61-140">انتبه إلى المتطلبات الأساسية لاستخدام الأداة.</span><span class="sxs-lookup"><span data-stu-id="f0c61-140">Pay attention to the prerequisites for using the tool.</span></span> <span data-ttu-id="f0c61-141">يبين الرسم التوضيحي التالي مثالاً لإعدادات RSAT.</span><span class="sxs-lookup"><span data-stu-id="f0c61-141">The following illustration shows an example of the RSAT settings.</span></span> <span data-ttu-id="f0c61-142">المستطيل الأزرق يحيط بالمعلمات التي تحدد الوصول إلى Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f0c61-142">The blue rectangle encloses the parameters that specify access to Azure DevOps.</span></span> <span data-ttu-id="f0c61-143">المستطيل الأخضر يحيط بالمعلمات التي تحدد الوصول إلى المثيل.</span><span class="sxs-lookup"><span data-stu-id="f0c61-143">The green rectangle encloses the parameters that specify access to the instance.</span></span>

    <span data-ttu-id="f0c61-144">![إعدادات RSAT](media/GER-Configure.png "لقطة شاشة لمربع حوار RSAT")</span><span class="sxs-lookup"><span data-stu-id="f0c61-144">![RSAT settings](media/GER-Configure.png "Screenshot of the RSAT Settings dialog box")</span></span>

- <span data-ttu-id="f0c61-145">لتنظيم حالات الاختبار في مجموعات للمساعدة في ضمان التسلسل الصحيح للتنفيذ، لكي يمكنك تجميع سجلات عمليات تنفيذ الاختبارات لمزيد من التقارير والاستقصاءات، يجب أن يكون لديك حق الوصول إلى Azure DevOps من المخطط المنشور.</span><span class="sxs-lookup"><span data-stu-id="f0c61-145">To organize test cases in suites to help guarantee the correct execution sequence, so that you can collect logs of test executions for further reporting and investigation, you must have access to Azure DevOps from the deployed topology.</span></span>
- <span data-ttu-id="f0c61-146">لإكمال المثال في هذا الموضوع، نوصي بتنزيل [استخدام ER لاختبارات RSAT](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="f0c61-146">To complete the example in this topic, we recommend that you download [ER usage for RSAT tests](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="f0c61-147">يحتوي هذا الملف المضغوط على دلائل المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="f0c61-147">This zip file contains the following task guides:</span></span>

    | <span data-ttu-id="f0c61-148">المحتوى</span><span class="sxs-lookup"><span data-stu-id="f0c61-148">Content</span></span>                                           | <span data-ttu-id="f0c61-149">اسم الملف والموقع</span><span class="sxs-lookup"><span data-stu-id="f0c61-149">File name and location</span></span> |
    |---------------------------------------------------|------------------------|
    | <span data-ttu-id="f0c61-150">نموذج تسجيل المهمة لإعداد البيانات للاختبار</span><span class="sxs-lookup"><span data-stu-id="f0c61-150">Sample task recording to prepare data for testing</span></span> | <span data-ttu-id="f0c61-151">Prepare\\Recording.xml</span><span class="sxs-lookup"><span data-stu-id="f0c61-151">Prepare\\Recording.xml</span></span> |
    | <span data-ttu-id="f0c61-152">نموذج لتسجيل المهمة لمعالجة مدفوعات المورد</span><span class="sxs-lookup"><span data-stu-id="f0c61-152">Sample task recording to process vendor payment</span></span>   | <span data-ttu-id="f0c61-153">Process\\Recording.xml</span><span class="sxs-lookup"><span data-stu-id="f0c61-153">Process\\Recording.xml</span></span> |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a><span data-ttu-id="f0c61-154">إعداد وحدة الحسابات الدائنة لمعالجة مدفوعات المورد</span><span class="sxs-lookup"><span data-stu-id="f0c61-154">Prepare the Accounts payable module to process vendor payments</span></span>

1. <span data-ttu-id="f0c61-155">تسجيل الدخول إلى المثيل الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="f0c61-155">Sign in to your instance.</span></span>
2. <span data-ttu-id="f0c61-156">قم بتنزيل تكوينات ER التالية من LCS.</span><span class="sxs-lookup"><span data-stu-id="f0c61-156">Download the following ER configurations from LCS.</span></span> <span data-ttu-id="f0c61-157">لمعرفة التعليمات، راجع [استيراد أحد التكوينات من Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md)</span><span class="sxs-lookup"><span data-stu-id="f0c61-157">For instructions, see [ER Import a configuration from Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).</span></span>

    - <span data-ttu-id="f0c61-158">**نموذج الدفع** تكوين نموذج ER</span><span class="sxs-lookup"><span data-stu-id="f0c61-158">**Payment model** ER model configuration</span></span>
    - <span data-ttu-id="f0c61-159">**تعيين نموذج الدفع 1611** تكوين تعيين نموذج ER</span><span class="sxs-lookup"><span data-stu-id="f0c61-159">**Payment model mapping 1611** ER model mapping configuration</span></span>
    - <span data-ttu-id="f0c61-160">**BACS (UK)** تكوين تنسيق ER</span><span class="sxs-lookup"><span data-stu-id="f0c61-160">**BACS (UK)** ER format configuration</span></span>

    <span data-ttu-id="f0c61-161">![تكوينات التقارير الإلكترونية](media/GER-Configurations.png "لقطة شاشة لصفحة التكوينات في التقارير الإلكترونية")</span><span class="sxs-lookup"><span data-stu-id="f0c61-161">![Electronic reporting configurations](media/GER-Configurations.png "Screenshot of the Configurations page in Electronic reporting")</span></span>

3. <span data-ttu-id="f0c61-162">حدد شركة البيانات التجريبية **GBSI**، والذي يوجد سياق البلد/المنطقة لها في بريطانيا العظمى.</span><span class="sxs-lookup"><span data-stu-id="f0c61-162">Select the **GBSI** demo data company, which has a country/region context in Great Britain.</span></span>
4. <span data-ttu-id="f0c61-163">تكوين معلمات الحسابات الدائنة:</span><span class="sxs-lookup"><span data-stu-id="f0c61-163">Configure Accounts payable parameters:</span></span>

    1. <span data-ttu-id="f0c61-164">انتقل إلى **الحسابات الدائنة \> إعداد الدفع \> طرق الدفع**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-164">Go to **Accounts payable \> Payment setup \> Methods of payment**.</span></span>
    2. <span data-ttu-id="f0c61-165">حدد طريقة الدفع **الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-165">Select the **Electronic** method of payment.</span></span>
    3. <span data-ttu-id="f0c61-166">تكوين طريقه الدفع المحددة بحيث تستخدم تنسيق **BACS (UK)** الخاص بـ ER الذي قمت بتنزيله سابقا لمعالجة دفع المورد:</span><span class="sxs-lookup"><span data-stu-id="f0c61-166">Configure the selected method of payment so that it uses the **BACS (UK)** ER format that you downloaded earlier for vendor payment processing:</span></span>

        1. <span data-ttu-id="f0c61-167">في علامة التبويب السريعة **تنسيقات الملف**، قم بتعيين خيار **تنسيق التصدير الإلكتروني العام‬** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-167">On the **File formats** FastTab, set the **Generic electronic Export format** option to **Yes**.</span></span>
        2. <span data-ttu-id="f0c61-168">في حقل **تكوين تنسيق التصدير**، حدد **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-168">In the **Export format configuration** field, select **BACS (UK)**.</span></span>

    <span data-ttu-id="f0c61-169">![صفحة طرق الدفع](media/GER-APParameters.png "لقطة شاشة لصفحة طرق الدفع")</span><span class="sxs-lookup"><span data-stu-id="f0c61-169">![Methods of payment page](media/GER-APParameters.png "Screenshot of the Methods of payment page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="f0c61-170">إذا كان لديك الإصدار المشتق لتنسيق ER هذا والذي تم إنشاؤه لدعم التخصيصات، فيمكنك تحديد هذا التكوين في طريقه الدفع **الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-170">If you have the derived version of this ER format that was created to support customizations, you can select this configuration in the **Electronic** method of payment.</span></span>

5. <span data-ttu-id="f0c61-171">إنشاء مثل للدفع للمورد:</span><span class="sxs-lookup"><span data-stu-id="f0c61-171">Create an example vendor payment:</span></span>

    1. <span data-ttu-id="f0c61-172">انتقل إلى **الحسابات الدائنة \> المدفوعات \> دفتر يومية المدفوعات**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-172">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
    2. <span data-ttu-id="f0c61-173">تأكد من أنك لم تقم بترحيل دفتر يومية المدفوعات.</span><span class="sxs-lookup"><span data-stu-id="f0c61-173">Make sure that you haven't posted the payment journal.</span></span>

        <span data-ttu-id="f0c61-174">![صفحة دفتر يومية المدفوعات](media/GER-APJournal.png "لقطة شاشة لصفحة دفتر يومية المدفوعات")</span><span class="sxs-lookup"><span data-stu-id="f0c61-174">![Payment journal page](media/GER-APJournal.png "Screenshot of the Payment journal page")</span></span>

    3. <span data-ttu-id="f0c61-175">حدد **البنود**، ثم أدخل البند الذي يحتوي على المعلومات التالية.</span><span class="sxs-lookup"><span data-stu-id="f0c61-175">Select **Lines**, and enter a line that has the following information.</span></span>

        | <span data-ttu-id="f0c61-176">الحقل</span><span class="sxs-lookup"><span data-stu-id="f0c61-176">Field</span></span>               | <span data-ttu-id="f0c61-177">قيمه المثال</span><span class="sxs-lookup"><span data-stu-id="f0c61-177">Example value</span></span>   |
        |---------------------|-----------------|
        | <span data-ttu-id="f0c61-178">اسم المورّد</span><span class="sxs-lookup"><span data-stu-id="f0c61-178">Vendor name</span></span>         | <span data-ttu-id="f0c61-179">GB\_SI\_000001</span><span class="sxs-lookup"><span data-stu-id="f0c61-179">GB\_SI\_000001</span></span>  |
        | <span data-ttu-id="f0c61-180">مدين</span><span class="sxs-lookup"><span data-stu-id="f0c61-180">Debit</span></span>               | <span data-ttu-id="f0c61-181">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f0c61-181">1,000.00</span></span>        |
        | <span data-ttu-id="f0c61-182">العملة</span><span class="sxs-lookup"><span data-stu-id="f0c61-182">Currency</span></span>            | <span data-ttu-id="f0c61-183">GBP</span><span class="sxs-lookup"><span data-stu-id="f0c61-183">GBP</span></span>             |
        | <span data-ttu-id="f0c61-184">نوع حساب مقابل</span><span class="sxs-lookup"><span data-stu-id="f0c61-184">Offset account type</span></span> | <span data-ttu-id="f0c61-185">البنك</span><span class="sxs-lookup"><span data-stu-id="f0c61-185">Bank</span></span>            |
        | <span data-ttu-id="f0c61-186">الحساب المقابل</span><span class="sxs-lookup"><span data-stu-id="f0c61-186">Offset account</span></span>      | <span data-ttu-id="f0c61-187">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="f0c61-187">GBSI OPER</span></span>       |
        | <span data-ttu-id="f0c61-188">الطريقة الخاصة بالدفع</span><span class="sxs-lookup"><span data-stu-id="f0c61-188">Method of payment</span></span>   | <span data-ttu-id="f0c61-189">إلكتروني</span><span class="sxs-lookup"><span data-stu-id="f0c61-189">Electronic</span></span>      |

    <span data-ttu-id="f0c61-190">![صفحة مدفوعات الموردين](media/GER-APJournalLines.png "لقطة شاشة لصفحة مدفوعات الموردين")</span><span class="sxs-lookup"><span data-stu-id="f0c61-190">![Vendor payments page](media/GER-APJournalLines.png "Screenshot of the Vendor payments page")</span></span>

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a><span data-ttu-id="f0c61-191">تحضير إطار عمل ER لاختيار معالجة مدفوعات المورد</span><span class="sxs-lookup"><span data-stu-id="f0c61-191">Prepare the ER framework to test vendor payment processing</span></span>

### <a name="configure-er-parameters"></a><span data-ttu-id="f0c61-192">تكوين معلمات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="f0c61-192">Configure ER parameters</span></span>

1. <span data-ttu-id="f0c61-193">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> معلمات إعداد التقارير الإلكترونية‬‬**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-193">Go to **Organization administration \> Electronic reporting \> Electronic reporting parameters**.</span></span>
2. <span data-ttu-id="f0c61-194">من علامة تبويب **المرفقات** في حقل **الأساس** ، حدد **ملف** كنوع المستند الذي يستخدمه إطار عمل إدارة المستندات (DM) للاحتفاظ بالمستندات المرتبطة بالميزة الأساسية لمرفقات DM.</span><span class="sxs-lookup"><span data-stu-id="f0c61-194">On the **Attachments** tab, in the **Baseline** field, select **File** as the document type that the Document management (DM) framework uses to keep documents that are related to the baseline feature as DM attachments.</span></span>

    <span data-ttu-id="f0c61-195">![صفحة معلمات التقارير الإلكترونية](media/GER-ERParameters.png "لقطة شاشة لصفحة معلمات التقارير الإلكترونية")</span><span class="sxs-lookup"><span data-stu-id="f0c61-195">![Electronic reporting parameters page](media/GER-ERParameters.png "Screenshot of the Electronic reporting parameters page")</span></span>

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a><span data-ttu-id="f0c61-196">إنشاء نُسخ أساسية للمستندات المتعلقة بمدفوعات المورد</span><span class="sxs-lookup"><span data-stu-id="f0c61-196">Generate baseline copies of vendor payment–related documents</span></span>

1. <span data-ttu-id="f0c61-197">انتقل إلى **الحسابات الدائنة \> المدفوعات \> دفتر يومية المدفوعات**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-197">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="f0c61-198">حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-198">Select **Lines**.</span></span>
3. <span data-ttu-id="f0c61-199">حدد **إنشاء المدفوعات**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-199">Select **Generate payments**.</span></span>
4. <span data-ttu-id="f0c61-200">حدد طريقة الدفع **الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-200">Select the **Electronic** method of payment.</span></span>
5. <span data-ttu-id="f0c61-201">حدد حساب البنك **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-201">Select the **GBSI OPER** bank account.</span></span>
6. <span data-ttu-id="f0c61-202">قم بتعيين خيار **طباعة تقرير التحكم** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-202">Set the **Print control report** option to **Yes**.</span></span>
7. <span data-ttu-id="f0c61-203">قم بتنزيل المخرجات التي تم إنشاؤه كملف مضغوط من نوع zip.</span><span class="sxs-lookup"><span data-stu-id="f0c61-203">Download the generated output as a zip file.</span></span>
8. <span data-ttu-id="f0c61-204">فتح الملف الذي تم تنزيله.</span><span class="sxs-lookup"><span data-stu-id="f0c61-204">Open the downloaded file.</span></span>
9. <span data-ttu-id="f0c61-205">استخرج الملفات التالية من الملف الذي تم تنزيله:</span><span class="sxs-lookup"><span data-stu-id="f0c61-205">Extract following files from the downloaded file:</span></span>

    - <span data-ttu-id="f0c61-206">**ملف** ملف الدفع بتنسيق نص</span><span class="sxs-lookup"><span data-stu-id="f0c61-206">**File** payment file in text format</span></span>
    - <span data-ttu-id="f0c61-207">**ERVendOutPaymControlReport** ملف تقرير التحكم بتنسيق XLSX</span><span class="sxs-lookup"><span data-stu-id="f0c61-207">**ERVendOutPaymControlReport** control report file in XLSX format</span></span>

    <span data-ttu-id="f0c61-208">![الملفات المستخرجة](media/GER-APJournalProcessed.png "لقطة شاشة لأسماء الملفات المستخرجة في Windows explorer")</span><span class="sxs-lookup"><span data-stu-id="f0c61-208">![Extracted files](media/GER-APJournalProcessed.png "Screenshot of extracted file names in Windows explorer")</span></span>

### <a name="turn-on-the-er-baseline-feature"></a><span data-ttu-id="f0c61-209">تشغيل الميزة الأساسية في ER</span><span class="sxs-lookup"><span data-stu-id="f0c61-209">Turn on the ER baseline feature</span></span>

1. <span data-ttu-id="f0c61-210">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-210">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f0c61-211">في جزء الإجراء، على علامة تبويب **الإعداد**، حدد **معلمات المستخدم‬**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-211">On the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
3. <span data-ttu-id="f0c61-212">قم بتعيين خيار **تشغيل في وضع التصحيح** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-212">Set the **Run in debug mode** option to **Yes**.</span></span>

<span data-ttu-id="f0c61-213">من خلال تشغيل معلمة **التشغيل في وضع التصحيح**، فإنك تجبر إطار عمل ER على تنفيذ الإجراءات التالية بعد تنفيذ أي من تنسيق ER الذي ينشئ المستندات الصادرة:</span><span class="sxs-lookup"><span data-stu-id="f0c61-213">By turning on the **Run in debug mode** parameter, you force the ER framework to perform the following actions after the execution of any ER format that generates outgoing documents:</span></span>

1. <span data-ttu-id="f0c61-214">حدد ما إذا كان قد تم تكوين أساس لأي من مكونات تنسيق ER الذي تم تنفيذه.</span><span class="sxs-lookup"><span data-stu-id="f0c61-214">Determine whether a baseline was configured for any of components of the executed ER format.</span></span>
2. <span data-ttu-id="f0c61-215">حدد ما إذا كان كل أساس تم تكوينه قابلا للتطبيق في الشروط الحالية (كود الشركة للشركة المسجلة واسم الملف وملحق اسم الملف للإخراج الذي تم إنشاؤه وهكذا).</span><span class="sxs-lookup"><span data-stu-id="f0c61-215">Determine whether each configured baseline is applicable in the current conditions (company code of the signed-in company, file name and file name extension of the generated output, and so on).</span></span>
3. <span data-ttu-id="f0c61-216">بالنسبة لكل أساس قابل للتطبيق، قم بتنفيذ الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="f0c61-216">For each applicable baseline, perform the following actions:</span></span>

    1. <span data-ttu-id="f0c61-217">قارن الإخراج الذي تم إنشاؤه أثناء تنفيذ تنسيق ER بالأساس المطابق.</span><span class="sxs-lookup"><span data-stu-id="f0c61-217">Compare the output that is generated during execution of the ER format with the corresponding baseline.</span></span>
    2. <span data-ttu-id="f0c61-218">خزّن نتائج المقارنة في سجل تصحيح تكوينات ER.</span><span class="sxs-lookup"><span data-stu-id="f0c61-218">Store the results of the comparison in the ER configurations debug log.</span></span>

### <a name="configure-er-baselines-for-vendor-payment-processing"></a><span data-ttu-id="f0c61-219">تكوين أسس ER لمعالجة مدفوعات المورد</span><span class="sxs-lookup"><span data-stu-id="f0c61-219">Configure ER baselines for vendor payment processing</span></span>

1. <span data-ttu-id="f0c61-220">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-220">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f0c61-221">حدد **الأسس**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-221">Select **Baselines**.</span></span>
3. <span data-ttu-id="f0c61-222">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-222">Select **New**.</span></span>
4. <span data-ttu-id="f0c61-223">في حقل **المرجع**، حدد تنسيق **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-223">In the **Reference** field, select the **BACS (UK)** format.</span></span>
5. <span data-ttu-id="f0c61-224">حدد **المرفقات**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-224">Select **Attachments**.</span></span>
6. <span data-ttu-id="f0c61-225">أضف الأساس الجديد لملف دفع المورد:</span><span class="sxs-lookup"><span data-stu-id="f0c61-225">Add a new baseline for the vendor payment file:</span></span>

    1. <span data-ttu-id="f0c61-226">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-226">Select **New**.</span></span>
    2. <span data-ttu-id="f0c61-227">في الحقل **النوع**، حدد نوع مستند DM **ملف** الذي قمت بتكوينه في معلمات ER لتخزين منتجات الأساس.</span><span class="sxs-lookup"><span data-stu-id="f0c61-227">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="f0c61-228">استعرض لتحديد ملف دفع **ملف** المحفوظ محليا بتنسيق نص.</span><span class="sxs-lookup"><span data-stu-id="f0c61-228">Browse to select the locally saved **File** payment file in text format.</span></span>
    4. <span data-ttu-id="f0c61-229">في حقل **الوصف**، أدخل **ملف TXT للدفع**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-229">In the **Description** field, enter **Payment TXT file**.</span></span>

7. <span data-ttu-id="f0c61-230">أضف أساسًا جديدًا لتقرير التحكم الخاص بدفع المورد:</span><span class="sxs-lookup"><span data-stu-id="f0c61-230">Add a new baseline for the control report for the vendor payment:</span></span>

    1. <span data-ttu-id="f0c61-231">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-231">Select **New**.</span></span>
    2. <span data-ttu-id="f0c61-232">في الحقل **النوع**، حدد نوع مستند DM **ملف** الذي قمت بتكوينه في معلمات ER لتخزين منتجات الأساس.</span><span class="sxs-lookup"><span data-stu-id="f0c61-232">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="f0c61-233">استعرض لتحديد ملف تقرير التحكم **ERVendOutPaymControlReport** المحفوظ محليًا بتنسيق XLSX.</span><span class="sxs-lookup"><span data-stu-id="f0c61-233">Browse to select the locally saved **ERVendOutPaymControlReport** control report file in XLSX format.</span></span>
    4. <span data-ttu-id="f0c61-234">في حقل **الوصف**، أدخل **تقرير تحكم XLSX للدفع**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-234">In the **Description** field, enter **Payment XLSX control report**.</span></span>

    <span data-ttu-id="f0c61-235">![الأسس لملف دفع المورد وتقرير التحكم](media/GER-BaselineAttachments.png "لقطة شاشة لصفحة التكوينات مع تحديد تقرير التحكم XLSX")</span><span class="sxs-lookup"><span data-stu-id="f0c61-235">![Baselines for the vendor payment file and control report](media/GER-BaselineAttachments.png "Screenshot of the Configurations page with the Payment XLSX control report selected")</span></span>

8. <span data-ttu-id="f0c61-236">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f0c61-236">Close the page.</span></span>
9. <span data-ttu-id="f0c61-237">في علامة التبويب السريعة **الأسس**، حدد **جديد** لتكوين أساس لملف الدفع:</span><span class="sxs-lookup"><span data-stu-id="f0c61-237">On the **Baselines** FastTab, select **New** to configure a baseline for the payment file:</span></span>

    1. <span data-ttu-id="f0c61-238">قم بتسمية البند **إعداد الأساس لملف الدفع**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-238">Name the line **Baseline setting for payment file**.</span></span>
    2. <span data-ttu-id="f0c61-239">في حقل **اسم مكون الملف**، حدد  **ملف** لتطبيق هذا الأساس على إخراج تنسيق ER الذي يقوم بإنشاء ملف الدفع بتنسيق نص BACS (UK).</span><span class="sxs-lookup"><span data-stu-id="f0c61-239">In the **File component name** field, select **file** to apply this baseline to the ER format output that generates the payment file in BACS (UK) text format.</span></span>
    3. <span data-ttu-id="f0c61-240">في حقل **الشركات**، حدد **GBSI** لتطبيق هذا الأساس عند تشغيل تنسيق ER بالقيمة **BACS (UK)** في شركة GBSI.</span><span class="sxs-lookup"><span data-stu-id="f0c61-240">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="f0c61-241">في حقل **قناع اسم الملف**، أدخل **\*.TXT** لتطبيق هذا الأساس فقط على مخرجات مكون تنسيق **ملف** الذي يحتوي على ملحق اسم ملف **.txt**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-241">In **File name mask** field, enter **\*.TXT** to apply this baseline only to outputs of the **file** format component that have the **.txt** file name extension.</span></span>
    5. <span data-ttu-id="f0c61-242">في حقل **الأساس**، حدد **ملف TXT للدفع** لكي يتم استخدام هذا الأساس للمقارنة مع الإخراج الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="f0c61-242">In the **Baseline** field, select **Payment TXT file** so that this baseline is used for comparison with the generated output.</span></span>

10. <span data-ttu-id="f0c61-243">حدد **جديد** لتكوين أساس لتقرير التحكم:</span><span class="sxs-lookup"><span data-stu-id="f0c61-243">Select **New** to configure a baseline for the control report:</span></span>

    1. <span data-ttu-id="f0c61-244">قم بتسمية البند **إعداد الأساس لتقرير التحكم**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-244">Name the line **Baseline setting for control report**.</span></span>
    2. <span data-ttu-id="f0c61-245">في حقل **اسم مكون الملف**، حدد  **ERVendOutPaymControlReport** لتطبيق هذا الأساس على إخراج تنسيق ER الذي يقوم بإنشاء تقرير التحكم.</span><span class="sxs-lookup"><span data-stu-id="f0c61-245">In the **File component name** field, select **ERVendOutPaymControlReport** to apply this baseline to the ER format output that generates the control report.</span></span>
    3. <span data-ttu-id="f0c61-246">في حقل **الشركات**، حدد **GBSI** لتطبيق هذا الأساس عند تشغيل تنسيق ER بالقيمة **BACS (UK)** في شركة GBSI.</span><span class="sxs-lookup"><span data-stu-id="f0c61-246">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="f0c61-247">في حقل **قناع اسم الملف**، أدخل **\*.TXT** لتطبيق هذا الأساس فقط على مخرجات مكون تنسيق **ERVendOutPaymControlReport** الذي يحتوي على ملحق اسم ملف **.xslx**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-247">In **File name mask** field, enter **\*.XLSX** to apply this baseline only to outputs of the **ERVendOutPaymControlReport** format component that have the **.xslx** file name extension.</span></span>
    5. <span data-ttu-id="f0c61-248">في حقل **الأساس**، حدد **تقرير تحكم XLSX للدفع** لكي يتم استخدام هذا الأساس للمقارنة مع الإخراج الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="f0c61-248">In the **Baseline** field, select **Payment XLSX control report** so that this baseline is used for comparison with the generated output.</span></span>

    <span data-ttu-id="f0c61-249">![علامة التبويب السريع للأسس في صفحة التكوينات](media/GER-BaselineRules.png "علامة التبويب السريع للأسس في صفحة التكوينات")</span><span class="sxs-lookup"><span data-stu-id="f0c61-249">![Baselines FastTab on the Configurations page](media/GER-BaselineRules.png "Screenshot of the Baselines FastTab on the Configurations page")</span></span>

## <a name="record-tests-to-validate-vendor-payment-processing"></a><span data-ttu-id="f0c61-250">تسجيل الاختبارات للتحقق من صحة معالجة دفع المورد</span><span class="sxs-lookup"><span data-stu-id="f0c61-250">Record tests to validate vendor payment processing</span></span>

<span data-ttu-id="f0c61-251">وبصفتك مستخدم محترف وظيفي، يمكنك تسجيل الخطوات الخاصة بك لاختبار معالجة الدفع الخاصة بالمورد.</span><span class="sxs-lookup"><span data-stu-id="f0c61-251">As a functional power user, you can record your own steps to test vendor payment processing.</span></span> <span data-ttu-id="f0c61-252">نوصي أن تقوم بتشغيل تسجيل المهمة **Prepare\\Recording.xml** (وتحريره حسب الحاجة) والذي قمت بتنزيله سابقًا.</span><span class="sxs-lookup"><span data-stu-id="f0c61-252">We recommend that you play (and edit, as required) the **Prepare\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="f0c61-253">يتم استخدام هذا التسجيل لتعيين كافة بيانات الاختبار إلى الحالة الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="f0c61-253">This recording is used to set all testing data to the correct state.</span></span> <span data-ttu-id="f0c61-254">هذه الخطوة مطلوبة لأنه يمكن إجراء الاختبار عدة مرات و يجب أن يستخدم كل اختبار البيانات بنفس الحالة.</span><span class="sxs-lookup"><span data-stu-id="f0c61-254">That step is required because the testing can be done many times, and every test must use data that is in the same state.</span></span>

### <a name="reset-user-settings"></a><span data-ttu-id="f0c61-255">إعادة تعيين إعدادات المستخدم</span><span class="sxs-lookup"><span data-stu-id="f0c61-255">Reset user settings</span></span>

1. <span data-ttu-id="f0c61-256">افتح لوحة المعلومات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="f0c61-256">Open the default dashboard.</span></span>
2. <span data-ttu-id="f0c61-257">حدد زر **الإعدادات** (رمز الترس).</span><span class="sxs-lookup"><span data-stu-id="f0c61-257">Select the **Settings** button (the gear symbol).</span></span>
3. <span data-ttu-id="f0c61-258">حدد **خيارات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-258">Select **User options**.</span></span>
4. <span data-ttu-id="f0c61-259">حدد **بيانات الاستخدام**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-259">Select **Usage data**.</span></span>
5. <span data-ttu-id="f0c61-260">حدد **إعادة التعيين**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-260">Select **Reset**.</span></span>
6. <span data-ttu-id="f0c61-261">حدد **نعم** لتأكيد رغبتك في إعادة تعيين بيانات الاستخدام.</span><span class="sxs-lookup"><span data-stu-id="f0c61-261">Select **Yes** to confirm that you want to reset usage data.</span></span>
7. <span data-ttu-id="f0c61-262">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f0c61-262">Close the page.</span></span>

### <a name="record-the-steps-to-prepare-data-for-testing"></a><span data-ttu-id="f0c61-263">تسجيل الخطوات لإعداد البيانات للاختبار</span><span class="sxs-lookup"><span data-stu-id="f0c61-263">Record the steps to prepare data for testing</span></span>

1. <span data-ttu-id="f0c61-264">حدد زر **الإعدادات** (رمز الترس).</span><span class="sxs-lookup"><span data-stu-id="f0c61-264">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="f0c61-265">حدد **مسجل المهام**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-265">Select **Task recorder**.</span></span>
3. <span data-ttu-id="f0c61-266">حدد **تسجيل التشغيل**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-266">Select **Playback recording**.</span></span>
4. <span data-ttu-id="f0c61-267">حدد **فتح من هذا الكمبيوتر الشخصي**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-267">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="f0c61-268">حدد **استعراض**، وحدد ملف **Prepare\\Recording.xml** الذي حفظته محليًا.</span><span class="sxs-lookup"><span data-stu-id="f0c61-268">Select **Browse**, and select the locally save **Prepare\\Recording.xml** file.</span></span>
6. <span data-ttu-id="f0c61-269">حدد **بدء**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-269">Select **Start**.</span></span>
7. <span data-ttu-id="f0c61-270">استمر في تحديد **تشغيل الخطوة التالية المعلقة‬** حتى يتم تشغيل كافة الخطوات الموجودة في التسجيل.</span><span class="sxs-lookup"><span data-stu-id="f0c61-270">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="f0c61-271">ينفذ تسجيل المهمة هذا الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="f0c61-271">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="f0c61-272">قم بتعيين حالة بند الدفع الذي تمت معالجته إلى **بلا**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-272">Set the status of the processed payment line to **None**.</span></span>

    <span data-ttu-id="f0c61-273">![تسجيل المهام الخطوات 3 حتى 4](media/GER-Recording1Review1.png "لقطة شاشة لتسجيل المهام الخطوات 3 حتى 4")</span><span class="sxs-lookup"><span data-stu-id="f0c61-273">![Task recording steps 3 through 4](media/GER-Recording1Review1.png "Screenshot of task recording steps 3 through 4")</span></span>

2. <span data-ttu-id="f0c61-274">شغل معلمة مستخدم ER **تشغيل في وضع التصحيح**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-274">Turn on the **Run in debug mode** ER user parameter.</span></span>

    <span data-ttu-id="f0c61-275">![تسجيل المهام الخطوات 9 حتى 10](media/GER-Recording1Review2.png "لقطة شاشة لتسجيل المهام الخطوات 9 حتى 10")</span><span class="sxs-lookup"><span data-stu-id="f0c61-275">![Task recording steps 9 through 10](media/GER-Recording1Review2.png "Screenshot of task recording steps 9 through 10")</span></span>

3. <span data-ttu-id="f0c61-276">نظّف سجل تصحيح ER والذي يحتوي على نتائج مقارنة الملفات التي تم إنشاؤها بالأسس.</span><span class="sxs-lookup"><span data-stu-id="f0c61-276">Clean up the ER debug log that contains the results of the comparison of generated files to baselines.</span></span>

    <span data-ttu-id="f0c61-277">![تسجيل المهام الخطوات 13 حتى 15](media/GER-Recording1Review3.png "لقطة شاشة لتسجيل المهام الخطوات 13 حتى 15")</span><span class="sxs-lookup"><span data-stu-id="f0c61-277">![Task recording steps 13 through 15](media/GER-Recording1Review3.png "Screenshot of task recording steps 13 through 15")</span></span>

### <a name="record-the-steps-to-test-vendor-payment-processing"></a><span data-ttu-id="f0c61-278">تسجيل الخطوات لاختبار معالجة دفع المورد</span><span class="sxs-lookup"><span data-stu-id="f0c61-278">Record the steps to test vendor payment processing</span></span>

<span data-ttu-id="f0c61-279">نوصي أن تقوم بتشغيل تسجيل المهمة **Process\\Recording.xml**(وتحريره حسب الحاجة) والذي قمت بتنزيله سابقًا.</span><span class="sxs-lookup"><span data-stu-id="f0c61-279">We recommend that you play (and edit, as required) the **Process\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="f0c61-280">يتم استخدام هذا التسجيل لمعالجة مدفوعات المورد والتحقق من صحة نتائج مقارنة المستندات التي تم إنشاؤها بالأسس.</span><span class="sxs-lookup"><span data-stu-id="f0c61-280">This recording is used to process vendor payments and validate the results of the comparison of generated documents to corresponding baselines.</span></span>

1. <span data-ttu-id="f0c61-281">حدد زر **الإعدادات** (رمز الترس).</span><span class="sxs-lookup"><span data-stu-id="f0c61-281">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="f0c61-282">حدد **مسجل المهام**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-282">Select **Task recorder**.</span></span>
3. <span data-ttu-id="f0c61-283">حدد **تسجيل التشغيل**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-283">Select **Playback recording**.</span></span>
4. <span data-ttu-id="f0c61-284">حدد **فتح من هذا الكمبيوتر الشخصي**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-284">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="f0c61-285">حدد **استعراض**، وحدد ملف **Process\\Recording.xml** الذي حفظته محليًا.</span><span class="sxs-lookup"><span data-stu-id="f0c61-285">Select **Browse**, and select the locally saved **Process\\Recording.xml** file.</span></span>
6. <span data-ttu-id="f0c61-286">حدد **بدء**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-286">Select **Start**.</span></span>
7. <span data-ttu-id="f0c61-287">استمر في تحديد **تشغيل الخطوة التالية المعلقة‬** حتى يتم تشغيل كافة الخطوات الموجودة في التسجيل.</span><span class="sxs-lookup"><span data-stu-id="f0c61-287">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="f0c61-288">ينفذ تسجيل المهمة هذا الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="f0c61-288">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="f0c61-289">ابدأ معالجة دفع المورّد.</span><span class="sxs-lookup"><span data-stu-id="f0c61-289">Start vendor payment processing.</span></span>
2. <span data-ttu-id="f0c61-290">حدد معلمات وقت التشغيل الصحيحة، ثم قم بتشغيل إنشاء تقرير التحكم.</span><span class="sxs-lookup"><span data-stu-id="f0c61-290">Select the correct runtime parameters, and turn on generation of a control report.</span></span>

    <span data-ttu-id="f0c61-291">![تسجيل المهام الخطوات 3 حتى 8](media/GER-Recording2Review1.png "لقطة شاشة لتسجيل المهام الخطوات 3 حتى 8")</span><span class="sxs-lookup"><span data-stu-id="f0c61-291">![Task recording steps 3 through 8](media/GER-Recording2Review1.png "Screenshot of task recording steps 3 through 8")</span></span>

3. <span data-ttu-id="f0c61-292">قم بالوصول إلى سجل تصحيح ER لتسجيل نتائج مقارنة المخرجات التي تم إنشاؤها بالأسس المقابلة.</span><span class="sxs-lookup"><span data-stu-id="f0c61-292">Access the ER debug log to record the results of the comparison of generated outputs to corresponding baselines.</span></span>

    <span data-ttu-id="f0c61-293">في سجل تصحيح ER، تظهر نتائج المقارنة في حقل **النص الذي تم إنشاؤه**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-293">In the ER debug log, the results of the comparison appear in the **Generated text** field.</span></span> <span data-ttu-id="f0c61-294">يشير حقل **مكون التنسيق** و **مسار التنسيق الذي تسبب في إدخال سجل** إلى مكون الملف الذي تمت مقارنة الإخراج الناشئ به مع الأساس.</span><span class="sxs-lookup"><span data-stu-id="f0c61-294">The **Format component** and **Format path that caused a log entry** fields refer to the file component for which the generated output has been compared to the baseline.</span></span>

    <span data-ttu-id="f0c61-295">![الإدخالات في صفحة سجلات تشغيل التقارير الإلكترونية](media/GER-ERDebugLog.png "لقطة لشاشة للإدخالات في صفحة سجلات تشغيل التقارير الإلكترونية")</span><span class="sxs-lookup"><span data-stu-id="f0c61-295">![Entries on the Electronic reporting run logs page](media/GER-ERDebugLog.png "Screenshot of entries on the Electronic reporting run logs page")</span></span>

4. <span data-ttu-id="f0c61-296">يتم تسجيل مقارنة الإخراج الحالي بالأساس بواسطة استخدام خيار مسجل المهام **التحقق من الصحة** واختيار  **القيمة الحالية**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-296">The comparison of the current output to the baseline is recorded by using the **Validate** Task recorder option and selecting  **Current Value**.</span></span>

    <span data-ttu-id="f0c61-297">![استخدام خيار التحقق من الصحة للمقارنة بالقيمة الحالية](media/GER-TRRecordValidation.png "لقطة شاشة لاستخدام خيار التحقق من الصحة للمقارنة بالقيمة الحالية")</span><span class="sxs-lookup"><span data-stu-id="f0c61-297">![Using the Validate option for comparison with the current value](media/GER-TRRecordValidation.png "Screenshot of using the Validate option for comparison with the current value")</span></span>

    <span data-ttu-id="f0c61-298">يبين الرسم التوضيحي التالي كيف تبدو خطوات التحقق من الصحة المسجلة في تسجيل المهام.</span><span class="sxs-lookup"><span data-stu-id="f0c61-298">The following illustration shows what the recorded validation steps look like in the task recording.</span></span>

    <span data-ttu-id="f0c61-299">![خطوات تسجيل المهم 13و 15](media/GER-Recording2Review2.png "لقطة شاشة لخطوات تسجيل المهم 13و 15")</span><span class="sxs-lookup"><span data-stu-id="f0c61-299">![Task recording steps 13 and 15](media/GER-Recording2Review2.png "Screenshot of task recording steps 13 and 15")</span></span>

## <a name="add-the-recorded-tests-to-azure-devops"></a><span data-ttu-id="f0c61-300">إضافة اختبارات مسجلة إلى Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="f0c61-300">Add the recorded tests to Azure DevOps</span></span>

1. <span data-ttu-id="f0c61-301">افتح بيئة Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f0c61-301">Open the Azure DevOps environment.</span></span>
2. <span data-ttu-id="f0c61-302">حدد المشروع الذي قمت بتحديده في معلمات RSAT عندما قمت [بتكوين الأداة](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="f0c61-302">Select the project that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
3. <span data-ttu-id="f0c61-303">حدد خطة الاختبار التي قمت بتحديدها في معلمات RSAT عندما قمت [بتكوين الأداة](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="f0c61-303">Select the test plan that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
4. <span data-ttu-id="f0c61-304">قم بإنشاء حالة اختبار جديدة لخطة الاختبار المحددة:</span><span class="sxs-lookup"><span data-stu-id="f0c61-304">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="f0c61-305">قم بتسميه حالة الاختبار **إعداد البيانات لاختبار معالجة الدفع الإلكتروني للمورد**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-305">Name the test case **Prepare data to test processing of vendor's electronic payment**.</span></span>
    2. <span data-ttu-id="f0c61-306">أرفق ملف **Recording.xml** من مجلد **Prepare** الذي قمت بتنزيله في السابق.</span><span class="sxs-lookup"><span data-stu-id="f0c61-306">Attach the **Recording.xml** file from the **Prepare** folder that you downloaded earlier.</span></span>

5. <span data-ttu-id="f0c61-307">قم بإنشاء حالة اختبار جديدة لخطة الاختبار المحددة:</span><span class="sxs-lookup"><span data-stu-id="f0c61-307">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="f0c61-308">قم بتسمية حالة الاختبار **اختبار المعالجة لمدفوعات المورد باستخدام تنسيق ER بقيمة BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-308">Name the test case **Test processing of vendor payments by using ER format BACS (UK)**.</span></span>
    2. <span data-ttu-id="f0c61-309">أرفق ملف **Recording.xml** من مجلد **العملية** الذي قمت بتنزيله في السابق.</span><span class="sxs-lookup"><span data-stu-id="f0c61-309">Attach the **Recording.xml** file from the **Process** folder that you downloaded earlier.</span></span>

    <span data-ttu-id="f0c61-310">![حالات اختبار جديدة لخطة الاختبار المحددة](media/GER-RSAT-DevOps-Tests-Passed.png "لقطة شاشة لحالات اختبار جديدة لخطة الاختبار المحددة")</span><span class="sxs-lookup"><span data-stu-id="f0c61-310">![New test cases for the selected test plan](media/GER-RSAT-DevOps-Tests-Passed.png "Screenshot of the new test cases for the selected test plan")</span></span>

> [!NOTE]
> <span data-ttu-id="f0c61-311">انتبه لطلب التنفيذ الصحيح للاختبارات التي تمت إضافتها.</span><span class="sxs-lookup"><span data-stu-id="f0c61-311">Pay attention to the correct execution order of the tests that are added.</span></span>

## <a name="prepare-rsat-to-run-the-recorded-tests"></a><span data-ttu-id="f0c61-312">تحضير RSAT لتشغيل الاختبارات المسجلة</span><span class="sxs-lookup"><span data-stu-id="f0c61-312">Prepare RSAT to run the recorded tests</span></span>

### <a name="load-the-tests-from-azure-devops-to-rsat"></a><span data-ttu-id="f0c61-313">تحميل الاختبارات من Azure DevOps إلى RSAT</span><span class="sxs-lookup"><span data-stu-id="f0c61-313">Load the tests from Azure DevOps to RSAT</span></span>

1. <span data-ttu-id="f0c61-314">افتح تطبيق RSAT المحلي في المخطط الحالي.</span><span class="sxs-lookup"><span data-stu-id="f0c61-314">Open the local RSAT application in the current topology.</span></span>
2. <span data-ttu-id="f0c61-315">حدد **تحميل** لتحميل الاختبارات الموجودة حاليا في Azure DevOps إلى RSAT.</span><span class="sxs-lookup"><span data-stu-id="f0c61-315">Select **Load** to load the tests that currently reside in Azure DevOps into RSAT.</span></span>

    <span data-ttu-id="f0c61-316">![الاختبارات المحملة إلى RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "لقطة شاشة للاختبارات المحملة إلى RSAT")</span><span class="sxs-lookup"><span data-stu-id="f0c61-316">![Tests loaded into RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Screenshot of the tests loaded into RSAT")</span></span>

### <a name="create-automation-and-parameters-files"></a><span data-ttu-id="f0c61-317">إنشاء ملفات الأتمتة والمعلمات</span><span class="sxs-lookup"><span data-stu-id="f0c61-317">Create automation and parameters files</span></span>

1. <span data-ttu-id="f0c61-318">في RSAT، حدد الاختبارات التي قمت بتحميلها من Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f0c61-318">In RSAT, select the tests that you loaded from Azure DevOps.</span></span>
2. <span data-ttu-id="f0c61-319">حدد **جديد** لإنشاء ملفات الأتمتة والمعلمات لـ RSAT.</span><span class="sxs-lookup"><span data-stu-id="f0c61-319">Select **New** to create RSAT automation and parameters files.</span></span>

    <span data-ttu-id="f0c61-320">![ملفات الأتمتة والمعلمات لـ RSAT التي تم إنشائها في RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "لقطة شاشة لملفات الأتمتة والمعلمات لـ RSAT التي تم إنشائها في RSAT")</span><span class="sxs-lookup"><span data-stu-id="f0c61-320">![RSAT automation and parameters files created in RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Screenshot of the RSAT automation and parameters files created in RSAT")</span></span>

### <a name="modify-the-parameters-files"></a><span data-ttu-id="f0c61-321">تعديل ملفات المعلمات</span><span class="sxs-lookup"><span data-stu-id="f0c61-321">Modify the parameters files</span></span>

1. <span data-ttu-id="f0c61-322">في RSAT، حدد حالة الاختبار **إعداد البيانات لاختبار معالجة الدفع الإلكتروني للمورد**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-322">In RSAT, select the **Prepare data to test processing of vendor's electronic payment** test case.</span></span>
2. <span data-ttu-id="f0c61-323">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-323">Select **Edit**.</span></span>
3. <span data-ttu-id="f0c61-324">في ورقة عمل Microsoft Excel التي تم فتحها، في ورقة عامل **عام**، قم بتغيير كود الشركة إلى **GBSI**، نظرًا لأنه سوف يتم استخدام هذه الشركة لتنفيذ الاختبار.</span><span class="sxs-lookup"><span data-stu-id="f0c61-324">In the Microsoft Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**, because this company will be used for test execution.</span></span>
4. <span data-ttu-id="f0c61-325">في RSAT، حدد حالة الاختبار **اختبار المعالجة لمدفوعات المورد باستخدام تنسيق ER بقيمة BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-325">In RSAT, select the **Test processing of vendor payments by using ER format BACS (UK)** test case.</span></span>
5. <span data-ttu-id="f0c61-326">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-326">Select **Edit**.</span></span>
6. <span data-ttu-id="f0c61-327">في مصنف Excel المفتوح، في ورقه العمل **عام**، قم بتغيير كود الشركة إلى **GBSI**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-327">In the Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**.</span></span>
7. <span data-ttu-id="f0c61-328">في ورقة عمل **ERFormatMappingRunLogTable**، لاحظ أن الخلايا A:3 و C:3 تحتوي على نص الحقول في جدول سجل تصحيحات ER المستخدم للتحقق من نتائج مقارنة الإخراج بالأساس.</span><span class="sxs-lookup"><span data-stu-id="f0c61-328">On the **ERFormatMappingRunLogTable** worksheet, notice that cells A:3 and C:3 contain the text of the fields in the ER debug log table that are used to validate the results of the comparison of the output to the baseline.</span></span> <span data-ttu-id="f0c61-329">سيتم استخدام هذه النصوص لتقييم سجلات تصحيح ER التي تم إنشاؤها أثناء تنفيذ الاختبار.</span><span class="sxs-lookup"><span data-stu-id="f0c61-329">These texts will be used to evaluate ER debug log records that are created during test execution.</span></span>

    <span data-ttu-id="f0c61-330">![ورقة عمل ERFormatMappingRunLogTable](media/GER-RSAT-RSAT-ExcelParameters.png "لقطة شاشة لورقة عمل ERFormatMappingRunLogTable")</span><span class="sxs-lookup"><span data-stu-id="f0c61-330">![ERFormatMappingRunLogTable worksheet](media/GER-RSAT-RSAT-ExcelParameters.png "Screenshot of the ERFormatMappingRunLogTable worksheet")</span></span>

## <a name="run-the-tests-and-analyze-the-results"></a><span data-ttu-id="f0c61-331">تشغيل الاختبارات وتحليل النتائج</span><span class="sxs-lookup"><span data-stu-id="f0c61-331">Run the tests and analyze the results</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="f0c61-332">تشغيل الاختبارات في RSAT</span><span class="sxs-lookup"><span data-stu-id="f0c61-332">Run the tests in RSAT</span></span>

1. <span data-ttu-id="f0c61-333">في RSAT، حدد الاختبارات المحملة.</span><span class="sxs-lookup"><span data-stu-id="f0c61-333">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="f0c61-334">حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-334">Select **Run**.</span></span>

<span data-ttu-id="f0c61-335">لاحظ أنه يتم تشغيل حالات الاختبار تلقائيا في التطبيق باستخدام مستعرض ويب.</span><span class="sxs-lookup"><span data-stu-id="f0c61-335">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="f0c61-336">حلل نتائج تنفيذ الاختبار</span><span class="sxs-lookup"><span data-stu-id="f0c61-336">Analyze the results of test execution</span></span>

<span data-ttu-id="f0c61-337">يتم تخزين نتائج تنفيذ الاختبار في RSAT.</span><span class="sxs-lookup"><span data-stu-id="f0c61-337">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="f0c61-338">لاحظ أنه تم اجتياز كلا الاختبارين.</span><span class="sxs-lookup"><span data-stu-id="f0c61-338">Notice that both tests were passed.</span></span>

<span data-ttu-id="f0c61-339">![اختبارات تم اجتيازها في RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "لقطة شاشة لاختبارات تم اجتيازها RSAT")</span><span class="sxs-lookup"><span data-stu-id="f0c61-339">![Tests that passed in RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Screenshot of tests that passed in RSAT")</span></span>

<span data-ttu-id="f0c61-340">لاحظ أنه يتم أيضًا إرسال نتائج تنفيذ الاختبار إلى Azure DevOpsحتى يمكنك إجراء مزيد من التحليل.</span><span class="sxs-lookup"><span data-stu-id="f0c61-340">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="f0c61-341">![نتائج تنفيذ الاختبار في Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "لقطه شاشة لنتائج تنفيذ الاختبار في Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="f0c61-341">![Results of test execution in Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Screenshot of the results of test execution in Azure DevOps")</span></span>

### <a name="simulate-a-situation-where-tests-fail"></a><span data-ttu-id="f0c61-342">محاكاة موقف فشل الاختبارات</span><span class="sxs-lookup"><span data-stu-id="f0c61-342">Simulate a situation where tests fail</span></span>

<span data-ttu-id="f0c61-343">يجب أن تفشل مجموعة الاختبارات هذه في حالة عدم تطابق واحد على الأقل من المخرجات التي تم إنشاؤها مع الأساس المقابل.</span><span class="sxs-lookup"><span data-stu-id="f0c61-343">This test suite must fail when at least one of the generated outputs doesn't match the corresponding baseline.</span></span> <span data-ttu-id="f0c61-344">لتحقيق هذا الموقف، يمكنك استخدام الإصدار المشتق من التنسيق **BACS (UK)** الذي سيقوم بإنشاء ملف دفع له محتوى مختلف عن الأساس المقابل.</span><span class="sxs-lookup"><span data-stu-id="f0c61-344">To achieve this situation, you can use your derived version of the **BACS (UK)** format that will generate a payment file that has different content than the corresponding baseline.</span></span> <span data-ttu-id="f0c61-345">لمحاكاة هذا الموقف، يمكنك استخدام نفس تنسيق **BACS (UK)** ولكن يمكنك تغيير مبلغ الدفع في بند الدفع الذي تمت معالجته.</span><span class="sxs-lookup"><span data-stu-id="f0c61-345">To simulate this situation, you can use the same **BACS (UK)** format but change the payment amount on the processed payment line.</span></span>

1. <span data-ttu-id="f0c61-346">افتح التطبيق، وانتقل إلى **الحسابات الدائنة \> المدفوعات \> دفتر يومية المدفوعات**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-346">Open the application and go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="f0c61-347">حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-347">Select **Lines**.</span></span>
3. <span data-ttu-id="f0c61-348">حدد بند الدفع، ثم قم بتحديد **حالة الدفع \> بلا**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-348">Select the payment line, and then select **Payment status \> None**.</span></span>
4. <span data-ttu-id="f0c61-349">في الحقل **المدين**، قم بتغيير القيمة من **1,000.00** إلى **2,000.00**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-349">In the **Debit** field, change the value from **1,000.00** to **2,000.00**.</span></span>
5. <span data-ttu-id="f0c61-350">حدد **حفظ** لحفظ تغييراتك.</span><span class="sxs-lookup"><span data-stu-id="f0c61-350">Select **Save** to save your changes.</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="f0c61-351">تشغيل الاختبارات في RSAT</span><span class="sxs-lookup"><span data-stu-id="f0c61-351">Run the tests in RSAT</span></span>

1. <span data-ttu-id="f0c61-352">في RSAT، حدد الاختبارات المحملة.</span><span class="sxs-lookup"><span data-stu-id="f0c61-352">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="f0c61-353">حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="f0c61-353">Select **Run**.</span></span>

<span data-ttu-id="f0c61-354">لاحظ أنه يتم تشغيل حالات الاختبار تلقائيا في التطبيق باستخدام مستعرض ويب.</span><span class="sxs-lookup"><span data-stu-id="f0c61-354">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="f0c61-355">حلل نتائج تنفيذ الاختبار</span><span class="sxs-lookup"><span data-stu-id="f0c61-355">Analyze the results of test execution</span></span>

<span data-ttu-id="f0c61-356">يتم تخزين نتائج تنفيذ الاختبار في RSAT.</span><span class="sxs-lookup"><span data-stu-id="f0c61-356">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="f0c61-357">لاحظ فشل الاختبار الثاني أثناء عملية التنفيذ الثانية.</span><span class="sxs-lookup"><span data-stu-id="f0c61-357">Notice that the second test failed during the second execution.</span></span>

<span data-ttu-id="f0c61-358">![نتائج الاختبار الفاشل في RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "لقطة شاشة لنتائج الاختبار الفاشل في RSAT")</span><span class="sxs-lookup"><span data-stu-id="f0c61-358">![Failed test results in RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Screenshot of the failed test results in RSAT")</span></span>

<span data-ttu-id="f0c61-359">لاحظ أنه يتم أيضًا إرسال نتائج تنفيذ الاختبار إلى Azure DevOpsحتى يمكنك إجراء مزيد من التحليل.</span><span class="sxs-lookup"><span data-stu-id="f0c61-359">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="f0c61-360">![نتائج الاختبار الفاشل في Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "لقطة شاشة لنتائج الاختبار الفاشل في Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="f0c61-360">![Failed test results in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Screenshot of the failed test results in Azure DevOps")</span></span>

<span data-ttu-id="f0c61-361">يمكنك الوصول إلى حالة كل اختبار.</span><span class="sxs-lookup"><span data-stu-id="f0c61-361">You can access the status of each test.</span></span> <span data-ttu-id="f0c61-362">يمكنك أيضا الوصول إلى سجل التنفيذ لكي تقوم بتحليل أسباب أي فشل.</span><span class="sxs-lookup"><span data-stu-id="f0c61-362">You can also access the execution log so that you analyze the reasons for any failure.</span></span> <span data-ttu-id="f0c61-363">في التوضيح التالي، يوضح سجل التنفيذ أن الفشل حدث بسبب الاختلاف في المحتوى بين ملف الدفع الذي تم إنشاؤه وأساسه.</span><span class="sxs-lookup"><span data-stu-id="f0c61-363">In the following illustration, the execution log shows that the failure occurred because of the difference in content between the generated payment file and its baseline.</span></span>

<span data-ttu-id="f0c61-364">![سجل التنفيذ لتحليل الفشل في Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "لقطة شاشة لسجل التنفيذ لتحليل الفشل في Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="f0c61-364">![Execution log for analyzing failure in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Screenshot of the execution log for analyzing failure in Azure DevOps")</span></span>

<span data-ttu-id="f0c61-365">بالتالي، كما رأيت، يمكن تقييم عمل أي تنسيق ER تلقائيًا باستخدام RSAT كمنصة اختبار وباستخدام حالات الاختبار المستندة إلى مسجل المهام التي تستخدم ميزة أساس ER.</span><span class="sxs-lookup"><span data-stu-id="f0c61-365">Therefore, as you've seen, the functioning of any ER format can be evaluated automatically by using RSAT as the testing platform and by using Task recorder-based test cases that use the ER baseline feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0c61-366">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f0c61-366">Additional resources</span></span>

- [<span data-ttu-id="f0c61-367">مسجل المهام</span><span class="sxs-lookup"><span data-stu-id="f0c61-367">Task recorder</span></span>](../user-interface/task-recorder.md)
- [<span data-ttu-id="f0c61-368">Regression suite automation tool</span><span class="sxs-lookup"><span data-stu-id="f0c61-368">Regression suite automation tool</span></span>](https://www.microsoft.com/download/details.aspx?id=57357)
- [<span data-ttu-id="f0c61-369">إنشاء مكتبات اختبارات قبول المستخدم باستخدام تسجيلات المهام وBPM</span><span class="sxs-lookup"><span data-stu-id="f0c61-369">Create user acceptance test libraries by using task recordings and BPM</span></span>](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [<span data-ttu-id="f0c61-370">نشر مخططات تدعم البناء المستمر والتنفيذ التلقائي للاختبار‬ات</span><span class="sxs-lookup"><span data-stu-id="f0c61-370">Deploy topologies that support continuous build and test automation</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="f0c61-371">تتبع نتائج التقارير المنشأة ومقارنتها بقيم أساس ER</span><span class="sxs-lookup"><span data-stu-id="f0c61-371">Trace generated report results and compare them with ER baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="f0c61-372">ترقية تنسيق ER باعتماد إصدار أساسي جديد لهذا التنسيق</span><span class="sxs-lookup"><span data-stu-id="f0c61-372">Upgrade your ER format by adopting a new, base version of that format</span></span>](tasks/er-upgrade-format.md)
- [<span data-ttu-id="f0c61-373">استيراد تكوين ER من Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="f0c61-373">Import ER configuration from Lifecycle Services</span></span>](tasks/er-import-configuration-lifecycle-services.md)
