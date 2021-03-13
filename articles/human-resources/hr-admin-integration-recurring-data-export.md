---
title: إنشاء تطبيق تصدير بيانات متكررة
description: يوضح هذا المقال كيفية إنشاء تطبيق Microsoft Azure Logic الذي يقوم بتصدير البيانات من Microsoft Dynamics 365 Human Resources على جدول متكرر.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 97972d2179c42e9d2d672cbebb75643ef0a02a62
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111312"
---
# <a name="create-a-recurring-data-export-app"></a><span data-ttu-id="bc59c-103">إنشاء تطبيق تصدير بيانات متكررة</span><span class="sxs-lookup"><span data-stu-id="bc59c-103">Create a recurring data export app</span></span>

<span data-ttu-id="bc59c-104">يوضح هذا المقال كيفية إنشاء تطبيق Microsoft Azure Logic الذي يقوم بتصدير البيانات من Microsoft Dynamics 365 Human Resources على جدول متكرر.</span><span class="sxs-lookup"><span data-stu-id="bc59c-104">This article shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 Human Resources on a recurring schedule.</span></span> <span data-ttu-id="bc59c-105">يستفيد البرنامج التعليمي من واجهة برمجة تطبيقات REST لحزمة Human Resources' DMF لتصدير البيانات.</span><span class="sxs-lookup"><span data-stu-id="bc59c-105">The tutorial takes advantage of Human Resources' DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="bc59c-106">بعد تصدير البيانات، يحفظ تطبيق logic حزمة البيانات المصدرة إلى Microsoft OneDrive إلى مجلد Business.</span><span class="sxs-lookup"><span data-stu-id="bc59c-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="bc59c-107">سيناريو الأعمال</span><span class="sxs-lookup"><span data-stu-id="bc59c-107">Business scenario</span></span>

<span data-ttu-id="bc59c-108">في أحد سيناريوهات العمل النموذجية لعمليات تكامل Microsoft Dynamics 365، يجب تصدير البيانات إلى نظام نهائي على جدول متكرر.</span><span class="sxs-lookup"><span data-stu-id="bc59c-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="bc59c-109">يظهر هذا البرنامج التعليمي كيفية تصدير كافة سجلات العمال من Microsoft Dynamics 365 Human Resources وحفظ قائمة العمال في OneDrive لمجلد Business.</span><span class="sxs-lookup"><span data-stu-id="bc59c-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 Human Resources and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="bc59c-110">تمثل البيانات المُحددة التي يتم تصديرها في هذا البرنامج التعليمي ووجهة البيانات المُصدرة أمثلة فقط.</span><span class="sxs-lookup"><span data-stu-id="bc59c-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="bc59c-111">يُمكنك تغييرها بسهولة لتلبي احتياجات أعمالك.</span><span class="sxs-lookup"><span data-stu-id="bc59c-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="bc59c-112">التقنيات المستخدمة</span><span class="sxs-lookup"><span data-stu-id="bc59c-112">Technologies used</span></span>

<span data-ttu-id="bc59c-113">يستخدم هذا البرنامج التعليمي التقنيات التالية:</span><span class="sxs-lookup"><span data-stu-id="bc59c-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="bc59c-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – مصدر البيانات الرئيسية للعمال الذين سوف يتم تصديرهم.</span><span class="sxs-lookup"><span data-stu-id="bc59c-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="bc59c-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** - التقنية التي توفر خدمات التنسيق والجدولة للتصدير المتكرر.</span><span class="sxs-lookup"><span data-stu-id="bc59c-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="bc59c-116">**[الموصلات](https://docs.microsoft.com/azure/connectors/apis-list)** – التقنية المستخدمة لربط تطبيق logic بنقاط النهاية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="bc59c-116">**[Connectors](https://docs.microsoft.com/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="bc59c-117">[HTTP مع موصل Azure AD](https://docs.microsoft.com/connectors/webcontents/)</span><span class="sxs-lookup"><span data-stu-id="bc59c-117">[HTTP with Azure AD](https://docs.microsoft.com/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="bc59c-118">موصل [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)</span><span class="sxs-lookup"><span data-stu-id="bc59c-118">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="bc59c-119">**[واجهة برمجة تطبيقات REST لحزمة DMF](../dev-itpro/data-entities/data-management-api.md)** - التقنية المستخدمة لتشغيل التصدير ومراقبة تقدمه. </span><span class="sxs-lookup"><span data-stu-id="bc59c-119">**[DMF package REST API](../dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="bc59c-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** - وجهة العاملين المُصدرين.</span><span class="sxs-lookup"><span data-stu-id="bc59c-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bc59c-121">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="bc59c-121">Prerequisites</span></span>

