---
title: إرشادات النشر لآلات تسجيل المدفوعات النقدية الخاصة بالنرويج
description: يقدم هذا الموضوع دليلا حول كيفيه تمكين وظيفة تسجيل النقد لترجمة Microsoft Dynamics 365 Commerce للنرويج.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: c7e64dbfe6a300c097b5b3711ac4310f3386df11
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944730"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>إرشادات النشر لآلات تسجيل المدفوعات النقدية الخاصة بالنرويج

[!include[banner](../includes/banner.md)]

يقدم هذا الموضوع دليلا حول كيفيه تمكين وظيفة تسجيل النقد لترجمة Microsoft Dynamics 365 Commerce للنرويج. تتكون الترجمة من عده ملحقات من المكونات. تتيح لك هذه الملحقات تنفيذ إجراءات مثل طباعة الحقول المخصصة على الإيصالات، وتسجيل أحداث تدقيق إضافية، ومعاملات المبيعات، ومعاملات الدفع في نقاط البيع (POS)، وتوقيع معاملات المبيعات رقميًا، وطباعة التقارير بالتنسيقات المحلية. لمزيد من المعلومات حول الترجمة الخاصة بالنرويج، راجع [وظيفة تسجيل النقد للنرويج](./emea-nor-cash-registers.md). لمزيد من المعلومات حول كيفية تكوين Commerce للنرويج، راجع [إعداد Commerce للنرويج](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

> [!WARNING]
> وبسبب قيود [التعبئة المستقلة الجديدة ونموذج التوسيع](../dev-itpro/build-pipeline.md)، لا يمكن استخدامها حاليًا لوظيفة الترجمة هذه. يجب استخدام إصدار عينه التوقيع الرقمي للنرويج في الإصدار السابق من مجموعه تطوير برامج Retail (VM) علي الجهاز الظاهري (VM) للمطور في Microsoft Dynamics Lifecycle Services (LCS). لمزيد من المعلومات، راجع [إرشادات التوزيع للسجلات النقدية للنرويج (قديم)](./emea-nor-loc-deployment-guidelines.md).
>
> يتم تخطيط الدعم الخاص بالتعبئة المستقلة الجديدة ونموذج الملحق الخاص بنماذج التكامل المالي للإصدارات اللاحقة.

## <a name="set-up-fiscal-registration-for-norway"></a>إعداد عملية التسجيل المالي للنرويج

تعتمد عينة التسجيل المالي للنرويج على [وظيفة التكامل المالي](fiscal-integration-for-retail-channel.md) وهي جزء من Retail SDK. النموذج موجود في مجلد **src\\FiscalIntegration\\SequentialSignatureNorway** الخاص [بحلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)، المستودع (على سبيل المثال [النموذج في الإصدار/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34/src/FiscalIntegration/SequentialSignatureNorway)). يتكون [النموذج](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) من موفر المستند المالي والموصل المالي، وهما امتدادان لCommerce Runtime (CRT). لمزيد من المعلومات حول كيفيه استخدام Retail SDK، راجع [هندسة Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)و[قم بإعداد تدفق البناء لمجموعة SDK المستقلة](../dev-itpro/build-pipeline.md).

أكمل خطوات اعداد التسجيل المالي كما هو موضح في [اعداد التكامل المالي لقنوات Commerce](./setting-up-fiscal-integration-for-retail-channel.md):

1. [إعداد عملية التسجيل المالي](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). تاكد من تدوين الإعدادات الخاصة بعمليه التسجيل المالي [الخاصة بالنرويج](#configure-the-fiscal-registration-process).
1. [تعيين إعدادات معالجة الأخطاء‬](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [تمكين التنفيذ اليدوي للتسجيل المالي المؤجل](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [تكوين مكونات القناة](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>تكوين عمليه التسجيل المالي

اتبع هذه الخطوات لتمكين عملية التسجيل المالي للنرويج في مقر Commerce الرئيسي.

1. تنزيل ملفات التكوين لموفر المستند المالي والموصل المالي من Commerce SDK:

    1. افتح مستودع [حلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. يستخدم هذا الزر في فتح فرع الإصدار الذي تم توفيره مؤخرا (على سبيل المثال، **[إصدار/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34)**).
    1. افتح **src \> FiscalIntegration \> SequentialSignatureNorway \> CommerceRuntime**.
    1. قم بتنزيل ملف تكوين موفر المستند المالي في **DocumentProvider.SequentialSignNorway \> Configuration \> DocumentProviderSequentialSignatureNorwaySample.xml** (على سبيل المثال، [لملف إصدار/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/DocumentProvider.SequentialSignNorway/Configuration/DocumentProviderSequentialSignatureNorwaySample.xml)).
    1. قم بتنزيل ملف تكوين الموصل المالي في **Connector.SequentialSignNorway \> Configuration \> ConnectorSequentialSignatureNorwaySample.xml** (على سبيل المثال، [ملف الإصدار/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/Connector.SequentialSignNorway/Configuration/ConnectorSequentialSignatureNorwaySample.xml)).

1. انتقل إلى **Retail وCommerce \> إعداد Headquarters \> المعلمات \> المعلمات المشتركة**. في علامة التبويب السريعة **عام**، عيّن خيار **تمكين التكامل المالي** إلى **نعم**.
1. انتقل إلى **Retail وCommerce \> إعداد القناة \> التكامل المالي \> الموصلات المالية**، وقم بتحميل ملف تكوين موفر المستندات المالية الذي قمت بتنزيله مسبقًا.
1. انتقل إلى **Retail وCommerce \> إعداد القناة \> التكامل المالي \> موفري المستندات المالية**، وقم بتحميل ملف تكوين موفر المستندات المالية الذي قمت بتنزيله مسبقًا.
1. انتقل إلى **Retail وCommerce \> إعداد القناة \> التكامل المالي \> ملفات تعريف الموصل الوظيفية**. قم بإنشاء ملف تعريف وظيفي جديد للموصل، وحدد موفر المستندات والموصل الذي قمت بتحميله مسبقًا.
1. انتقل إلى **Retail وCommerce \> إعداد القناة \> التكامل المالي \> ملفات تعريف الموصل الفنية**. قم بإنشاء ملف تعريف فني جديد للموصل، وحدد الموصل الذي قمت بتحميله مسبقًا. قم بتعيين نوع الموصل إلى **داخلي**.
1. انتقل إلى **Retail وCommerce \> إعداد القناة \> التكامل المالي \> مجموعات الموصلات المالية**، وأنشئ مجموعة موصلات مالية جديدة لملف التعريف الوظيفي للموصل الذي قمت بإنشائه مسبقًا.
1. انتقل إلى **Retail وCommerce \> إعداد القناة \> التكامل المالي \> عمليات التسجيل المالي**. قم بإنشاء عملية تسجيل مالي جديد وخطوة عملية تسجيل مالي، وحدد مجموعة الرابط المالي الذي قمت بإنشائه مسبقًا.
1. انتقل إلى **البيع بالتجزئة والتجارة \> إعداد القناة \> إعداد قناة البيع \> ملفات تعريف نقطة البيع \> ملفات تعريف الوظائف**. حدد ملف تعريف وظائف مرتبط بالمتجر حيث يجب تنشيط عمليه التسجيل. في علامة التبويب السريعة **عملية التسجيل المالي**، حدد عملية التسجيل المالي التي قمت بإنشائها مسبقًا. في علامة التبويب السريعة **الأجهزة المالية**، حدد ملف التعريف الفني للموصل الذي قمت بإنشائه مسبقًا. 
1. انتقل إلى **البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**. افتح جدول التوزيع، وحدد وظيفتي **1070** and **1090** لنقل البيانات إلى قاعدة بيانات القناة.

### <a name="configure-the-digital-signature-parameters"></a>تكوين معلمات التوقيع الرقمي

يجب تكوين الشهادات التي سيتم استخدامها للتوقيع الرقمي لحركات المبيعات في أحد المتاجر. تستخدم الشهادة الرقمية التي يتم تخزينها في مخزن مفتاح Azure لاجراء التوقيع. بالنسبة لوضع العمل دون اتصال بالوسائط الحديثة، يمكن أيضا اجراء التوقيع باستخدام شهادة رقميه يتم تخزينها في التخزين المحلي للجهاز الذي تم تثبيت نقطه البيع الحديثة عليه.

قبل ان تتمكن من استخدام شهادة رقميه مخزنه في مخزن المخزن الأساسي، يجب إكمال الخطوات التالية.

1. يجب إنشاء مخزن المخزن الأساسي. نوصي بنشر التخزين في نفس المنطقة الجغرافية بمثابة Commerce Scale Unit.
1. يجب تحميل الشهادة إلى تخزين المفتاح المخزن ككلمه سر لسلسله base64.
1. يجب أن يكون تطبيق Application Object Server (AOS) مفوضًا لقراءة الأسرار من مخزن Key Vault.

لمزيد من المعلومات حول كيفيه العمل مع المخزن الرئيسي، راجع [الشروع في العمل مع المخزن الرئيسي لـ Azure](/azure/key-vault/key-vault-get-started).

وبعد ذلك، في صفحة **معلمات المخزن الرئيسي**، يجب تحديد المعلمات للوصول إلى المخزن الرئيسي:

- **الاسم** و **الوصف** – اسم ووصف المخزن الرئيسي.
- **عنوان URL للمخزن الرئيسي** – عنوان URL الخاص بالمخزن الرئيسي.
- **عميل المخزن الرئيسي** – معرف العميل التفاعلي لتطبيق Azure Active Directory (Azure AD) المرتبط بتخزين Key Vault لأغراض المصادقة. يجب أن يكون لهذا العميل حق الوصول لقراءة الأسرار من التخزين.
- **مفتاح سر Key Vault** – مفتاح السر مرتبط بتطبيق Azure AD المستخدم للمصادقة في تخزين Key Vault.
- **الاسم**، و **الوصف**، و **المرجع السري** – الاسم والوصف والمرجع السري للشهادة.

بعد ذلك، يجب عليك تكوين موصل لشهاداتك المخزنة في Key Vault أو تخزين الشهادة المحلي. يتم استخدام هذا الموصل للتوقيع علي جانب القناة.

1. انتقل إلى **Retail وCommerce \> إعداد القناة \> التكامل المالي \> ملفات تعريف الموصل الفنية**.
1. في علامة التبويب السريعة **الإعدادات**، حدد المعلمات التالية للتوقيعات الرقمية:

    - **الاسم السري** – حدد الاسم السري الذي قمت بتكوينه مسبقا في صفحة **معلمات Key Vault**.
    - **بصمه إبهام الشهادة المحلية** – توفر بصمه الإبهام لشهادة مخزنه محليا.
    - **خوارزميه التجزئة** – تحديد واحده من خوارزميات تجزئه التشفير التي يتم دعمها من قبل Microsoft .NET، مثل **SHA1**.
    - **اسم مخزن الشهادات** – هذا الحقل اختياري. يتم استخدام ذلك لتحديد اسم المتجر الافتراضي الذي يجب استخدامه للبحث في الشهادات المحلية.
    - **موقع مخزن الشهادات** – هذا الحقل اختياري. يتم استخدام ذلك لتحديد موقع المتجر الافتراضي الذي يجب استخدامه للبحث في الشهادات المحلية.
    - **جرب الشهادة المحلية أولاً** – حدد هذا الخيار لاستخدام الشهادة من المتجر المحلي افتراضيًا لتوقيع البيانات، بدلاً من الشهادة من Key Vault.
    - **تنشيط فحص السلامة** – لمزيد من المعلومات حول ميزة فحص السلامة، راجع [فحص سلامة التسجيل المالي](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

> [!NOTE]
> - فقط خوارزميه تجزئه التشفير **SHA1** مقبوله حاليا للنرويج.
> - تتم أضافه اسم المتجر وموقع التخزين الافتراضيين لتبسيط عمليه البحث عن الشهادات المحلية في CRT. يتضمن X509StoreProvider قائمه بالمجلدات التي يتم تخزين الشهادات بها. إذا لم يتم تحديد اسم المتجر الافتراضي وموقع المتجر الافتراضي، X509StoreProvider يحاول العثور علي شهادة في جميع المجلدات الموجودة على القائمة الخاصة بها.

### <a name="configure-channel-components"></a>تكوين مكونات القناة

### <a name="development-environment"></a>بيئة التطوير

اتبع هذه الخطوات لإعداد بيئة تطوير بحيث يمكنك اختبار العينة وتوسيعها.

1. قم بنسخ مستودع [حلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) أو تنزيله. حدد إصدار فرع إصدار صحيح وفقا لإصدار التطبيق أو SDK الخاص بك. لمزيد من المعلومات، راجع [تنزيل نماذج Retail SDK والحزم المرجعية من GitHub وNuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. افتح حل **SequentialSignatureNorway.sln** ضمن **Dynamics365Commerce.Solutions\\FiscalIntegration\\SequentialSignatureNorway**، وقم بإنشائه.
1. تثبيت ملحقات CRT:

    1. ابحث عن مثبت ملحق CRT:

        - **Commerce Scale Unit:** في مجلد **SequentialSignatureNorway\\ScaleUnit\\ScaleUnit.SequentialSignNorway.Installer\\bin\\Debug\\net461**، ابحث عن مثبت **ScaleUnit.SequentialSignNorway.Installer**.
        - **CRT المحلي في نقطة البيع الحديثة:** في مجلد **SequentialSignatureNorway\\ModernPOS\\ModernPos.SequentialSignNorway.Installer\\bin\\Debug\\net461**، ابحث عن مثبت **ModernPos.SequentialSignNorway.Installer**.

    1. ابدأ مثبت ملحق CRT من سطر الأوامر:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **CRT المحلي في نقطة البيع الحديثة:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

### <a name="production-environment"></a>بيئة الإنتاج

اتبع الخطوات الواردة في [إعداد تدفق البناء لنموذج تكامل مالي](fiscal-integration-sample-build-pipeline.md) لإنشاء وإصدار وحده مقياس السحابة وحزم الخدمة الذاتية القابلة للنشر لنموذج التكامل المالي. يمكن العثور على ملف YAML لقالب **SequentialSignatureNorway build-pipeline.yaml** في مجلد **Pipeline\\YAML_Files** الخاص بمستودع [حلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>تمكين التوقيع الرقمي في وضع عدم الاتصال لنقاط البيع الحديثة

لتمكين التوقيع الرقمي في وضع عدم الاتصال لـ Modern POS، يجب اتباع هذه الخطوات بعد تنشيط Modern POS على جهاز جديد.

1. سجل الدخول إلى POS.
1. في صفحة **حالة اتصال قاعدة البيانات**، تاكد من مزامنة قاعده البيانات غير المتصلة بشكل كامل. عندما تكون قيمه حقل **التنزيلات المعلقة** هي **0** (صفر)، تتم مزامنة قاعده البيانات بالكامل.
1. قم بتسجيل الخروج من نقطة البيع.
1. انتظر حتى تتم مزامنة قاعدة البيانات دون اتصال بشكل كامل.
1. سجل الدخول إلى POS.
1. في صفحة **حالة اتصال قاعدة البيانات**، تاكد من مزامنة قاعده البيانات غير المتصلة بشكل كامل. عندما تكون قيمه حقل **الحركات المعلقة في قاعدة البيانات غير المتصلة** هي **0** (صفر)، تتم مزامنة قاعده البيانات بالكامل.
1. أعد فتح Modern POS.
