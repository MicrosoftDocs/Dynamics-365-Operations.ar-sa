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
ms.openlocfilehash: 84f5e949f0c81f840c8a9086d05bbcfc576e42aa
ms.sourcegitcommit: b67665ed689c55df1a67d1a7840947c3977d600c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6016996"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="13466-103">الوظيفة الإضافية لرؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="13466-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="13466-104">تعد الوظيفة الإضافية لرؤية المخزون بمثابه خدمة صغيرة مستقله وقابله للتغيير بشكل كبير والتي تمكن تتبع المخزون الفعلي في الوقت الحقيقي ، مما يوفر عرضا شاملا لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="13466-105">يتم تصدير كافة المعلومات المرتبطة بالمخزون الفعلي إلى الخدمة بالقرب من الوقت الحقيقي خلال تكامل SQL في المستوي المنخفض.</span><span class="sxs-lookup"><span data-stu-id="13466-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="13466-106">تقوم الانظمه الخارجية بالوصول إلى الخدمة من خلال واجهات RESTful API للاستعلام عن المعلومات الفعلية حول المجموعات المحددة من الابعاد ، ومن ثم استرداد قائمه بالمناصب الفعلية المتاحة.</span><span class="sxs-lookup"><span data-stu-id="13466-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="13466-107">رؤية المخزون عبارة عن خدمة صغيرة مضمنة في Microsoft Dataverse، مما يعني انه يمكنك توسيعها بواسطة إنشاء Power Apps وتطبيق Power BI لتوفير وظيفة مخصصه لتلبيه متطلبات الاعمال الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="13466-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="13466-108">من الممكن أيضا ترقيه الفهرس للقيام باستعلامات المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="13466-109">توفر امكانيه رؤية المخزون خيارات التكوين التي تتيح له التكامل مع أنظمه متعددة الجهات الخارجية.</span><span class="sxs-lookup"><span data-stu-id="13466-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="13466-110">وهو يدعم بعد المخزون القياسي والقابلية للتوسعة المخصصة والكميات التي تم حسابها والقياسية القابلة للتكوين.</span><span class="sxs-lookup"><span data-stu-id="13466-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="13466-111">يصف هذا الموضوع كيفيه تثبيت وتكوين الوظيفة الإضافية لرؤية المخزون لـ Dynamics 365 Supply Chain Management، وكيفيه استخدام واجهه برمجه التطبيقات (API) الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="13466-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="13466-112">تثبيت الوظيفة الإضافية لرؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="13466-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="13466-113">يجب تثبيت الوظيفة الإضافية لرؤية المخزون باستخدام Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="13466-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="13466-114">LCS عبارة عن مدخل تعاون يوفر بيئة ومجموعه من الخدمات المحدثة بشكل منتظم والتي تساعدك علي أداره دوره حياه التطبيقات الخاصة بتطبيقات Dynamics 365 Finance and Operations الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="13466-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="13466-115">للحصول على مزيد من المعلومات، راجع [موارد Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="13466-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="inventory-visibility-add-in-prerequisites"></a><span data-ttu-id="13466-116">المتطلبات الأساسية للوظيفة الإضافية لرؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="13466-116">Inventory Visibility Add-in prerequisites</span></span>

