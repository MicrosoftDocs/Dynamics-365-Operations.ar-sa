---
title: بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في المكسيك
description: يوفر هذا الموضوع معلومات تساعدك على بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في المكسيك في Microsoft Dynamics 365 Finance وفي Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 6d15a79a359b3c708b2b33893d700377a57c3eb7
ms.sourcegitcommit: cfd84321fba38e02e270d361df369a536a48efa3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/11/2020
ms.locfileid: "4512224"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-mexico"></a><span data-ttu-id="e8c52-103">بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في المكسيك</span><span class="sxs-lookup"><span data-stu-id="e8c52-103">Get started with the Electronic invoicing add-on for Mexico</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="e8c52-104">قد لا تدعم الوظيفة الإضافية الفوترة الإلكترونية في المكسيك في الوقت الحالي جميع الوظائف المتوفرة في مستند Comprobante Fiscal Digital por Internet (CFDI)، وفي التكامل ذي الصلة المبني في Microsoft Dynamics 365 Finance أو Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e8c52-104">The Electronic invoicing add-on for Mexico might not currently support all the functions that are available in the Comprobante Fiscal Digital por Internet (CFDI) document, and in the related integration that is built into Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="e8c52-105">يوفر هذا الموضوع معلومات تساعدك على بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="e8c52-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Mexico.</span></span> <span data-ttu-id="e8c52-106">وهو يرشدك عبر خطوات التكوين التي تعتمد على البلد في Regulatory Configuration Services (RCS) وFinance.</span><span class="sxs-lookup"><span data-stu-id="e8c52-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="e8c52-107">ويقوم أيضًا بإرشادك عبر الخطوات التي يجب اتباعها في Finance لإرسال فواتير CFDI من خلال الخدمة، ويشرح كيفية مراجعة نتائج المعالجة وحالة فواتير CFDI.</span><span class="sxs-lookup"><span data-stu-id="e8c52-107">It also guides you through the steps that you must follow in Finance to submit CFDI invoices through the service, and it explains how to review the processing results and the status of CFDI invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e8c52-108">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="e8c52-108">Prerequisites</span></span>

