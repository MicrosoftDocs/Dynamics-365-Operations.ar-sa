---
title: بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في البرازيل
description: يوفر هذا الموضوع معلومات تساعدك على بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في البرازيل في Microsoft Dynamics 365 Finance وفي Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
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
ms.openlocfilehash: fb3ec2d60875d7a0747d64b397aafaa0a3d26348
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039859"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a><span data-ttu-id="ffb6f-103">بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في البرازيل</span><span class="sxs-lookup"><span data-stu-id="ffb6f-103">Get started with the Electronic invoicing add-on for Brazil</span></span> 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="ffb6f-104">قد لا تدعم الوظيفة الإضافية الفوترة الإلكترونية في البرازيل في الوقت الحالي جميع الوظائف المتوفرة في تكامل المستند المالي المبني في Microsoft Dynamics 365 Finance أو Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-104">The Electronic invoicing add-on for Brazil doesn't currently support all the functions that are available in the fiscal document integration that is built into Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="ffb6f-105">يوفر هذا الموضوع معلومات تساعدك على بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في البرازيل.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Brazil.</span></span> <span data-ttu-id="ffb6f-106">وهو يرشدك عبر خطوات التكوين التي تعتمد على البلد في Regulatory Configuration Services (RCS) وFinance وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and in Finance and Supply Chain Management.</span></span> <span data-ttu-id="ffb6f-107">كما يرشدك من خلال عملية إرسال مستند مالي NF-e (نموذج المستند المالي الإلكتروني 55) من خلال الخدمة، ويوضح كيفية مراجعة نتائج معالجة وحالة المستندات المالية.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-107">It also guides you through the process of submitting an NF-e fiscal document (Electronic fiscal document model 55) through the service, and it explains how review the processing results and the status of the fiscal documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ffb6f-108">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-108">Prerequisites</span></span>

