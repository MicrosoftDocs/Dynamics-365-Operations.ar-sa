---
title: إرشادات النشر لعينة تكامل خدمة التسجيل المالي لجمهورية التشيك (قديمة)
description: يوفر هذا الموضوع إرشادات لنشر نموذج التكامل المالي لجمهورية التشيك من مجموعة تطوير برامج Microsoft Dynamics 365 Commerce ‏Retail ‏(SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: adafde2123afdc793a6ef4edf8fa16b857c55bf8
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076926"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-the-czech-republic-legacy"></a>إرشادات النشر لعينة تكامل خدمة التسجيل المالي لجمهورية التشيك (قديمة)

[!include [banner](../includes/banner.md)]

يوفر هذا الموضوع إرشادات لنشر نموذج تكامل خدمة التسجيل المالي لجمهورية التشيك من مجموعة تطوير برنامج Microsoft Dynamics 365 Commerce ‏(SDK) على جهاز ظاهري للمطور (VM) في Microsoft Dynamics Lifecycle Services ‏(LCS). لمزيد من المعلومات حول نموذج التكامل المالي هذا، راجع [عينة تكامل خدمة التسجيل المالي لجمهورية التشيك](emea-cze-fi-sample.md). 

تعد عينة التكامل المالي لجمهورية التشيك جزءًا من Retail SDK. للحصول على مزيد من المعلومات حول كيفية تثبيت واستخدام SDK، راجع [بنية مجموعة تطوير برنامج Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). يتكون هذا النموذج من ملحقات Commerce Runtime (CRT) ومحطة الأجهزة. لتشغيل هذا النموذج، يجب تعديل مشاريع CRT ومشاريع محطة الأجهزة وإنشائها. نوصي باستخدام Retail SDK غير معدل لإجراء التغييرات الموضحة في هذا الموضوع. نوصي أيضًا باستخدام نظام تحكم بالمصادر مثل Azure DevOps حيث لم يتم تغيير أي ملفات حتى الآن.

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
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
    ```

### <a name="enable-hardware-station-extensions"></a>تمكين ملحقات محطة الأجهزة

يتم تضمين مكونات توسيع محطة الأجهزة في عينات محطة الأجهزة. لإكمال الإجراءات التالية، افتح حل **HardwareStationSamples.sln** ضمن **RetailSdk\\SampleExtensions\\HardwareStation**.

#### <a name="efrsample-component"></a>مكون EFRSample

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

### <a name="production-environment"></a>بيئة الإنتاج

يتيح الإجراء السابق الملحقات التي تشكل مكونات عينة تكامل خدمة التسجيل المالي. بالإضافة إلى ذلك، يجب اتباع هذه الخطوات لإنشاء حزم قابلة للنشر تحتوي على مكونات التجارة، ولتطبيق هذه الحزم في بيئة إنتاج.

1. قم بإجراء التغييرات التالية في ملفات تكوين الحزمة ضمن مجلد **RetailSdk\\Assets**.

    - في ملفات تكوين **commerceruntime.ext.config** و **CommerceRuntime.MPOSOffline.Ext.config**، أضف الأسطر التالية إلى قسم **التأليف**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
        ```

    - في ملف تكوين **HardwareStation.Extension.config**، أضف السطر التالي إلى قسم **التأليف**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

2. قم بإجراء التغييرات التالية في ملف تكوين تخصيص حزمة **Customization.settings** ضمن مجلد **BuildTools**.

    - أضف الأسطر التالية لتضمين ملحقات CRT في الحزم القابلة للنشر.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - أضف السطر التالي لتضمين ملحق محطة الأجهزة في الحزم القابلة للنشر.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. أبدا تشغيل موجه الأوامر MSBuild للحصول على أداة Visual Studio المساعدة، وقم بتشغيل **msbuild** ضمن مجلد Retail SDK لإنشاء الحزم القابلة للنشر.
4. قم بتطبيق الحزم من خلال LCS أو يدويًا. لمزيد من المعلومات، راجع [إنشاء الحزم القابلة للنشر](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. أكمل كافة مهام الاعداد المطلوبة الموضحة في [اعداد Commerce الخاص بجمهورية التشيك](emea-cze-fi-sample.md#set-up-commerce-for-the-czech-republic).

## <a name="design-of-extensions"></a>تصميم الملحقات

تعتمد عينة تكامل خدمة التسجيل المالي لجمهورية التشيك في [وظيفة التكامل المالي](fiscal-integration-for-retail-channel.md). لمزيد من المعلومات حول تصميم حل التكامل المالي، راجع [نظرة عامة على تصميم نموذج التكامل](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>تصميم ملحق Commerce Runtime

الغرض من الامتداد الذي يمثل موفر المستندات المالية هو إنشاء مستندات خاصة بالخدمة ومعالجة الاستجابات من خدمة التسجيل المالي.

ملحق CRT هو **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>معالج الطلب

يوجد معالج طلب **DocumentProviderEFRFiscalCZE** واحد لموفر المستندات. وهي تستخدم لإنشاء المستندات المالية لخدمه التسجيل المالي.

هذا المعالج موروث من واجهة **INamedRequestHandler**. طريقة **HandlerName** مسؤولة عن إرجاع اسم المعالج. يجب أن يتطابق اسم المعالج مع اسم موفر مستند الموصل المحدد في مقر Commerce الرئيسي.

يدعم الموصل الطلبات التالية:

- **GetFiscalDocumentDocumentProviderRequest** – يحتوي هذا الطلب على معلومات حول المستند الذي يجب إنشاؤه. تقوم بإرجاع مستند خاص بالخدمة يجب تسجيله في خدمة التسجيل المالي.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – يعيد هذا الطلب قائمة الأحداث للاشتراك فيها. حاليًا، يتم دعم الأحداث التالية: المبيعات وإيداعات حساب العملاء وإيداعات أوامر العملاء.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – يقوم هذا الطلب بإرجاع الاستجابة من خدمة التسجيل المالي. يتم اجراء تسلسل لهذه الاستجابة لتكوين سلسله بحيث تكون جاهزه ليتم حفظها.

#### <a name="configuration"></a>تكوين

يوجد ملف تكوين **DocumentProviderFiscalEFRSampleCzech** في مجلد **التكوين** لمشروع الملحق. الغرض من هذا الملف هو تمكين إعدادات موفر المستندات ليتم تكوينها من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي. تمت إضافة الإعدادات التالية:

- تعيين معدلات ضريبة القيمة المضافة
- مجموعة ضريبة القيمة المضافة الافتراضية
- إيداع مجموعة ضريبة القيمة المضافة

### <a name="hardware-station-extension-design"></a>تصميم ملحقات محطة الأجهزة

الغرض من الامتداد الذي يعتبر رابطًا ماليًا هو الاتصال بخدمة التسجيل المالي.

ملحق محطة الأجهزة هو **HardwareStation.Extension.EFRSample**. يستخدم ملحق محطة الأجهزة بروتوكول HTTP لإرسال المستندات التي ينشئها ملحق CRT لخدمة التسجيل المالي. كما أنه يتعامل مع الاستجابات التي يتم تلقيها من خدمة التسجيل المالي.

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