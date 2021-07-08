---
title: تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها
description: يوفر هذا الموضوع معلومات حول كيفية استخدام ميزة تتبع الأداء في التقارير الإلكترونية (ER) لاستكشاف مشكلات الأداء وإصلاحها.
author: NickSelin
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7fbec962fea374afdbabaad48a42dad380708678
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295563"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="9c93a-103">تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="9c93a-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9c93a-104">كجزء من عملية تصميم تكوينات التقارير الإلكترونية (ER) لإنشاء مستندات إلكترونية، يمكنك تحديد الطريقة المستخدمة للحصول على البيانات من التطبيق وإدخالها في الإخراج الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="9c93a-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="9c93a-105">تساعد ميزة تتبع أداء التقارير الإلكترونية في تقليل الوقت والتكلفة بشكل كبير في جمع تفاصيل تنفيذ تنسيق التقارير الإلكترونية واستخدامها لاستكشاف مشكلات الأداء وإصلاحها.</span><span class="sxs-lookup"><span data-stu-id="9c93a-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="9c93a-106">يوفر هذا البرنامج التعليمي إرشادات حول كيفية أخذ تتبعات الأداء لتنسيقات التقارير الإلكترونية المنفذة، وكيفية استخدام المعلومات من هذه التتبعات للمساعدة في تحسين الأداء.</span><span class="sxs-lookup"><span data-stu-id="9c93a-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9c93a-107">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="9c93a-107">Prerequisites</span></span>

<span data-ttu-id="9c93a-108">لإكمال الأمثلة في هذا البرنامج التعليمي، يجب أن يكون لديك الوصول التالي:</span><span class="sxs-lookup"><span data-stu-id="9c93a-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="9c93a-109">الوصول إلى أحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="9c93a-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="9c93a-110">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="9c93a-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="9c93a-111">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="9c93a-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="9c93a-112">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="9c93a-112">System administrator</span></span>

- <span data-ttu-id="9c93a-113">يمكنك الوصول إلى مثيل خدمات التكوين التنظيمية (RCS) التي تم توفيرها لنفس المستأجر مثل التطبيق، لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="9c93a-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="9c93a-114">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="9c93a-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="9c93a-115">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="9c93a-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="9c93a-116">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="9c93a-116">System administrator</span></span>

