---
title: تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها
description: يوفر هذا الموضوع معلومات حول كيفية استخدام ميزة تتبع الأداء في التقارير الإلكترونية (ER) لاستكشاف مشكلات الأداء وإصلاحها.
author: NickSelin
manager: AnnBe
ms.date: 05/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: aa71db2752889bc905c22bab1cf2fa46d7ee07c7
ms.sourcegitcommit: 67d00b95952faf0db580d341249d4e50be59119c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1576536"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="a0158-103">تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="a0158-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a0158-104">كجزء من عملية تصميم تكوينات التقارير الإلكترونية (ER) لإنشاء مستندات إلكترونية ، يمكنك تحديد الطريقة المستخدمة للحصول على البيانات من Microsoft Dynamics 365 for Finance and Operations وإدخالها في الإخراج الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="a0158-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</span></span> <span data-ttu-id="a0158-105">تساعد ميزة تتبع أداء التقارير الإلكترونية في تقليل الوقت والتكلفة بشكل كبير في جمع تفاصيل تنفيذ تنسيق التقارير الإلكترونية واستخدامها لاستكشاف مشكلات الأداء وإصلاحها.</span><span class="sxs-lookup"><span data-stu-id="a0158-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="a0158-106">يوفر هذا البرنامج التعليمي إرشادات حول كيفية أخذ تتبعات الأداء لتنسيقات التقارير الإلكترونية المنفذة في Finance and Operations، وكيفية استخدام المعلومات من هذه التتبعات للمساعدة في تحسين الأداء.</span><span class="sxs-lookup"><span data-stu-id="a0158-106">This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a0158-107">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="a0158-107">Prerequisites</span></span>

<span data-ttu-id="a0158-108">لإكمال الأمثلة في هذا البرنامج التعليمي، يجب أن يكون لديك الوصول التالي:</span><span class="sxs-lookup"><span data-stu-id="a0158-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="a0158-109">الوصول إلى Finance and Operations لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="a0158-109">Access to Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="a0158-110">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="a0158-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="a0158-111">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="a0158-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="a0158-112">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="a0158-112">System administrator</span></span>

- <span data-ttu-id="a0158-113">يمكنك الوصول إلى مثيل خدمات التكوين التنظيمية (RCS) التي تم توفيرها لنفس المستأجر مثل Finance and Operations، لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="a0158-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</span></span>

    - <span data-ttu-id="a0158-114">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="a0158-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="a0158-115">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="a0158-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="a0158-116">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="a0158-116">System administrator</span></span>

<span data-ttu-id="a0158-117">يجب عليك أيضًا تنزيل الملفات التالية وتخزينها محليًا.</span><span class="sxs-lookup"><span data-stu-id="a0158-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="a0158-118">ملف</span><span class="sxs-lookup"><span data-stu-id="a0158-118">File</span></span>                                  | <span data-ttu-id="a0158-119">المحتوى</span><span class="sxs-lookup"><span data-stu-id="a0158-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="a0158-120">إصدار نموذج تتبع الأداء رقم 1</span><span class="sxs-lookup"><span data-stu-id="a0158-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="a0158-121">تكوين نموذج عينة بيانات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a0158-121">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| <span data-ttu-id="a0158-122">إصدار بيانات تعريف تتبع الأداء رقم 1</span><span class="sxs-lookup"><span data-stu-id="a0158-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="a0158-123">تكوين بيانات تعريف عينة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a0158-123">Sample ER metadata configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| <span data-ttu-id="a0158-124">إصدار تعيين تتبع الأداء رقم 1.1</span><span class="sxs-lookup"><span data-stu-id="a0158-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="a0158-125">تكوين تعيين نموذج عينة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a0158-125">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="a0158-126">إصدار تنسيق تتبع الأداء رقم 1.1</span><span class="sxs-lookup"><span data-stu-id="a0158-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="a0158-127">تكوين تنسيق عينة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a0158-127">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="a0158-128">تكوين معلمات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a0158-128">Configure ER parameters</span></span>

