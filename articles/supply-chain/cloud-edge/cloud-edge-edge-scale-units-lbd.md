---
title: انشر وحدات مقياس الحافة على أجهزة مخصصة باستخدام LBD (الإصدار الأولي)
description: يشرح هذا الموضوع كيفيه توفير وحدات مقياس الحافة المحلية باستخدام الاجهزه والتوزيع المخصص الذي يستند إلى بيانات العمل المحلية (LBD).
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ebbdaab9d6f040497d3158db2712e102b6e9aa8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678971"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a>انشر وحدات مقياس الحافة على أجهزة مخصصة باستخدام LBD (الإصدار الأولي)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)] <!--KFM: Until 11/1/2021 -->

تعمل وحدات مقياس الحافة علي تشغيل دور مهم في المخطط المختلط الموزع لـ supply chain management. في المخطط المختلط ، يمكنك توزيع أحمال الابعاد بين Supply Chain Management ووحدات المقياس الاضافيه في السحابة أو علي الحافة.

يمكن نشر وحدات مقياس الحافة بواسطة إنشاء بيئة بيانات عمل محليه (LBD) [علي بيئة محليه](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md)ثم تكوينها لتعمل كوحدة قياس في المخطط المختلط الموزع لـ supply chain management. ويتم تحقيق ذلك عن طريق اقران بيئة LBD الداخلية ببيئة Supply Chain Management في السحابة ، التي تم تكوينها لتعمل كلوحه وصل.  

