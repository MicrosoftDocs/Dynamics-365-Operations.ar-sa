---
title: بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في إيطاليا
description: يوفر هذا الموضوع معلومات تساعدك على بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في إيطاليا في Microsoft Dynamics 365 Finance وفي Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c513141f820c95fe3842478361693701f1e3641b
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039782"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a><span data-ttu-id="5f62f-103">بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في إيطاليا</span><span class="sxs-lookup"><span data-stu-id="5f62f-103">Get started with the Electronic invoicing add-on for Italy</span></span>

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="5f62f-104">قد لا تدعم الوظيفة الإضافية الفوترة الإلكترونية في إيطاليا في الوقت الحالي جميع الوظائف المتوفرة للفواتير الإلكترونية في Microsoft Dynamics 365 Finance وفي Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5f62f-104">The Electronic invoicing add-on for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="5f62f-105">يوفر هذا الموضوع معلومات تساعدك على بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في إيطاليا.</span><span class="sxs-lookup"><span data-stu-id="5f62f-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Italy.</span></span> <span data-ttu-id="5f62f-106">وهو يرشدك عبر خطوات التكوين التي تعتمد على البلد في Regulatory Configuration Services (RCS) وFinance.</span><span class="sxs-lookup"><span data-stu-id="5f62f-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="5f62f-107">كما يرشدك من خلال عملية إرسال الفواتير الإلكترونية التي يتم إنشاؤها بالتنسيق **FatturaPA** الخاص بإيطاليا من خلال الخدمة، ويشرح كيفية مراجعة نتائج المعالجة.</span><span class="sxs-lookup"><span data-stu-id="5f62f-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5f62f-108">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="5f62f-108">Prerequisites</span></span>

