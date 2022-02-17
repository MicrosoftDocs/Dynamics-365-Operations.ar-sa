---
title: عينة تكامل وحدة التحكم للسويد
description: يقدم هذا الموضوع نظرة عامة على عينة التكامل المالي للسويد في Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: ace1bd5b1a06317b6753a34779ecfa96e519a63e
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077003"
---
# <a name="control-unit-integration-sample-for-sweden"></a>عينة تكامل وحدة التحكم للسويد

[!include [banner](../includes/banner.md)]

يقدم هذا الموضوع نظرة عامة على عينة التكامل المالي للسويد في Microsoft Dynamics 365 Commerce.

> [!NOTE]
> يؤدي هذا النموذج في وظيفة التكامل المالي إلى استبدال [النموذج السابق لتكامل نقطه البيع بوحدات التحكم الخاصة بالسويد](retail-sdk-control-unit-sample.md). لا يستفيد النموذج السابق من [إطار عمل التكامل المالي](./fiscal-integration-for-retail-channel.md) وسيصبح قديمًا في التحديثات اللاحقة. للحصول علي معلومات حول كيفيه الترحيل من النموذج السابق إلى النموذج الذي يتوافق مع Dynamics 365 Commerce، الإصدار **10.0.22 وما قبله**، راجع [الترحيل من نموذج التكامل السابق](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample).

