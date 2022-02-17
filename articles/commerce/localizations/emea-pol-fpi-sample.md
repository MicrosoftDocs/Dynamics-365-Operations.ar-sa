---
title: عينة تكامل طابعة الضرائب المحصلة لبولندا
description: يقدم هذا الموضوع نظرة عامة على عينة التكامل المالي لبولندا في Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-2-1
ms.openlocfilehash: 43d9a54334d97a65a1f9a356daf54154f6c069b3
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076826"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>عينة تكامل طابعة الضرائب المحصلة لبولندا

[!include[banner](../includes/banner.md)]

يقدم هذا الموضوع نظرة عامة على عينة التكامل المالي لبولندا في Microsoft Dynamics 365 Commerce.

تتضمن وظيفة Dynamics 365 Commerce لبولندا نموذجًا لتكامل نقطة البيع (POS) مع طابعة مالية. يقوم النموذج بتوسيع [وظيفة التكامل المالي](fiscal-integration-for-retail-channel.md) ويدعم بروتوكول POSNET THERMAL HD 2.02 للطابعات المالية من شركة [Posnet Polska S.A.](https://www.posnet.com.pl) يتيح النموذج الاتصال بطابعة مالية متصلة عبر منفذ COM باستخدام برنامج تشغيل أصلي. تم تنفيذه واختباره باستخدام محاكي برمجي قدمته Posnet للطابعة المالية Posnet Thermal HD FV EJ. يتم توفير العينة في شكل كود المصدر وهي جزء من مجموعة تطوير برامج البيع بالتجزئة (SDK).

لا تصدر Microsoft إيه أجهزه أو برامج أو وثائق من Posnet. للحصول على معلومات حول كيفية الحصول على الطابعة المالية وتشغيلها، اتصل بشركة [Posnet Polska S.A.](https://www.posnet.com.pl).

## <a name="scenarios"></a>السيناريوهات

يتم تغطية السيناريوهات التالية بواسطة عينة تكامل الطابعة المالية لبولندا:

- سيناريوهات المبيعات:

    - اطبع إيصالًا ماليًا للمبيعات والمرتجعات نقدًا وبالاستلام.
    - قم بالتقاط استجابه من الطابعة المالية، ثم قم بتخزينها في قاعده بيانات القناة.
    - الضرائب:

        - تعيين إلى أكواد الضريبة للطابعة المالية (الأقسام).
        - تحويل بيانات الضريبة المعينة إلى الطابعة المالية.

    - المدفوعات:

        - تعيين إلى طرق الدفع الخاصة بالطابعة المالية.
        - طباعة المدفوعات على إيصال مالي.
        - طباعه معلومات التغيير.

    - طباعة خصومات البند.
    - بطاقات الهدايا:

        - استبعاد بند بطاقة الهدايا الذي تم إصداره/أعاده تحميله من إيصال مالي للبيع.
        - يستخدم هذا الزر في طباعه عمليه دفع تستخدم بطاقة الهدايا كطريقه دفع دوريه.

    - طباعه عمليات الاستلام المالية لعمليات أمر العميل:

        - لا تتم طباعه إيصال مالي لإيداع أمر العميل.
        - اطبع إيصالًا ماليًا للبنود المرحلة لأمر عميل مختلط.
        - يستخدم في طباعه إيصال مالي لعمليه الانتقاء الخاصة بامر العميل.
        - طباعه إيصال مالي لأمر إرجاع.

    - اطبع [معلومات العميل](emea-pol-customer-information.md) المحددة لحركة مبيعات في إيصال مالي. مثال على هذه المعلومات هو رقم ضريبة القيمة المضافة للعميل.

- كشوفات نهاية اليوم (تقارير X المالية وتقارير Z المالية).
- معالجه الأخطاء، مثل الخيارات التالية:

    - أعد محاولة التسجيل المالي إذا كانت إعادة المحاولة ممكنة، على سبيل المثال إذا كانت الطابعة المالية غير متصلة أو غير جاهزة أو لا تستجيب أو نفد الورق من الطابعة أو حدث انحشار للورق.
    - تأجيل عملية التسجيل المالي.
    - يستخدم لتخطي التسجيل المالي أو وضع علامة علي الحركة كمسجله، وتضمين رموز المعلومات للتقاط سبب الفشل والمعلومات الاضافيه.
    - تحقق من توفر الطابعة المالية قبل فتح معاملة مبيعات جديدة أو إنهاء معاملة المبيعات.

### <a name="gift-cards"></a>بطاقات الهدايا

تطبق عينة تكامل الطابعة المالية القواعد التالية المتعلقة ببطاقات الهدايا:

- استبعاد سطور المبيعات ذات الصلة بعمليتي *إصدار بطاقة الهدايا* و *إضافة إلى بطاقة الهدايا* من الإيصال الضريبي.
- لا تطبع إيصالًا ماليًا إذا كان يتكون من خطوط بطاقة هدايا فقط.
- قم بخصم المبلغ الإجمالي لبطاقات الهدايا التي تم إصدارها أو إعادة تحصيلها في معاملة من سطور الدفع الخاصة بالإيصال المالي.
- حفظ التسويات المحسوبة لبنود الدفع في قاعده بيانات القناة مع وجود مرجع لحركه مالية مقابله.
- ويعتبر الدفع حسب بطاقة الهدايا دفعا منتظما.

### <a name="customer-deposits-and-customer-order-deposits"></a>ودائع العملاء وودائع أوامر العملاء

يطبق نموذج تكامل الطابعة المالية القواعد التالية المتعلقة بإيداعات العملاء وإيداعات أوامر العميل:

- لا تقم بطباعه إيصال مالي إذا كانت الحركة عبارة عن إيداع للعميل.
- لا تطبع إيصالًا ماليًا إذا كانت المعاملة تحتوي فقط على إيداع طلب العميل أو استرداد إيداع طلب العميل.
- قم بطباعه مبلغ الإيداع السابق الذي تم دفعه في إيصال مالي لعمليه انتقاء أمر العميل.
- خصم مبلغ إيداع أمر العميل من بنود الدفع عند إنشاء أمر عميل مختلط.
- احفظ التعديلات المحسوبة لبنود الدفع في قاعدة بيانات القناة بمرجع إلى حركة مالية لأمر زبون مختلط.

### <a name="limitations-of-the-sample"></a>قيود العينة

- تدعم الطابعة المالية فقط السيناريوهات التي يتم فيها تضمين ضريبة المبيعات في السعر. لذلك، يجب تعيين خيار **السعر شامل ضريبة المبيعات** إلى **نعم** لكل من المتاجر والعملاء.
- تتم طباعه التقارير اليومية (X المالية X و Z) باستخدام تنسيق *تقرير الوردية* المدمج.
- يعتبر طباعه الكود الشريطي في الإيصالات المالية تخصيصا محتملا، لان هذه الميزة غير معتمده في التنسيقات المضمنة ويمكن تطبيقها فقط باستخدام تقرير **التنسيق الفائق** القابل للتخصيص.
- الطابعة المالية لا تدعم الحركات المختلطة. يجب تعيين خيار **منع خلط المبيعات والإرجاع في إيصال واحد** إلى **نعم** في ملفات تعريف وظائف نقطة البيع.

## <a name="set-up-fiscal-integration-for-poland"></a>إعداد التكامل المالي لبولندا

تعتمد عينة تكامل الطابعة المالية لبولندا على [وظيفة التكامل المالي](fiscal-integration-for-retail-channel.md) وهي جزء من Retail SDK. النموذج موجود في مجلد **src\\FiscalIntegration\\Posnet** الخاص [بحلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)، المستودع (على سبيل المثال [النموذج في الإصدار/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). يتكون [النموذج](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) من موفر المستند المالي، وهو امتداد لCommerce Runtime (CRT)، والموصل المالي، وهو امتداد لمحطة أجهزة Commerce. لمزيد من المعلومات حول كيفيه استخدام Retail SDK، راجع [هندسة Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)و[قم بإعداد تدفق البناء لمجموعة SDK المستقلة](../dev-itpro/build-pipeline.md).

> [!WARNING]
> وبسبب قيود [التعبئة المستقلة الجديدة ونموذج التوسيع](../dev-itpro/build-pipeline.md)، لا يمكن استخدامها حاليًا لنموذج التكامل المالي هذا. يجب استخدام الإصدار السابق من Retail SDK على الجهاز الظاهري (VM) للمطور في Microsoft Dynamics Lifecycle Services (LCS). لمزيد من المعلومات، راجع [إرشادات التوزيع الخاصة بنموذج تكامل الطابعة المالي لبولندا (قديم)](emea-pol-fpi-sample-sdk.md).
>
> يتم تخطيط الدعم الخاص بالتعبئة المستقلة الجديدة ونموذج الملحق الخاص بنماذج التكامل المالي للإصدارات اللاحقة.

قم بإكمال خطوات اعداد التكامل المالي كما هو موضح في [اعداد التكامل المالي لقنوات Commerce](setting-up-fiscal-integration-for-retail-channel.md).

1. [إعداد عملية التسجيل المالي](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). وكذلك قم بتسجيل الإعدادات الخاصة بعمليه التسجيل المالي [الخاصة بنموذج تكامل الطابعة المالية هذه](#set-up-the-registration-process).
1. [تعيين إعدادات معالجة الأخطاء‬](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [إعداد التقارير المالية X/Z من نقطة البيع](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [تمكين التنفيذ اليدوي للتسجيل المالي المؤجل](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [تكوين مكونات القناة](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>إعداد عملية التسجيل

لتمكين عملية التسجيل، اتبع هذه الخطوات لإعداد مقر Commerce الرئيسي. لمزيد من المعلومات، راجع [إعداد التكامل المالي لقنوات Commerce](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. تنزيل ملفات التكوين لموفر المستند المالي والموصل المالي:

    1. افتح مستودع [حلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. حدد إصدار فرع إصدار صحيح وفقا لإصدار التطبيق أو SDK الخاص بك (علي سبيل المثال، **[إصدار/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. افتح **src \> FiscalIntegration \> Posnet**.
    1. قم بتنزيل ملف تكوين موفر المستند المالي في **CommerceRuntime \> DocumentProvider.PosnetSample \> Configuration \> DocumentProviderPosnetSample.xml** (على سبيل المثال، [ملف الإصدار/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/CommerceRuntime/DocumentProvider.PosnetSample/Configuration/DocumentProviderPosnetSample.xml)).
    1. قم بتنزيل ملف تكوين الموصل المالي في **HardwareStation \> ThermalDeviceSample \> Configuration \> ConnectorPosnetThermalFVEJ.xml** (على سبيل المثال، [ملف الإصدار/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/HardwareStation/ThermalDeviceSample/Configuration/ConnectorPosnetThermalFVEJ.xml)).

    > [!WARNING]
    > وبسبب قيود [التعبئة المستقلة الجديدة ونموذج التوسيع](../dev-itpro/build-pipeline.md)، لا يمكن استخدامها حاليًا لنموذج التكامل المالي هذا. يجب استخدام الإصدار السابق من Retail SDK على الجهاز الظاهري (VM) للمطور في LCS. توجد ملفات التكوين لعينة التكامل المالي هذه في المجلدات التالية من Retail SDK على الجهاز الظاهري VM للمطور في LCS:
    >
    > - **ملف تكوين موفري المستندات المالية:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml
    > - **ملف تكوين الموصل المالي:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.Posnet.ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml
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

- **تعيين معدلات القيمة المضافة (VAT)** - تعيين قيم النسبة المئوية للضريبة التي يتم اعدادها لأكواد ضريبة المبيعات إلى الطابعة المالية – معدلات ضريبة القيمة المضافة الخاصة. هنا هو التعيين الافتراضي:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    يمثل المكون الأول في كل زوج رقم معدل ضريبة القيمة المضافة الذي تم تكوينه في طابعه الضرائب المحصلة. المكون الثاني يمثل معدل ضريبة القيمة المضافة المقابلة. لمزيد من المعلومات حول تكوين معدل ضريبة القيمة المضافة للطابعة المالية، راجع وثائق برنامج تشغيل POSNET.

- **تعيين نوع طريقة الدفع** - تعيين طرق الدفع التي تم تكوينها للمخزن لنماذج الدفع التي تدعمها الطابعة المالية. هنا هو التعيين الافتراضي:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    يمثل المكون الأول في كل زوج طريقه الدفع التي يتم اعدادها للمتجر. يمثل المكون الثاني نموذج الدفع المقابل الذي تدعمه الطابعة المالية. لمزيد من المعلومات حول نماذج الدفع التي تدعمها الطابعة المالية، راجع وثائق برنامج تشغيل POSNET. يجب تعديل تعيين النموذج وفقا لطرق الدفع التي تم تكوينها في التطبيق الخاص بك.

#### <a name="fiscal-connector-settings"></a>إعدادات الموصل المالي

يتم تضمين الإعدادات التالية في تكوين الرابط المالي الذي يتم توفيره كجزء من نموذج التكامل المالي:

- **سلسله الاتصال** – سلسله تصف تفاصيل الاتصال بالجهاز بأحد التنسيقات التي يدعمها برنامج التشغيل. لمزيد من المعلومات، راجع وثائق برنامج تشغيل POSNET.
- **مزامنة التاريخ والوقت** - قيمه تحدد ما إذا كان يجب مزامنة تاريخ الطابعة ووقتها مع محطه الاجهزه المتصلة.
- **مهلة الجهاز** – مقدار الوقت، بالمللي ثانية، الذي سينتظر فيه برنامج التشغيل استجابة من الجهاز. لمزيد من المعلومات، راجع وثائق برنامج تشغيل POSNET.

### <a name="configure-channel-components"></a>تكوين مكونات القناة

> [!WARNING]
> وبسبب قيود [التعبئة المستقلة الجديدة ونموذج التوسيع](../dev-itpro/build-pipeline.md)، لا يمكن استخدامها حاليًا لنموذج التكامل المالي هذا. يجب استخدام الإصدار السابق من Retail SDK على الجهاز الظاهري (VM) للمطور في LCS. لمزيد من المعلومات، راجع [إرشادات التوزيع الخاصة بنموذج تكامل الطابعة المالي لبولندا (قديم)](emea-pol-fpi-sample-sdk.md).
>
> يتم تخطيط الدعم الخاص بالتعبئة المستقلة الجديدة ونموذج الملحق الخاص بنماذج التكامل المالي للإصدارات اللاحقة.

#### <a name="set-up-the-development-environment"></a>إعداد بيئة التطوير

لإعداد بيئة تطوير لاختبار العينة وتوسيعها، اتبع هذه الخطوات.

1. قم بنسخ مستودع [حلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) أو تنزيله. حدد إصدار فرع إصدار صحيح وفقا لإصدار التطبيق أو SDK الخاص بك. لمزيد من المعلومات، راجع [تنزيل نماذج Retail SDK والحزم المرجعية من GitHub وNuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. افتح حل تكامل الطابعة المالي على **Dynamics365Commerce.Solutions\\FiscalIntegration\\Posnet\\Posnet.sln**، وقم بإنشائه.
1. تثبيت ملحقات CRT:

    1. ابحث عن مثبت ملحق CRT:

        - **Commerce Scale Unit:** في مجلد **Posnet\\ScaleUnit\\ScaleUnit.Posnet.Installer\\bin\\Debug\\net461**، ابحث عن مثبت **ScaleUnit.Posnet.Installer**.
        - **CRT المحلي في نقطة البيع الحديثة:** في مجلد **Posnet\\ModernPOS\\ModernPOS.Posnet.Installer\\bin\\Debug\\net461**، ابحث عن مثبت **ModernPOS.Posnet.Installer**.

    1. ابدأ مثبت ملحق CRT من سطر الأوامر:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **CRT المحلي في نقطة البيع الحديثة:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. تثبيت ملحقات محطة الأجهزة:

    1. في مجلد **Posnet\\HardwareStation\\HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\bin\\Debug\\net461**، ابحث عن مثبت **HardwareStation.PosnetThermalFVFiscalPrinter.Installer**.
    1. أبدا بتشغيل مثبت الملحق من سطر الأوامر:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>بيئة الإنتاج

اتبع الخطوات الواردة في [إعداد تدفق البناء لنموذج تكامل مالي](fiscal-integration-sample-build-pipeline.md) لإنشاء وإصدار وحده مقياس السحابة وحزم الخدمة الذاتية القابلة للنشر لنموذج التكامل المالي. يمكن العثور على ملف YAML لقالب **Posnet build-pipeline.yml** في مجلد **Pipeline\\YAML_Files** الخاص بمستودع [حلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>تصميم الملحقات

تعتمد عينة تكامل الطابعة المالية لبولندا على [وظيفة التكامل المالي](fiscal-integration-for-retail-channel.md) وهي جزء من Retail SDK. النموذج موجود في مجلد **src\\FiscalIntegration\\Posnet** الخاص [بحلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)، المستودع (على سبيل المثال [النموذج في الإصدار/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). يتكون [النموذج](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) من موفر المستند المالي، وهو ملحق لـ (CRT)، والموصل المالي، وهو ملحق لمحطة أجهزة Commerce. لمزيد من المعلومات حول كيفيه استخدام Retail SDK، راجع [هندسة Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)و[قم بإعداد تدفق البناء لمجموعة SDK المستقلة](../dev-itpro/build-pipeline.md).

> [!WARNING]
> وبسبب قيود [التعبئة المستقلة الجديدة ونموذج التوسيع](../dev-itpro/build-pipeline.md)، لا يمكن استخدامها حاليًا لنموذج التكامل المالي هذا. يجب استخدام الإصدار السابق من Retail SDK على الجهاز الظاهري (VM) للمطور في LCS. لمزيد من المعلومات، راجع [إرشادات التوزيع الخاصة بنموذج تكامل الطابعة المالي لبولندا (قديم)](emea-pol-fpi-sample-sdk.md). يتم تخطيط الدعم الخاص بالتعبئة المستقلة الجديدة ونموذج الملحق الخاص بنماذج التكامل المالي للإصدارات اللاحقة.

### <a name="commerce-runtime-extension-design"></a>تصميم ملحق Commerce Runtime

الغرض من الملحق الذي يمثل موفر المستندات المالية هو إنشاء مستندات خاصة بالطابعة والتعامل مع الاستجابات من الطابعة المالية. ينشئ هذا الملحق مجموعة من الأوامر الخاصة بالطابعة بتنسيق JavaScript Object Notation (JSON) التي تم تحديدها بواسطة مواصفة POSNET رقم 19-3678.

#### <a name="request-handler"></a>معالج الطلب

إن معالج طلب **DocumentProviderPosnetProtocol** هو نقطه الإدخال الخاصة بالطلب لإنشاء مستندات من الطابعة المالية.

المعالج موروث من واجهة **INamedRequestHandler**. طريقة **HandlerName** مسؤولة عن إرجاع اسم المعالج. يجب أن يتطابق اسم المعالج مع اسم موفر مستند الموصل المحدد في مقر Commerce الرئيسي.

يدعم الموصل الطلبات التالية:

- **GetFiscalDocumentDocumentProviderRequest** – يحتوي هذا الطلب على معلومات حول المستند الذي يجب إنشاؤه. تقوم بإرجاع مستند خاص بالطابعة يجب تسجيله في الطابعة المالية.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – يعيد هذا الطلب قائمة الأحداث للاشتراك فيها. حاليًا، يتم دعم الأحداث التالية: المبيعات وطباعة تقرير X وطباعة تقرير Z.

#### <a name="configuration"></a>تكوين

يوجد ملف التكوين لموفر المستند المالي في **src\\FiscalIntegration\\Posnet\\CommerceRuntime\\DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml** في مستودع [حلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). الغرض من هذا الملف هو تمكين إعدادات موفر المستندات المالية المراد تكوينها من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي.

### <a name="hardware-station-extension-design"></a>تصميم ملحقات محطة الأجهزة

الغرض من الملحق الذي يمثل رابطًا ماليًا هو الاتصال بالطابعة المالية. يستدعي هذا الملحق وظائف برنامج تشغيل POSNET لإرسال الأوامر التي ينشئها ملحق CRT للطابعة المالية. كما يعالج أخطاء الجهاز.

#### <a name="request-handler"></a>معالج الطلب

معالج الطلب **FiscalPrinterHandler** هو نقطة الإدخال لمعالجة الطلب للجهاز المالي الطرفي.

المعالج موروث من واجهة **INamedRequestHandler**. طريقة **HandlerName** مسؤولة عن إرجاع اسم المعالج. يجب أن يتطابق اسم المعالج مع اسم الموصل المالي المحدد في مقر Commerce الرئيسي.

يدعم الموصل الطلبات التالية:

- **SubmitDocumentFiscalDeviceRequest** – يرسل هذا الطلب المستندات إلى الطابعات ويعيد الاستجابة من الطابعة المالية.
- **IsReadyFiscalDeviceRequest** – يستخدم هذا الطلب لإجراء فحص سلامة الجهاز.
- **InitializeFiscalDeviceRequest** – يستخدم هذا الطلب لتهيئة الطابعة.

#### <a name="configuration"></a>تكوين

يوجد ملف التكوين للموصل المالي في **src\\FiscalIntegration\\Posnet\\HardwareStation\\ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml** في مستودع [حلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). الغرض من الملف هو تمكين إعدادات الموصل المالي ليتم تكوينه من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]