وحدات مقياس الحافة قيد المعاينة حاليا. ولذلك ، يمكنك استخدام بيئة من هذا النوع فقط وفقا [لشروط المعاينة](https://aka.ms/scmcnepreviewterms).

يصف هذا الموضوع كيفيه اعداد بيئة LBD الداخلية كوحدة مقياس حافه ثم ربطها بأحدي الموزعات.

## <a name="deployment-overview"></a>نظرة عامة حول النشر

وفيما يلي نظرة عامة على خطوات النشر.

1. **تمكين فتحه LBD في مشروع LBD الخاص بك في Microsoft Dynamics Lifecycle Services (LCS)**

    اثناء المعاينة ، LBD الحافة التي تستهدف وحدات مقياس الحافة عملاء LBD الموجودة. سيتم توفير فتحه بيئة الاختبار المعزولة لتحديد صلاحيات LBD الاضافيه 60 يومًا في مواقف محدده للعميل فقط.

1. **يستخدم في اعداد بيئة لبد ونشرها مع قاعده بيانات *فارغه*.**

    استخدم LCS لنشر بيئة LBD بأحدث طبولوجيا وقاعده بيانات فارغه. لمزيد من المعلومات ، راجع [اعداد بيئة LBD ونشرها باستخدام مقطع قاعده بيانات فارغ](#set-up-deploy) لاحقا في هذا الموضوع. يجب استخدام إصدار 10.0.19 من Supply Chain Management مع النظام الأساسي 43 أو اعلي عبر بيئات الوصل ووحده المقياس.

1. **تحميل الحزم الهدف إلى أصول LBD في المشروع في LCS.**

    اعداد التطبيق والنظام الأساسي وحزم التخصيص التي تستخدمها عبر الموزع ووحده مقياس الحافة. لمزيد من المعلومات ، راجع قسم [تحميل الحزم الهدف إلى أصول مشروع LBD في LCS](#upload-packages) لاحقا في هذا الموضوع.

1. **خدمه البيئة LBD مع الحزم الهدف.**

    وتضمن هذه الخطوة نشر نفس البنية والتخصيصات علي لوحه الوصل والوصلات. لمزيد من المعلومات ، راجع القسم [قم بصيانة بيئة LBD الخاصة بحزم الهدف](#service-target-packages) لاحقا في هذا الموضوع.

1. **أكمل تكوين وحده القياس وتعيين حمل العمل.**

    لمزيد من المعلومات ، راجع [تعيين وحده مقياس LBD الخاصة بك علي قسم لوحه وصل](#assign-edge-to-hub) لاحقا في هذا الموضوع.

توفر المقاطع المتبقية من هذا الموضوع تفاصيل إضافية حول كيفية إكمال هذه الخطوات.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>يستخدم في اعداد بيئة لبد ونشرها مع قاعده بيانات فارغه.

تعمل هذه الخطوة علي إنشاء بيئة LBD وظيفية. ومع ذلك ، لا تكون البيئة بالضرورة لديها نفس إصدارات التطبيق والنظام الأساسي كبيئة الموزع. بالاضافه إلى ذلك ، فان هذه التخصيصات لا تزال مفقوده ، ولم يتم تمكينها بعد للعمل كوحدة قياس.

1. اتبع الإرشادات في [إعداد البيئات المحلية ونشرها (تحديث Platform update 41 وتحديث لاحق)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). يجب استخدام إصدار 10.0.19 من Supply Chain Management مع النظام الأساسي 43 أو اعلي عبر بيئات الوصل ووحده المقياس

    > [!IMPORTANT]
    > أقرا باقي هذا القسم **قبل** إكمال الخطوات الواردة في هذا الموضوع.

1. قبل وصف التكوين الخاص بك في ملف ConfigTemplate.xml\\للبنية التحتية، قم بتشغيل البرنامج النصي التالي:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > سيقوم هذا البرنامج النصي بازاله اي تكوين غير مطلوب لنشر وحدات مقياس الحافة.

1. قم باعداد قاعده بيانات تحتوي علي بيانات فارغه ، كما هو موضح في [تكوين قواعد البيانات](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). استخدم ملف data.bak فارغا لهذه الخطوة.
1. اعداد البرنامج النصي الخاص بما قبل النشر. للحصول على مزيد من المعلومات، راجع [البرامج النصية لما قبل النشر وما بعد النشر للوكيل المحلي](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. قم بنسخ المحتويات من المجلد **ScaleUnit** في **البرامج النصية للبنية الاساسيه** إلى مجلد **البرامج النصية** في مشاركه مخزن ملفات الوكيل التي تم اعدادها في البيئة. المسار النموذجي هو \\\\lbdiscsi01\\agent\\Scripts.
    2. قم بإنشاء البرنامج النصي **PreDeployment.ps1** الذي سيستدعي البرامج النصية باستخدام المعلمات المطلوبة. يجب وضع البرنامج النصي للنشر المسبق في مجلد **البرامج النصية** في مشاركه مخزن ملفات العميل. والا ، فلا يمكن تشغيله. المسار النموذجي هو \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        ستشبه محتويات البرنامج النصي PreDeployment.ps1 المثال التالي.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
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

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>تحميل الحزم الهدف إلى أصول LBD في المشروع في LCS

تقوم هذه الخطوة بتحضير إصدار التطبيق وإصدار النظام الأساسي والتخصيصات التي سيتم تحويلها إلى بيئة وحده مقياس LBD.

1. تحميل نفس حزمه التطبيق/النظام الأساسي المجمعة التي تم تطبيقها علي بيئة الوصل في مكتبه الأصول للمشروع LCS المحلي.
1. احصل على نسخة من الحزمه القابلة للنشر والمخصصة التي تم تطبيقها علي بيئة الوصل في مكتبه الأصول للمشروع LCS المحلي.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>خدمه البيئة LBD مع الحزم الهدف

تقوم هذه الخطوة بمحاذاة إصدار التطبيق وإصدار النظام الأساسي والتخصيصات في بيئة وحده مقياس LBD باستخدام لوحة الوصل.

1. قم بخدمه البيئة LBD باستخدام حزمه التطبيق/النظام الأساسي المجمعة التي قمت بتحميلها في الخطوة السابقة.
1. قم بخدمه البيئة LBD باستخدام الحزمه القابلة للنشر والمخصصة التي قمت بتحميلها في الخطوة السابقة.

    ![تحديد الاحتفاظ > تطبيق التحديثات في LCS.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "تحديد الاحتفاظ > تطبيق التحديثات في LCS")

    ![تحديد حزمه التخصيص الخاصة بك.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "تحديد حزمه التخصيص الخاصة بك")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>تعيين وحده مقياس LBD الخاصة بك علي لوحه وصل

بينما لا تزال وحدات مقياس الحافة في حاله المعاينة ، يجب استخدام [أدوات التكوين ونشر وحده القياس](https://github.com/microsoft/SCMScaleUnitDevTools) المتوفرة في GitHub لتعيين وحده مقياس LBD الخاصة بك إلى لوحه وصل. تقوم العملية بتمكين تكوين LBD لتعمل كوحدة مقياس حافه وربطها بلوحه الوصل. وتتشابه العملية مع تكوين بيئة تطوير من المربع الواحد.

1. قم بتنزيل أحدث إصدار من [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases) وفك ضغط محتويات الملف.
1. قم بإنشاء نسخه من ملف `UserConfig.sample.xml` ثم قم بتسميته `UserConfig.xml`.
1. قم بإنشاء تطبيق Microsoft Azure Active Directory (Azure AD) في مستاجر Azure AD الخاص بك ، كما هو موضح في [دليل النشر لوحده القياس وأحمال العمليات](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations).
    1. بمجرد إنشاء ، انتقل إلى نموذج التطبيقات Azure AD (SysAADClientTable) علي لوحه الوصل الخاصة بك.
    1. قم بإنشاء إدخال جديد وقم بتعيين **معرف العميل** إلى المعرف الخاص بالتطبيق الذي قمت بإنشاءه. قم بتعيين **الاسم** إلى *ScaleUnits* و **معرف المستخدم** إلى *المسؤول*.

1. قم بإنشاء تطبيق خدمه الاتحاد الموحد لـ Active directory (AD FS) كما هو موضح في [دليل النشر لوحده القياس وأحمال العمليات](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations).
    1. بمجرد إنشاء ، انتقل إلى نموذج التطبيقات Azure AD (SysAADClientTable) علي وحدة مقياس الحافة الخاصة بك.
    1. قم بإنشاء إدخال جديد وقم بتعيين **معرف العميل** إلى المعرف الخاص بالتطبيق الذي قمت بإنشاءه. عيّن **معرف التطبيق** إلى *المسؤول*.

1. قم بتعديل ملف `UserConfig.xml`.
    1. أسفل قسم `InterAOSAADConfiguration`، ادخل المعلومات من تطبيق Azure AD الذي قمت بإنشاءه سابقا.
        - في العنصر `AppId`، ادخل معرف التطبيق الخاص بتطبيق Azure.
        - في العنصر `AppSecret`، ادخل سر التطبيق الخاص بتطبيق Azure.
        - يجب ان يحتوي العنصر `Authority` علي عنوان URL يحدد تخويل الأمان للمستاجر الخاص بك.

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. أسفل القسم `ScaleUnitConfiguration`، بالنسبة لأول `ScaleUnitInstance` ، قم بتعديل القسم `AuthConfiguration`.
        - في العنصر `AppId`، ادخل معرف التطبيق الخاص بتطبيق Azure.
        - في العنصر `AppSecret`، ادخل سر التطبيق الخاص بتطبيق Azure.
        - يجب ان يحتوي العنصر `Authority` علي عنوان URL يحدد تخويل الأمان للمستاجر الخاص بك.

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. قم بتعيين القيم التالية لـ `ScaleUnitInstance` نفسه:
        - في العنصر `Domain`، حدد عنوان URL للوحه الوصل الخاصة بك. على سبيل المثال: `https://cloudhub.sandbox.operations.dynamics.com/`
        - في العنصر `EnvironmentType`، تاكد من تعيين القيمة `LCSHosted`.

    1. أسفل القسم `ScaleUnitConfiguration`، بالنسبة لثاني `ScaleUnitInstance` ، قم بتعديل القسم `AuthConfiguration`.
        - في العنصر `AppId`، ادخل معرف التطبيق الخاص بتطبيق AD FS.
        - في العنصر `AppSecret`، ادخل سر التطبيق الخاص بتطبيق ADFS.
        - يجب ان يحتوي العنصر `Authority` علي محدد موقع المعلومات الخاص بمثيل AD FS الخاص بك.

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. قم بتعيين القيم التالية لـ `ScaleUnitInstance` نفسه:
        - في العنصر `Domain`، حدد عنوان URL لوحدة مقياس الحافة. على سبيل المثال: https://ax.contoso.com/
        - في العنصر `EnvironmentType`، تاكد من تعيين قيمة LBD.
        - في العنصر `ScaleUnitId`، ادخل نفس القيمة التي قمت بتحديدها لـ `InstanceId` عند تكوين البرنامج النصي قبل النشر `Configure-CloudandEdge.ps1`.

        > [!NOTE]
        > إذا لم تستخدم المعرف الافتراضي (@A) ، فتاكد من تحديث ScaleUnitId لكل ConfiguredWorkload تحت قسم أحمال الحدث.

1. افتح PowerShell وانتقل إلى المجلد الذي يحتوي علي الملف `UserConfig.xml`.

1. قم بتشغيل الاداه مع هذا الأمر.

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > بعد كل اجراء سيتعين عليك بدء تشغيل الاداه مره أخرى.

1. في الاداه ، حدد **2. تحضير البيئات لتثبيت حمل العمل**. بعد ذلك يلزم تشغيل الخطوات التالية:
    1. حدد **1. تحضير لوحه الوصل**.
    1. حدد **2. قم باعداد وحده المقياس**.

    > [!NOTE]
    > إذا لم تقم بتشغيل هذا الأمر من التثبيت النظيف وفشل التثبيت ، فقم بالإجراءات التالية:
    >
    > - قم بازاله كافة المجلدات من المجلد `aos-storage` (فيما عدا الخاص ب `GACAssemblies`).
    > - قم بتشغيل أمر SQL التالي علي قاعده بيانات الاعمال (AXDB):
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. قم بتشغيل أوامر SQL التالي علي قاعده بيانات الاعمال (AXDB):

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. التحقق من تمكين تعقب التغييرات علي قاعده بيانات الاعمال (AXDB)
    1. بدء تشغيل SQL Server Management Studio (SSMS).
    1. انقر بزر الماوس الأيمن فوق قاعده بيانات الاعمال الخاصة بك (AXDB) وحدد خصائص.
    1. في الإطار الذي يتم فتحه ، حدد **تعقب التغيير** وقم باجراء الإعدادات التالية:

        - **تعقب التغييرات:** *صحيح*
        - **فتره الاستبقاء:** *7*
        - **وحدات الاستبقاء:** *الأيام*
        - **التنظيف التلقائي:** *صحيح*

1. في الاداه ، حدد **3. تثبيت أحمال الأحمال**. بعد ذلك يلزم تشغيل الخطوات التالية:
    1. حدد **1. تثبيت علي لوحه الوصل**.
    1. حدد **2. قم بالتثبيت علي وحده المقياس**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
