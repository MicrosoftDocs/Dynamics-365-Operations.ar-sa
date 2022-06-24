---
title: إرشادات النشر لعينة تكامل خدمة التسجيل المالي لألمانيا (قديمة)
description: يوفر هذا المقال إرشادات لنشر نموذج التكامل المالي لألمانيا من مجموعة تطوير برامج Microsoft Dynamics 365 Commerce ‏Retail ‏(SDK).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 9f6ecc715e10538806998459b7fd837648494ad7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845827"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-germany-legacy"></a>إرشادات النشر لعينة تكامل خدمة التسجيل المالي لألمانيا (قديمة)

[!include [banner](../includes/banner.md)]

يوفر هذا المقال إرشادات لنشر نموذج تكامل خدمة التسجيل المالي لألمانيا من مجموعة تطوير برنامج Microsoft Dynamics 365 Commerce ‏(SDK) على جهاز ظاهري للمطور (VM) في Microsoft Dynamics Lifecycle Services ‏(LCS). لمزيد من المعلومات حول نموذج التكامل المالي هذا، راجع [عينة تكامل خدمة التسجيل المالي لألمانيا](emea-deu-fi-sample.md). 

تعد عينة التكامل المالي لألمانيا جزءًا من Retail SDK. للحصول على مزيد من المعلومات حول كيفية تثبيت واستخدام SDK، راجع [بنية مجموعة تطوير برنامج Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). يتكون هذا النموذج من ملحقات Commerce Runtime (CRT) ومحطة الأجهزة. لتشغيل هذا النموذج، يجب تعديل مشاريع CRT ومشاريع محطة الأجهزة وإنشائها. نوصي باستخدام Retail SDK غير معدل لإجراء التغييرات الموضحة في هذا المقال. نوصي أيضًا باستخدام نظام تحكم بالمصادر مثل Azure DevOps حيث لم يتم تغيير أي ملفات حتى الآن.

## <a name="development-environment"></a>بيئة التطوير

اتبع هذه الخطوات لإعداد بيئة تطوير بحيث يمكنك اختبار العينة وتوسيعها.

### <a name="enable-commerce-runtime-extensions"></a>تمكين ملحقات Commerce Runtime

تم تضمين مكونات ملحق CRT في نماذج CRT. لإكمال الإجراءات التالية، افتح حل **CommerceRuntimeSamples.sln** ضمن **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>مكون DocumentProvider.EFRSample

1. ابحث عن مشروع **Runtime.Extensions.DocumentProvider.EFRSample**، وقم بإنشائه.
2. في مجلد **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **Commerce Scale Unit:** انسخ الملف إلى مجلد **\\bin\\ext** ضمن موقع Commerce Scale Unit لخدمات معلومات الإنترنت (IIS).
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ الملف إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **Commerce Scale Unit:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهو موجود في مجلد **bin\\ext** ضمن موقع Commerce Scale Unit لخدمات معلومات الإنترنت (IIS).‬
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>مكون DocumentProvider.DataModelEFR

1. ابحث عن مشروع **Runtime.Extensions.DocumentProvider.DataModelEFR**، وقم بإنشائه.
2. في مجلد **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **Commerce Scale Unit:** انسخ الملف إلى مجلد **\\bin\\ext** ضمن موقع Commerce Scale Unit لخدمات معلومات الإنترنت (IIS).
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ الملف إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **Commerce Scale Unit:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهو موجود في مجلد **bin\\ext** ضمن موقع Commerce Scale Unit لخدمات معلومات الإنترنت (IIS).‬
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>ملف تكوين الملحق

1. ابحث عن ملف تكوين الملحق لـ CRT:

    - **Commerce Scale Unit:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهو موجود في مجلد **bin\\ext** ضمن موقع Commerce Scale Unit لخدمات معلومات الإنترنت (IIS).‬
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

2. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>تمكين ملحقات الموصل المالي