<span data-ttu-id="bc59c-122">قبل البدء في التدريب في هذا البرنامج التعليمي، يجب أن يكون لديك العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="bc59c-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="bc59c-123">بيئة Human Resources التي لها أذونات على مستوى المسؤول في البيئة</span><span class="sxs-lookup"><span data-stu-id="bc59c-123">A Human Resources environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="bc59c-124">[اشتراك Azure](https://azure.microsoft.com/free/) لاستضافة تطبيق logic.</span><span class="sxs-lookup"><span data-stu-id="bc59c-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="bc59c-125">التمرين</span><span class="sxs-lookup"><span data-stu-id="bc59c-125">The exercise</span></span>

<span data-ttu-id="bc59c-126">في نهاية هذا التدريب، سوف يكون لديك تطبيق logic متصل ببيئة Human Resources الخاصة بك وحساب OneDrive for Business.</span><span class="sxs-lookup"><span data-stu-id="bc59c-126">At the end of this exercise, you will have a logic app that is connected to your Human Resources environment and your OneDrive for Business account.</span></span> <span data-ttu-id="bc59c-127">سوف يقوم تطبيق logic بتصدير حزمة البيانات من Human Resources، والانتظار حتى اكتمال التصدير وتنزيل حزمة البيانات المصدرة وحفظ حزمة البيانات في مجلد OneDrive for Business الذي قمت بتحديده.</span><span class="sxs-lookup"><span data-stu-id="bc59c-127">The logic app will export a data package from Human Resources, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="bc59c-128">سوف يشبه تطبيق logic المكتمل الرسم التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="bc59c-128">The completed logic app will resemble the following illustration.</span></span>