<span data-ttu-id="13466-117">قبل أن تتمكن من تثبيت الوظيفة الإضافية لرؤية المخزون، يجب عليك القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="13466-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="13466-118">احصل علي مشروع تنفيذ LCS مع نشر بيئة واحده علي الأقل.</span><span class="sxs-lookup"><span data-stu-id="13466-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="13466-119">تأكد من اكتمال المتطلبات الأساسية لإعداد الوظائف الإضافية المتوفرة في [نظرة عامة على الوظائف الإضافية](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="13466-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="13466-120">لا تتطلب رؤية المخزون ارتباطًا ثنائي الكتابة.</span><span class="sxs-lookup"><span data-stu-id="13466-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="13466-121">تواصل مع فريق رؤية المخزون على [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) للحصول على الملفات الثلاثة المطلوبة التالية:</span><span class="sxs-lookup"><span data-stu-id="13466-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - <span data-ttu-id="13466-122">`Inventory Visibility Integration.zip` (إذا كان إصدار Supply Chain Management الذي تقوم بتشغيله أقدم من الإصدار 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="13466-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="13466-123">بدلاً من ذلك، تواصل مع فريق رؤية المخزون على [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) للحصول على حزم package deployer.</span><span class="sxs-lookup"><span data-stu-id="13466-123">Alternatively, contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package deployer packages.</span></span> <span data-ttu-id="13466-124">يمكن استخدام هذه الحزم بواسطة أداة package deployer الرسمية.</span><span class="sxs-lookup"><span data-stu-id="13466-124">These packages can be used by an official package deployer tool.</span></span>
  - `InventoryServiceBase.PackageDeployer.zip`
  - <span data-ttu-id="13466-125">`InventoryServiceApplication.PackageDeployer.zip` (تحتوي هذه الحزمة علي كافة التغييرات في حزم  `InventoryServiceBase`، بالإضافة إلى مكونات إضافية لتطبيق واجهة المستخدم)</span><span class="sxs-lookup"><span data-stu-id="13466-125">`InventoryServiceApplication.PackageDeployer.zip` (this package contains all of the changes in the `InventoryServiceBase` package, plus additional UI application components)</span></span>
- <span data-ttu-id="13466-126">اتبع الإرشادات المذكورة في [تشغيل سريع: تسجيل تطبيق مع النظام الأساسي للهوية في Microsoft](/azure/active-directory/develop/quickstart-register-app) لتسجيل تطبيق وإضافة سر العميل ضمن اشتراكك في Azure.</span><span class="sxs-lookup"><span data-stu-id="13466-126">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
  - [<span data-ttu-id="13466-127">تسجيل تطبيق</span><span class="sxs-lookup"><span data-stu-id="13466-127">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
  - [<span data-ttu-id="13466-128">إضافة سر عميل</span><span class="sxs-lookup"><span data-stu-id="13466-128">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - <span data-ttu-id="13466-129">سيتم استخدام **معرف التطبيق (العميل)** و **سر العميل** و **معرف المستأجر** في الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="13466-129">The **Application(Client) Id**, **Client Secret**, and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="13466-130">تتضمن البلدان والمناطق المدعومة حاليًا كندا والولايات المتحدة والاتحاد الأوروبي (EU).</span><span class="sxs-lookup"><span data-stu-id="13466-130">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="13466-131">إذا كانت لديك إيه اسئله حول هذه المتطلبات الاساسيه ، الرجاء الاتصال بفريق رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-131">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="13466-132">إعداد Dataverse</span><span class="sxs-lookup"><span data-stu-id="13466-132">Set up Dataverse</span></span>

<span data-ttu-id="13466-133">لإعداد Dataverse للاستخدام مع رؤية المخزون، يجب أولاً إعداد المتطلبات الأساسية ثم تحديد ما إذا كان سيتم إعداد Dataverse باستخدام إما أداة package deployer أو عن طريق استيراد الحلول يدويًا (ليس من الضروري القيام بكلاهما).</span><span class="sxs-lookup"><span data-stu-id="13466-133">To set up Dataverse for use with Inventory Visibility, you must first prepare the prerequisites and then decide whether to set up Dataverse using either the package deployer tool or by manually importing the solutions (you don't have to do both).</span></span> <span data-ttu-id="13466-134">ثم قم بتثبيت الوظيفة الإضافية لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-134">Then install the Inventory Visibility Add-in.</span></span> <span data-ttu-id="13466-135">تصف الأقسام الفرعية التالية كيفية إكمال كل مهمة من هذه المهام.</span><span class="sxs-lookup"><span data-stu-id="13466-135">The following subsections describe how to complete each of these tasks.</span></span>

#### <a name="prepare-dataverse-prerequisites"></a><span data-ttu-id="13466-136">تحضير المتطلبات Dataverse الأساسية</span><span class="sxs-lookup"><span data-stu-id="13466-136">Prepare Dataverse prerequisites</span></span>

<span data-ttu-id="13466-137">قبل البدء في إعداد Dataverse، قم بإضافة مبدأ الخدمة للمستأجر الخاص بك عن طريق القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="13466-137">Before you start to set up Dataverse, add a service principle to your tenant by doing the following:</span></span>

1. <span data-ttu-id="13466-138">قم بتثبيت Azure AD الوحدة النمطية PowerShell الإصدار 2 كما هو موضح في [تثبيت Azure Active Directory PowerShell للرسم البياني](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="13466-138">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>

1. <span data-ttu-id="13466-139">قم بتشغيل الأمر PowerShell التالي:</span><span class="sxs-lookup"><span data-stu-id="13466-139">Run the following PowerShell command:</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a><span data-ttu-id="13466-140">إعداد Dataverse باستخدام الأداة package deployer</span><span class="sxs-lookup"><span data-stu-id="13466-140">Set up Dataverse using the package deployer tool</span></span>

<span data-ttu-id="13466-141">بعد الحصول على المتطلبات الأساسية، استخدم الإجراء التالي إذا كنت تفضل إعداد Dataverse باستخدام أداة package deployer.</span><span class="sxs-lookup"><span data-stu-id="13466-141">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse using the package deployer tool.</span></span> <span data-ttu-id="13466-142">راجع القسم التالي للحصول على تفاصيل حول كيفية استيراد الحلول يدويًا بدلاً من ذلك (عدم القيام بكلاهما).</span><span class="sxs-lookup"><span data-stu-id="13466-142">See the next section for details about how to import the solutions manually instead (don't do both).</span></span>

1. <span data-ttu-id="13466-143">قم بتثبيت أدوات المطور كما هو موضح في [أدوات التنزيل من NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).</span><span class="sxs-lookup"><span data-stu-id="13466-143">Install developer tools as described in [Download tools from NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).</span></span>

1. <span data-ttu-id="13466-144">وبناءً على متطلبات الأعمال، اختر الحزمة `InventoryServiceBase` أو `InventoryServiceApplication`.</span><span class="sxs-lookup"><span data-stu-id="13466-144">Based on your business requirements, choose the `InventoryServiceBase` or `InventoryServiceApplication` package.</span></span>

1. <span data-ttu-id="13466-145">استيراد الحلول:</span><span class="sxs-lookup"><span data-stu-id="13466-145">Import the solutions:</span></span>
    1. <span data-ttu-id="13466-146">للحزمة `InventoryServiceBase`:</span><span class="sxs-lookup"><span data-stu-id="13466-146">For the `InventoryServiceBase` package:</span></span>
        - <span data-ttu-id="13466-147">إلغاء الضغط `InventoryServiceBase.PackageDeployer.zip`</span><span class="sxs-lookup"><span data-stu-id="13466-147">Unzip `InventoryServiceBase.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="13466-148">البحث عن المجلد `InventoryServiceBase` والملف `[Content_Types].xml` والملف `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll` والملف `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` والملف `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`.</span><span class="sxs-lookup"><span data-stu-id="13466-148">Find folder `InventoryServiceBase`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`.</span></span> 
        - <span data-ttu-id="13466-149">قم بنسخ كل من هذه المجلدات والملفات إلى الدليل `.\Tools\PackageDeployment`، والذي تم إنشاؤه عند تثبيت أدوات المطور.</span><span class="sxs-lookup"><span data-stu-id="13466-149">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="13466-150">للحزمة `InventoryServiceApplication`:</span><span class="sxs-lookup"><span data-stu-id="13466-150">For the `InventoryServiceApplication` package:</span></span>
        - <span data-ttu-id="13466-151">إلغاء الضغط `InventoryServiceApplication.PackageDeployer.zip`</span><span class="sxs-lookup"><span data-stu-id="13466-151">Unzip `InventoryServiceApplication.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="13466-152">البحث عن المجلد `InventoryServiceApplication` والملف `[Content_Types].xml` والملف `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll` والملف `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` والملف `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.</span><span class="sxs-lookup"><span data-stu-id="13466-152">Find folder `InventoryServiceApplication`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.</span></span>
        - <span data-ttu-id="13466-153">قم بنسخ كل من هذه المجلدات والملفات إلى الدليل `.\Tools\PackageDeployment`، والذي تم إنشاؤه عند تثبيت أدوات المطور.</span><span class="sxs-lookup"><span data-stu-id="13466-153">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="13466-154">قم بتنفيذ `.\Tools\PackageDeployment\PackageDeployer.exe`.</span><span class="sxs-lookup"><span data-stu-id="13466-154">Execute `.\Tools\PackageDeployment\PackageDeployer.exe`.</span></span> <span data-ttu-id="13466-155">اتبع الإرشادات التي تظهر على الشاشة لاستيراد الحلول.</span><span class="sxs-lookup"><span data-stu-id="13466-155">Follow the instructions on your screen to import the solutions.</span></span>

1. <span data-ttu-id="13466-156">قم بتعيين أدوار أمان لمستخدم التطبيق.</span><span class="sxs-lookup"><span data-stu-id="13466-156">Assign security roles to the application user.</span></span>
    1. <span data-ttu-id="13466-157">افتح عنوان URL الخاص ببيئة Dataverse الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="13466-157">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="13466-158">انتقل إلى **إعدادات متقدمة \> النظام \> الأمان \> المستخدمين**، والبحث عن مستخدم باسم **# InventoryVisibility**.</span><span class="sxs-lookup"><span data-stu-id="13466-158">Go to **Advanced Setting \> System \> Security \> Users**, and find user the named **# InventoryVisibility**.</span></span>
    1. <span data-ttu-id="13466-159">حدد **تعيين دور**، ثم حدد **مسؤول النظام**.</span><span class="sxs-lookup"><span data-stu-id="13466-159">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="13466-160">إذا كان هناك دور يسمي **مستخدم Common Data Service**، فحدده أيضًا.</span><span class="sxs-lookup"><span data-stu-id="13466-160">If there is a role that is named **Common Data Service User**, select it as well.</span></span>

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a><span data-ttu-id="13466-161">إعداد Dataverse يدويًا عن طريق استيراد الحلول</span><span class="sxs-lookup"><span data-stu-id="13466-161">Set up Dataverse manually by importing solutions</span></span>

<span data-ttu-id="13466-162">بعد الحصول على المتطلبات الأساسية، استخدم الإجراء التالي إذا كنت تفضل إعداد Dataverse عن طريق استيراد الحلول يدويًا.</span><span class="sxs-lookup"><span data-stu-id="13466-162">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse by manually importing solutions.</span></span> <span data-ttu-id="13466-163">راجع القسم السابق للحصول على تفاصيل حول كيفية استخدام أداة package deployer بدلاً من (لا تقم بكلاهما).</span><span class="sxs-lookup"><span data-stu-id="13466-163">See the previous section for details about how to use the package deployer tool instead (don't do both).</span></span>

1. <span data-ttu-id="13466-164">إنشاء مستخدم تطبيق لرؤية المخزون في Dataverse:</span><span class="sxs-lookup"><span data-stu-id="13466-164">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="13466-165">افتح عنوان URL الخاص ببيئة Dataverse الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="13466-165">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="13466-166">انتقل إلى **إعدادات متقدمة \> النظام \> الأمان \> المستخدمين**، وقم بإنشاء مستخدم تطبيق.</span><span class="sxs-lookup"><span data-stu-id="13466-166">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="13466-167">استخدم القائمة عرض لتغيير طريقة عرض الصفحة إلى **مستخدمي التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="13466-167">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="13466-168">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="13466-168">Select **New**.</span></span> <span data-ttu-id="13466-169">عيّن معرف التطبيق إلى *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="13466-169">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="13466-170">(سيتم تحميل مُعرّف الكائن تلقائيًا عند حفظ التغييرات الخاصة بك.) يمكنك تخصيص الاسم.</span><span class="sxs-lookup"><span data-stu-id="13466-170">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="13466-171">على سبيل المثال، يمكنك تغييره إلى *رؤية المخزون*.</span><span class="sxs-lookup"><span data-stu-id="13466-171">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="13466-172">عند الانتهاء، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="13466-172">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="13466-173">حدد **تعيين دور**، ثم حدد **مسؤول النظام**.</span><span class="sxs-lookup"><span data-stu-id="13466-173">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="13466-174">إذا كان هناك دور يسمي **مستخدم Common Data Service**، فحدده أيضًا.</span><span class="sxs-lookup"><span data-stu-id="13466-174">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="13466-175">لمزيد من المعلومات، راجع [إنشاء مستخدم تطبيق](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="13466-175">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="13466-176">إذا لم تكن لغة Dataverse  الافتراضية اللغة **الإنجليزية**:</span><span class="sxs-lookup"><span data-stu-id="13466-176">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="13466-177">انتقل إلى **إعداد متقدم \> الإدارة \> اللغات**.</span><span class="sxs-lookup"><span data-stu-id="13466-177">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="13466-178">حدد **الإنجليزية (LanguageCode=1033)** وحدد **تطبيق**.</span><span class="sxs-lookup"><span data-stu-id="13466-178">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="13466-179">قم باستيراد الملف `Inventory Visibility Dataverse Solution.zip`، الذي يتضمن تكوين Dataverse المرتبط بالكيانات و Power Apps:</span><span class="sxs-lookup"><span data-stu-id="13466-179">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="13466-180">انتقل إلى الصفحة **حلول**.</span><span class="sxs-lookup"><span data-stu-id="13466-180">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="13466-181">حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="13466-181">Select **Import**.</span></span>

1. <span data-ttu-id="13466-182">استيراد تدفق مشغل ترقية التكوين:</span><span class="sxs-lookup"><span data-stu-id="13466-182">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="13466-183">انتقل إلى الصفحة Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="13466-183">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="13466-184">تأكد من وجود الاتصال المسمى *Dataverse (قديم)*.</span><span class="sxs-lookup"><span data-stu-id="13466-184">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="13466-185">(إذا لم يكن موجودًا، فقم بإنشاءه).</span><span class="sxs-lookup"><span data-stu-id="13466-185">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="13466-186">استيراد الملف `Inventory Visibility Configuration Trigger.zip`.</span><span class="sxs-lookup"><span data-stu-id="13466-186">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="13466-187">وبعد استيراده، سيظهر المشغل ضمن **التدفقات الخاصة بي**.</span><span class="sxs-lookup"><span data-stu-id="13466-187">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="13466-188">قم بتهيئة المتغيرات الأربعة التالية استنادًا إلى معلومات البيئة:</span><span class="sxs-lookup"><span data-stu-id="13466-188">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="13466-189">مُعرّف مستأجر Azure</span><span class="sxs-lookup"><span data-stu-id="13466-189">Azure Tenant ID</span></span>
        - <span data-ttu-id="13466-190">معرف عميل تطبيق Azure</span><span class="sxs-lookup"><span data-stu-id="13466-190">Azure Application Client ID</span></span>
        - <span data-ttu-id="13466-191">سر عميل تطبيق Azure</span><span class="sxs-lookup"><span data-stu-id="13466-191">Azure Application Client Secret</span></span>
        - <span data-ttu-id="13466-192">نقطة نهاية رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="13466-192">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="13466-193">لمزيد من المعلومات حول هذا المتغير، راجع القسم [إعداد تكامل رؤية المخزون](#setup-inventory-visibility-integration) لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="13466-193">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="13466-194">![مشغل التكوين](media/configuration-trigger.png "مشغل التكوين")</span><span class="sxs-lookup"><span data-stu-id="13466-194">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="13466-195">حدد **تشغيل**</span><span class="sxs-lookup"><span data-stu-id="13466-195">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="13466-196">تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="13466-196">Install the add-in</span></span>

<span data-ttu-id="13466-197">لتثبيت الوظيفة الإضافية لرؤية المخزون، يجب عليك القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="13466-197">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="13466-198">سجل الدخول إلى بوابة [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="13466-198">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="13466-199">في الصفحة الرئيسية ، حدد المشروع حيث يتم نشر البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="13466-199">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="13466-200">في الصفحة المشروع ، حدد البيئة التي ترغب في تثبيت الوظيفة الإضافية بها.</span><span class="sxs-lookup"><span data-stu-id="13466-200">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="13466-201">في الصفحة البيئة، قم بالتمرير لأسفل حتى تشاهد القسم **الوظائف الإضافية الخاصة بالبيئة** في القسم **Power Platform تكامل**، حيث يمكنك العثور على اسم بيئة Dataverse.</span><span class="sxs-lookup"><span data-stu-id="13466-201">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="13466-202">في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="13466-202">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="13466-203">![صفحة البيئة في LCS](media/inventory-visibility-environment.png "صفحة البيئة في LCS")</span><span class="sxs-lookup"><span data-stu-id="13466-203">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="13466-204">حدد الرابط **تثبيت وظيفة إضافية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="13466-204">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="13466-205">يتم فتح قائمه بالوظائف الإضافية المتاحة.</span><span class="sxs-lookup"><span data-stu-id="13466-205">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="13466-206">حدد **رؤية المخزون** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="13466-206">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="13466-207">ادخل قيما للحقول التالية الخاصة ببيئتك:</span><span class="sxs-lookup"><span data-stu-id="13466-207">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="13466-208">**مُعرّف تطبيق AAD (العميل)**</span><span class="sxs-lookup"><span data-stu-id="13466-208">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="13466-209">**معرف مستأجر AAD**</span><span class="sxs-lookup"><span data-stu-id="13466-209">**AAD tenant ID**</span></span>

    <span data-ttu-id="13466-210">![أضافه في صفحه الإعداد](media/inventory-visibility-setup.png "صفحه إعداد الوظيفة الإضافية")</span><span class="sxs-lookup"><span data-stu-id="13466-210">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="13466-211">الموافقة علي البنود والشروط عن طريق تحديد خانه الاختيار **البنود والشروط**.</span><span class="sxs-lookup"><span data-stu-id="13466-211">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="13466-212">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="13466-212">Select **Install**.</span></span> <span data-ttu-id="13466-213">ستظهر حاله الوظيفة الإضافية باعتبارها **قيد التثبيت**.</span><span class="sxs-lookup"><span data-stu-id="13466-213">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="13466-214">عند الانتهاء ، قم بتحديث الصفحة لرؤية تغيير الحالة علي **مثبت**.</span><span class="sxs-lookup"><span data-stu-id="13466-214">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="13466-215">إلغاء تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="13466-215">Uninstall the add-in</span></span>

<span data-ttu-id="13466-216">للغاء تثبيت الوظيفة الإضافية ، حدد **إلغاء التثبيت**.</span><span class="sxs-lookup"><span data-stu-id="13466-216">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="13466-217">عندما تقوم بتحديث LCS، فإنه ستتم إزالة الوظيفة الإضافية لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-217">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="13466-218">تقوم عمليه إزالة التثبيت على إزالة تسجيل الوظيفة الإضافية وبدء مهمة أيضًا لتنظيف كافة بيانات الشركات المخزنة في الخدمة.</span><span class="sxs-lookup"><span data-stu-id="13466-218">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="13466-219">استخدام بيانات المخزون الفعلي من Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="13466-219">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="13466-220">توزيع حزمة تكامل رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="13466-220">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="13466-221">إذا كنت تقوم بتشغيل Supply Chain Management الإصدار 10.0.17 أو إصدار سابق عنه، فتواصل بفريق دعم رؤية المخزون على [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) للحصول علي ملف الحزمة.</span><span class="sxs-lookup"><span data-stu-id="13466-221">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="13466-222">ثم قم بنشر الحزمة في LCS.</span><span class="sxs-lookup"><span data-stu-id="13466-222">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="13466-223">إذا حدث خطأ عدم تطابق في الإصدار أثناء التوزيع، يجب عليك استيراد مشروع X++ يدويًا إلى بيئة التطوير الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="13466-223">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="13466-224">ثم قم بإنشاء الحزمة القابلة للنشر في بيئة التطوير الخاصة بك، ثم قم بنشرها في بيئة الإنتاج الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="13466-224">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="13466-225">يتم تضمين الكود Supply Chain Management في الإصدار 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="13466-225">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="13466-226">إذا كنت تقوم بتشغيل هذا الإصدار أو الأحدث، فإن عملية النشر تكون غير ضرورية.</span><span class="sxs-lookup"><span data-stu-id="13466-226">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="13466-227">تأكد من أنه يتم تشغيل الميزات التالية في بيئة Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="13466-227">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="13466-228">(افتراضيًا، فإنه يتم تشغيلها.)</span><span class="sxs-lookup"><span data-stu-id="13466-228">(By default, they are turned on.)</span></span>

| <span data-ttu-id="13466-229">وصف الميزة</span><span class="sxs-lookup"><span data-stu-id="13466-229">Feature description</span></span> | <span data-ttu-id="13466-230">إصدار الكود</span><span class="sxs-lookup"><span data-stu-id="13466-230">Code version</span></span> | <span data-ttu-id="13466-231">تبديل الفئة</span><span class="sxs-lookup"><span data-stu-id="13466-231">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="13466-232">تمكين أو تعطيل استخدام أبعاد المخزون في جدول InventSum</span><span class="sxs-lookup"><span data-stu-id="13466-232">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="13466-233">10.0.11</span><span class="sxs-lookup"><span data-stu-id="13466-233">10.0.11</span></span> | <span data-ttu-id="13466-234">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="13466-234">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="13466-235">تمكين أو تعطيل استخدام أبعاد المخزون في جدول InventSumDelta</span><span class="sxs-lookup"><span data-stu-id="13466-235">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="13466-236">10.0.12</span><span class="sxs-lookup"><span data-stu-id="13466-236">10.0.12</span></span> | <span data-ttu-id="13466-237">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="13466-237">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="13466-238">إعداد تكامل رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="13466-238">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="13466-239">في Supply Chain Management، افتح مساحة عمل **[إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**، وقم بتشغيل الميزة **تكامل رؤية المخزون**.</span><span class="sxs-lookup"><span data-stu-id="13466-239">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="13466-240">انتقل إلى **إدارة المخزون \> الإعداد \> معلمات تكامل رؤية المخزون**، وأدخل عنوان URL للبيئة التي تقوم فيها بتشغيل رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-240">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="13466-241">ابحث عن منطقة LCS الخاصة ببيئة Azure، ثم أدخل عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="13466-241">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="13466-242">يحتوي عنوان URL على النموذج التالي:</span><span class="sxs-lookup"><span data-stu-id="13466-242">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="13466-243">على سبيل المثال، إذا كنت في أوروبا، سيكون لدي البيئة واحدًا من عناوين (URL) التالية:</span><span class="sxs-lookup"><span data-stu-id="13466-243">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="13466-244">تتوفر المناطق التالية حاليًا.</span><span class="sxs-lookup"><span data-stu-id="13466-244">The following regions are currently available.</span></span>

    | <span data-ttu-id="13466-245">منطقة Azure</span><span class="sxs-lookup"><span data-stu-id="13466-245">Azure region</span></span> | <span data-ttu-id="13466-246">اسم المنطقة القصير</span><span class="sxs-lookup"><span data-stu-id="13466-246">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="13466-247">شرق أستراليا</span><span class="sxs-lookup"><span data-stu-id="13466-247">Australia east</span></span> | <span data-ttu-id="13466-248">eau</span><span class="sxs-lookup"><span data-stu-id="13466-248">eau</span></span> |
    | <span data-ttu-id="13466-249">جنوب شرق أستراليا</span><span class="sxs-lookup"><span data-stu-id="13466-249">Australia southeast</span></span> | <span data-ttu-id="13466-250">seau</span><span class="sxs-lookup"><span data-stu-id="13466-250">seau</span></span> |
    | <span data-ttu-id="13466-251">وسط كندا</span><span class="sxs-lookup"><span data-stu-id="13466-251">Canada central</span></span> | <span data-ttu-id="13466-252">cca</span><span class="sxs-lookup"><span data-stu-id="13466-252">cca</span></span> |
    | <span data-ttu-id="13466-253">شرق كندا</span><span class="sxs-lookup"><span data-stu-id="13466-253">Canada east</span></span> | <span data-ttu-id="13466-254">eca</span><span class="sxs-lookup"><span data-stu-id="13466-254">eca</span></span> |
    | <span data-ttu-id="13466-255">شمال أوروبا</span><span class="sxs-lookup"><span data-stu-id="13466-255">North Europe</span></span> | <span data-ttu-id="13466-256">neu</span><span class="sxs-lookup"><span data-stu-id="13466-256">neu</span></span> |
    | <span data-ttu-id="13466-257">غرب أوروبا</span><span class="sxs-lookup"><span data-stu-id="13466-257">West Europe</span></span> | <span data-ttu-id="13466-258">weu</span><span class="sxs-lookup"><span data-stu-id="13466-258">weu</span></span> |
    | <span data-ttu-id="13466-259">شرق الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="13466-259">East US</span></span> | <span data-ttu-id="13466-260">eus</span><span class="sxs-lookup"><span data-stu-id="13466-260">eus</span></span> |
    | <span data-ttu-id="13466-261">غرب الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="13466-261">West US</span></span> | <span data-ttu-id="13466-262">wus</span><span class="sxs-lookup"><span data-stu-id="13466-262">wus</span></span> |

1. <span data-ttu-id="13466-263">انتقل إلى **إدارة المخزون \> دوري \> تكامل رؤية المخزون**، وقم بتمكين الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="13466-263">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="13466-264">سيتم الآن ترحيل كافة أحداث تغيير المخزون من Supply Chain Management إلى رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-264">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="13466-265">واجهة API العامة للوظيفة الإضافية لرؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="13466-265">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="13466-266">تقدم واجهة برمجة التطبيقات العامة لـ REST الخاصة بالوظيفة الإضافية لرؤية المخزون العديد من نقاط التكامل الخاصة.</span><span class="sxs-lookup"><span data-stu-id="13466-266">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="13466-267">ويدعم ثلاثه أنواع من التفاعلات الرئيسية:</span><span class="sxs-lookup"><span data-stu-id="13466-267">It supports three main interaction types:</span></span>

- <span data-ttu-id="13466-268">ترحيل تغييرات المخزون الفعلية إلى الوظيفة الإضافية من نظام خارجي</span><span class="sxs-lookup"><span data-stu-id="13466-268">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="13466-269">الاستعلام عن الكميات الفعلية الحالية من نظام خارجي</span><span class="sxs-lookup"><span data-stu-id="13466-269">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="13466-270">مزامنة تلقائية مع مخزون Supply Chain Management الفعلي</span><span class="sxs-lookup"><span data-stu-id="13466-270">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="13466-271">لا تعتبر المزامنة التلقائية جزءًا من API العامة.</span><span class="sxs-lookup"><span data-stu-id="13466-271">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="13466-272">وبدلاً من ذلك، تتم معالجتة في الخلفية للبيئات التي تم فيها تمكين الوظيفة الإضافية لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-272">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="13466-273">مصادقة</span><span class="sxs-lookup"><span data-stu-id="13466-273">Authentication</span></span>

<span data-ttu-id="13466-274">يتم استخدام الرمز المميز لأمان النظام الأساسي لاستدعاء الوظيفة الإضافية لرؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-274">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="13466-275">ولذلك، يجب إنشاء رمز *Azure Active Directory (Azure AD) المميز* باستخدام تطبيق Azure AD.</span><span class="sxs-lookup"><span data-stu-id="13466-275">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="13466-276">يجب استخدام رمز Azure AD المميز للحصول على *رمز الوصول المميز* من خدمة الأمان.</span><span class="sxs-lookup"><span data-stu-id="13466-276">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="13466-277">احصل علي رمز خدمه أمان بالقيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="13466-277">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="13466-278">سجل دخولك إلى مدخل Azure واستخدمه للعثور على `clientId` و `clientSecret` لتطبيق Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="13466-278">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="13466-279">إحضار Azure Active Directory رمز مميز (`aadToken`) عن طريق إرسال طلب HTTP بالخصائص التالية:</span><span class="sxs-lookup"><span data-stu-id="13466-279">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="13466-280">**عنوان URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="13466-280">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="13466-281">**الطريقة** - `GET`</span><span class="sxs-lookup"><span data-stu-id="13466-281">**Method** - `GET`</span></span>
    - <span data-ttu-id="13466-282">**محتوي النص الأساسي (بيانات النموذج)**:</span><span class="sxs-lookup"><span data-stu-id="13466-282">**Body content (form data)**:</span></span>

        | <span data-ttu-id="13466-283">المفتاح</span><span class="sxs-lookup"><span data-stu-id="13466-283">key</span></span> | <span data-ttu-id="13466-284">القيمة</span><span class="sxs-lookup"><span data-stu-id="13466-284">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="13466-285">client_id</span><span class="sxs-lookup"><span data-stu-id="13466-285">client_id</span></span> | <span data-ttu-id="13466-286">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="13466-286">${aadAppId}</span></span> |
        | <span data-ttu-id="13466-287">client_secret</span><span class="sxs-lookup"><span data-stu-id="13466-287">client_secret</span></span> | <span data-ttu-id="13466-288">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="13466-288">${aadAppSecret}</span></span> |
        | <span data-ttu-id="13466-289">grant_type</span><span class="sxs-lookup"><span data-stu-id="13466-289">grant_type</span></span> | <span data-ttu-id="13466-290">client_credentials</span><span class="sxs-lookup"><span data-stu-id="13466-290">client_credentials</span></span> |
        | <span data-ttu-id="13466-291">مورد</span><span class="sxs-lookup"><span data-stu-id="13466-291">resource</span></span> | <span data-ttu-id="13466-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="13466-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="13466-293">يجب ان تتلقي `aadToken` استجابه فيها، والتي تشبه المثال التالي.</span><span class="sxs-lookup"><span data-stu-id="13466-293">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="13466-294">المستقبل طلب JSON مشابها لما يلي:</span><span class="sxs-lookup"><span data-stu-id="13466-294">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="13466-295">المكان:</span><span class="sxs-lookup"><span data-stu-id="13466-295">Where:</span></span>
    - <span data-ttu-id="13466-296">`client_assertion`يجب ان تكون القيمة هي `aadToken` التي استلمتها في الخطوة السابقة.</span><span class="sxs-lookup"><span data-stu-id="13466-296">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="13466-297">`context`يجب ان تكون القيمة معرف البيئة حيث تريد توزيع الوظيفة الإضافية.</span><span class="sxs-lookup"><span data-stu-id="13466-297">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="13466-298">قم بتعيين كافة القيم الأخرى كما هو موضح في المثال.</span><span class="sxs-lookup"><span data-stu-id="13466-298">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="13466-299">قم بإرسال طلب HTTP بالخصائص التالية:</span><span class="sxs-lookup"><span data-stu-id="13466-299">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="13466-300">**عنوان URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="13466-300">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="13466-301">**الطريقة** - `POST`</span><span class="sxs-lookup"><span data-stu-id="13466-301">**Method** - `POST`</span></span>
    - <span data-ttu-id="13466-302">**راس HTTP** - تضمين إصدار API (`Api-Version` المفتاح هو والقيمة هو `1.0`)</span><span class="sxs-lookup"><span data-stu-id="13466-302">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="13466-303">**محتوي أساسي** - تضمين طلب JSON الذي قمت بإنشاءه في الخطوة السابقة.</span><span class="sxs-lookup"><span data-stu-id="13466-303">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="13466-304">ستحصل علي `access_token` في الاستجابة.</span><span class="sxs-lookup"><span data-stu-id="13466-304">You will get an `access_token` in response.</span></span> <span data-ttu-id="13466-305">وهذا ما تحتاجه كرمز مميز في الحامل لاستدعاء امكانيه رؤية API للمخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-305">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="13466-306">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="13466-306">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="13466-307">عينة طلب</span><span class="sxs-lookup"><span data-stu-id="13466-307">Sample Request</span></span>

<span data-ttu-id="13466-308">كمرجع لك، فيما يلي عينة طلب http، يمكنك استخدام أي أدوات أو لغة تعليمات برمجية لإرسال هذا الطلب، مثل ``Postman``.</span><span class="sxs-lookup"><span data-stu-id="13466-308">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

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

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="13466-309">تكوين واجهه برمجه تطبيقات امكانيه رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="13466-309">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="13466-310">قبل استخدام الخدمة ، يجب إكمال التكوينات الموضحة في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="13466-310">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="13466-311">قد يختلف التكوين استنادا إلى تفاصيل البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="13466-311">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="13466-312">وهو يتضمن بشكل أساسي أربعه أجزاء:</span><span class="sxs-lookup"><span data-stu-id="13466-312">It primarily includes four parts:</span></span>

- [<span data-ttu-id="13466-313">تقسيم</span><span class="sxs-lookup"><span data-stu-id="13466-313">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="13466-314">تكوينات الأبعاد</span><span class="sxs-lookup"><span data-stu-id="13466-314">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="13466-315">فهرسة</span><span class="sxs-lookup"><span data-stu-id="13466-315">Indexing</span></span>](#indexing)
- [<span data-ttu-id="13466-316">قياس مخصص</span><span class="sxs-lookup"><span data-stu-id="13466-316">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="13466-317">تقسيم</span><span class="sxs-lookup"><span data-stu-id="13466-317">Partitioning</span></span>

<span data-ttu-id="13466-318">يمكن للتقسيم ان يؤثر بشكل كبير علي أداء واجهة API الخاصة برؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-318">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="13466-319">انها لفكره جيده ان تقوم بتعريف نظام يسمح بالتجميعات الصغيرة للبيانات مع استمرار السماح باستعلامات البيانات ذات المعني.</span><span class="sxs-lookup"><span data-stu-id="13466-319">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="13466-320">سيكون `organizationId` (`dataAreaId` في Supply Chain Management) دائما جزءا من التقسيم ، ويتم تعيين رؤية المخزون بشكل افتراضي علي قسم حسب الابعاد *كموقع إلكتروني + موقع جغرافي*.</span><span class="sxs-lookup"><span data-stu-id="13466-320">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="13466-321">وهذا يعني انه يجب دوما الاستعلام عن الخدمة باستخدام هذه الابعاد المحددة في عوامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="13466-321">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="13466-322">*الموقع الإلكتروني* و *الموقع الجغرافي* هما اثنان من الابعاد الافتراضية في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-322">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="13466-323">في Supply Chain Management، تسمي هذه الابعاد *بالموقع الإلكتروني* (`InventSiteId`) *والمستودع* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="13466-323">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="13466-324">تكوينات الأبعاد</span><span class="sxs-lookup"><span data-stu-id="13466-324">Dimension configurations</span></span>

<span data-ttu-id="13466-325">ستوفر امكانيه رؤية المخزون قائمه بالابعاد الافتراضية العامة لتمكين تكامل النظام المصدر المتعدد.</span><span class="sxs-lookup"><span data-stu-id="13466-325">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="13466-326">يسرد الجدول التالي ابعاد المخزون التي ستكون أسماء الابعاد الافتراضية في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-326">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="13466-327">نوع البعد</span><span class="sxs-lookup"><span data-stu-id="13466-327">Dimension type</span></span> | <span data-ttu-id="13466-328">اسم البُعد</span><span class="sxs-lookup"><span data-stu-id="13466-328">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="13466-329">منتج</span><span class="sxs-lookup"><span data-stu-id="13466-329">Product</span></span> | `ColorId` |
| <span data-ttu-id="13466-330">منتج</span><span class="sxs-lookup"><span data-stu-id="13466-330">Product</span></span> | `SizeId` |
| <span data-ttu-id="13466-331">منتج</span><span class="sxs-lookup"><span data-stu-id="13466-331">Product</span></span> | `StyleId` |
| <span data-ttu-id="13466-332">منتج</span><span class="sxs-lookup"><span data-stu-id="13466-332">Product</span></span> | `ConfigId` |
| <span data-ttu-id="13466-333">التعقب</span><span class="sxs-lookup"><span data-stu-id="13466-333">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="13466-334">التعقب</span><span class="sxs-lookup"><span data-stu-id="13466-334">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="13466-335"> الموق</span><span class="sxs-lookup"><span data-stu-id="13466-335">Location</span></span> | `LocationId` |
| <span data-ttu-id="13466-336"> الموق</span><span class="sxs-lookup"><span data-stu-id="13466-336">Location</span></span> | `SiteId` |
| <span data-ttu-id="13466-337">حالة المخزون</span><span class="sxs-lookup"><span data-stu-id="13466-337">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="13466-338">خاص بالمستودع</span><span class="sxs-lookup"><span data-stu-id="13466-338">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="13466-339">خاص بالمستودع</span><span class="sxs-lookup"><span data-stu-id="13466-339">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="13466-340">خاص بالمستودع</span><span class="sxs-lookup"><span data-stu-id="13466-340">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="13466-341">يكون نوع البعد المدرج في الجدول السابق كمرجع فقط.</span><span class="sxs-lookup"><span data-stu-id="13466-341">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="13466-342">لا يلزم تحديد نوع البعد في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-342">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="13466-343">في حاله وجود بعد مخصص والحاجة إلى التدفق للقيمة الافتراضية عند استهلاك رؤية المخزون ، يمكنك تكوين **اسم البعد المخصص** في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-343">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="13466-344">وصول الانظمه الخارجية إلى رؤية المخزون من خلال واجات برمجه التطبيقات RESTful التي تتيح معلومات الكمية الفعلية حول مجموعات الابعاد المحددة التي سيتم الاستعلام عنها.</span><span class="sxs-lookup"><span data-stu-id="13466-344">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="13466-345">بالنسبة للتكامل ، يمكنك رؤية المخزون من تكوين *مصدر بيانات القناة الخارجية* وبعد المصدر علي *الابعاد المستهدفة* في رؤية المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-345">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="13466-346">يجب ان تكون الابعاد المستهدفة واحده مما يلي:</span><span class="sxs-lookup"><span data-stu-id="13466-346">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="13466-347">الابعاد الافتراضية في رؤية المخزون</span><span class="sxs-lookup"><span data-stu-id="13466-347">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="13466-348">الأبعاد المخصصة</span><span class="sxs-lookup"><span data-stu-id="13466-348">Custom dimensions</span></span>

<span data-ttu-id="13466-349">والغرض من تكوين الابعاد هو توحيد التكامل المتعدد الانظمه للاستعلام علي الابعاد وحدث الترحيل مع الابعاد.</span><span class="sxs-lookup"><span data-stu-id="13466-349">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="13466-350">فهرسة</span><span class="sxs-lookup"><span data-stu-id="13466-350">Indexing</span></span>

<span data-ttu-id="13466-351">في معظم الأوقات ، لن يكون الاستعلام الفعلي الخاص بالمخزون علي مستوي "الإجمالي" الأعلى فقط ، ولكن قد ترغب في رؤية النتائج المجمعة استنادا إلى ابعاد المخزون.</span><span class="sxs-lookup"><span data-stu-id="13466-351">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="13466-352">توفر امكانيه رؤية المخزون المرونة عن طريق السماح لك بإعداد الفهارس ، التي تعتمد علي البعد أو مجموعه الابعاد.</span><span class="sxs-lookup"><span data-stu-id="13466-352">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="13466-353">حاليا ، يمكنك فقط تكوين الفهارس بخمسه كحد اقصي.</span><span class="sxs-lookup"><span data-stu-id="13466-353">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="13466-354">يجب مراعاه البعد أو مجموعه الابعاد التي ستستخدمها قبل التنفيذ للتاكد من انها ستفي باحتياجات أعمالك.</span><span class="sxs-lookup"><span data-stu-id="13466-354">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="13466-355">علي سبيل المثال ، إذا كنت ترغب في الاستعلام عن المنتجات كالتالي:</span><span class="sxs-lookup"><span data-stu-id="13466-355">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="13466-356">الاستعلام عن المنتج المجمع الفعلي بواسطة ابعاد *اللون* و *الحجم*.</span><span class="sxs-lookup"><span data-stu-id="13466-356">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="13466-357">في بعض الحالات ، تريد فقط الاستعلام عن المنتج إجمالا.</span><span class="sxs-lookup"><span data-stu-id="13466-357">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="13466-358">سيكون لديك فهرسين محددين كالتالي:</span><span class="sxs-lookup"><span data-stu-id="13466-358">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="13466-359">سيتم تجميع القوس الفارغ استنادا إلى "معرف المنتج" داخل القسم.</span><span class="sxs-lookup"><span data-stu-id="13466-359">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="13466-360">تحدد الفهرسة كيفيه تجميع النتائج استنادا إلى إعداد الاستعلام `groupBy`.</span><span class="sxs-lookup"><span data-stu-id="13466-360">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="13466-361">في هذه الحالة إذا لم تقم بتحديد أي قيم `groupBy`، سيتم الحصول علي الإجماليات بواسطة `productid`.</span><span class="sxs-lookup"><span data-stu-id="13466-361">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="13466-362">وإلا، إذا قمت بتحديد `groupBy` كـ `groupBy=ColorId&groupBy=SizeId`، ستحصل على بنود متعددة يتم إرجاعها، استنادًا إلى مجموعتي اللون والحجم المختلفتين في النظام.</span><span class="sxs-lookup"><span data-stu-id="13466-362">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="13466-363">يمكنك وضع معايير الاستعلام في النص الأساسي للطلب.</span><span class="sxs-lookup"><span data-stu-id="13466-363">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="13466-364">فيما يلي نموذج استعلام حول المنتج بمجموعه اللون والحجم.</span><span class="sxs-lookup"><span data-stu-id="13466-364">Here is a sample query on the product with color and size combination.</span></span>

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

<span data-ttu-id="13466-365">فيما يتعلق بالحقل `filters`، وحده `ProductId` يدعم القيم المتعددة.</span><span class="sxs-lookup"><span data-stu-id="13466-365">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="13466-366">إذا كان `ProductId`مصفوفة فارغة، فسيتم الاستعلام عن كافة المنتجات.</span><span class="sxs-lookup"><span data-stu-id="13466-366">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="13466-367">قياس مخصص</span><span class="sxs-lookup"><span data-stu-id="13466-367">Custom measurement</span></span>

<span data-ttu-id="13466-368">يتم ربط كميات القياس الافتراضية بـ Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="13466-368">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="13466-369">ومع ذلك، قد ترغب في الحصول على كمية تتكون من مجموعة من القياسات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="13466-369">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="13466-370">وللقيام بذلك ، يمكن ان يكون لديك تكوين كميات مخصصه ، والتي ستتم اضافتها إلى إخراج الاستعلامات الفعلية.</span><span class="sxs-lookup"><span data-stu-id="13466-370">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="13466-371">وتتيح الوظيفة ببساطه تحديد مجموعه من القياسات التي ستتم اضافتها ، و/أو مجموعه من المقاييس التي سيتم طرحها ، من أجل القياس المخصص.</span><span class="sxs-lookup"><span data-stu-id="13466-371">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="13466-372">علي سبيل المثال ، باستخدام شرط الاستعلام التالي ، ستقوم بتكوين كميه القياس المخصصة باعتبارها `MyCustomAvailableforReservation` ليتم استهلاكها من قبل نظام الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="13466-372">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="13466-373">نظام الاستهلاك</span><span class="sxs-lookup"><span data-stu-id="13466-373">Consumption system</span></span> | <span data-ttu-id="13466-374">القياسات المحتسبة</span><span class="sxs-lookup"><span data-stu-id="13466-374">Calculated measurers</span></span> | <span data-ttu-id="13466-375">مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="13466-375">Data source</span></span> | <span data-ttu-id="13466-376">أداه التعديل</span><span class="sxs-lookup"><span data-stu-id="13466-376">Modifier</span></span> | <span data-ttu-id="13466-377">نوع حساب أداة التعديل</span><span class="sxs-lookup"><span data-stu-id="13466-377">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="13466-378">الجمع</span><span class="sxs-lookup"><span data-stu-id="13466-378">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="13466-379">الجمع</span><span class="sxs-lookup"><span data-stu-id="13466-379">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="13466-380">الطرح</span><span class="sxs-lookup"><span data-stu-id="13466-380">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="13466-381">الجمع</span><span class="sxs-lookup"><span data-stu-id="13466-381">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="13466-382">الطرح</span><span class="sxs-lookup"><span data-stu-id="13466-382">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="13466-383">الجمع</span><span class="sxs-lookup"><span data-stu-id="13466-383">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="13466-384">الجمع</span><span class="sxs-lookup"><span data-stu-id="13466-384">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="13466-385">الطرح</span><span class="sxs-lookup"><span data-stu-id="13466-385">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="13466-386">الطرح</span><span class="sxs-lookup"><span data-stu-id="13466-386">Subtraction</span></span> |

<span data-ttu-id="13466-387">ومع ذلك ، سيقوم الاستعلام الموجود علي كميه القياس المخصصة بإرجاع المخرجات التالية.</span><span class="sxs-lookup"><span data-stu-id="13466-387">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="13466-388">يعتمد إخراج `MyCustomAvailableforReservation`علي إعداد الحساب في القياسات المخصصة كما يلي:</span><span class="sxs-lookup"><span data-stu-id="13466-388">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="13466-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="13466-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="13466-390">ترحيل التغييرات الفعلية</span><span class="sxs-lookup"><span data-stu-id="13466-390">Posting on-hand changes</span></span>

<span data-ttu-id="13466-391">ويعتمد عنوان URL الذي يتم ترحيل الحدث عليه علي المنطقة الجغرافية بالبالضبط.</span><span class="sxs-lookup"><span data-stu-id="13466-391">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="13466-392">سياخذ النموذج ما يلي:</span><span class="sxs-lookup"><span data-stu-id="13466-392">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="13466-393">عند المصادقة ، يمكن استخدام محدد موقع المعلومات (URL) هذا مع أسلوب `POST` HTTP لإرسال احداث التغيير الفعلي إلى الخدمة.</span><span class="sxs-lookup"><span data-stu-id="13466-393">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="13466-394">يتم استخدام الراس الخاص للاتصال مع خدمات Dynamics 365 من خلال طلبات HTTP ، والذي يشير إلى معرف البيئة لمثيل Supply Chain Management الذي ترتبط به البيانات.</span><span class="sxs-lookup"><span data-stu-id="13466-394">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="13466-395">على سبيل المثال:</span><span class="sxs-lookup"><span data-stu-id="13466-395">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="13466-396">ترحيل التغييرات الفعلية مثال الاستعلام 1</span><span class="sxs-lookup"><span data-stu-id="13466-396">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="13466-397">يوضح هذا المثال السيناريو الذي ستقوم فيه بإعداد تكوين البعد في Power Apps.</span><span class="sxs-lookup"><span data-stu-id="13466-397">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="13466-398">استخدم الاستعلام التالي لتكوين تعيين البعد في Power Apps:</span><span class="sxs-lookup"><span data-stu-id="13466-398">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="13466-399">يمكنك الآن تحديد `dimensionDataSource` واستخدام الابعاد المخصصة في الاستعلامات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="13466-399">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="13466-400">سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="13466-400">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="13466-401">ترحيل التغييرات الفعلية مثال الاستعلام 2</span><span class="sxs-lookup"><span data-stu-id="13466-401">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="13466-402">يوضح هذا المثال السيناريو الذي لا يتم فيه إعداد تعيينات لتكوين البعد في Power Apps، التالي يجب ان تستخدم الترحيل أيضا الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="13466-402">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="13466-403">يجب ان تكون كافة الابعاد بابعاد أساسيه عندما يكون الحقل `dimensionDataSource` خاليا أو فارغا أو مسافة بيضاء.</span><span class="sxs-lookup"><span data-stu-id="13466-403">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="13466-404">خصائص حقل مستند JSON</span><span class="sxs-lookup"><span data-stu-id="13466-404">JSON document field properties</span></span>

<span data-ttu-id="13466-405">تتضمن الحقول الموجودة في أمثله استعلام JSON المتوفرة في السابق الخصائص المسرودة في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="13466-405">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="13466-406">معرف الحقل</span><span class="sxs-lookup"><span data-stu-id="13466-406">Field ID</span></span> | <span data-ttu-id="13466-407">الوصف</span><span class="sxs-lookup"><span data-stu-id="13466-407">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="13466-408">معرف فريد لحدث التغيير المحدد.</span><span class="sxs-lookup"><span data-stu-id="13466-408">A unique ID for the specific change event.</span></span> <span data-ttu-id="13466-409">يتم استخدام هذا المعرف للتاكد من فشل الاتصال بالخدمة اثناء الترحيل ، ولن يؤدي أعاده إرسال الحدث إلى نفس الحدث الذي يتم حسابه مرتين في النظام.</span><span class="sxs-lookup"><span data-stu-id="13466-409">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="13466-410">معرف المؤسسة المرتبط بالحدث.</span><span class="sxs-lookup"><span data-stu-id="13466-410">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="13466-411">وهذا ما يعين لمؤسسات Supply Chain Management أو معرفات مناطق البيانات.</span><span class="sxs-lookup"><span data-stu-id="13466-411">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="13466-412">معرف أمر الإنتاج المحدد.</span><span class="sxs-lookup"><span data-stu-id="13466-412">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="13466-413">الكمية التي يجب تغيير الكمية الحالية وفقا لها.</span><span class="sxs-lookup"><span data-stu-id="13466-413">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="13466-414">علي سبيل المثال ، تمت أضافه 10 قطع من خبز البيغلز جديده إلى الرف، ستكون هذه القيمة 10.</span><span class="sxs-lookup"><span data-stu-id="13466-414">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="13466-415">إذا تمت أزاله 3 قطع من خبز البيغلز من الرف أو بيعه ، ستكون هذه القيمة -3.</span><span class="sxs-lookup"><span data-stu-id="13466-415">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="13466-416">مصدر البيانات الخاص بالابعاد المستخدمة في حدث تغيير الترحيل والاستعلام.</span><span class="sxs-lookup"><span data-stu-id="13466-416">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="13466-417">إذا قمت بتحديد مصدر البيانات ، يمكنك استخدام الابعاد المخصصة من مصدر البيانات المحدد.</span><span class="sxs-lookup"><span data-stu-id="13466-417">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="13466-418">باستخدام تكوين البعد ، يمكن ان يقوم ظهور المخزون بتعيين الابعاد المخصصة إلى الابعاد الافتراضية العامة.</span><span class="sxs-lookup"><span data-stu-id="13466-418">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="13466-419">في حاله عدم تحديد `dimensionDataSource`، يمكنك استخدام الابعاد الافتراضية العامة فقط في الاستعلامات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="13466-419">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="13466-420">كيس مجموعه حيوية من أزواج مفتاح/قيمه.</span><span class="sxs-lookup"><span data-stu-id="13466-420">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="13466-421">سيتم تعيينها لبعض الابعاد في Supply Chain Management، ولكن يمكنك أيضا أضافه ابعاد مخصصه (مثل *المصدر*) والتي قد تشير إلى ما إذا كان الحدث واردا من Supply Chain Management أو من النظام الخارجي.</span><span class="sxs-lookup"><span data-stu-id="13466-421">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="13466-422">الاستعلام عن الكمية الحالية</span><span class="sxs-lookup"><span data-stu-id="13466-422">Querying current on-hand</span></span>

<span data-ttu-id="13466-423">سيكون للنقطة النهائية للاستعلام عن الكمية الحالية عنوان URL مشابه:</span><span class="sxs-lookup"><span data-stu-id="13466-423">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="13466-424">سيتم الاستعلام عنها باستخدام أسلوب `POST` HTTP.</span><span class="sxs-lookup"><span data-stu-id="13466-424">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="13466-425">مثال علي الاستعلام الفعلي حاليا 1</span><span class="sxs-lookup"><span data-stu-id="13466-425">Current on-hand query example 1</span></span>

<span data-ttu-id="13466-426">يوضح هذا المثال السيناريو الذي ستقوم فيه بإعداد تكوين البعد في Power Apps.</span><span class="sxs-lookup"><span data-stu-id="13466-426">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="13466-427">استخدم الاستعلام التالي لتكوين تعيين البعد في Power Apps:</span><span class="sxs-lookup"><span data-stu-id="13466-427">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="13466-428">يمكنك الآن تحديد `dimensionDataSource` واستخدام الابعاد المخصصة في الاستعلامات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="13466-428">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="13466-429">سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="13466-429">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="13466-430">يمكنك تحديد `DimensionDataSource` في `filters` وتحديد ابعاد مخصصه في كل من `filters` و`groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="13466-430">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="13466-431">سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="13466-431">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="13466-432">مثال علي الاستعلام الفعلي حاليا 2</span><span class="sxs-lookup"><span data-stu-id="13466-432">Current on-hand query example 2</span></span>

<span data-ttu-id="13466-433">يوضح هذا المثال السيناريو الذي لا يتم فيه إعداد تعيينات لتكوين البعد في Power Apps، التالي يجب ان تستخدم الترحيل أيضا الابعاد الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="13466-433">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="13466-434">يجب ان تكون كافة الابعاد بابعاد أساسيه عندما يكون الحقل `dimensionDataSource`، ضمن `filters` خاليا أو فارغا أو مسافة بيضاء.</span><span class="sxs-lookup"><span data-stu-id="13466-434">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="13466-435">مثال نتيجة الإرجاع</span><span class="sxs-lookup"><span data-stu-id="13466-435">Example return result</span></span>

<span data-ttu-id="13466-436">قد تؤدي الاستعلامات المعروضة في الامثله السابقة إلى إرجاع نتيجة مثل هذه.</span><span class="sxs-lookup"><span data-stu-id="13466-436">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="13466-437">لاحظ انه يتم بناء حقول الكميات كقاموس للمقاييس والقيم المقترنة بها.</span><span class="sxs-lookup"><span data-stu-id="13466-437">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
