---
title: إرشادات النشر لعينة تكامل خدمة التسجيل المالي للنمسا (قديمة)
description: يوفر هذا الموضوع إرشادات لنشر نموذج التكامل المالي للنمسا من مجموعة تطوير برامج Microsoft Dynamics 365 Commerce ‏Retail ‏(SDK).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 7cb0e7b665add397b12e1a841b6a2e9565528d6d
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/19/2022
ms.locfileid: "8613926"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-austria-legacy"></a>إرشادات النشر لعينة تكامل خدمة التسجيل المالي للنمسا (قديمة)

[!include [banner](../includes/banner.md)]

يوفر هذا الموضوع إرشادات لنشر نموذج تكامل خدمة التسجيل المالي للنمسا من مجموعة تطوير برنامج Microsoft Dynamics 365 Commerce ‏(SDK) على جهاز ظاهري للمطور (VM) في Microsoft Dynamics Lifecycle Services ‏(LCS). لمزيد من المعلومات حول نموذج التكامل المالي هذا، راجع [عينة تكامل خدمة التسجيل المالي للنمسا](emea-aut-fi-sample.md). 

تعد عينة التكامل المالي للنمسا جزءًا من Retail SDK. للحصول على مزيد من المعلومات حول كيفية تثبيت واستخدام SDK، راجع [بنية مجموعة تطوير برنامج Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). تتكون عينة التكامل المالي من ملحقات لـ Commerce Runtime (CRT) ومحطة الأجهزة ونقطة البيع (POS). لتشغيل هذا النموذج، يجب تعديل مشاريع CRT ومحطة الأجهزة ونقاط البيع وإنشائها. نوصي باستخدام Retail SDK غير معدل لإجراء التغييرات الموضحة في هذا الموضوع. نوصي أيضًا باستخدام نظام تحكم بالمصادر مثل Azure DevOps حيث لم يتم تغيير أي ملفات حتى الآن.

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
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
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

### <a name="enable-modern-pos-extension-components"></a>تمكين مكونات ملحقات نقاط البيع الحديثة

1. افتح حل **ModernPOS.sln** ضمن **RetailSdk\\POS**، وتأكد من إمكانية تجميعه بدون أخطاء. بالإضافة إلى ذلك، تأكد من أنه يمكنك تشغيل نقطة البيع الحديثة Visual Studio باستخدام أمر **التشغيل**.

    > [!NOTE]
    > يجب عدم تخصيص نقطة البيع الحديثة. يجب عليك تمكين التحكم في حساب المستخدم (UAC)، ويجب عليك إلغاء تثبيت مثيلات نقطة البيع الحديثة المثبتة مسبقًا كما هو مطلوب.

2. قم بتمكين الملحقات المراد تحميلها عن طريق إضافة الأسطر التالية في ملف **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > لمزيد من المعلومات، وللحصول على نماذج توضح كيفية تضمين مجلدات التعليمات البرمجية المصدر وتمكين تحميل الامتدادات، راجع الإرشادات الموجودة في ملف readme.md في مشروع **Pos.Extensions**.

3. أعد إنشاء الحل.
4. قم بتشغيل Modern POS في مصحح الأخطاء، واختبر الوظيفة.

### <a name="enable-cloud-pos-extension-components"></a>تمكين مكونات ملحقات نقطة بيع المجموعة

1. افتح حل **CloudPOS.sln** ضمن **RetailSdk\\POS**، وتأكد من إمكانية تجميعه بدون أخطاء.
2. قم بتمكين الملحقات المراد تحميلها عن طريق إضافة الأسطر التالية في ملف **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > لمزيد من المعلومات، وللحصول على نماذج توضح كيفية تضمين مجلدات التعليمات البرمجية المصدر وتمكين تحميل الامتدادات، راجع الإرشادات الموجودة في ملف readme.md في مشروع **Pos.Extensions**.

3. أعد إنشاء الحل.
4. قم بتشغيل الحل باستخدام أمر **التشغيل** واتباع الخطوات الموجودة في دليل Retail SDK.

## <a name="production-environment"></a>بيئة الإنتاج

يتيح الإجراء السابق الملحقات التي تشكل مكونات عينة تكامل خدمة التسجيل المالي. بالإضافة إلى ذلك، يجب اتباع هذه الخطوات لإنشاء حزم قابلة للنشر تحتوي على مكونات التجارة، ولتطبيق هذه الحزم في بيئة إنتاج.

1. قم بإجراء التغييرات التالية في ملفات تكوين الحزمة ضمن مجلد **RetailSdk\\Assets**:

    - في ملفات تكوين **commerceruntime.ext.config** و **CommerceRuntime.MPOSOffline.Ext.config**، أضف الأسطر التالية إلى قسم **التأليف**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    - في ملف تكوين **HardwareStation.Extension.config**، أضف السطر التالي إلى قسم **التأليف**.

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

    - أضف السطر التالي لتضمين ملحق محطة الأجهزة في الحزم القابلة للنشر.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. أبدا تشغيل موجه الأوامر MSBuild للحصول على أداة Visual Studio المساعدة، وقم بتشغيل **msbuild** ضمن مجلد Retail SDK لإنشاء الحزم القابلة للنشر.
