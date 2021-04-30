---
title: تكوين Finance Insights (معاينة)
description: يشرح هذا الموضوع خطوات التكوين التي تتيح لنظامك إمكانية استخدام القدرات المتوفرة في Finance Insights.
author: ShivamPandey-msft
ms.date: 11/25/2020
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
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 54117c009cfeb7307938cc6bd43e774ccfedcfb1
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908820"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="60f9f-103">تكوين Finance insights (معاينة)</span><span class="sxs-lookup"><span data-stu-id="60f9f-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="60f9f-104">تضم Finance insights الوظيفة من Microsoft Dynamics 365 Finance مع Microsoft Dataverse وAzure و AI Builder لتوفير أدوات التنبؤ القوية لمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="60f9f-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="60f9f-105">يشرح هذا الموضوع خطوات التكوين التي تتيح لنظامك إمكانية استخدام القدرات المتوفرة في Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="60f9f-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="60f9f-106">نشر Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="60f9f-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="60f9f-107">نشر البيئات باتباع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="60f9f-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="60f9f-108">في Microsoft Dynamics Lifecycle Services (LCS)، قم بإنشاء أو تحديث بيئة Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="60f9f-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="60f9f-109">تتطلب البيئة تحديث التطبيق النظام الأساسي 10.0.11 إلى الإصدار 35 أو أحدث.</span><span class="sxs-lookup"><span data-stu-id="60f9f-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="60f9f-110">يجب أن تكون البيئة بيئة عالية التوافر (HA) في وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="60f9f-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="60f9f-111">(يُعرف هذا النوع من البيئة أيضًا ببيئة الطبقة 2). لمزيد من المعلومات، راجع [تخطيط البيئة](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="60f9f-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="60f9f-112">إذا كنت تستخدم البيانات التجريبية لشركات Contoso، فإنك ستحتاج إلى بيانات نموذج إضافية لاستخدام ميزات توقعات دفع العميل وتقديرات التدفقات النقدية والتنبؤ بالموازنة.</span><span class="sxs-lookup"><span data-stu-id="60f9f-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="60f9f-113">تكوين Dataverse</span><span class="sxs-lookup"><span data-stu-id="60f9f-113">Configure Dataverse</span></span>

<span data-ttu-id="60f9f-114">يمكنك إكمال خطوات التكوين اليدوي التالية، أو يمكنك تسريع عملية التكوين باستخدام البرنامج النصي Windows PowerShell الذي تم توفيره.</span><span class="sxs-lookup"><span data-stu-id="60f9f-114">You can complete the manual configuration steps that follow, or you can speed up the configuration process by using the Windows PowerShell script that is provided.</span></span> <span data-ttu-id="60f9f-115">عند انتهاء تشغيل البرنامج النصي PowerShell، فإنه سيتم منحك القيم المراد استخدامها لتكوين Finance insights.</span><span class="sxs-lookup"><span data-stu-id="60f9f-115">When the PowerShell script has finished running, it will give you values to use to configure Finance insights.</span></span> 

> [!NOTE]
> <span data-ttu-id="60f9f-116">افتح PowerShell على الكمبيوتر لتشغيل البرنامج النصي.</span><span class="sxs-lookup"><span data-stu-id="60f9f-116">Open PowerShell on your PC to run the script.</span></span> <span data-ttu-id="60f9f-117">قد تحتاج إلى الإصدار 5 من PowerShell.</span><span class="sxs-lookup"><span data-stu-id="60f9f-117">You may need PowerShell version 5.</span></span> <span data-ttu-id="60f9f-118">قد لا يعمل الخيار Microsoft Azure CLI "جربه".</span><span class="sxs-lookup"><span data-stu-id="60f9f-118">The Microsoft Azure CLI "Try it" option may not work.</span></span>

# <a name="manual-configuration-steps"></a>[<span data-ttu-id="60f9f-119">خطوات التكوين اليدوي</span><span class="sxs-lookup"><span data-stu-id="60f9f-119">Manual configuration steps</span></span>](#tab/configuration-steps)