<span data-ttu-id="9c93a-117">يجب عليك أيضًا تنزيل الملفات التالية وتخزينها محليًا.</span><span class="sxs-lookup"><span data-stu-id="9c93a-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="9c93a-118">ملف</span><span class="sxs-lookup"><span data-stu-id="9c93a-118">File</span></span>                                  | <span data-ttu-id="9c93a-119">المحتوى</span><span class="sxs-lookup"><span data-stu-id="9c93a-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="9c93a-120">إصدار نموذج تتبع الأداء رقم 1</span><span class="sxs-lookup"><span data-stu-id="9c93a-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="9c93a-121">تكوين نموذج عينة بيانات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="9c93a-121">Sample ER data model configuration</span></span>](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| <span data-ttu-id="9c93a-122">إصدار بيانات تعريف تتبع الأداء رقم 1</span><span class="sxs-lookup"><span data-stu-id="9c93a-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="9c93a-123">تكوين بيانات تعريف عينة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="9c93a-123">Sample ER metadata configuration</span></span>](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| <span data-ttu-id="9c93a-124">إصدار تعيين تتبع الأداء رقم 1.1</span><span class="sxs-lookup"><span data-stu-id="9c93a-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="9c93a-125">تكوين تعيين نموذج عينة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="9c93a-125">Sample ER model mapping configuration</span></span>](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| <span data-ttu-id="9c93a-126">إصدار تنسيق تتبع الأداء رقم 1.1</span><span class="sxs-lookup"><span data-stu-id="9c93a-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="9c93a-127">تكوين تنسيق عينة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="9c93a-127">Sample ER format configuration</span></span>](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="9c93a-128">تكوين معلمات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="9c93a-128">Configure ER parameters</span></span>

<span data-ttu-id="9c93a-129">يتم تخزين كل تتبع أداء تقارير إلكترونية يتم إنشاؤه في التطبيق كمرفق بسجل تسجيل التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="9c93a-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="9c93a-130">يُستخدم إطار إدارة المستندات (DM) لإدارة هذه المرفقات.</span><span class="sxs-lookup"><span data-stu-id="9c93a-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="9c93a-131">يجب تكوين معلمات التقارير الإلكترونية مسبقًا، لتحديد نوع مستند إدارة المستندات (DM) الذي يجب استخدامه لإرفاق تتبعات الأداء.</span><span class="sxs-lookup"><span data-stu-id="9c93a-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="9c93a-132">في مساحة عمل **إعداد التقارير الإلكترونية**، حدد **معلمات ‏‫إعداد التقارير الإلكترونية‬**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="9c93a-133">ثم في صفحة **معلمات التقارير الإلكترونية**، ضمن علامة التبويب **مرفقات**، في حقل **أخرى**، حدد نوع مستند إدارة المستندات الذي سيتم استخدامه لتتبعات الأداء.</span><span class="sxs-lookup"><span data-stu-id="9c93a-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![صفحة معلمات التقارير الإلكترونية](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="9c93a-135">لتوفيره في حقل البحث **أخرى**، يجب تكوين نوع مستند إدارة المستندات بالطريقة التالية في صفحة **أنواع المستندات** (**إدارة المؤسسة\>إدارة المستندات\>أنواع المستندات**):</span><span class="sxs-lookup"><span data-stu-id="9c93a-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="9c93a-136">**الفئة:** إرفاق ملف</span><span class="sxs-lookup"><span data-stu-id="9c93a-136">**Class:** Attach file</span></span>
- <span data-ttu-id="9c93a-137">**المجموعة** : ملف</span><span class="sxs-lookup"><span data-stu-id="9c93a-137">**Group:** File</span></span>

![صفحة أنواع المستندات](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="9c93a-139">يجب أن يكون نوع المستند المحدد متاحًا في كل شركة من المثيل الحالي، لأن مرفقات إدارة المستندات خاصة بالشركة.</span><span class="sxs-lookup"><span data-stu-id="9c93a-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="9c93a-140">تكوين معلمات خدمات التكوين التنظيمية (RCS)</span><span class="sxs-lookup"><span data-stu-id="9c93a-140">Configure RCS parameters</span></span>

<span data-ttu-id="9c93a-141">سيتم استيراد تتبعات أداء التقارير الإلكترونية التي تم إنشاؤها إلى خدمات التكوين التنظيمية (RCS) للتحليل باستخدام مصمم التنسيق الخاص بالتقارير الإلكترونية ومصمم تعيينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9c93a-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="9c93a-142">نظرًا لأنه يتم تخزين تتبعات أداء التقارير الإلكترونية كمرفقات لسجل تسجيل التنفيذ المرتبط بتنسيق التقارير الإلكترونية، يجب عليك تكوين معلمات خدمات التكوين التنظيمية مسبقًا، لتحديد نوع مستند إدارة المستندات الذي يجب استخدامه لإرفاق تتبعات الأداء.</span><span class="sxs-lookup"><span data-stu-id="9c93a-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="9c93a-143">في مثيل خدمات التكوين التنظيمية (RCS) الذي تم توفيره للشركة الخاصة بك، في مساحة عمل **التقارير الإلكترونية**، حدد **معلمات التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="9c93a-144">ثم في صفحة **معلمات التقارير الإلكترونية**، ضمن علامة التبويب **مرفقات**، في حقل **أخرى**، حدد نوع مستند إدارة المستندات الذي سيتم استخدامه لتتبعات الأداء.</span><span class="sxs-lookup"><span data-stu-id="9c93a-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![صفحة معلمات التقارير الإلكترونية في خدمات التكوين التنظيمية](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="9c93a-146">لتوفيره في حقل البحث **أخرى**، يجب تكوين نوع مستند إدارة المستندات بالطريقة التالية في صفحة **أنواع المستندات** (**إدارة المؤسسة\>إدارة المستندات\>أنواع المستندات**):</span><span class="sxs-lookup"><span data-stu-id="9c93a-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="9c93a-147">**الفئة:** إرفاق ملف</span><span class="sxs-lookup"><span data-stu-id="9c93a-147">**Class:** Attach file</span></span>
- <span data-ttu-id="9c93a-148">**المجموعة** : ملف</span><span class="sxs-lookup"><span data-stu-id="9c93a-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="9c93a-149">تصميم حل تقارير إلكترونية</span><span class="sxs-lookup"><span data-stu-id="9c93a-149">Design an ER solution</span></span>

<span data-ttu-id="9c93a-150">افترض انك قمت بالبدء بتصميم حل جديد للتقارير الإلكترونية لإنشاء تقرير جديد يقدم حركات المورد.</span><span class="sxs-lookup"><span data-stu-id="9c93a-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="9c93a-151">في الوقت الحالي، يمكنك العثور علي حركات مورد محدد في **حركات الموردين** (انتقل إلى **الحساب المستحق\> الموردين\> جميع الموردين**، وحدد موردًا، ثم في جزء الإجراءات، في علامة التبويب **مود**، في مجموعة **الحركات**، حدد **الحركات**).</span><span class="sxs-lookup"><span data-stu-id="9c93a-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="9c93a-152">ومع ذلك، فأنت تريد أن يكون لديك كل حركة بائع في نفس الوقت في مستند إلكتروني واحد بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="9c93a-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="9c93a-153">سيتألف هذا الحل من العديد من تكوينات التقارير الإلكترونية التي تحتوي على مكونات نموذج البيانات وبيانات التعريف ورسم الخرائط ومكونات التنسيق المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="9c93a-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="9c93a-154">سجل الدخول إلى مثيل خدمات التكوين التنظيمية الذي تم توفيره لشركتك.</span><span class="sxs-lookup"><span data-stu-id="9c93a-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="9c93a-155">في هذا البرنامج التعليمي، ستقوم بإنشاء وتعديل تكوينات لعينة الشركة **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="9c93a-156">لذلك، تأكد من إضافة موفر التكوين هذا إلى خدمة التكوين التنظيمية وتحديده نشطًا.</span><span class="sxs-lookup"><span data-stu-id="9c93a-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="9c93a-157">للحصول علي الإرشادات، راجع [إنشاء موفري التكوين ووضع علامة عليهم كنشطين](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="9c93a-157">For instructions, see the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>
3. <span data-ttu-id="9c93a-158">في مساحة عمل **إعداد التقارير الإلكترونية**، حدد الإطار المتجانب **تكوينات إعداد التقارير**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="9c93a-159">في صفحة **التكوينات**، قم باستيراد تكوينات التقارير الإلكترونية التي قمت بتنزيلها كشرط مسبق في خدمة التكوين التنظيمية، بالترتيب التالي: نموذج البيانات، وبيانات التعريف، وتعيين النموذج، والتنسيق.</span><span class="sxs-lookup"><span data-stu-id="9c93a-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="9c93a-160">بالنسبة لكل تكوين، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="9c93a-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="9c93a-161">في جزء الإجراءات، حدد **تبادل \> تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="9c93a-162">حدد **استعراض** لتحديد الملف المناسب لتكوين التقارير الإلكترونية المطلوب بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="9c93a-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="9c93a-163">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-163">Select **OK**.</span></span>

    ![صفحة التكوينات في خدمة التكوين التنظيمية](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="9c93a-165">تشغيل حل التقارير الإلكترونية لتتبع التنفيذ</span><span class="sxs-lookup"><span data-stu-id="9c93a-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="9c93a-166">افترض أنك قمت بالانتهاء من تصميم الإصدار الأول لحل التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9c93a-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="9c93a-167">وتريد الآن اختبارها في المثيل الخاص بك وتحليل أداء التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="9c93a-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a><span data-ttu-id="9c93a-168">استيراد تكوين التقارير الإلكترونية من RCS إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9c93a-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="9c93a-169">قم بتسجيل الدخول إلى مثيل التطبيق.</span><span class="sxs-lookup"><span data-stu-id="9c93a-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="9c93a-170">بالنسبة لهذا البرنامج التعليمي، ستقوم باستيراد التكوينات من مثيل خدمة التكوين التنظيمية الخاص بك (حيث تقوم بتصميم مكونات التقارير الإلكترونية الخاصة بك) في المثيل (حيث تقوم باختبارها وأخيرًا استخدامها).</span><span class="sxs-lookup"><span data-stu-id="9c93a-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="9c93a-171">ولذلك، يجب التأكد من إعداد كافة النتائج الملموسة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="9c93a-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="9c93a-172">لمزيد من المعلومات، راجع إجراء [استيراد تكوينات التقارير الإلكترونية من خدمات التكوين التنظيمية (RCS)](rcs-download-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="9c93a-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md) procedure.</span></span>
3. <span data-ttu-id="9c93a-173">اتبع الخطوات التالية لاستيراد التكوينات من خدمات التكوين التنظيمية إلى التطبيق:</span><span class="sxs-lookup"><span data-stu-id="9c93a-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="9c93a-174">في مساحة عمل **التقارير الإلكترونية**، وفي تجانب موفر تكوين **Litware, Inc.**، حدد **المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="9c93a-175">في صفحة **مستودع التكوين**، حدد المستودع من **خدمات التكوين التنظيمية**، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="9c93a-176">في علامة التبويب **التكوينات**، حدد تكوين **تنسيق تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="9c93a-177">في علامة التبويب السريع **الإصدارات**، حدد الإصدار **1.1** من التكوين المحدد، ثم حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![صفحة مستودع التكوين](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="9c93a-179">يتم تلقائيا استيراد الإصدارات المقابلة من نموذج البيانات وتكوينات تعيين النموذج كمتطلبات مسبقة لتكوين تنسيق التقارير الإلكترونية المستورد.</span><span class="sxs-lookup"><span data-stu-id="9c93a-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="9c93a-180">تشغيل تتبع أداء التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="9c93a-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="9c93a-181">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="9c93a-182">في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="9c93a-183">في مربع الحوار **معلمات المستخدمين**، في قسم **تتبع التنفيذ**، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="9c93a-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="9c93a-184">في الحقل **تنسيق تتبع التنفيذ**، حدد تنسيق تتبع الأداء الذي تم إنشاؤه بحيث يجب تخزين تفاصيل التنفيذ بتنسيق التقارير الإلكترونية وعناصر التعيينات:</span><span class="sxs-lookup"><span data-stu-id="9c93a-184">In the **Execution trace format** field, specify the format of the generated performance trace that the execution details should be stored in for ER format and mapping elements:</span></span>

        - <span data-ttu-id="9c93a-185">**تنسيق تتبع الأخطاء** – حدد هذه القيمة إذا كنت تخطط لتشغيل تنسيق التقارير الإلكترونية الذي يحتوي على وقت تنفيذ قصير بشكل تفاعلي.</span><span class="sxs-lookup"><span data-stu-id="9c93a-185">**Debug trace format** – Select this value if you plan to interactively run an ER format that has a short execution time.</span></span> <span data-ttu-id="9c93a-186">يتم بعد ذلك بدء مجموعة التفاصيل المتعلقة بتنفيذ تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9c93a-186">The collection of details about ER format execution is then started.</span></span> <span data-ttu-id="9c93a-187">عند تحديد هذه القيمة، يقوم تتبع الأداء بجمع معلومات حول الوقت الذي يتم إنفاقه على الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="9c93a-187">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="9c93a-188">تشغيل كل مصدر بيانات في تعيين النموذج الذي تم استدعاؤه للحصول على البيانات</span><span class="sxs-lookup"><span data-stu-id="9c93a-188">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="9c93a-189">معالجة كل عنصر تنسيق لإدخال البيانات في الإخراج الذي يتم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="9c93a-189">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="9c93a-190">إذا قمت بتحديد القيمة **تنسيق تتبع الأخطاء**، يمكنك تحليل محتوى التتبع في مصمم عمليات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9c93a-190">If you select the **Debug trace format** value, you can analyze the content of the trace in the ER Operation designer.</span></span> <span data-ttu-id="9c93a-191">هناك، يمكنك عرض تنسيق التقارير الإلكترونية أو تعيين عناصر التعيين المذكورة في التتبع.</span><span class="sxs-lookup"><span data-stu-id="9c93a-191">There, you can view the ER format or mapping elements that are mentioned in the trace.</span></span>

        - <span data-ttu-id="9c93a-192">**تنسيق التتبع المجمع** – حدد هذه القيمة إذا كنت تخطط لتشغيل تنسيق التقارير الإلكترونية الذي يحتوي على وقت تنفيذ طويل بشكل تفاعلي.</span><span class="sxs-lookup"><span data-stu-id="9c93a-192">**Aggregated trace format** – Select this value if you plan to run an ER format that has a long execution time in batch mode.</span></span> <span data-ttu-id="9c93a-193">يتم بعد ذلك بدء مجموعة التفاصيل المجمعة المتعلقة بتنفيذ تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9c93a-193">The collection of the aggregated details about ER format execution is then started.</span></span> <span data-ttu-id="9c93a-194">عند تحديد هذه القيمة، يقوم تتبع الأداء بجمع معلومات حول الوقت الذي يتم إنفاقه على الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="9c93a-194">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="9c93a-195">تشغيل كل مصدر بيانات في تعيين النموذج الذي تم استدعاؤه للحصول على البيانات</span><span class="sxs-lookup"><span data-stu-id="9c93a-195">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="9c93a-196">تشغيل كل مصدر بيانات في تعيين التنسيق الذي تم استدعاؤه للحصول على البيانات</span><span class="sxs-lookup"><span data-stu-id="9c93a-196">Running each data source in the format mapping that is called to get data</span></span>
            - <span data-ttu-id="9c93a-197">معالجة كل عنصر تنسيق لإدخال البيانات في الإخراج الذي يتم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="9c93a-197">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="9c93a-198">تتوفر قيمة **تنسيق التتبع المجمع** في Microsoft Dynamics 365 Finance الإصدار 10.0.20 والإصدارات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="9c93a-198">The **Aggregated trace format** value is available in Microsoft Dynamics 365 Finance version 10.0.20 and later.</span></span>

            <span data-ttu-id="9c93a-199">في مصمم التنسيق الخاص بالتقارير الإلكترونية ومصمم تعيين نموذج التقارير الإلكترونية، يمكنك عرض إجمالي وقت التنفيذ لمكون واحد.</span><span class="sxs-lookup"><span data-stu-id="9c93a-199">In the ER format designer and ER model mapping designer, you can view the total execution time for a single component.</span></span> <span data-ttu-id="9c93a-200">بالإضافة إلى ذلك، يحتوي التتبع على تفاصيل حول التنفيذ، مثل عدد عمليات التنفيذ، والحد الأدنى والحد الأقصى لوقت تنفيذ واحد.</span><span class="sxs-lookup"><span data-stu-id="9c93a-200">Additionally, the trace contains details about the execution, such as the number of executions, and the minimum and maximum time of a single execution.</span></span>

            > [!NOTE]
            > <span data-ttu-id="9c93a-201">يتم تجميع هذا التتبع استنادًا إلى مسار المكونات التي تم تتبعها.</span><span class="sxs-lookup"><span data-stu-id="9c93a-201">This trace is collected based on the traced components path.</span></span> <span data-ttu-id="9c93a-202">لذلك، قد تكون الإحصائيات غير صحيحة عندما يحتوي مكون أصلي مفرد على عدة مكونات فرعية غير مسماه، أو عندما يكون لعدة مكونات تابعة الاسم نفسه.</span><span class="sxs-lookup"><span data-stu-id="9c93a-202">Therefore, the statistics might be incorrect when a single parent component contains several unnamed child components, or when several child components have the same name.</span></span>

    2. <span data-ttu-id="9c93a-203">قم بتعيين الخيارات التالية إلى **نعم** لجمع التفاصيل الخاصة بتنفيذ تعيين نموذج التقارير الإلكترونية ومكونات تنسيق التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="9c93a-203">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="9c93a-204">**جمع إحصاءات الاستعلام** – عند تشغيل هذا الخيار، سيقوم تتبع الأداء بجمع المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="9c93a-204">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="9c93a-205">عدد استدعاءات قواعد البيانات التي تم إجراؤها بواسطة مصادر البيانات</span><span class="sxs-lookup"><span data-stu-id="9c93a-205">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="9c93a-206">عدد الاستدعاءات المتكررة لقاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="9c93a-206">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="9c93a-207">تفاصيل بيانات SQL التي تم استخدامها لإجراء استدعاءات قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="9c93a-207">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="9c93a-208">**تتبع الوصول إلى التخزين المؤقت** – عند تشغيل هذا الخيار، سيقوم تتبع الأداء بجمع معلومات حول استخدام ذاكره التخزين المؤقت لتعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9c93a-208">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="9c93a-209">**الوصول إلى بيانات التتبع** - عند تشغيل هذا الخيار، سيقوم تتبع الأداء بجمع معلومات حول عدد الاستدعاءات إلى قاعدة البيانات لمصادر البيانات المنفذة الخاصة بنوع قائمة السجلات.</span><span class="sxs-lookup"><span data-stu-id="9c93a-209">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="9c93a-210">**تتبع تعداد القائمة‬** - عند تشغيل هذا الخيار، سيقوم تتبع الأداء بجمع معلومات حول عدد السجلات التي تم طلبها من مصادر البيانات الخاصة بنوع قائمة السجلات.</span><span class="sxs-lookup"><span data-stu-id="9c93a-210">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9c93a-211">وتكون المحددات الموجودة في مربع الحوار **معلمات المستخدمين** خاصة بالمستخدم والشركة الحالية.</span><span class="sxs-lookup"><span data-stu-id="9c93a-211">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![مربع علامة تبويب معلمات المستخدمين](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a><span data-ttu-id="9c93a-213">تشغيل تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="9c93a-213">Run the ER format</span></span>

1. <span data-ttu-id="9c93a-214">قم بتحديد شركة **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-214">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="9c93a-215">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-215">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="9c93a-216">في صفحة **التكوينات**، في شجرة التكوين، حدد عنصر **تنسيق تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-216">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="9c93a-217">في جزء الإجراءات، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-217">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="9c93a-218">لاحظ أن الملف الذي تم إنشاؤه يقدم معلومات حول 265 حركة لستة موردين.</span><span class="sxs-lookup"><span data-stu-id="9c93a-218">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="9c93a-219">مراجعه تتبع التنفيذ</span><span class="sxs-lookup"><span data-stu-id="9c93a-219">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a><span data-ttu-id="9c93a-220">تصدير التتبع الذي تم إنشاؤه من التطبيق</span><span class="sxs-lookup"><span data-stu-id="9c93a-220">Export the generated trace from the application</span></span>

<span data-ttu-id="9c93a-221">يتم فصل تتبعات الأداء من تنسيق التقارير الإلكترونية المصدر ويمكن إجراء تسلسلها إلى ملف مضغوط خارجي.</span><span class="sxs-lookup"><span data-stu-id="9c93a-221">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="9c93a-222">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> سجلات تصحيح التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-222">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="9c93a-223">في صفحة **سجلات تشغيل التقارير الإلكترونية**، في الجزء الأيسر، في حقل **اسم التكوين**، حدد **تنسيق تتبع الأداء** للعثور علي سجلات التسجيل التي تم إنشاؤها بواسطة تنفيذ تكوين **تنسيق تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-223">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="9c93a-224">حدد الزر **المرفقات** (رمز مشبك الورق) في الواوية العلوية اليمنى للصفحة، أو اضغط على **Ctrl+Shift+A**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-224">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![زر المرفقات في صفحة سجلات تشغيل التقارير الإلكترونية](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="9c93a-226">في الصفحة **المرفقات الخاصة بسجلات تشغيل التقارير الإلكترونية**، في جزء الإجراء، حدد **فتح** للحصول علي تتبع الأداء كملف zip وتخزينه محليًا.</span><span class="sxs-lookup"><span data-stu-id="9c93a-226">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![مرفقات لسجلات تشغيل التقارير الإلكترونية](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="9c93a-228">يحتوي التتبع الذي تم إنشاؤه علي مرجع لتقرير التقارير الإلكترونية المصدر من خلال معرف تقرير بتنسيق **GUID** فقط.</span><span class="sxs-lookup"><span data-stu-id="9c93a-228">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="9c93a-229">ترقيم إصدار التنسيق غير مهم.</span><span class="sxs-lookup"><span data-stu-id="9c93a-229">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="9c93a-230">لاحظ أن الاقتران بين تتبع الأداء الذي تم إنشاؤه لتنسيق التقارير الإلكترونية الذي تم تنفيذه وتعيين نموذج التقارير الإلكترونية يستند إلى الواصف الجذر الذي تم استخدامه ونموذج البيانات العامة.</span><span class="sxs-lookup"><span data-stu-id="9c93a-230">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="9c93a-231">ترقيم إصدار التنسيق وتعيين النموذج غير مهم.</span><span class="sxs-lookup"><span data-stu-id="9c93a-231">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="9c93a-232">إن تعيين علامة **الإعداد الافتراضي لتعيين النموذج** لتعيين النموذج غير مهم أيضًا.</span><span class="sxs-lookup"><span data-stu-id="9c93a-232">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a><span data-ttu-id="9c93a-233">استيراد التتبع الذي تم إنشاؤه في خدمة التكوين التنظيمية</span><span class="sxs-lookup"><span data-stu-id="9c93a-233">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="9c93a-234">في خدمة التكوين التنظيمية، في مساحة عمل **إعداد التقارير الإلكترونية**، حدد الإطار المتجانب **تكوينات إعداد التقارير**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-234">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="9c93a-235">في صفحة **التكوينات**، في شجره التكوين، قم بتوسيع نصر **نموذج تتبع الأداء**، وحدد عنصر **تنسيق تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-235">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="9c93a-236">في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-236">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="9c93a-237">في صفحة **مصمم التنسيق**، في جزء الإجراءات، حدد **تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-237">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="9c93a-238">في مربع الحوار **إعدادات نتيجة تتبع الأداء**، حدد **تتبع الأداء المهم**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-238">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="9c93a-239">حدد **استعراض**، ثم حدد ملف zip الذي قمت بتصديره مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="9c93a-239">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="9c93a-240">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-240">Select **OK**.</span></span>

    ![مربع الحوار إعدادات نتيجة تتبع الأداء في خدمة التكوين التنظيمية](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="9c93a-242">استخدام تتبع الأداء للتحليل في خمة التكوين التنظمية - تنفيذ التنسيق</span><span class="sxs-lookup"><span data-stu-id="9c93a-242">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="9c93a-243">في خدمات التكوين التنظيمية، في صفحة **مصمم التنسيق**، حدد **توسيع/طي** لتوسيع محتويات كافة عناصر التنسيق.</span><span class="sxs-lookup"><span data-stu-id="9c93a-243">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="9c93a-244">لاحظ أنه يتم عرض معلومات إضافية لبعض عناصر التنسيق الحالي:</span><span class="sxs-lookup"><span data-stu-id="9c93a-244">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="9c93a-245">الوقت الفعلي الذي استغرقه إدخال البيانات في الإخراج الذي تم إنشاؤه باستخدام عنصر التنسيق</span><span class="sxs-lookup"><span data-stu-id="9c93a-245">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="9c93a-246">نفس الوقت معبر عنه كنسبه مئوية من إجمالي الوقت المستغرق في تكوين الإخراج بأكمله</span><span class="sxs-lookup"><span data-stu-id="9c93a-246">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![صفحة مصمم التنسيق‬ في خدمات التكوين التنظيمية](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="9c93a-248">أغلق صفحة **مصمم التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-248">Close **Format designer** page.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a><span data-ttu-id="9c93a-249">استخدام تتبع الأداء للتحليل في خدمات التكوين التنظمية - تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="9c93a-249">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="9c93a-250">في خدمات التكوين التنظيمية، في صفحة **التكوينات**، في شجرة التكوين، حدد عنصر **تعيين تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-250">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="9c93a-251">في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-251">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="9c93a-252">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-252">Select **Designer**.</span></span>
4. <span data-ttu-id="9c93a-253">في صفحة **مصمم تعيين النموذج**، في جزء الإجراءات، حدد **تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-253">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="9c93a-254">حدد التتبع الذي قمت باستيراده سابقًا.</span><span class="sxs-lookup"><span data-stu-id="9c93a-254">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="9c93a-255">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-255">Select **OK**.</span></span>

<span data-ttu-id="9c93a-256">لاحظ أن المعلومات الجديدة تصبح متوفرة لبعض عناصر مصدر البيانات الخاصة بتعيين الطراز الحالي:</span><span class="sxs-lookup"><span data-stu-id="9c93a-256">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="9c93a-257">الوقت الفعلي الذي استغرقه إحضار البيانات باستخدام مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="9c93a-257">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="9c93a-258">نفس الوقت معبر عنه كنسبة مئوية من إجمالي الوقت المستغرق في تشغيل تعيين النموذج بالكامل</span><span class="sxs-lookup"><span data-stu-id="9c93a-258">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="9c93a-259">لاحظ أنه تقوم التقارير الإلكترونية بإعلامك بأن تعيين النموذج الحالي يكرر طلبات قاعدة البيانات بينما يتم تشغيل مصدر بيانات VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span><span class="sxs-lookup"><span data-stu-id="9c93a-259">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="9c93a-260">يحدث هذا التكرار نظرًا لاستدعاء قائمة حركات المورد مرتين لكل سجل مورد تم تكراره:</span><span class="sxs-lookup"><span data-stu-id="9c93a-260">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="9c93a-261">يتم إجراء استدعاء واحد لإدخال تفاصيل كل حركة في نموذج البيانات، استنادا إلى الروابط التي تم تكوينها.</span><span class="sxs-lookup"><span data-stu-id="9c93a-261">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="9c93a-262">يتم إجراء مكالمة واحده لإدخال العدد المحسوب للحركات لكل مورد في نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="9c93a-262">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![رسالة حول طلبات قواعد البيانات المكررة في صفحة مصمم تعيينات النماذج في خدمات التكوين التنظيمية](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="9c93a-264">تشير القيمة **\[Q:530\]** إلى أنه تم استدعاء جدول VendTrans بعدد 530 مرة لإرجاع لعرض سحل من هذا الجدول لمصدر بيانات /\<Relations/VendTrans.VendTable\_AccountNum.</span><span class="sxs-lookup"><span data-stu-id="9c93a-264">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="9c93a-265">تشير القيمة **\[530\]** إلى استدعاء مصدر بيانات VendTable/\<Relations/VendTrans.VendTable\_AccountNum بعدد 530 مرة لعرض سجل من مصدر البيانات وإدخال التفاصيل منها في نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="9c93a-265">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="9c93a-266">نوصيك باستخدام التخزين المؤقت لمصدر بيانات VendTable/\<Relations/VendTrans.VendTable\_AccountNum للحد من عدد الاستدعاءات التي تم إجراؤها للحصول على تفاصيل 265 حركة وللمساعدة في تحسين أداء تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="9c93a-266">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="9c93a-267">قد يكون من المفيد أيضًا تقليل عدد المكالمات التي يتم إجراؤها لمصدر بيانات LedgerTransTypeList.</span><span class="sxs-lookup"><span data-stu-id="9c93a-267">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="9c93a-268">يتم استخدام مصدر البيانات هذا لإقران كل قيمة لتعداد **LedgerTransType** بالتسمية الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="9c93a-268">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="9c93a-269">باستخدام مصدر البيانات هذا، يمكنك العثور على تسمية مناسبة وإدخالها في نموذج البيانات لكل حركة مورد.</span><span class="sxs-lookup"><span data-stu-id="9c93a-269">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="9c93a-270">عدد الاستدعاءات الحالي لمصدر البيانات هذا (9,027) مرتفع جدًا لـ 265 حركة.</span><span class="sxs-lookup"><span data-stu-id="9c93a-270">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![صفحة مصمم تعيين النموذج في خدمات التكوين التنظيمية تعرض 9,027 استدعاء لمصدر البيانات](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="9c93a-272">تحسين تعيين النموذج استنادًا إلى المعلومات الواردة من تتبع التنفيذ</span><span class="sxs-lookup"><span data-stu-id="9c93a-272">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="9c93a-273">تعديل منطق تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="9c93a-273">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="9c93a-274">اتبع الخطوات التالية لاستخدام التخزين المؤقت، للمساعدة في منع الاستدعاءات المكررة لقاعدة البيانات:</span><span class="sxs-lookup"><span data-stu-id="9c93a-274">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="9c93a-275">في خدمات التكوين التنظيمية، في صفحة **مصمم تعيين النموذج**، في جزء **مصادر البيانات**، حدد عنصر **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-275">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="9c93a-276">حدد **ذاكرة التخزين المؤقت**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-276">Select **Cache**.</span></span>
    3. <span data-ttu-id="9c93a-277">قم بتوسيع عنصر **VendTable**، وقم بتوسيع قائمة العلاقات بين الواحد والعديد لمصدر بيانات VendTable (عنصر **\<العلاقات**)، وحدد عنصر **VendTrans.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-277">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="9c93a-278">حدد **ذاكرة التخزين المؤقت**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-278">Select **Cache**.</span></span>

    ![إعداد التخزين المؤقت للمساعدة على منع المكالمات المتكررة](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="9c93a-280">اتبع هذه الخطوات لإحضار مصدر بيانات LedgerTransTypeList إلى نطاق مصدر بيانات VendTable:</span><span class="sxs-lookup"><span data-stu-id="9c93a-280">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="9c93a-281">في جزء **انواع مصادر البيانات**، قم بتوسيع عنصر **الوظائف**، وحدد عنصر **الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-281">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="9c93a-282">في جزء **مصادر البيانات**، حدد عنصر **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-282">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="9c93a-283">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-283">Select **Add**.</span></span>
    4. <span data-ttu-id="9c93a-284">في حقل **الاسم**، حدد **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-284">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="9c93a-285">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-285">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="9c93a-286">في حقل **المعادلة**، أدخل **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-286">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="9c93a-287">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-287">Select **Save**.</span></span>
    8. <span data-ttu-id="9c93a-288">أغلق صفحة **محرر المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-288">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="9c93a-289">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-289">Click **OK**.</span></span>

3. <span data-ttu-id="9c93a-290">اتبع الخطوات التالية للقيام بالتخزين المؤقت في حقل **\$TransType**:</span><span class="sxs-lookup"><span data-stu-id="9c93a-290">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="9c93a-291">حدد عنصر **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-291">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="9c93a-292">حدد **ذاكرة التخزين المؤقت**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-292">Select **Cache**.</span></span>
    3. <span data-ttu-id="9c93a-293">حدد صنف **VendTable.\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-293">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="9c93a-294">حدد **ذاكرة التخزين المؤقت**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-294">Select **Cache**.</span></span>

    ![إعداد التخزين المؤقت لحقل $TransType](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="9c93a-296">اتبع الخطوات التالية لتغيير حقل **\$TransTypeRecord** بحيث يبدأ في استخدام حقل **\$TransType** المخزن مؤقتًا:</span><span class="sxs-lookup"><span data-stu-id="9c93a-296">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="9c93a-297">في جزء **مصادر البيانات**، قم بتوسيع عنصر **VendTable**، وقم بتوسيع عنصر **\<العلاقات**، وقم بتوسيع عنصر **VendTrans.VendTable\_AccountNum**، وحدد عنصر **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-297">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="9c93a-298">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-298">Select **Edit**.</span></span>
    3. <span data-ttu-id="9c93a-299">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-299">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="9c93a-300">في حقل **المعادلة**، ابحث عن التعبير التالي:</span><span class="sxs-lookup"><span data-stu-id="9c93a-300">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="9c93a-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="9c93a-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="9c93a-302">في حقل **المعادلة**، ابحث عن التعبير التالي:</span><span class="sxs-lookup"><span data-stu-id="9c93a-302">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="9c93a-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="9c93a-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="9c93a-304">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-304">Select **Save**.</span></span>
    7. <span data-ttu-id="9c93a-305">أغلق صفحة **محرر المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-305">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="9c93a-306">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-306">Select **OK**.</span></span>

5. <span data-ttu-id="9c93a-307">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-307">Select **Save**.</span></span>
6. <span data-ttu-id="9c93a-308">أغلق صفحة **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-308">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="9c93a-309">أغلق صفحة **تعيينات النماذج**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-309">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="9c93a-310">إكمال الإصدار المعدل من تعيين طراز التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="9c93a-310">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="9c93a-311">في خدمات التكوين التنظيمية، في صفحة **التكوينات**، في علامة التبويب السريع **الإصدارات**، حدد الإصدار **1.2** في تكوين **تعيين تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-311">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="9c93a-312">حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-312">Select **Change status**.</span></span>
3. <span data-ttu-id="9c93a-313">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-313">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="9c93a-314">استيراد تكوين تعيين نموذج التقارير الإلكترونية المعدل من خدمات التكوين التنظيمية إلى التطبيق</span><span class="sxs-lookup"><span data-stu-id="9c93a-314">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="9c93a-315">كرر الخطوات الواردة في [استيراد تكوين التقارير الإلكترونية من RCS إلى Finance and Operations](#import-configuration) سابقًا في هذا الموضوع لاستيراد الإصدار 1.2 من تكوين **تعيين تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-315">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="9c93a-316">تشغيل حل التقارير الإلكترونية المعدل لتتبع التنفيذ</span><span class="sxs-lookup"><span data-stu-id="9c93a-316">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="9c93a-317">تشغيل تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="9c93a-317">Run the ER format</span></span>

<span data-ttu-id="9c93a-318">كرر الخطوات الموجودة في قسم [تشغيل تنسيق التقارير الإلكترونية](#run-format) من قبل في هذا الموضوع لإنشاء تتبع أداء جديد.</span><span class="sxs-lookup"><span data-stu-id="9c93a-318">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="work-with-the-execution-trace"></a><span data-ttu-id="9c93a-319">العمل مع تتبع التنفيذ</span><span class="sxs-lookup"><span data-stu-id="9c93a-319">Work with the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="9c93a-320">تصدير التتبع الذي تم إنشاؤه من التطبيق</span><span class="sxs-lookup"><span data-stu-id="9c93a-320">Export the generated trace from the application</span></span>

<span data-ttu-id="9c93a-321">كرر الخطوات الموجودة في قسم [تصدير التتبع الذي تم إنشاؤه من التطبيق](#export-trace) من قبل في هذا الموضوع لحفظ تتبع أداء جديد محليًا.</span><span class="sxs-lookup"><span data-stu-id="9c93a-321">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="9c93a-322">استيراد التتبع الذي تم إنشاؤه في خدمة التكوين التنظيمية</span><span class="sxs-lookup"><span data-stu-id="9c93a-322">Import the generated trace into RCS</span></span>

<span data-ttu-id="9c93a-323">كرر الخطوات الموجودة في قسم [استيراد التتبع الذي تم إنشاؤه في خدمة التكوين التنظيمية‬](#import-trace) من قبل هذا الموضوع لاستيراد عملية تتبع الأداء الجديدة إلى خدمات التكوين التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="9c93a-323">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="9c93a-324">استخدام تتبع الأداء للتحليل في خدمات التكوين التنظمية - تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="9c93a-324">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="9c93a-325">كرر الخطوات الموجودة في قسم [استخدام تتبع الأداء للتحليل في خدمات التكوين التنظمية - تعيين النموذج](#use-trace) من قبل في هذا الموضوع لتحليل آخر تتبع للأداء.</span><span class="sxs-lookup"><span data-stu-id="9c93a-325">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="9c93a-326">لاحظ أن التسويات التي أجريتها على تعيين النموذج قد تقوم بإزالة الاستعلامات المكررة لقاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="9c93a-326">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="9c93a-327">يتم أيضًا تقليل عدد الاستدعاءات إلى جداول قاعدة البيانات ومصادر البيانات لتعيين هذا النموذج.</span><span class="sxs-lookup"><span data-stu-id="9c93a-327">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="9c93a-328">وبالتالي، تم تحسين أداء حل التقارير الإلكترونية بالكامل.</span><span class="sxs-lookup"><span data-stu-id="9c93a-328">Therefore, the performance of the whole ER solution has improved.</span></span>

![تتبع معلومات مصدر بيانات VendTable في صفحة مصمم تعيين النموذج في خدمات التكوين التنظيمية](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="9c93a-330">في معلومات التتبع، تشير القيمة **\[12\]** الخاصة بمصدر بيانات VendTable إلى أن مصدر البيانات هذا تم استدعاؤه 12 مرة.</span><span class="sxs-lookup"><span data-stu-id="9c93a-330">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="9c93a-331">تشير القيمة **\[Q:6\]** إلى أنه تمت ترجمة ست استدعاءات إلى استدعاءات قاعدة البيانات لجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="9c93a-331">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="9c93a-332">تشير القيمة **\[C:6\]** إلى أنه تم تخزين السجلات التي تم إحضارها من قاعده البيانات مؤقتًا، وتمت معالجة ست استدعاءات أخرى باستخدام ذاكرة التخزين المؤقت.</span><span class="sxs-lookup"><span data-stu-id="9c93a-332">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="9c93a-333">لاحظ أنه تم تقليل عدد الاستدعاءات إلى مصدر بيانات LedgerTransTypeList من 9,027 إلى 240.</span><span class="sxs-lookup"><span data-stu-id="9c93a-333">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![تتبع معلومات مصدر بيانات LedgerTransTypeList في صفحة مصمم تعيين النموذج في خدمات التكوين التنظيمية](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="9c93a-335">مراجعة تتبع التنفيذ في التطبيق</span><span class="sxs-lookup"><span data-stu-id="9c93a-335">Review the execution trace in the application</span></span>

<span data-ttu-id="9c93a-336">بالإضافة إلى خدمات التكوين التنظمية، قد توفر بعض الإصدارات إمكانات لتجربة مصمم إطار التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9c93a-336">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="9c93a-337">تشتمل هذه الإصدارات على خيار **تمكين وضع التصميم** الذي يمكن تشغيله.</span><span class="sxs-lookup"><span data-stu-id="9c93a-337">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="9c93a-338">يمكنك العثور على هذا الخيار في علامة التبويب **عام** في صفحة **معلمات التقارير الإلكترونية**، التي يمكنك فتحها من مساحة عمل **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-338">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![صفحة تمكين خيار وضع التصميم على معلمات التقارير الإلكترونية](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="9c93a-340">في حاله استخدام أحد هذه الإصدارات من Finance and Operations، يمكنك تحليل تفاصيل تتبعات الأداء التي يتم إنشاؤها مباشرة في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="9c93a-340">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="9c93a-341">وليس من الضروري أن تقوم بتصديرها من التطبيق واستيرادها في خدمات التكوين التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="9c93a-341">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="9c93a-342">مراجعة تتبع التنفيذ باستخدام الأدوات الخارجية</span><span class="sxs-lookup"><span data-stu-id="9c93a-342">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="9c93a-343">تكوين معلمات المستخدمين</span><span class="sxs-lookup"><span data-stu-id="9c93a-343">Configure user parameters</span></span>

1. <span data-ttu-id="9c93a-344">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-344">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="9c93a-345">في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="9c93a-346">في مربع الحوار **معلمات المستخدمين**، في قسم **تتبع التنفيذ**، في حقل **تنسيق تتبع التنفيذ**، حدد **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-346">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="9c93a-347">تشغيل تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="9c93a-347">Run the ER format</span></span>

<span data-ttu-id="9c93a-348">كرر الخطوات الموجودة في قسم [تشغيل تنسيق التقارير الإلكترونية](#run-format) من قبل في هذا الموضوع لإنشاء تتبع أداء جديد.</span><span class="sxs-lookup"><span data-stu-id="9c93a-348">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="9c93a-349">لاحظ أن مستعرض الويب يعرض ملفًا من نوع zip للتنزيل.</span><span class="sxs-lookup"><span data-stu-id="9c93a-349">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="9c93a-350">يحتوي هذا الملف على تتبع الأداء بتنسيق PerfView.</span><span class="sxs-lookup"><span data-stu-id="9c93a-350">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="9c93a-351">يمكنك بعد ذلك استخدام أداه تحليل أداء PerfView لتحليل تفاصيل تنفيذ تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9c93a-351">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![معلومات تتبع الأداء بتنسيق PerfView](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="9c93a-353">استخدم أدوات خارجية لمراجعة تتبع التنفيذ الذي يتضمن استعلامات قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="9c93a-353">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="9c93a-354">نظرًا للتحسينات التي تم إجراؤها علي إطار عمل التقارير الإلكترونية، يقدم تتبع الأداء الذي تم إنشاؤه بتنسيق PerfView الآن تفاصيل أكثر حول تنفيذ التنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9c93a-354">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="9c93a-355">في Microsoft Dynamics 365 for Finance and Operations الإصدار 10.0.4 (يوليو 2019)، يمكن أن يتضمن هذا التتبع أيضًا تفاصيل استعلامات SQL التي تم تنفيذها على قاعدة بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="9c93a-355">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="9c93a-356">تكوين معلمات المستخدمين</span><span class="sxs-lookup"><span data-stu-id="9c93a-356">Configure user parameters</span></span>

1. <span data-ttu-id="9c93a-357">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-357">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9c93a-358">في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-358">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="9c93a-359">في مربع الحوار **معلمات المستخدمين**، في قسم **تتبع التنفيذ**، عيِّن المعلمات التالية:</span><span class="sxs-lookup"><span data-stu-id="9c93a-359">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="9c93a-360">في حقل **تنسيق تتبع التنفيذ**، حدد **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-360">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="9c93a-361">عيّن الخيار **تجميع إحصائيات الاستعلام** على القيمة **نعم**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-361">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="9c93a-362">عيّن الخيار **استعلام التتبع** على القيمة **نعم**.</span><span class="sxs-lookup"><span data-stu-id="9c93a-362">Set the **Trace query** option to **Yes**.</span></span>

    ![قسم تتبع التنفيذ، مربع حوار معلمات المستخدم](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="9c93a-364">تشغيل تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="9c93a-364">Run the ER format</span></span>

<span data-ttu-id="9c93a-365">كرر الخطوات الموجودة في قسم [تشغيل تنسيق التقارير الإلكترونية](#run-format) من قبل في هذا الموضوع لإنشاء تتبع أداء جديد.</span><span class="sxs-lookup"><span data-stu-id="9c93a-365">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="9c93a-366">لاحظ أن مستعرض الويب يعرض ملفًا من نوع zip للتنزيل.</span><span class="sxs-lookup"><span data-stu-id="9c93a-366">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="9c93a-367">يحتوي هذا الملف على تتبع الأداء بتنسيق PerfView.</span><span class="sxs-lookup"><span data-stu-id="9c93a-367">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="9c93a-368">يمكنك بعد ذلك استخدام أداه تحليل أداء PerfView لتحليل تفاصيل تنفيذ تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9c93a-368">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="9c93a-369">يتضمن هذا التتبع الآن تفاصيل الوصول إلى قاعدة بيانات SQL أثناء تنفيذ تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9c93a-369">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![معلومات التتبع لتنسيق التقارير الإلكترونية الذي تم تنفيذه في PerfView](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a><span data-ttu-id="9c93a-371">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9c93a-371">Additional resources</span></span>

- [<span data-ttu-id="9c93a-372">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="9c93a-372">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="9c93a-373">تحسين أداء حلول التقارير الإلكتروني عن طريق إضافة مصادر بيانات الحقول المحسوبة ذات معلمات</span><span class="sxs-lookup"><span data-stu-id="9c93a-373">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