<span data-ttu-id="5f62f-109">قبل إكمال الخطوات الواردة في هذا الموضوع، يجب إكمال الخطوات في [بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="5f62f-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="5f62f-110">إعداد RCS</span><span class="sxs-lookup"><span data-stu-id="5f62f-110">RCS setup</span></span>

<span data-ttu-id="5f62f-111">اثناء إعداد RCS، ستقوم بإكمال المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="5f62f-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="5f62f-112">استيراد ميزة الفوترة الإلكترونية لتصدير الفواتير الإلكترونية للعميل بتنسيق **FatturaPA**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="5f62f-113">مراجعة تكوينات التنسيق المطلوبة لإنشاء الاستجابات وإرسالها واستلامها حول الفواتير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="5f62f-114">تكوين الأحداث التي تدعم سيناريوهات إرسال الفواتير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="5f62f-115">نشر ميزة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="5f62f-116">"ميزة الفوترة الإلكترونية" هي الاسم العام للمورد الذي تم تكوينه ونشره لاستهلاك خادم الوظيفة الإضافية الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="5f62f-117">في هذه الحالة، تصدير الفواتير الإلكترونية للعميل هو ميزة الفوترة الإلكترونية التي ستقوم بإعدادها.</span><span class="sxs-lookup"><span data-stu-id="5f62f-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="5f62f-118">استيراد ميزة الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5f62f-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="5f62f-119">سجل دخولك إلى حساب RCS.</span><span class="sxs-lookup"><span data-stu-id="5f62f-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="5f62f-120">في مساحة العمل **ميزات العولمة** ، في قسم **الميزات** ، حدد الإطار المتجانب **الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="5f62f-121">في الصفحة **ميزات الفوترة الإلكترونية** ، حدد **استيراد** لاستيراد ميزة الفوترة الإلكترونية‏‎ من المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="5f62f-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5f62f-122">إذا لم تظهر قائمة الميزات المتوفرة، فحدد **مزامنة**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="5f62f-123">حدد ميزة **تصدير الفواتير الإلكترونية (IT)** ، ثم حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![استيراد ميزة تصدير الفواتير الإلكترونية (IT)](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="5f62f-125">عند استيراد ميزة **تصدير الفواتير الإلكترونية (IT)** من المستودع العمومي، يتم أيضًا استيراد كافة الإعدادات الموضحة في الأقسام التالية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="5f62f-126">إنشاء إصدار جديد من ميزة تصدير الفواتير الإلكترونية (IT)</span><span class="sxs-lookup"><span data-stu-id="5f62f-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="5f62f-127">في صفحة **ميزات الفوترة الإلكترونية** ، على علامة التبويب **الإصدارات** ، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![إضافة إصدار جديد لميزة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="5f62f-129">بعد ذلك، ستقوم بتكوين تنسيقات التقارير الإلكترونية (ER) المقترنة بميزة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="5f62f-130">في علامة التبويب **التكوينات** ، حدد **إضافة** لإدارة إصدارات التكوين.</span><span class="sxs-lookup"><span data-stu-id="5f62f-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![إدارة إصدارات تكوين ميزة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="5f62f-132">في هذه الخطوة، تقوم بإضافة وتكوين تنسيقات التقارير الإلكترونية لملفات مختلفة يتم استخدام لتصدير الفواتير الإلكترونية الإيطالية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="5f62f-133">بالنسبة للفواتير الإلكترونية الإيطالية FatturaPA، استخدم إما التكوينات القياسية التالية أو التكوينات المخصصة الفعلية التي تستخدمها للفوترة الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="5f62f-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="5f62f-134">فاتورة المبيعات (IT)</span><span class="sxs-lookup"><span data-stu-id="5f62f-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="5f62f-135">فاتورة المشروع (IT)</span><span class="sxs-lookup"><span data-stu-id="5f62f-135">Project invoice (IT)</span></span>

    <span data-ttu-id="5f62f-136">عند إنشاء ميزه الفوترة الإلكترونية التي تشتق من ميزة فوترة إلكترونية أخرى، يتم توارث جميع تنسيقات التقارير الإلكترونية من الميزة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="5f62f-137">حدد تكوين ملف تنسيق تقارير إلكترونية محدد.</span><span class="sxs-lookup"><span data-stu-id="5f62f-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="5f62f-138">حدد **تحرير** أو **عرض** لفتح صفحة **مصمم التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![فتح صفحة مصمم التنسيق](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="5f62f-140">استخدم الصفحة **مصمم التنسيق** لتحرير وعرض تكوينات ملف تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![صفحة مصمم التنسيق‬](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="5f62f-142">إدارة عمليات إعداد ميزة الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5f62f-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="5f62f-143">في صفحة **ميزات الفوترة الإلكترونية** ، على علامة تبويب **عمليات الإعداد** ، حدد **إضافة** أو **حذف** أو **تحرير** لإدارة عمليات إعداد ميزة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add** , **Delete** , or **Edit** to manage the e-Invoicing feature setups.</span></span>

![إدارة عمليات إعداد ميزة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="5f62f-145">في هذه الخطوة، تقوم بتكوين الأحداث التي تنطبق على الفواتير الإلكترونية، بما في ذلك إنشاء ملفات إخراج XML بتنسيق **FatturaPA** والتوقيع الرقمي (إذا كان مطلوبًا).</span><span class="sxs-lookup"><span data-stu-id="5f62f-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="5f62f-146">تكوين إعداد ميزة فاتورة المبيعات</span><span class="sxs-lookup"><span data-stu-id="5f62f-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="5f62f-147">في صفحة **ميزات الفوترة الإلكترونية‬** ، على علامة تبويب **عمليات الإعداد** في العمود **إعداد الميزة** ، حدد **فاتورة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="5f62f-148">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-148">Select **Edit**.</span></span>
3. <span data-ttu-id="5f62f-149">في الصفحة **إعداد إصدار الميزة** ، حدد علامة التبويب **الإجراءات** لإدارة قائمة الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="5f62f-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="5f62f-150">تحدد الإجراءات قائمة بالعمليات التي يجب تشغيلها بترتيب تسلسلي لاستكمال التنفيذ الكامل للحدث.</span><span class="sxs-lookup"><span data-stu-id="5f62f-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![علامة تبويب الإجراءات‏‎](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="5f62f-152">معرف الإجراء</span><span class="sxs-lookup"><span data-stu-id="5f62f-152">Action ID</span></span> | <span data-ttu-id="5f62f-153">اسم الإجراء</span><span class="sxs-lookup"><span data-stu-id="5f62f-153">Action name</span></span>        | <span data-ttu-id="5f62f-154">وصف الإجراء</span><span class="sxs-lookup"><span data-stu-id="5f62f-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="5f62f-155">1</span><span class="sxs-lookup"><span data-stu-id="5f62f-155">1</span></span>         | <span data-ttu-id="5f62f-156">تحويل المستند</span><span class="sxs-lookup"><span data-stu-id="5f62f-156">Transform document</span></span> | <span data-ttu-id="5f62f-157">إنشاء ملف XML الخاص بالفاتورة الإلكترونية بتنسيق **FatturaPA**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="5f62f-158">2</span><span class="sxs-lookup"><span data-stu-id="5f62f-158">2</span></span>         | <span data-ttu-id="5f62f-159">توقيع مستند</span><span class="sxs-lookup"><span data-stu-id="5f62f-159">Sign document</span></span>      | <span data-ttu-id="5f62f-160">تطبيق توقيع رقمي على ملف XML.</span><span class="sxs-lookup"><span data-stu-id="5f62f-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="5f62f-161">حدد علامة التبويب **قواعد قابلية التطبيق** لعرض قواعد قابلية التطبيق والمحافظة عليها.</span><span class="sxs-lookup"><span data-stu-id="5f62f-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="5f62f-162">تحدد قواعد قابلية التطبيق السياق الذي سيتم تشغيل الإجراء فيه.</span><span class="sxs-lookup"><span data-stu-id="5f62f-162">Applicability rules define the context where the action will be run.</span></span>

    ![علامة تبويب قواعد قابلية التطبيق](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="5f62f-164">حدد علامة التبويب **المتغيرات** لعرض المتغيرات والمحافظة عليها.</span><span class="sxs-lookup"><span data-stu-id="5f62f-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![علامة تبويب المتغيرات](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="5f62f-166">حدد المتغيرات العامة المطلوبة لتشغيل الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="5f62f-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="5f62f-167">تكوين إعداد ميزة فاتورة المشروع</span><span class="sxs-lookup"><span data-stu-id="5f62f-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="5f62f-168">تعتبر الخطوات والإعدادات المطلوبة لإعداد ميزة **فاتورة المشروع** مماثلة جدًا للخطوات والإعدادات المطلوبة لإعداد ميزة **فاتورة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="5f62f-169">عند العمل على فواتير المشروع، راجع الإجراءات الخاصة بفواتير المبيعات.</span><span class="sxs-lookup"><span data-stu-id="5f62f-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="5f62f-170">تعيين ميزة الفوترة الإلكترونية إلى البيئة</span><span class="sxs-lookup"><span data-stu-id="5f62f-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="5f62f-171">في صفحة **ميزات الفوترة الإلكترونية** ، على علامة التبويب **البيئات** ، حدد **تمكين**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="5f62f-172">في حقل **البيئة** ، حدد البيئة.</span><span class="sxs-lookup"><span data-stu-id="5f62f-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="5f62f-173">في الحقل **ساري من‬‏‫** ، حدد التاريخ الذي يجب أن تصبح فيه البيئة سارية المفعول.</span><span class="sxs-lookup"><span data-stu-id="5f62f-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="5f62f-174">حدد **تمكين**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-174">Select **Enable**.</span></span> 

![تمكين بيئة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="5f62f-176">نشر ميزة الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5f62f-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="5f62f-177">يمكنك نشر ميزة الفوترة الإلكترونية عن طريق تغيير حالة الإصدار إلى **مكتمل** أو **منشور**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="5f62f-178">تغيير حالة الإصدار إلى "مكتمل"</span><span class="sxs-lookup"><span data-stu-id="5f62f-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="5f62f-179">في الصفحة **ميزات الفوترة الإلكترونية** ، على علامة تبويب **الإصدارات** ، حدد إصدار ميزة الفوترة الإلكترونية بالحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="5f62f-180">حدد **حالة التغيير \> مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="5f62f-181">تغيير حالة الإصدار إلى "منشور"</span><span class="sxs-lookup"><span data-stu-id="5f62f-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="5f62f-182">في الصفحة **ميزات الفوترة الإلكترونية** ، على علامة تبويب **الإصدارات** ، حدد إصدار ميزة الفوترة الإلكترونية بالحالة **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="5f62f-183">حدد **تغيير الحالة \> نشر**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-183">Select **Change status \> Publish**.</span></span>

![تغيير حالة ميزة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="5f62f-185">إعداد تكامل الوظيفة الإضافية الفوترة الإلكترونية في Finance</span><span class="sxs-lookup"><span data-stu-id="5f62f-185">Set up the Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="5f62f-186">اثناء إعداد Finance، ستقوم بإكمال المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="5f62f-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="5f62f-187">استيراد نموذج بيانات التقارير الإلكترونية وتعيين نموذج بيانات التقارير الإلكترونية، وتكوينات السياق للفواتير الإلكترونية FatturaPA.</span><span class="sxs-lookup"><span data-stu-id="5f62f-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="5f62f-188">تكوين الشهادة المطلوبة للتوقيع الرقمي على الفواتير الإلكترونية الإيطالية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="5f62f-189">استيراد نموذج بيانات التقارير الإلكترونية وتعيين نموذج بيانات التقارير الإلكترونية والتنسيقات</span><span class="sxs-lookup"><span data-stu-id="5f62f-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="5f62f-190">في مساحة عمل **إعداد التقارير الإلكترونية** ، تأكد من تعيين موفر تكوين **خدمة مستندات الأعمال** إلى **نشط**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="5f62f-191">حدد **المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="5f62f-192">حدد **المورد العمومي \> فتح**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="5f62f-193">استورد **نموذج الفاتورة** و **تعيين نموذج الفاتورة** و **نموذج سياق فاتورة العميل**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-193">Import **Invoice model** , **Invoice model mapping** , and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="5f62f-194">تشغيل ميزة تصدير فواتير العميل الإلكترونية لإيطاليا</span><span class="sxs-lookup"><span data-stu-id="5f62f-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="5f62f-195">انتقل إلى **إدارة المؤسسة \> الإعداد \> معلمات المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="5f62f-196">على علامة التبويب **الميزات** ، حدد خانة الاختيار **ممكّن** في صف مرجع الميزة **IT00036**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![تشغيل ميزة FatturaPA](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="5f62f-198">تكوين المستندات الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5f62f-198">Configure electronic documents</span></span>

1. <span data-ttu-id="5f62f-199">انتقل إلى **إدارة المؤسسة \> الإعداد \> معلمات المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="5f62f-200">من علامة التبويب **المستند الإلكتروني** ، حدد **إضافة** ، ثم أدخل الجداول المطلوبة لإنشاء الفواتير الإلكترونية الإيطالية:</span><span class="sxs-lookup"><span data-stu-id="5f62f-200">On the **Electronic document** tab, select **Add** , and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="5f62f-201">**اسم الجدول:** دفتر يومية فواتير العميل</span><span class="sxs-lookup"><span data-stu-id="5f62f-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="5f62f-202">**اسم الجدول:** فاتورة المشروع</span><span class="sxs-lookup"><span data-stu-id="5f62f-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="5f62f-203">لكل جدول، حدد سياق مستند ذي صلة:</span><span class="sxs-lookup"><span data-stu-id="5f62f-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="5f62f-204">بالنسبة إلى **دفتر يومية فاتورة العميل** ، حدد **سياق فاتورة العميل**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-204">For **Customer invoice journal** , select **Customer invoice context**.</span></span>
    - <span data-ttu-id="5f62f-205">بالنسبة إلى **فاتورة المشروع** ، حدد **سياق فاتورة المشروع**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-205">For **Project invoice** , select **Project invoice context**.</span></span>

![إعداد أنواع الاستجابات](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="5f62f-207">معالجة الفواتير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5f62f-207">Electronic invoice processing</span></span>

<span data-ttu-id="5f62f-208">اثناء المعالجة في Finance، ستقوم بإكمال المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="5f62f-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="5f62f-209">إنشاء الفواتير الإلكترونية الإيطالية من خلال الوظيفة الإضافية الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5f62f-209">Generate Italian e-invoices through the Electronic invoicing add-on</span></span>
2. <span data-ttu-id="5f62f-210">عرض سجلات التنفيذ ومراجعة نتائج المعالجة</span><span class="sxs-lookup"><span data-stu-id="5f62f-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="5f62f-211">إنشاء الفواتير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5f62f-211">Generate electronic invoices</span></span>

<span data-ttu-id="5f62f-212">بعد قيامك بتشغيل ميزة **تكامل الوظيفة الإضافية الفوترة الإلكترونية القابلة للتكوين** وتنشيط ميزة **IT00036** ، سيتعذر استخدام وظيفة Finance القديمة لإنشاء الفواتير الإلكترونية الإيطالية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-212">After you turn on the **Configurable Electronic invoicing add-on integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="5f62f-213">لقد تم استبدال هذه العملية بأخرى جديدة تسمى **إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="5f62f-214">يمكنك إرسال المستندات يدويًا، بالاستناد إلى طلبك لمستندات الفواتير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="5f62f-215">قبل المتابعة، تأكد من إكمال الإعداد المطلوب للفواتير الإلكترونية الإيطالية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="5f62f-216">للحصول على مزيد من المعلومات، راجع [فواتير العملاء الإلكترونية‬](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span><span class="sxs-lookup"><span data-stu-id="5f62f-216">For more information, see [Customer electronic invoices](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span></span> <span data-ttu-id="5f62f-217">يرجى العلم أن بعض خطوات الإعداد التي ورد وصفها في هذا الموضوع قد لا تكون متوفرة بسبب تنشيط الوظيفة الإضافية الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing add-on activation.</span></span>

1. <span data-ttu-id="5f62f-218">انتقل إلى **إدارة المؤسسة \> دوري \> المستندات الإلكترونية \> إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="5f62f-219">بالنسبة لعملية الإرسال الأولى لأي مستند، عيّن الخيار **إعادة إرسال المستندات** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="5f62f-220">إذا كان من الضروري إعادة إرسال مستند من خلال الخدمة، فقم بتعيين هذا الخيار إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="5f62f-221">على علامة التبويب السريعة **السجلات المطلوب تضمينها‬** ، حدد **تصفية** لفتح مربع الحوار **استعلام** حيث يمكنك إنشاء استعلام لتحديد مستندات لإرسالها.</span><span class="sxs-lookup"><span data-stu-id="5f62f-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![مربع الحوار إرسال المستندات الإلكترونية](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="5f62f-223">استعلام تصفية</span><span class="sxs-lookup"><span data-stu-id="5f62f-223">Filter query</span></span>

1. <span data-ttu-id="5f62f-224">في مربع الحوار **استعلام** ، قم بتكوين شروط التصفية لكل من فواتير المبيعات وفواتير المشروع، أو اترك الشروط فارغة لتضمين كافة الفواتير غير المرسلة.</span><span class="sxs-lookup"><span data-stu-id="5f62f-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![إعداد معايير تصفية الإرسال](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="5f62f-226">حدد **موافق** لإغلاق مربع الحوار **استعلام**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="5f62f-227">حدد **موافق** لإرسال المستندات المحددة.</span><span class="sxs-lookup"><span data-stu-id="5f62f-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="5f62f-228">![ملاحظة] أثناء محاولتك الأولى لإرسال مستند من خلال الخدمة، ستتم مطالبتك بتأكيد الاتصال بالوظيفة الإضافية الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5f62f-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="5f62f-229">حدد **انقر هنا للاتصال بخدمة إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="5f62f-230">عرض سجلات الإرسال</span><span class="sxs-lookup"><span data-stu-id="5f62f-230">View submission logs</span></span>

<span data-ttu-id="5f62f-231">يمكنك عرض سجلات الإرسال لكافة المستندات المرسلة.</span><span class="sxs-lookup"><span data-stu-id="5f62f-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="5f62f-232">انتقل إلى **إدارة المؤسسة \> دوري \> المستندات الإلكترونية \> سجل إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="5f62f-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="5f62f-233">في الحقل **نوع المستند** ، حدد **دفتر يومية فواتير العميل** أو **فاتورة المشروع** لتصفية المستندات الإلكترونية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="5f62f-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![تحديد نوع المستند لعرض سجلات الإرسال](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="5f62f-235">تمثل القيمة التي تظهر في العمود **حالة الإرسال** حالة عملية الإرسال.</span><span class="sxs-lookup"><span data-stu-id="5f62f-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="5f62f-236">وتشير إلى ما إذا تم تشغيل العميل كما هي مكوّنة وما إذا كان ثمة حاجة لتنفيذ إجراء إضافي.</span><span class="sxs-lookup"><span data-stu-id="5f62f-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="5f62f-237">في جزء الإجراءات، حدد **الاستعلامات \> تفاصيل الإرسال** لعرض سجلات تنفيذ الإرسال.</span><span class="sxs-lookup"><span data-stu-id="5f62f-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![عرض تفاصيل سجل الإرسال](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="5f62f-239">على علامة التبويب السريعة **إجراءات المعالجة** ، يمكنك عرض سجل التنفيذ للإجراءات التي تم تكوينها في إصدار الميزة الذي تم إعداده في RCS.</span><span class="sxs-lookup"><span data-stu-id="5f62f-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="5f62f-240">يعرض عمود **الحالة** ما إذا كان قد تم تشغيل الإجراء بنجاح ام لا.</span><span class="sxs-lookup"><span data-stu-id="5f62f-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="5f62f-241">على علامة التبويب السريعة **ملفات الإجراءات** ، يمكنك عرض الملفات الوسيطة التي تم إنشاؤها أثناء تنفيذ الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="5f62f-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="5f62f-242">يمكنك تحديد **عرض** لتنزيل ملف الإخراج XML بالتنسيق **FatturaPA** وعرض محتوياته.</span><span class="sxs-lookup"><span data-stu-id="5f62f-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f62f-243">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="5f62f-243">Related topics</span></span>

- [<span data-ttu-id="5f62f-244">نظرة عامة على الوظيفة الإضافية الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5f62f-244">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="5f62f-245">بدء استخدام الوظيفة الإضافية "الفوترة الإلكترونية"</span><span class="sxs-lookup"><span data-stu-id="5f62f-245">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="5f62f-246">إعداد الوظيفة الإضافية الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5f62f-246">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