<span data-ttu-id="a0158-129">يتم تخزين كل تتبع أداء تقارير إلكترونية يتم إنشاؤه في Finance and Operations كمرفق بسجل تسجيل التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="a0158-129">Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="a0158-130">يُستخدم إطار إدارة المستندات (DM) في Finance and Operations لإدارة هذه المرفقات.</span><span class="sxs-lookup"><span data-stu-id="a0158-130">The Document management (DM) framework of Finance and Operations is used to manage these attachments.</span></span> <span data-ttu-id="a0158-131">يجب تكوين معلمات التقارير الإلكترونية مسبقًا، لتحديد نوع مستند إدارة المستندات (DM) الذي يجب استخدامه لإرفاق تتبعات الأداء.</span><span class="sxs-lookup"><span data-stu-id="a0158-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="a0158-132">في Finance and Operation، في مساحة عمل **التقارير الإلكترونية**، حدد **معلمات التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="a0158-132">In Finance and Operation, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="a0158-133">ثم في صفحة **معلمات التقارير الإلكترونية**، ضمن علامة التبويب **مرفقات**، في حقل **أخرى**، حدد نوع مستند إدارة المستندات الذي سيتم استخدامه لتتبعات الأداء.</span><span class="sxs-lookup"><span data-stu-id="a0158-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![صفحه معلمات التقارير الإلكترونية في Finance and Operations](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="a0158-135">لتوفيره في حقل البحث **أخرى**، يجب تكوين نوع مستند إدارة المستندات بالطريقة التالية في صفحة **أنواع المستندات** (**إدارة المؤسسة\>إدارة المستندات\>أنواع المستندات**):</span><span class="sxs-lookup"><span data-stu-id="a0158-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="a0158-136">**الفئة:** إرفاق ملف</span><span class="sxs-lookup"><span data-stu-id="a0158-136">**Class:** Attach file</span></span>
- <span data-ttu-id="a0158-137">**المجموعة** : ملف</span><span class="sxs-lookup"><span data-stu-id="a0158-137">**Group:** File</span></span>

![صفحه أنواع المستندات في Finance and Operations](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="a0158-139">يجب أن يكون نوع المستند المحدد متاحًا في كل شركة من مثيلات Financial and Operations الحالية ، لأن مرفقات إدارة المستندات خاصة بالشركة.</span><span class="sxs-lookup"><span data-stu-id="a0158-139">The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="a0158-140">تكوين معلمات خدمات التكوين التنظيمية (RCS)</span><span class="sxs-lookup"><span data-stu-id="a0158-140">Configure RCS parameters</span></span>

<span data-ttu-id="a0158-141">سيتم استيراد تتبعات أداء التقارير الإلكترونية التي تم إنشاؤها في Finance and Operations إلى خدمات التكوين التنظيمية (RCS) للتحليل باستخدام مصمم التنسيق الخاص بالتقارير الإلكترونية ومصمم تعيينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a0158-141">ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="a0158-142">نظرًا لأنه يتم تخزين تتبعات أداء التقارير الإلكترونية كمرفقات لسجل تسجيل التنفيذ المرتبط بتنسيق التقارير الإلكترونية، يجب عليك تكوين معلمات خدمات التكوين التنظيمية مسبقًا، لتحديد نوع مستند إدارة المستندات الذي يجب استخدامه لإرفاق تتبعات الأداء.</span><span class="sxs-lookup"><span data-stu-id="a0158-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="a0158-143">في مثيل خدمات التكوين التنظيمية (RCS) الذي تم توفيره للشركة الخاصة بك، في مساحة عمل **التقارير الإلكترونية**، حدد **معلمات التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="a0158-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="a0158-144">ثم في صفحة **معلمات التقارير الإلكترونية**، ضمن علامة التبويب **مرفقات**، في حقل **أخرى**، حدد نوع مستند إدارة المستندات الذي سيتم استخدامه لتتبعات الأداء.</span><span class="sxs-lookup"><span data-stu-id="a0158-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![صفحة معلمات التقارير الإلكترونية في خدمات التكوين التنظيمية](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="a0158-146">لتوفيره في حقل البحث **أخرى**، يجب تكوين نوع مستند إدارة المستندات بالطريقة التالية في صفحة **أنواع المستندات** (**إدارة المؤسسة\>إدارة المستندات\>أنواع المستندات**):</span><span class="sxs-lookup"><span data-stu-id="a0158-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="a0158-147">**الفئة:** إرفاق ملف</span><span class="sxs-lookup"><span data-stu-id="a0158-147">**Class:** Attach file</span></span>
- <span data-ttu-id="a0158-148">**المجموعة** : ملف</span><span class="sxs-lookup"><span data-stu-id="a0158-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="a0158-149">تصميم حل تقارير إلكترونية</span><span class="sxs-lookup"><span data-stu-id="a0158-149">Design an ER solution</span></span>

<span data-ttu-id="a0158-150">افترض انك قمت بالبدء بتصميم حل جديد للتقارير الإلكترونية لإنشاء تقرير جديد يقدم حركات المورد.</span><span class="sxs-lookup"><span data-stu-id="a0158-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="a0158-151">في الوقت الحالي، يمكنك العثور علي حركات مورد محدد في **حركات الموردين** (انتقل إلى **الحساب المستحق\> الموردين\> جميع الموردين**، وحدد موردًا، ثم في جزء الإجراءات، في علامة التبويب **مود**، في مجموعة **الحركات**، حدد **الحركات**).</span><span class="sxs-lookup"><span data-stu-id="a0158-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="a0158-152">ومع ذلك، فأنت تريد أن يكون لديك كل حركة بائع في نفس الوقت في مستند إلكتروني واحد بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="a0158-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="a0158-153">سيتألف هذا الحل من العديد من تكوينات التقارير الإلكترونية التي تحتوي على مكونات نموذج البيانات وبيانات التعريف ورسم الخرائط ومكونات التنسيق المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="a0158-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="a0158-154">سجل الدخول إلى مثيل خدمات التكوين التنظيمية الذي تم توفيره لشركتك.</span><span class="sxs-lookup"><span data-stu-id="a0158-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="a0158-155">في هذا البرنامج التعليمي ، ستقوم بإنشاء وتعديل تكوينات لعينة الشركة **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="a0158-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="a0158-156">لذلك ، تأكد من إضافة موفر التكوين هذا إلى خدمة التكوين التنظيمية وتحديده نشطًا.</span><span class="sxs-lookup"><span data-stu-id="a0158-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="a0158-157">للحصول علي الإرشادات، راجع [إنشاء موفري التكوين ووضع علامة عليهم كنشطين](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="a0158-157">For instructions, see the [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) procedure.</span></span>
3. <span data-ttu-id="a0158-158">في مساحة عمل **إعداد التقارير الإلكترونية**، حدد الإطار المتجانب **تكوينات إعداد التقارير**.</span><span class="sxs-lookup"><span data-stu-id="a0158-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="a0158-159">في صفحه **التكوينات**، قم باستيراد تكوينات التقارير الإلكترونية التي قمت بتنزيلها كشرط مسبق في خدمة التكوين التنظيمية، بالترتيب التالي: نموذج البيانات، وبيانات التعريف، وتعيين النموذج، والتنسيق.</span><span class="sxs-lookup"><span data-stu-id="a0158-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="a0158-160">بالنسبة لكل تكوين، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="a0158-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="a0158-161">في جزء الإجراءات، حدد **تبادل \> تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="a0158-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="a0158-162">حدد **استعراض** لتحديد الملف المناسب لتكوين التقارير الإلكترونية المطلوب بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="a0158-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="a0158-163">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a0158-163">Select **OK**.</span></span>

    ![صفحة التكوينات في خدمة التكوين التنظيمية](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="a0158-165">تشغيل حل التقارير الإلكترونية لتتبع التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a0158-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="a0158-166">افترض أنك قمت بالانتهاء من تصميم الإصدار الأول لحل التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a0158-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="a0158-167">وتريد الآن اختبارها في مثيل Finance and Operations وتحليل أداء التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="a0158-167">You now want to test it in your Finance and Operations instance and analyze execution performance.</span></span>

### <a id='import-configuration'></a><span data-ttu-id="a0158-168">استيراد تكوين التقارير الإلكترونية من خدمة التكوين التنظيمية إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a0158-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="a0158-169">سجل الدخول إلى مثيل Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a0158-169">Sign in to your Finance and Operations instance.</span></span>
2. <span data-ttu-id="a0158-170">بالنسبة لهذا البرنامج التعليمي، ستقوم باستيراد التكوينات من مثيل خدمة التكوين التنظيمية الخاص بك (حيث تقوم بتصميم مكونات التقارير الإلكترونية الخاصة بك) في مثيل Finance and Operations (حيث تقوم باختبارها وأخيرًا استخدامها).</span><span class="sxs-lookup"><span data-stu-id="a0158-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</span></span> <span data-ttu-id="a0158-171">ولذلك، يجب التأكد من إعداد كافة النتائج الملموسة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="a0158-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="a0158-172">لمزيد من المعلومات، راجع إجراء [استيراد تكوينات التقارير الإلكترونية من خدمات التكوين التنظيمية (RCS)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).</span><span class="sxs-lookup"><span data-stu-id="a0158-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) procedure.</span></span>
3. <span data-ttu-id="a0158-173">اتبع الخطوات التالية لاستيراد التكوينات من خدمات التكوين التنظيمية إلى Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="a0158-173">Follow these steps to import the configurations from RCS into Finance and Operations:</span></span>

    1. <span data-ttu-id="a0158-174">في مساحة عمل **التقارير الإلكترونية**، وفي تجانب موفر تكوين **Litware, Inc.**، حدد **المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="a0158-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="a0158-175">في صفحة **مستودع التكوين**، حدد المستودع من **خدمات التكوين التنظيمية**، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="a0158-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="a0158-176">في علامة التبويب **التكوينات**، حدد تكوين **تنسيق تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="a0158-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="a0158-177">في علامة التبويب السريع **الإصدارات**، حدد الإصدار **1.1** من التكوين المحدد، ثم حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="a0158-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![تكوين مستودع التكوين في Finance and Operations](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="a0158-179">يتم تلقائيا استيراد الإصدارات المقابلة من نموذج البيانات وتكوينات تعيين النموذج كمتطلبات مسبقة لتكوين تنسيق التقارير الإلكترونية المستورد.</span><span class="sxs-lookup"><span data-stu-id="a0158-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="a0158-180">تشغيل تتبع أداء التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a0158-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="a0158-181">في Finance and Operations، انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية\> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="a0158-181">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="a0158-182">في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="a0158-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="a0158-183">في مربع الحوار **معلمات المستخدمين**، في قسم **تتبع التنفيذ**، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="a0158-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="a0158-184">في حقل **تنسيق تتبع التنفيذ**، حدد **تصحيح تنسيق التتبع** للبدء في تجميع تفاصيل تنفيذ تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a0158-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="a0158-185">عند تحديد هذه القيمة ، سيقوم تتبع الأداء بجمع معلومات حول الوقت الذي يتم إنفاقه على الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="a0158-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="a0158-186">تشغيل كل مصدر بيانات في تعيين النموذج الذي تم استدعاؤه للحصول على البيانات</span><span class="sxs-lookup"><span data-stu-id="a0158-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="a0158-187">معالجة كل عنصر تنسيق لإدخال البيانات في الإخراج الذي يتم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="a0158-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="a0158-188">يمكنك استخدام حقل **تنسيق تتبع التنفيذ** لتحديد تنسيق تتبع الأداء الذي تم إنشاؤه والذي يتم تخزينه لتنسيق التقارير الإلكترونية وعناصر التعيينات.</span><span class="sxs-lookup"><span data-stu-id="a0158-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="a0158-189">عن طريق تحديد **تصحيح تنسيق التتبع** باعتبارها القيمة، ستتمكن من تحليل محتوى التتبع في مصمم عمليات التقارير الإلكترونية، ورؤية تنسيق التقارير الإلكترونية أو عناصر التعيين المذكورة في التتبع.</span><span class="sxs-lookup"><span data-stu-id="a0158-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="a0158-190">قم بتعيين الخيارات التالية إلى **نعم** لجمع التفاصيل الخاصة بتنفيذ تعيين نموذج التقارير الإلكترونية ومكونات تنسيق التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="a0158-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="a0158-191">**جمع إحصاءات الاستعلام** – عند تشغيل هذا الخيار، سيقوم تتبع الأداء بجمع المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="a0158-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="a0158-192">عدد استدعاءات قواعد البيانات التي تم إجراؤها بواسطة مصادر البيانات</span><span class="sxs-lookup"><span data-stu-id="a0158-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="a0158-193">عدد الاستدعاءات المتكررة لقاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="a0158-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="a0158-194">تفاصيل بيانات SQL التي تم استخدامها لإجراء استدعاءات قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="a0158-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="a0158-195">**تتبع الوصول إلى التخزين المؤقت** – عند تشغيل هذا الخيار، سيقوم تتبع الأداء بجمع معلومات حول استخدام ذاكره التخزين المؤقت لتعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a0158-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="a0158-196">**الوصول إلى بيانات التتبع** - عند تشغيل هذا الخيار، سيقوم تتبع الأداء بجمع معلومات حول عدد الاستدعاءات إلى قاعدة البيانات لمصادر البيانات المنفذة الخاصة بنوع قائمة السجلات.</span><span class="sxs-lookup"><span data-stu-id="a0158-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="a0158-197">**تتبع تعداد القائمة‬** - عند تشغيل هذا الخيار، سيقوم تتبع الأداء بجمع معلومات حول عدد السجلات التي تم طلبها من مصادر البيانات الخاصة بنوع قائمة السجلات.</span><span class="sxs-lookup"><span data-stu-id="a0158-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a0158-198">وتكون المحددات الموجودة في مربع الحوار **معلمات المستخدمين** خاصة بالمستخدم والشركة الحالية.</span><span class="sxs-lookup"><span data-stu-id="a0158-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![مربع حوار معلمات المستخدمين في Finance and Operations](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a><span data-ttu-id="a0158-200">تشغيل تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a0158-200">Run the ER format</span></span>

1. <span data-ttu-id="a0158-201">في Finance and Operations، حدد شركة **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="a0158-201">In Finance and Operations, select the **DEMF** company.</span></span>
2. <span data-ttu-id="a0158-202">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="a0158-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="a0158-203">في صفحة **التكوينات**، في شجرة التكوين، حدد عنصر **تنسيق تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="a0158-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="a0158-204">في جزء الإجراءات، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="a0158-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="a0158-205">لاحظ أن الملف الذي تم إنشاؤه يقدم معلومات حول 265 حركة لستة موردين.</span><span class="sxs-lookup"><span data-stu-id="a0158-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="a0158-206">مراجعه تتبع التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a0158-206">Review the execution trace</span></span>

### <a id='export-trace'></a><span data-ttu-id="a0158-207">تصدير التتبع الذي تم إنشاؤه من Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a0158-207">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="a0158-208">يتم فصل تتبعات الأداء من تنسيق التقارير الإلكترونية المصدر ويمكن إجراء تسلسلها إلى ملف مضغوط خارجي.</span><span class="sxs-lookup"><span data-stu-id="a0158-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="a0158-209">في Finance and Operations، انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> سجلات تصحيح التكوين**.</span><span class="sxs-lookup"><span data-stu-id="a0158-209">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="a0158-210">في صفحة **سجلات تشغيل التقارير الإلكترونية**، في الجزء الأيسر، في حقل **اسم التكوين**، حدد **تنسيق تتبع الأداء** للعثور علي سجلات التسجيل التي تم إنشاؤها بواسطة تنفيذ تكوين **تنسيق تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="a0158-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="a0158-211">حدد الزر **المرفقات** (رمز مشبك الورق) في الواوية العلوية اليمنى للصفحة، أو اضغط على **Ctrl+Shift+A**.</span><span class="sxs-lookup"><span data-stu-id="a0158-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![زر المرفقات في صفحة سجلات تشغيل التقارير الإلكترونية في Finance and Operations](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="a0158-213">في الصفحة **المرفقات الخاصة بسجلات تشغيل التقارير الإلكترونية**، في جزء الإجراء، حدد **فتح** للحصول علي تتبع الأداء كملف zip وتخزينه محليًا.</span><span class="sxs-lookup"><span data-stu-id="a0158-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![المرفقات الخاصة بصفحة سجلات تشغيل التقارير الإلكترونية في Finance and Operations](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="a0158-215">يحتوي التتبع الذي تم إنشاؤه علي مرجع لتقرير التقارير الإلكترونية المصدر من خلال معرف تقرير بتنسيق **GUID** فقط.</span><span class="sxs-lookup"><span data-stu-id="a0158-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="a0158-216">ترقيم إصدار التنسيق غير مهم.</span><span class="sxs-lookup"><span data-stu-id="a0158-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="a0158-217">لاحظ أن الاقتران بين تتبع الأداء الذي تم إنشاؤه لتنسيق التقارير الإلكترونية الذي تم تنفيذه وتعيين نموذج التقارير الإلكترونية يستند إلى الواصف الجذر الذي تم استخدامه ونموذج البيانات العامة.</span><span class="sxs-lookup"><span data-stu-id="a0158-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="a0158-218">ترقيم إصدار التنسيق وتعيين النموذج غير مهم.</span><span class="sxs-lookup"><span data-stu-id="a0158-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="a0158-219">إن تعيين علامة **الإعداد الافتراضي لتعيين النموذج** لتعيين النموذج غير مهم أيضًا.</span><span class="sxs-lookup"><span data-stu-id="a0158-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a id='import-trace'></a><span data-ttu-id="a0158-220">استيراد التتبع الذي تم إنشاؤه في خدمة التكوين التنظيمية</span><span class="sxs-lookup"><span data-stu-id="a0158-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="a0158-221">في خدمة التكوين التنظيمية، في مساحة عمل **إعداد التقارير الإلكترونية**، حدد الإطار المتجانب **تكوينات إعداد التقارير**.</span><span class="sxs-lookup"><span data-stu-id="a0158-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="a0158-222">في صفحة **التكوينات**، في شجره التكوين ، قم بتوسيع نصر **نموذج تتبع الأداء**، وحدد عنصر **تنسيق تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="a0158-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="a0158-223">في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="a0158-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="a0158-224">في صفحة **مصمم التنسيق**، في جزء الإجراءات، حدد **تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="a0158-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="a0158-225">في مربع الحوار **إعدادات نتيجة تتبع الأداء**، حدد **تتبع الأداء المهم**.</span><span class="sxs-lookup"><span data-stu-id="a0158-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="a0158-226">حدد **استعراض** لتحديد الملف المضغوط الذي قمت بتصديره من Finance and Operations من قبل.</span><span class="sxs-lookup"><span data-stu-id="a0158-226">Select **Browse** to select the zip file that you exported from Finance and Operations earlier.</span></span>
7. <span data-ttu-id="a0158-227">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a0158-227">Select **OK**.</span></span>

    ![مربع الحوار إعدادات نتيجة تتبع الأداء في خدمة التكوين التنظيمية](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="a0158-229">استخدام تتبع الأداء للتحليل في خمة التكوين التنظمية - تنفيذ التنسيق</span><span class="sxs-lookup"><span data-stu-id="a0158-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="a0158-230">في خدمات التكوين التنظيمية، في صفحة **مصمم التنسيق**، حدد **توسيع/طي** لتوسيع محتويات كافة عناصر التنسيق.</span><span class="sxs-lookup"><span data-stu-id="a0158-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="a0158-231">لاحظ أنه يتم عرض معلومات إضافية لبعض عناصر التنسيق الحالي:</span><span class="sxs-lookup"><span data-stu-id="a0158-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="a0158-232">الوقت الفعلي الذي استغرقه إدخال البيانات في الإخراج الذي تم إنشاؤه باستخدام عنصر التنسيق</span><span class="sxs-lookup"><span data-stu-id="a0158-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="a0158-233">نفس الوقت معبر عنه كنسبه مئوية من إجمالي الوقت المستغرق في تكوين الإخراج بأكمله</span><span class="sxs-lookup"><span data-stu-id="a0158-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![صفحة مصمم التنسيق‬ في خدمات التكوين التنظيمية](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="a0158-235">أغلق صفحة **مصمم التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="a0158-235">Close **Format designer** page.</span></span>

### <a id='use-trace'></a><span data-ttu-id="a0158-236">استخدام تتبع الأداء للتحليل في خدمات التكوين التنظمية - تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="a0158-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="a0158-237">في خدمات التكوين التنظيمية، في صفحة **التكوينات**، في شجرة التكوين، حدد عنصر **تعيين تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="a0158-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="a0158-238">في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="a0158-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="a0158-239">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="a0158-239">Select **Designer**.</span></span>
4. <span data-ttu-id="a0158-240">في صفحة **مصمم تعيين النموذج**، في جزء الإجراءات، حدد **تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="a0158-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="a0158-241">حدد التتبع الذي قمت باستيراده سابقًا.</span><span class="sxs-lookup"><span data-stu-id="a0158-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="a0158-242">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a0158-242">Select **OK**.</span></span>

<span data-ttu-id="a0158-243">لاحظ أن المعلومات الجديدة تصبح متوفرة لبعض عناصر مصدر البيانات الخاصة بتعيين الطراز الحالي:</span><span class="sxs-lookup"><span data-stu-id="a0158-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="a0158-244">الوقت الفعلي الذي استغرقه إحضار البيانات باستخدام مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="a0158-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="a0158-245">نفس الوقت معبر عنه كنسبة مئوية من إجمالي الوقت المستغرق في تشغيل تعيين النموذج بالكامل</span><span class="sxs-lookup"><span data-stu-id="a0158-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="a0158-246">لاحظ أنه تقوم التقارير الإلكترونية بإعلامك بأن تعيين النموذج الحالي يكرر طلبات قاعدة البيانات بينما يتم تشغيل مصدر بيانات VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span><span class="sxs-lookup"><span data-stu-id="a0158-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="a0158-247">يحدث هذا التكرار نظرًا لاستدعاء قائمة حركات المورد مرتين لكل سجل مورد تم تكراره:</span><span class="sxs-lookup"><span data-stu-id="a0158-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="a0158-248">يتم اجراء استدعاء واحد لإدخال تفاصيل كل حركة في نموذج البيانات، استنادا إلى الروابط التي تم تكوينها.</span><span class="sxs-lookup"><span data-stu-id="a0158-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="a0158-249">يتم إجراء مكالمة واحده لإدخال العدد المحسوب للحركات لكل مورد في نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="a0158-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![رسالة حول طلبات قواعد البيانات المكررة في صفحة مصمم تعيينات النماذج في خدمات التكوين التنظيمية](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="a0158-251">تشير القيمة **\[Q:530\]** إلى أنه تم استدعاء جدول VendTrans بعدد 530 مرة لإرجاع لعرض سحل من هذا الجدول لمصدر بيانات /\<Relations/VendTrans.VendTable\_AccountNum.</span><span class="sxs-lookup"><span data-stu-id="a0158-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="a0158-252">تشير القيمة **\[530\]** إلى استدعاء مصدر بيانات VendTable/\<Relations/VendTrans.VendTable\_AccountNum بعدد 530 مرة لعرض سجل من مصدر البيانات وإدخال التفاصيل منها في نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="a0158-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="a0158-253">نوصيك باستخدام التخزين المؤقت لمصدر بيانات VendTable/\<Relations/VendTrans.VendTable\_AccountNum للحد من عدد الاستدعاءات التي تم إجراؤها للحصول على تفاصيل 265 حركة وللمساعدة في تحسين أداء تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="a0158-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="a0158-254">قد يكون من المفيد أيضًا تقليل عدد المكالمات التي يتم إجراؤها لمصدر بيانات LedgerTransTypeList.</span><span class="sxs-lookup"><span data-stu-id="a0158-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="a0158-255">يتم استخدام مصدر البيانات هذا لإقران كل قيمة لتعداد **LedgerTransType** بالتسمية الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="a0158-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="a0158-256">باستخدام مصدر البيانات هذا، يمكنك العثور على تسمية مناسبة وإدخالها في نموذج البيانات لكل حركة مورد.</span><span class="sxs-lookup"><span data-stu-id="a0158-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="a0158-257">عدد الاستدعاءات الحالي لمصدر البيانات هذا (9,027) مرتفع جدًا لـ 265 حركة.</span><span class="sxs-lookup"><span data-stu-id="a0158-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![صفحة مصمم تعيين النموذج في خدمات التكوين التنظيمية تعرض 9,027 استدعاء لمصدر البيانات](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="a0158-259">تحسين تعيين النموذج استنادًا إلى المعلومات الواردة من تتبع التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a0158-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="a0158-260">تعديل منطق تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="a0158-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="a0158-261">اتبع الخطوات التالية لاستخدام التخزين المؤقت، للمساعدة في منع الاستدعاءات المكررة لقاعدة البيانات:</span><span class="sxs-lookup"><span data-stu-id="a0158-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="a0158-262">في خدمات التكوين التنظيمية، في صفحة **مصمم تعيين النموذج**، في جزء **مصادر البيانات**، حدد عنصر **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="a0158-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="a0158-263">حدد **ذاكرة التخزين المؤقت**.</span><span class="sxs-lookup"><span data-stu-id="a0158-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="a0158-264">قم بتوسيع عنصر **VendTable**، وقم بتوسيع قائمة العلاقات بين الواحد والعديد لمصدر بيانات VendTable (عنصر **\<العلاقات**)، وحدد عنصر **VendTrans.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="a0158-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="a0158-265">حدد **ذاكرة التخزين المؤقت**.</span><span class="sxs-lookup"><span data-stu-id="a0158-265">Select **Cache**.</span></span>

    ![إعداد التخزين المؤقت للمساعدة على منع المكالمات المتكررة](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="a0158-267">اتبع هذه الخطوات لإحضار مصدر بيانات LedgerTransTypeList إلى نطاق مصدر بيانات VendTable:</span><span class="sxs-lookup"><span data-stu-id="a0158-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="a0158-268">في حزء **انواع مصادر البيانات**، قم بتوسيع عنصر **الوظائف**، وحدد عنصر **الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="a0158-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="a0158-269">في جزء **مصادر البيانات**، حدد عنصر **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="a0158-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="a0158-270">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="a0158-270">Select **Add**.</span></span>
    4. <span data-ttu-id="a0158-271">في حقل **الاسم**، حدد **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="a0158-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="a0158-272">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="a0158-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="a0158-273">في حقل **المعادلة**، أدخل **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="a0158-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="a0158-274">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a0158-274">Select **Save**.</span></span>
    8. <span data-ttu-id="a0158-275">أغلق صفحة **محرر المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="a0158-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="a0158-276">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a0158-276">Click **OK**.</span></span>

3. <span data-ttu-id="a0158-277">اتبع الخطوات التالية للقيام بالتخزين المؤقت في حقل **\$TransType**:</span><span class="sxs-lookup"><span data-stu-id="a0158-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="a0158-278">حدد عنصر **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="a0158-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="a0158-279">حدد **ذاكرة التخزين المؤقت**.</span><span class="sxs-lookup"><span data-stu-id="a0158-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="a0158-280">حدد صنف **VendTable.\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="a0158-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="a0158-281">حدد **ذاكرة التخزين المؤقت**.</span><span class="sxs-lookup"><span data-stu-id="a0158-281">Select **Cache**.</span></span>

    ![إعداد التخزين المؤقت لحقل $TransType](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="a0158-283">اتبع الخطوات التالية لتغيير حقل **\$TransTypeRecord** بحيث يبدأ في استخدام حقل **\$TransType** المخزن مؤقتًا:</span><span class="sxs-lookup"><span data-stu-id="a0158-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="a0158-284">في جزء **مصادر البيانات**، قم بتوسيع عنصر **VendTable**، وقم بتوسيع عنصر **\<العلاقات**، وقم بتوسيع عنصر **VendTrans.VendTable\_AccountNum**، وحدد عنصر **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.</span><span class="sxs-lookup"><span data-stu-id="a0158-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="a0158-285">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="a0158-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="a0158-286">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="a0158-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="a0158-287">في حقل **المعادلة**، ابحث عن التعبير التالي:</span><span class="sxs-lookup"><span data-stu-id="a0158-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="a0158-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="a0158-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="a0158-289">في حقل **المعادلة**، ابحث عن التعبير التالي:</span><span class="sxs-lookup"><span data-stu-id="a0158-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="a0158-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="a0158-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="a0158-291">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a0158-291">Select **Save**.</span></span>
    7. <span data-ttu-id="a0158-292">أغلق صفحة **محرر المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="a0158-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="a0158-293">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a0158-293">Select **OK**.</span></span>

5. <span data-ttu-id="a0158-294">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a0158-294">Select **Save**.</span></span>
6. <span data-ttu-id="a0158-295">أغلق صفحة **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="a0158-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="a0158-296">أغلق صفحة **تعيينات النماذج**.</span><span class="sxs-lookup"><span data-stu-id="a0158-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="a0158-297">إكمال الإصدار المعدل من تعيين طراز التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a0158-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="a0158-298">في خدمات التكوين التنظيمية، في صفحة **التكوينات**، في علامة التبويب السريع **الإصدارات**، حدد الإصدار **1.2** في تكوين **تعيين تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="a0158-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="a0158-299">حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="a0158-299">Select **Change status**.</span></span>
3. <span data-ttu-id="a0158-300">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="a0158-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-finance-and-operations"></a><span data-ttu-id="a0158-301">استيراد تكوين تعيين نموذج التقارير الإلكترونية المعدل من خدمات التكوين التنظيمية إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a0158-301">Import the modified ER model mapping configuration from RCS into Finance and Operations</span></span>

<span data-ttu-id="a0158-302">كرر الخطوات الموجودة في قسم [استيراد تكوين التقارير الإلكترونية من خدمة التكوين التنظيمية إلى Finance and Operations‬](#import-configuration) من قبل في هذا الموضوع لاستيراد الإصدار 1.2 من تكوين **تعيين تتبع الأداء** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a0158-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration into Finance and Operations.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="a0158-303">تشغيل حل التقارير الإلكترونية المعدل لتتبع التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a0158-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="a0158-304">تشغيل تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a0158-304">Run the ER format</span></span>

<span data-ttu-id="a0158-305">كرر الخطوات الموجودة في قسم [تشغيل تنسيق التقارير الإلكترونية](#run-format) من قبل في هذا الموضوع لإنشاء تتبع أداء جديد.</span><span class="sxs-lookup"><span data-stu-id="a0158-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="a0158-306">مراجعه تتبع التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a0158-306">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-finance-and-operations"></a><span data-ttu-id="a0158-307">تصدير التتبع الذي تم إنشاؤه من Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a0158-307">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="a0158-308">كرر الخطوات الموجودة في قسم [تصدير التتبع الذي تم إنشاؤه من Finance and Operations‬](#export-trace) من قبل في هذا الموضوع لحفظ تتبع أداء جديد محليًا.</span><span class="sxs-lookup"><span data-stu-id="a0158-308">Repeat the steps in the [Export the generated trace from Finance and Operations](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="a0158-309">استيراد التتبع الذي تم إنشاؤه في خدمة التكوين التنظيمية</span><span class="sxs-lookup"><span data-stu-id="a0158-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="a0158-310">كرر الخطوات الموجودة في قسم [استيراد التتبع الذي تم إنشاؤه في خدمة التكوين التنظيمية‬](#import-trace) من قبل هذا الموضوع لاستيراد عملية تتبع الأداء الجديدة إلى خدمات التكوين التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="a0158-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="a0158-311">استخدام تتبع الأداء للتحليل في خدمات التكوين التنظمية - تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="a0158-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="a0158-312">كرر الخطوات الموجودة في قسم [استخدام تتبع الأداء للتحليل في خدمات التكوين التنظمية - تعيين النموذج](#use-trace) من قبل في هذا الموضوع لتحليل آخر تتبع للأداء.</span><span class="sxs-lookup"><span data-stu-id="a0158-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="a0158-313">لاحظ أن التسويات التي أجريتها على تعيين النموذج قد تقوم بإزالة الاستعلامات المكررة لقاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="a0158-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="a0158-314">يتم أيضًا تقليل عدد الاستدعاءات إلى جداول قاعدة البيانات ومصادر البيانات لتعيين هذا النموذج.</span><span class="sxs-lookup"><span data-stu-id="a0158-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="a0158-315">وبالتالي، تم تحسين أداء حل التقارير الإلكترونية بالكامل.</span><span class="sxs-lookup"><span data-stu-id="a0158-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![تتبع معلومات مصدر بيانات VendTable في صفحة مصمم تعيين النموذج في خدمات التكوين التنظيمية](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="a0158-317">في معلومات التتبع، تشير القيمة **\[12\]** الخاصة بمصدر بيانات VendTable إلى أن مصدر البيانات هذا تم استدعاؤه 12 مرة.</span><span class="sxs-lookup"><span data-stu-id="a0158-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="a0158-318">تشير القيمة**\[Q:6\]** إلى أنه تمت ترجمة ست استدعاءات إلى استدعاءات قاعدة البيانات لجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="a0158-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="a0158-319">تشير القيمة **\[C:6\]** إلى أنه تم تخزين السجلات التي تم إحضارها من قاعده البيانات مؤقتًا، وتمت معالجة ست استدعاءات أخرى باستخدام ذاكرة التخزين المؤقت.</span><span class="sxs-lookup"><span data-stu-id="a0158-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="a0158-320">لاحظ أنه تم تقليل عدد الاستدعاءات إلى مصدر بيانات LedgerTransTypeList من 9,027 إلى 240.</span><span class="sxs-lookup"><span data-stu-id="a0158-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![تتبع معلومات مصدر بيانات LedgerTransTypeList في صفحة مصمم تعيين النموذج في خدمات التكوين التنظيمية](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-finance-and-operations"></a><span data-ttu-id="a0158-322">مراجعه تتبع التنفيذ في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a0158-322">Review the execution trace in Finance and Operations</span></span>

<span data-ttu-id="a0158-323">بالاضافه إلى خدمات التكوين التنظمية، قد توفر بعض إصدارات Finance and Operations إمكانات لتجربة مصمم إطار التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a0158-323">In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="a0158-324">تشتمل هذه الإصدارات من Finance and Operations على خيار **تمكين وضع التصميم** الذي يمكن تشغيله.</span><span class="sxs-lookup"><span data-stu-id="a0158-324">These versions of Finance and Operations have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="a0158-325">يمكنك العثور على هذا الخيار في علامة التبويب **عام** في صفحة **معلمات التقارير الإلكترونية**، التي يمكنك فتحها من مساحة عمل **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="a0158-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![تمكين خيار وضع التصميم في صفحة معلمات التقارير الإلكترونية في Finance and Operations](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="a0158-327">في حاله استخدام أحد هذه الإصدارات من Finance and Operations، يمكنك تحليل تفاصيل تتبعات الأداء التي يتم إنشاؤها مباشرة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a0158-327">If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</span></span> <span data-ttu-id="a0158-328">وليس من الضروري أن تقوم بتصديرها من Finance and Operations واستيرادها في خدمات التكوين التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="a0158-328">You don't have to export them from Finance and Operation and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="a0158-329">مراجعة تتبع التنفيذ باستخدام الأدوات الخارجية</span><span class="sxs-lookup"><span data-stu-id="a0158-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="a0158-330">تكوين معلمات المستخدمين</span><span class="sxs-lookup"><span data-stu-id="a0158-330">Configure user parameters</span></span>

1. <span data-ttu-id="a0158-331">في Finance and Operations، انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية\> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="a0158-331">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="a0158-332">في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="a0158-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="a0158-333">في مربع الحوار **معلمات المستخدمين**، في قسم **تتبع التنفيذ**، في حقل **تنسيق تتبع التنفيذ**، حدد **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="a0158-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="a0158-334">تشغيل تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a0158-334">Run the ER format</span></span>

<span data-ttu-id="a0158-335">كرر الخطوات الموجودة في قسم [تشغيل تنسيق التقارير الإلكترونية](#run-format) من قبل في هذا الموضوع لإنشاء تتبع أداء جديد.</span><span class="sxs-lookup"><span data-stu-id="a0158-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="a0158-336">لاحظ أن مستعرض الويب يعرض ملفًا من نوع zip للتنزيل.</span><span class="sxs-lookup"><span data-stu-id="a0158-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="a0158-337">يحتوي هذا الملف على تتبع الأداء بتنسيق PerfView.</span><span class="sxs-lookup"><span data-stu-id="a0158-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="a0158-338">يمكنك بعد ذلك استخدام أداه تحليل أداء PerfView لتحليل تفاصيل تنفيذ تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a0158-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>
