---
title: تكوين Finance Insights - الإصدار 10.0.20 والإصدارات اللاحقة
description: يشرح هذا الموضوع كيفية تكوين نظامك لاستخدام الإمكانات المتوفرة في Finance Insights في الإصدار 10.0.20 والإصدارات الأحدث.
author: ShivamPandey-msft
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex,nofollow
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: cea6258d3a99ba33e73acd2508ec7b6c11d15859
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061744"
---
# <a name="configuration-for-finance-insights---version-10020-and-later"></a>تكوين Finance Insights - الإصدار 10.0.20 والإصدارات اللاحقة

[!include [banner](../includes/banner.md)]



يجمع Finance insights بين وظائف من Microsoft Dynamics 365 Finance ووظائف من Dataverse وAzure وAI Builder لتوفير أدوات تنبؤ قوية لمؤسستك. يشرح هذا الموضوع كيفية تكوين الإصدار 10.0.20 من Dynamics 365 Finance لتمكين النظام من استخدام القدرات المتوفرة في Finance insights.

> [!NOTE]
> تنطبق خطوات التكوين الموضحة في هذا الموضوع فقط على Finance الإصدار 10.0.20 والإصدارات اللاحقة. "لإعداد Finance insights في الإصدار 10.0.19 والإصدارات السابقة، راجع [تكوين Finance insights - الإصدارات حتى 10.0.19](configure-for-fin-insites.md).

## <a name="deploy-finance"></a>نشر Finance

اتبع هذه الخطوات لنشر البيئات.

