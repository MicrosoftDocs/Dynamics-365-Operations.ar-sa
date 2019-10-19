---
title: إعداد البرنامج التعليمي للأداة Regression Suite Automation Tool وتثبيته
description: هذا الموضوع هو برنامج تعليمي يوضح كيفية إعداد الأداة Regression Suite Automation Tool ‏(RSAT).
author: kfend
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 50450669387f4e2c9e81975d5345c525c7929c47
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180635"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="f4c10-103">إعداد البرنامج التعليمي للأداة Regression Suite Automation Tool وتثبيته</span><span class="sxs-lookup"><span data-stu-id="f4c10-103">Set up and install Regression suite automation tool tutorial</span></span>
<span data-ttu-id="f4c10-104">هذا الموضوع هو برنامج تعليمي يساعدك على الحصول على الإعداد والبدء باستخدام RSAT والأدوات المقترنة باستخدام RSAT.</span><span class="sxs-lookup"><span data-stu-id="f4c10-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span> 

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="f4c10-105">استخدم أدوات مستعرض الإنترنت لتنزيل هذه الصفحة وحفظها بتنسيق PDF.</span><span class="sxs-lookup"><span data-stu-id="f4c10-105">Use your internet browser tools to download and save this page in PDF format.</span></span> 

## <a name="key-concepts"></a><span data-ttu-id="f4c10-106">المفاهيم الأساسية</span><span class="sxs-lookup"><span data-stu-id="f4c10-106">Key concepts</span></span>

- <span data-ttu-id="f4c10-107">فهم التثبيت وإعداد المتطلبات الأساسية المطلوبين للتطبيقات المتنوعة التي تدعم Regression suite automation tool ‏(RSAT).</span><span class="sxs-lookup"><span data-stu-id="f4c10-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="f4c10-108">معرفة كيف تسمح لك ميزة مسجل المهام مع Microsoft Dynamics Lifecycle Services (LCS) وMicrosoft Azure DevOps، إنشاء حالات اختبار وتكوينها وتشغيلها والاستقصاء بشأنها وإعداد تقرير بها.</span><span class="sxs-lookup"><span data-stu-id="f4c10-108">Understand how the Task recorder feature, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="f4c10-109">تمكين المستخدمين الوظيفيين من تسجيل مهام العمل باستخدام "مسجل المهام"، ثم تحويل تسجيلات المهام إلى مجموعة من الاختبارات التلقائية دون الحاجة إلى كتابة كود مصدر.</span><span class="sxs-lookup"><span data-stu-id="f4c10-109">Empower functional users to record business tasks by using Task recorder, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="f4c10-110">قبل البدء</span><span class="sxs-lookup"><span data-stu-id="f4c10-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f4c10-111">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="f4c10-111">Prerequisites</span></span>

- <span data-ttu-id="f4c10-112">بيئة تقوم بتشغيل الإصدار 10.0 من Microsoft Dynamics 365 for Finance and Operations  (أبريل 2019) أو إصدار أحدث مطلوبة لهذا البرنامج التعليمي.</span><span class="sxs-lookup"><span data-stu-id="f4c10-112">An environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="f4c10-113">بالنسبة للعملاء الذين يستخدمون Microsoft Dynamics 365 for Finance and Operations Enterprise edition 7.3، فإن تحديث النظام الأساسي 20 (PU20) أو التحديث الأحدث مدعوم أيضًا.</span><span class="sxs-lookup"><span data-stu-id="f4c10-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="f4c10-114">يجب أن يكون لدى المستخدم حقوق المسؤول في هذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-114">The user must have admin rights to the environment.</span></span>
- <span data-ttu-id="f4c10-115">يجب أن يكون لديك حق الوصول إلى LCS المستأجر وAzure DevOps (وهو ما يُعرف سابقًا باسم Microsoft Visual Studio Team Services \[VSTS\]).</span><span class="sxs-lookup"><span data-stu-id="f4c10-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="f4c10-116">يجب أن يحتوي المستخدم الذي يقوم بإنشاء مجموعات الاختبارات وإدارتها على خطط اختبار Azure DevOps أو ترخيص مدير اختبارات.</span><span class="sxs-lookup"><span data-stu-id="f4c10-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="f4c10-117">ستمنحك التراخيص التالية حق الوصول إلى خطط الاختبار:</span><span class="sxs-lookup"><span data-stu-id="f4c10-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="f4c10-118">ترخيص Enterprise لـ Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f4c10-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="f4c10-119">ترخيص Test Professional لـ Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f4c10-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="f4c10-120">ترخيص المشترك لأنظمة MSDN الأساسية</span><span class="sxs-lookup"><span data-stu-id="f4c10-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="f4c10-121">يجب أن يمتلك RSAT إمكانية الوصول إلى بيئة الاختبار من خلال مستعرض ويب.</span><span class="sxs-lookup"><span data-stu-id="f4c10-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="f4c10-122">لإنشاء معلمات الاختبار وتحريرها، يجب تثبيت Microsoft Excel أولًا.</span><span class="sxs-lookup"><span data-stu-id="f4c10-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="f4c10-123">تكوين Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="f4c10-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="f4c10-124">أهلية المستخدم</span><span class="sxs-lookup"><span data-stu-id="f4c10-124">User eligibility</span></span>

