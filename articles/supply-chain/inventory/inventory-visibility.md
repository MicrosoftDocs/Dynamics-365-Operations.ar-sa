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
ms.openlocfilehash: 4e588be2ac5aae395ca66e3c9a743a67d71db7c0
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574212"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="e2d6f-103">الوظيفة الاضافيه لرؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="e2d6f-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="e2d6f-104">تعد الوظيفة الاضافيه لرؤية المخزون بمثابه خدمة صغيرة مستقله وقابله للتغيير بشكل كبير والتي تمكن تتبع المخزون الفعلي في الوقت الحقيقي ، مما يوفر عرضا شاملا لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="e2d6f-105">يتم تصدير كافة المعلومات المرتبطة بالمخزون الفعلي إلى الخدمة بالقرب من الوقت الحقيقي خلال تكامل SQL في المستوي المنخفض.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="e2d6f-106">تقوم الانظمه الخارجية بالوصول إلى الخدمة من خلال واجهات RESTful API للاستعلام عن المعلومات الفعلية حول المجموعات المحددة من الابعاد ، ومن ثم استرداد قائمه بالمناصب الفعلية المتاحة.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="e2d6f-107">رؤية المخزون عبارة عن خدمة صغيرة مضمنة في Microsoft Dataverse، مما يعني انه يمكنك توسيعها بواسطة إنشاء Power Apps وتطبيق Power BI لتوفير وظيفة مخصصه لتلبيه متطلبات الاعمال الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="e2d6f-108">من الممكن أيضا ترقيه الفهرس للقيام باستعلامات المخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="e2d6f-109">توفر امكانيه رؤية المخزون خيارات التكوين التي تتيح له التكامل مع أنظمه متعددة الجهات الخارجية.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="e2d6f-110">وهو يدعم بعد المخزون القياسي والقابلية للتوسعة المخصصة والكميات التي تم حسابها والقياسية القابلة للتكوين.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="e2d6f-111">يصف هذا الموضوع كيفيه تثبيت وتكوين الوظيفة الاضافيه لرؤية المخزون لـ Dynamics 365 Supply Chain Management، وكيفيه استخدام واجهه برمجه التطبيقات (API) الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="e2d6f-112">تثبيت الوظيفة الاضافيه لرؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="e2d6f-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="e2d6f-113">يجب تثبيت الوظيفة الاضافيه لرؤية المخزون باستخدام Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e2d6f-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e2d6f-114">LCS عبارة عن مدخل تعاون يوفر بيئة ومجموعه من الخدمات المحدثة بشكل منتظم والتي تساعدك علي أداره دوره حياه التطبيقات الخاصة بتطبيقات Dynamics 365 Finance and Operations الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="e2d6f-115">للحصول على مزيد من المعلومات، راجع [موارد Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="e2d6f-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e2d6f-116">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="e2d6f-116">Prerequisites</span></span>

<span data-ttu-id="e2d6f-117">قبل أن تتمكن من تثبيت الوظيفة الإضافية لرؤية المخزون، يجب عليك القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="e2d6f-118">احصل علي مشروع تنفيذ LCS مع نشر بيئة واحده علي الأقل.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="e2d6f-119">تأكد من اكتمال المتطلبات الأساسية لإعداد الوظائف الإضافية المتوفرة في [نظرة عامة على الوظائف الإضافية](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e2d6f-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="e2d6f-120">لا تتطلب رؤية المخزون ارتباطًا ثنائي الكتابة.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="e2d6f-121">تواصل مع فريق رؤية المخزون على [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) للحصول على الملفات الثلاثة المطلوبة التالية:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="e2d6f-122">`Inventory Visibility Integration.zip` (إذا كان إصدار Supply Chain Management الذي تقوم بتشغيله أقدم من الإصدار 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="e2d6f-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>

> [!NOTE]
> <span data-ttu-id="e2d6f-123">تتضمن البلدان والمناطق المدعومة حاليًا كندا والولايات المتحدة والاتحاد الأوروبي (EU).</span><span class="sxs-lookup"><span data-stu-id="e2d6f-123">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="e2d6f-124">إذا كانت لديك إيه اسئله حول هذه المتطلبات الاساسيه ، الرجاء الاتصال بفريق رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-124">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="e2d6f-125">إعداد Dataverse</span><span class="sxs-lookup"><span data-stu-id="e2d6f-125">Set up Dataverse</span></span>

<span data-ttu-id="e2d6f-126">اتبع هذه الخطوات لإعداد Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-126">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="e2d6f-127">إضافة مبدأ خدمة المستأجر الخاص بك:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-127">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="e2d6f-128">قم بتثبيت Azure AD الوحدة النمطية PowerShell الإصدار 2 كما هو موضح في [تثبيت Azure Active Directory PowerShell للرسم البياني](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="e2d6f-128">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="e2d6f-129">قم بتشغيل الأمر PowerShell التالي.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-129">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="e2d6f-130">إنشاء مستخدم تطبيق لرؤية المخزون في Dataverse:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-130">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="e2d6f-131">افتح عنوان URL الخاص ببيئة Dataverse الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-131">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="e2d6f-132">انتقل إلى **إعدادات متقدمة \> النظام \> الأمان \> المستخدمين**، وقم بإنشاء مستخدم تطبيق.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-132">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="e2d6f-133">استخدم القائمة عرض لتغيير طريقة عرض الصفحة إلى **مستخدمي التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-133">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="e2d6f-134">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-134">Select **New**.</span></span> <span data-ttu-id="e2d6f-135">عيّن معرف التطبيق إلى *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-135">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="e2d6f-136">(سيتم تحميل مُعرّف الكائن تلقائيًا عند حفظ التغييرات الخاصة بك.) يمكنك تخصيص الاسم.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-136">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="e2d6f-137">على سبيل المثال، يمكنك تغييره إلى *رؤية المخزون*.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-137">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="e2d6f-138">عند الانتهاء، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-138">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="e2d6f-139">حدد **تعيين دور**، ثم حدد **مسؤول النظام**.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-139">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="e2d6f-140">إذا كان هناك دور يسمي **مستخدم Common Data Service**، فحدده أيضًا.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-140">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="e2d6f-141">لمزيد من المعلومات، راجع [إنشاء مستخدم تطبيق](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="e2d6f-141">For more information, see [Create an application user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="e2d6f-142">قم باستيراد الملف `Inventory Visibility Dataverse Solution.zip`، الذي يتضمن تكوين Dataverse المرتبط بالكيانات و Power Apps:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-142">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="e2d6f-143">انتقل إلى الصفحة **حلول**.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-143">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="e2d6f-144">حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-144">Select **Import**.</span></span>

1. <span data-ttu-id="e2d6f-145">استيراد تدفق مشغل ترقية التكوين:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-145">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="e2d6f-146">انتقل إلى الصفحة Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-146">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="e2d6f-147">تأكد من وجود الاتصال المسمى *Dataverse (قديم)*.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-147">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="e2d6f-148">(إذا لم يكن موجودًا، فقم بإنشاءه).</span><span class="sxs-lookup"><span data-stu-id="e2d6f-148">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="e2d6f-149">استيراد الملف `Inventory Visibility Configuration Trigger.zip`.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-149">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="e2d6f-150">وبعد استيراده، سيظهر المشغل ضمن **التدفقات الخاصة بي**.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-150">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="e2d6f-151">قم بتهيئة المتغيرات الأربعة التالية استنادًا إلى معلومات البيئة:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-151">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="e2d6f-152">مُعرّف مستأجر Azure</span><span class="sxs-lookup"><span data-stu-id="e2d6f-152">Azure Tenant ID</span></span>
        - <span data-ttu-id="e2d6f-153">معرف عميل تطبيق Azure</span><span class="sxs-lookup"><span data-stu-id="e2d6f-153">Azure Application Client ID</span></span>
        - <span data-ttu-id="e2d6f-154">سر عميل تطبيق Azure</span><span class="sxs-lookup"><span data-stu-id="e2d6f-154">Azure Application Client Secret</span></span>
        - <span data-ttu-id="e2d6f-155">نقطة نهاية رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="e2d6f-155">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="e2d6f-156">لمزيد من المعلومات حول هذا المتغير، راجع القسم [إعداد تكامل رؤية المخزون](#setup-inventory-visibility-integration) لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-156">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="e2d6f-157">![مشغل التكوين](media/configuration-trigger.png "مشغل التكوين")</span><span class="sxs-lookup"><span data-stu-id="e2d6f-157">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="e2d6f-158">حدد **تشغيل**</span><span class="sxs-lookup"><span data-stu-id="e2d6f-158">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="e2d6f-159">تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="e2d6f-159">Install the add-in</span></span>

<span data-ttu-id="e2d6f-160">لتثبيت الوظيفة الإضافية لرؤية المخزون، يجب عليك القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-160">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="e2d6f-161">سجل الدخول إلى بوابة [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="e2d6f-161">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="e2d6f-162">في الصفحة الرئيسية ، حدد المشروع حيث يتم نشر البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-162">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="e2d6f-163">في الصفحة المشروع ، حدد البيئة التي ترغب في تثبيت الوظيفة الاضافيه بها.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-163">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="e2d6f-164">في الصفحة البيئة، قم بالتمرير لأسفل حتى تشاهد القسم **الوظائف الإضافية الخاصة بالبيئة** في القسم **Power Platform تكامل**، حيث يمكنك العثور على اسم بيئة Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-164">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="e2d6f-165">في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-165">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="e2d6f-166">![صفحة البيئة في LCS](media/inventory-visibility-environment.png "صفحة البيئة في LCS")</span><span class="sxs-lookup"><span data-stu-id="e2d6f-166">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="e2d6f-167">حدد الرابط **تثبيت وظيفة إضافية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-167">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="e2d6f-168">يتم فتح قائمه بالوظائف الاضافيه المتاحة.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-168">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="e2d6f-169">حدد **رؤية المخزون** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-169">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="e2d6f-170">ادخل قيما للحقول التالية الخاصة ببيئتك:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-170">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="e2d6f-171">**مُعرّف تطبيق AAD (العميل)**</span><span class="sxs-lookup"><span data-stu-id="e2d6f-171">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="e2d6f-172">**معرف مستأجر AAD**</span><span class="sxs-lookup"><span data-stu-id="e2d6f-172">**AAD tenant ID**</span></span>

    <span data-ttu-id="e2d6f-173">![أضافه في صفحه الاعداد](media/inventory-visibility-setup.png "صفحه اعداد الوظيفة الإضافية")</span><span class="sxs-lookup"><span data-stu-id="e2d6f-173">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="e2d6f-174">الموافقة علي البنود والشروط عن طريق تحديد خانه الاختيار **البنود والشروط**.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-174">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="e2d6f-175">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-175">Select **Install**.</span></span> <span data-ttu-id="e2d6f-176">ستظهر حاله الوظيفة الاضافيه باعتبارها **قيد التثبيت**.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-176">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="e2d6f-177">عند الانتهاء ، قم بتحديث الصفحة لرؤية تغيير الحالة علي **مثبت**.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-177">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="e2d6f-178">إلغاء تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="e2d6f-178">Uninstall the add-in</span></span>

<span data-ttu-id="e2d6f-179">للغاء تثبيت الوظيفة الاضافيه ، حدد **إلغاء التثبيت**.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-179">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="e2d6f-180">عندما تقوم بتحديث LCS، فإنه ستتم إزالة الوظيفة الإضافية لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-180">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="e2d6f-181">تقوم عمليه إزالة التثبيت على إزالة تسجيل الوظيفة الإضافية وبدء مهمة أيضًا لتنظيف كافة بيانات الشركات المخزنة في الخدمة.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-181">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="e2d6f-182">استخدام بيانات المخزون الفعلي من Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e2d6f-182">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="e2d6f-183">توزيع حزمة تكامل رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="e2d6f-183">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="e2d6f-184">إذا كنت تقوم بتشغيل Supply Chain Management الإصدار 10.0.17 أو إصدار سابق عنه، فتواصل بفريق دعم رؤية المخزون على [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) للحصول علي ملف الحزمة.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-184">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="e2d6f-185">ثم قم بنشر الحزمة في LCS.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-185">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="e2d6f-186">إذا حدث خطأ عدم تطابق في الإصدار أثناء التوزيع، يجب عليك استيراد مشروع X++ يدويًا إلى بيئة التطوير الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-186">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="e2d6f-187">ثم قم بإنشاء الحزمة القابلة للنشر في بيئة التطوير الخاصة بك، ثم قم بنشرها في بيئة الإنتاج الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-187">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="e2d6f-188">يتم تضمين الكود Supply Chain Management في الإصدار 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-188">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="e2d6f-189">إذا كنت تقوم بتشغيل هذا الإصدار أو الأحدث، فإن عملية النشر تكون غير ضرورية.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-189">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="e2d6f-190">تأكد من أنه يتم تشغيل الميزات التالية في بيئة Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-190">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="e2d6f-191">(افتراضيًا، فإنه يتم تشغيلها.)</span><span class="sxs-lookup"><span data-stu-id="e2d6f-191">(By default, they are turned on.)</span></span>

| <span data-ttu-id="e2d6f-192">وصف الميزة</span><span class="sxs-lookup"><span data-stu-id="e2d6f-192">Feature description</span></span> | <span data-ttu-id="e2d6f-193">إصدار الكود</span><span class="sxs-lookup"><span data-stu-id="e2d6f-193">Code version</span></span> | <span data-ttu-id="e2d6f-194">تبديل الفئة</span><span class="sxs-lookup"><span data-stu-id="e2d6f-194">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="e2d6f-195">تمكين أو تعطيل استخدام أبعاد المخزون في جدول InventSum</span><span class="sxs-lookup"><span data-stu-id="e2d6f-195">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="e2d6f-196">10.0.11</span><span class="sxs-lookup"><span data-stu-id="e2d6f-196">10.0.11</span></span> | <span data-ttu-id="e2d6f-197">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="e2d6f-197">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="e2d6f-198">تمكين أو تعطيل استخدام أبعاد المخزون في جدول InventSumDelta</span><span class="sxs-lookup"><span data-stu-id="e2d6f-198">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="e2d6f-199">10.0.12</span><span class="sxs-lookup"><span data-stu-id="e2d6f-199">10.0.12</span></span> | <span data-ttu-id="e2d6f-200">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="e2d6f-200">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="e2d6f-201">إعداد تكامل رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="e2d6f-201">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="e2d6f-202">في Supply Chain Management، افتح مساحة عمل **[إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**، وقم بتشغيل الميزة **تكامل رؤية المخزون**.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-202">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="e2d6f-203">انتقل إلى **إدارة المخزون \> الإعداد \> معلمات تكامل رؤية المخزون**، وأدخل عنوان URL للبيئة التي تقوم فيها بتشغيل رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-203">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="e2d6f-204">ابحث عن منطقة LCS الخاصة ببيئة Azure، ثم أدخل عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-204">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="e2d6f-205">يحتوي عنوان URL على النموذج التالي:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-205">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="e2d6f-206">على سبيل المثال، إذا كنت في أوروبا، سيكون لدي البيئة واحدًا من عناوين (URL) التالية:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-206">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="e2d6f-207">تتوفر المناطق التالية حاليًا.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-207">The following regions are currently available.</span></span>

    | <span data-ttu-id="e2d6f-208">منطقة Azure</span><span class="sxs-lookup"><span data-stu-id="e2d6f-208">Azure region</span></span> | <span data-ttu-id="e2d6f-209">اسم المنطقة القصير</span><span class="sxs-lookup"><span data-stu-id="e2d6f-209">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="e2d6f-210">شرق أستراليا</span><span class="sxs-lookup"><span data-stu-id="e2d6f-210">Australia east</span></span> | <span data-ttu-id="e2d6f-211">eau</span><span class="sxs-lookup"><span data-stu-id="e2d6f-211">eau</span></span> |
    | <span data-ttu-id="e2d6f-212">جنوب شرق أستراليا</span><span class="sxs-lookup"><span data-stu-id="e2d6f-212">Australia southeast</span></span> | <span data-ttu-id="e2d6f-213">seau</span><span class="sxs-lookup"><span data-stu-id="e2d6f-213">seau</span></span> |
    | <span data-ttu-id="e2d6f-214">وسط كندا</span><span class="sxs-lookup"><span data-stu-id="e2d6f-214">Canada central</span></span> | <span data-ttu-id="e2d6f-215">cca</span><span class="sxs-lookup"><span data-stu-id="e2d6f-215">cca</span></span> |
    | <span data-ttu-id="e2d6f-216">شرق كندا</span><span class="sxs-lookup"><span data-stu-id="e2d6f-216">Canada east</span></span> | <span data-ttu-id="e2d6f-217">eca</span><span class="sxs-lookup"><span data-stu-id="e2d6f-217">eca</span></span> |
    | <span data-ttu-id="e2d6f-218">شمال أوروبا</span><span class="sxs-lookup"><span data-stu-id="e2d6f-218">North Europe</span></span> | <span data-ttu-id="e2d6f-219">neu</span><span class="sxs-lookup"><span data-stu-id="e2d6f-219">neu</span></span> |
    | <span data-ttu-id="e2d6f-220">غرب أوروبا</span><span class="sxs-lookup"><span data-stu-id="e2d6f-220">West Europe</span></span> | <span data-ttu-id="e2d6f-221">weu</span><span class="sxs-lookup"><span data-stu-id="e2d6f-221">weu</span></span> |
    | <span data-ttu-id="e2d6f-222">شرق الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="e2d6f-222">East US</span></span> | <span data-ttu-id="e2d6f-223">eus</span><span class="sxs-lookup"><span data-stu-id="e2d6f-223">eus</span></span> |
    | <span data-ttu-id="e2d6f-224">غرب الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="e2d6f-224">West US</span></span> | <span data-ttu-id="e2d6f-225">wus</span><span class="sxs-lookup"><span data-stu-id="e2d6f-225">wus</span></span> |

1. <span data-ttu-id="e2d6f-226">انتقل إلى **إدارة المخزون \> دوري \> تكامل رؤية المخزون**، وقم بتمكين الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-226">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="e2d6f-227">سيتم الآن ترحيل كافة أحداث تغيير المخزون من Supply Chain Management إلى رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-227">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="e2d6f-228">واجهة API العامة للوظيفة الإضافية لرؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="e2d6f-228">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="e2d6f-229">تقدم واجهة برمجة التطبيقات العامة لـ REST الخاصة بالوظيفة الإضافية لرؤية المخزون العديد من نقاط التكامل الخاصة.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-229">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="e2d6f-230">ويدعم ثلاثه أنواع من التفاعلات الرئيسية:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-230">It supports three main interaction types:</span></span>

- <span data-ttu-id="e2d6f-231">ترحيل تغييرات المخزون الفعلية إلى الوظيفة الإضافية من نظام خارجي</span><span class="sxs-lookup"><span data-stu-id="e2d6f-231">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="e2d6f-232">الاستعلام عن الكميات الفعلية الحالية من نظام خارجي</span><span class="sxs-lookup"><span data-stu-id="e2d6f-232">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="e2d6f-233">مزامنة تلقائية مع مخزون Supply Chain Management الفعلي</span><span class="sxs-lookup"><span data-stu-id="e2d6f-233">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="e2d6f-234">لا تعتبر المزامنة التلقائية جزءًا من API العامة.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-234">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="e2d6f-235">وبدلاً من ذلك، تتم معالجتة في الخلفية للبيئات التي تم فيها تمكين الوظيفة الإضافية لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-235">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="e2d6f-236">مصادقة</span><span class="sxs-lookup"><span data-stu-id="e2d6f-236">Authentication</span></span>

<span data-ttu-id="e2d6f-237">يتم استخدام الرمز المميز لأمان النظام الأساسي لاستدعاء الوظيفة الإضافية لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-237">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="e2d6f-238">ولذلك، يجب إنشاء رمز *Azure Active Directory (Azure AD) المميز* باستخدام تطبيق Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-238">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="e2d6f-239">يجب استخدام رمز Azure AD المميز للحصول على *رمز الوصول المميز* من خدمة الأمان.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-239">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="e2d6f-240">احصل علي رمز خدمه أمان بالقيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-240">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="e2d6f-241">سجل دخولك إلى مدخل Azure واستخدمه للعثور على `clientId` و `clientSecret` لتطبيق Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-241">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="e2d6f-242">إحضار Azure Active Directory رمز مميز (`aadToken`) عن طريق إرسال طلب HTTP بالخصائص التالية:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-242">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="e2d6f-243">**عنوان URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="e2d6f-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="e2d6f-244">**الطريقة** - `GET`</span><span class="sxs-lookup"><span data-stu-id="e2d6f-244">**Method** - `GET`</span></span>
    - <span data-ttu-id="e2d6f-245">**محتوي النص الأساسي (بيانات النموذج)**:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-245">**Body content (form data)**:</span></span>

        | <span data-ttu-id="e2d6f-246">المفتاح</span><span class="sxs-lookup"><span data-stu-id="e2d6f-246">key</span></span> | <span data-ttu-id="e2d6f-247">القيمة</span><span class="sxs-lookup"><span data-stu-id="e2d6f-247">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="e2d6f-248">client_id</span><span class="sxs-lookup"><span data-stu-id="e2d6f-248">client_id</span></span> | <span data-ttu-id="e2d6f-249">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="e2d6f-249">${aadAppId}</span></span> |
        | <span data-ttu-id="e2d6f-250">client_secret</span><span class="sxs-lookup"><span data-stu-id="e2d6f-250">client_secret</span></span> | <span data-ttu-id="e2d6f-251">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="e2d6f-251">${aadAppSecret}</span></span> |
        | <span data-ttu-id="e2d6f-252">grant_type</span><span class="sxs-lookup"><span data-stu-id="e2d6f-252">grant_type</span></span> | <span data-ttu-id="e2d6f-253">client_credentials</span><span class="sxs-lookup"><span data-stu-id="e2d6f-253">client_credentials</span></span> |
        | <span data-ttu-id="e2d6f-254">مورد</span><span class="sxs-lookup"><span data-stu-id="e2d6f-254">resource</span></span> | <span data-ttu-id="e2d6f-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="e2d6f-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="e2d6f-256">يجب ان تتلقي `aadToken` استجابه فيها، والتي تشبه المثال التالي.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-256">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="e2d6f-257">المستقبل طلب JSON مشابها لما يلي:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-257">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="e2d6f-258">المكان:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-258">Where:</span></span>
    - <span data-ttu-id="e2d6f-259">`client_assertion`يجب ان تكون القيمة هي `aadToken` التي استلمتها في الخطوة السابقة.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-259">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="e2d6f-260">`context`يجب ان تكون القيمة معرف البيئة حيث تريد توزيع الوظيفة الاضافيه.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-260">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="e2d6f-261">قم بتعيين كافة القيم الأخرى كما هو موضح في المثال.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-261">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="e2d6f-262">قم بإرسال طلب HTTP بالخصائص التالية:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-262">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="e2d6f-263">**عنوان URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="e2d6f-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="e2d6f-264">**الطريقة** - `POST`</span><span class="sxs-lookup"><span data-stu-id="e2d6f-264">**Method** - `POST`</span></span>
    - <span data-ttu-id="e2d6f-265">**راس HTTP** - تضمين إصدار API (`Api-Version` المفتاح هو والقيمة هو `1.0`)</span><span class="sxs-lookup"><span data-stu-id="e2d6f-265">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="e2d6f-266">**محتوي أساسي** - تضمين طلب JSON الذي قمت بإنشاءه في الخطوة السابقة.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-266">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="e2d6f-267">ستحصل علي `access_token` في الاستجابة.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-267">You will get an `access_token` in response.</span></span> <span data-ttu-id="e2d6f-268">وهذا ما تحتاجه كرمز مميز في الحامل لاستدعاء امكانيه رؤية API للمخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-268">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="e2d6f-269">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-269">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="e2d6f-270">تكوين واجهه برمجه تطبيقات امكانيه رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="e2d6f-270">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="e2d6f-271">قبل استخدام الخدمة ، يجب إكمال التكوينات الموضحة في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-271">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="e2d6f-272">قد يختلف التكوين استنادا إلى تفاصيل البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-272">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="e2d6f-273">وهو يتضمن بشكل أساسي أربعه أجزاء:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-273">It primarily includes four parts:</span></span>

- [<span data-ttu-id="e2d6f-274">تقسيم</span><span class="sxs-lookup"><span data-stu-id="e2d6f-274">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="e2d6f-275">تكوينات الأبعاد</span><span class="sxs-lookup"><span data-stu-id="e2d6f-275">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="e2d6f-276">فهرسة</span><span class="sxs-lookup"><span data-stu-id="e2d6f-276">Indexing</span></span>](#indexing)
- [<span data-ttu-id="e2d6f-277">قياس مخصص</span><span class="sxs-lookup"><span data-stu-id="e2d6f-277">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="e2d6f-278">تقسيم</span><span class="sxs-lookup"><span data-stu-id="e2d6f-278">Partitioning</span></span>

<span data-ttu-id="e2d6f-279">يمكن للتقسيم ان يؤثر بشكل كبير علي أداء واجهة API الخاصة برؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-279">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="e2d6f-280">انها لفكره جيده ان تقوم بتعريف نظام يسمح بالتجميعات الصغيرة للبيانات مع استمرار السماح باستعلامات البيانات ذات المعني.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-280">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="e2d6f-281">سيكون `organizationId` (`dataAreaId` في Supply Chain Management) دائما جزءا من التقسيم ، ويتم تعيين رؤية المخزون بشكل افتراضي علي قسم حسب الابعاد *كموقع إلكتروني + موقع جغرافي*.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-281">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="e2d6f-282">وهذا يعني انه يجب دوما الاستعلام عن الخدمة باستخدام هذه الابعاد المحددة في عوامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-282">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="e2d6f-283">*الموقع الإلكتروني* و *الموقع الجغرافي* هما اثنان من الابعاد الافتراضية في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-283">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="e2d6f-284">في Supply Chain Management، تسمي هذه الابعاد *بالموقع الإلكتروني* (`InventSiteId`) *والمستودع* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="e2d6f-284">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="e2d6f-285">تكوينات الأبعاد</span><span class="sxs-lookup"><span data-stu-id="e2d6f-285">Dimension configurations</span></span>

<span data-ttu-id="e2d6f-286">ستوفر امكانيه رؤية المخزون قائمه بالابعاد الافتراضية العامة لتمكين تكامل النظام المصدر المتعدد.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-286">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="e2d6f-287">يسرد الجدول التالي ابعاد المخزون التي ستكون أسماء الابعاد الافتراضية في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-287">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="e2d6f-288">نوع البعد</span><span class="sxs-lookup"><span data-stu-id="e2d6f-288">Dimension type</span></span> | <span data-ttu-id="e2d6f-289">اسم البُعد</span><span class="sxs-lookup"><span data-stu-id="e2d6f-289">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="e2d6f-290">منتج</span><span class="sxs-lookup"><span data-stu-id="e2d6f-290">Product</span></span> | `ColorId` |
| <span data-ttu-id="e2d6f-291">منتج</span><span class="sxs-lookup"><span data-stu-id="e2d6f-291">Product</span></span> | `SizeId` |
| <span data-ttu-id="e2d6f-292">منتج</span><span class="sxs-lookup"><span data-stu-id="e2d6f-292">Product</span></span> | `StyleId` |
| <span data-ttu-id="e2d6f-293">منتج</span><span class="sxs-lookup"><span data-stu-id="e2d6f-293">Product</span></span> | `ConfigId` |
| <span data-ttu-id="e2d6f-294">التعقب</span><span class="sxs-lookup"><span data-stu-id="e2d6f-294">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="e2d6f-295">التعقب</span><span class="sxs-lookup"><span data-stu-id="e2d6f-295">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="e2d6f-296"> الموق</span><span class="sxs-lookup"><span data-stu-id="e2d6f-296">Location</span></span> | `LocationId` |
| <span data-ttu-id="e2d6f-297"> الموق</span><span class="sxs-lookup"><span data-stu-id="e2d6f-297">Location</span></span> | `SiteId` |
| <span data-ttu-id="e2d6f-298">حالة المخزون</span><span class="sxs-lookup"><span data-stu-id="e2d6f-298">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="e2d6f-299">خاص بالمستودع</span><span class="sxs-lookup"><span data-stu-id="e2d6f-299">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="e2d6f-300">خاص بالمستودع</span><span class="sxs-lookup"><span data-stu-id="e2d6f-300">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="e2d6f-301">خاص بالمستودع</span><span class="sxs-lookup"><span data-stu-id="e2d6f-301">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="e2d6f-302">يكون نوع البعد المدرج في الجدول السابق كمرجع فقط.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-302">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="e2d6f-303">لا يلزم تحديد نوع البعد في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-303">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="e2d6f-304">في حاله وجود بعد مخصص والحاجة إلى التدفق للقيمة الافتراضية عند استهلاك رؤية المخزون ، يمكنك تكوين **اسم البعد المخصص** في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-304">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="e2d6f-305">وصول الانظمه الخارجية إلى رؤية المخزون من خلال واجات برمجه التطبيقات RESTful التي تتيح معلومات الكمية الفعلية حول مجموعات الابعاد المحددة التي سيتم الاستعلام عنها.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-305">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="e2d6f-306">بالنسبة للتكامل ، يمكنك رؤية المخزون من تكوين *مصدر بيانات القناة الخارجية* وبعد المصدر علي *الابعاد المستهدفة* في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-306">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="e2d6f-307">يجب ان تكون الابعاد المستهدفة واحده مما يلي:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-307">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="e2d6f-308">الابعاد الافتراضية في رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="e2d6f-308">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="e2d6f-309">الأبعاد المخصصة</span><span class="sxs-lookup"><span data-stu-id="e2d6f-309">Custom dimensions</span></span>

<span data-ttu-id="e2d6f-310">والغرض من تكوين الابعاد هو توحيد التكامل المتعدد الانظمه للاستعلام علي الابعاد وحدث الترحيل مع الابعاد.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-310">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="e2d6f-311">فهرسة</span><span class="sxs-lookup"><span data-stu-id="e2d6f-311">Indexing</span></span>

<span data-ttu-id="e2d6f-312">في معظم الأوقات ، لن يكون الاستعلام الفعلي الخاص بالمخزون علي مستوي "الإجمالي" الأعلى فقط ، ولكن قد ترغب في رؤية النتائج المجمعة استنادا إلى ابعاد المخزون.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-312">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="e2d6f-313">توفر امكانيه رؤية المخزون المرونة عن طريق السماح لك باعداد الفهارس ، التي تعتمد علي البعد أو مجموعه الابعاد.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-313">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="e2d6f-314">حاليا ، يمكنك فقط تكوين الفهارس بخمسه كحد اقصي.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-314">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="e2d6f-315">يجب مراعاه البعد أو مجموعه الابعاد التي ستستخدمها قبل التنفيذ للتاكد من انها ستفي باحتياجات أعمالك.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-315">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="e2d6f-316">علي سبيل المثال ، إذا كنت ترغب في الاستعلام عن المنتجات كالتالي:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-316">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="e2d6f-317">الاستعلام عن المنتج المجمع الفعلي بواسطة ابعاد *اللون* و *الحجم*.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-317">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="e2d6f-318">في بعض الحالات ، تريد فقط الاستعلام عن المنتج إجمالا.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-318">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="e2d6f-319">سيكون لديك فهرسين محددين كالتالي:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-319">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="e2d6f-320">سيتم تجميع القوس الفارغ استنادا إلى "معرف المنتج" داخل القسم.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-320">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="e2d6f-321">تحدد الفهرسة كيفيه تجميع النتائج استنادا إلى اعداد الاستعلام `groupBy`.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-321">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="e2d6f-322">في هذه الحالة إذا لم تقم بتحديد أي قيم `groupBy`، سيتم الحصول علي الإجماليات بواسطة `productid`.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-322">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="e2d6f-323">وإلا، إذا قمت بتحديد `groupBy` كـ `groupBy=ColorId&groupBy=SizeId`، ستحصل على بنود متعددة يتم إرجاعها، استنادًا إلى مجموعتي اللون والحجم المختلفتين في النظام.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-323">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="e2d6f-324">يمكنك وضع معايير الاستعلام في النص الأساسي للطلب.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-324">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="e2d6f-325">فيما يلي نموذج استعلام حول المنتج بمجموعه اللون والحجم.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-325">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="e2d6f-326">قياس مخصص</span><span class="sxs-lookup"><span data-stu-id="e2d6f-326">Custom measurement</span></span>

<span data-ttu-id="e2d6f-327">يتم ربط كميات القياس الافتراضية بـ Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-327">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="e2d6f-328">ومع ذلك، قد ترغب في الحصول على كمية تتكون من مجموعة من القياسات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-328">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="e2d6f-329">وللقيام بذلك ، يمكن ان يكون لديك تكوين كميات مخصصه ، والتي ستتم اضافتها إلى إخراج الاستعلامات الفعلية.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-329">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="e2d6f-330">وتتيح الوظيفة ببساطه تحديد مجموعه من القياسات التي ستتم اضافتها ، و/أو مجموعه من المقاييس التي سيتم طرحها ، من أجل القياس المخصص.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-330">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="e2d6f-331">علي سبيل المثال ، باستخدام شرط الاستعلام التالي ، ستقوم بتكوين كميه القياس المخصصة باعتبارها `MyCustomAvailableforReservation` ليتم استهلاكها من قبل نظام الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-331">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="e2d6f-332">نظام الاستهلاك</span><span class="sxs-lookup"><span data-stu-id="e2d6f-332">Consumption system</span></span> | <span data-ttu-id="e2d6f-333">القياسات المحتسبة</span><span class="sxs-lookup"><span data-stu-id="e2d6f-333">Calculated measurers</span></span> | <span data-ttu-id="e2d6f-334">مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="e2d6f-334">Data source</span></span> | <span data-ttu-id="e2d6f-335">أداه التعديل</span><span class="sxs-lookup"><span data-stu-id="e2d6f-335">Modifier</span></span> | <span data-ttu-id="e2d6f-336">نوع حساب أداة التعديل</span><span class="sxs-lookup"><span data-stu-id="e2d6f-336">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="e2d6f-337">الجمع</span><span class="sxs-lookup"><span data-stu-id="e2d6f-337">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="e2d6f-338">الجمع</span><span class="sxs-lookup"><span data-stu-id="e2d6f-338">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="e2d6f-339">الطرح</span><span class="sxs-lookup"><span data-stu-id="e2d6f-339">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="e2d6f-340">الجمع</span><span class="sxs-lookup"><span data-stu-id="e2d6f-340">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="e2d6f-341">الطرح</span><span class="sxs-lookup"><span data-stu-id="e2d6f-341">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="e2d6f-342">الجمع</span><span class="sxs-lookup"><span data-stu-id="e2d6f-342">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="e2d6f-343">الجمع</span><span class="sxs-lookup"><span data-stu-id="e2d6f-343">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="e2d6f-344">الطرح</span><span class="sxs-lookup"><span data-stu-id="e2d6f-344">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="e2d6f-345">الطرح</span><span class="sxs-lookup"><span data-stu-id="e2d6f-345">Subtraction</span></span> |

<span data-ttu-id="e2d6f-346">ومع ذلك ، سيقوم الاستعلام الموجود علي كميه القياس المخصصة بإرجاع المخرجات التالية.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-346">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="e2d6f-347">يعتمد إخراج `MyCustomAvailableforReservation`علي اعداد الحساب في القياسات المخصصة كما يلي:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-347">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="e2d6f-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="e2d6f-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="e2d6f-349">ترحيل التغييرات الفعلية</span><span class="sxs-lookup"><span data-stu-id="e2d6f-349">Posting on-hand changes</span></span>

<span data-ttu-id="e2d6f-350">ويعتمد عنوان URL الذي يتم ترحيل الحدث عليه علي المنطقة الجغرافية بالبالضبط.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-350">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="e2d6f-351">سياخذ النموذج ما يلي:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-351">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="e2d6f-352">عند المصادقة ، يمكن استخدام محدد موقع المعلومات (URL) هذا مع أسلوب `POST` HTTP لإرسال احداث التغيير الفعلي إلى الخدمة.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-352">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="e2d6f-353">يتم استخدام الراس الخاص للاتصال مع خدمات Dynamics 365 من خلال طلبات HTTP ، والذي يشير إلى معرف البيئة لمثيل Supply Chain Management الذي ترتبط به البيانات.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-353">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="e2d6f-354">على سبيل المثال:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-354">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="e2d6f-355">ترحيل التغييرات الفعلية مثال الاستعلام 1</span><span class="sxs-lookup"><span data-stu-id="e2d6f-355">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="e2d6f-356">يوضح هذا المثال السيناريو الذي ستقوم فيه باعداد تكوين البعد في Power Apps.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-356">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="e2d6f-357">استخدم الاستعلام التالي لتكوين تعيين البعد في Power Apps:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-357">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="e2d6f-358">يمكنك الآن تحديد `dimensionDataSource` واستخدام الابعاد المخصصة في الاستعلامات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-358">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="e2d6f-359">سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-359">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="e2d6f-360">ترحيل التغييرات الفعلية مثال الاستعلام 2</span><span class="sxs-lookup"><span data-stu-id="e2d6f-360">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="e2d6f-361">يوضح هذا المثال السيناريو الذي لا يتم فيه اعداد تعيينات لتكوين البعد في Power Apps، التالي يجب ان تستخدم الترحيل أيضا الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-361">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="e2d6f-362">يجب ان تكون كافة الابعاد بابعاد أساسيه عندما يكون الحقل `dimensionDataSource` خاليا أو فارغا أو مسافة بيضاء.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-362">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="e2d6f-363">خصائص حقل مستند JSON</span><span class="sxs-lookup"><span data-stu-id="e2d6f-363">JSON document field properties</span></span>

<span data-ttu-id="e2d6f-364">تتضمن الحقول الموجودة في أمثله استعلام JSON المتوفرة في السابق الخصائص المسرودة في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-364">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="e2d6f-365">معرف الحقل</span><span class="sxs-lookup"><span data-stu-id="e2d6f-365">Field ID</span></span> | <span data-ttu-id="e2d6f-366">الوصف</span><span class="sxs-lookup"><span data-stu-id="e2d6f-366">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="e2d6f-367">معرف فريد لحدث التغيير المحدد.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-367">A unique ID for the specific change event.</span></span> <span data-ttu-id="e2d6f-368">يتم استخدام هذا المعرف للتاكد من فشل الاتصال بالخدمة اثناء الترحيل ، ولن يؤدي أعاده إرسال الحدث إلى نفس الحدث الذي يتم حسابه مرتين في النظام.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-368">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="e2d6f-369">معرف المؤسسة المرتبط بالحدث.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-369">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="e2d6f-370">وهذا ما يعين لمؤسسات Supply Chain Management أو معرفات مناطق البيانات.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-370">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="e2d6f-371">معرف أمر الإنتاج المحدد.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-371">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="e2d6f-372">الكمية التي يجب تغيير الكمية الحالية وفقا لها.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-372">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="e2d6f-373">علي سبيل المثال ، تمت أضافه 10 قطع من خبز البيغلز جديده إلى الرف، ستكون هذه القيمة 10.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-373">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="e2d6f-374">إذا تمت أزاله 3 قطع من خبز البيغلز من الرف أو بيعه ، ستكون هذه القيمة -3.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-374">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="e2d6f-375">مصدر البيانات الخاص بالابعاد المستخدمة في حدث تغيير الترحيل والاستعلام.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-375">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="e2d6f-376">إذا قمت بتحديد مصدر البيانات ، يمكنك استخدام الابعاد المخصصة من مصدر البيانات المحدد.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-376">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="e2d6f-377">باستخدام تكوين البعد ، يمكن ان يقوم ظهور المخزون بتعيين الابعاد المخصصة إلى الابعاد الافتراضية العامة.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-377">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="e2d6f-378">في حاله عدم تحديد `dimensionDataSource`، يمكنك استخدام الابعاد الافتراضية العامة فقط في الاستعلامات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-378">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="e2d6f-379">كيس مجموعه حيوية من أزواج مفتاح/قيمه.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-379">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="e2d6f-380">سيتم تعيينها لبعض الابعاد في Supply Chain Management، ولكن يمكنك أيضا أضافه ابعاد مخصصه (مثل *المصدر*) والتي قد تشير إلى ما إذا كان الحدث واردا من Supply Chain Management أو من النظام الخارجي.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-380">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="e2d6f-381">الاستعلام عن الكمية الحالية</span><span class="sxs-lookup"><span data-stu-id="e2d6f-381">Querying current on-hand</span></span>

<span data-ttu-id="e2d6f-382">سيكون للنقطة النهائية للاستعلام عن الكمية الحالية عنوان URL مشابه:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-382">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="e2d6f-383">سيتم الاستعلام عنها باستخدام أسلوب `POST` HTTP.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-383">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="e2d6f-384">مثال علي الاستعلام الفعلي حاليا 1</span><span class="sxs-lookup"><span data-stu-id="e2d6f-384">Current on-hand query example 1</span></span>

<span data-ttu-id="e2d6f-385">يوضح هذا المثال السيناريو الذي ستقوم فيه باعداد تكوين البعد في Power Apps.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-385">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="e2d6f-386">استخدم الاستعلام التالي لتكوين تعيين البعد في Power Apps:</span><span class="sxs-lookup"><span data-stu-id="e2d6f-386">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="e2d6f-387">يمكنك الآن تحديد `dimensionDataSource` واستخدام الابعاد المخصصة في الاستعلامات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-387">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="e2d6f-388">سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-388">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="e2d6f-389">يمكنك تحديد `DimensionDataSource` في `filters` وتحديد ابعاد مخصصه في كل من `filters` و`groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-389">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="e2d6f-390">سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-390">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="e2d6f-391">مثال علي الاستعلام الفعلي حاليا 2</span><span class="sxs-lookup"><span data-stu-id="e2d6f-391">Current on-hand query example 2</span></span>

<span data-ttu-id="e2d6f-392">يوضح هذا المثال السيناريو الذي لا يتم فيه اعداد تعيينات لتكوين البعد في Power Apps، التالي يجب ان تستخدم الترحيل أيضا الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-392">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="e2d6f-393">يجب ان تكون كافة الابعاد بابعاد أساسيه عندما يكون الحقل `dimensionDataSource`، ضمن `filters` خاليا أو فارغا أو مسافة بيضاء.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-393">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="e2d6f-394">مثال نتيجة الإرجاع</span><span class="sxs-lookup"><span data-stu-id="e2d6f-394">Example return result</span></span>

<span data-ttu-id="e2d6f-395">قد تؤدي الاستعلامات المعروضة في الامثله السابقة إلى إرجاع نتيجة مثل هذه.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-395">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="e2d6f-396">لاحظ انه يتم بناء حقول الكميات كقاموس للمقاييس والقيم المقترنة بها.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-396">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
