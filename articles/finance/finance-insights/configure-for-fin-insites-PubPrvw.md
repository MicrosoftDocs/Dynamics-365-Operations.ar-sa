---
title: تكوين Finance insights للإصدار أولي للاستخدام العام (إصدار أولي) - الإصدار 10.0.20 والإصدارات اللاحقة
description: يشرح هذا الموضوع كيفية تكوين النظام الخاص بك لاستخدام القدرات المتوفرة في Finance insights للإصدار أولي للاستخدام العام (إصدار أولي) - الإصدار 10.0.20 والإصدارات اللاحقة‬.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222602"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a><span data-ttu-id="de4aa-103">تكوين Finance insights للإصدار أولي للاستخدام العام (إصدار أولي) - الإصدار 10.0.20 والإصدارات اللاحقة</span><span class="sxs-lookup"><span data-stu-id="de4aa-103">Configuration for Finance insights for public preview (preview) - version 10.0.20 and later</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="de4aa-104">تضم Finance insights الوظيفة من Microsoft Dynamics 365 Finance مع Dataverse وAzure و AI Builder لتوفير أدوات التنبؤ القوية لمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="de4aa-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="de4aa-105">يشرح هذا الموضوع كيفية تكوين Dynamics 365 Finance الإصدار 10.0.20 لذلك يمكن للنظام استخدام القدرات المتوفرة في الإصدار الأولي للاستخدام العام من Finance insights.</span><span class="sxs-lookup"><span data-stu-id="de4aa-105">This topic explains how to configure Dynamics 365 Finance version 10.0.20 so that your system can use the capabilities that are available in Finance insights public preview.</span></span>

> [!NOTE]
> <span data-ttu-id="de4aa-106">تنطبق خطوات التكوين الموضحة في هذا الموضوع فقط على Finance الإصدار 10.0.20 والإصدارات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="de4aa-106">The configuration steps that are described in this topic apply only to Finance version 10.0.20 and later.</span></span> <span data-ttu-id="de4aa-107">"لإعداد Finance insights في الإصدار 10.0.19 والإصدارات السابقة، راجع [تكوين Finance insights - الإصدارات حتى 10.0.18](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="de4aa-107">'To set up Finance insights on version 10.0.19 and earlier, see [Configuration for Finance insights - versions up to 10.0.18](configure-for-fin-insites.md).</span></span>

## <a name="deploy-finance"></a><span data-ttu-id="de4aa-108">نشر Finance</span><span class="sxs-lookup"><span data-stu-id="de4aa-108">Deploy Finance</span></span>

<span data-ttu-id="de4aa-109">اتبع هذه الخطوات لنشر البيئات.</span><span class="sxs-lookup"><span data-stu-id="de4aa-109">Follow these steps to deploy the environments.</span></span>

1. <span data-ttu-id="de4aa-110">في Microsoft Dynamics Lifecycle Services (LCS)، قم بإنشاء بيئة Finance أو تحديثها.</span><span class="sxs-lookup"><span data-stu-id="de4aa-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Finance environment.</span></span> <span data-ttu-id="de4aa-111">تتطلب البيئة تطبيق الإصدار 10.0.20 أو أحدث من تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="de4aa-111">The environment requires app version 10.0.20 or later of Finance and Operations apps.</span></span>
2. <span data-ttu-id="de4aa-112">يجب أن تكون البيئة بيئة عالية التوافر (HA) في وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="de4aa-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="de4aa-113">(يُعرف هذا النوع من البيئة أيضًا ببيئة الطبقة 2). لمزيد من المعلومات، راجع [تخطيط البيئة](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="de4aa-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="de4aa-114">إذا كنت تقوم بتكوين Finance insights في بيئة حماية، فقد تحتاج إلى نسخ بيانات الإنتاج إلى تلك البيئة لتوقعات العمل.</span><span class="sxs-lookup"><span data-stu-id="de4aa-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="de4aa-115">يستخدم نموذج التنبؤ سنوات متعددة من البيانات لبناء التوقعات.</span><span class="sxs-lookup"><span data-stu-id="de4aa-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="de4aa-116">لا تحتوي بيانات العرض التوضيحي لـ Contoso على بيانات تاريخية كافية للتدريب على نموذج التوقع بشكل ملائم.</span><span class="sxs-lookup"><span data-stu-id="de4aa-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="de4aa-117">تكوين Dataverse</span><span class="sxs-lookup"><span data-stu-id="de4aa-117">Configure Dataverse</span></span>