![نظرة عامة على تطبيق logic](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a><span data-ttu-id="bc59c-130">الخطوة 1: إنشاء مشروع تصدير بيانات في Human Resources</span><span class="sxs-lookup"><span data-stu-id="bc59c-130">Step 1: Create a data export project in Human Resources</span></span>

<span data-ttu-id="bc59c-131">في Human Resources، قم بإنشاء مشروع تصدير بيانات الذي سوف يقوم بتصدير العمال.</span><span class="sxs-lookup"><span data-stu-id="bc59c-131">In Human Resources, create a data export project that exports workers.</span></span> <span data-ttu-id="bc59c-132">قم بتسمية المشروع **تصدير العمال** ، وتأكد أن خيار **إنشاء حزمة البيانات** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="bc59c-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="bc59c-133">أضف كيان واحد (**العامل**) إلى المشروع وحدد التنسيق المراد تصديره للمشروع.</span><span class="sxs-lookup"><span data-stu-id="bc59c-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="bc59c-134">(يتم استخدام Microsoft Excel في هذا البرنامج التعليمي.)</span><span class="sxs-lookup"><span data-stu-id="bc59c-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![تصدير مشروع بيانات العاملين](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="bc59c-136">تذكر اسم مشروع تصدير البيانات.</span><span class="sxs-lookup"><span data-stu-id="bc59c-136">Remember the name of the data export project.</span></span> <span data-ttu-id="bc59c-137">سوف تحتاج إليه عند إنشاء تطبيق logic في الخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="bc59c-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="bc59c-138">الخطوة 2: إنشاء تطبيق logic</span><span class="sxs-lookup"><span data-stu-id="bc59c-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="bc59c-139">تتضمن مجموعة التجارب إنشاء تطبيق logic.</span><span class="sxs-lookup"><span data-stu-id="bc59c-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="bc59c-140">في مدخل Azure ، قم بإنشاء تطبيق logic.</span><span class="sxs-lookup"><span data-stu-id="bc59c-140">In the Azure portal, create a logic app.</span></span>

    ![صفحة إنشاء تطبيق logic.](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="bc59c-142">في Logic Apps Designer ابدأ بتطبيق logic فارغ.</span><span class="sxs-lookup"><span data-stu-id="bc59c-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="bc59c-143">أضف [مشغل جدول متكرر](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) لتشغيل تطبيق logic كل 24 ساعة (أو وفقًا لجدول من اختيارك).</span><span class="sxs-lookup"><span data-stu-id="bc59c-143">Add a [Recurrence Schedule trigger](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![مربع حوار التكرار](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="bc59c-145">الاتصال بواجهة برمجية تطبيقات حزمة DMF REST [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) لجدولة تصدير حزمة بياناتك.</span><span class="sxs-lookup"><span data-stu-id="bc59c-145">Call the [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="bc59c-146">استخدم إجراء **استدعاء طلب HTTP** من HTTP مع موصل Azure AD.</span><span class="sxs-lookup"><span data-stu-id="bc59c-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="bc59c-147">**عنوان URL للمورد الأساسي** - عنوان URL لبيئة Human Resources الخاصة بك (لا تقم بتضمين معلومات المسار/مساحة الاسم.)</span><span class="sxs-lookup"><span data-stu-id="bc59c-147">**Base Resource URL:** The URL of your Human Resources environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="bc59c-148">**عنوان URL لـ Azure AD Resource:** `http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="bc59c-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="bc59c-149">لا توفر خدمة Human Resources موصل بعد التي تكشف جميع واجهات برمجيات التطبيقات التي تتألف منها واجهة بمرجية تطبيقات REST لحزمة DMF، مثل **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="bc59c-149">The Human Resources service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="bc59c-150">بدلًا من ذلك، يجب استدعاء واجهات برمجيات التطبيقات باستخدام طلبات HTTPS الأولية من خلال HTTP مع موصل Azure AD.</span><span class="sxs-lookup"><span data-stu-id="bc59c-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="bc59c-151">يستخدم هذا الموصل Azure Active Directory (Azure AD) للمصادقة والتخويل لـ Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bc59c-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Human Resources.</span></span>

        ![HTTP مع موصل Azure AD](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="bc59c-153">قم بتسجيل الدخول إلى بيئة Human Resources من خلال HTTP مع موصل Azure AD.</span><span class="sxs-lookup"><span data-stu-id="bc59c-153">Sign in to your Human Resources environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="bc59c-154">قم بإعداد طلب **POST** HTTP لاستدعاء واجهة برمجة التطبيقات REST لحزمة DMF **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="bc59c-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="bc59c-155">**الأسلوب:** POST</span><span class="sxs-lookup"><span data-stu-id="bc59c-155">**Method:** POST</span></span>
        - <span data-ttu-id="bc59c-156">**عنوان URL للطلب:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="bc59c-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="bc59c-157">**نص الطلب:**</span><span class="sxs-lookup"><span data-stu-id="bc59c-157">**Body of the request:**</span></span>

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![استدعاء إجراء طلب HTTP](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > <span data-ttu-id="bc59c-159">قد تحتاج إلى إعادة تسمية كل خطوة بحيث تكون أكثر نفعًا من الاسم الافتراضي، **استدعاء طلب HTTP**.</span><span class="sxs-lookup"><span data-stu-id="bc59c-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="bc59c-160">على سبيل المثال، يُمكن إعادة تسمية هذه الخطوة **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="bc59c-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="bc59c-161">[تهيئة](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) متغير لتخزين حالة تخزين طلب **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="bc59c-161">[Initialize a variable](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![تهيئة إجراء متغير](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="bc59c-163">انتظر حتى يتم **نجاح** تنفيذ حالة تصدير البيانات.</span><span class="sxs-lookup"><span data-stu-id="bc59c-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="bc59c-164">إضافة [حلقة حتى](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) تتكرر حتى تصبح قيمة متغير **ExecutionStatus** هي **تم بنجاح**.</span><span class="sxs-lookup"><span data-stu-id="bc59c-164">Add an [Until loop](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="bc59c-165">قم بإضافة إجراء **تأخير** ينتظر خمس ثوان قبل القيام بالاستقصاء لحالة التنفيذ الحالية للتصدير.</span><span class="sxs-lookup"><span data-stu-id="bc59c-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![حاوية حلقة حتى](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="bc59c-167">قم بتعيين عدد الحد إلى **15** للانتظار لمدة 75 ثانية بحد أقصى (15 تكرار \* 5 ثواني) حتى اكتمال التصدير.</span><span class="sxs-lookup"><span data-stu-id="bc59c-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="bc59c-168">إذا استغرقت عملية التصدير وقتًا إضافيًا، فقم بتعديل عدد الحد على النحو المناسب.</span><span class="sxs-lookup"><span data-stu-id="bc59c-168">If your export takes more time, adjust the limit count as appropriate.</span></span>        

    3. <span data-ttu-id="bc59c-169">أضف إجراء **استدعاء طلب HTTP** لاستدعاء واجهة برمجية التطبيق REST لحزمة DMF [GetExecutionSummaryStatue](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) ، وتعيين متغير **ExecutionStatue** إلى نتيجة استجابة **GetExecutionSummaryStatus** </span><span class="sxs-lookup"><span data-stu-id="bc59c-169">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="bc59c-170">لا يقوم هذا النموذج بالتحقق من الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="bc59c-170">This sample doesn't do error checking.</span></span> <span data-ttu-id="bc59c-171">يُمكن أن تُرجع واجهة برمجة تطبيق **GetExecutionSummaryStatus‎** الحالات الطرفية غير الناجحة (أي، الحالات الأخرى بخلاف **تم بنجاح**).</span><span class="sxs-lookup"><span data-stu-id="bc59c-171">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="bc59c-172">لمزيد من المعلومات، راجع [وثائق API](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span><span class="sxs-lookup"><span data-stu-id="bc59c-172">For more information, see the [API documentation](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

        - <span data-ttu-id="bc59c-173">**الأسلوب:** POST</span><span class="sxs-lookup"><span data-stu-id="bc59c-173">**Method:** POST</span></span>
        - <span data-ttu-id="bc59c-174">**عنوان URL للطلب:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="bc59c-174">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="bc59c-175">**نص الطلب:** body('Invoke\_an\_HTTP\_request')?['value']</span><span class="sxs-lookup"><span data-stu-id="bc59c-175">**Body of the request:** body('Invoke\_an\_HTTP\_request')?['value']</span></span>

            > [!NOTE]
            > <span data-ttu-id="bc59c-176">قد تحتاج إلى إدخال قيمة **نص الطلب** إما في طريقة عرض الكود أو في مُحرر الوظيفة في المصمم.</span><span class="sxs-lookup"><span data-stu-id="bc59c-176">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![استدعاء إجراء طلب HTTP 2](media/integration-logic-app-get-execution-status-step.png)

        ![تعيين الإجراء المتغير](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="bc59c-179">سوف تختلف القيمة للإجراء **تعيين المتغير** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) عن القيمة لقيمة نص **استدعاء طلب HTTP 2** حتى لو كان المصمم سوف يعرض القيم بالطريقة نفسها.</span><span class="sxs-lookup"><span data-stu-id="bc59c-179">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="bc59c-180">الحصول على عنوان URL للتنزيل للحزمة المُصدرة.</span><span class="sxs-lookup"><span data-stu-id="bc59c-180">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="bc59c-181">قم بإضافة إجراء **استدعاء طلب HTTP** لاستدعاء واجهة برمجة تطبيقات DMF REST [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl).</span><span class="sxs-lookup"><span data-stu-id="bc59c-181">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="bc59c-182">**الأسلوب:** POST</span><span class="sxs-lookup"><span data-stu-id="bc59c-182">**Method:** POST</span></span>
        - <span data-ttu-id="bc59c-183">**عنوان URL للطلب:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="bc59c-183">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="bc59c-184">**نص الطلب:** {"executionId": body('GetExportedPackageURL')?['value']}</span><span class="sxs-lookup"><span data-stu-id="bc59c-184">**Body of the request:** {"executionId": body('GetExportedPackageURL')?['value']}</span></span>

        ![إجراء GetExportedPackageURL ](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="bc59c-186">تنزيل الحزمة المُصدرة.</span><span class="sxs-lookup"><span data-stu-id="bc59c-186">Download the exported package.</span></span>

    - <span data-ttu-id="bc59c-187">ثم بإضافة طلب HTTP لـ **GET** ([إجراء موصل HTTP](https://docs.microsoft.com/azure/connectors/connectors-native-http) مضمن) لتنزيل الحزمة من عنوان URL الذي تم إرجاعه في الخطوة السابقة.</span><span class="sxs-lookup"><span data-stu-id="bc59c-187">Add an HTTP **GET** request (a built-in [HTTP connector action](https://docs.microsoft.com/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="bc59c-188">**الأسلوب:** GET</span><span class="sxs-lookup"><span data-stu-id="bc59c-188">**Method:** GET</span></span>
        - <span data-ttu-id="bc59c-189">**عنوان URL:** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="bc59c-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="bc59c-190">قد تحتاج إلى إدخال قيمة **عنوان URL** إما في طريقة عرض الكود أو في مُحرر الوظيفة في المصمم.</span><span class="sxs-lookup"><span data-stu-id="bc59c-190">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![إجراء HTTP GET](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="bc59c-192">لا يتطلب هذا الطلب أي مصادقة إضافية، لأن عنوان URL الذي تقوم واجهة برمجة التطبيقات **GetExportedPackageUrl‎** بإرجاعه يتضمن الرمز المميز لتوقيعات الوصول المشترك الذي يمنح الوصول لتنزيل الملف.</span><span class="sxs-lookup"><span data-stu-id="bc59c-192">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="bc59c-193">احفظ الحزمة التي تم تنزيلها باستخدام موصل [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness).</span><span class="sxs-lookup"><span data-stu-id="bc59c-193">Save the downloaded package by using the [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="bc59c-194">إضافة إجراء OneDrive For Business[إنشاء ملف](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file).</span><span class="sxs-lookup"><span data-stu-id="bc59c-194">Add a OneDrive for Business [Create File](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="bc59c-195">قم بالتوصيل إلى حساب OneDrive for Business الخاص بك، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="bc59c-195">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="bc59c-196">**مسار المجلد:** مجلد من اختيارك</span><span class="sxs-lookup"><span data-stu-id="bc59c-196">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="bc59c-197">**اسم الملف:** worker\_package.zip</span><span class="sxs-lookup"><span data-stu-id="bc59c-197">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="bc59c-198">**محتوى الملف:** النص من الخطوة السابقة (محتوى ديناميكي)</span><span class="sxs-lookup"><span data-stu-id="bc59c-198">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![إنشاء إجراء ملف](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="bc59c-200">الخطوة 3: اختبار تطبيق logic</span><span class="sxs-lookup"><span data-stu-id="bc59c-200">Step 3: Test the logic app</span></span>

<span data-ttu-id="bc59c-201">لاختبار تطبيق logic الخاص بك، حدد زر **تشغيل** في المصمم.</span><span class="sxs-lookup"><span data-stu-id="bc59c-201">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="bc59c-202">سوف ترى أن خطوات تطبيق logic بدأت في التشغيل.</span><span class="sxs-lookup"><span data-stu-id="bc59c-202">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="bc59c-203">بعد 30 إلى 40 ثانية، يجب أن ينهي تطبيق logic التشغيل، وينبغي أن يتضمن مجلد OneDrive for Business ملف حزمة جديد يحتوي على العاملين المُصدرين.</span><span class="sxs-lookup"><span data-stu-id="bc59c-203">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="bc59c-204">في حالة الإبلاغ عن فشل أي خطوة، حدد الخطوة الفاشلة في المصمم، وتحقق من حقول **الإدخالات** و **الاخراجات** الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="bc59c-204">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="bc59c-205">قم بالتصحيح وعدّل الخطوة حسب الحاجة لتصحيح الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="bc59c-205">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="bc59c-206">يُبين الرسم التوضيحي التالي كيف يبدو Logic Apps Designer عندما يتم تشغيل كافة خطوات تطبيق logic بنجاح.</span><span class="sxs-lookup"><span data-stu-id="bc59c-206">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![تشغيل تطبيق logic بنجاح](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="bc59c-208">ملخص</span><span class="sxs-lookup"><span data-stu-id="bc59c-208">Summary</span></span>

<span data-ttu-id="bc59c-209">في هذا البرنامج التعليمي، تعلمنا كيفية استخدام تطبيق logic لتصدير البيانات من Human Resources وحفظ البيانات المُصدرة إلى مُجلد OneDrive for Business.</span><span class="sxs-lookup"><span data-stu-id="bc59c-209">In this tutorial, you learned how to use a logic app to export data from Human Resources and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="bc59c-210">يمكنك تعديل خطوات هذا البرنامج التعليمي حسب الحاجة ليناسب احتياجات الأعمال الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="bc59c-210">You can modify the steps of this tutorial as required to suit your business needs.</span></span>


