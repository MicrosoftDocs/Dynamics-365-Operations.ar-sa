---
title: انشر وحدات مقياس الحافة على أجهزة مخصصة باستخدام LBD
description: يشرح هذا الموضوع كيفيه توفير وحدات مقياس الحافة المحلية باستخدام الاجهزه والتوزيع المخصص الذي يستند إلى بيانات العمل المحلية (LBD).
author: Mirzaab
ms.date: 01/24/2022
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 540ac1f6d69d869256f49b8501e18966575903fa
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674075"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>انشر وحدات مقياس الحافة على أجهزة مخصصة باستخدام LBD

[!include [banner](../includes/banner.md)]

تعمل وحدات مقياس الحافة علي تشغيل دور مهم في المخطط المختلط الموزع لـ supply chain management. في المخطط المختلط ، يمكنك توزيع أحمال الابعاد بين Supply Chain Management ووحدات المقياس الاضافيه في السحابة أو علي الحافة.

يمكن نشر وحدات مقياس الحافة بواسطة إنشاء بيئة بيانات عمل محليه (LBD) [علي بيئة محليه](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md)ثم تكوينها لتعمل كوحدة قياس في المخطط المختلط الموزع لـ supply chain management. ويتم تحقيق ذلك عن طريق اقران بيئة LBD الداخلية ببيئة Supply Chain Management في السحابة ، التي تم تكوينها لتعمل كلوحه وصل.  

يصف هذا الموضوع كيفيه اعداد بيئة LBD الداخلية كوحدة مقياس حافه ثم ربطها بأحدي الموزعات.

## <a name="infrastructure-considerations"></a>اعتبارات البنية الأساسية

يتم تشغيل وحدات قياس الحافة في بيئات محلية، بحيث تكون متطلبات البنية الأساسية متشابهة تمامًا. ومع ذلك، توجد بعض الاختلافات التي يجب ملاحظتها:

- لا تستخدم وحدات قياس الحافة Financial Reporting، لذا فهي لا تتطلب عُقد Financial Reporting.
- لا تتطلب أحمال عمل التخزين والتصنيع حوسبة مكثفة، وبالتالي يمكنك تغيير حجم قوة الحوسبة في عُقد AOS وفقًا لذلك.

## <a name="deployment-overview"></a>نظرة عامة حول النشر

وفيما يلي نظرة عامة على خطوات النشر.

1. **تمكين فتحه LBD في مشروع LBD الخاص بك في Microsoft Dynamics Lifecycle Services (LCS)**