1. في Microsoft Dynamics Lifecycle Services (LCS)، قم بإنشاء بيئة Finance أو تحديثها. تتطلب البيئة إصدار التطبيق 10.0.20 أو أحدث من تطبيقات التمويل والعمليات.
2. يجب أن تكون البيئة بيئة عالية التوافر (HA) في وضع الحماية. (يُعرف هذا النوع من البيئة أيضًا ببيئة الطبقة 2). لمزيد من المعلومات، راجع [تخطيط البيئة](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. إذا كنت تقوم بتكوين Finance insights في بيئة حماية، فقد تحتاج إلى نسخ بيانات الإنتاج إلى تلك البيئة لتوقعات العمل. يستخدم نموذج التنبؤ سنوات متعددة من البيانات لبناء التوقعات. لا تحتوي بيانات العرض التوضيحي لشركة Contoso على بيانات تاريخية كافية لتدريب نموذج التنبؤ بشكل مناسب. 

## <a name="configure-dataverse"></a>تكوين Dataverse

استخدم هذه الخطوات لتكوين Dataverse لـ Finance Insights.

1. في LCS، افتح صفحة البيئة، وتحقق من أن قسم **تكامل Power Platform** تم إعداده بالفعل.

    - في حالة إعداده بالفعل، يجب سرد اسم بيئة Dataverse المرتبط ببيئة Finance.
    - في حالة عدم إعداده بعد، اتبع الخطوات التالية:

        1. في القسم **تكامل Power Platform**، حدد **إعداد**. قد يستغرق إعداد البيئة ما يصل إلى ساعة واحدة.
        2. في حالة إعداد بيئة Dataverse بنجاح، يجب سرد اسم بيئة Dataverse المرتبط ببيئة Finance.

        > [!NOTE]
        > بعد إكمال إعداد البيئة، **لا** تقم بتحديد **ارتباط إلى CDS للتطبيقات**. هذا الزر غير مطلوب لـ Finance insights. إذا قمت بتحديده، فلن تتمكن من تكوين وظائف البيئة الإضافية المطلوبة في LCS.

## <a name="configure-azure"></a>تكوين Azure

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>استخدام Azure Cloud Shell لإعداد موارد Finance insights Data Lake

# <a name="use-a-windows-powershell-script"></a>[استخدم البرنامج النصي لـ Windows PowerShell](#tab/use-a-powershell-script)

لقد تم توفير برنامج Windows PowerShell النصي حتى يمكنك بسهولة إعداد موارد Azure الموضحة في [تكوين التصدير إلى Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md). إذا كنت تفضل القيام بالإعداد يدويًا، فعليك تخطي هذا الإجراء، وإكمال الإجراء في القسم [الإعداد اليدوي](#manual-setup) بدلاً منه.

> [!NOTE]
> استخدم الإجراء التالي لتشغيل البرنامج النصي Windows PowerShell. قد لا يعمل الإعداد إذا كنت تستخدم الخيار **جربه** في Azure CLI أو إذا قمت بتشغيل البرنامج النصي على الكمبيوتر الخاص بك.

اتبع الخطوات التالية لاستخدام البرنامج النصي Windows PowerShell لتكوين Azure. يجب أن يكون لديك حقوق بإنشاء مجموعة موارد Azure وموارد Azure وتطبيق Azure AD. للحصول على معلومات حول الأذونات المطلوبة، راجع [التحقق من أذونات Azure AD ](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. في [مدخل azure ](https://portal.azure.com)، انتقل إلى اشتراك هدف Azure.
2. حدد **Cloud Shell** الموجود إلى يمين الحقل **بحث**.
3. حدد **PowerShell**.
4. قم بإنشاء تخزين، إذا تمت مطالبتك بإنشائه.
5. في علامة التبويب **Azure CLI**، حدد **نسخ**.
6. في Notepad (المفكرة)، افتح ملفًا جديدًا، وألصقه في البرنامج النصي لـ Windows PowerShell.
7. احفظ الملف باسم **ConfigureDataLake.ps1**.
8. قم بتحميل البرنامج النصي Windows PowerShell إلى الجلسة باستخدام خيار القائمة للتحميل في Cloud Shell.
9. قم بتشغيل البرنامج النصي **.\ConfigureDataLake.ps1**.
10. اتبع المطالبات لتشغيل البرنامج النصي.
11. استخدم المعلومات من إخراج البرنامج النصي لتثبيت الوظيفة الإضافية التصدير إلى Data Lake في LCS.

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

1. على جهاز الكمبيوتر المحلي، في القائمة **ابدأ**، وابحث عن **powershell**.
2. حدد واستمر في الضغط (أو انقر بزر الماوس الأيمن) **Windows PowerShell**، ثم حدد **تشغيل كمسؤول**.
3. قم بتشغيل الأمر التالي لتثبيت الوحدة النمطية **AzureAD**.

    `Install-Module -Name AzureAD`

4. إذا كان موفر NuGet مطلوبًا للمتابعة، حدد **Y** لتثبيته.
5. إذا استلمت رسالة "مستودع غير موثوق به"، حدد **Y** للمتابعة.
6. بالنسبة لكل تطبيق يجب إضافته، قم بتشغيل الأوامر التالية لإضافة التطبيق إلى Azure AD. عند المطالبة، قم بتسجيل الدخول كمسؤول Azure AD.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>إنشاء موارد Azure

> [!NOTE]
> تأكد من إنشاء الموارد التالية في مثيل Azure AD نفسه الذي يكون داخل البيئة Dataverse. لا يمكنك استخدام موارد من مثيل Azure AD مختلف.

1. قم بإنشاء حساب تخزين:

    1. في [مدخل Azure](https://portal.azure.com)، قم بحساب تخزين.
    2. في مربع الحوار **إنشاء حساب تخزين**، قم بتعيين الحقول التالية:

        - **الموقع** – حدد مركز البيانات الذي تقع فيه البيئة الخاصة بك.
        - **الأداء** – إننا نوصي بأن تقوم بتحديد **قياسي**.
        - **نوع الحساب** – يجب تحديد **StorageV2**.

    3. في مربع الحوار **خيارات متقدمة**، بالنسبة للخيار **Data Lake storage Gen2**، حدد **تمكين** ضمن ميزة **مساحات الأسماء الهرمية**. في حالة عدم تمكين هذه الميزة، لا يمكنك استهلاك البيانات التي تكتبها تطبيقات التمويل والعمليات باستخدام خدمات مثل تدفقات بيانات Power BI.
    4. حدد **مراجعة وإنشاء**. عند اكتمال النشر، يظهر المورد الجديد في مدخل Azure.
    5. انتقل إلى حساب التخزين الذي قمت بإنشائه.
    6. في القائمة اليمنى، حدد **مفاتيح الوصول**.
    7. قم بنسخ اسم حساب التخزين وحفظه. سيتعين عليك توفير هذه القيمة لاحقًا، عند إعداد أسرار المخزن الرئيسي.

2. إنشاء مخزن رئيسي:

    1. في [مدخل Azure](https://portal.azure.com)، قم إنشاء مخزن رئيسي.
    2. في مربع الحوار **إنشاء مخزن رئيسي**، في الحقل **الموقع**، حدد مركز البيانات الذي تقع فيه البيئة الخاصة بك.
    3. بعد إنشاء مخزن المفاتيح، انتقل إلى **نظرة عامة حول مخزن مفتاح**، ثم قم بنسخ اسم DNS وحفظه. سيتعين عليك توفير هذه القيمة لاحقًا، عند إعداد الوظيفة الإضافية Data Lake.

3. إنشاء وتسجيل تطبيق Azure AD:

    1. في [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**، ثم حدد **عمليات تسجيل التطبيق**.
    2. حدد **تسجيل تطبيق جديد**، ثم قم بتعيين الحقول التالية:

        - **الاسم** - أدخل اسم التطبيق.
        - **نوع التطبيق** – حدد **API للويب**.
        - **إعادة توجيه إعداد عنوان URI** – أدخل عنوان URL لمثيل Dynamics 365 الخاص بك، مثل `https://yourdynamicsinstance.dynamics.com/auth`.

    3. انتقل إلى التطبيق الذي قمت بإنشائه الآن، وقم بنسخ وحفظ قيمة **معرف تطبيق (عميل) الخاصة بالتطبيق**. سيتعين عليك توفير هذه القيمة لاحقًا، عند إعداد أسرار المخزن الرئيسي.
    4. انتقل إلى **أذونات API**، واتبع الخطوات التالية:

        1. حدد **إضافة إذن**.
        2. حدد **مخزن Azure رئيسي**.
        3. بعد تحديد الأذونات المفوضة، حدد **user\_impersonation**.
        4. حدد **إضافة أذونات**.

    5. في القائمة الخاصة بالتطبيق، حدد **الشهادات \& الأسرار**، ثم اتبع الخطوات التالية لإنشاء أسرار المخزن الرئيسي:

        1. حدد **سر عميل جديد**.
        2. في الحقل **الوصف الرئيسي**، أدخل اسمًا.
        3. حدد مدة، ثم حدد **إضافة**. يتم إنشاء سر في الحفل **القيمة**.
        4. قم بنسخ القيمة السرية للعميل وحفظها. سيتعين عليك توفير هذه القيمة لاحقًا، عند إعداد أسرار المخزن الرئيسي.

4. إنشاء أسرار المخزن الرئيسي:

    1. انتقل إلى المخزن الرئيسي الذي قمت بإنشائه سابقًا، وحدد **الأسرار**.
    2. بالنسبة لكل اسم سري في الجدول التالي، اتبع الخطوات التالية:

        1. حدد **إنشاء/استيراد**.
        2. في مربع الحوار **إنشاء سر**، في الحقل **خيارات التحميل**، حدد **يدوي**.
        3. قم بإنشاء الاسم السري والقيمة من الجدول.
        4. حدد **ممكّن‬‬‏‫**، ثم حدد **إنشاء**. يتم إنشاء السر وإضافة إلى مخزن رئيسي.

        | اسم السر                       | قيمة سرية                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | معرف التطبيق                            | معرف التطبيق الخاص بالتطبيق الذي قمت بإنشائه سابقًا.                                      |
        | سر التطبيق                        | سر العميل الذي قمت بحفظه مسبقًا.                                                    |
        | اسم حساب التخزين              | اسم حساب التخزين الذي قمت بإنشائه مسبقًا، مثل **storageaccount1**.       |

5. تخويل التطبيق للوصول إلى المخزن الرئيسي:

    1. في [مدخل Azure](https://portal.azure.com)، قم بفتح المخزن الرئيسي الذي قمت بإنشائه سابقًا.
    2. حدد نهج الوصول.
    3. بالنسبة لكل تطبيق في الجدول التالي، اتبع الخطوات التالية:

        1. حدد **إضافة نهج وصول** لإنشاء سياسة وصول.
        2. في الحقل **الأذونات السرية**، حدد الأذونات من الجدول.
        3. في الحقل **تحديد الرئيسي**، ابحث عن اسم عرض التطبيق من الجدول.
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

        1. حدد الدور من الجدول.
        2. اجعل الحقل **تعيين حق الوصول إلى** على مستخدم **Azure AD أو مجموعة أو كيان الخدمة**.
        3. في الحقل **تحديد**، قم بالدخول إلى استمارة التقديم من الجدول.
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

## <a name="configure-the-export-to-data-lake-add-in"></a>تكوين الوظيفة الإضافية التصدير إلى Data Lake

اتبع الخطوات التالية لاستخدام LCS لإضافة الوظيفة الإضافية التصدير إلى Data Lake إلى البيئة.

1. قم بتسجيل الدخول إلى LCS، ثم، ضمن اسم البيئة على الجانب الأيسر من الصفحة، حدد **تفاصيل كاملة**.
2. في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.
3. حدد الوظيفة الإضافية، حدد **تصدير إلى Data Lake**.
4. أدخل القيم التالية.

    | قيمة                                                              | الوصف |
    |--------------------------------------------------------------------|-------------|
    | معرف المستأجر لاشتراك Azure حيث يوجد المخزن الرئيسي | يوجد معرف المستأجر الذي يوجد به حساب التخزين والتطبيقات والمخازن الرئيسية. للحصول على هذه القيمة، افتح [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**، ثم انسخ قيمة **معرف المستأجر**. |
    | توفير اسم DNS لـ Key Vault الخاص بك                             | اسم DNS للمخزن الرئيسي، مثل `https://customkeyvault.vault.azure.net/`. |
    | توفير السر الذي يحتوي على اسم حساب التخزين   | **اسم حساب التخزين** |
    | اسم السر لمعرف التطبيق الذي سيتم استخدامه للوصول إلى Data Lake          | **معرف التطبيق** |
    | الاسم السري لسر عميل التطبيق                                  | **سر التطبيق** |

5. وافق على الشروط، ثم حدد **تثبيت**.

سيتم تثبيت الوظيفة الإضافية خلال بضع دقائق.

## <a name="configure-the-finance-insights-add-in"></a>تكوين ‏الوظيفة الإضافية Finance insights

> [!NOTE]
> إذا كنت قد قمت بتثبيت الوظيفة الإضافية Get insights مسبقًا، فقم بإزالة تثبيتها قبل إكمال الإجراء التالي.

اتبع الخطوات التالية لتثبيت الوظيفة الإضافية لـ Finance insights.

1. قم بتسجيل الدخول إلى LCS، ثم، ضمن اسم البيئة على الجانب الأيسر من الصفحة، حدد **تفاصيل كاملة**.
2. في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.
3. حدد الوظيفة الإضافية **Finance insights**.
4. وافق على الشروط، ثم حدد **تثبيت**.

قد تستغرق الوظيفة الإضافية عدة دقائق لتثبيتها.

## <a name="feedback-and-support"></a>الملاحظات والدعم

إذا كنت مهتمًا بتقديم الملاحظات أو تحتاج إلى الدعم، فأرسل بريدًا الكترونيًا إلى [‏‫Finance insights](mailto:fiap@microsoft.com)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