1. <span data-ttu-id="60f9f-120">افتح مركز الإدارة [Power Platform ](https://admin.powerplatform.microsoft.com/)، واتبع هذه الخطوات لإنشاء بيئة Dataverse جديدة في مستأجر خدمة Active Directory نفسه.</span><span class="sxs-lookup"><span data-stu-id="60f9f-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="60f9f-121">افتح صفحة **البيئات**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-121">Open the **Environments** page.</span></span>

        <span data-ttu-id="60f9f-122">[![صفحة البيئات](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="60f9f-122">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="60f9f-123">حدد **بيئة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-123">Select **New environment**.</span></span>
    3. <span data-ttu-id="60f9f-124">في الحقل **نوع**، حدد **وضع الحماية**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-124">In the **Type** field, select **Sandbox**.</span></span>
    4. <span data-ttu-id="60f9f-125">عيّن الخيار **إنشاء قاعدة بيانات** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-125">Set the **Create Database** option to **Yes**.</span></span>
    5. <span data-ttu-id="60f9f-126">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-126">Select **Next**.</span></span>
    6. <span data-ttu-id="60f9f-127">حدد اللغة والعملة الخاصة بمؤسسك.</span><span class="sxs-lookup"><span data-stu-id="60f9f-127">Select the language and currency for your organization.</span></span>
    7. <span data-ttu-id="60f9f-128">اقبل القيم الافتراضية للحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="60f9f-128">Accept the default values for the other fields.</span></span>
    8. <span data-ttu-id="60f9f-129">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-129">Select **Save**.</span></span>
    9. <span data-ttu-id="60f9f-130">حدّث صفحة **البيئات**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-130">Refresh the **Environments** page.</span></span>
    10. <span data-ttu-id="60f9f-131">انتظر حتى يتم تحديث قيمة الحقل **الحالة** إلى **جاهز**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-131">Wait until the value of the **State** field is updated to **Ready**.</span></span>
    11. <span data-ttu-id="60f9f-132">دوِّن ملاحظة بمُعرف المؤسسة Dataverse.</span><span class="sxs-lookup"><span data-stu-id="60f9f-132">Make a note of the Dataverse organization ID.</span></span>
    12. <span data-ttu-id="60f9f-133">حدد البيئة المراد نسخها، ثم حدد **إعدادات**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-133">Select the environment, and then select **Settings**.</span></span>
    13. <span data-ttu-id="60f9f-134">حدد **الموارد \> كافة الإعدادات القديمة**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-134">Select **Resources \> All Legacy Settings**.</span></span>
    14. <span data-ttu-id="60f9f-135">في شريط التنقل العلوي، حدد **الإعدادات**، ثم حدد **التخصيصات**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-135">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    15. <span data-ttu-id="60f9f-136">حدد **موارد المطور**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-136">Select **Developer Resources**.</span></span>
    16. <span data-ttu-id="60f9f-137">انسخ قيمة **معرف مؤسسة Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-137">Copy the **Dataverse organization ID** value.</span></span>
    17. <span data-ttu-id="60f9f-138">في شريط العنوان الخاص بالمستعرض، قم بتسجيل عنوان URL الخاص بمؤسسة Dataverse.</span><span class="sxs-lookup"><span data-stu-id="60f9f-138">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="60f9f-139">على سبيل المثال، قد يكون عنوان URL `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="60f9f-139">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

2. <span data-ttu-id="60f9f-140">إذا كنت تخطط لاستخدام ميزة تقديرات التدفقات النقدية أو التنبؤ بالموازنة، اتبع الخطوات التالية لتحديث حد التعليق التوضيحي لمؤسسك إلى 50 ميغابايت على الأقل (MB):</span><span class="sxs-lookup"><span data-stu-id="60f9f-140">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="60f9f-141">افتح [مدخل Power Apps](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="60f9f-141">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="60f9f-142">حدد البيئة التي قمت بإنشائها للتو، ثم حدد **الإعدادات المتقدمة**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-142">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="60f9f-143">حدد **إعدادات \> تكوين البريد الإلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-143">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="60f9f-144">قم بتغيير قيمة الحقل **الحد الأقصى حجم الملف** إلى **51.200**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-144">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="60f9f-145">(ويتم التعبير عن القيمة بالكيلو بايت \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="60f9f-145">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="60f9f-146">حدد **موافق** لحفظ التغييرات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="60f9f-146">Select **OK** to save your changes.</span></span>

# <a name="windows-powershell-configuration-script"></a>[<span data-ttu-id="60f9f-147">برنامج التكوين النصي لـ Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="60f9f-147">Windows PowerShell configuration script</span></span>](#tab/powershell-configuration-script)

```azurecli-interactive
Write-Output 'The following modules need to be present for execution of this script:'
Write-Output '  Microsoft.PowerApps.Administration.PowerShell'
Write-Output '  Microsoft.PowerApps.PowerShell'
Write-Output '  Microsoft.Xrm.Tooling.CrmConnector.PowerShell'

try {
    $moduleConsent = Read-Host 'Is it ok to install or update these modules as needed? (yes/no)'
    if ($moduleConsent -ne 'yes' -and $moduleConsent -ne 'y') {
        Write-Warning 'User declined to install required modules.'
        return
    }

    $module = 'Microsoft.PowerApps.Administration.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '2.0.61' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '2.0.61' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.PowerApps.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '1.0.9' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '1.0.9' -AllowClobber -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.Xrm.Tooling.CrmConnector.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '3.3.0.892' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '3.3.0.892' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    Write-Output '================================================================================='

    $useMfa = $false
    $useMfaPrompt = Read-Host "Does your organization require the use of multi-factor authentication? (yes/no)"
    if ($useMfaPrompt -eq 'yes' -or $useMfaPrompt -eq 'y') {
        $useMfa = $true
    }
    if(-not $useMfa) {
        $credential = Get-Credential -Message 'Power Apps Credential'
    }

    $orgFriendlyName = Read-Host "Enter the name of the CDS Organization to use or create: (blank for 'FinanceInsightsOrg')"
    if ($orgFriendlyName.Trim() -eq '') {
        $orgFriendlyName = 'FinanceInsightsOrg'
    }

    $isDefaultOrgPrompt = Read-Host ("Is '" + $orgFriendlyName + "' the default organization for your tenant? (yes/no)")
    if ($isDefaultOrgPrompt -eq 'yes' -or $isDefaultOrgPrompt -eq 'y') {
        $isDefaultOrg = $true
    }

    if ($credential) {
        Add-PowerAppsAccount -Username $credential.UserName -Password $credential.Password
    }
    else {
        Add-PowerAppsAccount
    }

    if ($isDefaultOrg) {
        $orgMatch = ('(default)')
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { $_.IsDefault -eq $true })
    }
    else {
        $orgMatch = ('{0} (*)' -f $orgFriendlyName)
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.IsDefault -eq $false -and ($_.DisplayName -eq $orgFriendlyName -or $_.DisplayName -like $orgMatch)) })
    }

    $getCrmOrgParams = @{ 'OnlineType' = 'Office365' }
    if ($credential) {
        $getCrmOrgParams.Credential = $credential
    }

    if ($null -eq $environment) {
        Write-Output '================================================================================='
        Write-Output 'PowerApps environment not found. A new one will be provisioned.'

        $invalid = 'invalid'

        $location = $invalid
        $cdsLocations = (Get-AdminPowerAppEnvironmentLocations | Select-Object LocationName).LocationName
        while (-not ($location -in $cdsLocations)) {
            $location = (Read-Host -Prompt "Enter the location in which to create the new PowerApps environment: ('help' to see values)")
            if ($location -eq 'help') {
                $cdsLocations
            }
        }

        $currency = $invalid
        $cdsCurrencies = (Get-AdminPowerAppCdsDatabaseCurrencies -Location $location | Select-Object CurrencyName).CurrencyName
        while ($currency -ne '' -and -not ($currency -in $cdsCurrencies)) {
            $currency = (Read-Host -Prompt "Enter the currency to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($currency -eq 'help') {
                $cdsCurrencies
            }
        }

        $language = $invalid
        $cdsLanguages = (Get-AdminPowerAppCdsDatabaseLanguages -Location $location | Select-Object LanguageName, LanguageDisplayName)
        while ($language -ne '' -and -not ($language -in $cdsLanguages.LanguageName)) {
            $language = (Read-Host -Prompt "Enter the language name to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($language -eq 'help') {
                $cdsLanguages | Format-Table -Property LanguageName, LanguageDisplayName
            }
        }

        Write-Output 'Provisioning PowerApps environment. This may take several minutes.'

        $sleep = 15

        $envParams = @{ 'DisplayName' = $orgFriendlyName; 'EnvironmentSku' = 'Sandbox'; 'ProvisionDatabase' = $true; 'Location' = $location; 'WaitUntilFinished' = $true }
        if ($language.Trim() -ne '') {
            $envParams.LanguageName = $language
        }
        if ($currency.Trim() -ne '') {
            $envParams.CurrencyName = $currency
        }
        $newEnvResult = New-AdminPowerAppEnvironment @envParams
        if (($null -eq $newEnvResult) -or ($newEnvResult.CommonDataServiceDatabaseProvisioningState -ne 'Succeeded')) {
            Write-Warning 'Failed to create to PowerApps environment'
            if ($null -ne $newEnvResult) {
                $newEnvResult
            }
        }
        else {
            $environment = $null
            $retryCount = 0
            while (($null -eq $environment) -and ($retryCount -lt 5)) {
                Start-Sleep -Seconds $sleep
                $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.DisplayName -like $orgMatch) })
            }
            Write-Output ("Provisioned PowerApps environment with name: '" + $environment.DisplayName + "'")
        }

        Write-Output 'Waiting for CDS organization provisioning. This may take several minutes.'
        if (-not $credential) {
            $sleep = 120
            Write-Output 'You may be prompted for credentials multiple times while checking the status of the provisioning.'
        }

        while ($null -eq $crmOrg) {
            Start-Sleep -Seconds $sleep
            $crmOrg = (Get-CrmOrganizations @getCrmOrgParams) | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }
    else {
        $crmOrgs = Get-CrmOrganizations @getCrmOrgParams
        if ($UseDefaultOrganization -eq $true) {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -match $orgMatch }
        }
        else {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }

    Write-Output '================================================================================='
    Write-Output 'Values for PowerAI LCS Add-In:'
    Write-Output ("  CDS organization url:             " + $crmOrg.WebApplicationUrl)
    Write-Output ("  CDS organization ID:              " + $crmOrg.OrganizationId)
}
catch {
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $_.Exception.InnerException
    while ($null -ne $inner) {
        Write-Output 'Inner Exception:'
        Write-Error $_.Exception.Message
        Write-Warning $_.Exception.StackTrace
        $inner = $inner.InnerException
    }
}
```
---

## <a name="configure-the-azure-setup"></a><span data-ttu-id="60f9f-148">تكوين إعداد Azure</span><span class="sxs-lookup"><span data-stu-id="60f9f-148">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="60f9f-149">أدخل معرف الدليل Dataverse ومعرف الكائن الخاص بمستخدم Azure AD</span><span class="sxs-lookup"><span data-stu-id="60f9f-149">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="60f9f-150">أدخل مُعرف الدليل Dataverse:</span><span class="sxs-lookup"><span data-stu-id="60f9f-150">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="60f9f-151">افتح [مدخل Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="60f9f-151">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="60f9f-152">قم بتسجيل الدخول باستخدام معرف المستخدم الذي تم استخدامه لإنشاء البيئة Dataverse.</span><span class="sxs-lookup"><span data-stu-id="60f9f-152">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="60f9f-153">الانتقال إلى **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-153">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="60f9f-154">انسخ قيمة **معرف المستأجر**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-154">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="60f9f-155">أدخل معرف كائن Azure Active Directory (Azure AD):</span><span class="sxs-lookup"><span data-stu-id="60f9f-155">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="60f9f-156">في [مدخل Azure](https://portal.azure.com)، انتقل إلى **المستخدمين**، وابحث عن المستخدم بعنوان البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="60f9f-156">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="60f9f-157">حدد اسم المستخدم.</span><span class="sxs-lookup"><span data-stu-id="60f9f-157">Select the user's name.</span></span>
    3. <span data-ttu-id="60f9f-158">انسخ قيمة **معرف الكائن**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-158">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="60f9f-159">استخدام Azure Cloud Shell لإعداد موارد Finance insights Data Lake</span><span class="sxs-lookup"><span data-stu-id="60f9f-159">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="60f9f-160">استخدم البرنامج النصي لـ Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="60f9f-160">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="60f9f-161">لقد تم توفير برنامج Windows PowerShell النصي، حتى يمكنك بسهولة إعداد موارد Azure الموضحة في [تكوين التصدير إلى Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="60f9f-161">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="60f9f-162">إذا كنت تفضل القيام بالإعداد اليدوي، فعليك تخطي هذا الإجراء، ومتابعة الإجراء في القسم [الإعداد اليدوي](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="60f9f-162">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="60f9f-163">اتبع الخطوات التالية لتشغيل البرنامج النصي PowerShell.</span><span class="sxs-lookup"><span data-stu-id="60f9f-163">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="60f9f-164">قد لا يعمل الخيار Azure CLI "جربه"، أو تشغيل البرنامج النصي على الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="60f9f-164">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="60f9f-165">اتبع الخطوات التالية لتكوين Azure باستخدام البرنامج النصي لـ Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="60f9f-165">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="60f9f-166">يجب أن يكون لديك حقوق بإنشاء مجموعة موارد Azure وموارد Azure وتطبيق Azure AD.</span><span class="sxs-lookup"><span data-stu-id="60f9f-166">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="60f9f-167">للحصول على معلومات حول الأذونات المطلوبة، راجع [التحقق من أذونات Azure AD ](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="60f9f-167">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="60f9f-168">في [مدخل azure ](https://portal.azure.com)، انتقل إلى اشتراك هدف Azure.</span><span class="sxs-lookup"><span data-stu-id="60f9f-168">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="60f9f-169">حدد الزر **Cloud Shell** الموجود إلى يمين الحقل **بحث**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-169">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="60f9f-170">حدد **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-170">Select **PowerShell**.</span></span>
3. <span data-ttu-id="60f9f-171">قم بإنشاء تخزين، إذا تمت مطالبتك بالقيام بذلك.</span><span class="sxs-lookup"><span data-stu-id="60f9f-171">Create storage, if you're prompted to do so.</span></span> <span data-ttu-id="60f9f-172">ثم قم بتحميل البرنامج النصي لـ Windows PowerShell إلى جلسة العمل.</span><span class="sxs-lookup"><span data-stu-id="60f9f-172">Then upload the Windows PowerShell script to the session.</span></span>
4. <span data-ttu-id="60f9f-173">قم بتشغيل البرنامج النصي.</span><span class="sxs-lookup"><span data-stu-id="60f9f-173">Run the script.</span></span>
5. <span data-ttu-id="60f9f-174">اتبع المطالبات لتشغيل البرنامج النصي.</span><span class="sxs-lookup"><span data-stu-id="60f9f-174">Follow the prompts to run the script.</span></span>
6. <span data-ttu-id="60f9f-175">استخدم المعلومات من إخراج البرنامج النصي لتثبيت الوظيفة الإضافية **التصدير إلى Data Lake** في LCS.</span><span class="sxs-lookup"><span data-stu-id="60f9f-175">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
7. <span data-ttu-id="60f9f-176">استخدم المعلومات من إخراج البرنامج النصي لتمكين مخزن الكيان في الصفحة **اتصالات البيانات** في Finance (**إدارة النظام \> معلمات النظام \> اتصالات البيانات**).</span><span class="sxs-lookup"><span data-stu-id="60f9f-176">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="60f9f-177">إعداد يدوي</span><span class="sxs-lookup"><span data-stu-id="60f9f-177">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="60f9f-178">إضافة التطبيقات إلى المستأجر Azure AD</span><span class="sxs-lookup"><span data-stu-id="60f9f-178">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="60f9f-179">في [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-179">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="60f9f-180">حدد **إدارة \> تطبيقات Enterprise**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-180">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="60f9f-181">ابحث عن التطبيقات التالية حسب معرف التطبيق.</span><span class="sxs-lookup"><span data-stu-id="60f9f-181">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="60f9f-182">استمارة التقديم</span><span class="sxs-lookup"><span data-stu-id="60f9f-182">Application</span></span>                              | <span data-ttu-id="60f9f-183">معرف التطبيق</span><span class="sxs-lookup"><span data-stu-id="60f9f-183">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="60f9f-184">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="60f9f-184">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="60f9f-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="60f9f-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="60f9f-186">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="60f9f-186">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="60f9f-187">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="60f9f-187">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="60f9f-188">خدمة تخويل AI Builder</span><span class="sxs-lookup"><span data-stu-id="60f9f-188">AI Builder Authorization Service</span></span>         | <span data-ttu-id="60f9f-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="60f9f-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="60f9f-190">في حالة تعذر العثور على أي من التطبيقات السابقة، حاول القيام بالخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="60f9f-190">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="60f9f-191">على جهازك المحلي، حدد القائمة **ابدأ**، وابحث عن **powershell**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-191">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="60f9f-192">حدد واستمر في الضغط (أو انقر بزر الماوس الأيمن) **Windows PowerShell**، ثم حدد **تشغيل كمسؤول**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-192">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="60f9f-193">قم بتشغيل الأمر التالي لتثبيت الوحدة النمطية **AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-193">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="60f9f-194">إذا كان موفر NuGet مطلوبًا للمتابعة، حدد **Y** لتثبيته.</span><span class="sxs-lookup"><span data-stu-id="60f9f-194">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="60f9f-195">إذا ظهرت رسالة "مستودع غير موثوق به"، حدد **Y** للمتابعة.</span><span class="sxs-lookup"><span data-stu-id="60f9f-195">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="60f9f-196">بالنسبة لكل تطبيق يجب إضافته، قم بتشغيل الأوامر التالية لإضافة التطبيق إلى Azure AD.</span><span class="sxs-lookup"><span data-stu-id="60f9f-196">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="60f9f-197">عند المطالبة، قم بتسجيل الدخول كمسؤول Azure AD.</span><span class="sxs-lookup"><span data-stu-id="60f9f-197">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="60f9f-198">إنشاء موارد Azure</span><span class="sxs-lookup"><span data-stu-id="60f9f-198">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="60f9f-199">تأكد من إنشاء الموارد التالية في مثيل Azure AD نفسه كبيئة Dataverse.</span><span class="sxs-lookup"><span data-stu-id="60f9f-199">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="60f9f-200">لا يمكنك استخدام موارد من مثيل Azure AD مختلف.</span><span class="sxs-lookup"><span data-stu-id="60f9f-200">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="60f9f-201">قم بإنشاء حساب تخزين جديد:</span><span class="sxs-lookup"><span data-stu-id="60f9f-201">Create a new storage account:</span></span>

    1. <span data-ttu-id="60f9f-202">في [مدخل Azure](https://portal.azure.com)، قم بحساب تخزين.</span><span class="sxs-lookup"><span data-stu-id="60f9f-202">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="60f9f-203">في مربع الحوار **إنشاء حساب تخزين**، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="60f9f-203">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="60f9f-204">**الموقع** – حدد مركز البيانات الذي تقع فيه البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="60f9f-204">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="60f9f-205">**الأداء** – إننا نوصي بأن تقوم بتحديد **قياسي**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-205">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="60f9f-206">**نوع الحساب** – يجب تحديد **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-206">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="60f9f-207">في مربع الحوار **خيارات متقدمة**، بالنسبة للخيار **Data Lake storage Gen2**، حدد **تمكين** ضمن ميزة **مساحات الأسماء الهرمية**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-207">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="60f9f-208">في حالة تعطيل هذه الميزة، فإنه لا يمكنك استهلاك البيانات التي يكتبها تطبيق Finance and Operations باستخدام خدمات مثل تدفقات بيانات Power BI.</span><span class="sxs-lookup"><span data-stu-id="60f9f-208">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="60f9f-209">حدد **مراجعة وإنشاء**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-209">Select **Review and create**.</span></span> <span data-ttu-id="60f9f-210">عند اكتمال النشر، سيظهر المورد الجديد في مدخل Azure.</span><span class="sxs-lookup"><span data-stu-id="60f9f-210">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="60f9f-211">انتقل إلى حساب التخزين الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="60f9f-211">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="60f9f-212">في القائمة اليمنى، حدد **مفاتيح الوصول**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-212">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="60f9f-213">قم بنسخ سلسلة الاتصال وحفظها إما إلى **Key1** أو **Key2**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-213">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="60f9f-214">قم بنسخ اسم حساب التخزين وحفظه.</span><span class="sxs-lookup"><span data-stu-id="60f9f-214">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="60f9f-215">إنشاء مخزن رئيسي جديد:</span><span class="sxs-lookup"><span data-stu-id="60f9f-215">Create a new key vault:</span></span>

    1. <span data-ttu-id="60f9f-216">في [مدخل Azure](https://portal.azure.com)، قم إنشاء مخزن رئيسي.</span><span class="sxs-lookup"><span data-stu-id="60f9f-216">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="60f9f-217">في مربع الحوار **إنشاء مخزن رئيسي**، في الحقل **الموقع**، حدد مركز البيانات الذي تقع فيه البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="60f9f-217">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="60f9f-218">بعد إنشاء مخزن رئيسي، حدده في القائمة، ثم حدد **الأسرار**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-218">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="60f9f-219">حدد **إنشاء/استيراد**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-219">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="60f9f-220">في مربع الحوار **إنشاء سر**، في الحقل **خيارات التحميل**، حدد **يدوي**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-220">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="60f9f-221">أدخل اسمًا للسر.</span><span class="sxs-lookup"><span data-stu-id="60f9f-221">Enter a name for the secret.</span></span> <span data-ttu-id="60f9f-222">قم بتدوين الاسم، لأنه سيتعين عليك توفيره لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="60f9f-222">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="60f9f-223">في الحقل **القيمة**، أدخل سلسلة الاتصال التي حصلت عليها من حساب التخزين في الإجراء السابق.</span><span class="sxs-lookup"><span data-stu-id="60f9f-223">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="60f9f-224">حدد **ممكّن‬‬‏‫**، ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-224">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="60f9f-225">يتم إنشاء السر وإضافة إلى مخزن رئيسي.</span><span class="sxs-lookup"><span data-stu-id="60f9f-225">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="60f9f-226">انتقل إلى **نظرة عامة حول مخزن رئيسي**، وقم بتدوين اسم DNS.</span><span class="sxs-lookup"><span data-stu-id="60f9f-226">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="60f9f-227">إنشاء وتسجيل تطبيق Azure AD:</span><span class="sxs-lookup"><span data-stu-id="60f9f-227">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="60f9f-228">في [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**، ثم حدد **عمليات تسجيل التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-228">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="60f9f-229">حدد **تسجيل تطبيق جديد**، ثم قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="60f9f-229">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="60f9f-230">**الاسم** - أدخل اسم التطبيق.</span><span class="sxs-lookup"><span data-stu-id="60f9f-230">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="60f9f-231">**نوع التطبيق** – حدد **API للويب**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-231">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="60f9f-232">**إعادة توجيه إعداد عنوان URI** – أدخل عنوان URL لمثيل Dynamics 365 الخاص بك، مثل، `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="60f9f-232">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="60f9f-233">انتقل إلى التطبيق الذي قمت بإنشائه الآن، وقم بنسخ وحفظ قيمة **معرف تطبيق (عميل) الخاصة بالتطبيق**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-233">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="60f9f-234">سيتعين عليك توفير هذه القيمة لاحقًا، عند إعداد المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="60f9f-234">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="60f9f-235">انتقل إلى **أذونات API**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="60f9f-235">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="60f9f-236">حدد **إضافة إذن**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-236">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="60f9f-237">حدد **مخزن Azure رئيسي**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-237">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="60f9f-238">بعد تحديد الأذونات المفوضة، حدد **user\_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-238">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="60f9f-239">حدد **إضافة أذونات**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-239">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="60f9f-240">في القائمة الخاصة بالتطبيق، حدد **الشهادات \& الأسرار**، ثم اتبع الخطوات التالية لإنشاء أسرار المخزن الرئيسي:</span><span class="sxs-lookup"><span data-stu-id="60f9f-240">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="60f9f-241">حدد **سر عميل جديد**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-241">Select **New client secret**.</span></span>
        2. <span data-ttu-id="60f9f-242">في الحقل **الوصف الرئيسي**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="60f9f-242">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="60f9f-243">حدد مدة، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-243">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="60f9f-244">يتم إنشاء سر في الحفل **القيمة**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-244">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="60f9f-245">قم بنسخ القيمة السرية وحفظها.</span><span class="sxs-lookup"><span data-stu-id="60f9f-245">Copy and save the secret value.</span></span>