يمكنك تمكين ملحقات الموصل المالي في [محطة الأجهزة](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) أو [سجل نقطة البيع](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

#### <a name="enable-hardware-station-extensions"></a>تمكين ملحقات محطة الأجهزة

يتم تضمين مكونات توسيع محطة الأجهزة في عينات محطة الأجهزة. لإكمال الإجراءات التالية، افتح حل **HardwareStationSamples.sln** ضمن **RetailSdk\\SampleExtensions\\HardwareStation**.

##### <a name="efrsample-component"></a>مكون EFRSample

1. ابحث عن مشروع **HardwareStation.Extension.EFRSample**، وقم بإنشائه.
2. في مجلد **Extension.EFRSample\\bin\\Debug**،ابحث عن ملفات التجميع التالية:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. انسخ ملفات التجميع إلى مجلد ملحقات محطة الأجهزة:

    - **محطة الأجهزة المشتركة** انسخ الملفات إلى مجلد **الحاوية** ضمن موقع محطة أجهزة IIS.
    - **محطة الأجهزة المخصصة لنقاط البيع الحديثة:** انسخ الملفات إلى موقع وسيط عميل نقاط البيع الحديثة.

4. ابحث عن ملف تكوين الملحق لملحقات محطة الأجهزة. تمت تسمية الملف باسم **HardwareStation.Extension.config**.

    - **محطة الأجهزة المشتركة:** الملف موجود ضمن مكان موقع محطة أجهزة IIS.
    - **محطة الأجهزة المخصصة لنقاط البيع الحديثة:** الملف موجود ضمن موقع وسيط عميل نقاط البيع الحديثة.

5. أضف السطر التالي إلى قسم **التأليف** في ملف التكوين.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

#### <a name="enable-pos-extensions"></a>تمكين ملحقات POS

نموذج ملحق نقطة البيع موجود في مجلد **src\\FiscalIntegration\\PosFiscalConnectorSample** في مستودع [حلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).

لاستخدام نموذج ملحق نقطة البيع في SDK القديم، اتبع هذه الخطوات.

1. انسخ مجلد **Pos.Extension** إلى مجلد **ملحقات** نقطة البيع لـ SDK القديم (على سبيل المثال، `C:\RetailSDK\src\POS\Extensions`).
1. أعد تسمية نسخة مجلد **Pos.Extension** باسم **PosFiscalConnector**.
1. قم بازاله المجلدات والملفات التالية من المجلد **PosFiscalConnector**:

    - صندوق
    - DataService
    - devDependencies
    - المكتبات
    - obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - RetailServerEdmxModel.g.xml
    - tsconfig.json

1. افتح حل **CloudPos.sln** أو **ModernPos.sln**.
1. في مشروع **Pos.Extensions**، قم بتضمين مجلد **PosFiscalConnector**.
1. افتح ملف **extensions.json**، وأضف ملحق **PosFiscalConnector**.
1. أنشئ SDK.

### <a name="production-environment"></a>بيئة الإنتاج

في الإجراء السابق، قمت بتمكين الامتدادات التي تشكل مكونات نموذج تكامل خدمة التسجيل المالي. بالإضافة إلى ذلك، يجب اتباع هذه الخطوات لإنشاء حزم قابلة للنشر تحتوي على مكونات التجارة، ولتطبيق هذه الحزم في بيئة إنتاج.

1. قم بإجراء التغييرات التالية في ملفات تكوين الحزمة ضمن مجلد **RetailSdk\\Assets**:

    - في ملفات تكوين **commerceruntime.ext.config** و **CommerceRuntime.MPOSOffline.Ext.config**، أضف الأسطر التالية إلى قسم **التأليف**.

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

    - في ملف تكوين **HardwareStation.Extension.config**، أضف الأسطر التالية إلى قسم **التأليف**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. قم بإجراء التغييرات التالية في ملف تكوين تخصيص حزمة **Customization.settings** ضمن مجلد **BuildTools**:

    - أضف الأسطر التالية لتضمين ملحقات CRT في الحزم القابلة للنشر.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - أضف الأسطر التالية لتضمين ملحقات محطة الأجهزة في الحزم القابلة للنشر.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. أبدا تشغيل موجه الأوامر MSBuild للحصول على أداة Visual Studio المساعدة، وقم بتشغيل **msbuild** ضمن مجلد Retail SDK لإنشاء الحزم القابلة للنشر.
4. قم بتطبيق الحزم من خلال LCS أو يدويًا. لمزيد من المعلومات، راجع [إنشاء الحزم القابلة للنشر](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. أكمل كافة مهام الاعداد المطلوبة الموضحة في [اعداد Commerce الخاص بألمانيا](emea-deu-fi-sample.md#set-up-commerce-for-germany).

## <a name="design-of-extensions"></a>تصميم الملحقات

تعتمد عينة تكامل خدمة التسجيل المالي لألمانيا في [وظيفة التكامل المالي](fiscal-integration-for-retail-channel.md). لمزيد من المعلومات حول تصميم حل التكامل المالي، راجع [نظرة عامة على تصميم نموذج التكامل](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>تصميم ملحق Commerce Runtime

الغرض من الامتداد الذي يمثل موفر المستندات المالية هو إنشاء مستندات خاصة بالخدمة ومعالجة الاستجابات من خدمة التسجيل المالي.

ملحق CRT هو **Runtime.Extensions.DocumentProvider.EFRSample**. لمزيد من المعلومات حول تصميم حل التكامل المالي، راجع [نظرة عامة على التكامل المالي لقنوات Commerce](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>معالج الطلب

يوجد معالج طلب واحد لموفر المستندات، **DocumentProviderEFRFiscalDEU**. يتم استخدام هذا المعالج لإنشاء مستندات مالية لخدمة التسجيل المالي. إنه موروث من واجهة **INamedRequestHandler**. طريقة **HandlerName** مسؤولة عن إرجاع اسم المعالج. يجب أن يتطابق اسم المعالج مع اسم موفر مستند الموصل المحدد في مقر Commerce الرئيسي.

يدعم الموصل الطلبات التالية:

- **GetFiscalDocumentDocumentProviderRequest** – يحتوي هذا الطلب على معلومات حول المستند الذي يجب إنشاؤه. تقوم بإرجاع مستند خاص بالخدمة يجب تسجيله في خدمة التسجيل المالي.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – يعيد هذا الطلب الاستجابة مع البيانات الموسعة.

#### <a name="configuration"></a>تكوين

يوجد ملف تكوين **DocumentProviderFiscalEFRSampleGermany** في مجلد **التكوين** لمشروع الملحق. الغرض من هذا الملف هو تمكين إعدادات موفر المستندات ليتم تكوينها من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي.

تمت إضافة الإعدادات التالية:

- **تعيين أسعار ضريبة القيمة المضافة** – تعيين قيم النسبة المئوية للضريبة التي تم اعدادها لأكواد ضريبة المبيعات إلى قيم سمة **TaxG** (مجموعه الضرائب) في الطلبات التي يتم إرسالها إلى الخدمة المالية.
- **المجموعة الضريبية لبطاقات الهدايا والودائع** – قيمة سمة **TaxG** في الطلبات التي يتم إرسالها إلى الخدمة المالية، بناءً على العمليات التي تتضمن بطاقات هدايا أو إيداعات.
- **تعيين أنواع طرق الدفع** – تعيين طرق الدفع لقيم سمة **PayG** (مجموعة الدفع) في الطلبات التي تم إرسالها إلى الخدمة المالية.
- **مجموعة الضرائب لإعفاء ضريبة القيمة المضافة** – قيمة سمة **TaxG** في الطلبات التي يتم إرسالها إلى الخدمة المالية، استنادا إلى العمليات المعفاة من التزامات الضرائب.
- **تضمين بيانات العميل** – إذا تم تشغيل هذه المعلمة، فستحتوي الطلبات إلى الخدمة المالية على معلومات العميل، مثل الأسماء والعناوين، في الحالات التي تتم فيها إضافة عميل إلى حركة.

### <a name="hardware-station-extension-design"></a>تصميم ملحقات محطة الأجهزة

الغرض من الامتداد الذي يعتبر رابطًا ماليًا هو الاتصال بخدمة التسجيل المالي.

ملحق محطة الأجهزة هو **HardwareStation.Extension.EFRSample**. يستخدم بروتوكول HTTP لإرسال المستندات التي ينشئها ملحق CRT لخدمة التسجيل المالية. كما أنه يتعامل مع الاستجابات التي يتم تلقيها من خدمة التسجيل المالي.

#### <a name="request-handler"></a>معالج الطلب

معالج طلب **EFRHandler** هو نقطة الإدخال لمعالجة الطلبات إلى خدمة التسجيل المالي. هذا المعالج موروث من واجهة **INamedRequestHandler**. طريقة **HandlerName** مسؤولة عن إرجاع اسم المعالج. يجب أن يتطابق اسم المعالج مع اسم الموصل المالي المحدد في مقر Commerce الرئيسي.

يدعم الموصل الطلبات التالية:

- **SubmitDocumentFiscalDeviceRequest** – يرسل هذا الطلب المستندات إلى خدمة التسجيل المالي ويعيد ردًا منها.
- **IsReadyFiscalDeviceRequest** – يُستخدم هذا الطلب لإجراء فحص سلامة لخدمة التسجيل المالي.
- **InitializeFiscalDeviceRequest** – يستخدم هذا الطلب لتهيئة خدمة التسجيل المالي.

#### <a name="configuration"></a>تكوين

ملف التكوين موجود في مجلد **التكوين** لمشروع الملحق. الغرض من الملف هو تمكين إعدادات الرابط المالي ليتم تكوينه من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي.

تمت إضافة الإعدادات التالية:

- **عنوان نقطة النهاية** – عنوان URL الخاص بخدمه التسجيل المالية.
- **المهلة** – مقدار الوقت بالمللي ثانية الذي سينتظره برنامج التشغيل للحصول على استجابة من خدمة التسجيل المالي.
- **إظهار إخطارات التسجيل المالي** - في حاله تشغيل هذه المعلمة، سيتم عرض الإخطارات من الخدمة المالية كرسائل للمستخدمين في نقطه البيع.

### <a name="pos-fiscal-connector-extension-design"></a>تصميم ملحق موصل POS المالي

الغرض من امتداد الرابط المالي لنقاط البيع هو التواصل مع خدمة التسجيل المالي من نقطة البيع. يستخدم بروتوكول HTTPS للاتصال.

#### <a name="fiscal-connector-factory"></a>مصنع الموصل المالي

يقوم مصنع الموصل المالي بتعيين اسم الموصل إلى تطبيق الموصل المالي ويوجد في ملف **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts**. يجب أن يتطابق اسم الموصل مع اسم الموصل المالي المحدد في مقر Commerce الرئيسي.

#### <a name="efr-fiscal-connector"></a>الموصل المالي لـ EFR

يوجد الموصل المالي EFR في ملف **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts**. يقوم بتنفيذ واجهة **IFiscalConnector** التي تدعم الطلبات التالية:

- **FiscalRegisterSubmitDocumentClientRequest** – يرسل هذا الطلب المستندات إلى خدمة التسجيل المالي ويعيد ردًا منها.
- **FiscalRegisterIsReadyClientRequest** – يُستخدم هذا الطلب لإجراء فحص سلامة لخدمة التسجيل المالي.
- **FiscalRegisterInitializeClientRequest** – يستخدم هذا الطلب لتهيئة خدمة التسجيل المالي.

#### <a name="configuration"></a>تكوين

ملف التكوين موجود في مجلد **src\\FiscalIntegration\\Efr\\التكوينات\\الموصلات** في مستودع [حلول Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). الغرض من الملف هو تمكين إعدادات الرابط المالي ليتم تكوينه من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي. تمت إضافة الإعدادات التالية:

- **عنوان نقطة النهاية** – عنوان URL الخاص بخدمه التسجيل المالية.
- **المهلة** – مقدار الوقت بالمللي ثانية الذي سينتظره الموصل للحصول على استجابة من خدمة التسجيل المالي.
