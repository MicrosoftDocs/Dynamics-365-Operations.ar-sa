---
title: الوظيفة الإضافية لرؤية المخزون
description: يوضح هذا الموضوع كيفيه تثبيت الوظيفة الإضافية لرؤية المخزون وتكوينها لـ Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d09c7be5de75511b10d7a69d4b8ac12917b0dbe8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910415"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="7faa5-103">الوظيفة الإضافية لرؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="7faa5-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="7faa5-104">تعد الوظيفة الإضافية لرؤية المخزون بمثابه خدمة صغيرة مستقله وقابله للتغيير بشكل كبير والتي تمكن تتبع المخزون الفعلي في الوقت الحقيقي ، مما يوفر عرضا شاملا لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="7faa5-105">يتم تصدير كافة المعلومات المرتبطة بالمخزون الفعلي إلى الخدمة بالقرب من الوقت الحقيقي خلال تكامل SQL في المستوي المنخفض.</span><span class="sxs-lookup"><span data-stu-id="7faa5-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="7faa5-106">تقوم الانظمه الخارجية بالوصول إلى الخدمة من خلال واجهات RESTful API للاستعلام عن المعلومات الفعلية حول المجموعات المحددة من الابعاد ، ومن ثم استرداد قائمه بالمناصب الفعلية المتاحة.</span><span class="sxs-lookup"><span data-stu-id="7faa5-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="7faa5-107">رؤية المخزون عبارة عن خدمة صغيرة مضمنة في Microsoft Dataverse، مما يعني انه يمكنك توسيعها بواسطة إنشاء Power Apps وتطبيق Power BI لتوفير وظيفة مخصصه لتلبيه متطلبات الاعمال الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="7faa5-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="7faa5-108">من الممكن أيضا ترقيه الفهرس للقيام باستعلامات المخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="7faa5-109">توفر امكانيه رؤية المخزون خيارات التكوين التي تتيح له التكامل مع أنظمه متعددة الجهات الخارجية.</span><span class="sxs-lookup"><span data-stu-id="7faa5-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="7faa5-110">وهو يدعم بعد المخزون القياسي والقابلية للتوسعة المخصصة والكميات التي تم حسابها والقياسية القابلة للتكوين.</span><span class="sxs-lookup"><span data-stu-id="7faa5-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="7faa5-111">يصف هذا الموضوع كيفيه تثبيت وتكوين الوظيفة الإضافية لرؤية المخزون لـ Dynamics 365 Supply Chain Management، وكيفيه استخدام واجهه برمجه التطبيقات (API) الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="7faa5-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="7faa5-112">تثبيت الوظيفة الإضافية لرؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="7faa5-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="7faa5-113">يجب تثبيت الوظيفة الإضافية لرؤية المخزون باستخدام Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="7faa5-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="7faa5-114">LCS عبارة عن مدخل تعاون يوفر بيئة ومجموعه من الخدمات المحدثة بشكل منتظم والتي تساعدك علي أداره دوره حياه التطبيقات الخاصة بتطبيقات Dynamics 365 Finance and Operations الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="7faa5-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="7faa5-115">للحصول على مزيد من المعلومات، راجع [موارد Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="7faa5-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7faa5-116">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="7faa5-116">Prerequisites</span></span>

