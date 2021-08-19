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
ms.openlocfilehash: 8faae53f66c069c53609dee72fa30ca18a22c9eb8a86b4669c745c00976af34d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742694"
---
# <a name="inventory-visibility-add-in"></a>الوظيفة الإضافية لرؤية المخزون

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

تعد الوظيفة الإضافية لرؤية المخزون بمثابه خدمة صغيرة مستقله وقابله للتغيير بشكل كبير والتي تمكن تتبع المخزون الفعلي في الوقت الحقيقي ، مما يوفر عرضا شاملا لرؤية المخزون.

يتم تصدير كافة المعلومات المرتبطة بالمخزون الفعلي إلى الخدمة بالقرب من الوقت الحقيقي خلال تكامل SQL في المستوي المنخفض. تقوم الانظمه الخارجية بالوصول إلى الخدمة من خلال واجهات RESTful API للاستعلام عن المعلومات الفعلية حول المجموعات المحددة من الابعاد ، ومن ثم استرداد قائمه بالمناصب الفعلية المتاحة.

رؤية المخزون عبارة عن خدمة صغيرة مضمنة في Microsoft Dataverse، مما يعني انه يمكنك توسيعها بواسطة إنشاء Power Apps وتطبيق Power BI لتوفير وظيفة مخصصه لتلبيه متطلبات الاعمال الخاصة بك. من الممكن أيضا ترقيه الفهرس للقيام باستعلامات المخزون.

توفر امكانيه رؤية المخزون خيارات التكوين التي تتيح له التكامل مع أنظمه متعددة الجهات الخارجية. وهو يدعم بعد المخزون القياسي والقابلية للتوسعة المخصصة والكميات التي تم حسابها والقياسية القابلة للتكوين.

يصف هذا الموضوع كيفيه تثبيت وتكوين الوظيفة الإضافية لرؤية المخزون لـ Dynamics 365 Supply Chain Management، وكيفيه استخدام واجهه برمجه التطبيقات (API) الخاصة بها.

## <a name="install-the-inventory-visibility-add-in"></a>تثبيت الوظيفة الإضافية لرؤية المخزون

يجب تثبيت الوظيفة الإضافية لرؤية المخزون باستخدام Microsoft Dynamics Lifecycle Services (LCS). LCS عبارة عن مدخل تعاون يوفر بيئة ومجموعه من الخدمات المحدثة بشكل منتظم والتي تساعدك علي أداره دوره حياه التطبيقات الخاصة بتطبيقات Dynamics 365 Finance and Operations الخاصة بك.