<span data-ttu-id="de4aa-118">استخدم هذه الخطوات لتكوين Dataverse لـ Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="de4aa-118">Follow these steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="de4aa-119">في LCS، افتح صفحة البيئة، وتحقق من أن قسم **تكامل Power Platform** تم إعداده بالفعل.</span><span class="sxs-lookup"><span data-stu-id="de4aa-119">In LCS, open the environment page, and verify that the **Power Platform Integration** section is already set up.</span></span>

    - <span data-ttu-id="de4aa-120">في حالة إعداده بالفعل، يجب سرد اسم بيئة Dataverse المرتبط ببيئة Finance.</span><span class="sxs-lookup"><span data-stu-id="de4aa-120">If it's already set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>
    - <span data-ttu-id="de4aa-121">في حالة عدم إعداده بعد، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="de4aa-121">If it isn't yet set up, follow these steps:</span></span>

        1. <span data-ttu-id="de4aa-122">في القسم **تكامل Power Platform**، حدد **إعداد**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-122">In the **Power Platform Integration** section, select **Setup**.</span></span> <span data-ttu-id="de4aa-123">قد يستغرق إعداد البيئة ما يصل إلى ساعة واحدة.</span><span class="sxs-lookup"><span data-stu-id="de4aa-123">Setup of the environment might take up to an hour.</span></span>
        2. <span data-ttu-id="de4aa-124">في حالة إعداد بيئة Dataverse بنجاح، يجب سرد اسم بيئة Dataverse المرتبط ببيئة Finance.</span><span class="sxs-lookup"><span data-stu-id="de4aa-124">If the Dataverse environment is successfully set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>

        > [!NOTE]
        > <span data-ttu-id="de4aa-125">بعد إكمال إعداد البيئة، **لا** تقم بتحديد **ارتباط إلى CDS للتطبيقات**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-125">After you complete the environment setup, do **not** select **Link to CDS for Apps**.</span></span> <span data-ttu-id="de4aa-126">هذا الزر غير مطلوب لـ Finance insights.</span><span class="sxs-lookup"><span data-stu-id="de4aa-126">This button isn't required for Finance insights.</span></span> <span data-ttu-id="de4aa-127">إذا قمت بتحديده، فلن تتمكن من تكوين وظائف البيئة الإضافية المطلوبة في LCS.</span><span class="sxs-lookup"><span data-stu-id="de4aa-127">If you select it, you won't be able to configure the required environment add-ins in LCS.</span></span>

## <a name="configure-azure"></a><span data-ttu-id="de4aa-128">تكوين Azure</span><span class="sxs-lookup"><span data-stu-id="de4aa-128">Configure Azure</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="de4aa-129">استخدام Azure Cloud Shell لإعداد موارد Finance insights Data Lake</span><span class="sxs-lookup"><span data-stu-id="de4aa-129">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="de4aa-130">استخدم البرنامج النصي لـ Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="de4aa-130">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="de4aa-131">لقد تم توفير برنامج Windows PowerShell النصي حتى يمكنك بسهولة إعداد موارد Azure الموضحة في [تكوين التصدير إلى Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="de4aa-131">A Windows PowerShell script has been provided so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="de4aa-132">إذا كنت تفضل القيام بالإعداد يدويًا، فعليك تخطي هذا الإجراء، وإكمال الإجراء في القسم [الإعداد اليدوي](#manual-setup) بدلاً منه.</span><span class="sxs-lookup"><span data-stu-id="de4aa-132">If you prefer to do the setup manually, skip this procedure, and complete the procedure in the [Manual setup](#manual-setup) section instead.</span></span>

> [!NOTE]
> <span data-ttu-id="de4aa-133">استخدم الإجراء التالي لتشغيل البرنامج النصي Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="de4aa-133">Use the following procedure to run the Windows PowerShell script.</span></span> <span data-ttu-id="de4aa-134">قد لا يعمل الإعداد إذا كنت تستخدم الخيار **جربه** في Azure CLI أو إذا قمت بتشغيل البرنامج النصي على الكمبيوتر الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="de4aa-134">The setup might not work if you use the **Try it** option in Azure CLI or if you run the script on your computer.</span></span>

