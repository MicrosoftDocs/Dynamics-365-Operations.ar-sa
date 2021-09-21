---
title: تثبيت الوظيفة الإضافية لرؤية المخزون
description: يوضح هذا الموضوع كيفيه تثبيت الوظيفة الإضافية لرؤية المخزون لـ Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b2b85f533a3318701ed08857b899cf9bdd103863
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474810"
---
# <a name="install-and-set-up-inventory-visibility"></a>تثبيت إعداد رؤية المخزون

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

يوضح هذا الموضوع كيفيه تثبيت الوظيفة الإضافية لرؤية المخزون لـ Microsoft Dynamics 365 Supply Chain Management.

يجب عليك استخدام Microsoft Dynamics Lifecycle Services (LCS) لتثبيت الوظيفة الإضافية لرؤية المخزون. LCS عبارة عن مدخل تعاون يوفر بيئة ومجموعه من الخدمات المحدثة بشكل منتظم والتي تساعدك علي أداره دوره حياه التطبيقات الخاصة بتطبيقات finance and operations الخاصة بك.

للحصول على مزيد من المعلومات، راجع [موارد Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>المتطلبات الأساسية لرؤية المخزون

قبل تثبيت رؤية المخزون، يجب عليك إكمال المهام التالية:

- احصل على مشروع تنفيذ LCS حيث يتم نشر بيئة واحدة على الأقل.
- تأكد من أن المتطلبات الأساسية لإعداد الوظائف الإضافية قد اكتملت. للحصول على معلومات حول هذه المتطلبات الأساسية، راجع [نظرة عامة على الوظائف الإضافية](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). لا تتطلب رؤية المخزون ارتباطًا ثنائي الكتابة.
- تواصل مع فريق منتج رؤية المخزون على [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) للحصول على الملفات المطلوبة التالية:

    - `InventoryServiceApplication.PackageDeployer.zip`
    - `Inventory Visibility Integration.zip` (إذا كان إصدار Supply Chain Management الذي تقوم بتشغيله أقدم من الإصدار 10.0.18)

> [!NOTE]
> تشمل البلدان والمناطق المدعومة حاليًا كندا (CCA، ECA)، والولايات المتحدة (WUS، EUS)، والاتحاد الأوروبي (NEU، WEU)، والمملكة المتحدة (SUK، WUK)، وأستراليا (EAU، SEAU) واليابان (EJP, WJP)، والبرازيل (SBR, SCUS).

إذا كانت لديك إيه اسئله حول هذه المتطلبات الاساسيه، الرجاء الاتصال بفريق رؤية المخزون.

## <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>إعداد Dataverse

لإعداد Dataverse بحيث يمكن استخدامها مع "رؤية المخزون"، استخدم أداة نشر الحزمة لنشر حزمة "رؤية المخزون". تصف الأقسام الفرعية التالية كيفية إكمال كل مهمة.

> [!NOTE]
> حاليا، يتم اعتماد بيئات Dataverse التي تم إنشاؤها باستخدام LCS فقط. إذا تم إنشاء بيئة Dataverse الخاصة بك بطريقة أخرى (على سبيل المثال، باستخدام مركز إدارة Power Apps)، وإذا كانت مرتبطة ببيئة Supply Chain Management الخاصة بك، فيجب عليك أولاً الاتصال بالمخزون رؤية فريق المنتج لإصلاح مشكلة التعيين. يمكنك بعد ذلك تثبيت رؤية المخزون.

### <a name="migrate-from-an-old-version-of-the-dataverse-solution"></a>ترحيل من إصدار قديم لحل Dataverse

إذا قمت بتثبيت إصدار قديم من حل Dataverse لرؤية المخزون، فاستخدم هذه الإرشادات لتحديث الإصدار. هناك حالتان:

- **الحالة 1:** إذا قمت بإعداد Dataverse يدويًا عن طريق استيراد حل `Inventory Visibility Dataverse Solution_1_0_0_2_managed.zip`، اتبع الخطوات التالية:

    1. قم بتنزيل الملفات الثلاثة التالية:

        - `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip`
        - `InventoryServiceBase_managed.cab`
        - `InventoryServiceApplication.PackageDeployer.zip`

    1. قم باستيراد `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip` و`InventoryServiceBase_managed.cab` إلى Dataverse يدويًا باتباع الخطوات التالية:

        1. افتح عنوان URL الخاص ببيئة Dataverse الخاصة بك.
        1. افتح صفحة **الحلول**.
        1. حدد **استيراد**.

    1. استخدم أداة نشر الحزمة لنشر حزمة `InventoryServiceApplication.PackageDeployer.zip`. للحصول على إرشادات، راجع قسم [استخدام أداة نشر الحزمة لنشر الحزمة](#deploy-package) لاحقًا في هذا الموضوع.

- **الحالة 2:** إذا قمت بإعداد Dataverse باستخدام أداة نشر الحزمة قبل تثبيت حزمة `.*PackageDeployer.zip` الأقدم، قم بتنزيل `InventoryServiceApplication.PackageDeployer.zip`، وقم بتحديث. للحصول على إرشادات، راجع قسم [استخدام أداة نشر الحزمة لنشر الحزمة](#deploy-package).

### <a name="use-the-package-deployer-tool-to-deploy-the-package"></a><a name="deploy-package"></a>استخدام أداة نشر الحزمة لنشر الحزمة

1. قم بتثبيت أدوات المطور كما هو موضح في [أدوات التنزيل من NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).
1. قم بإلغاء حظر ملف `InventoryServiceApplication.PackageDeployer.zip` الذي قمت بتنزيله من مجموعة Teams باتباع الخطوات التالية:

    1. حدد ثم اضغط (أو انقر بزر الماوس الأيمن) فوق الملف، ثم حدد **خصائص**.
    1. في مربع الحوار **خصائص**، في علامة التبويب **عام**، ابحث عن قسم **الأمان**، وحدد **إلغاء الحظر**، وطبق التغيير. إذا لم يكن هناك قسم **أمان**  في علامة التبويب **عام**، فلن يتم حظر الملف. في هذه الحالة، انتقل إلى الخطوة التالية.

    ![إلغاء حظر الملف الذي تم تنزيله](media/unblock-file.png "إلغاء حظر الملف الذي تم تنزيله")

1. فك ضغط `InventoryServiceApplication.PackageDeployer.zip` للعثور على العناصر التالية:

    - مجلد `InventoryServiceApplication`
    - ملف `[Content_Types].xml`
    - ملف `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`

1. انسخ كل عنصر من هذه العناصر إلى دليل `.\Tools\PackageDeployment`. (تم إنشاء هذا الدليل عند تثبيت أدوات المطور.)
1. قم بتشغيل `.\Tools\PackageDeployment\PackageDeployer.exe`، واتبع الإرشادات التي تظهر على الشاشة لاستيراد الحلول.

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>تثبيت الوظيفة الإضافية لرؤية المخزون

قبل تثبيت الوظيفة الإضافية، قم بتسجيل تطبيق وإضافة سر عميل إلى Azure Active Directory (Azure AD) ضمن اشتراك Azure. للحصول على إرشادات، راجع [تسجيل تطبيق](/azure/active-directory/develop/quickstart-register-app) و[إضافة سر عميل](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). تأكد من تدوين ملاحظة بشأن قيم **معرف التطبيق (العميل)**، و **سر العميل**، و **معرف المستأجر**، لأنك ستحتاج إليها لاحقًا.

بعد تسجيل تطبيق وإضافة سر عميل إلى Azure AD، اتبع الخطوات التالية لتثبيت الوظيفة الإضافية "رؤية المخزون".

1. سجل الدخول إلى [LCS](https://lcs.dynamics.com/Logon/Index).
1. في الصفحة الرئيسية ، حدد المشروع حيث يتم نشر البيئة الخاصة بك.
1. في الصفحة المشروع ، حدد البيئة التي ترغب في تثبيت الوظيفة الإضافية بها.
1. في الصفحة البيئة، قم بالتمرير لأسفل حتى تعثر على قسم **الوظائف الإضافية الخاصة بالبيئة** في قسم **تكامل Power Platform**. هناك، يمكنك العثور على اسم بيئة Dataverse.
1. في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.

    ![صفحة البيئة في LCS](media/inventory-visibility-environment.png "صفحة البيئة في LCS")

1. حدد الرابط **تثبيت وظيفة إضافية جديدة**. تظهر قائمة بالوظائف الإضافية المتاحة.
1. في القائمة، حدد **رؤية المخزون**.
1. قم بتعيين الحقول التالية لبيئتك:

    - **معرف تطبيق AAD (العميل)** – أدخل معرف تطبيق Azure AD الذي أنشأته ودونت ملاحظة عنه سابقًا.
    - **معرف مستأجر AAD** – أدخل معرف المستأجر الذي دونت ملاحظة عنه في وقت سابق.

    ![صفحة إعداد الوظيفة الإضافية](media/inventory-visibility-setup.png "صفحة إعداد الوظيفة الإضافية")

1. الموافقة علي البنود والشروط عن طريق تحديد خانه الاختيار **البنود والشروط**.
1. حدد **تثبيت**. تظهر حاله الوظيفة الإضافية باعتبارها **قيد التثبيت**. عند اكتمال التثبيت، قم بتحديث الصفحة. يجب تغيير الحالة إلى **تم التثبيت**.

> [!IMPORTANT]
> إذا كان لديك أكثر من بيئة LCS، فقم بإنشاء تطبيق Azure AD مختلف لكل بيئة. في حالة استخدام نفس معرف التطبيق ومعرف المستاجر لتثبيت الوظيفة الإضافية لرؤية المخزون لبيئات مختلفة، ستحدث مشكلة في الرمز المميز للبيئات الأقدم. سيكون آخر رمز تم تثبيته صالحاً فقط.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>إزالة تثبيت الوظيفة الإضافية لرؤية المخزون

لإلغاء تثبيت الوظيفة الإضافية "رؤية المخزون"، حدد **إزالة تثبيت** في صفحة LCS. تقوم عملية إلغاء التثبيت بإنهاء الوظيفة الإضافية رؤية المخزون، وإلغاء تسجيل الوظيفة الإضافية من LCS، وحذف أي بيانات مؤقتة مخزنة في ذاكرة التخزين المؤقت لبيانات الجرد الإضافية. ومع ذلك، لا يتم حذف بيانات المخزون الأساسية المخزنة في اشتراك Dataverse.

لإزالة تثبيت بيانات المخزون المخزنة في اشتراك Dataverse، افتح [Power Apps](https://make.powerapps.com)، وحدد **بيئة**  على شريط التنقل، وحدد بيئة Dataverse المرتبطة ببيئة LCS. ثم انتقل إلى **الحلول**، ثم احذف الحلول الخمسة التالية:

- حل تثبيت لتطبيق رؤية المخزون في حلول Dynamics 365
- حل لتطبيقات Dynamics 365 FNO SCM Inventory Visibility
- تكوين خدمة الجرد
- خدمة رؤية المخزون المستقلة
- الحل الأساسي لـ Dynamics 365 FNO SCM Inventory Visibility

بعد حذف هذه الحلول، سيتم حذف البيانات المخزنة في الجداول أيضا.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>إعداد رؤية المخزون في Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>توزيع حزمة تكامل رؤية المخزون

إذا كنت تقوم بتشغيل Supply Chain Management الإصدار 10.0.17 أو إصدار سابق عنه، فتواصل بفريق دعم رؤية المخزون على [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) للحصول علي ملف الحزمة. ثم قم بنشر الحزمة في LCS.

> [!NOTE]
> إذا حدث خطأ عدم تطابق في الإصدار أثناء التوزيع، يجب عليك استيراد مشروع X++ يدويًا إلى بيئة التطوير الخاصة بك. ثم قم بإنشاء الحزمة القابلة للنشر في بيئة التطوير الخاصة بك، ثم قم بنشرها في بيئة الإنتاج الخاصة بك.
>
> يتم تضمين الكود Supply Chain Management في الإصدار 10.0.18. إذا كنت تقوم بتشغيل هذا الإصدار أو الأحدث، فإن عملية النشر تكون غير ضرورية.

تأكد من أنه يتم تشغيل الميزات التالية في بيئة Supply Chain Management. (افتراضيًا، فإنه يتم تشغيلها.)

| وصف الميزة | إصدار الكود | تبديل الفئة |
|---|---|---|
| تمكين أو تعطيل استخدام أبعاد المخزون في جدول InventSum      | 10.0.11 | InventUseDimOfInventSumToggle      |
| تمكين أو تعطيل استخدام أبعاد المخزون في جدول InventSumDelta | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>إعداد تكامل رؤية المخزون

بمجرد تثبيت الوظيفة الإضافية، قم بتحضير نظام Supply Chain Management الخاص بك للعمل معها عن طريق إجراء الخطوات التالية.

1. في Supply Chain Management، افتح مساحة عمل **[إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**، وقم بتشغيل الميزات التالية:
    - *تكامل رؤية المخزون* - مطلوب.
    - *تكامل رؤية المخزون مع إزاحة الحجز* - موصي به لكنه اختياري. يتطلب الإصدار 10.0.22 أو إصدار لاحق. لمزيد من المعلومات، راجع [حجوزات رؤية المخزون](inventory-visibility-reservations.md).

1. انتقل إلى **إدارة المخزون \> الإعداد \> معلمات تكامل رؤية المخزون**.
1. افتح علامة التبويب **عام** وقم بإجراء الإعدادات التالية:
    - **نقطه نهاية رؤية المخزون** – أدخل عنوان URL الخاص بالبيئة التي تقوم فيها بتشغيل رؤية المخزون. للحصول على مزيد من المعلومات، راجع [البحث عن نقطة نهاية الخدمة](inventory-visibility-configuration.md#get-service-endpoint).
    - **الحد الأقصى لعدد السجلات في طلب مفرد** - يتم تعيينه إلى الحد الأقصى لعدد السجلات المطلوب تضمينها في طلب واحد. يجب إدخال عدد صحيح موجب أقل من أو يساوي 1000. القيمة الافتراضية هي 512. نوصي بشدة بالاحتفاظ بالقيمة الافتراضية إلا إذا كنت قد تلقيت نصيحة من دعم Microsoft أو أنك متأكد من أنك تحتاج إلى تغييرها.

1. إذا قمت بتمكين ميزة *تكامل رؤية المخزون مع إزاحة الحجز*، افتح علامة التبويب **إزاحة الحجز** ثم قم بإجراء الإعدادات التالية:
    - **تمكين إزاحة الحجز** - قم بتعيينها إلى *نعم* لتمكين هذه الوظيفة.
    - **معدل إزاحة الحجز** – حدد حالة حركة المخزون التي ستقوم بازاحة عمليات الحجز التي تم إجراؤها في رؤية المخزون. يحدد هذا الإعداد مرحلة معالجة الأمر التي تشغل الإزاحات. يتم تتبع المرحلة حسب حالة حركة المخزون الخاصة بالأمر. اختر واحدًا مما يلي:
        - *في أمر* – بالنسبة لحالة *في الحركة*، سيقوم أمر بإرسال طلب إزاحة عند إنشائه. ستكون كمية الإزاحة هي الكمية الخاصة بالأمر الذي تم إنشاؤه.
        - *الحجز* – بالنسبة لحالة *الحركة المطلوبة للحجز*، سيقوم أمر بإرسال طلب تعويض عند حجزه أو انتقاؤها أو ترحيل كشف التعبئة أو فوترتها. سيتم تشغيل الطلب مرة واحدة فقط، للخطوة الأولى عند حدوث العملية المذكورة. ستكون كمية الإزاحة هي الكمية التي تغيرت فيها حالة حركة المخزون من *تحت الطلب* إلى *مطلوب محجوز* (أو لاحقًا الحالة) في بند الأمر المقابل.

1. انتقل إلى **إدارة المخزون \> دوري \> تكامل رؤية المخزون**، وقم بتمكين الوظيفة. سيتم الآن ترحيل كافة أحداث تغيير المخزون من Supply Chain Management إلى رؤية المخزون.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