1. **يستخدم في اعداد بيئة لبد ونشرها مع قاعده بيانات *فارغه*.**

    استخدم LCS لنشر بيئة LBD بأحدث طبولوجيا وقاعده بيانات فارغه. لمزيد من المعلومات ، راجع [اعداد بيئة LBD ونشرها باستخدام مقطع قاعده بيانات فارغ](#set-up-deploy) لاحقا في هذا الموضوع. يجب عليك استخدام Supply Chain Management الإصدار 10.0.21 أو إصدارًا أحدث عبر بيئات وحدة القياس والمركز.

1. **تحميل الحزم الهدف إلى أصول LBD في المشروع في LCS.**

    اعداد التطبيق والنظام الأساسي وحزم التخصيص التي تستخدمها عبر الموزع ووحده مقياس الحافة. لمزيد من المعلومات ، راجع قسم [تحميل الحزم الهدف إلى أصول مشروع LBD في LCS](#upload-packages) لاحقا في هذا الموضوع.

1. **خدمه البيئة LBD مع الحزم الهدف.**

    وتضمن هذه الخطوة نشر نفس البنية والتخصيصات علي لوحه الوصل والوصلات. لمزيد من المعلومات ، راجع القسم [قم بصيانة بيئة LBD الخاصة بحزم الهدف](#service-target-packages) لاحقا في هذا الموضوع.

1. **أكمل تكوين وحده القياس وتعيين حمل العمل.**

    لمزيد من المعلومات ، راجع [تعيين وحده مقياس LBD الخاصة بك علي قسم لوحه وصل](#assign-edge-to-hub) لاحقا في هذا الموضوع.

توفر المقاطع المتبقية من هذا الموضوع تفاصيل إضافية حول كيفية إكمال هذه الخطوات.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>يستخدم في اعداد بيئة لبد ونشرها مع قاعده بيانات فارغه.

تعمل هذه الخطوة علي إنشاء بيئة LBD وظيفية. ومع ذلك ، لا تكون البيئة بالضرورة لديها نفس إصدارات التطبيق والنظام الأساسي كبيئة الموزع. بالاضافه إلى ذلك ، فان هذه التخصيصات لا تزال مفقوده ، ولم يتم تمكينها بعد للعمل كوحدة قياس.

1. اتبع الإرشادات في [إعداد البيئات المحلية ونشرها (تحديث Platform update 41 وتحديث لاحق)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). يجب عليك استخدام Supply Chain Management الإصدار 10.0.21 أو إصدارًا أحدث عبر بيئات وحدة القياس والمركز. بالإضافة إلى ذلك ، يجب عليك استخدام الإصدار 2.12.0 أو أحدث من البرامج النصية للبنية التحتية. 

    > [!IMPORTANT]
    > أقرا باقي هذا القسم **قبل** إكمال الخطوات الواردة في هذا الموضوع.

1. قبل وصف التكوين الخاص بك في ملف ConfigTemplate.xml\\للبنية التحتية، قم بتشغيل البرنامج النصي التالي:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > سيقوم هذا البرنامج النصي بازاله اي تكوين غير مطلوب لنشر وحدات مقياس الحافة.

1. قم باعداد قاعده بيانات تحتوي علي بيانات فارغه ، كما هو موضح في [تكوين قواعد البيانات](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). استخدم ملف data.bak فارغا لهذه الخطوة.
1. بعد إكمال خطوة [تكوين قواعد البيانات](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb)، قم بتشغيل البرنامج النصي التالي لتكوين قاعدة بيانات Scale Unit Alm Orchestrator.

    > [!NOTE]
    > لا تقم بتكوين قاعدة بيانات Financial Reporting أثناء خطوة [تكوين قواعد البيانات](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb).

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    يقوم البرنامج النصي Initialize-Database.ps1 بتنفيذ الإجراءات التالية:

    1. قم بإنشاء قاعدة بيانات فارغة تسمى **ScaleUnitAlmDb**.
    2. قم بتعيين المستخدمين لأدوار قاعدة البيانات ، بناءً على الجدول التالي.

        | المستخدم            | النوع | دور قاعدة البيانات |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | db\_owner     |

1. واصل اتباع الإرشادات في [إعداد البيئات المحلية ونشرها (تحديث Platform update 41 وتحديث لاحق)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md).
1. بعد إكمال خطوة [تكوين AD FS](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb)، اتبع الخطوات التالية:

    1. أنشئ تطبيقًا جديدًا لخدمات اتحاد الدليل النشط (AD FS) والذي سيمكن خدمة Alm Orchestration من التواصل مع خادم كائن التطبيق (AOS).

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. أنشئ تطبيق Azure Active Directory (Azure AD) جديدًا سيُمكّن خدمة Alm Orchestration من التواصل مع خدمة إدارة وحدة القياس.

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. واصل اتباع الإرشادات في [إعداد البيئات المحلية ونشرها (تحديث Platform update 41 وتحديث لاحق)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). عندما يتعين عليك إدخال التكوين للوكيل المحلي ، تأكد من تمكين ميزات وحدة مقياس الحافة وتوفير جميع المعلمات المطلوبة.

    ![تمكين ميزات Edge Scale Unit.](media/EnableEdgeScaleUnitFeatures.png "تمكين ميزات Edge Scale Unit.")

1. قبل نشر بيئتك من LCS، قم بإعداد البرنامج النصي للنشر المسبق. للحصول على مزيد من المعلومات، راجع [البرامج النصية لما قبل النشر وما بعد النشر للوكيل المحلي](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. قم بنسخ برنامج نصي Configure-CloudAndEdge.ps1 من المجلد **ScaleUnit** في **البرامج النصية للبنية الاساسيه** إلى مجلد **البرامج النصية** في مشاركه مخزن ملفات الوكيل التي تم اعدادها في البيئة. المسار النموذجي هو \\\\lbdiscsi01\\agent\\Scripts.
    2. قم بإنشاء البرنامج النصي **PreDeployment.ps1** الذي سيستدعي البرامج النصية باستخدام المعلمات المطلوبة. يجب وضع البرنامج النصي للنشر المسبق في مجلد **البرامج النصية** في مشاركه مخزن ملفات العميل. والا ، فلا يمكن تشغيله. المسار النموذجي هو \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        ستشبه محتويات البرنامج النصي PreDeployment.ps1 المثال التالي.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
        ```

        > [!NOTE]
        > يجب ان تكون معلمه InstanceId حرفين فقط. الحرف الأول هو @ والثاني يمكن ان يكون حرفا كبيرا في الابجديه الانجليزيه.
        >
        > - قيم صالحة:
        >   - @D
        >   - @X
        > - قيم غير صالحة:
        >   - @a
        >   - @4
        >   - @#

1. نشر البيئة باستخدام أحدث طبولوجيا أساسيه متوفرة.
1. بعد نشر بيئتك ، اتبع الخطوات التالية:

    1. قم بتشغيل أوامر SQL التالي علي قاعده بيانات الاعمال (AXDB).

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. قم بزيادة الحد الأقصى لجلسة الدُفعات المتزامنة إلى قيمة تزيد على 4.

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. التحقق من تمكين تعقب التغييرات علي قاعده بيانات الاعمال (AXDB).

        1. افتح SQL Server Management Studio ‏(SSMS).
        1. حدد مع الاستمرار (أو انقر بزر الماوس الأيمن فوق) قاعدة بيانات الأعمال الخاصة بك (AXDB)، ثم حدد **خصائص**.
        1. في النافذة التي تظهر ، حدد **تعقب التغييرات**، ثم قم بتعيين القيم التالية:

            - **تعقب التغييرات:** *صحيح*
            - **فتره الاستبقاء:** *7*
            - **وحدات الاستبقاء:** *الأيام*
            - **التنظيف التلقائي:** *صحيح*

    1. أضف معرف تطبيق AD FS الذي قمت بإنشائه مسبقًا (باستخدام البرنامج النصي Create-ADFSServerApplicationForEdgeScaleUnits.ps1) إلى جدول تطبيقات Azure AD في وحدة القياس الخاصة بك. يمكنك إكمال هذه الخطوة يدويًا من خلال واجهة المستخدم (UI). بدلاً من ذلك ، يمكنك إكماله من خلال قاعدة البيانات باستخدام البرنامج النصي التالي.

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a>قم بإعداد مخزن مفاتيح Azure وتطبيق Azure AD لتمكين الاتصال بين وحدات القياس

1. بعد نشر بيئتك ، قم بإنشاء تطبيق Azure AD إضافي لتمكين الاتصال الموثوق به بين الموزع ووحدة القياس.

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. بعد إنشاء التطبيق ، يجب عليك إنشاء سر للعميل وحفظ المعلومات في مخزن مفاتيح Azure. بالإضافة إلى ذلك ، يجب منح حق الوصول إلى تطبيق Azure AD الذي تم إنشاؤه ، حتى يتمكن من استرداد الأسرار المخزنة في مخزن المفاتيح. من أجل راحتك ، سيقوم البرنامج النصي التالي تلقائيًا بتنفيذ جميع الإجراءات المطلوبة.

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > إذا لم يكن هناك خزنة مفاتيح تحتوي على القيمة المحددة **KeyVaultName** ، يقوم البرنامج النصي بإنشاء واحدة تلقائيًا.

1. أضف معرّف تطبيق Azure AD الذي أنشأته للتو (عند استخدام البرنامج النصي Create-SpokeToHubAADApplication.ps1) إلى جدول تطبيقات Azure AD في المحور الخاص بك. يمكنك إكمال هذه الخطوة يدويًا من خلال واجهة المستخدم (UI).

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>تحميل الحزم الهدف إلى أصول LBD في المشروع في LCS

تقوم هذه الخطوة بتحضير إصدار التطبيق وإصدار النظام الأساسي والتخصيصات التي سيتم تحويلها إلى بيئة وحده مقياس LBD.

1. تحميل نفس حزمه التطبيق/النظام الأساسي المجمعة التي تم تطبيقها علي بيئة الوصل في مكتبه الأصول للمشروع LCS المحلي.
1. احصل على نسخة من الحزمه القابلة للنشر والمخصصة التي تم تطبيقها علي بيئة الوصل في مكتبه الأصول للمشروع LCS المحلي.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>خدمه البيئة LBD مع الحزم الهدف

تقوم هذه الخطوة بمحاذاة إصدار التطبيق وإصدار النظام الأساسي والتخصيصات في بيئة وحده مقياس LBD باستخدام لوحة الوصل.

1. قم بخدمه البيئة LBD باستخدام حزمه التطبيق/النظام الأساسي المجمعة التي قمت بتحميلها في الخطوة السابقة.
1. قم بخدمه البيئة LBD باستخدام الحزمه القابلة للنشر والمخصصة التي قمت بتحميلها في الخطوة السابقة.

    ![تطبيق التحديثات في LCS.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "تطبيق التحديثات في LCS")

    ![تحديد حزمه التخصيص الخاصة بك.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "تحديد حزمه التخصيص الخاصة بك")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>تعيين وحده مقياس LBD الخاصة بك علي لوحه وصل

يمكنك تكوين وحدة مقياس الحافة وإدارتها من خلال مدخل إدارة وحدة القياس. لمزيد من المعلومات، راجع [إدارة وحدات القياس وأحمال العمل باستخدام مدخل إدارة وحدة القياس](./cloud-edge-landing-page.md#scale-unit-manager-portal).

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