<span data-ttu-id="de4aa-135">اتبع الخطوات التالية لاستخدام البرنامج النصي Windows PowerShell لتكوين Azure.</span><span class="sxs-lookup"><span data-stu-id="de4aa-135">Follow these steps to use the Windows PowerShell script to configure Azure.</span></span> <span data-ttu-id="de4aa-136">يجب أن يكون لديك حقوق بإنشاء مجموعة موارد Azure وموارد Azure وتطبيق Azure AD.</span><span class="sxs-lookup"><span data-stu-id="de4aa-136">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="de4aa-137">للحصول على معلومات حول الأذونات المطلوبة، راجع [التحقق من أذونات Azure AD ](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="de4aa-137">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="de4aa-138">في [مدخل azure ](https://portal.azure.com)، انتقل إلى اشتراك هدف Azure.</span><span class="sxs-lookup"><span data-stu-id="de4aa-138">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span>
2. <span data-ttu-id="de4aa-139">حدد **Cloud Shell** الموجود إلى يمين الحقل **بحث**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-139">Select **Cloud Shell** to the right of the **Search** field.</span></span>
3. <span data-ttu-id="de4aa-140">حدد **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-140">Select **PowerShell**.</span></span>
4. <span data-ttu-id="de4aa-141">قم بإنشاء تخزين، إذا تمت مطالبتك بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="de4aa-141">Create storage if you're prompted to create it.</span></span>
5. <span data-ttu-id="de4aa-142">في علامة التبويب **Azure CLI**، حدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-142">On the **Azure CLI** tab, select **Copy**.</span></span>
6. <span data-ttu-id="de4aa-143">في Notepad (المفكرة)، افتح ملفًا جديدًا، وألصقه في البرنامج النصي لـ Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="de4aa-143">In Notepad, open a new file, and paste in the Windows PowerShell script.</span></span>
7. <span data-ttu-id="de4aa-144">احفظ الملف باسم **ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-144">Save the file as **ConfigureDataLake.ps1**.</span></span>
8. <span data-ttu-id="de4aa-145">قم بتحميل البرنامج النصي Windows PowerShell إلى الجلسة باستخدام خيار القائمة للتحميل في Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="de4aa-145">Upload the Windows PowerShell script to the session by using the menu option for upload in Cloud Shell.</span></span>
9. <span data-ttu-id="de4aa-146">قم بتشغيل البرنامج النصي **.\ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-146">Run the **.\ConfigureDataLake.ps1** script.</span></span>
10. <span data-ttu-id="de4aa-147">اتبع المطالبات لتشغيل البرنامج النصي.</span><span class="sxs-lookup"><span data-stu-id="de4aa-147">Follow the prompts to run the script.</span></span>
11. <span data-ttu-id="de4aa-148">استخدم المعلومات من إخراج البرنامج النصي لتثبيت الوظيفة الإضافية التصدير إلى Data Lake في LCS.</span><span class="sxs-lookup"><span data-stu-id="de4aa-148">Use the information from the script output to install the Export to Data Lake add-in in LCS.</span></span>

### <a name="manual-setup"></a><span data-ttu-id="de4aa-149">إعداد يدوي</span><span class="sxs-lookup"><span data-stu-id="de4aa-149">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="de4aa-150">إضافة التطبيقات إلى المستأجر Azure AD</span><span class="sxs-lookup"><span data-stu-id="de4aa-150">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="de4aa-151">في [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-151">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="de4aa-152">حدد **إدارة \> تطبيقات Enterprise**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-152">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="de4aa-153">ابحث عن التطبيقات التالية حسب معرف التطبيق.</span><span class="sxs-lookup"><span data-stu-id="de4aa-153">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="de4aa-154">استمارة التقديم</span><span class="sxs-lookup"><span data-stu-id="de4aa-154">Application</span></span>                              | <span data-ttu-id="de4aa-155">معرف التطبيق</span><span class="sxs-lookup"><span data-stu-id="de4aa-155">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="de4aa-156">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="de4aa-156">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="de4aa-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="de4aa-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="de4aa-158">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="de4aa-158">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="de4aa-159">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="de4aa-159">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="de4aa-160">خدمة تخويل AI Builder</span><span class="sxs-lookup"><span data-stu-id="de4aa-160">AI Builder Authorization Service</span></span>         | <span data-ttu-id="de4aa-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="de4aa-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="de4aa-162">في حالة تعذر العثور على أي من التطبيقات السابقة، حاول القيام بالخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="de4aa-162">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="de4aa-163">على جهاز الكمبيوتر المحلي، في القائمة **ابدأ**، وابحث عن **powershell**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-163">On your local computer, on the **Start** menu, search for **powershell**.</span></span>
2. <span data-ttu-id="de4aa-164">حدد واستمر في الضغط (أو انقر بزر الماوس الأيمن) **Windows PowerShell**، ثم حدد **تشغيل كمسؤول**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-164">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="de4aa-165">قم بتشغيل الأمر التالي لتثبيت الوحدة النمطية **AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-165">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="de4aa-166">إذا كان موفر NuGet مطلوبًا للمتابعة، حدد **Y** لتثبيته.</span><span class="sxs-lookup"><span data-stu-id="de4aa-166">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="de4aa-167">إذا استلمت رسالة "مستودع غير موثوق به"، حدد **Y** للمتابعة.</span><span class="sxs-lookup"><span data-stu-id="de4aa-167">If you receive an "Untrusted repository" message, select **Y** to continue.</span></span>
6. <span data-ttu-id="de4aa-168">بالنسبة لكل تطبيق يجب إضافته، قم بتشغيل الأوامر التالية لإضافة التطبيق إلى Azure AD.</span><span class="sxs-lookup"><span data-stu-id="de4aa-168">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="de4aa-169">عند المطالبة، قم بتسجيل الدخول كمسؤول Azure AD.</span><span class="sxs-lookup"><span data-stu-id="de4aa-169">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="de4aa-170">إنشاء موارد Azure</span><span class="sxs-lookup"><span data-stu-id="de4aa-170">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="de4aa-171">تأكد من إنشاء الموارد التالية في مثيل Azure AD نفسه الذي يكون داخل البيئة Dataverse.</span><span class="sxs-lookup"><span data-stu-id="de4aa-171">Make sure that you create the following resources in the same Azure AD instance that the Dataverse environment is in.</span></span> <span data-ttu-id="de4aa-172">لا يمكنك استخدام موارد من مثيل Azure AD مختلف.</span><span class="sxs-lookup"><span data-stu-id="de4aa-172">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="de4aa-173">قم بإنشاء حساب تخزين:</span><span class="sxs-lookup"><span data-stu-id="de4aa-173">Create a storage account:</span></span>

    1. <span data-ttu-id="de4aa-174">في [مدخل Azure](https://portal.azure.com)، قم بحساب تخزين.</span><span class="sxs-lookup"><span data-stu-id="de4aa-174">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="de4aa-175">في مربع الحوار **إنشاء حساب تخزين**، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="de4aa-175">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="de4aa-176">**الموقع** – حدد مركز البيانات الذي تقع فيه البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="de4aa-176">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="de4aa-177">**الأداء** – إننا نوصي بأن تقوم بتحديد **قياسي**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-177">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="de4aa-178">**نوع الحساب** – يجب تحديد **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-178">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="de4aa-179">في مربع الحوار **خيارات متقدمة**، بالنسبة للخيار **Data Lake storage Gen2**، حدد **تمكين** ضمن ميزة **مساحات الأسماء الهرمية**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-179">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="de4aa-180">في حالة عدم تمكين هذه الميزة، فإنه لا يمكنك استهلاك البيانات التي يكتبها تطبيق Finance and Operations باستخدام خدمات مثل تدفقات بيانات Power BI.</span><span class="sxs-lookup"><span data-stu-id="de4aa-180">If you don't enable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="de4aa-181">حدد **مراجعة وإنشاء**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-181">Select **Review and create**.</span></span> <span data-ttu-id="de4aa-182">عند اكتمال النشر، يظهر المورد الجديد في مدخل Azure.</span><span class="sxs-lookup"><span data-stu-id="de4aa-182">When the deployment is completed, the new resource is shown in the Azure portal.</span></span>
    5. <span data-ttu-id="de4aa-183">انتقل إلى حساب التخزين الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="de4aa-183">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="de4aa-184">في القائمة اليمنى، حدد **مفاتيح الوصول**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-184">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="de4aa-185">قم بنسخ اسم حساب التخزين وحفظه.</span><span class="sxs-lookup"><span data-stu-id="de4aa-185">Copy and save the name of the storage account.</span></span> <span data-ttu-id="de4aa-186">سيتعين عليك توفير هذه القيمة لاحقًا، عند إعداد أسرار المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="de4aa-186">You will have to provide this value later, when you set up key vault secrets.</span></span>

2. <span data-ttu-id="de4aa-187">إنشاء مخزن رئيسي:</span><span class="sxs-lookup"><span data-stu-id="de4aa-187">Create a key vault:</span></span>

    1. <span data-ttu-id="de4aa-188">في [مدخل Azure](https://portal.azure.com)، قم إنشاء مخزن رئيسي.</span><span class="sxs-lookup"><span data-stu-id="de4aa-188">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="de4aa-189">في مربع الحوار **إنشاء مخزن رئيسي**، في الحقل **الموقع**، حدد مركز البيانات الذي تقع فيه البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="de4aa-189">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="de4aa-190">بعد إنشاء مخزن المفاتيح، انتقل إلى **نظرة عامة حول مخزن مفتاح**، ثم قم بنسخ اسم DNS وحفظه.</span><span class="sxs-lookup"><span data-stu-id="de4aa-190">After key vault is created, go to **Key Vault Overview**, and copy and save the DNS name.</span></span> <span data-ttu-id="de4aa-191">سيتعين عليك توفير هذه القيمة لاحقًا، عند إعداد الوظيفة الإضافية Data Lake.</span><span class="sxs-lookup"><span data-stu-id="de4aa-191">You will have to provide this value later, when you set up the Data Lake add-in.</span></span>

3. <span data-ttu-id="de4aa-192">إنشاء وتسجيل تطبيق Azure AD:</span><span class="sxs-lookup"><span data-stu-id="de4aa-192">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="de4aa-193">في [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**، ثم حدد **عمليات تسجيل التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-193">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="de4aa-194">حدد **تسجيل تطبيق جديد**، ثم قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="de4aa-194">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="de4aa-195">**الاسم** - أدخل اسم التطبيق.</span><span class="sxs-lookup"><span data-stu-id="de4aa-195">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="de4aa-196">**نوع التطبيق** – حدد **API للويب**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-196">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="de4aa-197">**إعادة توجيه إعداد عنوان URI** – أدخل عنوان URL لمثيل Dynamics 365 الخاص بك، مثل `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="de4aa-197">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="de4aa-198">انتقل إلى التطبيق الذي قمت بإنشائه الآن، وقم بنسخ وحفظ قيمة **معرف تطبيق (عميل) الخاصة بالتطبيق**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-198">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="de4aa-199">سيتعين عليك توفير هذه القيمة لاحقًا، عند إعداد أسرار المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="de4aa-199">You will have to provide this value later, when you set up key vault secrets.</span></span>
    4. <span data-ttu-id="de4aa-200">انتقل إلى **أذونات API**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="de4aa-200">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="de4aa-201">حدد **إضافة إذن**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-201">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="de4aa-202">حدد **مخزن Azure رئيسي**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-202">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="de4aa-203">بعد تحديد الأذونات المفوضة، حدد **user\_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-203">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="de4aa-204">حدد **إضافة أذونات**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-204">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="de4aa-205">في القائمة الخاصة بالتطبيق، حدد **الشهادات \& الأسرار**، ثم اتبع الخطوات التالية لإنشاء أسرار المخزن الرئيسي:</span><span class="sxs-lookup"><span data-stu-id="de4aa-205">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="de4aa-206">حدد **سر عميل جديد**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-206">Select **New client secret**.</span></span>
        2. <span data-ttu-id="de4aa-207">في الحقل **الوصف الرئيسي**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="de4aa-207">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="de4aa-208">حدد مدة، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-208">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="de4aa-209">يتم إنشاء سر في الحفل **القيمة**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-209">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="de4aa-210">قم بنسخ القيمة السرية للعميل وحفظها.</span><span class="sxs-lookup"><span data-stu-id="de4aa-210">Copy and save the client secret value.</span></span> <span data-ttu-id="de4aa-211">سيتعين عليك توفير هذه القيمة لاحقًا، عند إعداد أسرار المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="de4aa-211">You will have to provide this value later, when you set up key vault secrets.</span></span>

4. <span data-ttu-id="de4aa-212">إنشاء أسرار المخزن الرئيسي:</span><span class="sxs-lookup"><span data-stu-id="de4aa-212">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="de4aa-213">انتقل إلى المخزن الرئيسي الذي قمت بإنشائه سابقًا، وحدد **الأسرار**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-213">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="de4aa-214">بالنسبة لكل اسم سري في الجدول التالي، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="de4aa-214">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="de4aa-215">حدد **إنشاء/استيراد**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-215">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="de4aa-216">في مربع الحوار **إنشاء سر**، في الحقل **خيارات التحميل**، حدد **يدوي**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-216">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="de4aa-217">قم بإنشاء الاسم السري والقيمة من الجدول.</span><span class="sxs-lookup"><span data-stu-id="de4aa-217">Create the secret name and value from the table.</span></span>
        4. <span data-ttu-id="de4aa-218">حدد **ممكّن‬‬‏‫**، ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-218">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="de4aa-219">يتم إنشاء السر وإضافة إلى مخزن رئيسي.</span><span class="sxs-lookup"><span data-stu-id="de4aa-219">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="de4aa-220">اسم السر</span><span class="sxs-lookup"><span data-stu-id="de4aa-220">Secret name</span></span>                       | <span data-ttu-id="de4aa-221">قيمة سرية</span><span class="sxs-lookup"><span data-stu-id="de4aa-221">Secret value</span></span>                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | <span data-ttu-id="de4aa-222">معرف التطبيق</span><span class="sxs-lookup"><span data-stu-id="de4aa-222">app-id</span></span>                            | <span data-ttu-id="de4aa-223">معرف التطبيق الخاص بالتطبيق الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="de4aa-223">The app ID of the application that you created earlier.</span></span>                                      |
        | <span data-ttu-id="de4aa-224">سر التطبيق</span><span class="sxs-lookup"><span data-stu-id="de4aa-224">app-secret</span></span>                        | <span data-ttu-id="de4aa-225">سر العميل الذي قمت بحفظه مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="de4aa-225">The client secret that you saved earlier.</span></span>                                                    |
        | <span data-ttu-id="de4aa-226">اسم حساب التخزين</span><span class="sxs-lookup"><span data-stu-id="de4aa-226">storage-account-name</span></span>              | <span data-ttu-id="de4aa-227">اسم حساب التخزين الذي قمت بإنشائه مسبقًا، مثل **storageaccount1**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-227">The name of the storage account that you created earlier, such as **storageaccount1**.</span></span>       |

5. <span data-ttu-id="de4aa-228">تخويل التطبيق للوصول إلى المخزن الرئيسي:</span><span class="sxs-lookup"><span data-stu-id="de4aa-228">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="de4aa-229">في [مدخل Azure](https://portal.azure.com)، قم بفتح المخزن الرئيسي الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="de4aa-229">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="de4aa-230">حدد نهج الوصول.</span><span class="sxs-lookup"><span data-stu-id="de4aa-230">Select the access policies.</span></span>
    3. <span data-ttu-id="de4aa-231">بالنسبة لكل تطبيق في الجدول التالي، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="de4aa-231">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="de4aa-232">حدد **إضافة نهج وصول** لإنشاء سياسة وصول.</span><span class="sxs-lookup"><span data-stu-id="de4aa-232">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="de4aa-233">في الحقل **الأذونات السرية**، حدد الأذونات من الجدول.</span><span class="sxs-lookup"><span data-stu-id="de4aa-233">In the **Secret permissions** field, select the permissions from the table.</span></span>
        3. <span data-ttu-id="de4aa-234">في الحقل **تحديد الرئيسي**، ابحث عن اسم عرض التطبيق من الجدول.</span><span class="sxs-lookup"><span data-stu-id="de4aa-234">In the **Select principal** field, search for the application display name from the table.</span></span>
        4. <span data-ttu-id="de4aa-235">حدد **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-235">Select **Select**.</span></span>
        5. <span data-ttu-id="de4aa-236">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-236">Select **Add**.</span></span>
        6. <span data-ttu-id="de4aa-237">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-237">Select **Save**.</span></span>

        | <span data-ttu-id="de4aa-238">استمارة التقديم</span><span class="sxs-lookup"><span data-stu-id="de4aa-238">Application</span></span>                                              | <span data-ttu-id="de4aa-239">الأذونات</span><span class="sxs-lookup"><span data-stu-id="de4aa-239">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="de4aa-240">اسم عرض التطبيق الجديد الذي قمت بإنشائه</span><span class="sxs-lookup"><span data-stu-id="de4aa-240">The display name of the new application that you created</span></span> | <span data-ttu-id="de4aa-241">الحصول على، قائمة</span><span class="sxs-lookup"><span data-stu-id="de4aa-241">Get, List</span></span>   |
        | <span data-ttu-id="de4aa-242">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="de4aa-242">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="de4aa-243">الحصول على، قائمة</span><span class="sxs-lookup"><span data-stu-id="de4aa-243">Get, List</span></span>   |

6. <span data-ttu-id="de4aa-244">قم بتعيين أدوار للوصول إلى حساب التخزين:</span><span class="sxs-lookup"><span data-stu-id="de4aa-244">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="de4aa-245">في [مدخل Azure](https://portal.azure.com)، قم بفتح حساب التخزين الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="de4aa-245">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="de4aa-246">حدد **التحكم في الوصول (IAM)**، ثم حدد **مهمات الأدوار**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-246">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="de4aa-247">حدد **إضافة، أضف مهمة الدور**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-247">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="de4aa-248">بالنسبة لكل تطبيق في الجدول التالي، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="de4aa-248">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="de4aa-249">حدد الدور من الجدول.</span><span class="sxs-lookup"><span data-stu-id="de4aa-249">Select the role from the table.</span></span>
        2. <span data-ttu-id="de4aa-250">اجعل الحقل **تعيين حق الوصول إلى** على مستخدم **Azure AD أو مجموعة أو كيان الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-250">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="de4aa-251">في الحقل **تحديد**، قم بالدخول إلى استمارة التقديم من الجدول.</span><span class="sxs-lookup"><span data-stu-id="de4aa-251">In the **Select** field, enter the application from the table.</span></span>
        4. <span data-ttu-id="de4aa-252">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-252">Select **Save**.</span></span>

        | <span data-ttu-id="de4aa-253">استمارة التقديم</span><span class="sxs-lookup"><span data-stu-id="de4aa-253">Application</span></span>                                              | <span data-ttu-id="de4aa-254">دور</span><span class="sxs-lookup"><span data-stu-id="de4aa-254">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="de4aa-255">اسم عرض التطبيق الجديد الذي قمت بإنشائه</span><span class="sxs-lookup"><span data-stu-id="de4aa-255">The display name of the new application that you created</span></span> | <span data-ttu-id="de4aa-256">المالك</span><span class="sxs-lookup"><span data-stu-id="de4aa-256">Owner</span></span>                       |
        | <span data-ttu-id="de4aa-257">اسم عرض التطبيق الجديد الذي قمت بإنشائه</span><span class="sxs-lookup"><span data-stu-id="de4aa-257">The display name of the new application that you created</span></span> | <span data-ttu-id="de4aa-258">المساهم</span><span class="sxs-lookup"><span data-stu-id="de4aa-258">Contributor</span></span>                 |
        | <span data-ttu-id="de4aa-259">اسم عرض التطبيق الجديد الذي قمت بإنشائه</span><span class="sxs-lookup"><span data-stu-id="de4aa-259">The display name of the new application that you created</span></span> | <span data-ttu-id="de4aa-260">المساهم في حساب التخزين</span><span class="sxs-lookup"><span data-stu-id="de4aa-260">Storage Account Contributor</span></span> |
        | <span data-ttu-id="de4aa-261">اسم عرض التطبيق الجديد الذي قمت بإنشائه</span><span class="sxs-lookup"><span data-stu-id="de4aa-261">The display name of the new application that you created</span></span> | <span data-ttu-id="de4aa-262">مالك بيانات التخزين كبيرة الحجم</span><span class="sxs-lookup"><span data-stu-id="de4aa-262">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="de4aa-263">**خدمة تخويل AI Builder**</span><span class="sxs-lookup"><span data-stu-id="de4aa-263">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="de4aa-264">قارئ بيانات التخزين كبيرة الحجم</span><span class="sxs-lookup"><span data-stu-id="de4aa-264">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="de4aa-265">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="de4aa-265">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}
```
---

## <a name="configure-the-export-to-data-lake-add-in"></a><span data-ttu-id="de4aa-266">تكوين الوظيفة الإضافية التصدير إلى Data Lake</span><span class="sxs-lookup"><span data-stu-id="de4aa-266">Configure the Export to Data Lake add-in</span></span>

<span data-ttu-id="de4aa-267">اتبع الخطوات التالية لاستخدام LCS لإضافة الوظيفة الإضافية التصدير إلى Data Lake إلى البيئة.</span><span class="sxs-lookup"><span data-stu-id="de4aa-267">Follow these steps to use LCS to add the Export to Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="de4aa-268">قم بتسجيل الدخول إلى LCS، ثم، ضمن اسم البيئة على الجانب الأيسر من الصفحة، حدد **تفاصيل كاملة**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-268">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="de4aa-269">في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-269">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="de4aa-270">حدد الوظيفة الإضافية، حدد **تصدير إلى Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-270">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="de4aa-271">أدخل القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="de4aa-271">Enter the following values.</span></span>

    | <span data-ttu-id="de4aa-272">قيمة</span><span class="sxs-lookup"><span data-stu-id="de4aa-272">Value</span></span>                                                              | <span data-ttu-id="de4aa-273">الوصف</span><span class="sxs-lookup"><span data-stu-id="de4aa-273">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="de4aa-274">معرف المستأجر لاشتراك Azure حيث يوجد المخزن الرئيسي</span><span class="sxs-lookup"><span data-stu-id="de4aa-274">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="de4aa-275">يوجد معرف المستأجر الذي يوجد به حساب التخزين والتطبيقات والمخازن الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="de4aa-275">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="de4aa-276">للحصول على هذه القيمة، افتح [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**، ثم انسخ قيمة **معرف المستأجر**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-276">To obtain this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="de4aa-277">توفير اسم DNS لـ Key Vault الخاص بك</span><span class="sxs-lookup"><span data-stu-id="de4aa-277">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="de4aa-278">اسم DNS للمخزن الرئيسي، مثل `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="de4aa-278">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> |
    | <span data-ttu-id="de4aa-279">توفير السر الذي يحتوي على اسم حساب التخزين</span><span class="sxs-lookup"><span data-stu-id="de4aa-279">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="de4aa-280">**اسم حساب التخزين**</span><span class="sxs-lookup"><span data-stu-id="de4aa-280">**storage-account-name**</span></span> |
    | <span data-ttu-id="de4aa-281">اسم السر لمعرف التطبيق الذي سيتم استخدامه للوصول إلى Data Lake</span><span class="sxs-lookup"><span data-stu-id="de4aa-281">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="de4aa-282">**معرف التطبيق**</span><span class="sxs-lookup"><span data-stu-id="de4aa-282">**app-id**</span></span> |
    | <span data-ttu-id="de4aa-283">الاسم السري لسر عميل التطبيق</span><span class="sxs-lookup"><span data-stu-id="de4aa-283">Secret name for App client secret</span></span>                                  | <span data-ttu-id="de4aa-284">**سر التطبيق**</span><span class="sxs-lookup"><span data-stu-id="de4aa-284">**app-secret**</span></span> |

5. <span data-ttu-id="de4aa-285">وافق على الشروط، ثم حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-285">Agree to the terms, and then select **Install**.</span></span>

<span data-ttu-id="de4aa-286">سيتم تثبيت الوظيفة الإضافية خلال بضع دقائق.</span><span class="sxs-lookup"><span data-stu-id="de4aa-286">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-the-finance-insights-add-in"></a><span data-ttu-id="de4aa-287">تكوين ‏الوظيفة الإضافية Finance insights</span><span class="sxs-lookup"><span data-stu-id="de4aa-287">Configure the Finance insights add-in</span></span>

> [!NOTE]
> <span data-ttu-id="de4aa-288">إذا كنت قد قمت بتثبيت الوظيفة الإضافية Get insights مسبقًا، فقم بإزالة تثبيتها قبل إكمال الإجراء التالي.</span><span class="sxs-lookup"><span data-stu-id="de4aa-288">If you previously installed the Get insights add-in, uninstall it before you complete the following procedure.</span></span>

<span data-ttu-id="de4aa-289">اتبع الخطوات التالية لتثبيت الوظيفة الإضافية لـ Finance insights.</span><span class="sxs-lookup"><span data-stu-id="de4aa-289">Follow these steps to install the Finance insights add-in.</span></span>

1. <span data-ttu-id="de4aa-290">قم بتسجيل الدخول إلى LCS، ثم، ضمن اسم البيئة على الجانب الأيسر من الصفحة، حدد **تفاصيل كاملة**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-290">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="de4aa-291">في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-291">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="de4aa-292">حدد الوظيفة الإضافية **Finance insights**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-292">Select the **Finance insights** add-in.</span></span>
4. <span data-ttu-id="de4aa-293">وافق على الشروط، ثم حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="de4aa-293">Agree to the terms, and then select **Install**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="de4aa-294">الملاحظات والدعم</span><span class="sxs-lookup"><span data-stu-id="de4aa-294">Feedback and support</span></span>

<span data-ttu-id="de4aa-295">إذا كنت مهتمًا بتقديم الملاحظات أو تحتاج إلى الدعم، أرسل بريد الكتروني إلى [‏‫Finance insights (إصدار أولي)](mailto:fiap@microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="de4aa-295">If you're interested in providing feedback, or if you require support, send an email to [Finance insights (Preview)](mailto:fiap@microsoft.com).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
