---
title: تكوين Finance Insights (معاينة)
description: يشرح هذا الموضوع خطوات التكوين التي تتيح لنظامك إمكانية استخدام القدرات المتوفرة في Finance Insights.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 38cdeb9110691e594b4b90fc5bc79e369c9f4707
ms.sourcegitcommit: 1cfd6e0c808341b0f5bafbde7d04b0255b27352f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664080"
---
# <a name="configuration-for-finance-insights-preview"></a>تكوين Finance insights (معاينة)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

تضم Finance insights الوظيفة من Microsoft Dynamics 365 Finance مع Common Data Service وAzure و AI Builder لتوفير أدوات التنبؤ القوية لمؤسستك. يشرح هذا الموضوع خطوات التكوين التي تتيح لنظامك إمكانية استخدام القدرات المتوفرة في Finance Insights.

## <a name="deploy-dynamics-365-finance"></a>نشر Dynamics 365 Finance

نشر البيئات باتباع هذه الخطوات.

1. في Microsoft Dynamics Lifecycle Services (LCS)، قم بإنشاء أو تحديث بيئة Dynamics 365 Finance. تتطلب البيئة تحديث التطبيق النظام الأساسي 10.0.11 إلى الإصدار 35 أو أحدث.
2. يجب أن تكون البيئة بيئة عالية التوافر (HA) في وضع الحماية. (يُعرف هذا النوع من البيئة أيضًا ببيئة الطبقة 2). لمزيد من المعلومات، راجع [تخطيط البيئة](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. إذا كنت تستخدم البيانات التجريبية لشركات Contoso، فإنك ستحتاج إلى بيانات نموذج إضافية لاستخدام ميزات توقعات دفع العميل وتقديرات التدفقات النقدية والتنبؤ بالموازنة. 

## <a name="configure-common-data-service"></a>تكوين Common Data Service

يمكنك إكمال خطوات التكوين اليدوي التالية، أو يمكنك تسريع عملية التكوين باستخدام البرنامج النصي Windows PowerShell الذي تم توفيره. عند انتهاء تشغيل البرنامج النصي PowerShell، فإنه سيتم منحك القيم المراد استخدامها لتكوين Finance insights. 

> [!NOTE]
> افتح PowerShell على الكمبيوتر لتشغيل البرنامج النصي. قد تحتاج إلى الإصدار 5 من PowerShell. قد لا يعمل الخيار Microsoft Azure CLI "جربه".

# <a name="manual-configuration-steps"></a>[خطوات التكوين اليدوي](#tab/configuration-steps)

1. افتح مركز الإدارة [Power Platform ](https://admin.powerplatform.microsoft.com/)، واتبع هذه الخطوات لإنشاء بيئة Common Data Service جديدة في مستأجر خدمة Active Directory نفسه.

    1. افتح صفحة **البيئات**.

        [![صفحة البيئات](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. حدد **بيئة جديدة**.
    3. في الحقل **نوع**، حدد **وضع الحماية**.
    4. عيّن الخيار **إنشاء قاعدة بيانات** إلى **نعم**.
    5. حدد **التالي**.
    6. حدد اللغة والعملة الخاصة بمؤسسك.
    7. اقبل القيم الافتراضية للحقول الأخرى.
    8. حدد **حفظ**.
    9. حدّث صفحة **البيئات**.
    10. انتظر حتى يتم تحديث قيمة الحقل **الحالة** إلى **جاهز**.
    11. دوِّن ملاحظة بمُعرف المؤسسة Common Data Service.
    12. حدد البيئة المراد نسخها، ثم حدد **إعدادات**.
    13. حدد **الموارد \> كافة الإعدادات القديمة**.
    14. في شريط التنقل العلوي، حدد **الإعدادات**، ثم حدد **التخصيصات**.
    15. حدد **موارد المطور**.
    16. قم بتعيين الحقل **معرف معلومات مرجع المثيل** إلى قيمة معرف المؤسسة Common Data Service التي قمت بتدوين ملاحظة لها مسبقًا.
    17. في شريط العنوان الخاص بالمستعرض، قم بتسجيل عنوان URL الخاص بمؤسسة Common Data Service. على سبيل المثال، قد يكون عنوان URL `https://org42b2b3d3.crm.dynamics.com`.

2. إذا كنت تخطط لاستخدام ميزة تقديرات التدفقات النقدية أو التنبؤ بالموازنة، اتبع الخطوات التالية لتحديث حد التعليق التوضيحي لمؤسسك إلى 50 ميغابايت على الأقل (MB):

    1. افتح [مدخل Power Apps](https://make.powerapps.com).
    2. حدد البيئة التي قمت بإنشائها للتو، ثم حدد **الإعدادات المتقدمة**.
    3. حدد **إعدادات \> تكوين البريد الإلكتروني**.
    4. قم بتغيير قيمة الحقل **الحد الأقصى حجم الملف** إلى **51.200**. (ويتم التعبير عن القيمة بالكيلو بايت \[KB\].)
    5. حدد **موافق** لحفظ التغييرات الخاصة بك.

# <a name="windows-powershell-configuration-script"></a>[برنامج التكوين النصي لـ Windows PowerShell](#tab/powershell-configuration-script)

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

## <a name="configure-the-azure-setup"></a>تكوين إعداد Azure

### <a name="enter-the-common-data-service-directory-id-and-the-users-azure-ad-object-id"></a>أدخل معرف الدليل Common Data Service ومعرف الكائن الخاص بمستخدم Azure AD

1. أدخل مُعرف الدليل Common Data Service:

    1. افتح [مدخل Azure](https://portal.azure.com).
    2. قم بتسجيل الدخول باستخدام معرف المستخدم الذي تم استخدامه لإنشاء البيئة Common Data Service.
    3. الانتقال إلى **Azure Active Directory**.
    4. انسخ قيمة **معرف المستأجر**.

2. أدخل معرف كائن Azure Active Directory (Azure AD):

    1. في [مدخل Azure](https://portal.azure.com)، انتقل إلى **المستخدمين**، وابحث عن المستخدم بعنوان البريد الإلكتروني.
    2. حدد اسم المستخدم.
    3. انسخ قيمة **معرف الكائن**.

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>استخدام Azure Cloud Shell لإعداد موارد Finance insights Data Lake

# <a name="use-a-windows-powershell-script"></a>[استخدم البرنامج النصي لـ Windows PowerShell](#tab/use-a-powershell-script)

لقد تم توفير برنامج Windows PowerShell النصي، حتى يمكنك بسهولة إعداد موارد Azure الموضحة في [تكوين التصدير إلى Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake). إذا كنت تفضل القيام بالإعداد اليدوي، فعليك تخطي هذا الإجراء، ومتابعة الإجراء في القسم [الإعداد اليدوي](#manual-setup).

> [!NOTE]
> اتبع الخطوات التالية لتشغيل البرنامج النصي PowerShell. قد لا يعمل الخيار Azure CLI "جربه"، أو تشغيل البرنامج النصي على الكمبيوتر.

اتبع الخطوات التالية لتكوين Azure باستخدام البرنامج النصي لـ Windows PowerShell. يجب أن يكون لديك حقوق بإنشاء مجموعة موارد Azure وموارد Azure وتطبيق Azure AD. للحصول على معلومات حول الأذونات المطلوبة، راجع [التحقق من أذونات Azure AD ](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. في [مدخل azure ](https://portal.azure.com)، انتقل إلى اشتراك هدف Azure. حدد الزر **Cloud Shell** الموجود إلى يمين الحقل **بحث**.
2. حدد **PowerShell**.
3. قم بإنشاء تخزين، إذا تمت مطالبتك بالقيام بذلك. ثم قم بتحميل البرنامج النصي لـ Windows PowerShell إلى جلسة العمل.
4. قم بتشغيل البرنامج النصي.
5. اتبع المطالبات لتشغيل البرنامج النصي.
6. استخدم المعلومات من إخراج البرنامج النصي لتثبيت الوظيفة الإضافية **التصدير إلى Data Lake** في LCS.
7. استخدم المعلومات من إخراج البرنامج النصي لتمكين مخزن الكيان في الصفحة **اتصالات البيانات** في Finance (**إدارة النظام \> معلمات النظام \> اتصالات البيانات**).

### <a name="manual-setup"></a>إعداد يدوي

#### <a name="add-applications-to-the-azure-ad-tenant"></a>إضافة التطبيقات إلى المستأجر Azure AD

1. في [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**.
2. حدد **إدارة \> تطبيقات Enterprise**.
3. ابحث عن التطبيقات التالية حسب معرف التطبيق.

    | استمارة التقديم                              | معرف التطبيق                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | خدمة تخويل AI Builder         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

في حالة تعذر العثور على أي من التطبيقات السابقة، حاول القيام بالخطوات التالية.

1. على جهازك المحلي، حدد القائمة **ابدأ**، وابحث عن **powershell**.
2. حدد واستمر في الضغط (أو انقر بزر الماوس الأيمن) **Windows PowerShell**، ثم حدد **تشغيل كمسؤول**.
3. قم بتشغيل الأمر التالي لتثبيت الوحدة النمطية **AzureAD**.

    `Install-Module -Name AzureAD`

4. إذا كان موفر NuGet مطلوبًا للمتابعة، حدد **Y** لتثبيته.
5. إذا ظهرت رسالة "مستودع غير موثوق به"، حدد **Y** للمتابعة.
6. بالنسبة لكل تطبيق يجب إضافته، قم بتشغيل الأوامر التالية لإضافة التطبيق إلى Azure AD. عند المطالبة، قم بتسجيل الدخول كمسؤول Azure AD.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>إنشاء موارد Azure

> [!NOTE]
> تأكد من إنشاء الموارد التالية في مثيل Azure AD نفسه كبيئة Common Data Service. لا يمكنك استخدام موارد من مثيل Azure AD مختلف.

1. قم بإنشاء حساب تخزين جديد:

    1. في [مدخل Azure](https://portal.azure.com)، قم بحساب تخزين.
    2. في مربع الحوار **إنشاء حساب تخزين**، قم بتعيين الحقول التالية:

        - **الموقع** – حدد مركز البيانات الذي تقع فيه البيئة الخاصة بك.
        - **الأداء** – إننا نوصي بأن تقوم بتحديد **قياسي**.
        - **نوع الحساب** – يجب تحديد **StorageV2**.

    3. في مربع الحوار **خيارات متقدمة**، بالنسبة للخيار **Data Lake storage Gen2**، حدد **تمكين** ضمن ميزة **مساحات الأسماء الهرمية**. في حالة تعطيل هذه الميزة، فإنه لا يمكنك استهلاك البيانات التي يكتبها تطبيق Finance and Operations باستخدام خدمات مثل تدفقات بيانات Power BI.
    4. حدد **مراجعة وإنشاء**. عند اكتمال النشر، سيظهر المورد الجديد في مدخل Azure.
    5. انتقل إلى حساب التخزين الذي قمت بإنشائه.
    6. في القائمة اليمنى، حدد **مفاتيح الوصول**.
    7. قم بنسخ سلسلة الاتصال وحفظها إما إلى **Key1** أو **Key2**.
    8. قم بنسخ اسم حساب التخزين وحفظه.

2. إنشاء مخزن رئيسي جديد:

    1. في [مدخل Azure](https://portal.azure.com)، قم إنشاء مخزن رئيسي.
    2. في مربع الحوار **إنشاء مخزن رئيسي**، في الحقل **الموقع**، حدد مركز البيانات الذي تقع فيه البيئة الخاصة بك.
    3. بعد إنشاء مخزن رئيسي، حدده في القائمة، ثم حدد **الأسرار**.
    4. حدد **إنشاء/استيراد**.
    5. في مربع الحوار **إنشاء سر**، في الحقل **خيارات التحميل**، حدد **يدوي**.
    6. أدخل اسمًا للسر. قم بتدوين الاسم، لأنه سيتعين عليك توفيره لاحقًا.
    7. في الحقل **القيمة**، أدخل سلسلة الاتصال التي حصلت عليها من حساب التخزين في الإجراء السابق.
    8. حدد **ممكّن‬‬‏‫**، ثم حدد **إنشاء**. يتم إنشاء السر وإضافة إلى مخزن رئيسي.
    9. انتقل إلى **نظرة عامة حول مخزن رئيسي**، وقم بتدوين اسم DNS.

3. إنشاء وتسجيل تطبيق Azure AD:

    1. في [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**، ثم حدد **عمليات تسجيل التطبيق**.
    2. حدد **تسجيل تطبيق جديد**، ثم قم بتعيين الحقول التالية:

        - **الاسم** - أدخل اسم التطبيق.
        - **نوع التطبيق** – حدد **API للويب**.
        - **إعادة توجيه إعداد عنوان URI** – أدخل عنوان URL لمثيل Dynamics 365 الخاص بك، مثل، `https://yourdynamicsinstance.dynamics.com/auth`.

    3. انتقل إلى التطبيق الذي قمت بإنشائه الآن، وقم بنسخ وحفظ قيمة **معرف تطبيق (عميل) الخاصة بالتطبيق**. سيتعين عليك توفير هذه القيمة لاحقًا، عند إعداد المخزن الرئيسي.
    4. انتقل إلى **أذونات API**، واتبع الخطوات التالية:

        1. حدد **إضافة إذن**.
        2. حدد **مخزن Azure رئيسي**.
        3. بعد تحديد الأذونات المفوضة، حدد **user\_impersonation**.
        4. حدد **إضافة أذونات**.

    5. في القائمة الخاصة بالتطبيق، حدد **الشهادات \& الأسرار**، ثم اتبع الخطوات التالية لإنشاء أسرار المخزن الرئيسي:

        1. حدد **سر عميل جديد**.
        2. في الحقل **الوصف الرئيسي**، أدخل اسمًا.
        3. حدد مدة، ثم حدد **إضافة**. يتم إنشاء سر في الحفل **القيمة**.
        4. قم بنسخ القيمة السرية وحفظها.

4. إنشاء أسرار المخزن الرئيسي:

    1. انتقل إلى المخزن الرئيسي الذي قمت بإنشائه سابقًا، وحدد **الأسرار**.
    2. بالنسبة لكل اسم سري في الجدول التالي، اتبع الخطوات التالية:

        1. حدد **إنشاء/استيراد**.
        2. في مربع الحوار **إنشاء سر**، في الحقل **خيارات التحميل**، حدد **يدوي**.
        3. قم بإنشاء الاسم السري والقيمة من الجدول التالي.
        4. حدد **ممكّن‬‬‏‫**، ثم حدد **إنشاء**. يتم إنشاء السر وإضافة إلى مخزن رئيسي.

        | اسم السر                       | قيمة سرية                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | معرف التطبيق                            | معرف التطبيق الخاص بالتطبيق الذي قمت بإنشائه سابقًا                                      |
        | سر التطبيق                        | سر العميل الذي قمت بحفظه مسبقًا                                                    |
        | اسم حساب التخزين              | اسم حساب التخزين الذي قمت بإنشائه مسبقًا، مثل **storageaccount1**       |
        | التخزين-الحساب-الاتصال-السلسلة | سلسلة الاتصال التي قمت بنسخها من الصفحة **مفاتيح الوصول** لحساب التخزين |

5. تخويل التطبيق للوصول إلى المخزن الرئيسي:

    1. في [مدخل Azure](https://portal.azure.com)، قم بفتح المخزن الرئيسي الذي قمت بإنشائه سابقًا.
    2. حدد نهج الوصول.
    3. بالنسبة لكل تطبيق في الجدول التالي، اتبع الخطوات التالية:

        1. حدد **إضافة نهج وصول** لإنشاء سياسة وصول.
        2. في الحقل **الأذونات السرية**، حدد الأذونات من الجدول التالي.
        3. في الحقل **تحديد الرئيسي**، ابحث عن اسم عرض التطبيق من الجدول التالي.
        4. حدد **تحديد**.
        5. حدد **إضافة**.
        6. حدد **حفظ**.

        | استمارة التقديم                                              | الأذونات |
        |----------------------------------------------------------|-------------|
        | اسم عرض التطبيق الجديد الذي قمت بإنشائه | الحصول على، قائمة   |
        | **Microsoft Dynamics ERP Microservices**                 | الحصول على، قائمة   |

6. قم بتعيين أدوار للوصول إلى حساب التخزين:

    1. في [مدخل Azure](https://portal.azure.com)، قم بفتح حساب التخزين الذي قمت بإنشائه سابقًا.
    2. حدد **التحكم في الوصول (IAM)**، ثم حدد **مهمات الأدوار**.
    3. حدد **إضافة، أضف مهمة الدور**.
    4. بالنسبة لكل تطبيق في الجدول التالي، اتبع الخطوات التالية:

        1. حدد الدور من الجدول التالي.
        2. اجعل الحقل **تعيين حق الوصول إلى** على مستخدم **Azure AD أو مجموعة أو كيان الخدمة**.
        3. في الحقل **تحديد**، قم بالدخول إلى استمارة التقديم من الجدول التالي.
        4. حدد **حفظ**.

        | استمارة التقديم                                              | دور                        |
        |----------------------------------------------------------|-----------------------------|
        | اسم عرض التطبيق الجديد الذي قمت بإنشائه | المالك                       |
        | اسم عرض التطبيق الجديد الذي قمت بإنشائه | المساهم                 |
        | اسم عرض التطبيق الجديد الذي قمت بإنشائه | المساهم في حساب التخزين |
        | اسم عرض التطبيق الجديد الذي قمت بإنشائه | مالك بيانات التخزين كبيرة الحجم     |
        | **خدمة تخويل AI Builder**                     | قارئ بيانات التخزين كبيرة الحجم    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    $defaultSecretExpiryInYear = 1

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

    $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (blank for default)")
    if ($subscriptionId.Trim() -ne '') {
        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }

    $resourceGroupName = (Read-Host -Prompt "Enter the Azure Resource Group name: (blank for 'FinanceDataLake')")
    if ($null -eq $resourceGroupName -or $resourceGroupName.Trim() -eq '') {
        $resourceGroupName = 'FinanceDataLake'
    }
    $resourceGroup = Get-AzResourceGroup -Name $resourceGroupName -ErrorAction SilentlyContinue

    if (-not ($resourceGroup)) {
        $resourceLocation = ''
        $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
        while ($resourceLocation.Trim() -eq '' -or (-not ($resourceLocation -in $azResourceLocations))) {
            $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
            if ($resourceLocation -eq 'help') {
                $azResourceLocations
                $resourceLocation = ''
            }
        }
        $resourceGroup = New-AzResourceGroup -Name $resourceGroupName -Location $resourceLocation
    }
    else {
        $resourceLocation = $resourceGroup.Location
    }

    $clientAppName = (Read-Host -Prompt "Enter the name of the application registration: (blank for 'Finance Data Lake Application')")
    if ($clientAppName.Trim() -eq '') {
        $clientAppName = 'Finance Data Lake Application'
    }

    Write-Output '================================================================================='

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    $MicrosoftDynamicsERPMicroservicesAppObjectId = $service.ObjectId

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesCDSAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Format-Table -AutoSize
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    $aibuilderAuthorizationServiceObjectId = $service.ObjectId

    Write-Output '================================================================================='

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $clientAppName + "'")
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

        $clientApp = New-AzureADApplication -DisplayName $clientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($clientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $clientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($defaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    $deployment = New-AzResourceGroupDeployment -ResourceGroupName $resourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId

    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $resourceGroupName)
    }

    Write-Output '================================================================================='

    $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
    Write-Output "Values for LCS Data Lake Add-In:"
    Write-Output ("  Tenant ID:                         " + $subscriptionContext.Context.Subscription.TenantId)
    Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
    Write-Output "  Storage account secret name:       storage-account-name"
    Write-Output "  Application ID secret name:        app-id"
    Write-Output "  Application Secret secret name:    app-secret"
    Write-Warning "Copy this information for the LCS Add-in as it is not saved. Azure Cloud Shell will eventually time out and close."

    Write-Output '================================================================================='
    Write-Output "Values for System parameters > Data connections:"
    Write-Output ("  Application ID:                    " + $clientAppId)
    Write-Output ("  Application Secret:                " + $ClientAppSecret)
    Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
    Write-Output "  Secret name:                       storage-account-connection-string"
    Write-Warning "Copy this information for the System parameters as it is not saved. Azure Cloud Shell will eventually time out and close."
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
  New-FinanceDataLakeAzureResources
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

## <a name="configure-the-entity-store"></a>تكوين متجر الكيان

اتبع هذه الخطوات لإعداد مخزن الكيان في بيئة Finance.

1. انتقل إلى **إدارة النظام \> إعداد \> معلمات النظام \> اتصالات البيانات**.
2. عيِّن الخيار **تمكين تكامل Data Lake** على **نعم**.
3. تعيين حقول المخزن الرئيسي التالية:

    - **معرف استمارة التطبيق (العميل)** – أدخل معرف عميل استمارة التقديم الذي قمت بإنشائه سابقًا.
    - **سر استمارة التقديم** – أدخل كلمة السر التي قمت بحفظها لاستمارة التقديم التي قمت بإنشائها سابقًا.
    - **اسم DNS** – يمكنك العثور على اسم نظام اسم المجال (DNS) في صفحة تفاصيل استمارة التقديم لاستمارة التطبيق التي قمت بإنشائها سابقًا.
    - **اسم السر** - أدخل **تخزين-حساب-اتصال-سلسلة**.

## <a name="configure-the-data-lake"></a>تكوين data lake

اتبع الخطوات التالية لاستخدام LCS لإضافة الوظيفة الإضافية Azure Data Lake add-in إلى البيئة.

1. قم بتسجيل الدخول إلى LCS، ثم، ضمن اسم البيئة على الجانب الأيسر من الصفحة، حدد **تفاصيل كاملة**.
2. في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.
3. حدد الوظيفة الإضافية، حدد **تصدير إلى Data Lake**.
4. أدخل القيم التالية.

    | قيمة                                                              | الوصف |
    |--------------------------------------------------------------------|-------------|
    | معرف المستأجر لاشتراك Azure حيث يوجد المخزن الرئيسي | يوجد معرف المستأجر الذي يوجد به حساب التخزين والتطبيقات والمخازن الرئيسية. للعثور على هذه القيمة، افتح [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**، ثم انسخ قيمة **معرف المستأجر**. |
    | توفير اسم DNS لـ Key Vault الخاص بك                             | اسم DNS للمخزن الرئيسي، مثل `https://customkeyvault.vault.azure.net/`. (تتطابق هذه القيمة مع اسم DNS المستخدم في مخزن الكيان.) |
    | توفير السر الذي يحتوي على اسم حساب التخزين   | **اسم حساب التخزين** |
    | اسم السر لمعرف التطبيق الذي سيتم استخدامه للوصول إلى Data Lake          | **معرف التطبيق** |
    | اسم السر الذي سيتم استخدامه مع معرف التطبيق                                 | **سر التطبيق** |

5. وافق علي الشروط، وحدد **تثبيت**.

سيتم تثبيت الوظيفة الإضافية خلال بضع دقائق.

## <a name="configure-ai-builder"></a>تكوين AI Builder

1. قم بتسجيل الدخول إلى LCS، وافتح الصفحة **تفاصيل البيئة**.
2. قم بالتمرير إلى قسم **الوظائف الإضافية للبيئة**. يجب أن ترى الوظائف الإضافية التي تم تثبيتها بالفعل في هذه البيئة. إذا لم تكن الوظيفة الإضافية **التصدير إلى Data Lake**، فقم بتكوين هذه الوظيفة الإضافية.
3. حدد الوظيفة الإضافية **Get insights**.
4. من صفحة التفاصيل **Get insights**، أدخل القيم التالية.

    | قيمة                                                    | الوصف |
    |----------------------------------------------------------|-------------|
    | عنوان URL للمؤسسة CDS                                     | عنوان URL الخاص بمؤسسة Common Data Service للمثيل Common Data Service. للعثور على هذه القيمة، افتح المدخل [Power Apps](https://make.powerapps.com)، حدد الزر **إعدادات** (رمز الترس) في الزاوية العلوية اليمنى، حدد **إعدادات متقدمة**، وانسخ عنوان URL. (ينتهي عنوان URL ب "dynamics.com") |
    | معرف مؤسسة CDS                                               | معرف بيئة المثيل Common Data Service. للعثور على هذه القيمة، افتح المدخل [Power Apps](https://make.powerapps.com)، حدد الزر **إعدادات** (رمز الترس) في الزاوية العلوية اليمنى، حدد **تخصيصات \> موارد المطور \> معلومات مرجع المثيل**، وانسخ قيمة **المعرف**. |
    | معرف مستأجر CDS (معرف الدليل من AAD)               | معرف مستأجر المثيل Common Data Service. للعثور على هذه القيمة، افتح [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**، ثم انسخ قيمة **معرف المستأجر**. |
    | قم بتوفير معرف كائن المستخدم الذي يمتلك دور مسؤول النظام | معرف كائن مستخدم Azure AD في Common Data Service. يجب أن يكون هذا المستخدم مسؤول نظام مثيل Common Data Service. للعثور على هذه القيمة، افتح [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory \> المستخدمين**، حدد المستخدم، ثم، في القسم **الهوية**، انسخ القيمة **معرف الكائن**. |
    | هل هذه هي بيئة CDS الافتراضية للمستأجر؟      | إذا كان مثيل Common Data Service هو أول مثيل إنتاج تم إنشاؤه، حدد خانة الاختيار هذه. إذا تم إنشاء مثيل Common Data Service يدويًا، فقم بإلغاء تحديد خانة الاختيار هذه. |

## <a name="feedback-and-support"></a>الملاحظات والدعم

الرجاء إرسال بريد الكتروني إلى [‏‫معلومات دفع العميل (معاينة) ](mailto:fiap@microsoft.com) إذا كنت مهتمًا بتقديم الملاحظات أو تحتاج إلى الدعم.

## <a name="privacy-notice"></a>إشعار الخصوصية

إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة (SLA) لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.
