---
title: إنشاء نماذج FTI قابلة للطباعة
description: يشرح هذا الموضوع كيفية استخدام إطار عمل التقارير الإلكترونية لإنشاء نماذج قابلة للطباعة لفاتورة النص الحر (FTI) كمستندات Microsoft Office.
author: NickSelin
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 9e64899e0bbdb5a9d8899e865de9ee32aae59382
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751646"
---
# <a name="generate-printable-fti-forms"></a><span data-ttu-id="5ca18-103">إنشاء نماذج فاتورة نص حر (FTI) قابلة للطباعة</span><span class="sxs-lookup"><span data-stu-id="5ca18-103">Generate printable FTI forms</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5ca18-104">يسمح لك إطار عمل التقارير الإلكترونية بإنشاء نماذج قابلة للطباعة لفاتورة النص الحر (FTI) كمستندات Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="5ca18-104">The Electronic reporting (ER) framework lets you generate printable free text invoice (FTI) forms as Microsoft Office documents.</span></span> <span data-ttu-id="5ca18-105">يوفر هذا الموضوع معلومات حول كيفية إنشاء تكوينات خاصة بك بالإضافة إلى تفاصيل حول قوالب التكوينات المتاحة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-105">This topic provides information about how to build your own configurations as well as details of available configuration templates.</span></span>

## <a name="overview"></a><span data-ttu-id="5ca18-106">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="5ca18-106">Overview</span></span>

<span data-ttu-id="5ca18-107">بالإضافة إلى القدرة الموجودة على إنشاء نماذج FTI قابلة للطباعة باستخدام Microsoft SQL Server Reporting Services (SSRS)، يمكنك الآن استخدام إطار عمل التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5ca18-107">In addition to the existing capability of generating printable FTI forms by using Microsoft SQL Server Reporting Services (SSRS), you can now use the ER framework.</span></span> <span data-ttu-id="5ca18-108">يمكنك إدارة نماذج FTI القابلة للطباعة في Microsoft Office Excel وWord.</span><span class="sxs-lookup"><span data-stu-id="5ca18-108">You can manage printable FTI forms in Microsoft Office Excel and Word.</span></span> <span data-ttu-id="5ca18-109">ويمكنك أيضًا تعديل التخطيط وتدفق البيانات والتنسيق لتلبية متطلبات محددة دون إدخال تغييرات على التعليمات البرمجية.</span><span class="sxs-lookup"><span data-stu-id="5ca18-109">You can also modify the layout, data flow, and formatting to meet specific requirements without making code changes.</span></span>

> [!NOTE]
> <span data-ttu-id="5ca18-110">إذا أردت البدء مع نظرة عامة على تكوينات التقارير الإلكترونية الموجودة لهذه العينة من حل نماذج FTI القابلة للطباعة، يمكنك الانتقال مباشرة إلى القسم **تنزيل عينة تكوينات التقارير الإلكترونية لإنشاء نماذج FTI قابلة للطباعة** لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="5ca18-110">If you want to start with an overview of existing ER configurations for this sample of the printable FTI forms solution, you can go directly to section **Download sample ER configurations to generate printable FTI forms** later in this topic.</span></span>

## <a name="create-customized-configurations-for-fti-printable-forms"></a><span data-ttu-id="5ca18-111">إنشاء تكوينات مخصصة لنماذج FTI القابلة للطباعة</span><span class="sxs-lookup"><span data-stu-id="5ca18-111">Create customized configurations for FTI printable forms</span></span>
<span data-ttu-id="5ca18-112">كجزء من الحل المخصص لنماذج FTI القابلة للطباعة، يجب إنشاء مجموعة من تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5ca18-112">As part of your customized solution for printable FTI forms, you must create a set of ER configurations.</span></span>

