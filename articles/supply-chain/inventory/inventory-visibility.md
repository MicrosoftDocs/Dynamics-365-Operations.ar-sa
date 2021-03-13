---
title: الوظيفة الاضافيه لرؤية المخزون
description: يوضح هذا الموضوع كيفيه تثبيت الوظيفة الاضافيه لرؤية المخزون وتكوينها لـ Dynamics 365 Supply Chain Management.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114660"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="0a8fc-103">الوظيفة الاضافيه لرؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="0a8fc-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="0a8fc-104">تعد الوظيفة الاضافيه لرؤية المخزون بمثابه خدمة صغيرة مستقله وقابله للتغيير بشكل كبير والتي تمكن تتبع المخزون الفعلي في الوقت الحقيقي ، مما يوفر عرضا شاملا لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="0a8fc-105">يتم تصدير كافة المعلومات المرتبطة بالمخزون الفعلي إلى الخدمة بالقرب من الوقت الحقيقي خلال تكامل SQL في المستوي المنخفض.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="0a8fc-106">تقوم الانظمه الخارجية بالوصول إلى الخدمة من خلال واجهات RESTful API للاستعلام عن المعلومات الفعلية حول المجموعات المحددة من الابعاد ، ومن ثم استرداد قائمه بالمناصب الفعلية المتاحة.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="0a8fc-107">رؤية المخزون عبارة عن خدمة صغيرة مضمنة في Microsoft Dataverse، مما يعني انه يمكنك توسيعها بواسطة إنشاء Power Apps وتطبيق Power BI لتوفير وظيفة مخصصه لتلبيه متطلبات الاعمال الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="0a8fc-108">من الممكن أيضا ترقيه الفهرس للقيام باستعلامات المخزون.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="0a8fc-109">توفر امكانيه رؤية المخزون خيارات التكوين التي تتيح له التكامل مع أنظمه متعددة الجهات الخارجية.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="0a8fc-110">وهو يدعم بعد المخزون القياسي والقابلية للتوسعة المخصصة والكميات التي تم حسابها والقياسية القابلة للتكوين.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="0a8fc-111">يصف هذا الموضوع كيفيه تثبيت وتكوين الوظيفة الاضافيه لرؤية المخزون لـ Dynamics 365 Supply Chain Management، وكيفيه استخدام واجهه برمجه التطبيقات (API) الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="0a8fc-112">تثبيت الوظيفة الاضافيه لرؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="0a8fc-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="0a8fc-113">يجب تثبيت الوظيفة الاضافيه لرؤية المخزون باستخدام Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="0a8fc-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="0a8fc-114">LCS عبارة عن مدخل تعاون يوفر بيئة ومجموعه من الخدمات المحدثة بشكل منتظم والتي تساعدك علي أداره دوره حياه التطبيقات الخاصة بتطبيقات Dynamics 365 Finance and Operations الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="0a8fc-115">للحصول على مزيد من المعلومات، راجع [موارد Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="0a8fc-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0a8fc-116">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="0a8fc-116">Prerequisites</span></span>

<span data-ttu-id="0a8fc-117">قبل أن تتمكن من تثبيت الوظيفة الإضافية لرؤية المخزون، يجب عليك القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="0a8fc-118">احصل علي مشروع تنفيذ LCS مع نشر بيئة واحده علي الأقل.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="0a8fc-119">أنشئ مفاتيح بيتا لتقديمك في LCS.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="0a8fc-120">قم بتمكين مفاتيح بيتا لعرضك من أجل المستخدم الخاص بك في LCS.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="0a8fc-121">اتصل بفريق المنتج الخاص برؤية المخزون لـ Microsoft وقم بتوفير معرف البيئة الذي ترغب في نشر الوظيفة الاضافيه لرؤية المخزون فيه.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="0a8fc-122">إذا كانت لديك إيه اسئله حول هذه المتطلبات الاساسيه ، الرجاء الاتصال بفريق رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="0a8fc-123">تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="0a8fc-123">Install the add-in</span></span>

<span data-ttu-id="0a8fc-124">لتثبيت الوظيفة الإضافية لرؤية المخزون، يجب عليك القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="0a8fc-125">سجل الدخول إلى بوابة [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="0a8fc-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="0a8fc-126">في الصفحة الرئيسية ، حدد المشروع حيث يتم نشر البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="0a8fc-127">في الصفحة المشروع ، حدد البيئة التي ترغب في تثبيت الوظيفة الاضافيه بها.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="0a8fc-128">في الصفحة البيئة ، قم بالتمرير لأسفل حتى تشاهد قسم **الوظائف الاضافيه الخاصة بالبيئة**.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="0a8fc-129">إذا لم يكن المقطع مرئيا ، فتاكد من انه قد تمت معالجه المفتاح بيتا بشكل كامل.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="0a8fc-130">في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="0a8fc-131">![صفحة البيئة في LCS](media/inventory-visibility-environment.png "صفحة البيئة في LCS")</span><span class="sxs-lookup"><span data-stu-id="0a8fc-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="0a8fc-132">حدد الرابط **تثبيت وظيفة إضافية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="0a8fc-133">يتم فتح قائمه بالوظائف الاضافيه المتاحة.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="0a8fc-134">حدد **خدمه المخزون** من القائمة.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="0a8fc-135">(ملاحظه، قد يتم ادراج هذا الآن علي انه **الوظيفة الاضافيه لرؤية المخزون لـ Dynamics 365 Supply Chain Management** .)</span><span class="sxs-lookup"><span data-stu-id="0a8fc-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="0a8fc-136">ادخل قيما للحقول التالية الخاصة ببيئتك:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="0a8fc-137">**مُعرِّف تطبيق AAD**</span><span class="sxs-lookup"><span data-stu-id="0a8fc-137">**AAD application ID**</span></span>
    - <span data-ttu-id="0a8fc-138">**معرف مستأجر AAD**</span><span class="sxs-lookup"><span data-stu-id="0a8fc-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="0a8fc-139">![أضافه في صفحه الاعداد](media/inventory-visibility-setup.png "صفحه اعداد الوظيفة الإضافية")</span><span class="sxs-lookup"><span data-stu-id="0a8fc-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="0a8fc-140">الموافقة علي البنود والشروط عن طريق تحديد خانه الاختيار **البنود والشروط**.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="0a8fc-141">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-141">Select **Install**.</span></span> <span data-ttu-id="0a8fc-142">ستظهر حاله الوظيفة الاضافيه باعتبارها **قيد التثبيت**.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="0a8fc-143">عند الانتهاء ، قم بتحديث الصفحة لرؤية تغيير الحالة علي **مثبت**.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="0a8fc-144">الحصول علي رمز خدمه أمان</span><span class="sxs-lookup"><span data-stu-id="0a8fc-144">Get a security service token</span></span>

<span data-ttu-id="0a8fc-145">احصل علي رمز خدمه أمان بالقيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-145">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="0a8fc-146">سجل دخولك إلى مدخل Azure واستخدمه للعثور علي `clientId`و`clientSecret` لتطبيق Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-146">Sign in to Azure Portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="0a8fc-147">إحضار Azure Active Directory رمز مميز (`aadToken`) عن طريق إرسال طلب HTTP بالخصائص التالية:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-147">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="0a8fc-148">**عنوان URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="0a8fc-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="0a8fc-149">**الطريقة** - `GET`</span><span class="sxs-lookup"><span data-stu-id="0a8fc-149">**Method** - `GET`</span></span>
    - <span data-ttu-id="0a8fc-150">**محتوي النص الأساسي (بيانات النموذج)**:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-150">**Body content (form data)**:</span></span>

        | <span data-ttu-id="0a8fc-151">المفتاح</span><span class="sxs-lookup"><span data-stu-id="0a8fc-151">key</span></span> | <span data-ttu-id="0a8fc-152">القيمة</span><span class="sxs-lookup"><span data-stu-id="0a8fc-152">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="0a8fc-153">client_id</span><span class="sxs-lookup"><span data-stu-id="0a8fc-153">client_id</span></span> | <span data-ttu-id="0a8fc-154">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="0a8fc-154">${aadAppId}</span></span> |
        | <span data-ttu-id="0a8fc-155">client_secret</span><span class="sxs-lookup"><span data-stu-id="0a8fc-155">client_secret</span></span> | <span data-ttu-id="0a8fc-156">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="0a8fc-156">${aadAppSecret}</span></span> |
        | <span data-ttu-id="0a8fc-157">grant_type</span><span class="sxs-lookup"><span data-stu-id="0a8fc-157">grant_type</span></span> | <span data-ttu-id="0a8fc-158">client_credentials</span><span class="sxs-lookup"><span data-stu-id="0a8fc-158">client_credentials</span></span> |
        | <span data-ttu-id="0a8fc-159">مورد</span><span class="sxs-lookup"><span data-stu-id="0a8fc-159">resource</span></span> | <span data-ttu-id="0a8fc-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="0a8fc-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="0a8fc-161">يجب ان تتلقي `aadToken` استجابه فيها، والتي تشبه المثال التالي.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-161">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="0a8fc-162">المستقبل طلب JSON مشابها لما يلي:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-162">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="0a8fc-163">المكان:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-163">Where:</span></span>
    - <span data-ttu-id="0a8fc-164">`client_assertion`يجب ان تكون القيمة هي `aadToken` التي استلمتها في الخطوة السابقة.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-164">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="0a8fc-165">`context`يجب ان تكون القيمة معرف البيئة حيث تريد توزيع الوظيفة الاضافيه.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-165">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="0a8fc-166">قم بتعيين كافة القيم الأخرى كما هو موضح في المثال.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-166">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="0a8fc-167">قم بإرسال طلب HTTP بالخصائص التالية:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-167">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="0a8fc-168">**عنوان URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="0a8fc-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="0a8fc-169">**الطريقة** - `POST`</span><span class="sxs-lookup"><span data-stu-id="0a8fc-169">**Method** - `POST`</span></span>
    - <span data-ttu-id="0a8fc-170">**راس HTTP** - تضمين إصدار API (`Api-Version` المفتاح هو والقيمة هو `1.0`)</span><span class="sxs-lookup"><span data-stu-id="0a8fc-170">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="0a8fc-171">**محتوي أساسي** - تضمين طلب JSON الذي قمت بإنشاءه في الخطوة السابقة.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-171">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="0a8fc-172">ستحصل علي `access_token` في الاستجابة.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-172">You will get an `access_token` in response.</span></span> <span data-ttu-id="0a8fc-173">وهذا ما تحتاجه كرمز مميز في الحامل لاستدعاء امكانيه رؤية API للمخزون.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-173">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="0a8fc-174">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-174">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="0a8fc-175">إلغاء تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="0a8fc-175">Uninstall the add-in</span></span>

<span data-ttu-id="0a8fc-176">للغاء تثبيت الوظيفة الاضافيه ، حدد **إلغاء التثبيت**.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-176">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="0a8fc-177">تحديث LCS ستتم أزاله الوظيفة الاضافيه لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-177">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="0a8fc-178">تقوم عمليه أزاله التثبيت بازاله تسجيل الوظيفة الاضافيه وبدء مهمة أيضا لتنظيف كافة بيانات الاعمال المخزنة في الخدمة.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-178">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="0a8fc-179">واجهة API العامة للوظيفة الاضافيه لرؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="0a8fc-179">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="0a8fc-180">تقدم واجهه برمجه التطبيقات العامة لـ REST الخاصة بالوظيفة الاضافيه لرؤية المخزون العديد من نقاط التكامل الخاصة.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-180">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="0a8fc-181">ويدعم ثلاثه أنواع من التفاعلات الرئيسية:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-181">It supports three main interaction types:</span></span>

- <span data-ttu-id="0a8fc-182">يتم الآن ترحيل التغييرات الفعلية إلى الوظيفة الاضافيه من نظام خارجي.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-182">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="0a8fc-183">تستعلم عن الكميات الفعلية الحالية من نظام خارجي.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-183">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="0a8fc-184">مزامنة تلقائية مع Supply Chain Management الفعلية.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-184">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="0a8fc-185">لا تعد المزامنة التلقائية جزءا من API العامة ، لكن يتم التعامل معها بدلا من ذلك في الخلفية للبيئات التي قامت بتمكين الوظيفة الاضافيه لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-185">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="0a8fc-186">مصادقة</span><span class="sxs-lookup"><span data-stu-id="0a8fc-186">Authentication</span></span>

<span data-ttu-id="0a8fc-187">يتم استخدام الرمز المميز لامان النظام لاستدعاء الوظيفة الاضافيه لرؤية المخزون ، لذا يجب إنشاء رمز مميز لـ Azure Active Directory باستخدام تطبيق Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-187">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="0a8fc-188">لمزيد من المعلومات حول كيفيه الحصول علي الرمز المميز للامان ، راجع [تثبيت الوظيفة الاضافيه لرؤية المخزون](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="0a8fc-188">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="0a8fc-189">تكوين واجهه برمجه تطبيقات امكانيه رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="0a8fc-189">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="0a8fc-190">قبل استخدام الخدمة ، يجب إكمال التكوينات الموضحة في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-190">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="0a8fc-191">قد يختلف التكوين استنادا إلى تفاصيل البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-191">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="0a8fc-192">وهو يتضمن بشكل أساسي أربعه أجزاء:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-192">It primarily includes four parts:</span></span>

- [<span data-ttu-id="0a8fc-193">تقسيم</span><span class="sxs-lookup"><span data-stu-id="0a8fc-193">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="0a8fc-194">تكوينات الأبعاد</span><span class="sxs-lookup"><span data-stu-id="0a8fc-194">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="0a8fc-195">فهرسة</span><span class="sxs-lookup"><span data-stu-id="0a8fc-195">Indexing</span></span>](#indexing)
- [<span data-ttu-id="0a8fc-196">قياس مخصص</span><span class="sxs-lookup"><span data-stu-id="0a8fc-196">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="0a8fc-197">تقسيم</span><span class="sxs-lookup"><span data-stu-id="0a8fc-197">Partitioning</span></span>

<span data-ttu-id="0a8fc-198">يمكن للتقسيم ان يؤثر بشكل كبير علي أداء واجهة API الخاصة برؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-198">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="0a8fc-199">انها لفكره جيده ان تقوم بتعريف نظام يسمح بالتجميعات الصغيرة للبيانات مع استمرار السماح باستعلامات البيانات ذات المعني.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-199">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="0a8fc-200">سيكون `organizationId` (`dataAreaId` في Supply Chain Management) دائما جزءا من التقسيم ، ويتم تعيين رؤية المخزون بشكل افتراضي علي قسم حسب الابعاد *كموقع إلكتروني + موقع جغرافي*.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-200">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="0a8fc-201">وهذا يعني انه يجب دوما الاستعلام عن الخدمة باستخدام هذه الابعاد المحددة في عوامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-201">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="0a8fc-202">*الموقع الإلكتروني* و *الموقع الجغرافي* هما اثنان من الابعاد الافتراضية في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-202">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="0a8fc-203">في Supply Chain Management، تسمي هذه الابعاد *بالموقع الإلكتروني* (`InventSiteId`) *والمستودع* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="0a8fc-203">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="0a8fc-204">تكوينات الأبعاد</span><span class="sxs-lookup"><span data-stu-id="0a8fc-204">Dimension configurations</span></span>

<span data-ttu-id="0a8fc-205">ستوفر امكانيه رؤية المخزون قائمه بالابعاد الافتراضية العامة لتمكين تكامل النظام المصدر المتعدد.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-205">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="0a8fc-206">يسرد الجدول التالي ابعاد المخزون التي ستكون أسماء الابعاد الافتراضية في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-206">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="0a8fc-207">نوع البعد</span><span class="sxs-lookup"><span data-stu-id="0a8fc-207">Dimension type</span></span> | <span data-ttu-id="0a8fc-208">اسم البُعد</span><span class="sxs-lookup"><span data-stu-id="0a8fc-208">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="0a8fc-209">منتج</span><span class="sxs-lookup"><span data-stu-id="0a8fc-209">Product</span></span> | `ColorId` |
| <span data-ttu-id="0a8fc-210">منتج</span><span class="sxs-lookup"><span data-stu-id="0a8fc-210">Product</span></span> | `SizeId` |
| <span data-ttu-id="0a8fc-211">منتج</span><span class="sxs-lookup"><span data-stu-id="0a8fc-211">Product</span></span> | `StyleId` |
| <span data-ttu-id="0a8fc-212">منتج</span><span class="sxs-lookup"><span data-stu-id="0a8fc-212">Product</span></span> | `ConfigId` |
| <span data-ttu-id="0a8fc-213">التعقب</span><span class="sxs-lookup"><span data-stu-id="0a8fc-213">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="0a8fc-214">التعقب</span><span class="sxs-lookup"><span data-stu-id="0a8fc-214">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="0a8fc-215"> الموق</span><span class="sxs-lookup"><span data-stu-id="0a8fc-215">Location</span></span> | `LocationId` |
| <span data-ttu-id="0a8fc-216"> الموق</span><span class="sxs-lookup"><span data-stu-id="0a8fc-216">Location</span></span> | `SiteId` |
| <span data-ttu-id="0a8fc-217">حالة المخزون</span><span class="sxs-lookup"><span data-stu-id="0a8fc-217">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="0a8fc-218">خاص بالمستودع</span><span class="sxs-lookup"><span data-stu-id="0a8fc-218">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="0a8fc-219">خاص بالمستودع</span><span class="sxs-lookup"><span data-stu-id="0a8fc-219">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="0a8fc-220">خاص بالمستودع</span><span class="sxs-lookup"><span data-stu-id="0a8fc-220">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="0a8fc-221">يكون نوع البعد المدرج في الجدول السابق كمرجع فقط.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-221">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="0a8fc-222">لا يلزم تحديد نوع البعد في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-222">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="0a8fc-223">في حاله وجود بعد مخصص والحاجة إلى التدفق للقيمة الافتراضية عند استهلاك رؤية المخزون ، يمكنك تكوين **اسم البعد المخصص** في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-223">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="0a8fc-224">وصول الانظمه الخارجية إلى رؤية المخزون من خلال واجات برمجه التطبيقات RESTful التي تتيح معلومات الكمية الفعلية حول مجموعات الابعاد المحددة التي سيتم الاستعلام عنها.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-224">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="0a8fc-225">بالنسبة للتكامل ، يمكنك رؤية المخزون من تكوين *مصدر بيانات القناة الخارجية* وبعد المصدر علي *الابعاد المستهدفة* في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-225">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="0a8fc-226">يجب ان تكون الابعاد المستهدفة واحده مما يلي:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-226">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="0a8fc-227">الابعاد الافتراضية في رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="0a8fc-227">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="0a8fc-228">الأبعاد المخصصة</span><span class="sxs-lookup"><span data-stu-id="0a8fc-228">Custom dimensions</span></span>

<span data-ttu-id="0a8fc-229">والغرض من تكوين الابعاد هو توحيد التكامل المتعدد الانظمه للاستعلام علي الابعاد وحدث الترحيل مع الابعاد.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-229">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="0a8fc-230">فهرسة</span><span class="sxs-lookup"><span data-stu-id="0a8fc-230">Indexing</span></span>

<span data-ttu-id="0a8fc-231">في معظم الأوقات ، لن يكون الاستعلام الفعلي الخاص بالمخزون علي مستوي "الإجمالي" الأعلى فقط ، ولكن قد ترغب في رؤية النتائج المجمعة استنادا إلى ابعاد المخزون.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-231">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="0a8fc-232">توفر امكانيه رؤية المخزون المرونة عن طريق السماح لك باعداد الفهارس ، التي تعتمد علي البعد أو مجموعه الابعاد.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-232">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="0a8fc-233">حاليا ، يمكنك فقط تكوين الفهارس بخمسه كحد اقصي.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-233">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="0a8fc-234">يجب مراعاه البعد أو مجموعه الابعاد التي ستستخدمها قبل التنفيذ للتاكد من انها ستفي باحتياجات أعمالك.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-234">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="0a8fc-235">علي سبيل المثال ، إذا كنت ترغب في الاستعلام عن المنتجات كالتالي:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-235">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="0a8fc-236">الاستعلام عن المنتج المجمع الفعلي بواسطة ابعاد *اللون* و *الحجم*.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-236">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="0a8fc-237">في بعض الحالات ، تريد فقط الاستعلام عن المنتج إجمالا.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-237">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="0a8fc-238">سيكون لديك فهرسين محددين كالتالي:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-238">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="0a8fc-239">سيتم تجميع القوس الفارغ استنادا إلى "معرف المنتج" داخل القسم.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-239">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="0a8fc-240">تحدد الفهرسة كيفيه تجميع النتائج استنادا إلى اعداد الاستعلام `groupBy`.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-240">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="0a8fc-241">في هذه الحالة إذا لم تقم بتحديد أي قيم `groupBy`، سيتم الحصول علي الإجماليات بواسطة `productid`.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-241">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="0a8fc-242">والا إذا قمت بتحديد `groupBy` كـ `groupBy=ColorId&groupBy=SizeId` ، ستحصل علي بنود متعددة يتم إرجاعها ، استنادا إلى مجموعتي اللون والحجم المختلفتين في النظام.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-242">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="0a8fc-243">يمكنك وضع معايير الاستعلام في النص الأساسي للطلب.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-243">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="0a8fc-244">فيما يلي نموذج استعلام حول المنتج بمجموعه اللون والحجم.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-244">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="0a8fc-245">قياس مخصص</span><span class="sxs-lookup"><span data-stu-id="0a8fc-245">Custom measurement</span></span>

<span data-ttu-id="0a8fc-246">وترتبط كميات القياس الافتراضية بـ Supply Chain Management، ومع ذلك قد ترغب في الحصول علي كميه تتكون من مجموعه من القياسات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-246">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="0a8fc-247">وللقيام بذلك ، يمكن ان يكون لديك تكوين كميات مخصصه ، والتي ستتم اضافتها إلى إخراج الاستعلامات الفعلية.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-247">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="0a8fc-248">وتتيح الوظيفة ببساطه تحديد مجموعه من القياسات التي ستتم اضافتها ، و/أو مجموعه من المقاييس التي سيتم طرحها ، من أجل القياس المخصص.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-248">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="0a8fc-249">علي سبيل المثال ، باستخدام شرط الاستعلام التالي ، ستقوم بتكوين كميه القياس المخصصة باعتبارها `MyCustomAvailableforReservation` ليتم استهلاكها من قبل نظام الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-249">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="0a8fc-250">نظام الاستهلاك</span><span class="sxs-lookup"><span data-stu-id="0a8fc-250">Consumption system</span></span> | <span data-ttu-id="0a8fc-251">القياسات المحتسبة</span><span class="sxs-lookup"><span data-stu-id="0a8fc-251">Calculated measurers</span></span> | <span data-ttu-id="0a8fc-252">مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="0a8fc-252">Data source</span></span> | <span data-ttu-id="0a8fc-253">أداه التعديل</span><span class="sxs-lookup"><span data-stu-id="0a8fc-253">Modifier</span></span> | <span data-ttu-id="0a8fc-254">نوع حساب أداة التعديل</span><span class="sxs-lookup"><span data-stu-id="0a8fc-254">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="0a8fc-255">الجمع</span><span class="sxs-lookup"><span data-stu-id="0a8fc-255">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="0a8fc-256">الجمع</span><span class="sxs-lookup"><span data-stu-id="0a8fc-256">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="0a8fc-257">الطرح</span><span class="sxs-lookup"><span data-stu-id="0a8fc-257">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="0a8fc-258">الجمع</span><span class="sxs-lookup"><span data-stu-id="0a8fc-258">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="0a8fc-259">الطرح</span><span class="sxs-lookup"><span data-stu-id="0a8fc-259">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="0a8fc-260">الجمع</span><span class="sxs-lookup"><span data-stu-id="0a8fc-260">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="0a8fc-261">الجمع</span><span class="sxs-lookup"><span data-stu-id="0a8fc-261">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="0a8fc-262">الطرح</span><span class="sxs-lookup"><span data-stu-id="0a8fc-262">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="0a8fc-263">الطرح</span><span class="sxs-lookup"><span data-stu-id="0a8fc-263">Subtraction</span></span> |

<span data-ttu-id="0a8fc-264">ومع ذلك ، سيقوم الاستعلام الموجود علي كميه القياس المخصصة بإرجاع المخرجات التالية.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-264">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="0a8fc-265">يعتمد إخراج `MyCustomAvailableforReservation`علي اعداد الحساب في القياسات المخصصة كما يلي:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-265">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="0a8fc-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="0a8fc-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="0a8fc-267">ترحيل التغييرات الفعلية</span><span class="sxs-lookup"><span data-stu-id="0a8fc-267">Posting on-hand changes</span></span>

<span data-ttu-id="0a8fc-268">ويعتمد عنوان URL الذي يتم ترحيل الحدث عليه علي المنطقة الجغرافية بالبالضبط.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-268">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="0a8fc-269">سياخذ النموذج ما يلي:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-269">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="0a8fc-270">عند المصادقة ، يمكن استخدام محدد موقع المعلومات (URL) هذا مع أسلوب `POST` HTTP لإرسال احداث التغيير الفعلي إلى الخدمة.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-270">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="0a8fc-271">يتم استخدام الراس الخاص للاتصال مع خدمات Dynamics 365 من خلال طلبات HTTP ، والذي يشير إلى معرف البيئة لمثيل Supply Chain Management الذي ترتبط به البيانات.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-271">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="0a8fc-272">على سبيل المثال:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-272">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="0a8fc-273">ترحيل التغييرات الفعلية مثال الاستعلام 1</span><span class="sxs-lookup"><span data-stu-id="0a8fc-273">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="0a8fc-274">يوضح هذا المثال السيناريو الذي ستقوم فيه باعداد تكوين البعد في Power Apps.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-274">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="0a8fc-275">استخدم الاستعلام التالي لتكوين تعيين البعد في Power Apps:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-275">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="0a8fc-276">يمكنك الآن تحديد `dimensionDataSource` واستخدام الابعاد المخصصة في الاستعلامات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-276">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="0a8fc-277">سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-277">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="0a8fc-278">ترحيل التغييرات الفعلية مثال الاستعلام 2</span><span class="sxs-lookup"><span data-stu-id="0a8fc-278">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="0a8fc-279">يوضح هذا المثال السيناريو الذي لا يتم فيه اعداد تعيينات لتكوين البعد في Power Apps، التالي يجب ان تستخدم الترحيل أيضا الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-279">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="0a8fc-280">يجب ان تكون كافة الابعاد بابعاد أساسيه عندما يكون الحقل `dimensionDataSource` خاليا أو فارغا أو مسافة بيضاء.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-280">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="0a8fc-281">خصائص حقل مستند JSON</span><span class="sxs-lookup"><span data-stu-id="0a8fc-281">JSON document field properties</span></span>

<span data-ttu-id="0a8fc-282">تتضمن الحقول الموجودة في أمثله استعلام JSON المتوفرة في السابق الخصائص المسرودة في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-282">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="0a8fc-283">معرف الحقل</span><span class="sxs-lookup"><span data-stu-id="0a8fc-283">Field ID</span></span> | <span data-ttu-id="0a8fc-284">الوصف</span><span class="sxs-lookup"><span data-stu-id="0a8fc-284">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="0a8fc-285">معرف فريد لحدث التغيير المحدد.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-285">A unique ID for the specific change event.</span></span> <span data-ttu-id="0a8fc-286">يتم استخدام هذا المعرف للتاكد من فشل الاتصال بالخدمة اثناء الترحيل ، ولن يؤدي أعاده إرسال الحدث إلى نفس الحدث الذي يتم حسابه مرتين في النظام.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-286">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="0a8fc-287">معرف المؤسسة المرتبط بالحدث.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-287">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="0a8fc-288">وهذا ما يعين لمؤسسات Supply Chain Management أو معرفات مناطق البيانات.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-288">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="0a8fc-289">معرف أمر الإنتاج المحدد.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-289">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="0a8fc-290">الكمية التي يجب تغيير الكمية الحالية وفقا لها.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-290">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="0a8fc-291">علي سبيل المثال ، تمت أضافه 10 قطع من خبز البيغلز جديده إلى الرف، ستكون هذه القيمة 10.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-291">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="0a8fc-292">إذا تمت أزاله 3 قطع من خبز البيغلز من الرف أو بيعه ، ستكون هذه القيمة -3.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-292">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="0a8fc-293">مصدر البيانات الخاص بالابعاد المستخدمة في حدث تغيير الترحيل والاستعلام.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-293">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="0a8fc-294">إذا قمت بتحديد مصدر البيانات ، يمكنك استخدام الابعاد المخصصة من مصدر البيانات المحدد.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-294">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="0a8fc-295">باستخدام تكوين البعد ، يمكن ان يقوم ظهور المخزون بتعيين الابعاد المخصصة إلى الابعاد الافتراضية العامة.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-295">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="0a8fc-296">في حاله عدم تحديد `dimensionDataSource`، يمكنك استخدام الابعاد الافتراضية العامة فقط في الاستعلامات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-296">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="0a8fc-297">كيس مجموعه حيوية من أزواج مفتاح/قيمه.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-297">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="0a8fc-298">سيتم تعيينها لبعض الابعاد في Supply Chain Management، ولكن يمكنك أيضا أضافه ابعاد مخصصه (مثل *المصدر*) والتي قد تشير إلى ما إذا كان الحدث واردا من Supply Chain Management أو من النظام الخارجي.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-298">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="0a8fc-299">الاستعلام عن الكمية الحالية</span><span class="sxs-lookup"><span data-stu-id="0a8fc-299">Querying current on-hand</span></span>

<span data-ttu-id="0a8fc-300">سيكون للنقطة النهائية للاستعلام عن الكمية الحالية عنوان URL مشابه:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-300">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="0a8fc-301">سيتم الاستعلام عنها باستخدام أسلوب `POST` HTTP.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-301">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="0a8fc-302">مثال علي الاستعلام الفعلي حاليا 1</span><span class="sxs-lookup"><span data-stu-id="0a8fc-302">Current on-hand query example 1</span></span>

<span data-ttu-id="0a8fc-303">يوضح هذا المثال السيناريو الذي ستقوم فيه باعداد تكوين البعد في Power Apps.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-303">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="0a8fc-304">استخدم الاستعلام التالي لتكوين تعيين البعد في Power Apps:</span><span class="sxs-lookup"><span data-stu-id="0a8fc-304">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="0a8fc-305">يمكنك الآن تحديد `dimensionDataSource` واستخدام الابعاد المخصصة في الاستعلامات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-305">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="0a8fc-306">سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-306">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="0a8fc-307">يمكنك تحديد `DimensionDataSource` في `filters` وتحديد ابعاد مخصصه في كل من `filters` و`groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-307">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="0a8fc-308">سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-308">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="0a8fc-309">مثال علي الاستعلام الفعلي حاليا 2</span><span class="sxs-lookup"><span data-stu-id="0a8fc-309">Current on-hand query example 2</span></span>

<span data-ttu-id="0a8fc-310">يوضح هذا المثال السيناريو الذي لا يتم فيه اعداد تعيينات لتكوين البعد في Power Apps، التالي يجب ان تستخدم الترحيل أيضا الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-310">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="0a8fc-311">يجب ان تكون كافة الابعاد بابعاد أساسيه عندما يكون الحقل `dimensionDataSource`، ضمن `filters` خاليا أو فارغا أو مسافة بيضاء.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-311">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="0a8fc-312">مثال نتيجة الإرجاع</span><span class="sxs-lookup"><span data-stu-id="0a8fc-312">Example return result</span></span>

<span data-ttu-id="0a8fc-313">قد تؤدي الاستعلامات المعروضة في الامثله السابقة إلى إرجاع نتيجة مثل هذه.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-313">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="0a8fc-314">لاحظ انه يتم بناء حقول الكميات كقاموس للمقاييس والقيم المقترنة بها.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-314">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