4. قم بتطبيق الحزم من خلال LCS أو يدويًا. لمزيد من المعلومات، راجع [إنشاء الحزم القابلة للنشر](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. أكمل كافة مهام الاعداد المطلوبة الموضحة في [اعداد Commerce الخاص بالنمسا](emea-aut-fi-sample.md#set-up-commerce-for-austria).

## <a name="design-of-extensions"></a>تصميم الملحقات

تعتمد عينة تكامل خدمة التسجيل المالي للنمسا في [وظيفة التكامل المالي](fiscal-integration-for-retail-channel.md). لمزيد من المعلومات حول تصميم حل التكامل المالي، راجع [نظرة عامة على تصميم نموذج التكامل](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>تصميم ملحق Commerce Runtime

الغرض من الامتداد الذي يمثل موفر المستندات المالية هو إنشاء مستندات خاصة بالخدمة ومعالجة الاستجابات من خدمة التسجيل المالي.

ملحق CRT هو **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>معالج الطلب

هناك معالجان لطلب المستندات لموفري المستندات:

- **DocumentProviderEFRFiscalAUT** – يتم استخدام هذا المعالج لإنشاء مستندات مالية لخدمة التسجيل المالي.
- **DocumentProviderEFRNonFiscalAUT** – يتم استخدام هذا المعالج لإنشاء مستندات غير مالية لخدمة التسجيل المالي.

هذه المعالجات موروثة من واجهة **INamedRequestHandler**. طريقة **HandlerName** مسؤولة عن إرجاع اسم المعالج. يجب أن يتطابق اسم المعالج مع اسم موفر مستند الموصل المحدد في مقر Commerce الرئيسي.

يدعم الموصل الطلبات التالية:

- **GetFiscalDocumentDocumentProviderRequest** – يحتوي هذا الطلب على معلومات حول المستند الذي يجب إنشاؤه. تقوم بإرجاع مستند خاص بالخدمة يجب تسجيله في خدمة التسجيل المالي.
- **GetNonFiscalDocumentDocumentProviderRequest** – يحتوي هذا الطلب على معلومات حول المستند غير المالي الذي يجب إنشاؤه. تقوم بإرجاع مستند خاص بالخدمة يجب تسجيله في خدمة التسجيل المالي.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – يعيد هذا الطلب قائمة الأحداث للاشتراك فيها. حاليًا، يتم دعم الأحداث التالية: المبيعات، وطباعة تقرير X، وطباعة تقرير Z، وإيداعات حساب العميل، وإيداعات أوامر العملاء، وأحداث التدقيق، والمعاملات غير المتعلقة بالمبيعات.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – يقوم هذا الطلب بإرجاع الاستجابة من خدمة التسجيل المالي. يتم اجراء تسلسل لهذه الاستجابة لتكوين سلسله بحيث تكون جاهزه ليتم حفظها.

#### <a name="configuration"></a>تكوين

ملفات التكوين موجودة في مجلد **التكوين** لمشروع الملحق:

- **DocumentProviderFiscalEFRSampleAustria** – للمستندات المالية.
- **DocumentProviderNonFiscalEFRSampleAustria** – للمستندات غير المالية.

الغرض من هذه الملفات هو تمكين إعدادات موفر المستندات ليتم تكوينها من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي. تمت إضافة الإعداد التالي:

- تعيين معدلات ضريبة القيمة المضافة

### <a name="hardware-station-extension-design"></a>تصميم ملحقات محطة الأجهزة

الغرض من ملحق الموصل المالي هو الاتصال بخدمة التسجيل المالي. ملحق محطة الأجهزة يُسمى **HardwareStation.Extension.EFRSample**. يستخدم بروتوكول HTTP أو HTTPS لإرسال المستندات التي ينشئها ملحق CRT لخدمة التسجيل المالية. كما أنه يتعامل مع الاستجابات التي يتم تلقيها من خدمة التسجيل المالي.

#### <a name="request-handler"></a>معالج الطلب

معالج طلب **EFRHandler** هو نقطة الإدخال لمعالجة الطلبات إلى خدمة التسجيل المالي.

المعالج موروث من واجهة **INamedRequestHandler**. طريقة **HandlerName** مسؤولة عن إرجاع اسم المعالج. يجب أن يتطابق اسم المعالج مع اسم الموصل المالي المحدد في مقر Commerce الرئيسي.

يدعم الموصل الطلبات التالية:

- **SubmitDocumentFiscalDeviceRequest** – يرسل هذا الطلب المستندات إلى خدمة التسجيل المالي ويعيد ردًا منها.
- **IsReadyFiscalDeviceRequest** – يُستخدم هذا الطلب لإجراء فحص سلامة لخدمة التسجيل المالي.
- **InitializeFiscalDeviceRequest** – يستخدم هذا الطلب لتهيئة خدمة التسجيل المالي.

#### <a name="configuration"></a>تكوين

ملف التكوين موجود في مجلد **التكوين** لمشروع الملحق. الغرض من الملف هو تمكين إعدادات الرابط المالي ليتم تكوينه من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي. تمت إضافة الإعدادات التالية:

- **عنوان نقطة النهاية** – عنوان URL الخاص بخدمه التسجيل المالية.
- **المهلة** – مقدار الوقت بالمللي ثانية الذي سينتظره برنامج التشغيل للحصول على استجابة من خدمة التسجيل المالي.

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