### <a name="configure-the-er-data-model"></a><span data-ttu-id="5ca18-113">تكوين نموذج بيانات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5ca18-113">Configure the ER data model</span></span>
<span data-ttu-id="5ca18-114">يجب أن يتضمن تطبيقك تكوين نموذج بيانات التقارير الإلكترونية الذي يحتوي على نموذج بيانات يصف مجال عمل فوترة العميل.</span><span class="sxs-lookup"><span data-stu-id="5ca18-114">Your application must include the ER data model configuration that contains a data model that describes the customer invoicing business domain.</span></span> <span data-ttu-id="5ca18-115">يجب أن يكون اسم نموذج البيانات **CustomersInvoicing**، وهذا عبارة عن شرط.</span><span class="sxs-lookup"><span data-stu-id="5ca18-115">As a requirement, the name of the data model must be **CustomersInvoicing**.</span></span> <span data-ttu-id="5ca18-116">لمزيد من المعلومات حول كيفية تصميم نماذج بيانات التقارير الإلكترونية، راجع [تصميم نموذج البيانات الخاص بالمجال للتقارير الإلكترونية](tasks/er-design-domain-specific-data-model-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5ca18-116">For information about how to design ER data models, see [ER Design domain specific data model](tasks/er-design-domain-specific-data-model-2016-11.md).</span></span>

### <a name="configure-the-er-model-mapping"></a><span data-ttu-id="5ca18-117">تعيين نموذج بيانات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5ca18-117">Configure the ER model mapping</span></span>
<span data-ttu-id="5ca18-118">يجب أن يتضمن تطبيقك تعيين نموذج التقارير الإلكترونية لنموذج البيانات CustomersInvoicing.</span><span class="sxs-lookup"><span data-stu-id="5ca18-118">Your application must include the ER model mapping for the CustomersInvoicing data model.</span></span> <span data-ttu-id="5ca18-119">بإمكان تعيين النموذج أن يكون في تكوين نموذج بيانات التقارير الإلكترونية أو في تكوين تعيين نموذج بيانات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5ca18-119">The model mapping can be in either the ER data model configuration or the ER model mapping configuration.</span></span> <span data-ttu-id="5ca18-120">ومع ذلك، يجب أن يكون **FreeTextInvoice** اسم واصف الجذر لتعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="5ca18-120">However, the name of the root descriptor of the model mapping must be **FreeTextInvoice**.</span></span>

<span data-ttu-id="5ca18-121">يجب أن يحتوي التعيين على مصادر البيانات التالية:</span><span class="sxs-lookup"><span data-stu-id="5ca18-121">The mapping must contain the following data sources:</span></span>

- <span data-ttu-id="5ca18-122">نوع مصدر البيانات: **سجلات الجدول**</span><span class="sxs-lookup"><span data-stu-id="5ca18-122">Data source type: **Table records**</span></span>

    - <span data-ttu-id="5ca18-123">يجب أن يحمل مصدر البيانات هذا الاسم **CustInvoiceJour**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-123">This data source must be named **CustInvoiceJour**.</span></span>
    - <span data-ttu-id="5ca18-124">يجب أن يشير إلى جدول التطبيق CustInvoiceJour.</span><span class="sxs-lookup"><span data-stu-id="5ca18-124">It must refer to the CustInvoiceJour application table.</span></span>
    - <span data-ttu-id="5ca18-125">يُستخدم في وقت التشغيل للمرور من التطبيق إلى نموذج التقارير الإلكترونية مع تعيين قائمة الفواتير التي تم تحديدها للطباعة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-125">It's used at runtime to pass from the application to the ER model mapping the list of invoices that have been selected for printing.</span></span>

- <span data-ttu-id="5ca18-126">نوع مصدر البيانات: **كائن**</span><span class="sxs-lookup"><span data-stu-id="5ca18-126">Data source type: **Object**</span></span>

    - <span data-ttu-id="5ca18-127">يجب أن يحمل مصدر البيانات هذا الاسم **PrintMgmtPrintSettingDetail‎**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-127">This data source must be named **PrintMgmtPrintSettingDetail**.</span></span>
    - <span data-ttu-id="5ca18-128">يجب أن يشير إلى فئة التطبيق **PrintMgmtPrintSettingDetail**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-128">It must refer to the **PrintMgmtPrintSettingDetail** application class.</span></span>
    - <span data-ttu-id="5ca18-129">‏‫يُستخدم في وقت التشغيل للمرور من التطبيق إلى نموذج التقارير الإلكترونية مع تعيين تفاصيل إعدادات إدارة الطباعة لتنسيق التقارير الإلكترونية قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="5ca18-129">It's used at runtime to pass from the application to the ER model mapping details of the print management settings for the ER format that is running.</span></span>

<span data-ttu-id="5ca18-130">يمكن العثور على تفاصيل حول تكامل التطبيق مع إطار عمل التقارير الإلكترونية في الفئة **ERPrintMgmtReportFormatSubscriber** (مجموعة تطبيقات التقارير الإلكترونية) في التعليمات البرمجية المصدر للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="5ca18-130">The details of the application integration with the ER framework can be found in the **ERPrintMgmtReportFormatSubscriber** class (ER Application Suite integration model) in the source code of the application.</span></span>

<span data-ttu-id="5ca18-131">للحصول على مزيد من المعلومات حول تعيينات نموذج التقارير الإلكترونية، راجع [تحديد تعيينات نماذج التقارير الإلكترونية وتحديد مصادر البيانات لها](tasks/er-define-model-mapping-select-data-sources-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5ca18-131">For more information about the design of ER model mappings, see [Define ER model mappings and select data sources for them](tasks/er-define-model-mapping-select-data-sources-2016-11.md).</span></span>

### <a name="configure-the-er-format"></a><span data-ttu-id="5ca18-132">تكوين تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5ca18-132">Configure the ER format</span></span>
<span data-ttu-id="5ca18-133">في مثيل تطبيقك، يجب أن يتوفر لديك تنسيق التقارير الإلكترونية الذي سيتم استخدامه لإنشاء نماذج FTI.</span><span class="sxs-lookup"><span data-stu-id="5ca18-133">In your application instance, you must have the ER format configuration that will be used to generate FTI forms.</span></span> 

> [!NOTE]
> <span data-ttu-id="5ca18-134">يجب إنشاء تكوين التنسيق هذا لنموذج البيانات CustomersInvoicing، ويجب أن يستخدم تعيين النموذج مع واصف الجذر **FreeTextInvoice**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-134">This format configuration must be created for the CustomersInvoicing data model, and it must use the model mapping that has the **FreeTextInvoice** root descriptor.</span></span>

<span data-ttu-id="5ca18-135">لمزيد من المعلومات حول كيفية تكوين تنسيقات التقارير الإلكترونية، راجع [إنشاء تكوين تنسيق للتقارير الإلكترونية‬ (نوفمبر 2016)](tasks/er-format-configuration-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5ca18-135">For information about how to configure ER formats, see [ER Create a format configuration (November 2016)](tasks/er-format-configuration-2016-11.md).</span></span> <span data-ttu-id="5ca18-136">لمزيد من المعلومات حول كيفية تصميم تنسيقات التقارير الإلكترونية لإنشاء تقارير بتنسيق OpenXML، راجع [تصميم تكوين لإنشاء التقارير بتنسيق OPENXML للتقارير الإلكترونية​‬ (نوفمبر 2016)](tasks/er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5ca18-136">For information about how to design ER formats to generate reports in OpenXML format, see [ER Design a configuration for generating reports in OPENXML format (November 2016)](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="configure-print-management"></a><span data-ttu-id="5ca18-137">تكوين إدارة الطباعة</span><span class="sxs-lookup"><span data-stu-id="5ca18-137">Configure print management</span></span>
<span data-ttu-id="5ca18-138">لإنشاء نماذج FTI باستخدام إطار عمل التقارير الإلكترونية، يمكنك تعيين تنسيقات التقارير الإلكترونية بالطريقة نفسها التي تعيّن بها تقارير SSRS.</span><span class="sxs-lookup"><span data-stu-id="5ca18-138">To generate FTI forms by using the ER framework, you can assign ER formats in the same way that you assign SSRS reports.</span></span> <span data-ttu-id="5ca18-139">لإقران تنسيق التقارير الإلكترونية بكافة فواتير النص الحر (FTI) للحسابات المدينة، انتقل إلى **الحسابات المدينة** \> **إعداد** \> **نماذج** \> **إعداد النموذج** \> **عام** \> **إدارة الطباعة** \> **فاتورة نص حر** \> **أصلي**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-139">To associate the ER format with all Accounts receivable FTIs, go to **Accounts receivable** \> **Setup** \> **Forms** \> **Form setup** \> **General** \> **Print management** \> **Free text invoice** \> **Original**.</span></span> <span data-ttu-id="5ca18-140">لإقران تنسيق التقارير الإلكترونية بعميل معين أو فاتورة معينة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="5ca18-140">To associate the ER format with a specific customer or invoice, follow these steps.</span></span>

1. <span data-ttu-id="5ca18-141">انتقل إلى **الحسابات المدين** \> **الفواتير** \> **جميع الفواتير بنص حر‬**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-141">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="5ca18-142">حدد فاتورة النص الحر (FTI) لإقران تنسيق التقارير الإلكترونية بها، وافتح صفحة **إعداد إدارة الطباعة**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-142">Select the FTI to associate the ER format with, and open the **Print management setup** page.</span></span>
3. <span data-ttu-id="5ca18-143">حدد مستوى المستند لتحديد نطاق الفواتير المطلوب معالجتها.</span><span class="sxs-lookup"><span data-stu-id="5ca18-143">Select the document level to specify the scope of invoices for processing.</span></span>
4. <span data-ttu-id="5ca18-144">حدد تنسيق التقارير الإلكترونية لمستوى المستند المحدد.</span><span class="sxs-lookup"><span data-stu-id="5ca18-144">Select the ER format for the specified document level.</span></span>

![إعداد إدارة الطباعة](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> <span data-ttu-id="5ca18-146">تنسيقات التقارير الإلكترونية التي تستخدم واصف الجذر **FreeTextInvoice** في نموذج البيانات **CustomersInvoicing** هي وحدها التي تظهر في الحقل **بحث عن تنسيق التقرير** للتنسيق المحدد.</span><span class="sxs-lookup"><span data-stu-id="5ca18-146">Only ER formats that use the **FreeTextInvoice** root descriptor of the **CustomersInvoicing** data model appear in the **Report format lookup** field for the selected format.</span></span>

## <a name="generate-fti-forms"></a><span data-ttu-id="5ca18-147">إنشاء نماذج FTI</span><span class="sxs-lookup"><span data-stu-id="5ca18-147">Generate FTI forms</span></span>
<span data-ttu-id="5ca18-148">يتم إنشاء نماذج FTI في إطار عمل التقارير الإلكترونية بالطريقة نفسها التي يتم بها إنشاء تقارير SSRS.</span><span class="sxs-lookup"><span data-stu-id="5ca18-148">FTI forms are generated in the ER framework in the same way that SSRS reports are generated.</span></span>

<span data-ttu-id="5ca18-149">لإنشاء نماذج FTI، يمكنك تحديد الفواتير إما بحسب النطاق أو بحسب التحديد.</span><span class="sxs-lookup"><span data-stu-id="5ca18-149">To generate FTI forms, you can select invoices either by range or by selection.</span></span> 

![تحديد الفواتير](media/FTIbyGER-InvoiceSelection.png)

![معاينة الفواتير](media/FTIbyGER-InvoiceExcelPreview.png)

<span data-ttu-id="5ca18-152">عندما تستخدم تنسيقات التقارير الإلكترونية لطباعة نماذج FTI بهذه الطريقة، يتم استخدام الوجهات الافتراضية لملفات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5ca18-152">When you use ER formats to print FTI forms in this way, the default ER file destinations are used.</span></span> <span data-ttu-id="5ca18-153">لا الافتراضي تغيير الوجهة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-153">You can't change the destination.</span></span> <span data-ttu-id="5ca18-154">لمزيد من المعلومات حول كيفية تكوين وجهات التقارير الإلكترونية لتنسيقات التقارير الإلكترونية، راجع [وجهات التقارير الإلكترونية (ER)‬](electronic-reporting-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="5ca18-154">For more information about how to configure the ER destinations for ER formats, see [Electronic reporting (ER) destinations](electronic-reporting-destinations.md).</span></span>

<span data-ttu-id="5ca18-155">يمكنك أيضا إنشاء نماذج FTI عندما تقوم بترحيل فاتورة FTI عن طريق تشغيل **طباعة فاتورة** وإيقاف تشغيل **استخدام وجهات إدارة الطباعة**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-155">You can also generate FTI forms when you post an FTI, by turning **Print invoice** on and turning **Use print management destinations** off.</span></span>

> [!NOTE]
> <span data-ttu-id="5ca18-156">عندما تستخدم تنسيقات التقارير الإلكترونية لطباعة نماذج FTI بهذه الطريقة، يتم استخدام الوجهات الافتراضية لملفات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5ca18-156">When you use ER formats to print FTI forms in this way, the default ER file destinations are used.</span></span> <span data-ttu-id="5ca18-157">يمكنك تغيير الوجهة الافتراضية في وقت التشغيل إذا كان تكوين الوجهة قد تم في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="5ca18-157">You can change the default destination at runtime if the destination has already been configured.</span></span> <span data-ttu-id="5ca18-158">لتغيير الوجهة، يجب أن يكون لديك امتياز الأمان التالي:</span><span class="sxs-lookup"><span data-stu-id="5ca18-158">To change the destination, you must have the following security privilege:</span></span>
>
> - <span data-ttu-id="5ca18-159">**الاسم:** ERFormatDestinationRuntimeMaintain</span><span class="sxs-lookup"><span data-stu-id="5ca18-159">**Name:** ERFormatDestinationRuntimeMaintain</span></span>
> - <span data-ttu-id="5ca18-160">**التسمية:** الاحتفاظ بوجهة ‏‫تنسيق إعداد التقارير الإلكترونية‬ أثناء وقت التشغيل</span><span class="sxs-lookup"><span data-stu-id="5ca18-160">**Label:** Maintain electronic reporting format destination during runtime</span></span>

![وجهة التقارير الإلكترونية‬](media/FTIbyGER-ERFileDestinationSetting.png)

![وجهة ‏‫تنسيق التقارير الإلكترونية](media/FTIbyGER-ERFileDestinationUsage.png)

<span data-ttu-id="5ca18-163">يدعم إطار عمل التقارير الإلكترونية في الوقت الحالي الوجهات التالية للمستندات التي تم إنشاؤها:</span><span class="sxs-lookup"><span data-stu-id="5ca18-163">The ER framework currently supports the following destinations for generated documents:</span></span>

- <span data-ttu-id="5ca18-164">**الملف الذي تم تنزيله** – يتم تقديم النماذج المُنشأة كتنزيلات يمكنك حفظها باستخدام المستعرض.</span><span class="sxs-lookup"><span data-stu-id="5ca18-164">**Downloaded file** – Generated forms are offered as downloads that you can save by using the browser.</span></span>
- <span data-ttu-id="5ca18-165">**الشاشة** – يُستخدم Microsoft 365 Excel لمعاينة نماذج FTI التي تم إنشاؤها بتنسيق Excel.</span><span class="sxs-lookup"><span data-stu-id="5ca18-165">**Screen** – Microsoft 365 Excel is used to preview generated FTI forms in Excel format.</span></span>
- <span data-ttu-id="5ca18-166">**مجلد SharePoint** – يتم تخزين النماذج المُنشأة استنادًا إلى الإعدادات الخاصة بإطار عمل إدارة المستندات.</span><span class="sxs-lookup"><span data-stu-id="5ca18-166">**SharePoint folder** – Generated forms are stored based on the settings of the Document management framework.</span></span>
- <span data-ttu-id="5ca18-167">**أرشيف التطبيق** – يتم تخزين النماذج المُنشأة كمرفقات لسجلات التنفيذ في Microsoft Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5ca18-167">**Application archive** – Generated forms are stored as attachments of execution log records in the Microsoft Azure Storage.</span></span>
- <span data-ttu-id="5ca18-168">**البريد الإلكتروني** – يتم إرسال النماذج المُنشأة كمرفقات بريد إلكتروني.</span><span class="sxs-lookup"><span data-stu-id="5ca18-168">**Email** – Generated forms are sent as email attachments.</span></span>

> [!NOTE]
> <span data-ttu-id="5ca18-169">لا يمكنك إرسال نماذج FTI المُنشأة مباشرة إلى الطابعة، لأن الطباعة المباشرة التي تستخدم وكيل توجيه الطباعة في Dynamics غير مدعومة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="5ca18-169">You can't send the FTI forms that are generated directly to the printer, because direct printing that uses the Dynamics Printer Routing Agent isn't currently supported.</span></span>

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a><span data-ttu-id="5ca18-170">تنزيل عينات تكوينات التقارير الإلكترونية لإنشاء نماذج FTI قابلة للطباعة</span><span class="sxs-lookup"><span data-stu-id="5ca18-170">Download sample ER configurations to generate printable FTI forms</span></span>
<span data-ttu-id="5ca18-171">يمكنك تنزيل عينات تكوينات التقارير الإلكترونية لاستخدامها كقالب لحل FTI.</span><span class="sxs-lookup"><span data-stu-id="5ca18-171">You can download sample ER configurations to use as a template for your FTI solution.</span></span> <span data-ttu-id="5ca18-172">يتم تخزين التكوينات في مكتبة الأصول المشتركة في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5ca18-172">The configurations are stored in the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="5ca18-173">تتضمن التكوينات:</span><span class="sxs-lookup"><span data-stu-id="5ca18-173">The configurations include:</span></span>

- <span data-ttu-id="5ca18-174">يحتوي تكوين **نموذج فوترة العملاء** على نموذج البيانات المطلوبة وتعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="5ca18-174">The **Customer invoicing model** configuration contains the required data model and model mapping.</span></span>
- <span data-ttu-id="5ca18-175">يحتوي تكوين **تقرير FTI المخصص (GER)** على عينة التنسيق.</span><span class="sxs-lookup"><span data-stu-id="5ca18-175">The **Customer FTI report (GER)** configuration contains the sample format.</span></span>

> [!NOTE]
> <span data-ttu-id="5ca18-176">تم إنشاء هذه التكوينات كعينات للمساعدة في توضيح سيناريوهات محتملة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-176">These configurations have been created as samples to help clarify possible scenarios.</span></span> <span data-ttu-id="5ca18-177">يتوقف مستقبل هذه التكوينات على نتائج هذا التقييم وأي ملاحظات يتم تلقيها.</span><span class="sxs-lookup"><span data-stu-id="5ca18-177">The future of these configurations depends on the results of this evaluation and any feedback that is received.</span></span>

### <a name="features-that-are-implemented-in-the-sample-er-format"></a><span data-ttu-id="5ca18-178">الميزات المطبقة في عينة تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5ca18-178">Features that are implemented in the sample ER format</span></span>
<span data-ttu-id="5ca18-179">في عينة تكوين تنسيق التقارير الإلكترونية، يتم استخدام ملف Excel كقالب لإنشاء نماذج FTI.</span><span class="sxs-lookup"><span data-stu-id="5ca18-179">In the sample ER format configuration, an Excel file is used as a template to generate FTI forms.</span></span>

![مصمم التنسيق](media/FTIbyGER-ERFormat.png)

<span data-ttu-id="5ca18-181">في الوقت الحالي، تدعم عينة تنسيق التقارير الإلكترونية هذه الميزات التالية لإنشاء نماذج FTI:</span><span class="sxs-lookup"><span data-stu-id="5ca18-181">Currently, this sample ER format supports the following features to generate FTI forms:</span></span>

- <span data-ttu-id="5ca18-182">يتم إنشاء نماذج FTI لكل من الفواتير الأصلية التي تم ترحيلها والفواتير الأصلية التي لم يتم ترحيلها بعد.</span><span class="sxs-lookup"><span data-stu-id="5ca18-182">FTI forms are generated for both original invoices that have been posted and original invoices that haven't yet been posted.</span></span> <span data-ttu-id="5ca18-183">لا يتوفر الدعم للفواتير المصححة والإشعارات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-183">Corrected invoices and credit notes aren't supported.</span></span>
- <span data-ttu-id="5ca18-184">يتم إنشاء نماذج FTI بلغة الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-184">FTI forms are generated in the invoice language.</span></span> <span data-ttu-id="5ca18-185">يستند تنسيق القيم والتواريخ في النماذج المُنشأة إلى الإعدادات المحلية لعميل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="5ca18-185">The format of values and dates in the generated forms is based on the settings of the user's client locale.</span></span>
- <span data-ttu-id="5ca18-186">تُظهر الفواتير المُنشاة إعلامات حول عدم توفر البيانات في حال عدم وجود بنود في الفواتير التي تتم معالجتها.</span><span class="sxs-lookup"><span data-stu-id="5ca18-186">Generated invoices show data unavailability notifications if there are no lines in the invoices that are processed.</span></span>
- <span data-ttu-id="5ca18-187">تستند رؤوس الفواتير المُنشاة إلى تنسيق الورق الذي تم تحديده لنموذج FTI في صفحة **معلمات الحسابات المدينة‬**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-187">Generated invoice headers are based on the paper format that has been selected for the FTI form on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="5ca18-188">تظهر تفاصيل الشركة في رأس الفاتورة المُنشأة فقط إذا كان تنسيق الورق فارغًا.</span><span class="sxs-lookup"><span data-stu-id="5ca18-188">Company details appear in the header of the generated invoice form only if the paper format is blank.</span></span>
- <span data-ttu-id="5ca18-189">تُظهر نماذج الفواتير المُنشأة أرقام الإعفاء الضريبي‬ للشركة والعميل عند تحديد الخيار المناسب لنموذج FTI في صفحة **معلمات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-189">Generated invoice forms show company and customer tax exempt numbers when the appropriate option has been selected for the FTI form on the **Accounts receivable parameters** page.</span></span>
- <span data-ttu-id="5ca18-190">تُظهر أقسام بنود الفاتورة المُنشأة وإجماليات الفاتورة التفاصيل المالية الافتراضية للفاتورة بعملة تسجيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-190">The generated invoice lines and invoice totals sections show the default invoice's monetary details in the invoice registration currency.</span></span>
- <span data-ttu-id="5ca18-191">بإمكان قسم إجماليات الفاتورة المُنشأة إظهار التفاصيل المالية بعملة اليورو وعملة تسجيل الفاتورة عند تمكين الخيار **طباعة المبلغ بعملة تمثل اليورو‬** في صفحة **معلمات الحسابات المدينة‬**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-191">The generated invoice totals section can show monetary details in the euro currency and the invoice registration currency when the **Print amount in currency representing the euro** option is enabled on the **Accounts receivable parameters** page.</span></span>
- <span data-ttu-id="5ca18-192">تُظهر نماذج الفواتير المُنشأة أي ملاحظات حول معالجة الفاتورة تتوفر استنادًا إلى الإعدادات في صفحة **معلمات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-192">Generated invoice forms show any process invoice notes that are available, based on settings on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="5ca18-193">يتم تضمين الملاحظات للفاتورة بكاملها ولكل بند فيها.</span><span class="sxs-lookup"><span data-stu-id="5ca18-193">Notes are included for both the whole invoice and each invoice line.</span></span>
- <span data-ttu-id="5ca18-194">تتضمن نماذج الفواتير المُنشأة ملاحظات لنموذج FTI للعميل ولغة معالجة الفاتورة عندما يتم تكوينها في قائمة ملاحظات نموذج الحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-194">Generated invoice forms include notes for the customer FTI form and the processing invoice language when they have been configured in the AR form notes list.</span></span>
- <span data-ttu-id="5ca18-195">استنادًا إلى إعدادات إدارة الطباعة، تتضمن الفواتير المُنشاة نص تذييل مخصصًا عند تكوينها للغة الفاتورة وتنسيق التقارير الإلكترونية ونطاق مستند FTI.</span><span class="sxs-lookup"><span data-stu-id="5ca18-195">Depending on the Print management settings, generated invoices include custom footer text when it has been configured for the invoice language, the ER format, and the FTI document scope.</span></span>
- <span data-ttu-id="5ca18-196">يتضمن قسم الإجماليات في نماذج الفواتير المُنشأة أي معلومات متوفرة عن الخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="5ca18-196">The totals section of generated invoice forms includes any cash discount information that is available.</span></span>
- <span data-ttu-id="5ca18-197">يتضمن قسم جدول الدفع في نماذج الفواتير المُنشاة أي تفاصيل متوفرة حول جدول الدفع.</span><span class="sxs-lookup"><span data-stu-id="5ca18-197">The payment schedule section of generated invoice forms includes any payment schedule details that are available.</span></span>
- <span data-ttu-id="5ca18-198">يتضمن قسم العلامات في نماذج الفواتير المُنشاة أي حركات مصاريف المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-198">The markup section of generated invoice forms includes any charges transactions that are available.</span></span>
- <span data-ttu-id="5ca18-199">تتضمن نماذج الفواتير المُنشأة تفاصيل حول ضريبة الدفع، استنادًا إلى إعداد **مواصفات ضريبة المبيعات‬** في صفحة **معلمات الحسابات المدينة‬**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-199">Generated invoice forms include sales tax details, based on the **Sales tax specification** setting on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="5ca18-200">يُظهر هذا القسم تفاصيل حول الضرائب بعملة تسجيل الفاتورة فقط، أو بعملة تسجيل الفاتورة وعملة المحاسبة للشركة في الوقت نفسه.</span><span class="sxs-lookup"><span data-stu-id="5ca18-200">This section can show tax details either in the invoice registration currency only, or in the invoice registration currency and the company accounting currency at the same time.</span></span>
- <span data-ttu-id="5ca18-201">تُظهر نماذج الفواتير المُنشأة تفاصيل إخطار الخصم المباشر.</span><span class="sxs-lookup"><span data-stu-id="5ca18-201">Generated invoice forms show direct debit notification details.</span></span> <span data-ttu-id="5ca18-202">على سبيل المثال، تُظهر هذه الوقت متى تم فيه اختيار طريقة الدفع التي تشتمل على معرّف تفويض الخصم المباشر‬ للفاتورة، ومتى تم تسجيل معالجة الفاتورة بعملة اليورو، ومتى تم تعريف معرّف تفويض الخصم المباشر للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-202">For example, they show when the method of payment that has the mandatory direct debit mandate ID was selected for the invoice, when the processing invoice was registered in the euro currency, and when the direct debit mandate ID was defined for the invoice.</span></span>
- <span data-ttu-id="5ca18-203">تُظهر الفواتير التي المُنشأة تفاصيل الدفعة المقدمة التي تتوفر للفواتير التي تم ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="5ca18-203">Generated invoices show any prepayment details that are available for posted invoices.</span></span>
- <span data-ttu-id="5ca18-204">يمكن إرسال نماذج الفواتير المُنشأة إلى عميل فاتورة كمرفق بريد إلكتروني.</span><span class="sxs-lookup"><span data-stu-id="5ca18-204">Generated invoice forms can be sent to an invoice customer as an email attachment.</span></span> <span data-ttu-id="5ca18-205">يجب تكوين وجهة ملف التقارير الإلكترونية لمناسب لتنسيق التقارير الإلكترونية قيد الاستخدام.</span><span class="sxs-lookup"><span data-stu-id="5ca18-205">The appropriate ER file destination should be configured for the ER format that is being used.</span></span>

### <a name="countryregion-specific-features"></a><span data-ttu-id="5ca18-206">ميزات خاصة على مستوى البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="5ca18-206">Country/region-specific features</span></span> 
<span data-ttu-id="5ca18-207">تم تضمين الميزات التالية الخاصة بالبلد/المنطقة في عينة تنسيق التقارير الإلكترونية‬ لإظهار كيفية التعامل مع المتطلبات الخاصة في تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5ca18-207">The following country/region-specific features are included in the sample ER format to show how specific requirements can be handled in ER configurations.</span></span>

#### <a name="norway"></a><span data-ttu-id="5ca18-208">النرويج</span><span class="sxs-lookup"><span data-stu-id="5ca18-208">Norway</span></span>
<span data-ttu-id="5ca18-209">يوضع مصطلح مسجّل المؤسسة على رأس نموذج الفاتورة المُنشأة عندما تتم معالجة فاتورة لكيان قانوني تم تكوينه على النحو التالي:</span><span class="sxs-lookup"><span data-stu-id="5ca18-209">The Enterprise register term is put on the header of the generated invoice form when the invoice is processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="5ca18-210">تم استخدام سياق البلد/المنطقة للنرويج.</span><span class="sxs-lookup"><span data-stu-id="5ca18-210">The country/region context for Norway is used.</span></span>
- <span data-ttu-id="5ca18-211">المعلمة **Print Foretaksregisteret** نشطة في مستندات المبيعات.</span><span class="sxs-lookup"><span data-stu-id="5ca18-211">The **Print Foretaksregisteret** parameter is active on sales documents.</span></span>

#### <a name="spain"></a><span data-ttu-id="5ca18-212">إسبانيا</span><span class="sxs-lookup"><span data-stu-id="5ca18-212">Spain</span></span>
<span data-ttu-id="5ca18-213">يوضع المصطلح **نظام خاص لطريقة المحاسبة النقدية‬** مصطلح مسجّل المؤسسة على رأس نموذج الفاتورة المُنشأة عندما تتم معالجة فاتورة لكيان قانوني تم تكوينه على النحو التالي:</span><span class="sxs-lookup"><span data-stu-id="5ca18-213">The **Special regime for cash accounting method** term is put on the header of the generated invoice form when the invoice is processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="5ca18-214">تم استخدام سياق البلد/المنطقة لأسبانيا.</span><span class="sxs-lookup"><span data-stu-id="5ca18-214">The country/region context for Spain is used.</span></span>
- <span data-ttu-id="5ca18-215">يتم تمكين النظام الخاص لطريقة المحاسبة النقدية‬ بتاريخ معالجة الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-215">The special regime for the cash accounting method is enabled on the invoice processing date.</span></span>

<span data-ttu-id="5ca18-216">عندما تتوفر تفاصيل الخصم النقدي، مثل مبلغ الخصم النقدي والمبلغ الصافي لبند الفاتورة، يتم تقديمها في قسم إجماليات الفاتورة في نموذج الفاتورة المُنشاة عندما تتم معالجتها لكيان قانوني تم تكوينه بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="5ca18-216">When cash discount details, such as the cash discount amount and invoice line net amount, are available, they are presented in the invoice totals section of the generated invoice form when it has been processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="5ca18-217">تم استخدام سياق البلد/المنطقة لأسبانيا.</span><span class="sxs-lookup"><span data-stu-id="5ca18-217">The country/region context for Spain is used.</span></span>
- <span data-ttu-id="5ca18-218">يتم تشغيل **يتم تطبيق الخصم النقدي في الفاتورة‬** على خيار الفاتورة (**محددات دفتر الأستاذ العام‬** \> **قسم ضريبة المبيعات‬**).</span><span class="sxs-lookup"><span data-stu-id="5ca18-218">**Cash discount is applied in the invoice** is turned on in the invoice option (**General ledger parameters** \> **Sales tax section**).</span></span>

#### <a name="italy"></a><span data-ttu-id="5ca18-219">إيطاليا</span><span class="sxs-lookup"><span data-stu-id="5ca18-219">Italy</span></span>
<span data-ttu-id="5ca18-220">يتم تضمين علامة خصم السلع على بنود الفاتورة المُنشأة عندما تتم معالجتها لكيان قانوني تم تكوينه باستخدام سياق البلد/المنطقة لإيطاليا.</span><span class="sxs-lookup"><span data-stu-id="5ca18-220">The goods discount mark is included on the invoice lines of the generated invoice when it's being processed for a legal entity that is configured using the country/region context for Italy.</span></span>

#### <a name="finland"></a><span data-ttu-id="5ca18-221">فنلندا</span><span class="sxs-lookup"><span data-stu-id="5ca18-221">Finland</span></span>
<span data-ttu-id="5ca18-222">بالإضافة إلى نموذج الفاتورة المُنشأة، يمكن إنشاء قسائم الحوالة النقدية بنظام giro‬ كما يلي:</span><span class="sxs-lookup"><span data-stu-id="5ca18-222">In addition to the generated invoice form, Giro money transfer slips can be generated as follows:</span></span>

- <span data-ttu-id="5ca18-223">للكيان القانوني الذي يستخدم سياق البلد/المنطقة لفنلندا، وله حساب بنكي واحد على الأقل وضعت عليه علامة **حساب Giro** و **الرمز الشريطي للبنك‬**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-223">For the legal entity that uses the country/region context for Finland, and that has at least one bank account that is marked as **Giro account** and **Bank bar code**.</span></span> 
- <span data-ttu-id="5ca18-224">بالنسبة إلى فاتورة تم وضع علامة عليها على أنها مطلوبة لمرفق الدفع المقترن **الفنلندي**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-224">For an invoice that is marked as required for the **Finnish** associated payment attachment.</span></span>

![قسيمة Giro](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> <span data-ttu-id="5ca18-226">تم تكوين عينة تنسيق التقارير الإلكترونية‬ لإنشاء قسائم الحوالات النقدية بنظام giro‬ في ورقة العمل المنفصلة، بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="5ca18-226">The sample ER format has been configured to optionally generate the Giro money transfer slips in the separate worksheet.</span></span>

> [!NOTE]
> <span data-ttu-id="5ca18-227">يجب عليك أولاً تثبيت الخط المستخدم لإنشاء الكود الشريطي على الجهاز المحلي حيث يتم عرض نموذج الفاتورة المُنشأة بتنسيق Excel.</span><span class="sxs-lookup"><span data-stu-id="5ca18-227">You must first install the font that is used to generate the bar code on the local machine where the generated invoice form in Excel format will be previewed.</span></span>

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a><span data-ttu-id="5ca18-228">استخدام عينة تنسيق التقارير الإلكترونية‬ لتكوين وجهات البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="5ca18-228">Use the sample ER format to configure email destinations</span></span>
<span data-ttu-id="5ca18-229">استخدم العناصر التالية لعينة تنسيق التقارير الإلكترونية‬ لتكوين وجهات البريد الإلكتروني:</span><span class="sxs-lookup"><span data-stu-id="5ca18-229">Use the following elements of the sample ER format to configure email destinations:</span></span>

- <span data-ttu-id="5ca18-230">يمكن الوصول إلى عنوان البريد الإلكتروني لجهة اتصال العميل من خلال تعبير التقرير الإلكتروني التالي: **model.InvoiceBase.Contact.ElectronicMail**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-230">The email address of a customer contact can be accessed through the following ER expression: **model.InvoiceBase.Contact.ElectronicMail**.</span></span>
- <span data-ttu-id="5ca18-231">يمكن الوصول إلى نص موضوع البريد الإلكتروني من خلال تعبير التقرير الإلكتروني التالي: **Emailing.TxtToUse.Subject**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-231">The email subject text can be accessed through the following ER expression: **Emailing.TxtToUse.Subject**.</span></span>
- <span data-ttu-id="5ca18-232">يمكن الوصول إلى النص الأساسي للبريد الإلكتروني من خلال تعبير التقرير الإلكتروني التالي: **Emailing.TxtToUse.Body**.</span><span class="sxs-lookup"><span data-stu-id="5ca18-232">The email body text can be accessed through the following ER expression: **Emailing.TxtToUse.Body**.</span></span>

![إعدادات الوجهة](media/FTIbyGER-ERFileDestinationSettingEmail.png)

<span data-ttu-id="5ca18-234">يتم تعريف النص الافتراضي لموضوع البريد الإلكتروني ونصه الأساسي في عينة تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5ca18-234">The default text of the email's subject and body is defined in the sample ER format.</span></span> <span data-ttu-id="5ca18-235">تتوقف اللغة على تسميات التنسيق.</span><span class="sxs-lookup"><span data-stu-id="5ca18-235">The language depends on the format's labels.</span></span> <span data-ttu-id="5ca18-236">سيتم استخدام هذا النص الافتراضي لرسائل البريد الإلكتروني إذا لم تتم إضافة قالب بريد إلكتروني مخصص للمؤسسة الذي يحتوي على معرّف **ERFTITMP** المحدد مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="5ca18-236">This default text will be used for emails if a custom organization email template that has the predefined **ERFTITMP** ID hasn't been added.</span></span>

> [!NOTE]
> <span data-ttu-id="5ca18-237">تم تعريف معرّف قالب البريد الإلكتروني **ERFTITMP** في عينة تنسيق التقارير الإلكترونية‬.</span><span class="sxs-lookup"><span data-stu-id="5ca18-237">The **ERFTITMP** email template ID has been defined in the sample ER format.</span></span> <span data-ttu-id="5ca18-238">ويمكن تغييره كما هو مطلوب إلى تنسيق تقارير إلكترونية جديد يتم إنشاؤه من عينة التنسيق هذه.</span><span class="sxs-lookup"><span data-stu-id="5ca18-238">It can be changed as required in a new ER format that is created from this sample format.</span></span>

<span data-ttu-id="5ca18-239">إذا تم إضافة قالب البريد الإلكتروني للمؤسسة الذي يحتوي على معّرف **ERFTITMP** المحدد مسبقًا إلى الكيان القانوني الذي تعمل على معالجة الفاتورة له، فسيتم استخدام قالب موضوع البريد الإلكتروني ونصه الأساسي لإنشاء رسالة بريد إلكتروني.</span><span class="sxs-lookup"><span data-stu-id="5ca18-239">If the organization email template that has the predefined **ERFTITMP** ID has been added for the legal entity that you're processing the invoice for, the template for the email subject and body text will be used to generate the email.</span></span> 

![قوالب البريد الإلكتروني للمؤسسة](media/FTIbyGER-EmailTemplate.png)

![تحميل قالب البريد الإلكتروني](media/FTIbyGER-EmailTemplateBody.png)

<span data-ttu-id="5ca18-242">يتم تكوين تعبير التقارير الإلكترونية **Emailing.TxtToUse.Subject** لعينة تنسيق التقارير الإلكترونية‬ لاستبدال أي حدوث للعنصر النائب %1 بواسطة معرّف معالجة الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-242">The **Emailing.TxtToUse.Subject** ER expression of the sample ER format is configured to replace any occurrences of the placeholder %1 by the processing invoice ID.</span></span>

<span data-ttu-id="5ca18-243">يتم تكوين تعبير **Emailing.TxtToUse.Body** لعينة التنسيق للاستبدالات التالية للعناصر النائبة:</span><span class="sxs-lookup"><span data-stu-id="5ca18-243">The **Emailing.TxtToUse.Body** expression of the sample format is configured for the following substitutions for placeholders:</span></span>

- <span data-ttu-id="5ca18-244">يتم استبدال "%1" باسم جهة اتصال العميل.</span><span class="sxs-lookup"><span data-stu-id="5ca18-244">"%1" is replaced with the name of the customer's contact person.</span></span>
- <span data-ttu-id="5ca18-245">يتم استبدال "%2" باسم الشركة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-245">"%2" is replaced with the company name.</span></span>
- <span data-ttu-id="5ca18-246">يتم استبدال "%3" باسم العميل.</span><span class="sxs-lookup"><span data-stu-id="5ca18-246">"%3" is replaced with the customer name.</span></span>
- <span data-ttu-id="5ca18-247">يتم استبدال "%4" باسم شخص جهة اتصال الشركة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-247">"%4" is replaced with the name of the company's contact person.</span></span>
- <span data-ttu-id="5ca18-248">يتم استبدال "%5" بالمسمى الوظيفي لشخص جهة اتصال الشركة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-248">"%5" is replaced with the job title of the company's contact person.</span></span>
- <span data-ttu-id="5ca18-249">يتم استبدال "%6" بعنوان البريد الإلكتروني لشخص جهة اتصال الشركة.</span><span class="sxs-lookup"><span data-stu-id="5ca18-249">"%6" is replaced with the email address of the company's contact person.</span></span>

![البريد الإلكتروني](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a><span data-ttu-id="5ca18-251">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5ca18-251">Additional resources</span></span>
[<span data-ttu-id="5ca18-252">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5ca18-252">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]