<span data-ttu-id="e8c52-109">قبل إكمال الخطوات الواردة في هذا الموضوع، يجب إكمال الخطوات في [بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="e8c52-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="e8c52-110">إعداد RCS</span><span class="sxs-lookup"><span data-stu-id="e8c52-110">RCS setup</span></span>

<span data-ttu-id="e8c52-111">اثناء إعداد RCS، ستقوم بإكمال المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="e8c52-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="e8c52-112">استيراد ميزة الفوترة الإلكترونية لمعالجة فواتير CFDI.</span><span class="sxs-lookup"><span data-stu-id="e8c52-112">Import the e-Invoicing feature for processing CFDI invoices.</span></span>
2. <span data-ttu-id="e8c52-113">مراجعة تكوينات التنسيق المطلوبة لإنشاء الاستجابات حول فواتير CFDI وإرسالها وتلقيها، ولإرسال الاستجابات حول الإلغاء وتلقيها.</span><span class="sxs-lookup"><span data-stu-id="e8c52-113">Review the format configurations that are required to generate, submit, and receive responses about CFDI invoices, and to submit and receive responses about cancellation.</span></span>
3. <span data-ttu-id="e8c52-114">تكوين الأحداث التي تدعم سيناريوهات إرسال فواتير CFDI.</span><span class="sxs-lookup"><span data-stu-id="e8c52-114">Configure the events that support the CFDI invoice submission scenarios.</span></span>
4. <span data-ttu-id="e8c52-115">نشر ميزة الفوترة الإلكترونية لمعالجة فواتير CFDI.</span><span class="sxs-lookup"><span data-stu-id="e8c52-115">Publish the e-Invoicing feature for CFDI invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="e8c52-116">"ميزة الفوترة الإلكترونية" هي الاسم العام للمورد الذي تم تكوينه ونشره لاستهلاك خادم الوظيفة الإضافية الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e8c52-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="e8c52-117">في هذه الحالة، فواتير CFDI‏ (MX) هي ميزة الفوترة الإلكترونية التي ستقوم بإعدادها.</span><span class="sxs-lookup"><span data-stu-id="e8c52-117">In this case, CFDI invoices (MX) are the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="e8c52-118">استيراد ميزة الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e8c52-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="e8c52-119">سجل دخولك إلى حساب RCS.</span><span class="sxs-lookup"><span data-stu-id="e8c52-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="e8c52-120">في مساحة العمل **ميزات العولمة**، في قسم **الميزات**، حدد الإطار المتجانب **الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="e8c52-121">في الصفحة **ميزات الفوترة الإلكترونية**، حدد **استيراد** لاستيراد ميزة **فواتير CFDI‏ (MX)** من المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="e8c52-121">On the **e-Invoicing Features** page, select **Import** to import the **CFDI invoices (MX)** feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e8c52-122">إذا لم تظهر الميزة في القائمة، فحدد **مزامنة** ، ثم كرر الخطوة رقم 3.</span><span class="sxs-lookup"><span data-stu-id="e8c52-122">If you don't see the feature in the list, select **Synchronize**, and then repeat step 3.</span></span>

![استيراد ميزة فواتير CFDI‏ (MX)](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

<span data-ttu-id="e8c52-124">عند استيراد ميزة **فواتير CFDI ‏(MX)** من المستودع العمومي، يتم أيضًا استيراد كافة إعدادات الميزة، بما في ذلك التكوينات والإجراءات.</span><span class="sxs-lookup"><span data-stu-id="e8c52-124">When you import the **CFDI invoices (MX)** feature from the Global repository, all the feature settings, including configurations and actions, are also imported.</span></span>

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a><span data-ttu-id="e8c52-125">إنشاء إصدار جديد من ميزة فواتير CFDI ‏(MX)</span><span class="sxs-lookup"><span data-stu-id="e8c52-125">Create a new version of the CFDI invoices (MX) feature</span></span>

<span data-ttu-id="e8c52-126">يمكنك إنشاء إصدار جديد إذا كان، على سبيل المثال، يجب تحديث عناوين URL.</span><span class="sxs-lookup"><span data-stu-id="e8c52-126">You can create a new version if, for example, URLs must be updated.</span></span> <span data-ttu-id="e8c52-127">لمزيد من المعلومات، راجع [الفوترة الإلكترونية CFDI‎](tasks/mx-00010-e-invoicing-cfdi.md).</span><span class="sxs-lookup"><span data-stu-id="e8c52-127">For more information, see [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span></span>

- <span data-ttu-id="e8c52-128">في صفحة **ميزات الفوترة الإلكترونية**، على علامة التبويب **الإصدارات**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-128">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![إضافة إصدار جديد لميزة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="e8c52-130">تحديث إصدار التكوين</span><span class="sxs-lookup"><span data-stu-id="e8c52-130">Update the configuration version</span></span>

1. <span data-ttu-id="e8c52-131">في الصفحة **ميزات الفوترة الإلكترونية**، على علامة تبويب **التكوينات**، حدد **إضافة** أو **حذف** لإدارة إصدارات التكوين (تكوينات تنسيق ملفات التقارير الإلكترونية).</span><span class="sxs-lookup"><span data-stu-id="e8c52-131">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![إدارة تكوينات ميزة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    <span data-ttu-id="e8c52-133">عند إنشاء إصدار جديد، يتم توارث كافة التكوينات من آخر إصدار منشور.</span><span class="sxs-lookup"><span data-stu-id="e8c52-133">When you create a new version, all configurations are inherited from the last published version.</span></span> <span data-ttu-id="e8c52-134">لمعالجة فواتير CFDI، تحتاج إلى التكوينات التالية:</span><span class="sxs-lookup"><span data-stu-id="e8c52-134">To process CFDI invoices, the following configurations are required:</span></span>

    - <span data-ttu-id="e8c52-135">فاتورة CFDI‏ (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="e8c52-135">CFDI invoice (BusinessDocumentService)</span></span>
    - <span data-ttu-id="e8c52-136">استيراد رسالة استجابة CFDI</span><span class="sxs-lookup"><span data-stu-id="e8c52-136">CFDI response message import</span></span>
    - <span data-ttu-id="e8c52-137">استيراد سجل أخطاء CFDI</span><span class="sxs-lookup"><span data-stu-id="e8c52-137">CFDI error log import</span></span>
    - <span data-ttu-id="e8c52-138">طلب إلغاء CFDI‏ (MX) (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="e8c52-138">CFDI cancelation request (MX) (BusinessDocumentService)</span></span>
    - <span data-ttu-id="e8c52-139">فاتورة CFDI‏ (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="e8c52-139">CFDI invoice (BusinessDocumentService)</span></span>

2. <span data-ttu-id="e8c52-140">في القائمة، حدد إصدار تكوين، ثم حدد **تحرير** أو **عرض** لفتح الصفحة **مصمم التنسيق**، حيث يمكنك تحرير التكوين أو عرضه.</span><span class="sxs-lookup"><span data-stu-id="e8c52-140">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![فتح صفحة مصمم التنسيق](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. <span data-ttu-id="e8c52-142">استخدم الصفحة **مصمم التنسيق** لتحرير وعرض تكوينات ملف تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e8c52-142">Use the **Format designer** page to edit and view the ER format file configurations.</span></span> <span data-ttu-id="e8c52-143">للحصول على مزيد من التفاصيل، راجع [إنشاء تكوينات المستندات الإلكترونية](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="e8c52-143">For more information, see [Create electronic document configurations](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span></span>

    ![صفحة مصمم التنسيق‬](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="e8c52-145">إدارة عمليات إعداد ميزة الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e8c52-145">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="e8c52-146">في صفحة **ميزات الفوترة الإلكترونية**، على علامة تبويب **عمليات الإعداد**، حدد **إضافة** أو **حذف** أو **تحرير** لإدارة عمليات إعداد ميزة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e8c52-146">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![إدارة عمليات إعداد ميزة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

<span data-ttu-id="e8c52-148">لإرسال فواتير CFDI للتخويل (إنشاء ملف XML، وإرسال ملف XML، ومعالجة الاستجابة)، يجب إعداد ميزة **فاتورة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-148">To submit CFDI invoices for authorization (generate the XML file, submit the XML file, and process the response), the **Sales invoice** feature setup is required.</span></span>

<span data-ttu-id="e8c52-149">لإرسال إلغاء فواتير CFDI، يجب إعداد ميزتي **طلب الإلغاء** و **الإلغاء**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-149">To submit CFDI invoice cancellation, the **Cancellation** and **Cancel** feature setups are required.</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="e8c52-150">تكوين إعداد ميزة فاتورة المبيعات</span><span class="sxs-lookup"><span data-stu-id="e8c52-150">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="e8c52-151">في صفحة **ميزات الفوترة الإلكترونية‬**، على علامة تبويب **عمليات الإعداد** في العمود **إعداد الميزة**، حدد **فاتورة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-151">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="e8c52-152">حدد **تحرير** لتكوين الإجراءات وقواعد قابلية التطبيق والمتغيرات.</span><span class="sxs-lookup"><span data-stu-id="e8c52-152">Select **Edit** to configure the actions, applicability rules, and variables.</span></span>

    ![تحرير إعداد ميزة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="e8c52-154">في الصفحة **إعداد إصدار الميزة**، حدد علامة التبويب **الإجراءات** لإدارة قائمة الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="e8c52-154">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="e8c52-155">تحدد الإجراءات قائمة بالعمليات التي يجب تشغيلها بترتيب تسلسلي لاستكمال التنفيذ الكامل للحدث.</span><span class="sxs-lookup"><span data-stu-id="e8c52-155">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![علامة تبويب الإجراءات‏‎](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | <span data-ttu-id="e8c52-157">معرف الإجراء</span><span class="sxs-lookup"><span data-stu-id="e8c52-157">Action ID</span></span> | <span data-ttu-id="e8c52-158">الإجراء</span><span class="sxs-lookup"><span data-stu-id="e8c52-158">Action</span></span>                   | <span data-ttu-id="e8c52-159">اسم الإجراء</span><span class="sxs-lookup"><span data-stu-id="e8c52-159">Action name</span></span>                                  | <span data-ttu-id="e8c52-160">وصف الإجراء</span><span class="sxs-lookup"><span data-stu-id="e8c52-160">Action description</span></span>                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="e8c52-161">1</span><span class="sxs-lookup"><span data-stu-id="e8c52-161">1</span></span>         | <span data-ttu-id="e8c52-162">تحويل المستند</span><span class="sxs-lookup"><span data-stu-id="e8c52-162">Transform document</span></span>       | <span data-ttu-id="e8c52-163">إنشاء الفاتورة الإلكترونية CFDI بدون التوقيع الرقمي</span><span class="sxs-lookup"><span data-stu-id="e8c52-163">Generate CFDI E-Invoice without digital sign</span></span> | <span data-ttu-id="e8c52-164">إنشاء الفاتورة الإلكترونية CFDI.</span><span class="sxs-lookup"><span data-stu-id="e8c52-164">Generate the CFDI e-invoice.</span></span>                                |
    | <span data-ttu-id="e8c52-165">2</span><span class="sxs-lookup"><span data-stu-id="e8c52-165">2</span></span>         | <span data-ttu-id="e8c52-166">توقيع مستند</span><span class="sxs-lookup"><span data-stu-id="e8c52-166">Sign document</span></span>            | <span data-ttu-id="e8c52-167">التوقيع الرقمي</span><span class="sxs-lookup"><span data-stu-id="e8c52-167">Digital sign</span></span>                                 | <span data-ttu-id="e8c52-168">التوقيع الرقمي على الفاتورة الإلكترونية لإرسالها.</span><span class="sxs-lookup"><span data-stu-id="e8c52-168">Digitally sign the e-invoice for submission.</span></span>                |
    | <span data-ttu-id="e8c52-169">3</span><span class="sxs-lookup"><span data-stu-id="e8c52-169">3</span></span>         | <span data-ttu-id="e8c52-170">استدعاء خدمة PAC المكسيكية</span><span class="sxs-lookup"><span data-stu-id="e8c52-170">Call Mexican PAC service</span></span> | <span data-ttu-id="e8c52-171">إرسال الفاتورة الإلكترونية CFDI</span><span class="sxs-lookup"><span data-stu-id="e8c52-171">Submit CFDI E-Invoice</span></span>                        | <span data-ttu-id="e8c52-172">يقوم عميل Windows Communication Foundation ‏(WCF) بإرسال الفاتورة الإلكترونية CFDI.</span><span class="sxs-lookup"><span data-stu-id="e8c52-172">The Windows Communication Foundation (WCF) client submits the CFDI e-invoice.</span></span> |
    | <span data-ttu-id="e8c52-173">4</span><span class="sxs-lookup"><span data-stu-id="e8c52-173">4</span></span>         | <span data-ttu-id="e8c52-174">استجابة العملية</span><span class="sxs-lookup"><span data-stu-id="e8c52-174">Process response</span></span>         | <span data-ttu-id="e8c52-175">تحليل استجابة خدمة الويب</span><span class="sxs-lookup"><span data-stu-id="e8c52-175">Analyze web service response</span></span>                 | <span data-ttu-id="e8c52-176">تحليل استجابة خدمة الويب، وإرجاع سجل الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="e8c52-176">Analyze the web service response, and return the error log.</span></span> |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a><span data-ttu-id="e8c52-177">إعداد عنوان URL لخدمات الويب المكسيكية PAC</span><span class="sxs-lookup"><span data-stu-id="e8c52-177">Set up the URL for Mexican PAC web services</span></span> 

1. <span data-ttu-id="e8c52-178">في الصفحة **إعداد إصدار الميزة**، على علامة التبويب **الإجراءات**، على علامة التبويب السريعة **الإجراءات‏‎**، حدد **استدعاء خدمة PAC المكسيكية**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-178">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Mexican PAC service**.</span></span>
2. <span data-ttu-id="e8c52-179">على علامة التبويب السريعة **المعلمات**، في حقل **عنوان URL**، أدخل عنوان URL لخدمة الويب لإرسال فواتير CFDI.</span><span class="sxs-lookup"><span data-stu-id="e8c52-179">On the **Parameters** FastTab, in the **URL address** field, enter the URL of the web service for CFDI invoice submission.</span></span>

> [!NOTE]
> <span data-ttu-id="e8c52-180">استخدم نفس الخطوات لتحديث عنوان URL الخاص بالإجراء **استدعاء خدمة PAC المكسيكية**‬ لعمليات إعداد ميزات **الإلغاء** و **طلب الإلغاء**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-180">Use the same steps to update the URL for **Call Mexican PAC service** action for the **Cancel** and **Cancelation request** feature setups.</span></span>

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a><span data-ttu-id="e8c52-181">تعيين إصدار المسودة إلى بيئة الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e8c52-181">Assign the Draft version to an e-Invoicing environment</span></span>

1. <span data-ttu-id="e8c52-182">في صفحة **ميزات الفوترة الإلكترونية**، على علامة التبويب **البيئات**، حدد **تمكين**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-182">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="e8c52-183">في حقل **البيئة**، حدد البيئة.</span><span class="sxs-lookup"><span data-stu-id="e8c52-183">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="e8c52-184">في الحقل **ساري من‬‏‫**، حدد التاريخ الذي يجب أن تصبح فيه البيئة سارية المفعول.</span><span class="sxs-lookup"><span data-stu-id="e8c52-184">In the **Effective from** field, select the date when the environment should become effective.</span></span>
3. <span data-ttu-id="e8c52-185">حدد **تمكين**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-185">Select **Enable**.</span></span>

![تمكين بيئة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a><span data-ttu-id="e8c52-187">تغيير حالة الإصدار إلى "مكتمل"</span><span class="sxs-lookup"><span data-stu-id="e8c52-187">Change the version status to Completed</span></span>

1. <span data-ttu-id="e8c52-188">في الصفحة **ميزات الفوترة الإلكترونية**، على علامة تبويب **الإصدارات**، حدد إصدار ميزة الفوترة الإلكترونية بالحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-188">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="e8c52-189">حدد **حالة التغيير \> مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-189">Select **Change status \> Complete**.</span></span>

## <a name="change-the-version-status-to-published"></a><span data-ttu-id="e8c52-190">تغيير حالة الإصدار إلى "منشور"</span><span class="sxs-lookup"><span data-stu-id="e8c52-190">Change the version status to Published</span></span>

- <span data-ttu-id="e8c52-191">في صفحة **ميزات الفوترة الإلكترونية**، على علامة التبويب **الإصدارات**، حدد **تغيير الحالة \> نشر**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-191">On the **e-Invoicing Features** page, on the **Versions** tab, select **Change status \> Publish**.</span></span>

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="e8c52-192">نشر ميزة الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e8c52-192">Publish the e-Invoicing feature</span></span>

1. <span data-ttu-id="e8c52-193">في الصفحة **ميزات الفوترة الإلكترونية**، حدد علامة التبويب **الإصدارات** لإدارة حالة ميزة **فواتير CFDI‏ (MX)**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-193">On the **e-Invoicing Features** page, select the **Versions** tab to manage the status of the **CFDI invoices (MX)** feature.</span></span>
2. <span data-ttu-id="e8c52-194">حدد **تغيير الحالة** لتغيير حالة الميزة.</span><span class="sxs-lookup"><span data-stu-id="e8c52-194">Select **Change status** to change the status of the feature.</span></span>

![تغيير حالة ميزة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="e8c52-196">إعداد تكامل الوظيفة الإضافية الفوترة الإلكترونية في Finance</span><span class="sxs-lookup"><span data-stu-id="e8c52-196">Set up Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="e8c52-197">لإعداد تكامل الوظيفة الإضافية الفوترة الإلكترونية في Finance، ستقوم بإكمال هذه المهام:</span><span class="sxs-lookup"><span data-stu-id="e8c52-197">To set up the Electronic invoicing add-on in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="e8c52-198">استيراد نموذج بيانات التقارير الإلكترونية وتعيين نموذج بيانات التقارير الإلكترونية والتنسيقات المطلوبة لفواتير CFDI.</span><span class="sxs-lookup"><span data-stu-id="e8c52-198">Import the ER data model, the ER data model mapping, and the formats that are required for CFDI invoices.</span></span>
2. <span data-ttu-id="e8c52-199">تكوين أنواع الاستجابات لتحديث فواتير CFDI.</span><span class="sxs-lookup"><span data-stu-id="e8c52-199">Configure response types for updating the CFDI invoices.</span></span> <span data-ttu-id="e8c52-200">يتم استخدام أنواع الاستجابات هذه للاستجابة من خادم موفر الشهادات المعتمد (PAC).</span><span class="sxs-lookup"><span data-stu-id="e8c52-200">These response types are used for the response from the authorized certification provider (PAC) server.</span></span>

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a><span data-ttu-id="e8c52-201">استيراد نموذج بيانات التقارير الإلكترونية وتعيين نموذج بيانات التقارير الإلكترونية، وتكوينات السياق للفواتير الإلكترونية CFDI</span><span class="sxs-lookup"><span data-stu-id="e8c52-201">Import the ER data model, ER data model mapping, and context configurations for CFDI invoices</span></span>

1. <span data-ttu-id="e8c52-202">سجل دخولك إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="e8c52-202">Sign in to Finance.</span></span>
2. <span data-ttu-id="e8c52-203">في مساحة عمل **إعداد التقارير الإلكترونية**، في قسم **موفرو التكوين**، حدد العنوان **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-203">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span> <span data-ttu-id="e8c52-204">تأكد من تعيين موفر التكوين هذا إلى **نشط**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-204">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="e8c52-205">لمزيد من المعلومات حول كيفية تعيين موفر إلى **نشط**، راجع [إنشاء موفري التكوين ووضع علامة نشط عليهم‬](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="e8c52-205">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="e8c52-206">حدد **المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-206">Select **Repositories**.</span></span>
4. <span data-ttu-id="e8c52-207">حدد **المورد العمومي \> فتح**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-207">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="e8c52-208">استورد **نموذج الفاتورة** و **تعيين نموذج الفاتورة** و **تنسيق فواتير CFDI‏ (MX)** و **تنسيق طلب إلغاء فواتير CFDI‏ (MX)** و **تنسيق إلغاء فواتير CFDI ‏(MX)**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-208">Import **Invoice model**, **Invoice model mapping**, **CFDI invoice format (MX)**, **CFDI invoice cancelation request format (MX)**, and **CFDI invoice cancel format (MX)**.</span></span>

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a><span data-ttu-id="e8c52-209">تشغيل الميزة لمعالجة فواتير CFDI</span><span class="sxs-lookup"><span data-stu-id="e8c52-209">Turn on the feature for processing CFDI invoices</span></span>

1. <span data-ttu-id="e8c52-210">انتقل إلى **إدارة المؤسسة \> الإعداد \> معلمات المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="e8c52-211">على علامة التبويب **الميزات**، حدد خانة الاختيار **تمكين** في الصفوف لمراجع الميزات **MX-00010** و **MX-00016**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-211">On the **Features** tab, select the **Enable** check box in the rows for feature references **MX-00010** and **MX-00016**.</span></span>

![تشغيل الميزات لمعالجة فواتير CFDI](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a><span data-ttu-id="e8c52-213">استيراد تكوينات التقارير الإلكترونية وإعداد أنواع الاستجابات لتحديث فواتير MX-00016</span><span class="sxs-lookup"><span data-stu-id="e8c52-213">Import ER configurations and set up the response types for updating CFDI invoices</span></span>

#### <a name="import-er-configurations"></a><span data-ttu-id="e8c52-214">استيراد تكوينات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e8c52-214">Import ER configurations</span></span>

1. <span data-ttu-id="e8c52-215">في مساحة عمل **إعداد التقارير الإلكترونية**، في قسم **موفرو التكوين**، حدد العنوان **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-215">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span>
3. <span data-ttu-id="e8c52-216">حدد **المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-216">Select **Repositories**.</span></span>
4. <span data-ttu-id="e8c52-217">حدد **المورد العمومي \> فتح**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-217">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="e8c52-218">استورد **نموذج رسالة الاستجابة** و **استيراد سجل أخطاء CFDI‏ (MX)** و **استيراد رسائل استجابة CFDI‏ (MX)**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-218">Import **Response message model**, **CFDI error log import (MX)**, and **CFDI response message import (MX)**.</span></span>

#### <a name="set-up-the-response-types"></a><span data-ttu-id="e8c52-219">إعداد أنواع الاستجابات</span><span class="sxs-lookup"><span data-stu-id="e8c52-219">Set up the response types</span></span>

1. <span data-ttu-id="e8c52-220">انتقل إلى **إدارة المؤسسة \> الإعداد \> معلمات المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-220">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="e8c52-221">على علامة التبويب **المستند الإلكتروني**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-221">On the **Electronic document** tab, select **Add**.</span></span>
3. <span data-ttu-id="e8c52-222">أدخل دفتر يومية فواتير العميل، ثم في الحقل **اسم الجدول**، حدد فاتورة المشروع.</span><span class="sxs-lookup"><span data-stu-id="e8c52-222">Enter the customer invoice journal, and then, in the **Table name** field, select the project invoice.</span></span>
4. <span data-ttu-id="e8c52-223">لكل جدول، حدد سياق مستند ذي صلة:</span><span class="sxs-lookup"><span data-stu-id="e8c52-223">For each table, define a related document context:</span></span>

    - <span data-ttu-id="e8c52-224">بالنسبة إلى **دفتر يومية فاتورة العميل**، أدخل **سياق فاتورة العميل**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-224">For **Customer invoice journal**, enter **Customer invoice context**.</span></span>
    - <span data-ttu-id="e8c52-225">بالنسبة إلى **فاتورة المشروع**، أدخل **سياق فاتورة المشروع**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-225">For **Project invoice**, enter **Project invoice context**.</span></span>

4. <span data-ttu-id="e8c52-226">حدد **أنواع الاستجابات** لتكوين أنواع الاستجابات التي يمكن إرجاعها من الوظيفة الإضافية الفوترة الإلكترونية وتضمينها في دفتر يومية فواتير العميل أو فاتورة المشروع.</span><span class="sxs-lookup"><span data-stu-id="e8c52-226">Select **Response types** to configure the response types that can be returned from the Electronic invoicing add-on and included in a customer invoice journal or project invoice.</span></span>
5. <span data-ttu-id="e8c52-227">حدد **جديد**، ثم في حقل **نوع الاستجابة**، حدد **استجابة‎**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-227">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
6. <span data-ttu-id="e8c52-228">في الحقل **حالة الإرسال**، حدد **معلّق**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-228">In the **Submission status** field, select **Pending**.</span></span>
7. <span data-ttu-id="e8c52-229">في الحقل **تعيين النموذج**، حدد **تنسيق استيراد رسالة الاستجابة – تعيين النموذج من رسالة الاستجابة**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-229">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
8. <span data-ttu-id="e8c52-230">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-230">Select **Save**.</span></span>
9. <span data-ttu-id="e8c52-231">حدد **جديد**، ثم في حقل **نوع الاستجابة**، حدد **ResponseData‎**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-231">Select **New**, and then, in the **Response type** field, select **ResponseData**.</span></span>
10. <span data-ttu-id="e8c52-232">في الحقل **حالة الإرسال**، حدد **معلّق**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-232">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="e8c52-233">في الحقل **تعيين النموذج**، حدد **تنسيق استيراد بيانات الاستجابة CFDI (التفاصيل) - استيراد بيانات الاستجابة**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-233">In the **Model mapping** field, select **CFDI response data import format (details) – Response data import**.</span></span>
12. <span data-ttu-id="e8c52-234">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-234">Select **Save**.</span></span>

## <a name="process-electronic-invoices-in-finance"></a><span data-ttu-id="e8c52-235">معالجه الفواتير الإلكترونية في Finance</span><span class="sxs-lookup"><span data-stu-id="e8c52-235">Process electronic invoices in Finance</span></span> 

<span data-ttu-id="e8c52-236">اثناء معالجة فواتير CFDI في Finance من خلال الوظيفة الإضافية الفوترة الإلكترونية، يمكنك تنفيذ المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="e8c52-236">During the processing of CFDI invoices in Finance through the Electronic invoicing add-on, you can perform the following tasks:</span></span>

- <span data-ttu-id="e8c52-237">إرسال فواتير CFDI.</span><span class="sxs-lookup"><span data-stu-id="e8c52-237">Submit CFDI invoices.</span></span>
- <span data-ttu-id="e8c52-238">عرض سجلات تنفيذ الإرسال.</span><span class="sxs-lookup"><span data-stu-id="e8c52-238">View the submission execution logs.</span></span>
- <span data-ttu-id="e8c52-239">إرسال إلغاء فاتورة CFDI.</span><span class="sxs-lookup"><span data-stu-id="e8c52-239">Submit the cancellation of a CFDI invoice.</span></span>

### <a name="submit-cfdi-invoices"></a><span data-ttu-id="e8c52-240">إرسال فواتير CFDI</span><span class="sxs-lookup"><span data-stu-id="e8c52-240">Submit CFDI invoices</span></span>

<span data-ttu-id="e8c52-241">بعد تشغيل الميزة **تكامل الوظيفة الإضافية الفوترة الإلكترونية القابلة للتكوين**، لن يعود استخدام العملية **تصدير/استيراد الفاتورة الإلكترونية** (**الحسابات المدينة \> الفواتير \> الفواتير الإلكترونية**) لإرسال فواتير CFDI ممكنًا.</span><span class="sxs-lookup"><span data-stu-id="e8c52-241">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the **Export/Import electronic invoice** process (**Accounts receivable \> Invoices \> E-invoices**) for submitting CFDI invoices can no longer be used.</span></span> <span data-ttu-id="e8c52-242">لقد تم استبدال هذه العملية بأخرى جديدة تسمى **إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-242">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="e8c52-243">قبل استخدام العملية الجديدة **إرسال المستندات الإلكترونية**، تحقق من اكتمال الإعداد المطلوب للفواتير الإلكترونية المكسيكية.</span><span class="sxs-lookup"><span data-stu-id="e8c52-243">Before you use the new **Submit electronic documents** process, verify that the setup that is required for Mexican e-invoices was completed.</span></span> <span data-ttu-id="e8c52-244">لمزيد من المعلومات، راجع [الإصدار 3.3 من تخطيط CFDI](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span><span class="sxs-lookup"><span data-stu-id="e8c52-244">For more information, see [CFDI layout version 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span></span>

1. <span data-ttu-id="e8c52-245">انتقل إلى **إدارة المؤسسة \> دوري \> المستندات الإلكترونية \> إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-245">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="e8c52-246">بالنسبة لعملية الإرسال الأولى لأي مستند، عيّن دائمًا الخيار **إعادة إرسال المستندات** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-246">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="e8c52-247">إذا كان من الضروري إعادة إرسال مستند من خلال الخدمة، فقم بتعيين هذا الخيار إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-247">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="e8c52-248">على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**، حدد **تصفية** لفتح مربع الحوار **استعلام** حيث يمكنك إنشاء استعلام لتحديد مستندات لإرسالها.</span><span class="sxs-lookup"><span data-stu-id="e8c52-248">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![إرسال مستند CFDI](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> <span data-ttu-id="e8c52-250">أثناء محاولتك الأولى لإرسال مستند من خلال الخدمة، ستتم مطالبتك بتأكيد الاتصال بالوظيفة الإضافية الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e8c52-250">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="e8c52-251">حدد **انقر هنا للاتصال بخدمة إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-251">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-submission-logs"></a><span data-ttu-id="e8c52-252">عرض سجلات الإرسال</span><span class="sxs-lookup"><span data-stu-id="e8c52-252">View submission logs</span></span>

<span data-ttu-id="e8c52-253">يمكنك عرض سجلات الإرسال لكافة المستندات المرسلة أو لمستند مرسل واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="e8c52-253">You can view the submission logs for all submitted documents or for just one submitted document.</span></span>

#### <a name="view-all-submission-logs"></a><span data-ttu-id="e8c52-254">عرض جميع سجلات الإرسال</span><span class="sxs-lookup"><span data-stu-id="e8c52-254">View all submission logs</span></span>

<span data-ttu-id="e8c52-255">بعد تشغيل الميزة **تكامل الوظيفة الإضافية الفوترة الإلكترونية القابلة للتكوين‬‏‫**، تتوفر صفحة جديدة تتيح لك متابعة عملية إرسال المستند.</span><span class="sxs-lookup"><span data-stu-id="e8c52-255">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="e8c52-256">يمكنك استخدام هذه الصفحة عرض سجلات الإرسال لكافة المستندات المرسلة.</span><span class="sxs-lookup"><span data-stu-id="e8c52-256">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="e8c52-257">انتقل إلى **إدارة المؤسسة \> دوري \> المستندات الإلكترونية \> سجل إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-257">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="e8c52-258">في الحقل **نوع المستند**، حدد **دفتر يومية فواتير العميل** لتصفية المستندات الإلكترونية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="e8c52-258">In the **Document type** field, select **Customer invoice journal** to filter for the required electronic documents.</span></span>

    ![تحديد نوع المستند لعرض سجلات الإرسال](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. <span data-ttu-id="e8c52-260">في جزء الإجراءات، حدد **الاستعلامات \> تفاصيل الإرسال** لعرض سجلات تنفيذ الإرسال.</span><span class="sxs-lookup"><span data-stu-id="e8c52-260">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![عرض تفاصيل سجل الإرسال](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

<span data-ttu-id="e8c52-262">تنقسم المعلومات الموجودة في سجلات الإرسال بين ثلاث علامات تبويب سريعة:</span><span class="sxs-lookup"><span data-stu-id="e8c52-262">The information in the submission logs is divided among three FastTabs:</span></span>

- <span data-ttu-id="e8c52-263">**إجراءات المعالجة** – تُظهر علامة التبويب السريعة هذه سجل التنفيذ للإجراءات التي تم تكوينها في إصدار الميزة الذي تم إعداده في RCS.</span><span class="sxs-lookup"><span data-stu-id="e8c52-263">**Processing actions** – This FastTab shows the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="e8c52-264">يعرض عمود **الحالة** ما إذا كان قد تم تشغيل الإجراء بنجاح ام لا.</span><span class="sxs-lookup"><span data-stu-id="e8c52-264">The **Status** column shows whether the action was successfully run.</span></span>
- <span data-ttu-id="e8c52-265">**ملفات الإجراءات**، تُظهر علامة التبويب السريعة هذه الملفات الوسيطة التي تم إنشاؤها أثناء تنفيذ الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="e8c52-265">**Action files** – This FastTab shows the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="e8c52-266">يمكنك تحديد **عرض** لتنزيل الملف وعرضه.</span><span class="sxs-lookup"><span data-stu-id="e8c52-266">You can select **View** to download and view the file.</span></span>
- <span data-ttu-id="e8c52-267">**سجل إجراء المعالجة** – تُظهر علامة التبويب السريعة هذه نتائج الاتصال بين الوظيفة الإضافية الفوترة الإلكترونية وخدمة الويب المستهدفة.</span><span class="sxs-lookup"><span data-stu-id="e8c52-267">**Processing action log** – This FastTab shows the results of the communication between the Electronic invoicing add-on and the target web service.</span></span> <span data-ttu-id="e8c52-268">وتُظهر أيضًا ما تم إرجاعه بواسطة المعالجة من خدمة الويب.</span><span class="sxs-lookup"><span data-stu-id="e8c52-268">It also shows what was returned by the processing from the web service.</span></span> <span data-ttu-id="e8c52-269">يُظهر عمود **رمز الخطأ** رمز الإرجاع المرتجع بواسطة خدمة الويب للتخويل.</span><span class="sxs-lookup"><span data-stu-id="e8c52-269">The **Error code** column shows the return code that was returned by the authorization web service.</span></span>

<span data-ttu-id="e8c52-270">عند تخويل فاتورة CFDI المرسلة، يتم تحديث حالتها إلى **موافق عليها**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-270">When the submitted CFDI invoice is authorized, its status is updated to **Approved**.</span></span>

#### <a name="view-submission-logs-from-cfdi-invoices"></a><span data-ttu-id="e8c52-271">عرض سجلات الإرسال من فواتير CFDI</span><span class="sxs-lookup"><span data-stu-id="e8c52-271">View submission logs from CFDI invoices</span></span>

<span data-ttu-id="e8c52-272">بعد تشغيل ميزة **الوظيفة الإضافية الفوترة الإلكترونية القابلة للتكوين‬‏‫**، يمكنك أيضًا عرض سجلات الإرسال من فواتير CFDI.</span><span class="sxs-lookup"><span data-stu-id="e8c52-272">After you turn on the **ConfigurableElectronic invoicing add-on integration** feature, you can also view the submission logs from CFDI invoices.</span></span>

1. <span data-ttu-id="e8c52-273">انتقل إلى **الحسابات المدينة \> الاستعلامات والتقارير \> CFDI (الفواتير الإلكترونية)**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-273">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="e8c52-274">حدد فاتورة CFDI تم إرسالها بعد تشغيل الميزة **تكامل الوظيفة الإضافية الفوترة الإلكترونية القابلة للتكوين‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-274">Select a CFDI invoice that was submitted after the **Configurable Electronic invoicing add-on integration** feature was turned on.</span></span>
3. <span data-ttu-id="e8c52-275">في جزء الإجراءات، على علامة تبويب **المحفوظات**، حدد **سجل المستندات الإلكترونية‬**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-275">On the Action Pane, on the **History** tab, select **Electronic document log**.</span></span>

![عرض سجلات الإرسال من فواتير CFDI](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> <span data-ttu-id="e8c52-277">بالنسبة إلى فواتير CFDI المرسلة قبل تشغيل الميزة **تكامل الوظيفة الإضافية الفوترة الإلكترونية القابلة للتكوين‬‏‫**، يتوفر زر **المحفوظات**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-277">For CFDI invoices that were submitted before the **Configurable Electronic invoicing add-on integration** feature was turned on, the **History** button is available.</span></span> <span data-ttu-id="e8c52-278">لا يتوفر زر **المحفوظات** لفواتير CFDI المرسلة بعد تشغيل الميزة **تكامل الوظيفة الإضافية الفوترة الإلكترونية القابلة للتكوين**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-278">The **History** button isn't available for CFDI invoices that were submitted after the **Configurable Electronic invoicing add-on integration** feature was turned on.</span></span>

### <a name="submit-cancellation-of-cfdi-invoices"></a><span data-ttu-id="e8c52-279">إرسال إلغاء فواتير CFDI</span><span class="sxs-lookup"><span data-stu-id="e8c52-279">Submit cancellation of CFDI invoices</span></span>

<span data-ttu-id="e8c52-280">بعد تشغيل الميزة **تكامل الوظيفة الإضافية الفوترة الإلكترونية القابلة للتكوين**، لن يعود استخدام العملية القديمة لإلغاء فواتير CFDI ممكنًا.</span><span class="sxs-lookup"><span data-stu-id="e8c52-280">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling CFDI invoices can no longer be used.</span></span> <span data-ttu-id="e8c52-281">سيتم استبدال العملية بعملية إلغاء جديدة مضمنة في صفحة **سجل إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-281">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

1. <span data-ttu-id="e8c52-282">انتقل إلى **الحسابات المدينة \> الاستعلامات والتقارير \> CFDI (الفواتير الإلكترونية)**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-282">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="e8c52-283">إذا كانت حالة فاتورة CFDI هي **موافق عليها**، فحدد **الوظائف \> إلغاء CFDI**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-283">If the CFDI invoice has a status of **Approved**, select **Functions \> Cancel CFDI**.</span></span>
3. <span data-ttu-id="e8c52-284">انتقل إلى **إدارة المؤسسة \> دوري \> المستندات الإلكترونية \> سجل إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-284">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
4. <span data-ttu-id="e8c52-285">حدد فاتورة CFDI، ثم حدد **الوظائف \> إرسال عمليات الإرسال ذات الصلة**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-285">Select the CFDI invoice, and then select **Functions \> Send related submissions**.</span></span>
5. <span data-ttu-id="e8c52-286">ادخل وصفًا لعملية الإرسال ذات الصلة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-286">Enter a description for the related submission, and then select **OK**.</span></span>

#### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="e8c52-287">عرض سجلات إرسال الإلغاء</span><span class="sxs-lookup"><span data-stu-id="e8c52-287">View cancellation submission logs</span></span>

1. <span data-ttu-id="e8c52-288">انتقل إلى **إدارة المؤسسة \> دوري \> المستندات الإلكترونية \> سجل إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="e8c52-289">في الحقل **نوع المستند**، حدد **دفتر يومية فواتير العميل** لإجراء التصفية فقط لمستندات دفتر يومية فواتير العميل.</span><span class="sxs-lookup"><span data-stu-id="e8c52-289">In the **Document type** field, select **Customer invoice journal** to filter for customer invoice journal documents only.</span></span>
3. <span data-ttu-id="e8c52-290">حدد فاتورة CFDI، ثم في جزء الإجراءات، حدد **الاستعلامات \> الإرسال ذو الصلة**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-290">Select the CFDI invoice, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="e8c52-291">تعرض صفحة **عمليات الإرسال ذات الصلة** جميع عمليات الإرسال ذات الصلة وحالة الإرسال لفاتورة CFDI معينة.</span><span class="sxs-lookup"><span data-stu-id="e8c52-291">The **Related submissions** page shows all related submissions, and their submission status, for a given CFDI invoice.</span></span> <span data-ttu-id="e8c52-292">في الرسم التوضيحي التالي، يمثل السطر الأول الإرسال الذي طالب بالموافقة على فاتورة CFDI.</span><span class="sxs-lookup"><span data-stu-id="e8c52-292">In the following illustration, the first line represents the submission that requested approval of the CFDI invoice.</span></span> <span data-ttu-id="e8c52-293">ويمثل السطر الثاني الإرسال الذي قام بإلغاء فاتورة CFDI هذه.</span><span class="sxs-lookup"><span data-stu-id="e8c52-293">The second line represents the submission that canceled that CFDI invoice.</span></span>

    ![عرض سجلات إرسال الإلغاء](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. <span data-ttu-id="e8c52-295">في جزء الإجراءات، حدد **الاستعلامات \> تفاصيل الإرسال** لعرض سجلات تنفيذ الإرسال.</span><span class="sxs-lookup"><span data-stu-id="e8c52-295">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![عرض تفاصيل سجلات إرسال الإلغاء](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="e8c52-297">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="e8c52-297">Privacy notice</span></span>
<span data-ttu-id="e8c52-298">قد يتطلب تمكين ميزات MX-00010 وMX-00016 (فاتورة CFDI وإلغاء CFDI) إرسال بيانات محدودة تتضمن معرف التسجيل الضريبي الخاص بالمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="e8c52-298">Enabling the MX-00010 and MX-00016 (CFDI Invoice and CFDI Cancellation) features may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="e8c52-299">سيتم إرسال هذه البيانات إلى وكالات خارجية معتمدة من قبل هيئة الضرائب لأغراض إرسال الفواتير الإلكترونية إلى هيئة الضرائب هذه بالتنسيق المعرف مسبقًا والمطلوب لإجراء التكامل مع خدمة الويب الخاصة بالحكومة.</span><span class="sxs-lookup"><span data-stu-id="e8c52-299">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="e8c52-300">بإمكان المسؤول تمكين وتعطيل ميزات MX-00010 وMX-00016 (فاتورة CFDI وإلغاء CFDI) من خلال الانتقال إلى **إدارة المؤسسة \> الإعداد \> معلمات المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="e8c52-300">An administrator can enable and disable the MX-00010 and MX-00016 (CFDI Invoice and CFDI Cancellation) features by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="e8c52-301">حدد علامة التبويب **الميزات**، وحدد الصفوف التي تحتوي على ميزات MX-00010 وMX-00016، ثم قم بإجراء التحديد المناسب.</span><span class="sxs-lookup"><span data-stu-id="e8c52-301">Select the **Features** tab, select the rows containing the MX-00010 and MX-00016 features, and then make the appropriate selection.</span></span> <span data-ttu-id="e8c52-302">تخضع البيانات المستوردة من هذه الأنظمة الخارجية في خدمة Dynamics 365 عبر الإنترنت [لبيان الخصوصية](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="e8c52-302">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="e8c52-303">الرجاء مراجعه أقسام إشعار الخصوصية في وثائق الميزات الخاصة بالبلد لمزيد من المعلومات.</span><span class="sxs-lookup"><span data-stu-id="e8c52-303">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8c52-304">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e8c52-304">Additional resources</span></span>

- [<span data-ttu-id="e8c52-305">نظرة عامة على الوظيفة الإضافية الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e8c52-305">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="e8c52-306">بدء استخدام الوظيفة الإضافية "الفوترة الإلكترونية"</span><span class="sxs-lookup"><span data-stu-id="e8c52-306">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="e8c52-307">إعداد الوظيفة الإضافية الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e8c52-307">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