<span data-ttu-id="ffb6f-109">قبل إكمال الخطوات الواردة في هذا الموضوع، يجب إكمال الخطوات في [بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="ffb6f-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="ffb6f-110">إعداد RCS</span><span class="sxs-lookup"><span data-stu-id="ffb6f-110">RCS setup</span></span>

<span data-ttu-id="ffb6f-111">اثناء إعداد RCS، ستقوم بإكمال المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb6f-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="ffb6f-112">استيراد ميزة الفوترة الإلكترونية للمستندات المالية NF-e.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-112">Import the e-Invoicing feature for NF-e fiscal documents.</span></span>
2. <span data-ttu-id="ffb6f-113">مراجعة تنسيقات الملفات المطلوبة لإرسال المستندات المالية NF-e للتخويل.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-113">Review the file formats that are required to submit NF-e fiscal documents for authorization.</span></span>
3. <span data-ttu-id="ffb6f-114">مراجعة تنسيقات الملفات المطلوبة لطلب إلغاء NF-e موافق عليه.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-114">Review the file formats that are required to request the cancellation of an approved NF-e.</span></span>
4. <span data-ttu-id="ffb6f-115">تكوين الحدث المطلوب لإرسال المستندات المالية NF-e للتخويل.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-115">Configure the event that is required to submit NF-e fiscal documents for authorization.</span></span>
5. <span data-ttu-id="ffb6f-116">تكوين الحدث المطلوب لطلب إلغاء NF-e موافق عليه.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-116">Configure the event that is required to request the cancellation of an approved NF-e.</span></span>
6. <span data-ttu-id="ffb6f-117">تعيين ميزة الفوترة الإلكترونية إلى بيئة الوظيفة الإضافية الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-117">Assign the e-Invoicing feature to an Electronic invoicing add-on environment.</span></span>
7. <span data-ttu-id="ffb6f-118">نشر ميزة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-118">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="ffb6f-119">"ميزة الفوترة الإلكترونية" هي الاسم العام للمورد الذي تم تكوينه ونشره لاستهلاك خادم الوظيفة الإضافية الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-119">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="ffb6f-120">يجمع إعداد ميزة الفوترة الإلكترونية، من ضمن أشياء أخرى، استخدام تنسيقات تكوين التقارير الإلكترونية لإنشاء ملفات تصدير واستيراد قابلة للتكوين، واستخدام إجراءات وسير مهام إجراءات لتمكين إنشاء قواعد قابلة للتكوين لإرسال الطلبات واستيراد الاستجابات وتحليل محتويات الاستجابات.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-120">The setup of the e-Invoicing feature combines, among other things, the use of Electronic reporting (ER) configuration formats to create configurable export and import files, and the use of actions and actions flows to enable the creation of configurable rules to send requests, import responses, and parse the response contents.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="ffb6f-121">استيراد ميزة الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-121">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="ffb6f-122">سجل دخولك إلى حساب RCS.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-122">Sign in to your RCS account</span></span>
2. <span data-ttu-id="ffb6f-123">في مساحة العمل **ميزات العولمة** ، في قسم **الميزات** ، حدد الإطار المتجانب **الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-123">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="ffb6f-124">في الصفحة **ميزات الفوترة الإلكترونية** ، حدد **استيراد** لاستيراد ميزة الفوترة الإلكترونية‏‎ لمستند مالي NF-e من المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-124">On the **e-Invoicing Features** page, select **Import** to import a NF-e fiscal document e-Invoicing feature from the Global repository.</span></span>

    ![الزر "استيراد"](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. <span data-ttu-id="ffb6f-126">حدد ميزة المستندات المالية NF-e، ثم حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-126">Select the NF-e fiscal document feature, and then select **Import**.</span></span>

    ![استيراد ميزة NF-e](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a><span data-ttu-id="ffb6f-128">إنشاء إصدار جديد من ميزة المستندات المالية NF-e</span><span class="sxs-lookup"><span data-stu-id="ffb6f-128">Create a new version of the NF-e fiscal document feature</span></span>

- <span data-ttu-id="ffb6f-129">في صفحة **ميزات الفوترة الإلكترونية** ، على علامة التبويب **الإصدارات** ، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-129">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![إضافة إصدار جديد لميزة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="ffb6f-131">تحديث إصدار التكوين</span><span class="sxs-lookup"><span data-stu-id="ffb6f-131">Update the configuration version</span></span>

1. <span data-ttu-id="ffb6f-132">في الصفحة **ميزات الفوترة الإلكترونية** ، على علامة تبويب **التكوينات** ، حدد **إضافة** أو **حذف** لإدارة إصدارات التكوين (تكوينات تنسيق ملفات التقارير الإلكترونية).</span><span class="sxs-lookup"><span data-stu-id="ffb6f-132">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![إدارة تكوينات ميزة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - <span data-ttu-id="ffb6f-134">عند إنشاء إصدار جديد من ميزة المستندات المالية NF-e، يتم توارث كافة إصدارات التكوين (تنسيقات ملفات التقارير الإلكترونية) من الإصدار الأحدث.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-134">When you create a new version of the NF-e fiscal document feature, all configuration version (ER file formats) are inherited from the latest version.</span></span>
    - <span data-ttu-id="ffb6f-135">لإرسال المستند المالي NF-e، إصدارات التكوين التالية مطلوبة:</span><span class="sxs-lookup"><span data-stu-id="ffb6f-135">To submit the NF-e fiscal document for authorization, the following configuration versions are required:</span></span>

        - <span data-ttu-id="ffb6f-136">تنسيق تصدير إرسال NF-e</span><span class="sxs-lookup"><span data-stu-id="ffb6f-136">NFe submit export format</span></span>
        - <span data-ttu-id="ffb6f-137">استيراد رسالة استجابة NF-e</span><span class="sxs-lookup"><span data-stu-id="ffb6f-137">NFe response message import</span></span>
        - <span data-ttu-id="ffb6f-138">استيراد سجل أخطاء NF-e</span><span class="sxs-lookup"><span data-stu-id="ffb6f-138">NFe error log import</span></span>

    - <span data-ttu-id="ffb6f-139">لإرسال إلغاء NF-e، يجب أن يتوفر إصدار التكوين التالي:</span><span class="sxs-lookup"><span data-stu-id="ffb6f-139">To submit the NF-e cancellation, the following configuration version is required:</span></span>

        - <span data-ttu-id="ffb6f-140">تنسيق تصدير إلغاء NF-e</span><span class="sxs-lookup"><span data-stu-id="ffb6f-140">NFe cancel export format</span></span>

2. <span data-ttu-id="ffb6f-141">في القائمة، حدد إصدار تكوين، ثم حدد **تحرير** أو **عرض** لفتح الصفحة **مصمم التنسيق** ، حيث يمكنك تحرير التكوين أو عرضه.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-141">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![فتح صفحة مصمم التنسيق](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. <span data-ttu-id="ffb6f-143">استخدم الصفحة **مصمم التنسيق** لتحرير أو عرض تكوينات ملف تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-143">Use the **Format designer** page to edit or view the ER format file configurations.</span></span> <span data-ttu-id="ffb6f-144">للحصول على مزيد من التفاصيل، راجع [إنشاء تكوينات المستندات الإلكترونية](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span><span class="sxs-lookup"><span data-stu-id="ffb6f-144">For more information, see [Create electronic document configurations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span></span>

    ![صفحة مصمم التنسيق‬](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="ffb6f-146">إدارة عمليات إعداد ميزة الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-146">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="ffb6f-147">في صفحة **ميزات الفوترة الإلكترونية** ، على علامة تبويب **عمليات الإعداد** ، حدد **إضافة** أو **حذف** لإدارة عمليات إعداد ميزة الفوترة الإلكترونية (أي أحداث NF-e).</span><span class="sxs-lookup"><span data-stu-id="ffb6f-147">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add** or **Delete** to manage the e-Invoicing feature setups (that is, NF-e events).</span></span>

![إدارة عمليات إعداد ميزة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="ffb6f-149">عند إنشاء إصدار جديد من ميزة المستندات المالية NF-e التي تشتق من ميزة فوترة إلكترونية أخرى، يتم توارث جميع عمليات إعداد الميزات (أحداث NF-e) من الإصدار الأحدث.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-149">When you create a new version of the NF-e fiscal document feature that is derived from another e-Invoicing feature, all feature setups (NF-e events) are inherited from the latest version.</span></span>

<span data-ttu-id="ffb6f-150">لإرسال المستندات المالية NF-e للتخويل، يجب إعداد الميزة **إرسال**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-150">To submit NF-e fiscal documents for authorization, the **Submit** feature setup is required.</span></span>

<span data-ttu-id="ffb6f-151">لإرسال إلغاء NF-e، يجب إعداد ميزة **الإلغاء**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-151">To submit NF-e cancellation, the **Cancellation** feature setup is required.</span></span>

#### <a name="configure-the-submit-feature-setup"></a><span data-ttu-id="ffb6f-152">تكوين إعداد ميزة الإرسال</span><span class="sxs-lookup"><span data-stu-id="ffb6f-152">Configure the Submit feature setup</span></span>

1. <span data-ttu-id="ffb6f-153">في صفحة **ميزات الفوترة الإلكترونية‬** ، على علامة تبويب **عمليات الإعداد** في العمود **إعداد الميزة** ، حدد **إرسال**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-153">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Submit**.</span></span>
2. <span data-ttu-id="ffb6f-154">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-154">Select **Edit**.</span></span>

    ![تحرير إعداد ميزة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="ffb6f-156">في الصفحة **إعداد إصدار الميزة** ، حدد علامة التبويب **الإجراءات** لإدارة قائمة الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-156">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>

    ![علامة تبويب الإجراءات‏‎](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. <span data-ttu-id="ffb6f-158">راجع الإجراءات المطلوبة لإرسال NF-e للتخويل.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-158">Review the actions that are required to submit an NF-e for authorization.</span></span>

    | <span data-ttu-id="ffb6f-159">معرف الإجراء</span><span class="sxs-lookup"><span data-stu-id="ffb6f-159">Action ID</span></span> | <span data-ttu-id="ffb6f-160">اسم الإجراء</span><span class="sxs-lookup"><span data-stu-id="ffb6f-160">Action name</span></span>                  | <span data-ttu-id="ffb6f-161">وصف الإجراء</span><span class="sxs-lookup"><span data-stu-id="ffb6f-161">Action description</span></span>                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | <span data-ttu-id="ffb6f-162">1</span><span class="sxs-lookup"><span data-stu-id="ffb6f-162">1</span></span>         | <span data-ttu-id="ffb6f-163">تحويل المستند</span><span class="sxs-lookup"><span data-stu-id="ffb6f-163">Transform document</span></span>           | <span data-ttu-id="ffb6f-164">إنشاء ملف NF-e XML للإرسال.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-164">Create the NF-e XML file for submission.</span></span>                          |
    | <span data-ttu-id="ffb6f-165">2</span><span class="sxs-lookup"><span data-stu-id="ffb6f-165">2</span></span>         | <span data-ttu-id="ffb6f-166">توقيع مستند</span><span class="sxs-lookup"><span data-stu-id="ffb6f-166">Sign document</span></span>                | <span data-ttu-id="ffb6f-167">تطبيق التوقيع الرقمي على ملف XML.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-167">Apply the digital certificate to the XML file.</span></span>                    |
    | <span data-ttu-id="ffb6f-168">3</span><span class="sxs-lookup"><span data-stu-id="ffb6f-168">3</span></span>         | <span data-ttu-id="ffb6f-169">استدعاء خدمة SEFAZ البرازيلية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-169">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="ffb6f-170">إرسال ملف XML الموقع إلى خدمات الويب للتخويل.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-170">Submit the signed XML file to the web services for authorization.</span></span> |
    | <span data-ttu-id="ffb6f-171">4</span><span class="sxs-lookup"><span data-stu-id="ffb6f-171">4</span></span>         | <span data-ttu-id="ffb6f-172">استجابة العملية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-172">Process response</span></span>             | <span data-ttu-id="ffb6f-173">الحصول على استجابة خدمة الويب.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-173">Get the web service response.</span></span>                                     |
    | <span data-ttu-id="ffb6f-174">5</span><span class="sxs-lookup"><span data-stu-id="ffb6f-174">5</span></span>         | <span data-ttu-id="ffb6f-175">تحويل المستند</span><span class="sxs-lookup"><span data-stu-id="ffb6f-175">Transform document</span></span>           | <span data-ttu-id="ffb6f-176">تحليل محتوى الملف الذي تم تلقيه كاستجابة.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-176">Parse the content of the file that is received as a response.</span></span>     |
    | <span data-ttu-id="ffb6f-177">6</span><span class="sxs-lookup"><span data-stu-id="ffb6f-177">6</span></span>         | <span data-ttu-id="ffb6f-178">تحويل المستند</span><span class="sxs-lookup"><span data-stu-id="ffb6f-178">Transform document</span></span>           | <span data-ttu-id="ffb6f-179">إنشاء ملف XML للاستعلام عن حالة الإرسال.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-179">Create the XML file to inquire about status of the submission.</span></span>    |
    | <span data-ttu-id="ffb6f-180">7</span><span class="sxs-lookup"><span data-stu-id="ffb6f-180">7</span></span>         | <span data-ttu-id="ffb6f-181">استدعاء خدمة SEFAZ البرازيلية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-181">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="ffb6f-182">إرسال ملف XML الذي يطلب حالة الإرسال.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-182">Submit the XML file that requests the submission status.</span></span>          |
    | <span data-ttu-id="ffb6f-183">8</span><span class="sxs-lookup"><span data-stu-id="ffb6f-183">8</span></span>         | <span data-ttu-id="ffb6f-184">استجابة العملية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-184">Process response</span></span>             | <span data-ttu-id="ffb6f-185">الحصول على استجابة خدمة الويب.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-185">Get the web service response.</span></span>                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="ffb6f-186">إعداد عنوان URL لخدمات الويب SEFAZ</span><span class="sxs-lookup"><span data-stu-id="ffb6f-186">Set up the URL for SEFAZ web services</span></span> 

1. <span data-ttu-id="ffb6f-187">في الصفحة **إعداد إصدار الميزة** ، على علامة التبويب **الإجراءات** ، على علامة التبويب السريعة **الإجراءات‏‎** ، حدد **استدعاء خدمة SEFAZ البرازيلية** (معرف الإجراء **3** ).</span><span class="sxs-lookup"><span data-stu-id="ffb6f-187">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3** ).</span></span>
2. <span data-ttu-id="ffb6f-188">على علامة التبويب السريعة **المعلمات** ، في حقل **معلمة عنوان URL** ، أدخل عنوان URL لخدمة الويب SEFAZ لإرسال NF-e.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-188">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>
3. <span data-ttu-id="ffb6f-189">على علامة التبويب السريعة **الإجراءات** ، حدد **استدعاء خدمة SEFAZ البرازيلية** (معرف الإجراء **7** ).</span><span class="sxs-lookup"><span data-stu-id="ffb6f-189">On the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **7** ).</span></span>
4. <span data-ttu-id="ffb6f-190">على علامة التبويب السريعة **المعلمات** ، في حقل **معلمة عنوان URL** ، أدخل عنوان URL لخدمة الويب SEFAZ لإرسال NF-e.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-190">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>

#### <a name="configure-the-cancellation-feature-setup"></a><span data-ttu-id="ffb6f-191">تكوين إعداد ميزة الإلغاء</span><span class="sxs-lookup"><span data-stu-id="ffb6f-191">Configure the Cancellation feature setup</span></span>

1. <span data-ttu-id="ffb6f-192">في صفحة **ميزات الفوترة الإلكترونية‬** ، على علامة تبويب **عمليات الإعداد** في العمود **إعداد الميزة** ، حدد **إلغاء**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-192">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Cancellation**.</span></span>
2. <span data-ttu-id="ffb6f-193">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-193">Select **Edit**.</span></span>
3. <span data-ttu-id="ffb6f-194">في الصفحة **إعداد إصدار الميزة** ، حدد علامة التبويب **الإجراءات** لإدارة قائمة الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-194">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>
4. <span data-ttu-id="ffb6f-195">راجع الإجراءات المطلوبة لطلب إلغاء NF-e موافق عليه.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-195">Review the actions that are required to request the cancellation of an approved NF-e.</span></span>

    | <span data-ttu-id="ffb6f-196">معرف الإجراء</span><span class="sxs-lookup"><span data-stu-id="ffb6f-196">Action ID</span></span> | <span data-ttu-id="ffb6f-197">اسم الإجراء</span><span class="sxs-lookup"><span data-stu-id="ffb6f-197">Action name</span></span>                  | <span data-ttu-id="ffb6f-198">وصف الإجراء</span><span class="sxs-lookup"><span data-stu-id="ffb6f-198">Action description</span></span>                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="ffb6f-199">1</span><span class="sxs-lookup"><span data-stu-id="ffb6f-199">1</span></span>         | <span data-ttu-id="ffb6f-200">تحويل المستند</span><span class="sxs-lookup"><span data-stu-id="ffb6f-200">Transform document</span></span>           | <span data-ttu-id="ffb6f-201">إنشاء ملف XML الخاص بإلغاء NF-e للإرسال.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-201">Create the NF-e cancellation XML file for submission.</span></span>            |
    | <span data-ttu-id="ffb6f-202">2</span><span class="sxs-lookup"><span data-stu-id="ffb6f-202">2</span></span>         | <span data-ttu-id="ffb6f-203">توقيع مستند</span><span class="sxs-lookup"><span data-stu-id="ffb6f-203">Sign document</span></span>                | <span data-ttu-id="ffb6f-204">تطبيق التوقيع الرقمي على ملف XML.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-204">Apply the digital certificate to the XML file.</span></span>                   |
    | <span data-ttu-id="ffb6f-205">3</span><span class="sxs-lookup"><span data-stu-id="ffb6f-205">3</span></span>         | <span data-ttu-id="ffb6f-206">استدعاء خدمة SEFAZ البرازيلية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-206">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="ffb6f-207">إرسال ملف XML الموقع إلى خدمات الويب للإلغاء.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-207">Submit the signed XML file to the web services for cancellation.</span></span> |
    | <span data-ttu-id="ffb6f-208">4</span><span class="sxs-lookup"><span data-stu-id="ffb6f-208">4</span></span>         | <span data-ttu-id="ffb6f-209">استجابة العملية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-209">Process response</span></span>             | <span data-ttu-id="ffb6f-210">الحصول على استجابة خدمة الويب.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-210">Get the web service response.</span></span>                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="ffb6f-211">إعداد عنوان URL لخدمات الويب SEFAZ</span><span class="sxs-lookup"><span data-stu-id="ffb6f-211">Set up the URL for SEFAZ web services</span></span>

1. <span data-ttu-id="ffb6f-212">في الصفحة **إعداد إصدار الميزة** ، على علامة التبويب **الإجراءات** ، على علامة التبويب السريعة **الإجراءات‏‎** ، حدد **استدعاء خدمة SEFAZ البرازيلية** (معرف الإجراء **3** ).</span><span class="sxs-lookup"><span data-stu-id="ffb6f-212">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3** ).</span></span>
2. <span data-ttu-id="ffb6f-213">على علامة التبويب السريعة **المعلمات** ، في حقل **معلمة عنوان URL** ، أدخل عنوان URL لخدمة الويب SEFAZ لإلغاء NF-e موافق عليه.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-213">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for cancellation of an approved NF-e.</span></span>

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a><span data-ttu-id="ffb6f-214">جعل بيئة الفوترة الإلكترونية متوفرة وتعيين إصدار تمهيدي</span><span class="sxs-lookup"><span data-stu-id="ffb6f-214">Make an e-Invoicing environment available and assign a Draft version</span></span>

1. <span data-ttu-id="ffb6f-215">في صفحة **ميزات الفوترة الإلكترونية** ، على علامة التبويب **البيئات** ، حدد **تمكين**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-215">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="ffb6f-216">في حقل **البيئة** ، حدد البيئة.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-216">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="ffb6f-217">في الحقل **ساري من‬‏‫** ، حدد التاريخ الذي يجب أن تصبح فيه البيئة سارية المفعول.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-217">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="ffb6f-218">حدد **تمكين**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-218">Select **Enable**.</span></span>

![تمكين بيئة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a><span data-ttu-id="ffb6f-220">تغيير الحالة إلى "مكتمل"</span><span class="sxs-lookup"><span data-stu-id="ffb6f-220">Change the status to Completed</span></span>

1. <span data-ttu-id="ffb6f-221">في الصفحة **ميزات الفوترة الإلكترونية** ، على علامة تبويب **الإصدارات** ، حدد إصدار ميزة الفوترة الإلكترونية بالحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-221">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="ffb6f-222">حدد **حالة التغيير \> مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-222">Select **Change status \> Complete**.</span></span>

### <a name="change-the-status-to-publish"></a><span data-ttu-id="ffb6f-223">تغيير المسار إلى "نشر"</span><span class="sxs-lookup"><span data-stu-id="ffb6f-223">Change the status to Publish</span></span>

1. <span data-ttu-id="ffb6f-224">في الصفحة **ميزات الفوترة الإلكترونية** ، على علامة تبويب **الإصدارات** ، حدد إصدار ميزة الفوترة الإلكترونية بالحالة **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-224">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="ffb6f-225">حدد **تغيير الحالة \> نشر**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-225">Select **Change status \> Publish**.</span></span>

![نشر ميزة الفوترة الإلكترونية](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a><span data-ttu-id="ffb6f-227">إعداد الوظيفة الإضافية الفوترة الإلكترونية في Finance أو Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ffb6f-227">Set up Electronic invoicing add-on integration in Finance or Supply Chain Management</span></span>

<span data-ttu-id="ffb6f-228">اثناء الإعداد، ستقوم بإكمال المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb6f-228">During setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="ffb6f-229">تشغيل ميزة NF-e الفيدرالية للبرازيل.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-229">Turn on the NF-e Federal feature for Brazil.</span></span>
2. <span data-ttu-id="ffb6f-230">استيراد نموذج بيانات التقارير الإلكترونية المحدد وتعيين نموذج البيانات والتنسيقات المطلوبة للمستندات المالية NF-e.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-230">Import the specific ER data model, the data model mapping, and the formats that are required for NF-e fiscal documents.</span></span>
3. <span data-ttu-id="ffb6f-231">استيراد تكوين التقارير الإلكترونية وإعداد أنواع الاستجابات المطلوبة لتحديث حالة المستند المالي بعد إرجاع عملية الإرسال.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-231">Import the ER configuration, and set up the response types that are required to update the status of the fiscal document after the submission process is returned.</span></span>

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a><span data-ttu-id="ffb6f-232">تشغيل ميزة NF-e الفيدرالية للبرازيل</span><span class="sxs-lookup"><span data-stu-id="ffb6f-232">Turn on the NF-e Federal feature for Brazil</span></span>

1. <span data-ttu-id="ffb6f-233">انتقل إلى **إدارة المؤسسة \> الإعداد \> معلمات المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-233">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="ffb6f-234">على علامة التبويب **الميزات** ، حدد خانة الاختيار **تمكين** في صف مرجع الميزة **BR00053**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-234">On the **Features** tab, select the **Enable** check box in the row for feature reference **BR00053**.</span></span>

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a><span data-ttu-id="ffb6f-235">استيراد تعيين نموذج بيانات التقارير الإلكترونية المطلوب للمستندات المالية NF-e</span><span class="sxs-lookup"><span data-stu-id="ffb6f-235">Import the ER data model mapping required for NF-e fiscal documents</span></span>

1. <span data-ttu-id="ffb6f-236">سجل دخولك إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-236">Sign in to Finance.</span></span>
2. <span data-ttu-id="ffb6f-237">في مساحة عمل **إعداد التقارير الإلكترونية** ، في قسم **موفرو التكوين** ، حدد اللوحة **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-237">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span> <span data-ttu-id="ffb6f-238">تأكد من تعيين موفر التكوين هذا إلى **نشط**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-238">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="ffb6f-239">لمزيد من المعلومات حول كيفية تعيين موفر إلى **نشط** ، راجع [إنشاء موفري التكوين ووضع علامة نشط عليهم‬](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="ffb6f-239">For information about how to set a provider to **Active** , see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="ffb6f-240">حدد **المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-240">Select **Repositories**.</span></span>
4. <span data-ttu-id="ffb6f-241">حدد **المورد العمومي \> فتح**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-241">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="ffb6f-242">استورد تكوينات **تعيين المستندات المالية**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-242">Import **Fiscal documents mapping** configurations.</span></span>

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a><span data-ttu-id="ffb6f-243">استيراد تكوينات التقارير الإلكترونية وإعداد أنواع الاستجابات للمستندات المالية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-243">Import ER configurations and set up the response types for fiscal documents</span></span>

1. <span data-ttu-id="ffb6f-244">في مساحة عمل **إعداد التقارير الإلكترونية** ، في قسم **موفرو التكوين** ، حدد اللوحة **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-244">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span>
2. <span data-ttu-id="ffb6f-245">حدد **المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-245">Select **Repositories**.</span></span>
3. <span data-ttu-id="ffb6f-246">حدد **المورد العمومي \> فتح**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-246">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="ffb6f-247">استورد **استيراد سجل أخطاء NF-e‬ ‏(BR)** و **تنسيق استيراد بيانات الاستجابة NF-e‬ ‏(BR)** و **استيراد رسالة استجابة NF-e‬‏ (BR)**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-247">Import **NF-e error log import (BR)** , **NF-e response data import format (BR)** , and **NF-e response message import (BR)**.</span></span>
5. <span data-ttu-id="ffb6f-248">انتقل إلى **إدارة المؤسسة \> الإعداد \> معلمات المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-248">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
6. <span data-ttu-id="ffb6f-249">على علامة التبويب **المستند الإلكتروني** ، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-249">On the **Electronic document** tab, select **Add**.</span></span>
6. <span data-ttu-id="ffb6f-250">في الحقل **اسم الجدول** ، أدخل **رأس المستند المالي**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-250">In the **Table name** field, enter **Fiscal document header**.</span></span>
7. <span data-ttu-id="ffb6f-251">في الحقل **سياق المستند** ، حدد **نموذج سياق فاتورة العميل - سياق المستند المالي**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-251">In the **Document context** field, select **Customer invoice context model – Fiscal document context**.</span></span>
8. <span data-ttu-id="ffb6f-252">حدد **أنواع الاستجابات**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-252">Select **Response types**.</span></span>
9. <span data-ttu-id="ffb6f-253">حدد **جديد** ، ثم في حقل **نوع الاستجابة** ، حدد **استجابة‎**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-253">Select **New** , and then, in the **Response type** field, select **Response**.</span></span>
10. <span data-ttu-id="ffb6f-254">في الحقل **حالة الإرسال** ، حدد **معلّق**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-254">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="ffb6f-255">في الحقل **تعيين النموذج** ، حدد **تنسيق استيراد رسالة الاستجابة – تعيين النموذج من رسالة الاستجابة**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-255">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
12. <span data-ttu-id="ffb6f-256">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-256">Select **Save**.</span></span>
13. <span data-ttu-id="ffb6f-257">حدد **جديد** ، ثم في حقل **نوع الاستجابة** ، أدخل **ResponseData‎**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-257">Select **New** , and then, in the **Response type** field, enter **ResponseData**.</span></span>
14. <span data-ttu-id="ffb6f-258">في الحقل **حالة الإرسال** ، حدد **معلّق**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-258">In the **Submission status** field, select **Pending**.</span></span>
15. <span data-ttu-id="ffb6f-259">في الحقل **تعيين النموذج** ، حدد **تنسيق استيراد بيانات الاستجابة NFe - استيراد بيانات الاستجابة**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-259">In the **Model mapping** field, select **NFe response data import format – Response data import**.</span></span>
16. <span data-ttu-id="ffb6f-260">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-260">Select **Save**.</span></span>

## <a name="electronic-invoice-processing"></a><span data-ttu-id="ffb6f-261">معالجة الفواتير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-261">Electronic invoice processing</span></span>

<span data-ttu-id="ffb6f-262">اثناء المعالجة في Finance، ستقوم بإكمال المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb6f-262">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="ffb6f-263">إرسال مستند مالي من خلال الوظيفة الإضافية الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-263">Submit a fiscal document through the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="ffb6f-264">عرض سجلات تنفيذ الإرسال ومراجعة نتائج المعالجة.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-264">View the submission execution logs and review the results of processing.</span></span>
3. <span data-ttu-id="ffb6f-265">إرسال إلغاء مستند مالي من خلال الوظيفة الإضافية الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-265">Submit the cancellation of a fiscal document through the Electronic invoicing add-on.</span></span>

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a><span data-ttu-id="ffb6f-266">إرسال المستندات المالية NF-e لتخويل SEFAZ</span><span class="sxs-lookup"><span data-stu-id="ffb6f-266">Submit NF-e fiscal documents for SEFAZ authorization</span></span> 

<span data-ttu-id="ffb6f-267">بعد تشغيل الميزة **تكامل الوظيفة الإضافية الفوترة الإلكترونية القابلة للتكوين** ، لن يعود استخدام العملية القديمة لإرسال المستندات المالية NF-e ممكنًا (عملية **تصدير/استيراد NF-e** ).</span><span class="sxs-lookup"><span data-stu-id="ffb6f-267">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for submitting NF-e fiscal documents for authorization ( **Export/Import NF-e process** ) can no longer be used.</span></span> <span data-ttu-id="ffb6f-268">لقد تم استبدال هذه العملية بأخرى جديدة تسمى **إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-268">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="ffb6f-269">قبل المتابعة، تأكد من وجود نموذج أو أكثر من نماذج المستندات المالية الإلكترونية 55 للعميل التي تم إصدارها بواسطة المؤسسة المالية للعميل.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-269">Before you continue, make sure that you have one or more customer fiscal documents model 55 that were issued by the customer's fiscal establishment.</span></span> <span data-ttu-id="ffb6f-270">يجب تعيين الاتجاه الخاص بهذه المستندات المالية إلى **صادر** ، ويجب أن تكون الحالة  **مُنشأ**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-270">The direction for these fiscal documents must be set to **Outgoing** , and the status must be **Created**.</span></span> <span data-ttu-id="ffb6f-271">لمزيد من المعلومات، راجع [إصدار المستند المالي للعميل (البرازيل)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span><span class="sxs-lookup"><span data-stu-id="ffb6f-271">For more information, see [Issue customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span></span>

1. <span data-ttu-id="ffb6f-272">انتقل إلى **إدارة المؤسسة \> دوري \> المستندات الإلكترونية \> إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-272">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="ffb6f-273">بالنسبة لعملية الإرسال الأولى لأي مستند، عيّن دائمًا الخيار **إعادة إرسال المستندات** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-273">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="ffb6f-274">إذا كان من الضروري إعادة إرسال مستند من خلال الخدمة، فقم بتعيين هذا الخيار إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-274">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="ffb6f-275">على علامة التبويب السريعة **السجلات المطلوب تضمينها‬** ، حدد **تصفية** لفتح مربع الحوار **استعلام** حيث يمكنك إنشاء استعلام لتحديد مستندات لإرسالها.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-275">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>
4. <span data-ttu-id="ffb6f-276">في علامة التبويب **نطاق** ، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-276">On the **Range** tab, select **Add**.</span></span>
5. <span data-ttu-id="ffb6f-277">في الحقل **الجدول** ، حدد **رأس المستند المالي**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-277">In the **Table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="ffb6f-278">في الحقل **الجدول المشتق** ، حدد **رأس المستند المالي**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-278">In the **Derived table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="ffb6f-279">في الحقل **الحقل** ، حدد **الرقم**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-279">In the **Field** field, select **Number**.</span></span>
7. <span data-ttu-id="ffb6f-280">في الحقل **المعايير** ، أدخل رقم المستند المالي الذي يجب إرساله.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-280">In the **Criteria** field, enter the number of the fiscal document that should be submitted.</span></span>
8. <span data-ttu-id="ffb6f-281">حدد **موافق** لإغلاق مربع الحوار **استعلام**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-281">Select **OK** to close the **Inquiry** dialog box.</span></span>
8. <span data-ttu-id="ffb6f-282">حدد **موافق** لإرسال المستندات المحددة.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-282">Select **OK** to submit the selected documents.</span></span>

> [!NOTE]
> <span data-ttu-id="ffb6f-283">أثناء محاولتك الأولى لإرسال مستند من خلال الخدمة، ستتم مطالبتك بتأكيد الاتصال بالوظيفة الإضافية الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-283">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="ffb6f-284">حدد **انقر هنا للاتصال بخدمة إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-284">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-all-submission-logs"></a><span data-ttu-id="ffb6f-285">عرض جميع سجلات الإرسال</span><span class="sxs-lookup"><span data-stu-id="ffb6f-285">View all submission logs</span></span>

<span data-ttu-id="ffb6f-286">بعد تشغيل الميزة **تكامل الوظيفة الإضافية الفوترة الإلكترونية القابلة للتكوين‬‏‫** ، تتوفر صفحة جديدة تتيح لك متابعة عملية إرسال المستند.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-286">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="ffb6f-287">يمكنك استخدام هذه الصفحة عرض سجلات الإرسال لكافة المستندات المرسلة.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-287">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="ffb6f-288">انتقل إلى **إدارة المؤسسة \> دوري \> المستندات الإلكترونية \> سجل إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="ffb6f-289">في الحقل **نوع المستند** ، حدد **رأس المستند المالي** لتصفية للمستندات المالية فقط.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-289">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="ffb6f-290">في جزء الإجراءات، حدد **الاستعلامات \> تفاصيل الإرسال** لعرض سجلات تنفيذ الإرسال.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-290">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

![عرض تفاصيل سجل الإرسال](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> <span data-ttu-id="ffb6f-292">للمستندات المالية NF-e، يُظهر عمود **رمز الخطأ** رمز الإرجاع المرتجع بواسطة خدمات الويب SEFAZ.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-292">For NF-e fiscal documents, the **Error code** column shows the return code that was returned by SEFAZ web services.</span></span>

### <a name="view-submission-logs-through-the-fiscal-document-page"></a><span data-ttu-id="ffb6f-293">عرض سجلات الإرسال من خلال صفحة المستندات المالية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-293">View submission logs through the fiscal document page</span></span>

<span data-ttu-id="ffb6f-294">بعد تشغيل ميزة **الوظيفة الإضافية الفوترة الإلكترونية القابلة للتكوين‬‏‫** ، يمكنك أيضًا عرض سجلات الإرسال من صفحة المستندات المالية.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-294">After you turn on the **Configurable Electronic invoicing add-on integration** feature, you can also view the submission logs through the fiscal document page.</span></span>

1. <span data-ttu-id="ffb6f-295">انتقل إلى **دفتر الأستاذ العام \> الاستعلامات والتقارير \> المستندات المالية \> جميع المستندات المالية**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-295">Go to **General ledger \> Inquiries and reports \> Fiscal documents \> All fiscal documents**.</span></span>
2. <span data-ttu-id="ffb6f-296">حدد مستندًا ماليًا تم إرساله في وقت سابق من خلال الوظيفة الإضافية الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-296">Select a fiscal document that was previously submitted through the Electronic invoicing add-on.</span></span>
3. <span data-ttu-id="ffb6f-297">في جزء الإجراءات، على علامة تبويب **NF-e الفيدرالية** ، حدد **سجل المستندات الإلكترونية‬**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-297">On the Action Pane, on the **NF-e federal** tab, select **Electronic document log**.</span></span>

![عرض سجلات الإرسال من صفحة المستندات المالية](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a><span data-ttu-id="ffb6f-299">إرسال المستندات المالية NF-e الموافق عليها لإلغاء SEFAZ</span><span class="sxs-lookup"><span data-stu-id="ffb6f-299">Submit approved NF-e fiscal documents for SEFAZ cancellation</span></span>

<span data-ttu-id="ffb6f-300">بعد تشغيل الميزة **تكامل الوظيفة الإضافية الفوترة الإلكترونية القابلة للتكوين** ، لن يعود استخدام العملية القديمة لإلغاء المستندات المالية NF-e ممكنًا.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-300">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling NF-e fiscal documents can no longer be used.</span></span> <span data-ttu-id="ffb6f-301">سيتم استبدال العملية بعملية إلغاء جديدة مضمنة في صفحة **سجل إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-301">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

> [!NOTE]
> <span data-ttu-id="ffb6f-302">تأكد من أنك قمت بتشغيل إلغاء المستند المالي للعميل لمستند مالي NF-e موافق عليه.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-302">Make sure that you've run the cancellation of the customer fiscal document for an approved NF-e fiscal document.</span></span> <span data-ttu-id="ffb6f-303">لمزيد من المعلومات، راجع [إلغاء المستند المالي للعميل (البرازيل)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span><span class="sxs-lookup"><span data-stu-id="ffb6f-303">For more information see, [Cancel customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span></span>

1. <span data-ttu-id="ffb6f-304">انتقل إلى **إدارة المؤسسة \> دوري \> المستندات الإلكترونية \> سجل إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-304">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="ffb6f-305">حدد المستند المالي، ثم حدد **الوظائف \> إرسال عمليات الإرسال ذات الصلة**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-305">Select the fiscal document, and then select **Functions \> Send related submissions**.</span></span>
3. <span data-ttu-id="ffb6f-306">ادخل وصفًا لعملية الإرسال ذات الصلة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-306">Enter a description for the related submission, and then select **OK**.</span></span>

### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="ffb6f-307">عرض سجلات إرسال الإلغاء</span><span class="sxs-lookup"><span data-stu-id="ffb6f-307">View cancellation submission logs</span></span>

1. <span data-ttu-id="ffb6f-308">انتقل إلى **إدارة المؤسسة \> دوري \> المستندات الإلكترونية \> سجل إرسال المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-308">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="ffb6f-309">في الحقل **نوع المستند** ، حدد **رأس المستند المالي** لتصفية للمستندات المالية فقط.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-309">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="ffb6f-310">حدد المستند المالي، ثم في جزء الإجراءات، حدد **الاستعلامات \> الإرسال ذو الصلة**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-310">Select the fiscal document, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="ffb6f-311">عمليات الإرسال ذات الصلة هي عمليات الإرسال ذات الصلة بعملية إرسال رئيسية تم تنفيذها أولاً.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-311">Related submissions are submissions that are related to a main submission that was made first.</span></span> <span data-ttu-id="ffb6f-312">على سبيل المثال، يعتبر الإرسال الذي يخول NF-e محدد الإرسال الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-312">For example, the submission that authorizes a specific NF-e is the main submission.</span></span> <span data-ttu-id="ffb6f-313">عملية الإرسال التي تتطلب إلغاء NF-e نفسه في SEFAZ هي عملية إرسال ذات صلة.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-313">The submission that requests the cancellation of the same NF-e in SEFAZ is a related submission.</span></span> <span data-ttu-id="ffb6f-314">وهي موجودة فقط لأنها تطلب إلغاء الوظيفة التي تم تنفيذها من خلال إرسال آخر.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-314">It exists only because it's requesting the cancellation of the job that was done through another submission.</span></span>

    <span data-ttu-id="ffb6f-315">تعرض صفحة **عمليات الإرسال ذات الصلة** جميع عمليات الإرسال ذات الصلة وحالة الإرسال لمستند مالي معين.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-315">The **Related submissions** page shows all related submissions, and their submission status, for a given fiscal document.</span></span> <span data-ttu-id="ffb6f-316">في الرسم التوضيحي التالي، يمثل السطر الأول الإرسال الذي طالب بالموافقة على المستند المالي.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-316">In the following illustration, the first line represents the submission that requested approval of the fiscal document.</span></span> <span data-ttu-id="ffb6f-317">ويمثل السطر الثاني الإرسال الذي قام بإلغاء المستند المالي هذا.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-317">The second line represents the submission that canceled that fiscal document.</span></span>

    ![عرض سجلات إرسال الإلغاء](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. <span data-ttu-id="ffb6f-319">في جزء الإجراءات، حدد **الاستعلامات \> تفاصيل الإرسال** لعرض سجلات تنفيذ الإرسال.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-319">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![عرض تفاصيل سجلات إرسال الإلغاء](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="ffb6f-321">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-321">Privacy notice</span></span>
<span data-ttu-id="ffb6f-322">قد يتطلب تمكين ميزة BR-00053‏ (NF-e الفيدرالية) إرسال بيانات محدودة، تتضمن معرف التسجيل الضريبي للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-322">Enabling the BR-00053 (NF-e Federal) feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="ffb6f-323">سيتم إرسال هذه البيانات إلى وكالات خارجية معتمدة من قبل هيئة الضرائب لأغراض إرسال الفواتير الإلكترونية إلى هيئة الضرائب هذه بالتنسيق المعرف مسبقًا والمطلوب لإجراء التكامل مع خدمة الويب الخاصة بالحكومة.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-323">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="ffb6f-324">بإمكان المسؤول تمكين وتعطيل ميزة BR-00053 ‏(NF-e الفيدرالية) من خلال الانتقال إلى **إدارة المؤسسة \> الإعداد \> معلمات المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-324">An administrator can enable and disable the BR-00053 (NF-e Federal) feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="ffb6f-325">حدد علامة التبويب **الميزات** ، وحدد الصف الذي تحتوي على ميزة BR-00053، ثم قم بإجراء التحديد المناسب.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-325">Select the **Features** tab, select the row containing the BR-00053 feature, and then make the appropriate selection.</span></span> <span data-ttu-id="ffb6f-326">تخضع البيانات المستوردة من هذه الأنظمة الخارجية في خدمة Dynamics 365 عبر الإنترنت [لبيان الخصوصية](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="ffb6f-326">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="ffb6f-327">الرجاء مراجعه أقسام إشعار الخصوصية في وثائق الميزات الخاصة بالبلد لمزيد من المعلومات.</span><span class="sxs-lookup"><span data-stu-id="ffb6f-327">Please consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="ffb6f-328">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-328">Additional resources</span></span>

- [<span data-ttu-id="ffb6f-329">نظرة عامة على الوظيفة الإضافية الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-329">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="ffb6f-330">بدء استخدام الوظيفة الإضافية "الفوترة الإلكترونية"</span><span class="sxs-lookup"><span data-stu-id="ffb6f-330">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="ffb6f-331">إعداد الوظيفة الإضافية الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="ffb6f-331">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