للحصول على مزيد من المعلومات، راجع [موارد Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="inventory-visibility-add-in-prerequisites"></a>المتطلبات الأساسية للوظيفة الإضافية لرؤية المخزون

قبل أن تتمكن من تثبيت الوظيفة الإضافية لرؤية المخزون، يجب عليك القيام بما يلي:

- احصل علي مشروع تنفيذ LCS مع نشر بيئة واحده علي الأقل.
- تأكد من اكتمال المتطلبات الأساسية لإعداد الوظائف الإضافية المتوفرة في [نظرة عامة على الوظائف الإضافية](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). لا تتطلب رؤية المخزون ارتباطًا ثنائي الكتابة.
- تواصل مع فريق رؤية المخزون على [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) للحصول على الملفات الثلاثة المطلوبة التالية:
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - `Inventory Visibility Integration.zip` (إذا كان إصدار Supply Chain Management الذي تقوم بتشغيله أقدم من الإصدار 10.0.18)
- بدلاً من ذلك، تواصل مع فريق رؤية المخزون على [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) للحصول على حزم package deployer. يمكن استخدام هذه الحزم بواسطة أداة package deployer الرسمية.
  - `InventoryServiceBase.PackageDeployer.zip`
  - `InventoryServiceApplication.PackageDeployer.zip` (تحتوي هذه الحزمة علي كافة التغييرات في حزم  `InventoryServiceBase`، بالإضافة إلى مكونات إضافية لتطبيق واجهة المستخدم)
- اتبع الإرشادات المذكورة في [تشغيل سريع: تسجيل تطبيق مع النظام الأساسي للهوية في Microsoft](/azure/active-directory/develop/quickstart-register-app) لتسجيل تطبيق وإضافة سر العميل ضمن اشتراكك في Azure.
  - [تسجيل تطبيق](/azure/active-directory/develop/quickstart-register-app)
  - [إضافة سر عميل](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - سيتم استخدام **معرف التطبيق (العميل)** و **سر العميل** و **معرف المستأجر** في الخطوات التالية.

> [!NOTE]
> تتضمن البلدان والمناطق المدعومة حاليًا كندا والولايات المتحدة والاتحاد الأوروبي (EU).

إذا كانت لديك إيه اسئله حول هذه المتطلبات الاساسيه ، الرجاء الاتصال بفريق رؤية المخزون.

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>إعداد Dataverse

لإعداد Dataverse للاستخدام مع رؤية المخزون، يجب أولاً إعداد المتطلبات الأساسية ثم تحديد ما إذا كان سيتم إعداد Dataverse باستخدام إما أداة package deployer أو عن طريق استيراد الحلول يدويًا (ليس من الضروري القيام بكلاهما). ثم قم بتثبيت الوظيفة الإضافية لرؤية المخزون. تصف الأقسام الفرعية التالية كيفية إكمال كل مهمة من هذه المهام.

#### <a name="prepare-dataverse-prerequisites"></a>تحضير المتطلبات Dataverse الأساسية

قبل البدء في إعداد Dataverse، قم بإضافة مبدأ الخدمة للمستأجر الخاص بك عن طريق القيام بما يلي:

1. قم بتثبيت Azure AD الوحدة النمطية PowerShell الإصدار 2 كما هو موضح في [تثبيت Azure Active Directory PowerShell للرسم البياني](/powershell/azure/active-directory/install-adv2).

1. قم بتشغيل الأمر PowerShell التالي:

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a>إعداد Dataverse باستخدام الأداة package deployer

بعد الحصول على المتطلبات الأساسية، استخدم الإجراء التالي إذا كنت تفضل إعداد Dataverse باستخدام أداة package deployer. راجع القسم التالي للحصول على تفاصيل حول كيفية استيراد الحلول يدويًا بدلاً من ذلك (عدم القيام بكلاهما).

1. قم بتثبيت أدوات المطور كما هو موضح في [أدوات التنزيل من NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).

1. وبناءً على متطلبات الأعمال، اختر الحزمة `InventoryServiceBase` أو `InventoryServiceApplication`.

1. استيراد الحلول:
    1. للحزمة `InventoryServiceBase`:
        - إلغاء الضغط `InventoryServiceBase.PackageDeployer.zip`
        - البحث عن المجلد `InventoryServiceBase` والملف `[Content_Types].xml` والملف `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll` والملف `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` والملف `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`. 
        - قم بنسخ كل من هذه المجلدات والملفات إلى الدليل `.\Tools\PackageDeployment`، والذي تم إنشاؤه عند تثبيت أدوات المطور.
    1. للحزمة `InventoryServiceApplication`:
        - إلغاء الضغط `InventoryServiceApplication.PackageDeployer.zip`
        - البحث عن المجلد `InventoryServiceApplication` والملف `[Content_Types].xml` والملف `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll` والملف `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` والملف `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.
        - قم بنسخ كل من هذه المجلدات والملفات إلى الدليل `.\Tools\PackageDeployment`، والذي تم إنشاؤه عند تثبيت أدوات المطور.
    1. قم بتنفيذ `.\Tools\PackageDeployment\PackageDeployer.exe`. اتبع الإرشادات التي تظهر على الشاشة لاستيراد الحلول.

1. قم بتعيين أدوار أمان لمستخدم التطبيق.
    1. افتح عنوان URL الخاص ببيئة Dataverse الخاصة بك.
    1. انتقل إلى **إعدادات متقدمة \> النظام \> الأمان \> المستخدمين**، والبحث عن مستخدم باسم **# InventoryVisibility**.
    1. حدد **تعيين دور**، ثم حدد **مسؤول النظام**. إذا كان هناك دور يسمي **مستخدم Common Data Service**، فحدده أيضًا.

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a>إعداد Dataverse يدويًا عن طريق استيراد الحلول

بعد الحصول على المتطلبات الأساسية، استخدم الإجراء التالي إذا كنت تفضل إعداد Dataverse عن طريق استيراد الحلول يدويًا. راجع القسم السابق للحصول على تفاصيل حول كيفية استخدام أداة package deployer بدلاً من (لا تقم بكلاهما).

1. إنشاء مستخدم تطبيق لرؤية المخزون في Dataverse:

    1. افتح عنوان URL الخاص ببيئة Dataverse الخاصة بك.
    1. انتقل إلى **إعدادات متقدمة \> النظام \> الأمان \> المستخدمين**، وقم بإنشاء مستخدم تطبيق. استخدم القائمة عرض لتغيير طريقة عرض الصفحة إلى **مستخدمي التطبيق**.
    1. حدد **جديد**. عيّن معرف التطبيق إلى *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*. (سيتم تحميل مُعرّف الكائن تلقائيًا عند حفظ التغييرات الخاصة بك.) يمكنك تخصيص الاسم. على سبيل المثال، يمكنك تغييره إلى *رؤية المخزون*. عند الانتهاء، حدد **حفظ**.
    1. حدد **تعيين دور**، ثم حدد **مسؤول النظام**. إذا كان هناك دور يسمي **مستخدم Common Data Service**، فحدده أيضًا.

    لمزيد من المعلومات، راجع [إنشاء مستخدم تطبيق](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

1. إذا لم تكن لغة Dataverse  الافتراضية اللغة **الإنجليزية**:

    1. انتقل إلى **إعداد متقدم \> الإدارة \> اللغات**.
    1. حدد **الإنجليزية (LanguageCode=1033)** وحدد **تطبيق**.

1. قم باستيراد الملف `Inventory Visibility Dataverse Solution.zip`، الذي يتضمن تكوين Dataverse المرتبط بالكيانات و Power Apps:

    1. انتقل إلى الصفحة **حلول**.
    1. حدد **استيراد**.

1. استيراد تدفق مشغل ترقية التكوين:

    1. انتقل إلى الصفحة Microsoft Flow.
    1. تأكد من وجود الاتصال المسمى *Dataverse (قديم)*. (إذا لم يكن موجودًا، فقم بإنشاءه).
    1. استيراد الملف `Inventory Visibility Configuration Trigger.zip`. وبعد استيراده، سيظهر المشغل ضمن **التدفقات الخاصة بي**.
    1. قم بتهيئة المتغيرات الأربعة التالية استنادًا إلى معلومات البيئة:

        - مُعرّف مستأجر Azure
        - معرف عميل تطبيق Azure
        - سر عميل تطبيق Azure
        - نقطة نهاية رؤية المخزون

            لمزيد من المعلومات حول هذا المتغير، راجع القسم [إعداد تكامل رؤية المخزون](#setup-inventory-visibility-integration) لاحقًا في هذا الموضوع.

        ![مشغل التكوين.](media/configuration-trigger.png "مشغل التكوين")

    1. حدد **تشغيل**

### <a name="install-the-add-in"></a><a name="install-add-in"></a>تثبيت الوظيفة الإضافية

لتثبيت الوظيفة الإضافية لرؤية المخزون، يجب عليك القيام بما يلي:

1. سجل الدخول إلى بوابة [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. في الصفحة الرئيسية ، حدد المشروع حيث يتم نشر البيئة الخاصة بك.
1. في الصفحة المشروع ، حدد البيئة التي ترغب في تثبيت الوظيفة الإضافية بها.
1. في الصفحة البيئة، قم بالتمرير لأسفل حتى تشاهد القسم **الوظائف الإضافية الخاصة بالبيئة** في القسم **Power Platform تكامل**، حيث يمكنك العثور على اسم بيئة Dataverse.
1. في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.

    ![صفحة البيئة في LCS.](media/inventory-visibility-environment.png "صفحة البيئة في LCS")

1. حدد الرابط **تثبيت وظيفة إضافية جديدة**. يتم فتح قائمه بالوظائف الإضافية المتاحة.
1. حدد **رؤية المخزون** في القائمة.
1. ادخل قيما للحقول التالية الخاصة ببيئتك:

    - **مُعرّف تطبيق AAD (العميل)**
    - **معرف مستأجر AAD**

    ![صفحة إعداد الوظيفة الإضافية](media/inventory-visibility-setup.png "صفحه إعداد الوظيفة الإضافية")

1. الموافقة علي البنود والشروط عن طريق تحديد خانه الاختيار **البنود والشروط**.
1. حدد **تثبيت**. ستظهر حاله الوظيفة الإضافية باعتبارها **قيد التثبيت**. عند الانتهاء ، قم بتحديث الصفحة لرؤية تغيير الحالة علي **مثبت**.

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a>إلغاء تثبيت الوظيفة الإضافية

للغاء تثبيت الوظيفة الإضافية ، حدد **إلغاء التثبيت**. عندما تقوم بتحديث LCS، فإنه ستتم إزالة الوظيفة الإضافية لرؤية المخزون. تقوم عمليه إزالة التثبيت على إزالة تسجيل الوظيفة الإضافية وبدء مهمة أيضًا لتنظيف كافة بيانات الشركات المخزنة في الخدمة.

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a>استخدام بيانات المخزون الفعلي من Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>توزيع حزمة تكامل رؤية المخزون

إذا كنت تقوم بتشغيل Supply Chain Management الإصدار 10.0.17 أو إصدار سابق عنه، فتواصل بفريق دعم رؤية المخزون على [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) للحصول علي ملف الحزمة. ثم قم بنشر الحزمة في LCS.

> [!NOTE]
> إذا حدث خطأ عدم تطابق في الإصدار أثناء التوزيع، يجب عليك استيراد مشروع X++ يدويًا إلى بيئة التطوير الخاصة بك. ثم قم بإنشاء الحزمة القابلة للنشر في بيئة التطوير الخاصة بك، ثم قم بنشرها في بيئة الإنتاج الخاصة بك.
> 
> يتم تضمين الكود Supply Chain Management في الإصدار 10.0.18. إذا كنت تقوم بتشغيل هذا الإصدار أو الأحدث، فإن عملية النشر تكون غير ضرورية.

تأكد من أنه يتم تشغيل الميزات التالية في بيئة Supply Chain Management. (افتراضيًا، فإنه يتم تشغيلها.)

| وصف الميزة | إصدار الكود | تبديل الفئة |
|---|---|---|
| تمكين أو تعطيل استخدام أبعاد المخزون في جدول InventSum | 10.0.11 | InventUseDimOfInventSumToggle |
| تمكين أو تعطيل استخدام أبعاد المخزون في جدول InventSumDelta | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>إعداد تكامل رؤية المخزون

1. في Supply Chain Management، افتح مساحة عمل **[إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**، وقم بتشغيل الميزة **تكامل رؤية المخزون**.
1. انتقل إلى **إدارة المخزون \> الإعداد \> معلمات تكامل رؤية المخزون**، وأدخل عنوان URL للبيئة التي تقوم فيها بتشغيل رؤية المخزون.

    ابحث عن منطقة LCS الخاصة ببيئة Azure، ثم أدخل عنوان URL. يحتوي عنوان URL على النموذج التالي:

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    على سبيل المثال، إذا كنت في أوروبا، سيكون لدي البيئة واحدًا من عناوين (URL) التالية:

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    تتوفر المناطق التالية حاليًا.

    | منطقة Azure | اسم المنطقة القصير |
    |---|---|
    | شرق أستراليا | eau |
    | جنوب شرق أستراليا | seau |
    | وسط كندا | cca |
    | شرق كندا | eca |
    | شمال أوروبا | neu |
    | غرب أوروبا | weu |
    | شرق الولايات المتحدة | eus |
    | غرب الولايات المتحدة | wus |

1. انتقل إلى **إدارة المخزون \> دوري \> تكامل رؤية المخزون**، وقم بتمكين الوظيفة. سيتم الآن ترحيل كافة أحداث تغيير المخزون من Supply Chain Management إلى رؤية المخزون.

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a>واجهة API العامة للوظيفة الإضافية لرؤية المخزون

تقدم واجهة برمجة التطبيقات العامة لـ REST الخاصة بالوظيفة الإضافية لرؤية المخزون العديد من نقاط التكامل الخاصة. ويدعم ثلاثه أنواع من التفاعلات الرئيسية:

- ترحيل تغييرات المخزون الفعلية إلى الوظيفة الإضافية من نظام خارجي
- الاستعلام عن الكميات الفعلية الحالية من نظام خارجي
- مزامنة تلقائية مع مخزون Supply Chain Management الفعلي

لا تعتبر المزامنة التلقائية جزءًا من API العامة. وبدلاً من ذلك، تتم معالجتة في الخلفية للبيئات التي تم فيها تمكين الوظيفة الإضافية لرؤية المخزون.

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a>مصادقة

يتم استخدام الرمز المميز لأمان النظام الأساسي لاستدعاء الوظيفة الإضافية لرؤية المخزون. ولذلك، يجب إنشاء رمز *Azure Active Directory (Azure AD) المميز* باستخدام تطبيق Azure AD. يجب استخدام رمز Azure AD المميز للحصول على *رمز الوصول المميز* من خدمة الأمان.

احصل علي رمز خدمه أمان بالقيام بما يلي:

1. سجل دخولك إلى مدخل Azure واستخدمه للعثور على `clientId` و `clientSecret` لتطبيق Supply Chain Management.
1. إحضار Azure Active Directory رمز مميز (`aadToken`) عن طريق إرسال طلب HTTP بالخصائص التالية:
    - **عنوان URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **الطريقة** - `GET`
    - **محتوي النص الأساسي (بيانات النموذج)**:

        | المفتاح | القيمة |
        | --- | --- |
        | client_id | ${aadAppId} |
        | client_secret | ${aadAppSecret} |
        | grant_type | client_credentials |
        | مورد | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
1. يجب ان تتلقي `aadToken` استجابه فيها، والتي تشبه المثال التالي.

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

1. المستقبل طلب JSON مشابها لما يلي:

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

    المكان:
    - `client_assertion`يجب ان تكون القيمة هي `aadToken` التي استلمتها في الخطوة السابقة.
    - `context`يجب ان تكون القيمة معرف البيئة حيث تريد توزيع الوظيفة الإضافية.
    - قم بتعيين كافة القيم الأخرى كما هو موضح في المثال.

1. قم بإرسال طلب HTTP بالخصائص التالية:
    - **عنوان URL** - `https://securityservice.operations365.dynamics.com/token`
    - **الطريقة** - `POST`
    - **راس HTTP** - تضمين إصدار API (`Api-Version` المفتاح هو والقيمة هو `1.0`)
    - **محتوي أساسي** - تضمين طلب JSON الذي قمت بإنشاءه في الخطوة السابقة.

1. ستحصل علي `access_token` في الاستجابة. وهذا ما تحتاجه كرمز مميز في الحامل لاستدعاء امكانيه رؤية API للمخزون. فيما يلي مثال على ذلك.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a>عينة طلب

كمرجع لك، فيما يلي عينة طلب http، يمكنك استخدام أي أدوات أو لغة تعليمات برمجية لإرسال هذا الطلب، مثل ``Postman``.

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

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a>تكوين واجهه برمجه تطبيقات امكانيه رؤية المخزون

قبل استخدام الخدمة ، يجب إكمال التكوينات الموضحة في الأقسام الفرعية التالية. قد يختلف التكوين استنادا إلى تفاصيل البيئة الخاصة بك. وهو يتضمن بشكل أساسي أربعه أجزاء:

- [تقسيم](#partitioning)
- [تكوينات الأبعاد](#dimension-configurations)
- [فهرسة](#indexing)
- [قياس مخصص](#custom-measurement)

#### <a name="partitioning"></a>تقسيم

يمكن للتقسيم ان يؤثر بشكل كبير علي أداء واجهة API الخاصة برؤية المخزون. انها لفكره جيده ان تقوم بتعريف نظام يسمح بالتجميعات الصغيرة للبيانات مع استمرار السماح باستعلامات البيانات ذات المعني.

سيكون `organizationId` (`dataAreaId` في Supply Chain Management) دائما جزءا من التقسيم ، ويتم تعيين رؤية المخزون بشكل افتراضي علي قسم حسب الابعاد *كموقع إلكتروني + موقع جغرافي*. وهذا يعني انه يجب دوما الاستعلام عن الخدمة باستخدام هذه الابعاد المحددة في عوامل التصفية.

> [!NOTE]
> *الموقع الإلكتروني* و *الموقع الجغرافي* هما اثنان من الابعاد الافتراضية في رؤية المخزون. في Supply Chain Management، تسمي هذه الابعاد *بالموقع الإلكتروني* (`InventSiteId`) *والمستودع* (`InventLocationId`)

### <a name="dimension-configurations"></a>تكوينات الأبعاد

ستوفر امكانيه رؤية المخزون قائمه بالابعاد الافتراضية العامة لتمكين تكامل النظام المصدر المتعدد.

يسرد الجدول التالي ابعاد المخزون التي ستكون أسماء الابعاد الافتراضية في رؤية المخزون.

| نوع البعد | اسم البُعد |
|---|---|
| منتج | `ColorId` |
| منتج | `SizeId` |
| منتج | `StyleId` |
| منتج | `ConfigId` |
| التعقب | `BatchId` |
| التعقب | `SerialId` |
|  الموق | `LocationId` |
|  الموق | `SiteId` |
| حالة المخزون | `StatusId` |
| خاص بالمستودع | `WMSLocationId` |
| خاص بالمستودع | `WMSPalletId` |
| خاص بالمستودع | `LicensePlateId` |

> [!NOTE]
> يكون نوع البعد المدرج في الجدول السابق كمرجع فقط. لا يلزم تحديد نوع البعد في رؤية المخزون.

في حاله وجود بعد مخصص والحاجة إلى التدفق للقيمة الافتراضية عند استهلاك رؤية المخزون ، يمكنك تكوين **اسم البعد المخصص** في رؤية المخزون.

وصول الانظمه الخارجية إلى رؤية المخزون من خلال واجات برمجه التطبيقات RESTful التي تتيح معلومات الكمية الفعلية حول مجموعات الابعاد المحددة التي سيتم الاستعلام عنها. بالنسبة للتكامل ، يمكنك رؤية المخزون من تكوين *مصدر بيانات القناة الخارجية* وبعد المصدر علي *الابعاد المستهدفة* في رؤية المخزون.

يجب ان تكون الابعاد المستهدفة واحده مما يلي:

- الابعاد الافتراضية في رؤية المخزون
- الأبعاد المخصصة

والغرض من تكوين الابعاد هو توحيد التكامل المتعدد الانظمه للاستعلام علي الابعاد وحدث الترحيل مع الابعاد.

#### <a name="indexing"></a>فهرسة

في معظم الأوقات ، لن يكون الاستعلام الفعلي الخاص بالمخزون علي مستوي "الإجمالي" الأعلى فقط ، ولكن قد ترغب في رؤية النتائج المجمعة استنادا إلى ابعاد المخزون.

توفر امكانيه رؤية المخزون المرونة عن طريق السماح لك بإعداد الفهارس ، التي تعتمد علي البعد أو مجموعه الابعاد.

> [!NOTE]
> حاليا ، يمكنك فقط تكوين الفهارس بخمسه كحد اقصي. يجب مراعاه البعد أو مجموعه الابعاد التي ستستخدمها قبل التنفيذ للتاكد من انها ستفي باحتياجات أعمالك. علي سبيل المثال ، إذا كنت ترغب في الاستعلام عن المنتجات كالتالي:

- الاستعلام عن المنتج المجمع الفعلي بواسطة ابعاد *اللون* و *الحجم*.
- في بعض الحالات ، تريد فقط الاستعلام عن المنتج إجمالا.

سيكون لديك فهرسين محددين كالتالي:

- `["ColorId", "SizeId"]`
- `[]`

سيتم تجميع القوس الفارغ استنادا إلى "معرف المنتج" داخل القسم.

تحدد الفهرسة كيفيه تجميع النتائج استنادا إلى إعداد الاستعلام `groupBy`. في هذه الحالة إذا لم تقم بتحديد أي قيم `groupBy`، سيتم الحصول علي الإجماليات بواسطة `productid`. وإلا، إذا قمت بتحديد `groupBy` كـ `groupBy=ColorId&groupBy=SizeId`، ستحصل على بنود متعددة يتم إرجاعها، استنادًا إلى مجموعتي اللون والحجم المختلفتين في النظام.

يمكنك وضع معايير الاستعلام في النص الأساسي للطلب.

فيما يلي نموذج استعلام حول المنتج بمجموعه اللون والحجم.

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

فيما يتعلق بالحقل `filters`، وحده `ProductId` يدعم القيم المتعددة. إذا كان `ProductId`مصفوفة فارغة، فسيتم الاستعلام عن كافة المنتجات.

#### <a name="custom-measurement"></a>قياس مخصص

يتم ربط كميات القياس الافتراضية بـ Supply Chain Management. ومع ذلك، قد ترغب في الحصول على كمية تتكون من مجموعة من القياسات الافتراضية. وللقيام بذلك ، يمكن ان يكون لديك تكوين كميات مخصصه ، والتي ستتم اضافتها إلى إخراج الاستعلامات الفعلية.

وتتيح الوظيفة ببساطه تحديد مجموعه من القياسات التي ستتم اضافتها ، و/أو مجموعه من المقاييس التي سيتم طرحها ، من أجل القياس المخصص.

علي سبيل المثال ، باستخدام شرط الاستعلام التالي ، ستقوم بتكوين كميه القياس المخصصة باعتبارها `MyCustomAvailableforReservation` ليتم استهلاكها من قبل نظام الاستهلاك.

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



| نظام الاستهلاك | القياسات المحتسبة | مصدر البيانات | أداه التعديل | نوع حساب أداة التعديل |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | الجمع |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | الجمع |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | الطرح |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | الجمع |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | الطرح |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | الجمع |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | الجمع |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | الطرح |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | الطرح |

ومع ذلك ، سيقوم الاستعلام الموجود علي كميه القياس المخصصة بإرجاع المخرجات التالية.

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

يعتمد إخراج `MyCustomAvailableforReservation`علي إعداد الحساب في القياسات المخصصة كما يلي:  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>ترحيل التغييرات الفعلية

ويعتمد عنوان URL الذي يتم ترحيل الحدث عليه علي المنطقة الجغرافية بالبالضبط. سياخذ النموذج ما يلي:

`https://{serviceURL}/api/environment/{environmentId}/onhand`

عند المصادقة ، يمكن استخدام محدد موقع المعلومات (URL) هذا مع أسلوب `POST` HTTP لإرسال احداث التغيير الفعلي إلى الخدمة.

يتم استخدام الراس الخاص للاتصال مع خدمات Dynamics 365 من خلال طلبات HTTP ، والذي يشير إلى معرف البيئة لمثيل Supply Chain Management الذي ترتبط به البيانات. على سبيل المثال:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>ترحيل التغييرات الفعلية مثال الاستعلام 1

يوضح هذا المثال السيناريو الذي ستقوم فيه بإعداد تكوين البعد في Power Apps.

استخدم الاستعلام التالي لتكوين تعيين البعد في Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

يمكنك الآن تحديد `dimensionDataSource` واستخدام الابعاد المخصصة في الاستعلامات الخاصة بك. سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.

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

#### <a name="posting-on-hand-changes-query-example-2"></a>ترحيل التغييرات الفعلية مثال الاستعلام 2

يوضح هذا المثال السيناريو الذي لا يتم فيه إعداد تعيينات لتكوين البعد في Power Apps، التالي يجب ان تستخدم الترحيل أيضا الابعاد الاساسيه. يجب ان تكون كافة الابعاد بابعاد أساسيه عندما يكون الحقل `dimensionDataSource` خاليا أو فارغا أو مسافة بيضاء.

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

#### <a name="json-document-field-properties"></a>خصائص حقل مستند JSON

تتضمن الحقول الموجودة في أمثله استعلام JSON المتوفرة في السابق الخصائص المسرودة في الجدول التالي.

| معرف الحقل | الوصف |
|---|---|
| `id` | معرف فريد لحدث التغيير المحدد. يتم استخدام هذا المعرف للتاكد من فشل الاتصال بالخدمة اثناء الترحيل ، ولن يؤدي أعاده إرسال الحدث إلى نفس الحدث الذي يتم حسابه مرتين في النظام. |
| `organizationId` | معرف المؤسسة المرتبط بالحدث. وهذا ما يعين لمؤسسات Supply Chain Management أو معرفات مناطق البيانات. |
| `productId` | معرف أمر الإنتاج المحدد. |
| `quantity` | الكمية التي يجب تغيير الكمية الحالية وفقا لها. علي سبيل المثال ، تمت أضافه 10 قطع من خبز البيغلز جديده إلى الرف، ستكون هذه القيمة 10. إذا تمت أزاله 3 قطع من خبز البيغلز من الرف أو بيعه ، ستكون هذه القيمة -3. |
| `dimensionDataSource` | مصدر البيانات الخاص بالابعاد المستخدمة في حدث تغيير الترحيل والاستعلام. إذا قمت بتحديد مصدر البيانات ، يمكنك استخدام الابعاد المخصصة من مصدر البيانات المحدد. باستخدام تكوين البعد ، يمكن ان يقوم ظهور المخزون بتعيين الابعاد المخصصة إلى الابعاد الافتراضية العامة. في حاله عدم تحديد `dimensionDataSource`، يمكنك استخدام الابعاد الافتراضية العامة فقط في الاستعلامات الخاصة بك.   |
| `dimensions` | كيس مجموعه حيوية من أزواج مفتاح/قيمه. سيتم تعيينها لبعض الابعاد في Supply Chain Management، ولكن يمكنك أيضا أضافه ابعاد مخصصه (مثل *المصدر*) والتي قد تشير إلى ما إذا كان الحدث واردا من Supply Chain Management أو من النظام الخارجي. |

### <a name="querying-current-on-hand"></a>الاستعلام عن الكمية الحالية

سيكون للنقطة النهائية للاستعلام عن الكمية الحالية عنوان URL مشابه:

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

سيتم الاستعلام عنها باستخدام أسلوب `POST` HTTP.

#### <a name="current-on-hand-query-example-1"></a>مثال علي الاستعلام الفعلي حاليا 1

يوضح هذا المثال السيناريو الذي ستقوم فيه بإعداد تكوين البعد في Power Apps.

استخدم الاستعلام التالي لتكوين تعيين البعد في Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

يمكنك الآن تحديد `dimensionDataSource` واستخدام الابعاد المخصصة في الاستعلامات الخاصة بك. سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه. يمكنك تحديد `DimensionDataSource` في `filters` وتحديد ابعاد مخصصه في كل من `filters` و`groupByValues`. سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.

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

#### <a name="current-on-hand-query-example-2"></a>مثال علي الاستعلام الفعلي حاليا 2

يوضح هذا المثال السيناريو الذي لا يتم فيه إعداد تعيينات لتكوين البعد في Power Apps، التالي يجب ان تستخدم الترحيل أيضا الابعاد الاساسيه. يجب ان تكون كافة الابعاد بابعاد أساسيه عندما يكون الحقل `dimensionDataSource`، ضمن `filters` خاليا أو فارغا أو مسافة بيضاء.

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

#### <a name="example-return-result"></a>مثال نتيجة الإرجاع

قد تؤدي الاستعلامات المعروضة في الامثله السابقة إلى إرجاع نتيجة مثل هذه.

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

لاحظ انه يتم بناء حقول الكميات كقاموس للمقاييس والقيم المقترنة بها.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