تشتمل وظيفة Commerce للسويد علي عينه من التكامل الخاص بنقطه البيع (POS) مع الاجهزه المالية الخاصة بالسويد والتي تعرف باسم *وحدات التحكم*. ويقوم هذا النموذج بتوسيع [وظيفة التكامل المالي](fiscal-integration-for-retail-channel.md). ومن المفترض ان تكون وحده التحكم متصلة فعليا بمحطه أجهزه يتم اقران نقطه البيع بها. كمثال، يستخدم هذا النموذج واجهة برمجة التطبيقات (API) لوحدة تحكم [نوع CleanCash أ](https://www.retailinnovation.se/produkter) بواسطة Retail Innovation HTT AB. يتم استخدام الإصدار 1.1.4 من CleanCash API.

يتم توفير العينة في شكل كود المصدر وهي جزء من مجموعة تطوير برامج البيع بالتجزئة (SDK).

لا تصدر Microsoft أي أجهزة أو برامج أو وثائق من Retail Innovation HTT AB. للحصول على معلومات حول كيفية الحصول على وحدة التحكم وتشغيلها، اتصل بـ [Retail Innovation HTT AB](https://www.retailinnovation.se/).

## <a name="scenarios"></a>السيناريوهات

يتضمن نموذج تكامل وحده التحكم الخاص بالسويد القدرات التالية:

- يتم تسجيل نسخ المبيعات والمرتجعات والإيصالات تلقائيا في وحده التحكم المرتبطة بمحطه الاجهزه المقترنة بنقطه البيع.
- يتم تسجيل رمز التحكم ورقم المصنع الخاص بوحدة التحكم الخاصة بالحركة المسجلة من وحده التحكم ويتم حفظها في الحركة. ويشار إلى هذه البيانات أيضًاباسم  *الاستجابة المالية*. يمكن عرض الاستجابة المالية في صفحة **حركات المتجر**.
- يمكن إضافة الحقول المخصصة لرمز التحكم ورقم التصنيع لوحده التحكم إلى تخطيط إيصال. بهذه الطريقة، يمكنك طباعة الاستجابة المالية لمعاملة ما على إيصال.
- يتم عرض الاستجابة المالية لمعاملة ما في تقرير قناة **دفتر اليومية الإلكتروني (السويد)**.
- تتوفر العديد من خيارات معالجه الخطا. فيما يلي بعض الأمثلة:

    - قم باعاده محاولة التسجيل المالي، إذا كانت أعاده المحاولة ممكنة. يمكنك أعاده محاولة التسجيل المالي في حاله ما إذا كانت وحده التحكم غير متصلة أو غير جاهزه أو لا تستجيب.
    - تأجيل عملية التسجيل المالي.
    - يستخدم لتخطي التسجيل المالي أو وضع علامة علي الحركة كمسجله، وتضمين رموز المعلومات للتقاط سبب الفشل والمعلومات الاضافيه.
    - تحقق من توفر وحدة التحكم قبل فتح حركة مبيعات جديدة أو إنهاء معاملة المبيعات.

### <a name="limitations-of-the-sample"></a>قيود العينة

لا يعتمد نموذج تكامل وحده التحكم في السويد حاليا سيناريوهات أوامر العميل.

## <a name="setting-up-the-integration-with-control-units"></a>إعداد التكامل باستخدام وحدات التحكم

لمزيد من المعلومات حول الاعداد المطلوب للسويد، راجع [اعداد Commerce للسويد](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden).

### <a name="configuring-swedenspecific-receipts"></a>تكوين الإيصالات الخاصة بالسويد

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>تكوين الحقول المخصصة بحيث يمكن استخدامها في تنسيقات الاستلام لإيصالات المبيعات

يمكنك تكوين نص اللغة والحقول المخصصة المستخدمة في تنسيقات إيصالات نقطه البيع. يجب ان تكون الشركة الافتراضية للمستخدم الذي يقوم بإنشاء اعداد الإيصال هي نفس الكيان القانوني الذي يتم إنشاء اعداد نص اللغة فيه. وبدلا من ذلك، يجب إنشاء نفس نصوص اللغة في الشركة الافتراضية لكل من المستخدم والكيان القانوني للمتجر الذي تم إنشاء الاعداد له.

في صفحة **نص اللغة**، قم باضافه السجلات التالية لتسميات الحقول المخصصة لتخطيطات الإيصال. لاحظ أن قيم **معرف اللغة** و **معرف النص** و **النص** التي تظهر في الجدول هي أمثله فقط. يمكنك تغييرها لتلبي متطلباتك. ومع ذلك، يجب أن تكون قيم **معرف النص** التي تستخدمها فريدة، ويجب أن تكون مساوية لـ 900001 أو أكبر.

أضف تسميات نقطه البيع التالية إلى قسم **نقطة البيع** لصفحة **نص اللغة**.

| معرف اللغة | معرف النص | النص                  |
|-------------|---------|-----------------------|
| ar‬       | 900001  | كود التحكم في التسجيل |
| ar‬       | 900002  | جهاز التسجيل       |

في صفحة **الحقول المخصصة**، قم باضافه السجلات التالية للحقول المخصصة لتخطيطات الإيصالات. لاحظ أن قيم **معرف نص التسمية التوضيحية** يجب أن تكون متوافقة مع قيم **معرف النص** التي حددتها في صفحة **نص اللغة**.

| Name                         | النوع    | معرف نص التسمية التوضيحية |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | استلام | 900001          |
| SE_FISCALREGISTERID          | استلام | 900002          |

> [!NOTE]
> من المهم تحديد أسماء الحقول المخصصة الصحيحة، كما هو موضح في الجدول السابق. سيتسبب اسم الحقل المخصص غير صحيح في فقدان البيانات في عمليات الاستلام.

#### <a name="configure-receipt-formats"></a>تكوين تنسيقات الإيصالات

بالنسبة لكل تنسيق إيصال مطلوب، قم بتغيير قيمة حقل **سلوك الطباعة** إلى **الطباعة دائمًا**.

في مصمم تنسيق الإيصال، أضف الحقول المخصصة التالية إلى قسم **التذييل**. لاحظ ان أسماء الحقول تتوافق مع نصوص اللغة التي قمت بتحديدها في المقطع السابق بهذا الموضوع.

- **رمز التحكم في التسجيل** – يقوم هذا الحقل بطباعه التعليمات البرمجية للتحكم.
- **جهاز التسجيل** – يقوم هذا الحقل بطباعه رقم التصنيع الخاص بوحدة التحكم.

للحصول على مزيد من المعلومات حول كيفية العمل بتنسيقات الايصالات، راجع [قوالب الايصالات والطباعة](../receipt-templates-printing.md).

### <a name="set-up-fiscal-integration-for-sweden"></a>إعداد التكامل المالي للسويد

تعتمد عينة تكامل وحدة التحكم في السويد على [وظيفة التكامل المالي](fiscal-integration-for-retail-channel.md) وهي جزء من Retail SDK. النموذج موجود في مجلد **src\\FiscalIntegration\\CleanCash** الخاص [بحلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)، المستودع (على سبيل المثال [النموذج في الإصدار/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). يتكون [النموذج](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) من موفر المستند المالي، وهو امتداد لCommerce Runtime (CRT)، والموصل المالي، وهو امتداد لمحطة أجهزة Commerce. لمزيد من المعلومات حول كيفيه استخدام Retail SDK، راجع [هندسة Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)و[قم بإعداد تدفق البناء لمجموعة SDK المستقلة](../dev-itpro/build-pipeline.md).

> [!WARNING]
> وبسبب قيود [التعبئة المستقلة الجديدة ونموذج التوسيع](../dev-itpro/build-pipeline.md)، لا يمكن استخدامها حاليًا لنموذج التكامل المالي هذا. يجب استخدام الإصدار السابق من Retail SDK على الجهاز الظاهري (VM) للمطور في Microsoft Dynamics Lifecycle Services (LCS). لمزيد من المعلومات، راجع [إرشادات التوزيع الخاصة بنموذج تكامل وحدة التحكم للسويد (قديم)](emea-swe-fi-sample-sdk.md).
>
> يتم تخطيط الدعم الخاص بالتعبئة المستقلة الجديدة ونموذج الملحق الخاص بنماذج التكامل المالي للإصدارات اللاحقة.

قم بإكمال خطوات اعداد التكامل المالي كما هو موضح في [اعداد التكامل المالي لقنوات Commerce](setting-up-fiscal-integration-for-retail-channel.md).

1. [إعداد عملية التسجيل المالي](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). وكذلك قم بتسجيل الإعدادات الخاصة بعمليه التسجيل المالي [الخاصة بنموذج تكامل وحدة التحكم هذه](#set-up-the-registration-process).
1. [تعيين إعدادات معالجة الأخطاء‬](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [تمكين التنفيذ اليدوي للتسجيل المالي المؤجل](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [تكوين مكونات القناة](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>إعداد عملية التسجيل

لتمكين عملية التسجيل، اتبع هذه الخطوات لإعداد مقر Commerce الرئيسي. لمزيد من المعلومات، راجع [إعداد التكامل المالي لقنوات Commerce](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. تنزيل ملفات التكوين لموفر المستند المالي والموصل المالي:

    1. افتح مستودع [حلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. حدد إصدار فرع إصدار صحيح وفقا لإصدار التطبيق أو SDK الخاص بك (علي سبيل المثال، **[إصدار/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. افتح **src \> FiscalIntegration \> CleanCash**.
    1. قم بتنزيل ملف تكوين موفر المستند المالي في **CommerceRuntime \> DocumentProvider.CleanCashSample \> Configuration \> DocumentProviderFiscalCleanCashSample.xml** (على سبيل المثال، [ملف الإصدار/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)).
    1. قم بتنزيل ملف تكوين الموصل المالي في **HardwareStation \> Connector.CleanCashSample \> Configuration \> ConnectorCleanCashSample.xml** (على سبيل المثال، [ملف الإصدار/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)).

    > [!WARNING]
    > وبسبب قيود [التعبئة المستقلة الجديدة ونموذج التوسيع](../dev-itpro/build-pipeline.md)، لا يمكن استخدامها حاليًا لنموذج التكامل المالي هذا. يجب استخدام الإصدار السابق من Retail SDK على الجهاز الظاهري (VM) للمطور في LCS. توجد ملفات التكوين لعينة التكامل المالي هذه في المجلدات التالية من Retail SDK على الجهاز الظاهري VM للمطور في LCS:
    >
    > - **ملف تكوين موفري المستندات المالية:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml
    > - **ملف تكوين الموصل المالي:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml
    > 
    > يتم تخطيط الدعم الخاص بالتعبئة المستقلة الجديدة ونموذج الملحق الخاص بنماذج التكامل المالي للإصدارات اللاحقة.

1. انتقل إلى **Retail and Commerce \> إعداد Headquarters \> المعلمات \> معلمات Commerce المشتركة**. في علامة التبويب السريعة **عام**، عيّن خيار **تمكين التكامل المالي** إلى **نعم**.
1. انتقل إلى **Retail وCommerce \> إعداد القناة \> التكامل المالي \> موفري المستندات المالية**، وقم بتحميل ملف تكوين موفر المستندات المالية الذي قمت بتنزيله مسبقًا.
1. انتقل إلى **Retail وCommerce \> إعداد القناة \> التكامل المالي \> الموصلات المالية**، وقم بتحميل ملف تكوين موفر المستندات المالية الذي قمت بتنزيله مسبقًا.
1. انتقل إلى **Retail وCommerce \> إعداد القناة \> التكامل المالي \> ملفات تعريف الموصل الوظيفية**. أنشئ ملف تعريف الموصل الوظيفي الجديد. حدد موفر المستند والموصل الذي قمت بتحميله سابقًا. قم بتحديث [إعدادات تعيين البيانات](#default-data-mapping) كما هو مطلوب.
1. انتقل إلى **Retail وCommerce \> إعداد القناة \> التكامل المالي \> ملفات تعريف الموصل الفنية**. قم بإنشاء ملف تعريف فني جديد للموصل، وحدد الرابط المالي الذي قمت بتحميله مسبقًا. قم بتحديث [إعدادات الموصل](#fiscal-connector-settings) كما هو مطلوب.
6. انتقل إلى **Retail وCommerce \> إعداد القناة \> التكامل المالي \> مجموعات الموصلات المالية**. قم بإنشاء مجموعة رابط مالي جديدة لملف التعريف الوظيفي للموصل الذي قمت بإنشائه مسبقًا.
7. انتقل إلى **Retail وCommerce \> إعداد القناة \> التكامل المالي \> عمليات التسجيل المالي**. قم بإنشاء عملية تسجيل مالي جديد وخطوة عملية تسجيل مالي، وحدد مجموعة الرابط المالي الذي قمت بإنشائه مسبقًا.
8. انتقل إلى **البيع بالتجزئة والتجارة \> إعداد القناة \> إعداد قناة البيع \> ملفات تعريف نقطة البيع \> ملفات تعريف الوظائف**. حدد ملف تعريف وظائف مرتبط بالمتجر حيث يجب تنشيط عمليه التسجيل. في علامة التبويب السريعة **عملية التسجيل المالي**، حدد عملية التسجيل المالي التي قمت بإنشائها مسبقًا.
9. انتقل إلى **Retail وCommerce \> إعداد القناة \> إعداد نقطة البيع \> ملفات تعريف نقطة البيع \> ملفات تعريف الأجهزة**. حدد ملف تعريف الجهاز المرتبط بمحطة الأجهزة التي سيتم توصيل الطابعة المالية بها. في علامة التبويب السريعة **الأجهزة الطرفية المالية**، حدد ملف التعريف الفني للموصل الذي قمت بإنشائه مسبقًا.
10. افتح جدول التوزيع (**Retail وCommerce \>تكنولوجيا معلومات Retail وCommerce\> جدول التوزيع**)، وحدد الوظيفتين **1070** و **1090** لنقل البيانات إلى قاعدة بيانت القناة.

#### <a name="default-data-mapping"></a>تعيين البيانات الافتراضي

يتم تضمين تعيين البيانات الافتراضي التالي في تكوين موفر المستندات المالية الذي يتم توفيره كجزء من نموذج التكامل المالي:

- **تعيين كود ضريبة القيمة المضافة (VAT)** – يقوم هذا التعيين بتعيين أكواد الضريبة المضافة الخاصة بالجهاز (vat) إلى أكواد ضريبة المبيعات المقابلة. يجب ان يكون لتعيين كود ضريبة القيمة المضافة (VAT) التنسيق التالي:

    ```
    1 : code1 ; 2 : code2
    ```

    فيما يلي شرح هذا التنسيق:

    - يُعد كل من *1* و *2* أكواد ضريبة القيمة المضافة الخاصة بالجهاز.
    - فاصلة منقوطة (;) يتم استخدامها كفاصل.
    - إن *code1* و *code2* هما أكواد ضريبة المبيعات التي تم تكوينها في مقر Commerce الرئيسي. يجب عليك تعديل نموذج التعيين وفقًا لأكواد الضرائب التي تم تكوينها في التطبيق الخاص بك.

    تدعم وحدات التحكم ما يصل إلى أربعه أكواد ضريبة قيمه مضافه مختلفه. لذلك، قد يتم اعداد تعيين كود ضريبة القيمة المضافة بالطريقة التالية:

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > يمكن تعيين أكواد ضريبة مبيعات متعددة إلى نفس رمز ضريبة القيمة المضافة الخاص بالجهاز.

#### <a name="fiscal-connector-settings"></a>إعدادات الموصل المالي

يتم تضمين الإعدادات التالية في تكوين الرابط المالي الذي يتم توفيره كجزء من نموذج التكامل المالي:

- **سلسلة الاتصالات** – إعدادات اتصال وحدة التحكم.
- **المهلة** – مقدار الوقت، بالمللي ثانية، الذي سينتظر فيه برنامج التشغيل استجابة من وحدة التحكم.

### <a name="configure-channel-components"></a>تكوين مكونات القناة

> [!WARNING]
> وبسبب قيود [التعبئة المستقلة الجديدة ونموذج التوسيع](../dev-itpro/build-pipeline.md)، لا يمكن استخدامها حاليًا لنموذج التكامل المالي هذا. يجب استخدام الإصدار السابق من Retail SDK على الجهاز الظاهري (VM) للمطور في LCS. لمزيد من المعلومات، راجع [إرشادات التوزيع الخاصة بنموذج تكامل وحدة التحكم للسويد (قديم)](emea-swe-fi-sample-sdk.md).
>
> يتم تخطيط الدعم الخاص بالتعبئة المستقلة الجديدة ونموذج الملحق الخاص بنماذج التكامل المالي للإصدارات اللاحقة.

#### <a name="set-up-the-development-environment"></a>إعداد بيئة التطوير

لإعداد بيئة تطوير لاختبار العينة وتوسيعها، اتبع هذه الخطوات.

1. قم بنسخ مستودع [حلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) أو تنزيله. حدد إصدار فرع إصدار صحيح وفقا لإصدار التطبيق أو SDK الخاص بك. لمزيد من المعلومات، راجع [تنزيل نماذج Retail SDK والحزم المرجعية من GitHub وNuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. افتح حل تكامل الطابعة المالي على **Dynamics365Commerce.Solutions\\FiscalIntegration\\CleanCash\\CleanCash.sln**، وقم بإنشائه.
1. تثبيت ملحقات CRT:

    1. ابحث عن مثبت ملحق CRT:

        - **Commerce Scale Unit:** في مجلد **CleanCash\\ScaleUnit\\ScaleUnit.CleanCash.Installer\\bin\\Debug\\net461**، ابحث عن مثبت **ScaleUnit.CleanCash.Installer**.
        - **CRT المحلي على نقطة البيع الحديثة:** في مجلد **CleanCash\\ModernPOS\\ModernPOS.CleanCash.Installer\\bin\\Debug\\net461**، ابحث عن مثبت **ModernPOS.CleanCash.Installer**.

    2. ابدأ مثبت ملحق CRT من سطر الأوامر:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **CRT المحلي في نقطة البيع الحديثة:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. تثبيت ملحقات محطة الأجهزة:

    1. في مجلد **CleanCash\\HardwareStation\\HardwareStation.CleanCash.Installer\\bin\\Debug\\net461**، ابحث عن مثبت **HardwareStation.CleanCash.Installer**.
    1. أبدا بتشغيل مثبت الملحق من سطر الأوامر:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>بيئة الإنتاج

اتبع الخطوات الواردة في [إعداد تدفق البناء لنموذج تكامل مالي](fiscal-integration-sample-build-pipeline.md) لإنشاء وإصدار وحده مقياس السحابة وحزم الخدمة الذاتية القابلة للنشر لنموذج التكامل المالي. يمكن العثور على ملف YAML لقالب **CleanCash build-pipeline.yml** في مجلد **Pipeline\\YAML_Files** الخاص بمستودع [حلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-the-extensions"></a>تصميم الملحقات

تعتمد عينة تكامل وحدة التحكم في السويد على [وظيفة التكامل المالي](fiscal-integration-for-retail-channel.md) وهي جزء من Retail SDK. النموذج موجود في مجلد **src\\FiscalIntegration\\CleanCash** الخاص [بحلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)، المستودع (على سبيل المثال [النموذج في الإصدار/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). يتكون [النموذج](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) من موفر المستند المالي، وهو ملحق لـ (CRT)، والموصل المالي، وهو ملحق لمحطة أجهزة Commerce. لمزيد من المعلومات حول كيفيه استخدام Retail SDK، راجع [هندسة Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)و[قم بإعداد تدفق البناء لمجموعة SDK المستقلة](../dev-itpro/build-pipeline.md).

> [!WARNING]
> وبسبب قيود [التعبئة المستقلة الجديدة ونموذج التوسيع](../dev-itpro/build-pipeline.md)، لا يمكن استخدامها حاليًا لنموذج التكامل المالي هذا. يجب استخدام الإصدار السابق من Retail SDK على الجهاز الظاهري (VM) للمطور في LCS. لمزيد من المعلومات، راجع [إرشادات التوزيع الخاصة بنموذج تكامل وحدة التحكم للسويد (قديم)](emea-swe-fi-sample-sdk.md). يتم تخطيط الدعم الخاص بالتعبئة المستقلة الجديدة ونموذج الملحق الخاص بنماذج التكامل المالي للإصدارات اللاحقة.

### <a name="crt-extension-design"></a>تصميم ملحق CRT

الغرض من الملحق الذي يمثل موفر المستندات المالية هو إنشاء مستندات خاصة بالخدمة والتعامل مع الاستجابات من وحدة التحكم.

#### <a name="request-handler"></a>معالج الطلب

يوجد معالج طلب **DocumentProviderCleanCash** واحد لموفر المستندات. يتم استخدام هذا المعالج لإنشاء مستندات مالية لوحدة التحكم.

هذا المعالج موروث من واجهة **INamedRequestHandler**. طريقة **HandlerName** مسؤولة عن إرجاع اسم المعالج. يجب أن يتطابق اسم المعالج مع اسم موفر مستند الموصل المحدد في مقر Commerce الرئيسي.

يدعم الموصل الطلبات التالية:

- **GetFiscalDocumentDocumentProviderRequest** – يحتوي هذا الطلب على معلومات حول المستند الذي يجب إنشاؤه. تقوم بإرجاع مستند خاص بالخدمة يجب تسجيله في وحدة التحكم.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – يعيد هذا الطلب قائمة الأحداث للاشتراك فيها. حاليًا، يتم دعم أحداث المبيعات وأحداث التدقيق.

#### <a name="configuration"></a>تكوين

يوجد ملف التكوين لموفر المستند المالي في **src\\FiscalIntegration\\CleanCash\\CommerceRuntime\\DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml** في مستودع [حلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). الغرض من هذا الملف هو تمكين إعدادات موفر المستندات ليتم تكوينها من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي.

### <a name="hardware-station-extension-design"></a>تصميم ملحقات محطة الأجهزة

الغرض من الملحق الذي يمثل رابطًا ماليًا هو الاتصال بوحدة التحكم. يستخدم بروتوكول HTTP لإرسال المستندات التي ينشئها ملحق CRT لوحدة التحكم. كما أنه يتعامل مع الردود التي يتم تلقيها من وحدة التحكم.

#### <a name="request-handler"></a>معالج الطلب

معالج الطلب **CleanCashHandler** هو نقطة الإدخال لمعالجة الطلبات لوحدة التحكم.

المعالج موروث من واجهة **INamedRequestHandler**. طريقة **HandlerName** مسؤولة عن إرجاع اسم المعالج. يجب أن يتطابق اسم المعالج مع اسم الموصل المالي المحدد في مقر Commerce الرئيسي.

يدعم الموصل الطلبات التالية:

- **SubmitDocumentFiscalDeviceRequest** – يرسل هذا الطلب المستندات إلى وحدة التحكم ويعيد الرد منها.
- **IsReadyFiscalDeviceRequest** – يستخدم هذا الطلب لإجراء فحص سلامة لوحدة التحكم.
- **InitializeFiscalDeviceRequest** – يستخدم هذا الطلب لتهيئة وحدة التحكم.

#### <a name="configuration"></a>تكوين

يوجد ملف التكوين للموصل المالي في **src\\FiscalIntegration\\CleanCash\\HardwareStation\\Connector.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml** في مستودع [حلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). الغرض من الملف هو تمكين إعدادات الرابط المالي ليتم تكوينه من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