<span data-ttu-id="f4c10-125">تأكد من إنشاء المستخدم في Azure DevOps وأن له مستوى الاشتراك الذي يوفر الوصول إلى خطط اختبار Azure.</span><span class="sxs-lookup"><span data-stu-id="f4c10-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="f4c10-126">إن ترخيص خطط اختبار Azure DevOps مطلوب فقط إذا كان المستخدم سيقوم بإنشاء حالات الاختبار وإدارتها (وهذا يعني، أنه لا يطلب كل مستخدمي RSAT هذا الترخيص).</span><span class="sxs-lookup"><span data-stu-id="f4c10-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="f4c10-127">للحصول على معلومات عن متطلبات الترخيص، راجع [متطلبات الترخيص](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements)</span><span class="sxs-lookup"><span data-stu-id="f4c10-127">For information about the license requirements, see [License requirements](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="f4c10-128">إنشاء مشروع Azure DevOps جديد</span><span class="sxs-lookup"><span data-stu-id="f4c10-128">Create a new Azure DevOps project</span></span>
<span data-ttu-id="f4c10-129">يقوم RSAT باستخدام Azure Devops لحالة الاختبار وإدارة مجموعة الاختبارات، وإعداد تقرير عن نتائج تشغيل الاختبار والتحقق منها.</span><span class="sxs-lookup"><span data-stu-id="f4c10-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span> 

> [!NOTE]
> <span data-ttu-id="f4c10-130">يمكنك استخدام مشروع Azure DevOps موجود.</span><span class="sxs-lookup"><span data-stu-id="f4c10-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="f4c10-131">ومع ذلك، إذا كان مشروع Azure DevOps الموجود مُعدًا بحيث يحتوي على قالب مخصص، فسيظهر لك خطأ "فشلت مزامنة VSTS‬" عند مزامنة حالات الاختبار من أداة تكوين عمليات التعيين (BPM) إلى Azure DevOps (راجع [اختبار التزامن من BPM إلى قسم Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops)).</span><span class="sxs-lookup"><span data-stu-id="f4c10-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="f4c10-132">وفي حالة اتباع أفضل الممارسات التالية للقالب المخصص، ستتمكن من مزامنة حالات الاختبار إلى Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f4c10-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="f4c10-133">(يتم سرد أفضل الممارسات هذه في رسالة الخطأ.)</span><span class="sxs-lookup"><span data-stu-id="f4c10-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="f4c10-134">لا تحذف أي نوع من أنواع عناصر العمل أو الحقول الجاهزة</span><span class="sxs-lookup"><span data-stu-id="f4c10-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="f4c10-135">لا تحذف أي حالة لنوع عنصر عمل.</span><span class="sxs-lookup"><span data-stu-id="f4c10-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="f4c10-136">لا تقم بإضافة أي حقول مطلوبة لنوع عنصر عمل.</span><span class="sxs-lookup"><span data-stu-id="f4c10-136">Do not add any required fields to a work item type.</span></span>

![رسالة خطا تتضمن قائمة بأفضل الممارسات](./media/setup_rsa_tool_02.png)

<span data-ttu-id="f4c10-138">وإلا، بالنسبة لهذا البرنامج التعليمي، نوصي بإنشاء مشروع Azure DevOps جديد.</span><span class="sxs-lookup"><span data-stu-id="f4c10-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="f4c10-139">للحصول على المزيد من المعلومات، راجع [المشكلات التي تحدث عند المزامنة مع BPM باستخدام قالب عملية Azure DevOps ‏(VSTS) مخصص](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span><span class="sxs-lookup"><span data-stu-id="f4c10-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="f4c10-140">افتح عنوان URL الخاص بـ Azure DevOps ‏(`https://dev.azure.com/<Azure DevOps Name>`)</span><span class="sxs-lookup"><span data-stu-id="f4c10-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="f4c10-141">حدد **إنشاء مشروع** في الركن العلوي الأيسر من الصفحة Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f4c10-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![زر إنشاء المشروع](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="f4c10-143">قم بملء الحقول التالية،ثم حدد **إنشاء**:</span><span class="sxs-lookup"><span data-stu-id="f4c10-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="f4c10-144">**اسم المشروع**</span><span class="sxs-lookup"><span data-stu-id="f4c10-144">**Project name**</span></span>
    - <span data-ttu-id="f4c10-145">**التحكم في الإصدار** - حدد **Team Foundation Version Control**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="f4c10-146">لاحظ أن الخيار الافتراضي، **Git**، غير مدعوم.</span><span class="sxs-lookup"><span data-stu-id="f4c10-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="f4c10-147">**عملية صنف العمل**</span><span class="sxs-lookup"><span data-stu-id="f4c10-147">**Work item process**</span></span>

    ![مربع الحوار "إنشاء مشروع جديد"](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="f4c10-149">إنشاء رمز وصول مميز شخصي</span><span class="sxs-lookup"><span data-stu-id="f4c10-149">Create a personal access token</span></span>

<span data-ttu-id="f4c10-150">في هذا البرنامج التعليمي، ستستخدم أداة تكوين عمليات الأعمال (BPM) لـ LCS لإنشاء مكتبة حالة اختبار ومزامنة حالات الاختبار مع Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f4c10-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="f4c10-151">وستحتاج إلى رمز وصول مميز شخصي لمزامنة BPM مع Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f4c10-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="f4c10-152">حدد رمز ملف التعريف الموجود في الركن الأيسر العلوي من صفحة مشروع Azure DevOps الخاص بك، ثم حدد **الأمان**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![أمر الأمان](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="f4c10-154">في الجزء الأيمن، ضمن **الأمان**، حدد **رمز الوصول المميز الشخصي**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="f4c10-155">ثم حدد **رمزًا مميزًا جديدًا**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-155">Then select **New Token**.</span></span>

    ![زر "الرمز المميز الجديد" في علامة التبويب "رموز الوصول المميزة الشخصية" في "إعدادات المستخدم"](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="f4c10-157">قم بملء الحقول التالية،ثم حدد **إنشاء**:</span><span class="sxs-lookup"><span data-stu-id="f4c10-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="f4c10-158">**الاسم**</span><span class="sxs-lookup"><span data-stu-id="f4c10-158">**Name**</span></span>
    - <span data-ttu-id="f4c10-159">**انتهاء الصلاحية (UTC)** - حدد **محدد مخصص**، ثم استخدم منتقي التاريخ لتحديد آخر تاريخ متاح.</span><span class="sxs-lookup"><span data-stu-id="f4c10-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="f4c10-160">**النطاقات** - حدد خيار **الوصول الكامل**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-160">**Scopes** – Select the **Full access** option.</span></span>

    ![مربع الحوار "إنشاء رمز وصول مميز شخصي"](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="f4c10-162">دوِّن ملحوظة بخصوص رمز الوصول المميز الشخصي الذي يتم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="f4c10-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="f4c10-163">ستحتاج إليها لاحقًا عند إعداد تكوين RSAT.</span><span class="sxs-lookup"><span data-stu-id="f4c10-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![رمز الوصول المميز الشخصي](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="f4c10-165">تكوين مشروع LCS</span><span class="sxs-lookup"><span data-stu-id="f4c10-165">Configure the LCS project</span></span>

<span data-ttu-id="f4c10-166">تحتاج إلى مشروع Lifecycle Services ‏(LCS) لمكتبة الاختبار الرئيسية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="f4c10-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="f4c10-167">وتُستخدم أداة تكوين عمليات الأعمال(BPM) لـ LCS بصفتها المكتبة الرئيسية لحالات الاختبار الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="f4c10-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="f4c10-168">وتُستخدم BPM لإدارة مكتبات الاختبار وتوزيعها عبر مشاريع LCS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="f4c10-169">علي سبيل المثال، يقوم أحد شركاء Microsoft أو مورِّد برامج مستقل (ISV) بإنشاء مكتبات الاختبار التي ستُصدر حالات الاختبار في شكل مكتبات BPM.</span><span class="sxs-lookup"><span data-stu-id="f4c10-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="f4c10-170">في BPM، يتم تنظيم حالات الاختبار حسب العملية التجارية.</span><span class="sxs-lookup"><span data-stu-id="f4c10-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="f4c10-171">لا تحدد BPM أمر التنفيذ أو التكرار الخاص باجتياز الاختبار الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="f4c10-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="f4c10-172">تتم إدارة هذه التفاصيل في Azure DevOps، كما هو مفصل لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="f4c10-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="f4c10-173">بالنسبة لمشروع LCS، يمكنك استخدام تطبيق عميل أو مشروع شريك موجود.</span><span class="sxs-lookup"><span data-stu-id="f4c10-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="f4c10-174">تحديث لغة LCS</span><span class="sxs-lookup"><span data-stu-id="f4c10-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="f4c10-175">حتى تتمكن واجهة المستخدم (UI) من إظهار العمليات التجارية بشكل صحيح، يجب تعيين لغة LCS المفضلة إلى **اللغة الانجليزية (الولايات المتحدة)**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="f4c10-176">انتقل إلى مشروع تطبيق LCS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="f4c10-177">حدد زر **الإعدادات** (رمز الترس) في الركن العلوي الأيسر، ثم حدد **تفضيل اللغة‬**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![الأوامر الموجودة في قائمة الإعدادات](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="f4c10-179">في حقل **اللغة المفضلة**، حدد **اللغة الإنجليزية (الولايات المتحدة)**، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![علامة تبويب تفضيل اللغة في إعدادات المستخدم](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="f4c10-181">تكوين LCS للاتصال بمشروع Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="f4c10-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="f4c10-182">إذا قمت بإنشاء Azure DevOps مشروع جديد مسبقًا، فقم بتكوين مشروع LCS للاتصال به.</span><span class="sxs-lookup"><span data-stu-id="f4c10-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="f4c10-183">وإلا، إذا كان مشروع LCS الخاص بك متصلًا بالفعل بمشروع Azure DevOps، فيمكنك المتابعة إلى القسم التالي.</span><span class="sxs-lookup"><span data-stu-id="f4c10-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="f4c10-184">انتقل إلى مشروع تطبيق LCS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="f4c10-185">حدد زر **القائمة**، ثم حدد **إعدادات المشروع**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![أمر "إعدادات المشروع"](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="f4c10-187">في الجزء الأيمن، حدد خدمات فريق **Visual Studio Team Services**، ثم حدد **إعداد Visual Studio Team Services**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![علامة التبويبVisual Studio Team Services في إعدادات المشروع](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="f4c10-189">في حقل **عنوان URL لموقع Azure DevOps**، أدخل عنوان URL لموقع Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f4c10-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="f4c10-190">وفي حقل **رمز الوصول المميز الشخصي**، أدخل رمز الوصول المميز الشخصي الذي تم إنشاؤه مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="f4c10-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4c10-191">على الرغم من أن VSTS تُعرف الآن باسم Azure DevOps، فاستخدم عنوان URL القديم لتوصيل LCS بمشروع Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f4c10-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="f4c10-192">على سبيل المثال، عنوان URL الخاص بـ Azure DevOps المستخدم في هذا البرنامج التعليمي هو `https://dev.azure.com/D365FOFastTrack/`</span><span class="sxs-lookup"><span data-stu-id="f4c10-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="f4c10-193">ومع ذلك، في الرسم التوضيحي التالي، تم إدخاله كـ `https://D365FOFastTrack.visualstudio.com/`.</span><span class="sxs-lookup"><span data-stu-id="f4c10-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![الخطوة 1 في إعداد Visual Studio Team Services](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="f4c10-195">حدد **متابعة**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-195">Select **Continue**.</span></span>
6. <span data-ttu-id="f4c10-196">في حقل **مشروع Visual Studio Team Services**، حدد مشروع VSTS في الموقع المحدد للربط بمشروع LCS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="f4c10-197">ويتم تعيين حقل **قالب العملية** إلى **Agile** افتراضيًا.</span><span class="sxs-lookup"><span data-stu-id="f4c10-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="f4c10-198">بالنسبة للقالب المخصص، راجع إرشادات أفضل الممارسات في قسم [إنشاء مشروع Azure DevOps جديد](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="f4c10-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="f4c10-199">ثم حدد **متابعة**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-199">Then select **Continue**.</span></span>

    ![الخطوة 2 في إعداد Visual Studio Team Services](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="f4c10-201">راجع إعداداتك، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-201">Review your settings, and then select **Save**.</span></span>

    ![الخطوة 3 في إعداد Visual Studio Team Services](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="f4c10-203">حدد **تخويل** لتخويل LCS للوصول إلى موقع Azure DevOps الذي تم تكوينه نيابة عنك ولتشغيل الميزات التي تتكامل مع VSTS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![زر التخويل](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="f4c10-205">يظهر مربع رسالة ينص على ما يلي: "أنت على وشك إعادة توجيهك إلى موقع أبدي لتخويل LCS للاتصال بخدمات Visual Studio Team Services نيابة عنك.</span><span class="sxs-lookup"><span data-stu-id="f4c10-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="f4c10-206">هل تريد المتابعة؟"</span><span class="sxs-lookup"><span data-stu-id="f4c10-206">Proceed?"</span></span> <span data-ttu-id="f4c10-207">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-207">Select **Yes**.</span></span>

    ![مربع الرسالة](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="f4c10-209">حدد **قبول**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-209">Select **Accept**.</span></span>

    ![تخويل الوصول](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="f4c10-211">إذا كنت مخولًا كمستخدم، فإن واجهة المستخدم التي يجب عليك الرجوع إليها هي صفحة إعدادات مشروع LCS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![المستخدم المخول](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="f4c10-213">إنشاء مكتبة BPM جديدة</span><span class="sxs-lookup"><span data-stu-id="f4c10-213">Create a new BPM library</span></span>

1. <span data-ttu-id="f4c10-214">انتقل إلى مشروع تطبيق LCS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="f4c10-215">حدد زر **القائمة**، ثم حدد **أداة تكوين عمليات الأعمال**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![أمر أداة تكوين عمليات الأعمال](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="f4c10-217">تحديد **مكتبة جديدة**</span><span class="sxs-lookup"><span data-stu-id="f4c10-217">Select **New library**.</span></span>

    ![زر المكتبة الجديدة](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="f4c10-219">في حقل **اسم المكتبة**، أدخل اسمًا ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="f4c10-220">وبالنسبة لهذا البرنامج التعليمي، فقم بتسمية مكتبة BPM ‏**RSAT**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![مربع الحوار "إنشاء مكتبة جديدة"](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="f4c10-222">افتح مكتبة **RSAT** BPM الجديدة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="f4c10-223">حدد عملية **نموذج عملية الأعمال الأساسية**، ثم حدد **وضع التحرير** من اليسار.</span><span class="sxs-lookup"><span data-stu-id="f4c10-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![زر وضع التحرير](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="f4c10-225">قم بتغيير قيمة حقل **الاسم** وحقل **الوصف** **لإنشاء منتج**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="f4c10-226">ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-226">Then select **Save**.</span></span>

    ![حقلي الاسم والوصف](./media/setup_rsa_tool_24.png)

## <a name="environment"></a><span data-ttu-id="f4c10-228">البيئة</span><span class="sxs-lookup"><span data-stu-id="f4c10-228">Environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="f4c10-229">متطلبات الإصدار</span><span class="sxs-lookup"><span data-stu-id="f4c10-229">Version requirement</span></span>

<span data-ttu-id="f4c10-230">يجب أن تتوفر بيئة اختبار أو بيئة اختبار معزولة تعمل بالإصدار 10.</span><span class="sxs-lookup"><span data-stu-id="f4c10-230">A test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="f4c10-231">وبالنسبة للعملاء الذين يستخدمون الإصدار 7.3، يتم دعم تحديث النظام الأساسي 20 أو الإصدارات أحدث.</span><span class="sxs-lookup"><span data-stu-id="f4c10-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="f4c10-232">يجب أن يمتلك RSAT إمكانية الوصول إلى بيئة الاختبار من خلال مستعرض ويب.</span><span class="sxs-lookup"><span data-stu-id="f4c10-232">RSAT must have access to your test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="f4c10-233">معايير المستخدم</span><span class="sxs-lookup"><span data-stu-id="f4c10-233">User criteria</span></span>

<span data-ttu-id="f4c10-234">يجب أن يكون للمستخدم حقوق المسؤول في هذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="f4c10-235">إعداد إعدادات المساعدة للاتصال بـ LCS</span><span class="sxs-lookup"><span data-stu-id="f4c10-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="f4c10-236">هذه الخطوة مطلوبة للاتصال بـ LCS بحيث يمكن حفظ تسجيلات المهام في مكتبة BPM المناسبة في LCS من خلال العميل.</span><span class="sxs-lookup"><span data-stu-id="f4c10-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the client.</span></span>

1. <span data-ttu-id="f4c10-237">افتح العميل.</span><span class="sxs-lookup"><span data-stu-id="f4c10-237">Open the client.</span></span>
2. <span data-ttu-id="f4c10-238">انتقل إلى **إدارة النظام \> الإعداد \> معلمات النظام**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="f4c10-239">من علامة التبويب **التعليمات**، في حقل **تكوين تعليمات Lifecycle Services**، حدد مشروع LCS ذي الصلة (**RSAT** لهذا البرنامج التعليمي).</span><span class="sxs-lookup"><span data-stu-id="f4c10-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![حقل تكوين تعليمات Lifecycle Services في علامة التبويب "تعليمات"](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="f4c10-241">يتم ملء مكتبات BPM ضمن مشروع LCS المناسب.</span><span class="sxs-lookup"><span data-stu-id="f4c10-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="f4c10-242">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-242">Select **Save**.</span></span>
5. <span data-ttu-id="f4c10-243">قد تحتاج إلى تحديث المستعرض لرؤية محتوى التعليمات المحدّث.</span><span class="sxs-lookup"><span data-stu-id="f4c10-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![الإخطار حول تحديث المستعرض](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="f4c10-245">تسجيلات المهام</span><span class="sxs-lookup"><span data-stu-id="f4c10-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="f4c10-246">تأكد أن جميع تسجيلات المهام الخاصة بك تبدأ من لوحة المعلومات.</span><span class="sxs-lookup"><span data-stu-id="f4c10-246">Make sure that all your task recordings start on the main dashboard.</span></span> <span data-ttu-id="f4c10-247">اجعل التسجيلات الفردية قصيرة، وركز على مهمة أعمال واحدة، مثل إنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="f4c10-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="f4c10-248">إنشاء تسجيل مهام وحفظه في مكتبة BPM</span><span class="sxs-lookup"><span data-stu-id="f4c10-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="f4c10-249">قم بإنشاء تسجيل مهمة مطابق يمكنك إرفاقه بعملية الأعمال البسيطة التي تم إنشاؤها في مكتبة BPM الجديدة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="f4c10-250">افتح العميل.</span><span class="sxs-lookup"><span data-stu-id="f4c10-250">Open the client.</span></span>
2. <span data-ttu-id="f4c10-251">من **لوحة المعلومات** الرئيسية، حدد زر الإعدادات (رمز الترس)، ثم حدد **مسجل المهام**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![الأوامر الموجودة في قائمة الإعدادات](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="f4c10-253">حدد **إنشاء تسجيل**</span><span class="sxs-lookup"><span data-stu-id="f4c10-253">Select **Create recording**.</span></span>

    ![زر إنشاء تسجيل](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="f4c10-255">املأ حقلي **اسم التسجيل** و**وصف التسجيل**، ثم حدد **بدء**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![حقلي ‏‎اسم التسجيل‏‎ و‎وصف التسجيل‏‎](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="f4c10-257">سجل خطوات إنشاء منتج.</span><span class="sxs-lookup"><span data-stu-id="f4c10-257">Record the steps for creating a product.</span></span> <span data-ttu-id="f4c10-258">عند الانتهاء، حدد **إيقاف** لإيقاف التسجيل.</span><span class="sxs-lookup"><span data-stu-id="f4c10-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![خطوات إنشاء منتج](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="f4c10-260">حدد **حفظ إلى Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-260">Select **Save to Lifecycle Services**.</span></span>

    ![خيارات الحفظ](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="f4c10-262">يتم تحميل معلومات المكتبة من LCS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-262">Library information is loaded from LCS.</span></span>

    ![مؤشر التقدم](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="f4c10-264">حدد مكتبة BPM لإقران تسجيل المهام بها.</span><span class="sxs-lookup"><span data-stu-id="f4c10-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="f4c10-265">وبالنسبة لهذا البرنامج التعليمي، حدد مكتبة **RSAT** BPM التي تم إنشاؤها مسبقًا وعملية الأعمال **لإنشاء منتج** ضمنها.</span><span class="sxs-lookup"><span data-stu-id="f4c10-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="f4c10-266">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-266">Then select **OK**.</span></span>

    ![إقران تسجيل المهام بمكتبة BPM وعملية أعمال](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="f4c10-268">تظهر رسالة "الحفظ إلى Lifecycle Services ناجحة".</span><span class="sxs-lookup"><span data-stu-id="f4c10-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![رسالة بشأن حفظ ناجح إلى LCS](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="f4c10-270">إذا كنت تريد حفظ تسجيل المهمة محليًا ثم تحميلها إلى BPM عبر LCS، فاتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f4c10-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="f4c10-271">بعد اكتمال التسجيل، حدد **حفظ إلى هذا الكمبيوتر**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![خيارات الحفظ](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="f4c10-273">في شريط الإعلام المستعرض، حدد **حفظ** أو **حفظ باسم** لحفظ الملف على الكمبيوتر المحلي الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="f4c10-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![شريط الإخطارات](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="f4c10-275">انتقل إلى مكتبة **RSAT** BPM، وحدد عملية الأعمال لحفظ تسجيل المهمة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="f4c10-276">من علامة التبويب **نظرة عامة**، حدد **تحميل**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-276">On the **Overview** tab, select **Upload**.</span></span>

        ![زر التحميل](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="f4c10-278">حدد **استعراض**، ثم حدد ملف ‎.axtr الذي قمت بحفظه مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="f4c10-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="f4c10-279">ثم حدد **تحميل**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-279">Then select **Upload**.</span></span>

        ![تحديد ملف ‎.axtr المراد تحميله](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="f4c10-281">اختبار المزامنة من BPM إلى Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="f4c10-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="f4c10-282">الآن وبعد إرفاق تسجيل مهمة بعملية الأعمال، يجب التحقق من إمكانية مزامنة عملية الأعمال وتسجيل المهام المرتبطة إلى Azure DevOps كميزة وحالة اختبار (على التوالي) باستخدام ميزة مزامنة VSTS في LCS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="f4c10-283">سيختلف نوع عنصر العمل المقابل الذي تم إنشاؤه في Azure DevOps، استنادًا إلى قالب العملية الذي حددته عند تكوين مشروع LCS مع Azure DevOps، كما هو موضح في قسم [إنشاء مشروع Azure DevOps جديد](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="f4c10-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="f4c10-284">انتقل إلى مكتبة BPM، وافتح مكتبة **RSAT** التي قمت بإنشائها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="f4c10-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="f4c10-285">حدد زر علامة القطع (**...**)، وحدد **مزامنة VSTS**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![أمر مزامنة VSTS في قائمة القطع](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="f4c10-287">بعد اكتمال مزامنة VSTS، تظهر علامة تبويب **المتطلبات** على الجانب الأيسر وتتضمن عنصر عمل Azure DevOps المقابل.</span><span class="sxs-lookup"><span data-stu-id="f4c10-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4c10-288">سيحمل عنصر العمل الذي تم إنشاؤه في Azure DevOps اسم مكتبة BPM كبادئة للعنوان.</span><span class="sxs-lookup"><span data-stu-id="f4c10-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![علامة تبويب المتطلبات](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="f4c10-290">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-290">Refresh the page.</span></span>
4. <span data-ttu-id="f4c10-291">حدد زر علامة القطع (**...**). وستلاحظ خيارًا إضافيًا، **حالات اختبار المزامنة**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="f4c10-292">حدد هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="f4c10-292">Select this option.</span></span>

    ![أمر حالات اختبار المزامنة في قائمة القطع](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="f4c10-294">إذا كان خيار **حالات اختبار المزامنة** غير متاح بعد تحديث الصفحة، فانتقل إلى الصفحة الرئيسية لـ BPM، وحدد **حالات اختبار المزامنة** للمكتبة ذاتها بأكملها.</span><span class="sxs-lookup"><span data-stu-id="f4c10-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="f4c10-295">وبهذه الطريقة، يمكنك فرض التزامن للمكتبة بأكملها بشكل فعال.</span><span class="sxs-lookup"><span data-stu-id="f4c10-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    > 
    > ![تحديد حالات اختبار المزامنة للمكتبة بالكامل](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="f4c10-297">بعد اكتمال حالات اختبار المزامنة، سيتم إنشاء حالة اختبار جديدة في علامة تبويب **المتطلبات**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![حالة اختبار جديدة على علامة تبويب المتطلبات](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="f4c10-299">انتقل إلى مشروع Azure DevOps، وحدد **لوحات المعلومات \> أصناف العمل**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![أمر عناصر العمل ضمن لوحات المعلومات](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="f4c10-301">تحقق من وجود صنف العمل وحالة الاختبار التي قمت بإنشائها من خلال مزامنة BPM.</span><span class="sxs-lookup"><span data-stu-id="f4c10-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![عنصر العمل و حالة الاختبار](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="f4c10-303">تثبيت RSAT وتكوينه</span><span class="sxs-lookup"><span data-stu-id="f4c10-303">Install and Configure RSAT</span></span>

<span data-ttu-id="f4c10-304">يمكن تثبيت RSAT على أي جهاز كمبيوتر يعمل بنظام Windows 10 ويمكنه الاتصال بالبيئة عبر مستعرض الويب (Internet Explorer أو Google Chrome).</span><span class="sxs-lookup"><span data-stu-id="f4c10-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="f4c10-305">قبل تثبيت إصدار جديد من الأداة، نوصي بإلغاء تثبيت الإصدار السابق.</span><span class="sxs-lookup"><span data-stu-id="f4c10-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="f4c10-306">تثبيت شهادة مصادقة</span><span class="sxs-lookup"><span data-stu-id="f4c10-306">Install an authentication certificate</span></span>

<span data-ttu-id="f4c10-307">لتمكين المصادقة، يجب إنشاء شهادة وتثبيتها على الكمبيوتر نفسه الذي يعمل عليه RSAT.</span><span class="sxs-lookup"><span data-stu-id="f4c10-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="f4c10-308">إنشاء شهادة</span><span class="sxs-lookup"><span data-stu-id="f4c10-308">Generate a certificate</span></span>

1. <span data-ttu-id="f4c10-309">لإنشاء ملف شهادة، افتح نافذة Microsoft Windows PowerShell كمسؤول، وقم بتشغيل الأمر التالي.</span><span class="sxs-lookup"><span data-stu-id="f4c10-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="f4c10-310">افتح مدير الشهادات عن طريق إدخال **certlm.msc** في مربع الحوار **تشغيل**، وتأكد من إنشاء شهادة **شهادة الاختبار المؤتمت D365** ضمن **شخصي \> الشهادات**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4c10-311">تأكد من إدخال **certlm.msc**، وليس **certmgr.msc**، لأنه يتم تخزين الشهادات على الكمبيوتر المحلي.</span><span class="sxs-lookup"><span data-stu-id="f4c10-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![شهادة شهادة الاختبار المؤتمت D365](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="f4c10-313">انقر بزر الماوس الأيمن فوق الشهادة، ثم حدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="f4c10-314">انتقل إلى **الشهادات الجذر الموثوقة \> الشهادات**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![مجلد الشهادات ضمن مجلد الشهادات الجذر الموثوقة](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="f4c10-316">في القائمة **إجراء**، حدد **لصق** لنسخ الشهادة إلى موقع **الشهادات الجذر الموثوقة**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![أمر اللصق في قائمة الإجراء](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="f4c10-318">للحصول على بصمة الإبهام للشهادة المثبتة، ولكن دون مسافات أو أحرف خاصة، افتح نافذة Windows PowerShell كمسؤول، وقم بتشغيل الأوامر التالية.</span><span class="sxs-lookup"><span data-stu-id="f4c10-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="f4c10-319">احفظ بصمة الإبهام، لأنك ستحتاج إليها لاحقًا عند تحديث ملفات ‎.wif لخادم كائن التطبيق (AOS) وإعداد تكوين RSAT.</span><span class="sxs-lookup"><span data-stu-id="f4c10-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="f4c10-320">تكوين كمبيوتر AOS للثقة في الاتصال</span><span class="sxs-lookup"><span data-stu-id="f4c10-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="f4c10-321">إذا كانت البيئة من الطبقة 2+، فيجب تحديث بصمة الإبهام للشهادة في ملف wif.config **لكل** أجهزة كمبيوتر AOS للبيئة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-321">If the environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="f4c10-322">أسس اتصال بروتوكول سطح المكتب البعيد (RDP) بكمبيوتر AOS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="f4c10-323">تتوفر تفاصيل تسجيل الدخول في صفحة تفاصيل البيئة في LCS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="f4c10-324">افتح Microsoft Internet Information Services ‏(IIS)، وابحث عن **AOSService** في قائمة المواقع.</span><span class="sxs-lookup"><span data-stu-id="f4c10-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![AOSService في قائمة المواقع](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="f4c10-326">انقر بزر الماوس الأيمن فوق **استكشاف** لفتح المجلد **\<Drive\>: \\AosService\\WebRoot**:</span><span class="sxs-lookup"><span data-stu-id="f4c10-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="f4c10-327">ابحث عن المجلد **wif.config**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-327">Find the **wif.config** file.</span></span>

    ![ملف Wif.config في المجلد WebRoot](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="f4c10-329">قم بتحديث ملف **wif.config** عن طريق إضافة إدخال مرجع جديد لشهادة واسم المرجع، كما هو موضح في المثال التالي.</span><span class="sxs-lookup"><span data-stu-id="f4c10-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="f4c10-330">إذا كان العديد من المستخدمين يستخدمون التطبيق نفسه، فيجب على كل مستخدم إنشاء بصمات أصابع منفصلة، ويجب إضافة جميع بصمات الأصابع هذه في قسم **\<keys\>**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-330">If multiple users are using the same application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="f4c10-331">إذا كان هناك أكثر من كمبيوتر AOS واحد، فكرر الخطوات من 3 إلى 4 لكل كمبيوتر إضافي</span><span class="sxs-lookup"><span data-stu-id="f4c10-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4c10-332">بخلاف بيئات الطبقة 2 القديمة، يتم نشر بيئات الطبقة 2 الجديدة بمثيليّ AOS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="f4c10-333">شغِّل **iisreset** على جميع أجهزة كمبيوتر AOS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4c10-334">إذا لم يكن لديك حقوق المسؤول لتشغيل **iisreset** على كمبيوتر الطبقة 1، فحدد صيانة > إعادة تشغيل الخدمات من صفحة تفاصيل البيئة في LCS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="f4c10-335">بيئة الطبقة 2+</span><span class="sxs-lookup"><span data-stu-id="f4c10-335">Tier 2+ environment</span></span>

<span data-ttu-id="f4c10-336">إذا تم استخدام الطبقة 2+ (بيئة الاختبار المعزولة لاختبار القبول القياسي أو أعلى)، فتحقق من إعداد التسجيل التالي أو قم بتعيينه على الكمبيوتر حيث تم تثبيت RSAT.</span><span class="sxs-lookup"><span data-stu-id="f4c10-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="f4c10-337">فهذه الخطوة مطلوبة لأنها تساعدك على تجنب أخطاء المصادقة أو أخطاء اتصال RSAT.</span><span class="sxs-lookup"><span data-stu-id="f4c10-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="f4c10-338">تثبيت RSAT</span><span class="sxs-lookup"><span data-stu-id="f4c10-338">Install RSAT</span></span>

1. <span data-ttu-id="f4c10-339">انتقل إلى <https://www.microsoft.com/download/details.aspx?id=57357>، وحدد **تنزيل**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="f4c10-340">حدد جميع الملفات، ثم حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-340">Select all the files, and then select **Next**.</span></span>

    ![تحديد كل الملفات](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="f4c10-342">انقر نقرًا مزدوجًا فوق حزمة msi لتشغيل المثبِّت.</span><span class="sxs-lookup"><span data-stu-id="f4c10-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="f4c10-343">ثم، حدد إنهاء عند **اكتمال** التثبيت.</span><span class="sxs-lookup"><span data-stu-id="f4c10-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![ملف مثبِّت RSAT](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="f4c10-345">تثبيت برامج تشغيل Selenium والمستعرض</span><span class="sxs-lookup"><span data-stu-id="f4c10-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="f4c10-346">في الإصدارات القديمة من RSAT، كان عليك تثبيت برامج تشغيل Selenium والمستعرض.</span><span class="sxs-lookup"><span data-stu-id="f4c10-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="f4c10-347">لكنك لم تعد مضطرًا إلى تثبيت برامج التشغيل هذه لأنها مثبتة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="f4c10-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="f4c10-348">في المرة الأولى التي تفتح فيها RSAT، تتم مطالبتك بتنزيل Selenium وتثبيته تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="f4c10-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="f4c10-349">وللحصول على المزيد من المعلومات، راجع قسم [تكوين RSAT](#configure-rsat).</span><span class="sxs-lookup"><span data-stu-id="f4c10-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="f4c10-350">حتى تتمكن من تشغيل حالة اختبار، تتم مطالبتك بتنزيل وتثبيت برنامج تشغيل المستعرض الذي يتوافق مع المستعرض الافتراضي المحدد في تكوين RSAT تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="f4c10-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="f4c10-351">وللحصول على المزيد من المعلومات، راجع قسم [تحميل حالات الاختبار وتشغيلها](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="f4c10-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="f4c10-352">بدء استخدام RSAT</span><span class="sxs-lookup"><span data-stu-id="f4c10-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="f4c10-353">إنشاء خطة اختبار ومجموعة اختبار</span><span class="sxs-lookup"><span data-stu-id="f4c10-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="f4c10-354">انتقل إلى مشروع Azure DevOps، ثم حدد **خطط الاختبار**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![أمر خطط الاختبار](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="f4c10-356">حدد **خطة اختبار جديدة**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-356">Select **New Test Plan**.</span></span>

    ![زر خطة الاختبار الجديدة](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="f4c10-358">املأ حقل **الاسم**، ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="f4c10-359">بالنسبة لهذا البرنامج التعليمي، قم بتسمية خطة الاختبار **خطة اختبار RSAT**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![مربع حوار خطة الاختبار الجديدة](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="f4c10-361">حدد علامة الجمع(**+**)، ثم حدد **مجموعة ثابتة** لإنشاء مجموعة ثابتة ضمن خطة الاختبار الجديدة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="f4c10-362">وقم بتسمية مجموعة الاختبار الجديدة **T01 - إدراج في المخزون**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4c10-363">يمكنك أيضًا إنشاء مجموعة مستندة إلى الاستعلام، إذا كنت تريد سحب حالات الاختبار الجديدة من BPM تلقائيًا إلى مجموعة اختبار RSAT.</span><span class="sxs-lookup"><span data-stu-id="f4c10-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![إنشاء مجموعة ثابتة](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="f4c10-365">إرفاق حالات الاختبار إلى مجموعة الاختبار</span><span class="sxs-lookup"><span data-stu-id="f4c10-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="f4c10-366">حدد **إضافة موجود** من الجانب الأيسر لإضافة حالات اختبار موجودة إلى مجموعة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="f4c10-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![إضافة زر موجود](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="f4c10-368">في صفحة **إضافة حالات اختبار إلى المجموعة**، حدد **تشغيل الاستعلام**، ثم حدد حالة الاختبار لإضافتها إلى مجموعة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="f4c10-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="f4c10-369">وبالنسبة لهذا البرنامج التعليمي، حدد حالة الاختبار **إنشاء منتج جديد**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="f4c10-370">ثم حدد **إضافة حالات اختبار** في الركن الأيسر السفلي من الصفحة (لا يظهر هذا الزر في الرسم التوضيحي التالي).</span><span class="sxs-lookup"><span data-stu-id="f4c10-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![زر تشغيل الاستعلام](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="f4c10-372">تتم إضافة حالة الاختبار إلى مجموعة اختبار‬‏ **T01-إدراج في المخزون**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![تمت إضافة حالة الاختبار إلى مجموعة الاختبار](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="f4c10-374">تكوين RSAT</span><span class="sxs-lookup"><span data-stu-id="f4c10-374">Configure RSAT</span></span>

1. <span data-ttu-id="f4c10-375">افتح RSAT..</span><span class="sxs-lookup"><span data-stu-id="f4c10-375">Open RSAT.</span></span>

    ![أيقونة RSAT](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="f4c10-377">استلمت رسالة تحذير تنص على أن " أداة Regression Suite Automation Tool تتطلب وجود Selenium، فهل تريد تنزيله وتثبيته تلقائيًا الآن؟"</span><span class="sxs-lookup"><span data-stu-id="f4c10-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="f4c10-378">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-378">Select **Yes**.</span></span>

    ![رسالة تحذير](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="f4c10-380">حدد زر **الإعدادات** (رمز الترس) في الركن العلوي الأيسر، ثم املأ الحقول التالية في مربع الحوار الذي سيظهر:</span><span class="sxs-lookup"><span data-stu-id="f4c10-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="f4c10-381">**عنوان Url لـ Azure DevOps** – ادخل عنوان URL لمشروع Azure DevOps، مثل `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span><span class="sxs-lookup"><span data-stu-id="f4c10-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="f4c10-382">**رمز الوصول المميز** - أدخل رمز الوصول المميز الذي يتيح للأداة الاتصال بـ Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f4c10-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="f4c10-383">واستخدم رمز الوصول المميز الشخصي الذي قمت بإنشائه مسبقًا في هذا البرنامج التعليمي.</span><span class="sxs-lookup"><span data-stu-id="f4c10-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="f4c10-384">وللحصول على المزيد من المعلومات، راجع [مصادقة الوصول باستخدام رموز الوصول المميزة الشخصية](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span><span class="sxs-lookup"><span data-stu-id="f4c10-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="f4c10-385">**اسم المشروع** - حدد اسم مشروع Azure DevOps الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="f4c10-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="f4c10-386">**خطة الاختبار** - حدد خطة اختبار Azure DevOps التي تتضمن حالات الاختبار الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="f4c10-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="f4c10-387">للحصول على المزيد من المعلومات، راجع [إنشاء خطط اختبار ومجموعات اختبار](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span><span class="sxs-lookup"><span data-stu-id="f4c10-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="f4c10-388">وبعد تحديد خطة اختبار، حدد **اختبار الاتصال** لاختبار اتصالك بـ Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f4c10-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="f4c10-389">**اسم المضيف** - أدخل اسم المضيف لبيئة الاختبار، مثل **\<myaos\>.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-389">**Hostname** – Enter the host name of the test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="f4c10-390">لا تقم بتضمين البادئة **https://** أو **http://**</span><span class="sxs-lookup"><span data-stu-id="f4c10-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="f4c10-391">**اسم مضيف SOAP** - أدخل اسم مضيف SOAP لبيئة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="f4c10-391">**SOAP Hostname** – Enter the SOAP host name of the test environment.</span></span> <span data-ttu-id="f4c10-392">وعادةً ما يكون اسم مضيف SOAP هو اسم المضيف نفسه، ولكنه يحتوي على لاحقة **soap**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="f4c10-393">وفيما يلي مثال: **\<myaos\>soap.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="f4c10-394">لا تقم بتضمين البادئة **https://** أو **http://**</span><span class="sxs-lookup"><span data-stu-id="f4c10-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="f4c10-395">للبحث عن اسم المضيف واسم مضيف SOAP، افتح إدارة IIS، وانقر بزر الماوس الأيمن فوق **المواقع \> AOSService**, ثم حدد **تحرير الروابط**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="f4c10-396">وتمنحك القيم الموجودة في عمود **اسم المضيف** اسم المضيف واسم مضيف SOAP (يحتوي اسم مضيف SOAP على **soap** كلاحقة في عنوان URL).</span><span class="sxs-lookup"><span data-stu-id="f4c10-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![اسم المضيف واسم مضيف SOAP في عمود اسم المضيف](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="f4c10-398">**اسم المستخدم المسؤول** - أدخل عنوان البريد الإلكتروني لمستخدم مسؤول في بيئة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="f4c10-398">**Admin user name** – Enter the email address of an admin user in the test environment.</span></span>
    - <span data-ttu-id="f4c10-399">**بصمة الإبهام** - أدخل بصمة الإبهام لشهادة المصادقة، كما هو موضح سابقًا في هذا البرنامج التعليمي.</span><span class="sxs-lookup"><span data-stu-id="f4c10-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="f4c10-400">**دليل العمل** - حدد موقع المجلد لتخزين ملفات أتمتة الاختبار، مثل ملفات بيانات اختبار Excel.</span><span class="sxs-lookup"><span data-stu-id="f4c10-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="f4c10-401">على سبيل المثال، أدخل أو حدد **C:\\Temp\\RegressionTool**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="f4c10-402">إذا كان اسم المجلد يتضمن مسافات، فسيفشل التنفيذ بسبب تعذر العثور على المجلد.</span><span class="sxs-lookup"><span data-stu-id="f4c10-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="f4c10-403">هذه المشكلة معروفة وسنعمل على إصلاحها في أحدث إصدار من الأداة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="f4c10-404">**المستعرض الافتراضي** - حدد إما **Internet Explorer** وإما **Google Chrome**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="f4c10-405">تأكد من تثبيت برامج تشغيل المستعرض المناسبة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="f4c10-406">**مهلة تشغيل الاختبار** - حدد فترة المهلة، بالدقائق، لعمليات تشغيل الاختبار.</span><span class="sxs-lookup"><span data-stu-id="f4c10-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="f4c10-407">وعندما تنقضي فترة المهلة، تُغلق جميع النوافذ النشطة وتفشل حالات الاختبار المعلقة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="f4c10-408">**مهلة إجراء الاختبار** - يتحكم هذا الحقل في فترة المهلة، بالدقائق، لطلبات خادم بيئة Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="f4c10-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="f4c10-409">وعادة، يجب أن تكون القيمة الافتراضية (دقيقتان) كافية.</span><span class="sxs-lookup"><span data-stu-id="f4c10-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="f4c10-410">ومع ذلك، بالنسبة للبيئات الأبطأ، فقد ترغب في زيادة القيمة في حالة حدوث أخطاء مرتبطة بالوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="f4c10-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="f4c10-411">**اسم الشركة** - أدخل اسم الشركة لاستخدامها كشركتك الافتراضية عند إنشاء ملفات معلمات Excel.</span><span class="sxs-lookup"><span data-stu-id="f4c10-411">**Company name** – Enter the company name to use as your default company when Excel parameter files are created.</span></span> <span data-ttu-id="f4c10-412">ويمكنك تغيير الشركة لاحقًا عن طريق تحرير ملف المعلمة Excel.</span><span class="sxs-lookup"><span data-stu-id="f4c10-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![مربع حوار الإعدادات](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="f4c10-414">حدد **تطبيق** لتطبيق الإعدادات الخاصة بك وحفظها.</span><span class="sxs-lookup"><span data-stu-id="f4c10-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="f4c10-415">لحفظ الإعدادات الحالية في ملف تكوين على جهاز الكمبيوتر لديك، حدد **حفظ باسم**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="f4c10-416">ولاستعادة إعداداتك من ملف التكوين على جهاز الكمبيوتر، حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="f4c10-417">حدد **إغلاق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="f4c10-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="f4c10-418">تحميل حالات الاختبار وتشغيلها</span><span class="sxs-lookup"><span data-stu-id="f4c10-418">Load and run test cases</span></span>

1. <span data-ttu-id="f4c10-419">حدد تحميل **لتحميل** خطة الاختبار الخاصة **بخطة اختبار RSAT** من مشروع Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f4c10-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![زر التحميل](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="f4c10-421">حدد **إنشاء حالة اختبار منتج جديد** من مجموعة الاختبار، ثم حدد **جديد \> إنشاء اختبار التنفيذ وملفات المعلمة**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![إنشاء أمر اختبار تنفيذ وملفات معلمة في القائمة جديد](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="f4c10-423">يتم إنشاء ملف معلمة Excel في المجلد المحلي الذي حددته في تكوين RSAT (على سبيل المثال، **C:\\Temp\\RegressionTool**).</span><span class="sxs-lookup"><span data-stu-id="f4c10-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![تم إنشاء ملف معلمة Excel](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="f4c10-425">إذا كنت تريد حفظ ملفات المعلمات، فحدد **تحميل**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="f4c10-426">يتم تحميل ملفات أتمتة الاختبار لجميع حالات الاختبار المحددة إلى Azure DevOps للاستخدام في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="f4c10-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="f4c10-427">(تتضمن هذه الملفات ملفات معلمات اختبار Excel.)</span><span class="sxs-lookup"><span data-stu-id="f4c10-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="f4c10-428">يمكنك بهذه الطريقة تحديد **تحميل** لتحميل ملفات المعلمات (وملفات الأتمتة) من حالة الاختبار مباشرة من Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f4c10-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="f4c10-429">ولا يجب عليك إعادة إنشاء ملفات المعلمات.</span><span class="sxs-lookup"><span data-stu-id="f4c10-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="f4c10-430">وسيصبح هذا النهج مهمًا في لاحقًا، عندما تريد الاحتفاظ بالتعديلات في ملف المعلمة ولا تريد استبدالها.</span><span class="sxs-lookup"><span data-stu-id="f4c10-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="f4c10-431">للتحقق من حفظ ملفات الأتمتة وملفات المعلمات في Azure DevOps، انتقل إلى مشروع Azure DevOps، وحدد **لوحات البيانات \> أصناف العمل**، ثم حدد حالة الاختبار **إنشاء منتج جديد**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="f4c10-432">من علامة التبويب **المرفقات**، ستظهر أربعة ملفات:</span><span class="sxs-lookup"><span data-stu-id="f4c10-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="f4c10-433">**.cs** – C\# ملف أتمتة C#</span><span class="sxs-lookup"><span data-stu-id="f4c10-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="f4c10-434">**.dll** – ملف أتمتة مترجم كتجميع</span><span class="sxs-lookup"><span data-stu-id="f4c10-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="f4c10-435">**.xlsx** – ملف معلمة Excel</span><span class="sxs-lookup"><span data-stu-id="f4c10-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="f4c10-436">**.xml** – ملف التسجيل</span><span class="sxs-lookup"><span data-stu-id="f4c10-436">**.xml** – Recording file</span></span>

    ![الملفات الموجودة في علامة التبويب "المرفقات"](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="f4c10-438">حدد حالة الاختبار المطلوب تشغيلها، ثم حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4c10-439">قبل تشغيل حالات الاختبار، إذا كنت تستخدم Internet Explorer كمستعرض، فتأكد من ضبط دقة سطح المكتب على **100٪** في **إعدادات عرض Windows \> تغيير الحجم والتخطيط**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="f4c10-440">وإذا لم تتمكن من تغيير هذا الإعداد على جهاز ظاهري (VM)، فقم بتغييره على (الكمبيوتر المحمول) للعميل الذي تحاول الوصول إلى VM منه.</span><span class="sxs-lookup"><span data-stu-id="f4c10-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="f4c10-441">ويتم عندئذ توريث إعدادات الدقة من قِبل إعدادات عرض VM.</span><span class="sxs-lookup"><span data-stu-id="f4c10-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![يتم تعيين دقة سطح المكتب إلى 100%](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="f4c10-443">إذا لم يتم تثبيت برامج تشغيل المستعرض في النظام، فستتلقى رسالة تحذير تنص على أن "هذه العملية تتطلب برنامج التشغيل \<اسم المستعرض\>.</span><span class="sxs-lookup"><span data-stu-id="f4c10-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="f4c10-444">هل تريد تنزيله وتثبيته تلقائيًا الآن؟ "</span><span class="sxs-lookup"><span data-stu-id="f4c10-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="f4c10-445">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-445">Select **Yes**.</span></span>

    ![رسالة تحذير من أجل Internet Explorer](./media/setup_rsa_tool_69.png)

    ![رسالة تحذير من أجل Chrome](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="f4c10-448">إذا كنت تستخدم Chrome كمستعرض وتلقيت رسالة خطأ تنص على أنه لم يتم إنشاء الجلسة لأن إصدار Chrome غير صحيح، فقم بتنزيل أحدث برنامج تشغيل Chrome من <http://chromedriver.chromium.org/downloads> إلى المجلد **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![رسالة خطأ من أجل Chrome](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="f4c10-450">يتم تشغيل حالة الاختبار، ويتم تحديث حقل **النتيجة**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-450">The test case is run, and the **Result** field is updated.</span></span>

    ![مؤشر التقدم](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="f4c10-452">إذا اتبعت هذا البرنامج التعليمي أثناء كتابته، فستفشل حالة الاختبار **إنشاء منتج جديد**، لأن تسجيل المهام لإنشاء منتج قد حفظ اسم المنتج كقيمة برمجية مضمّنة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="f4c10-453">وإذا قمت بإعادة تشغيل حالة الاختبار نفسها، يجب أن تتلقى رسالة خطأ، لأن المنتج موجود بالفعل.</span><span class="sxs-lookup"><span data-stu-id="f4c10-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![تم تعيين حقل النتيجة إلى "فشل"](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="f4c10-455">عرض نتائج الاختبار</span><span class="sxs-lookup"><span data-stu-id="f4c10-455">View the test results</span></span>

1. <span data-ttu-id="f4c10-456">انقر نقرًا مزدوجًا فوق حالة الاختبار الفاشلة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="f4c10-457">ستتلقى رسالة خطأ</span><span class="sxs-lookup"><span data-stu-id="f4c10-457">You receive an error message.</span></span>

    ![رسالة الخطأ](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="f4c10-459">حدد **التفاصيل** لعرض رسالة الخطأ بالكامل.</span><span class="sxs-lookup"><span data-stu-id="f4c10-459">Select **Details** to view the whole error message.</span></span>

    ![رسالة الخطأ بالكامل](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="f4c10-461">لعرض نسخة مفصلة من رسالة الخطأ في Azure DevOps، حدد **فتح في Azure DevOps**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="f4c10-462">في Azure DevOps، يمكنك عرض الحالة الخاصة بحالة الاختبار ورسالة الخطأ المفصلة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![رسالة خطأ مفصلة في Azure DevOps](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="f4c10-464">لعرض نتائج الاختبار مباشرة في مشروع Azure DevOps، انتقل إلى **خطط الاختبار \> خطط الاختبار \> عمليات التشغيل**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="f4c10-465">انقر نقرًا مزدوجًا فوق تشغيل الاختبار الذي تريد رؤية المزيد من التفاصيل عنه.</span><span class="sxs-lookup"><span data-stu-id="f4c10-465">Double-click the test run that you want to see more details for.</span></span>

    ![قائمة عمليات تشغيل الاختبارات في Azure DevOps](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="f4c10-467">تشير علامة التبويب **تشغيل الملخص** إلى فشل حالة الاختبار، لكنها لا تقدم رسالة الخطأ الفعلية.</span><span class="sxs-lookup"><span data-stu-id="f4c10-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="f4c10-468">لعرض رسالة الخطأ المفصلة، حدد علامة التبويب **نتائج الاختبار**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![علامة التبويب "تشغيل الملخص"](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="f4c10-470">توفر علامة التبويب **نتائج الاختبار** معلومات حالة الاختبار، إلى جانب النتيجة ورسالة الخطأ.</span><span class="sxs-lookup"><span data-stu-id="f4c10-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![علامة التبويب "نتائج الاختبار"](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="f4c10-472">انقر نقرًا مزدوجًا فوق السجل المعني لعرض رسالة الخطأ المفصلة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![رسالة خطأ مفصلة](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="f4c10-474">تتوفر أيضًا جميع رسائل الخطأ محليًا في **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="f4c10-475">يمكنك أيضًا تصدير نتائج تشغيل الاختبار من مستوى خطة الاختبار عن طريق تحديد **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![تصدير خطة اختبار](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="f4c10-477">تعديل ملف معلمة Excel</span><span class="sxs-lookup"><span data-stu-id="f4c10-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="f4c10-478">افتح RSAT..</span><span class="sxs-lookup"><span data-stu-id="f4c10-478">Open RSAT.</span></span>
2. <span data-ttu-id="f4c10-479">حدد حالات الاختبار، ثم حدد **تحرير** لفتح ملفات معلمة Excel.</span><span class="sxs-lookup"><span data-stu-id="f4c10-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="f4c10-480">في الورقة **EcoResProductCreate**، لاحظ أن قيمة حقل **رقم المنتج** هي قيمة برمجية مضمّنة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="f4c10-481">ويجب تحديث هذا الحقل إلى رقم منتج جديد قبل تشغيل حالة الاختبار مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="f4c10-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="f4c10-482">لإنشاء رقم منتج فريد لكل عملية تشغيل دون الحاجة إلى إعادة فتح ملف معلمة Excel وتحديث رقم المنتج يدويًا في كل مرة، استخدم معادلة Excel التالية.</span><span class="sxs-lookup"><span data-stu-id="f4c10-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="f4c10-483">بالإضافة إلى علامة التبويب **عام**، يحتوي ملف معلمة Excel على علامة تبويب بيانات لكل صفحة نموذج تقوم حالة الاختبار بزيارتها.</span><span class="sxs-lookup"><span data-stu-id="f4c10-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every form page the test case visits.</span></span>

    ![حقل رقم المنتج](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="f4c10-485">حدد **حفظ**، ثم قم بإغلاق مصنف Excel.</span><span class="sxs-lookup"><span data-stu-id="f4c10-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="f4c10-486">حدد **تحميل** لحفظ ملف معلمة Excel إلى Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f4c10-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![رسالة التحميل بنجاح](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="f4c10-488">لتشغيل حالات الاختبار في سياق مستخدم معين، أدخل معرف البريد الإلكتروني للمستخدم في حقل **مستخدم الاختبار** في علامة التبويب **عام** لملف معلمة Excel.</span><span class="sxs-lookup"><span data-stu-id="f4c10-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="f4c10-489">وفي أحدث إصدار من RSAT، تم تحديث تخطيط الحقول في ملف معلمة Excel، لكن ظل المفهوم كما هو.</span><span class="sxs-lookup"><span data-stu-id="f4c10-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![حقل مستخدم الاختبار](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="f4c10-491">التحقق من صحة النتائج</span><span class="sxs-lookup"><span data-stu-id="f4c10-491">Validate the results</span></span>

- <span data-ttu-id="f4c10-492">حدد **تشغيل** لإعادة تشغيل حالة الاختبار، وتحقق من ‏‫اجتياز‬ حالة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="f4c10-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="f4c10-493">ويمكنك عرض نتائج الاختبار كما هو موضح في قسم [عرض نتائج الاختبار](#view-the-test-results).</span><span class="sxs-lookup"><span data-stu-id="f4c10-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![تم تعيين حقل النتيجة إلى "‏‫تم الاجتياز‬"](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="f4c10-495">تسلسل حالات الاختبار</span><span class="sxs-lookup"><span data-stu-id="f4c10-495">Chaining of test cases</span></span>

<span data-ttu-id="f4c10-496">تتمثل إحدى الميزات الرئيسية لـ RSAT في تسلسل حالات الاختبار (أي، قدرة الاختبار على اجتياز القيم إلى اختبارات أخرى).</span><span class="sxs-lookup"><span data-stu-id="f4c10-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="f4c10-497">ويتم تشغيل حالات الاختبار وفقًا لترتيبها المحدد في خطة اختبار Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f4c10-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="f4c10-498">(يمكن أيضًا تحديث هذا الطلب في أداة الاختبار نفسها.) لذا إذا كنت تريد اجتياز المتغيرات من حالة اختبار إلى أخرى، فمن المهم جدًا أن تكون الاختبارات بالترتيب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="f4c10-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="f4c10-499">في هذا القسم، ستقوم بإنشاء متغير محفوظ في حالة الاختبار الأول وإنشاء حالة اختبار ثانية واجتياز المتغير المحفوظ من حالة الاختبار الأولى إلى حالة الاختبار الثانية.</span><span class="sxs-lookup"><span data-stu-id="f4c10-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="f4c10-500">وستقوم بعد ذلك بتشغيل حالات الاختبار كحالة اختبار متسلسلة في RSAT.</span><span class="sxs-lookup"><span data-stu-id="f4c10-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="f4c10-501">تعديل تسجيل مهام موجود لإنشاء متغير محفوظ</span><span class="sxs-lookup"><span data-stu-id="f4c10-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="f4c10-502">افتح العميل.</span><span class="sxs-lookup"><span data-stu-id="f4c10-502">Open the client.</span></span>
2. <span data-ttu-id="f4c10-503">حدد زر **الإعدادات** (رمز الترس)، ثم حدد **مسجل المهام**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="f4c10-504">حدد **تحرير التسجيل**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-504">Select **Edit Recording**.</span></span>

    ![زر تحرير التسجيل](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="f4c10-506">حدد **فتح من Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-506">Select **Open from Lifecycle Services**.</span></span>

    ![زر الفتح من Lifecycle Services](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="f4c10-508">حدد **تحديد مكتبة Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-508">Select **Select the Lifecycle Services library**.</span></span>

    ![زر تحديد مكتبة Lifecycle Services](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="f4c10-510">يتم تحميل مكتبات BPM من LCS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-510">BPM libraries are loaded from LCS.</span></span>

    ![مؤشر التقدم](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="f4c10-512">بعد تحميل مكتبات BPM من LCS، حدد مكتبة **RSAT** BPM وعملية الأعمال **إنشاء منتج أعمال جديد** التي كان تسجيل المهام مقترنًا بها .</span><span class="sxs-lookup"><span data-stu-id="f4c10-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="f4c10-513">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-513">Then select **OK**.</span></span>

    ![تحديد مكتبة BPM وعملية أعمال](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="f4c10-515">يتم إدخال اسم تسجيل المهام المناسب في حقل **اسم التسجيل**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="f4c10-516">حدد **بدء**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-516">Select **Start**.</span></span>

    ![اسم تسجيل المهام في الحقل "اسم التسجيل"](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="f4c10-518">انتقل إلى **إدارة معلومات المنتجات \> المنتجات**، وحدد **جديد** لفتح الصفحة التي تم فيها تسجيل المهمة الأصلية، **إنشاء منتج**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="f4c10-519">حدد **إدراج خطوه**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4c10-520">يتم إدراج الخطوة الجديدة **بعد** الخطوة التي حددتها في الجزء.</span><span class="sxs-lookup"><span data-stu-id="f4c10-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![زر إدراج خطوة](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="f4c10-522">انقر بزر الماوس الأيمن فوق الحقل **رقم المنتج**، ثم حدد **مسجل المهام \> نسخ**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![أمر النسخ](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="f4c10-524">تمت إضافة خطوة جديدة في الجزء.</span><span class="sxs-lookup"><span data-stu-id="f4c10-524">A new step is added in the pane.</span></span> <span data-ttu-id="f4c10-525">قم بتدوين القيمة في الحقل **رقم المنتج**، لأنك ستحتاج إليها لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="f4c10-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![تمت إضافة خطوة جديدة](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="f4c10-527">حدد **تم التحرير**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="f4c10-528">حدد  **حفظ إلى Lifecycle Services**، وقم بإقران تسجيل المهام الجديدة بمكتبة BPM نفسها وعملية الأعمال التي اقترن بها تسجيل المهام الأصلي.</span><span class="sxs-lookup"><span data-stu-id="f4c10-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="f4c10-529">للحصول على المزيد من المعلومات، راجع قسم [إنشاء تسجيل المهام وحفظها في قسم مكتبة BPM](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="f4c10-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="f4c10-530">انتقل إلى مكتبة BPM، وحدد **مزامنة حالات الاختبار** لاستبدال تسجيل المهام المرفق بحالة الاختبار في Azure DevOps، كما هو موضح في قسم [اختبار المزامنة من BPM إلى Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="f4c10-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="f4c10-531">افتح RSAT، وحدد **تحميل** لإعادة تحميل كل حالات الاختبار الموجودة في مجموعة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="f4c10-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="f4c10-532">ويجب إعادة إنشاء ملفات الأتمتة والمعلمات من أجل توفير حالة الاختبار المناسبة عن طريق تحديد حالة الاختبار ثم تحديد **جديد \> إنشاء ملفات اختبار التنفيذ والمعلمات**، كما هو موضح في قسم [حالات اختبار التحميل والتشغيل](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="f4c10-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4c10-533">إذا تم ترك ملف معلمة Excel مفتوحًا، فستفشل عملية التجديد.</span><span class="sxs-lookup"><span data-stu-id="f4c10-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="f4c10-534">لذا تأكد من إغلاق ملف معلمة Excel لحالة الاختبار قبل إنشاء ملف معلمة Excel الجديد.</span><span class="sxs-lookup"><span data-stu-id="f4c10-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="f4c10-535">حدد **تحرير** لفتح ملف معلمة Excel الجديد.</span><span class="sxs-lookup"><span data-stu-id="f4c10-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="f4c10-536">وستشاهد إدخالًا **متغيرِّا جديدًا محفوظًا** عبر الإنترنت في السطر 9.</span><span class="sxs-lookup"><span data-stu-id="f4c10-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="f4c10-537">يتم حفظ هذا المتغير، **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**، في ملف XML الخاص بتسجيل المهام ويمكن استخدامه في الاختبارات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![إدخال المتغير المحفوظ](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="f4c10-539">إنشاء حالة اختبار جديدة</span><span class="sxs-lookup"><span data-stu-id="f4c10-539">Create a new test case</span></span>

1. <span data-ttu-id="f4c10-540">انتقل إلى مكتبة **RSAT** BPM</span><span class="sxs-lookup"><span data-stu-id="f4c10-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="f4c10-541">حدد عملية **نموذج عملية أعمال الدعم**، ثم، على اليسار، حدد **وضع التحرير**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="f4c10-542">قم بتغيير قيمة حقل **الاسم** وحقل **الوصف** **لإصدار منتج**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="f4c10-543">ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-543">Then select **Save**.</span></span>

    ![تم تغيير الاسم والوصف لإصدار منتج](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="f4c10-545">إنشاء تسجيل مهام جديدة لها وظيفة التحقق من الصحة</span><span class="sxs-lookup"><span data-stu-id="f4c10-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="f4c10-546">قم بإنشاء تسجيل مهام لتحرير المنتج الذي تم إنشاؤه مسبقًا إلى الكيان القانوني USRT.</span><span class="sxs-lookup"><span data-stu-id="f4c10-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="f4c10-547">للحصول على المزيد من المعلومات، راجع قسم [إنشاء تسجيل المهام وحفظها في قسم مكتبة BPM](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="f4c10-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4c10-548">بالنسبة لحالات الاختبار المتسلسلة، نوصي دائمًا بالعثور على السجل الذي تحتاجه أو تصفيته عن طريق *كتابة قيمة الحقل يدويًا*.</span><span class="sxs-lookup"><span data-stu-id="f4c10-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="f4c10-549">وبهذه الطريقة، يمكن للأداة تحديد السجل الذي يجب اتخاذ الإجراء ضده في حالة الاختبار اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="f4c10-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![تسجيل مهام جديدة لها وظيفة التحقق من الصحة](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="f4c10-551">كما يوضح الرسم التوضيحي السابق، بعد العثور على المنتج باستخدام عامل التصفية السريع، ولكن قبل تحديد **إصدار المنتجات**، يجب أن تتحقق من قيمة حقل **رقم المنتج** للتأكد من أن معرف المنتج هو معرف المنتج الذي تم إنشاؤه مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="f4c10-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="f4c10-552">وللتحقق من صحة القيمة، انقر بزر الماوس الأيمن على حقل **رقم المنتج**، ثم حدد **مسجل المهام \> التحقق من الصحة \> القيمة الحالية**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![التحقق من صحة القيمة الحالية](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="f4c10-554">احفظ تسجيلات المهام إلى BPM</span><span class="sxs-lookup"><span data-stu-id="f4c10-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="f4c10-555">بعد اكتمال تسجيل المهام، حدد **حفظ إلى Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![خيارات الحفظ](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="f4c10-557">يتم تحميل معلومات المكتبة من LCS.</span><span class="sxs-lookup"><span data-stu-id="f4c10-557">Library information is loaded from LCS.</span></span>

    ![مؤشر التقدم](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="f4c10-559">حدد مكتبة BPM لإقران تسجيل المهام بها.</span><span class="sxs-lookup"><span data-stu-id="f4c10-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="f4c10-560">بالنسبة لهذا البرنامج التعليمي، حدد مكتبة **RSAT** BPM التي تم إنشاؤها مسبقًا وعملية أعمال **إصدار منتج** ضمنها.</span><span class="sxs-lookup"><span data-stu-id="f4c10-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="f4c10-561">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="f4c10-562">مزامنة BPM إلى Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="f4c10-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="f4c10-563">انتقل إلى مكتبة BPM، وافتح مكتبة **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="f4c10-564">حدد **مزامنة VSTS** ثم **مزامنة حالات الاختبار**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="f4c10-565">للحصول على المزيد من المعلومات، راجع قسم [اختبار المزامنة من BPM إلى Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="f4c10-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="f4c10-566">بعد اكتمال المزامنة سيظهر عنصر العمل الجديد وحالة الاختبار المقابلة لعملية الأعمال **إصدار منتج** في Azure DevOps في **لوحات المعلومات \> عناصر العمل**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="f4c10-567">إضافة حالة الاختبار الجديدة إلى مجموعة الاختبار الحالية</span><span class="sxs-lookup"><span data-stu-id="f4c10-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="f4c10-568">انتقل إلى **خطط الاختبار \> خطط الاختبار**، وحدد خطة **خطة اختبار RSAT**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="f4c10-569">حدد **إضافة موجود**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="f4c10-570">في الصفحة **إضافة حالات اختبار إلى مجموعة**، حدد **تشغيل الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="f4c10-571">حدد حالة الاختبار الجديدة التي تم إنشاؤها **لإصدار منتج**، ثم حدد **إضافة حالات اختبار** في الركن الأيسر السفلي من الصفحة (لا يظهر هذا الزر في الرسم التوضيحي التالي).</span><span class="sxs-lookup"><span data-stu-id="f4c10-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![صفحة "إضافة حالات اختبار إلى مجموعة"](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="f4c10-573">لدي مجموعة الاختبار الآن حالتي اختبار.</span><span class="sxs-lookup"><span data-stu-id="f4c10-573">The test suite now has two test cases.</span></span>

    ![توجد حالتا اختبار الآن في مجموعة الاختبار.](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="f4c10-575">تحميل حالات الاختبار إلى RSAT</span><span class="sxs-lookup"><span data-stu-id="f4c10-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="f4c10-576">افتح RSAT، وحدد **تحميل**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="f4c10-577">يتم تحميل حالات الاختبار، وستتلقى تحذيرًا ينص على ما يلي: "هذا الإجراء سيحل محل ملفات بيانات اختبار Excel، وستفقد التغييرات المحلية.</span><span class="sxs-lookup"><span data-stu-id="f4c10-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="f4c10-578">فهل تريد المتابعة?"</span><span class="sxs-lookup"><span data-stu-id="f4c10-578">Do you want to proceed?"</span></span> <span data-ttu-id="f4c10-579">حدد **نعم** لتحديث ملفات معلمات Excel في النظام المحلي ولكن ليس ملفات معلمات Excel التي تم تحميلها إلى Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f4c10-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![رسالة تحذير](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="f4c10-581">يتم تحميل حالتي الاختبار، إلى جانب ملف معلمة Excel لحالة الاختبار الأولى.</span><span class="sxs-lookup"><span data-stu-id="f4c10-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="f4c10-582">ونظرًا لأنك حددت **تحميل** في آخر عملية تشغيل، سيتم سحب ملفات المعلمات من Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f4c10-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![تم تحميل حالات الاختبار](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="f4c10-584">حدد حالة الاختبار الثانية فقط، ثم حدد **جديد \> إنشاء ملفات تنفيذ الاختبار والمعلمة**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="f4c10-585">تحرير ملف معلمة Excel</span><span class="sxs-lookup"><span data-stu-id="f4c10-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="f4c10-586">حدد حالة الاختبار الثانية فقط، ثم حدد **تحرير** لفتح ملف معلمة Excel المقابل.</span><span class="sxs-lookup"><span data-stu-id="f4c10-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="f4c10-587">انسخ المتغير المحفوظ **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (راجع قسم [تعديل تسجيل مهام موجودة لإنشاء متغير محفوظ](#modify-an-existing-task-recording-to-create-a-saved-variable)) من حالة الاختبار الأولى إلى جميع الحقول التي يتم استخدام رقم المنتج فيها.</span><span class="sxs-lookup"><span data-stu-id="f4c10-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="f4c10-588">وفي هذه الحالة، يمكنك نسخ المتغير إلى حقل **رقم المنتج** وحقل **التحقق من صحة رقم المنتج** في الورقة **EcoResProductListPage**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![حقل رقم المنتج وحقل التحقق من صحة رقم المنتج](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="f4c10-590">يمكن اجتياز المتغيرات بين الاختبارات فقط أثناء تشغيل الاختبار نفسه.</span><span class="sxs-lookup"><span data-stu-id="f4c10-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="f4c10-591">ويجب أن تطابق أسماء المتغيرات تطابقًا تامًا.</span><span class="sxs-lookup"><span data-stu-id="f4c10-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="f4c10-592">حدد **حفظ**، ثم قم بإغلاق مصنف Excel.</span><span class="sxs-lookup"><span data-stu-id="f4c10-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="f4c10-593">حدد **تحميل** لحفظ التغييرات التي أجريتها على ملف معلمة Excel.</span><span class="sxs-lookup"><span data-stu-id="f4c10-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="f4c10-594">تشغيل حالات الاختبار المتسلسلة</span><span class="sxs-lookup"><span data-stu-id="f4c10-594">Run the chained test cases</span></span>

1. <span data-ttu-id="f4c10-595">حدد كلتا الحالتين، ثم حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="f4c10-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="f4c10-596">تحقق من اجتياز كلتا حالتي الاختبار.</span><span class="sxs-lookup"><span data-stu-id="f4c10-596">Verify that both test cases have passed.</span></span>

    ![تم تعيين حقل النتيجة إلى تم الاجتياز لكلتا حالتي الاختبار](./media/setup_rsa_tool_105.png)