<span data-ttu-id="7faa5-117">قبل أن تتمكن من تثبيت الوظيفة الإضافية لرؤية المخزون، يجب عليك القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="7faa5-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="7faa5-118">احصل علي مشروع تنفيذ LCS مع نشر بيئة واحده علي الأقل.</span><span class="sxs-lookup"><span data-stu-id="7faa5-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="7faa5-119">تأكد من اكتمال المتطلبات الأساسية لإعداد الوظائف الإضافية المتوفرة في [نظرة عامة على الوظائف الإضافية](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7faa5-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="7faa5-120">لا تتطلب رؤية المخزون ارتباطًا ثنائي الكتابة.</span><span class="sxs-lookup"><span data-stu-id="7faa5-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="7faa5-121">تواصل مع فريق رؤية المخزون على [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) للحصول على الملفات الثلاثة المطلوبة التالية:</span><span class="sxs-lookup"><span data-stu-id="7faa5-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="7faa5-122">`Inventory Visibility Integration.zip` (إذا كان إصدار Supply Chain Management الذي تقوم بتشغيله أقدم من الإصدار 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="7faa5-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="7faa5-123">اتبع الإرشادات المذكورة في [تشغيل سريع: تسجيل تطبيق مع النظام الأساسي للهوية في Microsoft](/azure/active-directory/develop/quickstart-register-app) لتسجيل تطبيق وإضافة سر العميل ضمن اشتراكك في Azure.</span><span class="sxs-lookup"><span data-stu-id="7faa5-123">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
    - [<span data-ttu-id="7faa5-124">تسجيل تطبيق</span><span class="sxs-lookup"><span data-stu-id="7faa5-124">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
    - [<span data-ttu-id="7faa5-125">إضافة سر عميل</span><span class="sxs-lookup"><span data-stu-id="7faa5-125">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
    - <span data-ttu-id="7faa5-126">سيتم استخدام **معرف التطبيق (العميل)** و **سر العميل** و **معرف المستأجر** في الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="7faa5-126">The **Application(Client) Id**, **Client Secret** and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="7faa5-127">تتضمن البلدان والمناطق المدعومة حاليًا كندا والولايات المتحدة والاتحاد الأوروبي (EU).</span><span class="sxs-lookup"><span data-stu-id="7faa5-127">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="7faa5-128">إذا كانت لديك إيه اسئله حول هذه المتطلبات الاساسيه ، الرجاء الاتصال بفريق رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-128">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="7faa5-129">إعداد Dataverse</span><span class="sxs-lookup"><span data-stu-id="7faa5-129">Set up Dataverse</span></span>

<span data-ttu-id="7faa5-130">اتبع هذه الخطوات لإعداد Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7faa5-130">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="7faa5-131">إضافة مبدأ خدمة المستأجر الخاص بك:</span><span class="sxs-lookup"><span data-stu-id="7faa5-131">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="7faa5-132">قم بتثبيت Azure AD الوحدة النمطية PowerShell الإصدار 2 كما هو موضح في [تثبيت Azure Active Directory PowerShell للرسم البياني](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="7faa5-132">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="7faa5-133">قم بتشغيل الأمر PowerShell التالي.</span><span class="sxs-lookup"><span data-stu-id="7faa5-133">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="7faa5-134">إنشاء مستخدم تطبيق لرؤية المخزون في Dataverse:</span><span class="sxs-lookup"><span data-stu-id="7faa5-134">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="7faa5-135">افتح عنوان URL الخاص ببيئة Dataverse الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="7faa5-135">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="7faa5-136">انتقل إلى **إعدادات متقدمة \> النظام \> الأمان \> المستخدمين**، وقم بإنشاء مستخدم تطبيق.</span><span class="sxs-lookup"><span data-stu-id="7faa5-136">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="7faa5-137">استخدم القائمة عرض لتغيير طريقة عرض الصفحة إلى **مستخدمي التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-137">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="7faa5-138">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-138">Select **New**.</span></span> <span data-ttu-id="7faa5-139">عيّن معرف التطبيق إلى *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="7faa5-139">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="7faa5-140">(سيتم تحميل مُعرّف الكائن تلقائيًا عند حفظ التغييرات الخاصة بك.) يمكنك تخصيص الاسم.</span><span class="sxs-lookup"><span data-stu-id="7faa5-140">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="7faa5-141">على سبيل المثال، يمكنك تغييره إلى *رؤية المخزون*.</span><span class="sxs-lookup"><span data-stu-id="7faa5-141">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="7faa5-142">عند الانتهاء، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-142">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="7faa5-143">حدد **تعيين دور**، ثم حدد **مسؤول النظام**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-143">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="7faa5-144">إذا كان هناك دور يسمي **مستخدم Common Data Service**، فحدده أيضًا.</span><span class="sxs-lookup"><span data-stu-id="7faa5-144">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="7faa5-145">لمزيد من المعلومات، راجع [إنشاء مستخدم تطبيق](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="7faa5-145">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="7faa5-146">إذا لم تكن لغة Dataverse  الافتراضية اللغة **الإنجليزية**:</span><span class="sxs-lookup"><span data-stu-id="7faa5-146">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="7faa5-147">انتقل إلى **إعداد متقدم \> الإدارة \> اللغات**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-147">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="7faa5-148">حدد **الإنجليزية (LanguageCode=1033)** وحدد **تطبيق**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-148">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="7faa5-149">قم باستيراد الملف `Inventory Visibility Dataverse Solution.zip`، الذي يتضمن تكوين Dataverse المرتبط بالكيانات و Power Apps:</span><span class="sxs-lookup"><span data-stu-id="7faa5-149">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="7faa5-150">انتقل إلى الصفحة **حلول**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-150">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="7faa5-151">حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-151">Select **Import**.</span></span>

1. <span data-ttu-id="7faa5-152">استيراد تدفق مشغل ترقية التكوين:</span><span class="sxs-lookup"><span data-stu-id="7faa5-152">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="7faa5-153">انتقل إلى الصفحة Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="7faa5-153">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="7faa5-154">تأكد من وجود الاتصال المسمى *Dataverse (قديم)*.</span><span class="sxs-lookup"><span data-stu-id="7faa5-154">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="7faa5-155">(إذا لم يكن موجودًا، فقم بإنشاءه).</span><span class="sxs-lookup"><span data-stu-id="7faa5-155">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="7faa5-156">استيراد الملف `Inventory Visibility Configuration Trigger.zip`.</span><span class="sxs-lookup"><span data-stu-id="7faa5-156">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="7faa5-157">وبعد استيراده، سيظهر المشغل ضمن **التدفقات الخاصة بي**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-157">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="7faa5-158">قم بتهيئة المتغيرات الأربعة التالية استنادًا إلى معلومات البيئة:</span><span class="sxs-lookup"><span data-stu-id="7faa5-158">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="7faa5-159">مُعرّف مستأجر Azure</span><span class="sxs-lookup"><span data-stu-id="7faa5-159">Azure Tenant ID</span></span>
        - <span data-ttu-id="7faa5-160">معرف عميل تطبيق Azure</span><span class="sxs-lookup"><span data-stu-id="7faa5-160">Azure Application Client ID</span></span>
        - <span data-ttu-id="7faa5-161">سر عميل تطبيق Azure</span><span class="sxs-lookup"><span data-stu-id="7faa5-161">Azure Application Client Secret</span></span>
        - <span data-ttu-id="7faa5-162">نقطة نهاية رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="7faa5-162">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="7faa5-163">لمزيد من المعلومات حول هذا المتغير، راجع القسم [إعداد تكامل رؤية المخزون](#setup-inventory-visibility-integration) لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="7faa5-163">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="7faa5-164">![مشغل التكوين](media/configuration-trigger.png "مشغل التكوين")</span><span class="sxs-lookup"><span data-stu-id="7faa5-164">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="7faa5-165">حدد **تشغيل**</span><span class="sxs-lookup"><span data-stu-id="7faa5-165">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="7faa5-166">تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="7faa5-166">Install the add-in</span></span>

<span data-ttu-id="7faa5-167">لتثبيت الوظيفة الإضافية لرؤية المخزون، يجب عليك القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="7faa5-167">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="7faa5-168">سجل الدخول إلى بوابة [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="7faa5-168">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="7faa5-169">في الصفحة الرئيسية ، حدد المشروع حيث يتم نشر البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="7faa5-169">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="7faa5-170">في الصفحة المشروع ، حدد البيئة التي ترغب في تثبيت الوظيفة الإضافية بها.</span><span class="sxs-lookup"><span data-stu-id="7faa5-170">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="7faa5-171">في الصفحة البيئة، قم بالتمرير لأسفل حتى تشاهد القسم **الوظائف الإضافية الخاصة بالبيئة** في القسم **Power Platform تكامل**، حيث يمكنك العثور على اسم بيئة Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7faa5-171">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="7faa5-172">في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-172">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="7faa5-173">![صفحة البيئة في LCS](media/inventory-visibility-environment.png "صفحة البيئة في LCS")</span><span class="sxs-lookup"><span data-stu-id="7faa5-173">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="7faa5-174">حدد الرابط **تثبيت وظيفة إضافية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-174">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="7faa5-175">يتم فتح قائمه بالوظائف الإضافية المتاحة.</span><span class="sxs-lookup"><span data-stu-id="7faa5-175">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="7faa5-176">حدد **رؤية المخزون** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="7faa5-176">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="7faa5-177">ادخل قيما للحقول التالية الخاصة ببيئتك:</span><span class="sxs-lookup"><span data-stu-id="7faa5-177">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="7faa5-178">**مُعرّف تطبيق AAD (العميل)**</span><span class="sxs-lookup"><span data-stu-id="7faa5-178">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="7faa5-179">**معرف مستأجر AAD**</span><span class="sxs-lookup"><span data-stu-id="7faa5-179">**AAD tenant ID**</span></span>

    <span data-ttu-id="7faa5-180">![أضافه في صفحه الإعداد](media/inventory-visibility-setup.png "صفحه إعداد الوظيفة الإضافية")</span><span class="sxs-lookup"><span data-stu-id="7faa5-180">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="7faa5-181">الموافقة علي البنود والشروط عن طريق تحديد خانه الاختيار **البنود والشروط**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-181">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="7faa5-182">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-182">Select **Install**.</span></span> <span data-ttu-id="7faa5-183">ستظهر حاله الوظيفة الإضافية باعتبارها **قيد التثبيت**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-183">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="7faa5-184">عند الانتهاء ، قم بتحديث الصفحة لرؤية تغيير الحالة علي **مثبت**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-184">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="7faa5-185">إلغاء تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="7faa5-185">Uninstall the add-in</span></span>

<span data-ttu-id="7faa5-186">للغاء تثبيت الوظيفة الإضافية ، حدد **إلغاء التثبيت**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-186">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="7faa5-187">عندما تقوم بتحديث LCS، فإنه ستتم إزالة الوظيفة الإضافية لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-187">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="7faa5-188">تقوم عمليه إزالة التثبيت على إزالة تسجيل الوظيفة الإضافية وبدء مهمة أيضًا لتنظيف كافة بيانات الشركات المخزنة في الخدمة.</span><span class="sxs-lookup"><span data-stu-id="7faa5-188">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="7faa5-189">استخدام بيانات المخزون الفعلي من Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7faa5-189">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="7faa5-190">توزيع حزمة تكامل رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="7faa5-190">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="7faa5-191">إذا كنت تقوم بتشغيل Supply Chain Management الإصدار 10.0.17 أو إصدار سابق عنه، فتواصل بفريق دعم رؤية المخزون على [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) للحصول علي ملف الحزمة.</span><span class="sxs-lookup"><span data-stu-id="7faa5-191">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="7faa5-192">ثم قم بنشر الحزمة في LCS.</span><span class="sxs-lookup"><span data-stu-id="7faa5-192">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="7faa5-193">إذا حدث خطأ عدم تطابق في الإصدار أثناء التوزيع، يجب عليك استيراد مشروع X++ يدويًا إلى بيئة التطوير الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="7faa5-193">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="7faa5-194">ثم قم بإنشاء الحزمة القابلة للنشر في بيئة التطوير الخاصة بك، ثم قم بنشرها في بيئة الإنتاج الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="7faa5-194">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="7faa5-195">يتم تضمين الكود Supply Chain Management في الإصدار 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="7faa5-195">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="7faa5-196">إذا كنت تقوم بتشغيل هذا الإصدار أو الأحدث، فإن عملية النشر تكون غير ضرورية.</span><span class="sxs-lookup"><span data-stu-id="7faa5-196">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="7faa5-197">تأكد من أنه يتم تشغيل الميزات التالية في بيئة Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7faa5-197">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="7faa5-198">(افتراضيًا، فإنه يتم تشغيلها.)</span><span class="sxs-lookup"><span data-stu-id="7faa5-198">(By default, they are turned on.)</span></span>

| <span data-ttu-id="7faa5-199">وصف الميزة</span><span class="sxs-lookup"><span data-stu-id="7faa5-199">Feature description</span></span> | <span data-ttu-id="7faa5-200">إصدار الكود</span><span class="sxs-lookup"><span data-stu-id="7faa5-200">Code version</span></span> | <span data-ttu-id="7faa5-201">تبديل الفئة</span><span class="sxs-lookup"><span data-stu-id="7faa5-201">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="7faa5-202">تمكين أو تعطيل استخدام أبعاد المخزون في جدول InventSum</span><span class="sxs-lookup"><span data-stu-id="7faa5-202">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="7faa5-203">10.0.11</span><span class="sxs-lookup"><span data-stu-id="7faa5-203">10.0.11</span></span> | <span data-ttu-id="7faa5-204">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="7faa5-204">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="7faa5-205">تمكين أو تعطيل استخدام أبعاد المخزون في جدول InventSumDelta</span><span class="sxs-lookup"><span data-stu-id="7faa5-205">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="7faa5-206">10.0.12</span><span class="sxs-lookup"><span data-stu-id="7faa5-206">10.0.12</span></span> | <span data-ttu-id="7faa5-207">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="7faa5-207">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="7faa5-208">إعداد تكامل رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="7faa5-208">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="7faa5-209">في Supply Chain Management، افتح مساحة عمل **[إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**، وقم بتشغيل الميزة **تكامل رؤية المخزون**.</span><span class="sxs-lookup"><span data-stu-id="7faa5-209">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="7faa5-210">انتقل إلى **إدارة المخزون \> الإعداد \> معلمات تكامل رؤية المخزون**، وأدخل عنوان URL للبيئة التي تقوم فيها بتشغيل رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-210">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="7faa5-211">ابحث عن منطقة LCS الخاصة ببيئة Azure، ثم أدخل عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="7faa5-211">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="7faa5-212">يحتوي عنوان URL على النموذج التالي:</span><span class="sxs-lookup"><span data-stu-id="7faa5-212">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="7faa5-213">على سبيل المثال، إذا كنت في أوروبا، سيكون لدي البيئة واحدًا من عناوين (URL) التالية:</span><span class="sxs-lookup"><span data-stu-id="7faa5-213">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="7faa5-214">تتوفر المناطق التالية حاليًا.</span><span class="sxs-lookup"><span data-stu-id="7faa5-214">The following regions are currently available.</span></span>

    | <span data-ttu-id="7faa5-215">منطقة Azure</span><span class="sxs-lookup"><span data-stu-id="7faa5-215">Azure region</span></span> | <span data-ttu-id="7faa5-216">اسم المنطقة القصير</span><span class="sxs-lookup"><span data-stu-id="7faa5-216">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="7faa5-217">شرق أستراليا</span><span class="sxs-lookup"><span data-stu-id="7faa5-217">Australia east</span></span> | <span data-ttu-id="7faa5-218">eau</span><span class="sxs-lookup"><span data-stu-id="7faa5-218">eau</span></span> |
    | <span data-ttu-id="7faa5-219">جنوب شرق أستراليا</span><span class="sxs-lookup"><span data-stu-id="7faa5-219">Australia southeast</span></span> | <span data-ttu-id="7faa5-220">seau</span><span class="sxs-lookup"><span data-stu-id="7faa5-220">seau</span></span> |
    | <span data-ttu-id="7faa5-221">وسط كندا</span><span class="sxs-lookup"><span data-stu-id="7faa5-221">Canada central</span></span> | <span data-ttu-id="7faa5-222">cca</span><span class="sxs-lookup"><span data-stu-id="7faa5-222">cca</span></span> |
    | <span data-ttu-id="7faa5-223">شرق كندا</span><span class="sxs-lookup"><span data-stu-id="7faa5-223">Canada east</span></span> | <span data-ttu-id="7faa5-224">eca</span><span class="sxs-lookup"><span data-stu-id="7faa5-224">eca</span></span> |
    | <span data-ttu-id="7faa5-225">شمال أوروبا</span><span class="sxs-lookup"><span data-stu-id="7faa5-225">North Europe</span></span> | <span data-ttu-id="7faa5-226">neu</span><span class="sxs-lookup"><span data-stu-id="7faa5-226">neu</span></span> |
    | <span data-ttu-id="7faa5-227">غرب أوروبا</span><span class="sxs-lookup"><span data-stu-id="7faa5-227">West Europe</span></span> | <span data-ttu-id="7faa5-228">weu</span><span class="sxs-lookup"><span data-stu-id="7faa5-228">weu</span></span> |
    | <span data-ttu-id="7faa5-229">شرق الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="7faa5-229">East US</span></span> | <span data-ttu-id="7faa5-230">eus</span><span class="sxs-lookup"><span data-stu-id="7faa5-230">eus</span></span> |
    | <span data-ttu-id="7faa5-231">غرب الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="7faa5-231">West US</span></span> | <span data-ttu-id="7faa5-232">wus</span><span class="sxs-lookup"><span data-stu-id="7faa5-232">wus</span></span> |

1. <span data-ttu-id="7faa5-233">انتقل إلى **إدارة المخزون \> دوري \> تكامل رؤية المخزون**، وقم بتمكين الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="7faa5-233">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="7faa5-234">سيتم الآن ترحيل كافة أحداث تغيير المخزون من Supply Chain Management إلى رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-234">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="7faa5-235">واجهة API العامة للوظيفة الإضافية لرؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="7faa5-235">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="7faa5-236">تقدم واجهة برمجة التطبيقات العامة لـ REST الخاصة بالوظيفة الإضافية لرؤية المخزون العديد من نقاط التكامل الخاصة.</span><span class="sxs-lookup"><span data-stu-id="7faa5-236">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="7faa5-237">ويدعم ثلاثه أنواع من التفاعلات الرئيسية:</span><span class="sxs-lookup"><span data-stu-id="7faa5-237">It supports three main interaction types:</span></span>

- <span data-ttu-id="7faa5-238">ترحيل تغييرات المخزون الفعلية إلى الوظيفة الإضافية من نظام خارجي</span><span class="sxs-lookup"><span data-stu-id="7faa5-238">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="7faa5-239">الاستعلام عن الكميات الفعلية الحالية من نظام خارجي</span><span class="sxs-lookup"><span data-stu-id="7faa5-239">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="7faa5-240">مزامنة تلقائية مع مخزون Supply Chain Management الفعلي</span><span class="sxs-lookup"><span data-stu-id="7faa5-240">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="7faa5-241">لا تعتبر المزامنة التلقائية جزءًا من API العامة.</span><span class="sxs-lookup"><span data-stu-id="7faa5-241">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="7faa5-242">وبدلاً من ذلك، تتم معالجتة في الخلفية للبيئات التي تم فيها تمكين الوظيفة الإضافية لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-242">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="7faa5-243">مصادقة</span><span class="sxs-lookup"><span data-stu-id="7faa5-243">Authentication</span></span>

<span data-ttu-id="7faa5-244">يتم استخدام الرمز المميز لأمان النظام الأساسي لاستدعاء الوظيفة الإضافية لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-244">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="7faa5-245">ولذلك، يجب إنشاء رمز *Azure Active Directory (Azure AD) المميز* باستخدام تطبيق Azure AD.</span><span class="sxs-lookup"><span data-stu-id="7faa5-245">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="7faa5-246">يجب استخدام رمز Azure AD المميز للحصول على *رمز الوصول المميز* من خدمة الأمان.</span><span class="sxs-lookup"><span data-stu-id="7faa5-246">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="7faa5-247">احصل علي رمز خدمه أمان بالقيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="7faa5-247">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="7faa5-248">سجل دخولك إلى مدخل Azure واستخدمه للعثور على `clientId` و `clientSecret` لتطبيق Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7faa5-248">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="7faa5-249">إحضار Azure Active Directory رمز مميز (`aadToken`) عن طريق إرسال طلب HTTP بالخصائص التالية:</span><span class="sxs-lookup"><span data-stu-id="7faa5-249">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="7faa5-250">**عنوان URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="7faa5-250">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="7faa5-251">**الطريقة** - `GET`</span><span class="sxs-lookup"><span data-stu-id="7faa5-251">**Method** - `GET`</span></span>
    - <span data-ttu-id="7faa5-252">**محتوي النص الأساسي (بيانات النموذج)**:</span><span class="sxs-lookup"><span data-stu-id="7faa5-252">**Body content (form data)**:</span></span>

        | <span data-ttu-id="7faa5-253">المفتاح</span><span class="sxs-lookup"><span data-stu-id="7faa5-253">key</span></span> | <span data-ttu-id="7faa5-254">القيمة</span><span class="sxs-lookup"><span data-stu-id="7faa5-254">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="7faa5-255">client_id</span><span class="sxs-lookup"><span data-stu-id="7faa5-255">client_id</span></span> | <span data-ttu-id="7faa5-256">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="7faa5-256">${aadAppId}</span></span> |
        | <span data-ttu-id="7faa5-257">client_secret</span><span class="sxs-lookup"><span data-stu-id="7faa5-257">client_secret</span></span> | <span data-ttu-id="7faa5-258">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="7faa5-258">${aadAppSecret}</span></span> |
        | <span data-ttu-id="7faa5-259">grant_type</span><span class="sxs-lookup"><span data-stu-id="7faa5-259">grant_type</span></span> | <span data-ttu-id="7faa5-260">client_credentials</span><span class="sxs-lookup"><span data-stu-id="7faa5-260">client_credentials</span></span> |
        | <span data-ttu-id="7faa5-261">مورد</span><span class="sxs-lookup"><span data-stu-id="7faa5-261">resource</span></span> | <span data-ttu-id="7faa5-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="7faa5-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="7faa5-263">يجب ان تتلقي `aadToken` استجابه فيها، والتي تشبه المثال التالي.</span><span class="sxs-lookup"><span data-stu-id="7faa5-263">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="7faa5-264">المستقبل طلب JSON مشابها لما يلي:</span><span class="sxs-lookup"><span data-stu-id="7faa5-264">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="7faa5-265">المكان:</span><span class="sxs-lookup"><span data-stu-id="7faa5-265">Where:</span></span>
    - <span data-ttu-id="7faa5-266">`client_assertion`يجب ان تكون القيمة هي `aadToken` التي استلمتها في الخطوة السابقة.</span><span class="sxs-lookup"><span data-stu-id="7faa5-266">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="7faa5-267">`context`يجب ان تكون القيمة معرف البيئة حيث تريد توزيع الوظيفة الإضافية.</span><span class="sxs-lookup"><span data-stu-id="7faa5-267">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="7faa5-268">قم بتعيين كافة القيم الأخرى كما هو موضح في المثال.</span><span class="sxs-lookup"><span data-stu-id="7faa5-268">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="7faa5-269">قم بإرسال طلب HTTP بالخصائص التالية:</span><span class="sxs-lookup"><span data-stu-id="7faa5-269">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="7faa5-270">**عنوان URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="7faa5-270">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="7faa5-271">**الطريقة** - `POST`</span><span class="sxs-lookup"><span data-stu-id="7faa5-271">**Method** - `POST`</span></span>
    - <span data-ttu-id="7faa5-272">**راس HTTP** - تضمين إصدار API (`Api-Version` المفتاح هو والقيمة هو `1.0`)</span><span class="sxs-lookup"><span data-stu-id="7faa5-272">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="7faa5-273">**محتوي أساسي** - تضمين طلب JSON الذي قمت بإنشاءه في الخطوة السابقة.</span><span class="sxs-lookup"><span data-stu-id="7faa5-273">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="7faa5-274">ستحصل علي `access_token` في الاستجابة.</span><span class="sxs-lookup"><span data-stu-id="7faa5-274">You will get an `access_token` in response.</span></span> <span data-ttu-id="7faa5-275">وهذا ما تحتاجه كرمز مميز في الحامل لاستدعاء امكانيه رؤية API للمخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-275">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="7faa5-276">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="7faa5-276">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="7faa5-277">عينة طلب</span><span class="sxs-lookup"><span data-stu-id="7faa5-277">Sample Request</span></span>

<span data-ttu-id="7faa5-278">كمرجع لك، فيما يلي عينة طلب http، يمكنك استخدام أي أدوات أو لغة تعليمات برمجية لإرسال هذا الطلب، مثل ``Postman``.</span><span class="sxs-lookup"><span data-stu-id="7faa5-278">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="7faa5-279">تكوين واجهه برمجه تطبيقات امكانيه رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="7faa5-279">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="7faa5-280">قبل استخدام الخدمة ، يجب إكمال التكوينات الموضحة في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="7faa5-280">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="7faa5-281">قد يختلف التكوين استنادا إلى تفاصيل البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="7faa5-281">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="7faa5-282">وهو يتضمن بشكل أساسي أربعه أجزاء:</span><span class="sxs-lookup"><span data-stu-id="7faa5-282">It primarily includes four parts:</span></span>

- [<span data-ttu-id="7faa5-283">تقسيم</span><span class="sxs-lookup"><span data-stu-id="7faa5-283">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="7faa5-284">تكوينات الأبعاد</span><span class="sxs-lookup"><span data-stu-id="7faa5-284">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="7faa5-285">فهرسة</span><span class="sxs-lookup"><span data-stu-id="7faa5-285">Indexing</span></span>](#indexing)
- [<span data-ttu-id="7faa5-286">قياس مخصص</span><span class="sxs-lookup"><span data-stu-id="7faa5-286">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="7faa5-287">تقسيم</span><span class="sxs-lookup"><span data-stu-id="7faa5-287">Partitioning</span></span>

<span data-ttu-id="7faa5-288">يمكن للتقسيم ان يؤثر بشكل كبير علي أداء واجهة API الخاصة برؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-288">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="7faa5-289">انها لفكره جيده ان تقوم بتعريف نظام يسمح بالتجميعات الصغيرة للبيانات مع استمرار السماح باستعلامات البيانات ذات المعني.</span><span class="sxs-lookup"><span data-stu-id="7faa5-289">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="7faa5-290">سيكون `organizationId` (`dataAreaId` في Supply Chain Management) دائما جزءا من التقسيم ، ويتم تعيين رؤية المخزون بشكل افتراضي علي قسم حسب الابعاد *كموقع إلكتروني + موقع جغرافي*.</span><span class="sxs-lookup"><span data-stu-id="7faa5-290">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="7faa5-291">وهذا يعني انه يجب دوما الاستعلام عن الخدمة باستخدام هذه الابعاد المحددة في عوامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="7faa5-291">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="7faa5-292">*الموقع الإلكتروني* و *الموقع الجغرافي* هما اثنان من الابعاد الافتراضية في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-292">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="7faa5-293">في Supply Chain Management، تسمي هذه الابعاد *بالموقع الإلكتروني* (`InventSiteId`) *والمستودع* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="7faa5-293">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="7faa5-294">تكوينات الأبعاد</span><span class="sxs-lookup"><span data-stu-id="7faa5-294">Dimension configurations</span></span>

<span data-ttu-id="7faa5-295">ستوفر امكانيه رؤية المخزون قائمه بالابعاد الافتراضية العامة لتمكين تكامل النظام المصدر المتعدد.</span><span class="sxs-lookup"><span data-stu-id="7faa5-295">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="7faa5-296">يسرد الجدول التالي ابعاد المخزون التي ستكون أسماء الابعاد الافتراضية في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-296">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="7faa5-297">نوع البعد</span><span class="sxs-lookup"><span data-stu-id="7faa5-297">Dimension type</span></span> | <span data-ttu-id="7faa5-298">اسم البُعد</span><span class="sxs-lookup"><span data-stu-id="7faa5-298">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="7faa5-299">منتج</span><span class="sxs-lookup"><span data-stu-id="7faa5-299">Product</span></span> | `ColorId` |
| <span data-ttu-id="7faa5-300">منتج</span><span class="sxs-lookup"><span data-stu-id="7faa5-300">Product</span></span> | `SizeId` |
| <span data-ttu-id="7faa5-301">منتج</span><span class="sxs-lookup"><span data-stu-id="7faa5-301">Product</span></span> | `StyleId` |
| <span data-ttu-id="7faa5-302">منتج</span><span class="sxs-lookup"><span data-stu-id="7faa5-302">Product</span></span> | `ConfigId` |
| <span data-ttu-id="7faa5-303">التعقب</span><span class="sxs-lookup"><span data-stu-id="7faa5-303">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="7faa5-304">التعقب</span><span class="sxs-lookup"><span data-stu-id="7faa5-304">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="7faa5-305"> الموق</span><span class="sxs-lookup"><span data-stu-id="7faa5-305">Location</span></span> | `LocationId` |
| <span data-ttu-id="7faa5-306"> الموق</span><span class="sxs-lookup"><span data-stu-id="7faa5-306">Location</span></span> | `SiteId` |
| <span data-ttu-id="7faa5-307">حالة المخزون</span><span class="sxs-lookup"><span data-stu-id="7faa5-307">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="7faa5-308">خاص بالمستودع</span><span class="sxs-lookup"><span data-stu-id="7faa5-308">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="7faa5-309">خاص بالمستودع</span><span class="sxs-lookup"><span data-stu-id="7faa5-309">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="7faa5-310">خاص بالمستودع</span><span class="sxs-lookup"><span data-stu-id="7faa5-310">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="7faa5-311">يكون نوع البعد المدرج في الجدول السابق كمرجع فقط.</span><span class="sxs-lookup"><span data-stu-id="7faa5-311">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="7faa5-312">لا يلزم تحديد نوع البعد في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-312">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="7faa5-313">في حاله وجود بعد مخصص والحاجة إلى التدفق للقيمة الافتراضية عند استهلاك رؤية المخزون ، يمكنك تكوين **اسم البعد المخصص** في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-313">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="7faa5-314">وصول الانظمه الخارجية إلى رؤية المخزون من خلال واجات برمجه التطبيقات RESTful التي تتيح معلومات الكمية الفعلية حول مجموعات الابعاد المحددة التي سيتم الاستعلام عنها.</span><span class="sxs-lookup"><span data-stu-id="7faa5-314">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="7faa5-315">بالنسبة للتكامل ، يمكنك رؤية المخزون من تكوين *مصدر بيانات القناة الخارجية* وبعد المصدر علي *الابعاد المستهدفة* في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-315">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="7faa5-316">يجب ان تكون الابعاد المستهدفة واحده مما يلي:</span><span class="sxs-lookup"><span data-stu-id="7faa5-316">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="7faa5-317">الابعاد الافتراضية في رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="7faa5-317">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="7faa5-318">الأبعاد المخصصة</span><span class="sxs-lookup"><span data-stu-id="7faa5-318">Custom dimensions</span></span>

<span data-ttu-id="7faa5-319">والغرض من تكوين الابعاد هو توحيد التكامل المتعدد الانظمه للاستعلام علي الابعاد وحدث الترحيل مع الابعاد.</span><span class="sxs-lookup"><span data-stu-id="7faa5-319">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="7faa5-320">فهرسة</span><span class="sxs-lookup"><span data-stu-id="7faa5-320">Indexing</span></span>

<span data-ttu-id="7faa5-321">في معظم الأوقات ، لن يكون الاستعلام الفعلي الخاص بالمخزون علي مستوي "الإجمالي" الأعلى فقط ، ولكن قد ترغب في رؤية النتائج المجمعة استنادا إلى ابعاد المخزون.</span><span class="sxs-lookup"><span data-stu-id="7faa5-321">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="7faa5-322">توفر امكانيه رؤية المخزون المرونة عن طريق السماح لك بإعداد الفهارس ، التي تعتمد علي البعد أو مجموعه الابعاد.</span><span class="sxs-lookup"><span data-stu-id="7faa5-322">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="7faa5-323">حاليا ، يمكنك فقط تكوين الفهارس بخمسه كحد اقصي.</span><span class="sxs-lookup"><span data-stu-id="7faa5-323">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="7faa5-324">يجب مراعاه البعد أو مجموعه الابعاد التي ستستخدمها قبل التنفيذ للتاكد من انها ستفي باحتياجات أعمالك.</span><span class="sxs-lookup"><span data-stu-id="7faa5-324">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="7faa5-325">علي سبيل المثال ، إذا كنت ترغب في الاستعلام عن المنتجات كالتالي:</span><span class="sxs-lookup"><span data-stu-id="7faa5-325">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="7faa5-326">الاستعلام عن المنتج المجمع الفعلي بواسطة ابعاد *اللون* و *الحجم*.</span><span class="sxs-lookup"><span data-stu-id="7faa5-326">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="7faa5-327">في بعض الحالات ، تريد فقط الاستعلام عن المنتج إجمالا.</span><span class="sxs-lookup"><span data-stu-id="7faa5-327">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="7faa5-328">سيكون لديك فهرسين محددين كالتالي:</span><span class="sxs-lookup"><span data-stu-id="7faa5-328">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="7faa5-329">سيتم تجميع القوس الفارغ استنادا إلى "معرف المنتج" داخل القسم.</span><span class="sxs-lookup"><span data-stu-id="7faa5-329">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="7faa5-330">تحدد الفهرسة كيفيه تجميع النتائج استنادا إلى إعداد الاستعلام `groupBy`.</span><span class="sxs-lookup"><span data-stu-id="7faa5-330">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="7faa5-331">في هذه الحالة إذا لم تقم بتحديد أي قيم `groupBy`، سيتم الحصول علي الإجماليات بواسطة `productid`.</span><span class="sxs-lookup"><span data-stu-id="7faa5-331">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="7faa5-332">وإلا، إذا قمت بتحديد `groupBy` كـ `groupBy=ColorId&groupBy=SizeId`، ستحصل على بنود متعددة يتم إرجاعها، استنادًا إلى مجموعتي اللون والحجم المختلفتين في النظام.</span><span class="sxs-lookup"><span data-stu-id="7faa5-332">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="7faa5-333">يمكنك وضع معايير الاستعلام في النص الأساسي للطلب.</span><span class="sxs-lookup"><span data-stu-id="7faa5-333">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="7faa5-334">فيما يلي نموذج استعلام حول المنتج بمجموعه اللون والحجم.</span><span class="sxs-lookup"><span data-stu-id="7faa5-334">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
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

<span data-ttu-id="7faa5-335">فيما يتعلق بالحقل `filters`، وحده `ProductId` يدعم القيم المتعددة.</span><span class="sxs-lookup"><span data-stu-id="7faa5-335">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="7faa5-336">إذا كان `ProductId`مصفوفة فارغة، فسيتم الاستعلام عن كافة المنتجات.</span><span class="sxs-lookup"><span data-stu-id="7faa5-336">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="7faa5-337">قياس مخصص</span><span class="sxs-lookup"><span data-stu-id="7faa5-337">Custom measurement</span></span>

<span data-ttu-id="7faa5-338">يتم ربط كميات القياس الافتراضية بـ Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7faa5-338">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="7faa5-339">ومع ذلك، قد ترغب في الحصول على كمية تتكون من مجموعة من القياسات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="7faa5-339">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="7faa5-340">وللقيام بذلك ، يمكن ان يكون لديك تكوين كميات مخصصه ، والتي ستتم اضافتها إلى إخراج الاستعلامات الفعلية.</span><span class="sxs-lookup"><span data-stu-id="7faa5-340">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="7faa5-341">وتتيح الوظيفة ببساطه تحديد مجموعه من القياسات التي ستتم اضافتها ، و/أو مجموعه من المقاييس التي سيتم طرحها ، من أجل القياس المخصص.</span><span class="sxs-lookup"><span data-stu-id="7faa5-341">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="7faa5-342">علي سبيل المثال ، باستخدام شرط الاستعلام التالي ، ستقوم بتكوين كميه القياس المخصصة باعتبارها `MyCustomAvailableforReservation` ليتم استهلاكها من قبل نظام الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="7faa5-342">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="7faa5-343">نظام الاستهلاك</span><span class="sxs-lookup"><span data-stu-id="7faa5-343">Consumption system</span></span> | <span data-ttu-id="7faa5-344">القياسات المحتسبة</span><span class="sxs-lookup"><span data-stu-id="7faa5-344">Calculated measurers</span></span> | <span data-ttu-id="7faa5-345">مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="7faa5-345">Data source</span></span> | <span data-ttu-id="7faa5-346">أداه التعديل</span><span class="sxs-lookup"><span data-stu-id="7faa5-346">Modifier</span></span> | <span data-ttu-id="7faa5-347">نوع حساب أداة التعديل</span><span class="sxs-lookup"><span data-stu-id="7faa5-347">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="7faa5-348">الجمع</span><span class="sxs-lookup"><span data-stu-id="7faa5-348">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="7faa5-349">الجمع</span><span class="sxs-lookup"><span data-stu-id="7faa5-349">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="7faa5-350">الطرح</span><span class="sxs-lookup"><span data-stu-id="7faa5-350">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="7faa5-351">الجمع</span><span class="sxs-lookup"><span data-stu-id="7faa5-351">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="7faa5-352">الطرح</span><span class="sxs-lookup"><span data-stu-id="7faa5-352">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="7faa5-353">الجمع</span><span class="sxs-lookup"><span data-stu-id="7faa5-353">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="7faa5-354">الجمع</span><span class="sxs-lookup"><span data-stu-id="7faa5-354">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="7faa5-355">الطرح</span><span class="sxs-lookup"><span data-stu-id="7faa5-355">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="7faa5-356">الطرح</span><span class="sxs-lookup"><span data-stu-id="7faa5-356">Subtraction</span></span> |

<span data-ttu-id="7faa5-357">ومع ذلك ، سيقوم الاستعلام الموجود علي كميه القياس المخصصة بإرجاع المخرجات التالية.</span><span class="sxs-lookup"><span data-stu-id="7faa5-357">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="7faa5-358">يعتمد إخراج `MyCustomAvailableforReservation`علي إعداد الحساب في القياسات المخصصة كما يلي:</span><span class="sxs-lookup"><span data-stu-id="7faa5-358">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="7faa5-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="7faa5-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="7faa5-360">ترحيل التغييرات الفعلية</span><span class="sxs-lookup"><span data-stu-id="7faa5-360">Posting on-hand changes</span></span>

<span data-ttu-id="7faa5-361">ويعتمد عنوان URL الذي يتم ترحيل الحدث عليه علي المنطقة الجغرافية بالبالضبط.</span><span class="sxs-lookup"><span data-stu-id="7faa5-361">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="7faa5-362">سياخذ النموذج ما يلي:</span><span class="sxs-lookup"><span data-stu-id="7faa5-362">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="7faa5-363">عند المصادقة ، يمكن استخدام محدد موقع المعلومات (URL) هذا مع أسلوب `POST` HTTP لإرسال احداث التغيير الفعلي إلى الخدمة.</span><span class="sxs-lookup"><span data-stu-id="7faa5-363">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="7faa5-364">يتم استخدام الراس الخاص للاتصال مع خدمات Dynamics 365 من خلال طلبات HTTP ، والذي يشير إلى معرف البيئة لمثيل Supply Chain Management الذي ترتبط به البيانات.</span><span class="sxs-lookup"><span data-stu-id="7faa5-364">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="7faa5-365">على سبيل المثال:</span><span class="sxs-lookup"><span data-stu-id="7faa5-365">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="7faa5-366">ترحيل التغييرات الفعلية مثال الاستعلام 1</span><span class="sxs-lookup"><span data-stu-id="7faa5-366">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="7faa5-367">يوضح هذا المثال السيناريو الذي ستقوم فيه بإعداد تكوين البعد في Power Apps.</span><span class="sxs-lookup"><span data-stu-id="7faa5-367">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="7faa5-368">استخدم الاستعلام التالي لتكوين تعيين البعد في Power Apps:</span><span class="sxs-lookup"><span data-stu-id="7faa5-368">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="7faa5-369">يمكنك الآن تحديد `dimensionDataSource` واستخدام الابعاد المخصصة في الاستعلامات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="7faa5-369">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="7faa5-370">سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="7faa5-370">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="7faa5-371">ترحيل التغييرات الفعلية مثال الاستعلام 2</span><span class="sxs-lookup"><span data-stu-id="7faa5-371">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="7faa5-372">يوضح هذا المثال السيناريو الذي لا يتم فيه إعداد تعيينات لتكوين البعد في Power Apps، التالي يجب ان تستخدم الترحيل أيضا الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="7faa5-372">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="7faa5-373">يجب ان تكون كافة الابعاد بابعاد أساسيه عندما يكون الحقل `dimensionDataSource` خاليا أو فارغا أو مسافة بيضاء.</span><span class="sxs-lookup"><span data-stu-id="7faa5-373">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="7faa5-374">خصائص حقل مستند JSON</span><span class="sxs-lookup"><span data-stu-id="7faa5-374">JSON document field properties</span></span>

<span data-ttu-id="7faa5-375">تتضمن الحقول الموجودة في أمثله استعلام JSON المتوفرة في السابق الخصائص المسرودة في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="7faa5-375">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="7faa5-376">معرف الحقل</span><span class="sxs-lookup"><span data-stu-id="7faa5-376">Field ID</span></span> | <span data-ttu-id="7faa5-377">الوصف</span><span class="sxs-lookup"><span data-stu-id="7faa5-377">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="7faa5-378">معرف فريد لحدث التغيير المحدد.</span><span class="sxs-lookup"><span data-stu-id="7faa5-378">A unique ID for the specific change event.</span></span> <span data-ttu-id="7faa5-379">يتم استخدام هذا المعرف للتاكد من فشل الاتصال بالخدمة اثناء الترحيل ، ولن يؤدي أعاده إرسال الحدث إلى نفس الحدث الذي يتم حسابه مرتين في النظام.</span><span class="sxs-lookup"><span data-stu-id="7faa5-379">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="7faa5-380">معرف المؤسسة المرتبط بالحدث.</span><span class="sxs-lookup"><span data-stu-id="7faa5-380">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="7faa5-381">وهذا ما يعين لمؤسسات Supply Chain Management أو معرفات مناطق البيانات.</span><span class="sxs-lookup"><span data-stu-id="7faa5-381">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="7faa5-382">معرف أمر الإنتاج المحدد.</span><span class="sxs-lookup"><span data-stu-id="7faa5-382">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="7faa5-383">الكمية التي يجب تغيير الكمية الحالية وفقا لها.</span><span class="sxs-lookup"><span data-stu-id="7faa5-383">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="7faa5-384">علي سبيل المثال ، تمت أضافه 10 قطع من خبز البيغلز جديده إلى الرف، ستكون هذه القيمة 10.</span><span class="sxs-lookup"><span data-stu-id="7faa5-384">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="7faa5-385">إذا تمت أزاله 3 قطع من خبز البيغلز من الرف أو بيعه ، ستكون هذه القيمة -3.</span><span class="sxs-lookup"><span data-stu-id="7faa5-385">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="7faa5-386">مصدر البيانات الخاص بالابعاد المستخدمة في حدث تغيير الترحيل والاستعلام.</span><span class="sxs-lookup"><span data-stu-id="7faa5-386">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="7faa5-387">إذا قمت بتحديد مصدر البيانات ، يمكنك استخدام الابعاد المخصصة من مصدر البيانات المحدد.</span><span class="sxs-lookup"><span data-stu-id="7faa5-387">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="7faa5-388">باستخدام تكوين البعد ، يمكن ان يقوم ظهور المخزون بتعيين الابعاد المخصصة إلى الابعاد الافتراضية العامة.</span><span class="sxs-lookup"><span data-stu-id="7faa5-388">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="7faa5-389">في حاله عدم تحديد `dimensionDataSource`، يمكنك استخدام الابعاد الافتراضية العامة فقط في الاستعلامات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="7faa5-389">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="7faa5-390">كيس مجموعه حيوية من أزواج مفتاح/قيمه.</span><span class="sxs-lookup"><span data-stu-id="7faa5-390">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="7faa5-391">سيتم تعيينها لبعض الابعاد في Supply Chain Management، ولكن يمكنك أيضا أضافه ابعاد مخصصه (مثل *المصدر*) والتي قد تشير إلى ما إذا كان الحدث واردا من Supply Chain Management أو من النظام الخارجي.</span><span class="sxs-lookup"><span data-stu-id="7faa5-391">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="7faa5-392">الاستعلام عن الكمية الحالية</span><span class="sxs-lookup"><span data-stu-id="7faa5-392">Querying current on-hand</span></span>

<span data-ttu-id="7faa5-393">سيكون للنقطة النهائية للاستعلام عن الكمية الحالية عنوان URL مشابه:</span><span class="sxs-lookup"><span data-stu-id="7faa5-393">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="7faa5-394">سيتم الاستعلام عنها باستخدام أسلوب `POST` HTTP.</span><span class="sxs-lookup"><span data-stu-id="7faa5-394">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="7faa5-395">مثال علي الاستعلام الفعلي حاليا 1</span><span class="sxs-lookup"><span data-stu-id="7faa5-395">Current on-hand query example 1</span></span>

<span data-ttu-id="7faa5-396">يوضح هذا المثال السيناريو الذي ستقوم فيه بإعداد تكوين البعد في Power Apps.</span><span class="sxs-lookup"><span data-stu-id="7faa5-396">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="7faa5-397">استخدم الاستعلام التالي لتكوين تعيين البعد في Power Apps:</span><span class="sxs-lookup"><span data-stu-id="7faa5-397">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="7faa5-398">يمكنك الآن تحديد `dimensionDataSource` واستخدام الابعاد المخصصة في الاستعلامات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="7faa5-398">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="7faa5-399">سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="7faa5-399">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="7faa5-400">يمكنك تحديد `DimensionDataSource` في `filters` وتحديد ابعاد مخصصه في كل من `filters` و`groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="7faa5-400">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="7faa5-401">سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="7faa5-401">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="7faa5-402">مثال علي الاستعلام الفعلي حاليا 2</span><span class="sxs-lookup"><span data-stu-id="7faa5-402">Current on-hand query example 2</span></span>

<span data-ttu-id="7faa5-403">يوضح هذا المثال السيناريو الذي لا يتم فيه إعداد تعيينات لتكوين البعد في Power Apps، التالي يجب ان تستخدم الترحيل أيضا الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="7faa5-403">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="7faa5-404">يجب ان تكون كافة الابعاد بابعاد أساسيه عندما يكون الحقل `dimensionDataSource`، ضمن `filters` خاليا أو فارغا أو مسافة بيضاء.</span><span class="sxs-lookup"><span data-stu-id="7faa5-404">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="7faa5-405">مثال نتيجة الإرجاع</span><span class="sxs-lookup"><span data-stu-id="7faa5-405">Example return result</span></span>

<span data-ttu-id="7faa5-406">قد تؤدي الاستعلامات المعروضة في الامثله السابقة إلى إرجاع نتيجة مثل هذه.</span><span class="sxs-lookup"><span data-stu-id="7faa5-406">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="7faa5-407">لاحظ انه يتم بناء حقول الكميات كقاموس للمقاييس والقيم المقترنة بها.</span><span class="sxs-lookup"><span data-stu-id="7faa5-407">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]