4. <span data-ttu-id="60f9f-246">إنشاء أسرار المخزن الرئيسي:</span><span class="sxs-lookup"><span data-stu-id="60f9f-246">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="60f9f-247">انتقل إلى المخزن الرئيسي الذي قمت بإنشائه سابقًا، وحدد **الأسرار**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-247">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="60f9f-248">بالنسبة لكل اسم سري في الجدول التالي، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="60f9f-248">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="60f9f-249">حدد **إنشاء/استيراد**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-249">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="60f9f-250">في مربع الحوار **إنشاء سر**، في الحقل **خيارات التحميل**، حدد **يدوي**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-250">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="60f9f-251">قم بإنشاء الاسم السري والقيمة من الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="60f9f-251">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="60f9f-252">حدد **ممكّن‬‬‏‫**، ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-252">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="60f9f-253">يتم إنشاء السر وإضافة إلى مخزن رئيسي.</span><span class="sxs-lookup"><span data-stu-id="60f9f-253">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="60f9f-254">اسم السر</span><span class="sxs-lookup"><span data-stu-id="60f9f-254">Secret name</span></span>                       | <span data-ttu-id="60f9f-255">قيمة سرية</span><span class="sxs-lookup"><span data-stu-id="60f9f-255">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="60f9f-256">معرف التطبيق</span><span class="sxs-lookup"><span data-stu-id="60f9f-256">app-id</span></span>                            | <span data-ttu-id="60f9f-257">معرف التطبيق الخاص بالتطبيق الذي قمت بإنشائه سابقًا</span><span class="sxs-lookup"><span data-stu-id="60f9f-257">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="60f9f-258">سر التطبيق</span><span class="sxs-lookup"><span data-stu-id="60f9f-258">app-secret</span></span>                        | <span data-ttu-id="60f9f-259">سر العميل الذي قمت بحفظه مسبقًا</span><span class="sxs-lookup"><span data-stu-id="60f9f-259">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="60f9f-260">اسم حساب التخزين</span><span class="sxs-lookup"><span data-stu-id="60f9f-260">storage-account-name</span></span>              | <span data-ttu-id="60f9f-261">اسم حساب التخزين الذي قمت بإنشائه مسبقًا، مثل **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="60f9f-261">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="60f9f-262">التخزين-الحساب-الاتصال-السلسلة</span><span class="sxs-lookup"><span data-stu-id="60f9f-262">storage-account-connection-string</span></span> | <span data-ttu-id="60f9f-263">سلسلة الاتصال التي قمت بنسخها من الصفحة **مفاتيح الوصول** لحساب التخزين</span><span class="sxs-lookup"><span data-stu-id="60f9f-263">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="60f9f-264">تخويل التطبيق للوصول إلى المخزن الرئيسي:</span><span class="sxs-lookup"><span data-stu-id="60f9f-264">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="60f9f-265">في [مدخل Azure](https://portal.azure.com)، قم بفتح المخزن الرئيسي الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="60f9f-265">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="60f9f-266">حدد نهج الوصول.</span><span class="sxs-lookup"><span data-stu-id="60f9f-266">Select the access policies.</span></span>
    3. <span data-ttu-id="60f9f-267">بالنسبة لكل تطبيق في الجدول التالي، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="60f9f-267">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="60f9f-268">حدد **إضافة نهج وصول** لإنشاء سياسة وصول.</span><span class="sxs-lookup"><span data-stu-id="60f9f-268">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="60f9f-269">في الحقل **الأذونات السرية**، حدد الأذونات من الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="60f9f-269">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="60f9f-270">في الحقل **تحديد الرئيسي**، ابحث عن اسم عرض التطبيق من الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="60f9f-270">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="60f9f-271">حدد **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-271">Select **Select**.</span></span>
        5. <span data-ttu-id="60f9f-272">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-272">Select **Add**.</span></span>
        6. <span data-ttu-id="60f9f-273">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-273">Select **Save**.</span></span>

        | <span data-ttu-id="60f9f-274">استمارة التقديم</span><span class="sxs-lookup"><span data-stu-id="60f9f-274">Application</span></span>                                              | <span data-ttu-id="60f9f-275">الأذونات</span><span class="sxs-lookup"><span data-stu-id="60f9f-275">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="60f9f-276">اسم عرض التطبيق الجديد الذي قمت بإنشائه</span><span class="sxs-lookup"><span data-stu-id="60f9f-276">The display name of the new application that you created</span></span> | <span data-ttu-id="60f9f-277">الحصول على، قائمة</span><span class="sxs-lookup"><span data-stu-id="60f9f-277">Get, List</span></span>   |
        | <span data-ttu-id="60f9f-278">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="60f9f-278">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="60f9f-279">الحصول على، قائمة</span><span class="sxs-lookup"><span data-stu-id="60f9f-279">Get, List</span></span>   |

6. <span data-ttu-id="60f9f-280">قم بتعيين أدوار للوصول إلى حساب التخزين:</span><span class="sxs-lookup"><span data-stu-id="60f9f-280">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="60f9f-281">في [مدخل Azure](https://portal.azure.com)، قم بفتح حساب التخزين الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="60f9f-281">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="60f9f-282">حدد **التحكم في الوصول (IAM)**، ثم حدد **مهمات الأدوار**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-282">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="60f9f-283">حدد **إضافة، أضف مهمة الدور**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-283">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="60f9f-284">بالنسبة لكل تطبيق في الجدول التالي، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="60f9f-284">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="60f9f-285">حدد الدور من الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="60f9f-285">Select the role from the following table.</span></span>
        2. <span data-ttu-id="60f9f-286">اجعل الحقل **تعيين حق الوصول إلى** على مستخدم **Azure AD أو مجموعة أو كيان الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-286">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="60f9f-287">في الحقل **تحديد**، قم بالدخول إلى استمارة التقديم من الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="60f9f-287">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="60f9f-288">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-288">Select **Save**.</span></span>

        | <span data-ttu-id="60f9f-289">استمارة التقديم</span><span class="sxs-lookup"><span data-stu-id="60f9f-289">Application</span></span>                                              | <span data-ttu-id="60f9f-290">دور</span><span class="sxs-lookup"><span data-stu-id="60f9f-290">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="60f9f-291">اسم عرض التطبيق الجديد الذي قمت بإنشائه</span><span class="sxs-lookup"><span data-stu-id="60f9f-291">The display name of the new application that you created</span></span> | <span data-ttu-id="60f9f-292">المالك</span><span class="sxs-lookup"><span data-stu-id="60f9f-292">Owner</span></span>                       |
        | <span data-ttu-id="60f9f-293">اسم عرض التطبيق الجديد الذي قمت بإنشائه</span><span class="sxs-lookup"><span data-stu-id="60f9f-293">The display name of the new application that you created</span></span> | <span data-ttu-id="60f9f-294">المساهم</span><span class="sxs-lookup"><span data-stu-id="60f9f-294">Contributor</span></span>                 |
        | <span data-ttu-id="60f9f-295">اسم عرض التطبيق الجديد الذي قمت بإنشائه</span><span class="sxs-lookup"><span data-stu-id="60f9f-295">The display name of the new application that you created</span></span> | <span data-ttu-id="60f9f-296">المساهم في حساب التخزين</span><span class="sxs-lookup"><span data-stu-id="60f9f-296">Storage Account Contributor</span></span> |
        | <span data-ttu-id="60f9f-297">اسم عرض التطبيق الجديد الذي قمت بإنشائه</span><span class="sxs-lookup"><span data-stu-id="60f9f-297">The display name of the new application that you created</span></span> | <span data-ttu-id="60f9f-298">مالك بيانات التخزين كبيرة الحجم</span><span class="sxs-lookup"><span data-stu-id="60f9f-298">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="60f9f-299">**خدمة تخويل AI Builder**</span><span class="sxs-lookup"><span data-stu-id="60f9f-299">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="60f9f-300">قارئ بيانات التخزين كبيرة الحجم</span><span class="sxs-lookup"><span data-stu-id="60f9f-300">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="60f9f-301">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="60f9f-301">Azure CLI</span></span>](#tab/azure-azure-cli)

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



## <a name="configure-the-data-lake"></a><span data-ttu-id="60f9f-302">تكوين data lake</span><span class="sxs-lookup"><span data-stu-id="60f9f-302">Configure the data lake</span></span>

<span data-ttu-id="60f9f-303">اتبع الخطوات التالية لاستخدام LCS لإضافة الوظيفة الإضافية Azure Data Lake add-in إلى البيئة.</span><span class="sxs-lookup"><span data-stu-id="60f9f-303">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="60f9f-304">قم بتسجيل الدخول إلى LCS، ثم، ضمن اسم البيئة على الجانب الأيسر من الصفحة، حدد **تفاصيل كاملة**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-304">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="60f9f-305">في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-305">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="60f9f-306">حدد الوظيفة الإضافية، حدد **تصدير إلى Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-306">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="60f9f-307">أدخل القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="60f9f-307">Enter the following values.</span></span>

    | <span data-ttu-id="60f9f-308">قيمة</span><span class="sxs-lookup"><span data-stu-id="60f9f-308">Value</span></span>                                                              | <span data-ttu-id="60f9f-309">الوصف</span><span class="sxs-lookup"><span data-stu-id="60f9f-309">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="60f9f-310">معرف المستأجر لاشتراك Azure حيث يوجد المخزن الرئيسي</span><span class="sxs-lookup"><span data-stu-id="60f9f-310">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="60f9f-311">يوجد معرف المستأجر الذي يوجد به حساب التخزين والتطبيقات والمخازن الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="60f9f-311">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="60f9f-312">للعثور على هذه القيمة، افتح [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**، ثم انسخ قيمة **معرف المستأجر**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-312">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="60f9f-313">توفير اسم DNS لـ Key Vault الخاص بك</span><span class="sxs-lookup"><span data-stu-id="60f9f-313">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="60f9f-314">اسم DNS للمخزن الرئيسي، مثل `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="60f9f-314">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="60f9f-315">(تتطابق هذه القيمة مع اسم DNS المستخدم في مخزن الكيان.)</span><span class="sxs-lookup"><span data-stu-id="60f9f-315">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="60f9f-316">توفير السر الذي يحتوي على اسم حساب التخزين</span><span class="sxs-lookup"><span data-stu-id="60f9f-316">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="60f9f-317">**اسم حساب التخزين**</span><span class="sxs-lookup"><span data-stu-id="60f9f-317">**storage-account-name**</span></span> |
    | <span data-ttu-id="60f9f-318">اسم السر لمعرف التطبيق الذي سيتم استخدامه للوصول إلى Data Lake</span><span class="sxs-lookup"><span data-stu-id="60f9f-318">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="60f9f-319">**معرف التطبيق**</span><span class="sxs-lookup"><span data-stu-id="60f9f-319">**app-id**</span></span> |
    | <span data-ttu-id="60f9f-320">اسم السر الذي سيتم استخدامه مع معرف التطبيق</span><span class="sxs-lookup"><span data-stu-id="60f9f-320">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="60f9f-321">**سر التطبيق**</span><span class="sxs-lookup"><span data-stu-id="60f9f-321">**app-secret**</span></span> |

5. <span data-ttu-id="60f9f-322">وافق علي الشروط، وحدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-322">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="60f9f-323">سيتم تثبيت الوظيفة الإضافية خلال بضع دقائق.</span><span class="sxs-lookup"><span data-stu-id="60f9f-323">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="60f9f-324">تكوين AI Builder</span><span class="sxs-lookup"><span data-stu-id="60f9f-324">Configure AI Builder</span></span>

1. <span data-ttu-id="60f9f-325">قم بتسجيل الدخول إلى LCS، وافتح الصفحة **تفاصيل البيئة**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-325">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="60f9f-326">قم بالتمرير إلى قسم **الوظائف الإضافية للبيئة**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-326">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="60f9f-327">يجب أن ترى الوظائف الإضافية التي تم تثبيتها بالفعل في هذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="60f9f-327">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="60f9f-328">إذا لم تكن الوظيفة الإضافية **التصدير إلى Data Lake**، فقم بتكوين هذه الوظيفة الإضافية.</span><span class="sxs-lookup"><span data-stu-id="60f9f-328">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="60f9f-329">حدد الوظيفة الإضافية **Get insights**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-329">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="60f9f-330">من صفحة التفاصيل **Get insights**، أدخل القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="60f9f-330">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="60f9f-331">قيمة</span><span class="sxs-lookup"><span data-stu-id="60f9f-331">Value</span></span>                                                    | <span data-ttu-id="60f9f-332">الوصف</span><span class="sxs-lookup"><span data-stu-id="60f9f-332">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="60f9f-333">عنوان URL للمؤسسة CDS</span><span class="sxs-lookup"><span data-stu-id="60f9f-333">CDS Organization URL</span></span>                                     | <span data-ttu-id="60f9f-334">عنوان URL الخاص بمؤسسة Dataverse للمثيل Dataverse.</span><span class="sxs-lookup"><span data-stu-id="60f9f-334">The Dataverse organization URL of the Dataverse instance.</span></span> <span data-ttu-id="60f9f-335">للعثور على هذه القيمة، افتح المدخل [Power Apps](https://make.powerapps.com)، حدد الزر **إعدادات** (رمز الترس) في الزاوية العلوية اليمنى، حدد **إعدادات متقدمة**، وانسخ عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="60f9f-335">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Advanced settings**, and copy the URL.</span></span> <span data-ttu-id="60f9f-336">(ينتهي عنوان URL ب "dynamics.com")</span><span class="sxs-lookup"><span data-stu-id="60f9f-336">(The URL ends with "dynamics.com.")</span></span> |
    | <span data-ttu-id="60f9f-337">معرف مؤسسة CDS</span><span class="sxs-lookup"><span data-stu-id="60f9f-337">CDS Org ID</span></span>                                               | <span data-ttu-id="60f9f-338">معرف بيئة المثيل Dataverse.</span><span class="sxs-lookup"><span data-stu-id="60f9f-338">The environment ID of the Dataverse instance.</span></span> <span data-ttu-id="60f9f-339">للعثور على هذه القيمة، افتح المدخل [Power Apps](https://make.powerapps.com)، حدد الزر **إعدادات** (رمز الترس) في الزاوية العلوية اليمنى، حدد **تخصيصات \> موارد المطور \> معلومات مرجع المثيل**، وانسخ قيمة **المعرف**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-339">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Customizations \> Developer resources \> Instance Reference Information**, and copy the **ID** value.</span></span> |
    | <span data-ttu-id="60f9f-340">معرف مستأجر CDS (معرف الدليل من AAD)</span><span class="sxs-lookup"><span data-stu-id="60f9f-340">CDS Tenant ID (Directory ID from AAD)</span></span>               | <span data-ttu-id="60f9f-341">معرف مستأجر المثيل Dataverse.</span><span class="sxs-lookup"><span data-stu-id="60f9f-341">The tenant ID of the Dataverse instance.</span></span> <span data-ttu-id="60f9f-342">للعثور على هذه القيمة، افتح [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**، ثم انسخ قيمة **معرف المستأجر**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-342">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="60f9f-343">قم بتوفير معرف كائن المستخدم الذي يمتلك دور مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="60f9f-343">Provide user object ID who has system administrator role</span></span> | <span data-ttu-id="60f9f-344">معرف كائن مستخدم Azure AD في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="60f9f-344">The Azure AD user object ID of the user in Dataverse.</span></span> <span data-ttu-id="60f9f-345">يجب أن يكون هذا المستخدم مسؤول نظام مثيل Dataverse.</span><span class="sxs-lookup"><span data-stu-id="60f9f-345">This user must be a system administrator of the Dataverse instance.</span></span> <span data-ttu-id="60f9f-346">للعثور على هذه القيمة، افتح [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory \> المستخدمين**، حدد المستخدم، ثم، في القسم **الهوية**، انسخ القيمة **معرف الكائن**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-346">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory \> Users**, select the user, and then, in the **Identity** section, copy the **Object ID** value.</span></span> |
    | <span data-ttu-id="60f9f-347">هل هذه هي بيئة CDS الافتراضية للمستأجر؟</span><span class="sxs-lookup"><span data-stu-id="60f9f-347">Is this the default CDS environment for the tenant?</span></span>      | <span data-ttu-id="60f9f-348">إذا كان مثيل Dataverse هو أول مثيل إنتاج تم إنشاؤه، حدد خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="60f9f-348">If the Dataverse instance was the first production instance that was created, select this check box.</span></span> <span data-ttu-id="60f9f-349">إذا تم إنشاء مثيل Dataverse يدويًا، فقم بإلغاء تحديد خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="60f9f-349">If the Dataverse instance was manually created, clear this check box.</span></span> |

## <a name="configure-the-entity-store"></a><span data-ttu-id="60f9f-350">تكوين متجر الكيان</span><span class="sxs-lookup"><span data-stu-id="60f9f-350">Configure the entity store</span></span>

<span data-ttu-id="60f9f-351">اتبع هذه الخطوات لإعداد مخزن الكيان في بيئة Finance.</span><span class="sxs-lookup"><span data-stu-id="60f9f-351">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="60f9f-352">انتقل إلى **إدارة النظام \> إعداد \> معلمات النظام \> اتصالات البيانات**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-352">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="60f9f-353">عيِّن الخيار **تمكين تكامل Data Lake** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-353">Set the **Enable Data Lake integration** option to **Yes**.</span></span>
3. <span data-ttu-id="60f9f-354">تعيين حقول المخزن الرئيسي التالية:</span><span class="sxs-lookup"><span data-stu-id="60f9f-354">Set the following key vault fields:</span></span>

    - <span data-ttu-id="60f9f-355">**معرف استمارة التطبيق (العميل)** – أدخل معرف عميل استمارة التقديم الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="60f9f-355">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="60f9f-356">**سر استمارة التقديم** – أدخل كلمة السر التي قمت بحفظها لاستمارة التقديم التي قمت بإنشائها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="60f9f-356">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="60f9f-357">**اسم DNS** – يمكنك العثور على اسم نظام اسم المجال (DNS) في صفحة تفاصيل استمارة التقديم لاستمارة التطبيق التي قمت بإنشائها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="60f9f-357">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="60f9f-358">**اسم السر** - أدخل **تخزين-حساب-اتصال-سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="60f9f-358">**Secret name** – Enter **storage-account-connection-string**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="60f9f-359">الملاحظات والدعم</span><span class="sxs-lookup"><span data-stu-id="60f9f-359">Feedback and support</span></span>

<span data-ttu-id="60f9f-360">الرجاء إرسال بريد الكتروني إلى [‏‫معلومات دفع العميل (معاينة) ](mailto:fiap@microsoft.com) إذا كنت مهتمًا بتقديم الملاحظات أو تحتاج إلى الدعم.</span><span class="sxs-lookup"><span data-stu-id="60f9f-360">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="60f9f-361">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="60f9f-361">Privacy notice</span></span>

<span data-ttu-id="60f9f-362">إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة (SLA) لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.</span><span class="sxs-lookup"><span data-stu-id="60f9f-362">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
