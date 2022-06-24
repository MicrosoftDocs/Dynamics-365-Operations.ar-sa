---
title: إرشادات النشر لعينة تكامل وحدة التحكم في السويد (قديمة)
description: يوفر هذا المقال إرشادات لنشر نموذج تكامل وحدة التحكم للسويد من Retail SDK
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 05a49de43282c449c7b99072d8ac3ac4a5f2a67f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870537"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>إرشادات النشر لعينة تكامل وحدة التحكم في السويد (قديمة)

[!include [banner](../includes/banner.md)]

يوفر هذا المقال إرشادات لنشر نموذج تكامل وحدة التحكم للسويد من مجموعة أدوات تطوير برامج البيع بالتجزئة (SDK) على جهاز ظاهري للمطور (VM) في Microsoft Dynamics ‏Lifecycle Services ‏(LCS). لمزيد من المعلومات حول نموذج التكامل المالي هذا، راجع [عينة تكامل وحدة التحكم للسويد](emea-swe-fi-sample.md). 

تعد عينة التكامل المالي للسويد جزءًا من Retail SDK. للحصول على مزيد من المعلومات حول كيفية تثبيت واستخدام SDK، راجع [بنية مجموعة تطوير برنامج Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). يتكون هذا النموذج من ملحقات Commerce Runtime (CRT)، محطة الأجهزة ونقطة البيع (POS). لتشغيل هذا النموذج، يجب تعديل مشاريع CRT ومحطة الأجهزة ونقاط البيع وإنشائها. نوصي باستخدام Retail SDK غير معدل لإجراء التغييرات الموضحة في هذا المقال. نوصي أيضًا باستخدام نظام تحكم بالمصادر مثل Azure DevOps حيث لم يتم تغيير أي ملفات حتى الآن.

## <a name="development-environment"></a>بيئة التطوير

اتبع هذه الخطوات لإعداد بيئة تطوير بحيث يمكنك اختبار العينة وتوسيعها.

### <a name="enable-crt-extensions"></a>تمكين ملحقات CRT

تم تضمين مكونات ملحق CRT في نماذج CRT. لإكمال الإجراءات التالية، افتح حل **CommerceRuntimeSamples.sln** ضمن **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentprovidercleancashsample-component"></a>مكون DocumentProvider.CleanCashSample

1. ابحث عن مشروع **Runtime.Extensions.DocumentProvider.CleanCashSample**، وقم بإنشائه.
2. في مجلد **Runtime.Extensions.DocumentProvider.CleanCashSample\\الحاوية\\التصحيح**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **Commerce Scale Unit:** انسخ الملف إلى مجلد **\\bin\\ext** ضمن موقع Commerce Scale Unit لخدمات معلومات الإنترنت (IIS).
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ الملف إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **Commerce Scale Unit:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهو موجود في مجلد **bin\\ext** ضمن موقع Commerce Scale Unit لخدمات معلومات الإنترنت (IIS).‬
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    ```

#### <a name="extension-configuration-file"></a>ملف تكوين الملحق

1. ابحث عن ملف تكوين الملحق لـ CRT:

    - **Commerce Scale Unit:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهو موجود في مجلد **bin\\ext** ضمن موقع Commerce Scale Unit لخدمات معلومات الإنترنت (IIS).‬
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

2. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

### <a name="enable-hardware-station-extensions"></a>تمكين ملحقات محطة الأجهزة

يتم تضمين مكونات توسيع محطة الأجهزة في عينات محطة الأجهزة. لإكمال الإجراءات التالية، افتح حل **HardwareStationSamples.sln** ضمن **RetailSdk\\SampleExtensions\\HardwareStation**.

#### <a name="cleancash-component"></a>مكون CleanCash

1. ابحث عن مشروع **HardwareStation.Extension.CleanCashSample**، وقم بإنشائه.
2. في مجلد **Extension.CleanCashSample\\الحاوية\\التصحيح**، ابحث عن ملفات التجميع **Contoso.Commerce.HardwareStation.CleanCashSample.dll** و **Interop.CleanCash\_1\_1.dll**.
3. انسخ ملفات التجميع إلى مجلد ملحقات محطة الأجهزة:

    - **محطة الأجهزة المشتركة** انسخ الملفات إلى مجلد **الحاوية** ضمن موقع محطة أجهزة IIS.
    - **محطة الأجهزة المخصصة لنقاط البيع الحديثة:** انسخ الملفات إلى موقع وسيط عميل نقاط البيع الحديثة.

4. ابحث عن ملف تكوين الملحق لملحقات محطة الأجهزة. تمت تسمية الملف باسم **HardwareStation.Extension.config**.

    - **محطة الأجهزة المشتركة:** الملف موجود ضمن مكان موقع محطة أجهزة IIS.
    - **محطة الأجهزة المخصصة لنقاط البيع الحديثة:** الملف موجود ضمن موقع وسيط عميل نقاط البيع الحديثة.

5. أضف السطر التالي إلى قسم **التأليف** في ملف التكوين.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

### <a name="enable-modern-pos-extension-components"></a>تمكين مكونات ملحقات نقاط البيع الحديثة

1. افتح حل **ModernPOS.sln** ضمن **RetailSdk\\POS**، وتأكد من إمكانية تجميعه بدون أخطاء. بالإضافة إلى ذلك، تأكد من أنه يمكنك تشغيل نقطة البيع الحديثة Visual Studio باستخدام أمر **التشغيل**.

    > [!NOTE]
    > يجب عدم تخصيص نقطة البيع الحديثة. يجب عليك تمكين التحكم في حساب المستخدم (UAC)، ويجب عليك إلغاء تثبيت مثيلات نقطة البيع الحديثة المثبتة مسبقًا كما هو مطلوب.

2. قم بتمكين الملحقات التي يجب تحميلها عن طريق إضافة الأسطر التالية في ملف **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
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
2. قم بتمكين الملحقات التي يجب تحميلها عن طريق إضافة الأسطر التالية في ملف **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > لمزيد من المعلومات، وللحصول على نماذج توضح كيفية تضمين مجلدات التعليمات البرمجية المصدر وتمكين تحميل الامتدادات، راجع الإرشادات الموجودة في ملف readme.md في مشروع **Pos.Extensions**.

3. أعد إنشاء الحل.
4. قم بتشغيل الحل باستخدام أمر **التشغيل** واتباع الخطوات الموجودة في دليل Retail SDK.

## <a name="production-environment"></a>بيئة الإنتاج

يتيح الإجراء السابق الامتدادات التي تشكل مكونات عينة تكامل وحدة التحكم. بالإضافة إلى ذلك، يجب اتباع هذه الخطوات لإنشاء حزم قابلة للنشر تحتوي على مكونات التجارة، ولتطبيق هذه الحزم في بيئة إنتاج.

1. قم بإجراء التغييرات التالية في ملفات تكوين الحزمة ضمن مجلد **RetailSdk\\Assets**:

    - في ملفات تكوين **commerceruntime.ext.config** و **CommerceRuntime.MPOSOffline.Ext.config**، أضف الأسطر التالية إلى قسم **التأليف**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - في ملف تكوين **HardwareStation.Extension.config**، أضف السطر التالي إلى قسم **التأليف**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. قم بإجراء التغييرات التالية في ملف تكوين تخصيص حزمة **Customization.settings** ضمن مجلد **BuildTools**:

    - أضف السطر التالي لتضمين ملحقات CRT في الحزم القابلة للنشر.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - أضف الأسطر التالية لتضمين ملحق محطة الأجهزة في الحزم القابلة للنشر.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. قم بتمكين محلق نقطة البيع عن طريق إضافة الأسطر التالية في ملف **extensions.json** ضمن مجلد **RetailSDK\\نقطة البيع\\الملحقات**.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. أبدا تشغيل موجه الأوامر MSBuild للحصول على أداة Visual Studio المساعدة، وقم بتشغيل **msbuild** ضمن مجلد Retail SDK لإنشاء الحزم القابلة للنشر.
5. قم بتطبيق الحزم من خلال LCS أو يدويًا. لمزيد من المعلومات، راجع [إنشاء الحزم القابلة للنشر](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
6. أكمل جميع مهام الإعداد المطلوبة الموضحة في [إعداد التكامل باستخدام وحدات التحكم](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).

## <a name="design-of-the-extensions"></a>تصميم الملحقات

### <a name="crt-extension-design"></a>تصميم ملحق CRT

الغرض من الملحق الذي يمثل موفر المستندات المالية هو إنشاء مستندات خاصة بالخدمة والتعامل مع الاستجابات من وحدة التحكم.

ملحق CRT هو **Runtime.Extensions.DocumentProvider.CleanCashSample**.

لمزيد من المعلومات حول تصميم حل التكامل المالي، راجع [عينات عملية التسجيل المالي التكامل المالي للأجهزة والخدمات المالية](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>معالج الطلب

يوجد معالج طلب **DocumentProviderCleanCash** واحد لموفر المستندات. يتم استخدام هذا المعالج لإنشاء مستندات مالية لوحدة التحكم.

هذا المعالج موروث من واجهة **INamedRequestHandler**. طريقة **HandlerName** مسؤولة عن إرجاع اسم المعالج. يجب أن يتطابق اسم المعالج مع اسم موفر مستند الموصل المحدد في مقر Commerce الرئيسي.

يدعم الموصل الطلبات التالية:

- **GetFiscalDocumentDocumentProviderRequest** – يحتوي هذا الطلب على معلومات حول المستند الذي يجب إنشاؤه. تقوم بإرجاع مستند خاص بالخدمة يجب تسجيله في وحدة التحكم.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – يعيد هذا الطلب قائمة الأحداث للاشتراك فيها. حاليًا، يتم دعم أحداث المبيعات وأحداث التدقيق.

#### <a name="configuration"></a>تكوين

يوجد ملف تكوين **DocumentProviderFiscalCleanCashSample** في مجلد **التكوين** لمشروع الملحق. الغرض من هذا الملف هو تمكين إعدادات موفر المستندات ليتم تكوينها من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي. تمت إضافة الإعدادات التالية:

- تعيين أكواد ضريبة القيمة المضافة

### <a name="hardware-station-extension-design"></a>تصميم ملحقات محطة الأجهزة

الغرض من الملحق الذي يمثل رابطًا ماليًا هو الاتصال بوحدة التحكم.

ملحق محطة الأجهزة هو **HardwareStation.Extension.CleanCashSample**. يستخدم بروتوكول HTTP لإرسال المستندات التي ينشئها ملحق CRT لوحدة التحكم. كما أنه يتعامل مع الردود التي يتم تلقيها من وحدة التحكم.

#### <a name="request-handler"></a>معالج الطلب

معالج الطلب **CleanCashHandler** هو نقطة الإدخال لمعالجة الطلبات لوحدة التحكم.

المعالج موروث من واجهة **INamedRequestHandler**. طريقة **HandlerName** مسؤولة عن إرجاع اسم المعالج. يجب أن يتطابق اسم المعالج مع اسم الموصل المالي المحدد في مقر Commerce الرئيسي.

يدعم الموصل الطلبات التالية:

- **SubmitDocumentFiscalDeviceRequest** – يرسل هذا الطلب المستندات إلى وحدة التحكم ويعيد الرد منها.
- **IsReadyFiscalDeviceRequest** – يستخدم هذا الطلب لإجراء فحص سلامة لوحدة التحكم.
- **InitializeFiscalDeviceRequest** – يستخدم هذا الطلب لتهيئة وحدة التحكم.

#### <a name="configuration"></a>تكوين

ملف التكوين موجود في مجلد **التكوين** لمشروع الملحق. الغرض من الملف هو تمكين إعدادات الرابط المالي ليتم تكوينه من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي. تمت إضافة الإعدادات التالية:

- **سلسلة الاتصالات** – إعدادات اتصال وحدة التحكم.
- **المهلة** – مقدار الوقت، بالمللي ثانية، الذي سينتظر فيه برنامج التشغيل استجابة من وحدة التحكم.

## <a name="migrating-from-the-earlier-integration-sample"></a>الترحيل من نموذج التكامل السابق

إذا كنت تستخدم [نموذجًا سابقًا لتكامل نقاط البيع مع وحدات التحكم في السويد](retail-sdk-control-unit-sample.md)، قد تضطر إلى الترحيل منه إلى عينة التكامل الحالية. لاستيعاب التغيير وتلقي التحديثات في الوقت المناسب للميزات الخاصة بالسويد في المستقبل، قد تضطر إلى الترقية وإجراء تعديلات طفيفة على التعليمات البرمجية والتهيئة في الملحقات التي قمت بإنشائها وإعادة بناء الحلول الخاصة بك. لا يلزم إجراء تغييرات رئيسية في منطق الامتداد الذي قمت بإنشائه. ستستمر عينة التكامل السابقة والتخصيصات الخاصة بك في العمل إذا لم يتم إجراء تغييرات من جانبك. لذلك، يمكنك التخطيط والاستعداد والاستيعاب لبيئتك.

### <a name="migration-process"></a>عملية الترحيل

يجب أن يستند الترحيل من عينة التكامل السابقة إلى عينة تكامل وحدة التحكم الحالية على مفهوم التحديث التدريجي. بمعنى آخر، يجب تحديث جميع مكونات مقر Commerce الرئيسي وCommerce Scale Unit بالفعل قبل أن تبدأ في تحديث مكونات محطة الأجهزة ونقاط البيع.

للمساعدة في منع حدوث موقف يتم فيه توقيع حدث أو معاملة مرتين (أي أنه تم توقيعه بواسطة كل من الملحق السابق والملحق الحالي)، أو حيث لا يمكن توقيع حدث أو معاملة بسبب التكوين المفقود، نوصي بذلك تقوم بإيقاف تشغيل جميع أجهزة نقاط البيع وأجهزة محطة الأجهزة التي تستخدم النموذج السابق، ثم تقوم بتحديثها في وقت واحد. يمكن إجراء هذا التحديث المتزامن، على سبيل المثال، على أساس كل متجر على حدة عن طريق تحديث ملف تعريف وظائف المتجر وملف تعريف الأجهزة الخاص بمحطة الأجهزة.

يجب أن تتكون عملية الترحيل من الخطوات التالية.

1. تحديث مكونات مقر Commerce الرئيسي.
1. قم بتحديث مكونات Commerce Scale Unit، وقم بتمكين ملحقات النموذج الحالي.
1. تأكد من مزامنة جميع المعاملات التي تتم دون اتصال بالإنترنت من أجهزة MPOS الممكّنة في وضع عدم الاتصال.
1. قم بإيقاف تشغيل جميع الأجهزة التي تستخدم مكونات العينة السابقة.
1. أكمل جميع مهام الإعداد المطلوبة الموضحة في [إعداد التكامل باستخدام وحدات التحكم](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).
1. قم بتحديث مكونات نقاط البيع ومحطة الأجهزة، وقم بتعطيل الامتدادات التي تمثل أجزاء من العينة السابقة، وقم بتمكين امتدادات العينة الحالية.

    > [!NOTE]
    > اعتمادًا على نوع البيئة، يمكنك العثور على مزيد من التفاصيل الفنية حول عملية الترحيل إما في قسم [الترحيل في بيئة التطوير](#migration-in-a-development-environment) أو قسم [ الترحيل في بيئة الإنتاج](#migration-in-a-production-environment) في هذا المقال.

### <a name="migration-in-a-development-environment"></a>الترحيل في بيئة تطوير

#### <a name="update-crt"></a>تحديث CRT

1. ابحث عن مشروع **Runtime.Extensions.DocumentProvider.CleanCashSample**، وقم بإنشائه.
2. في مجلد **Runtime.Extensions.DocumentProvider.CleanCashSample\\الحاوية\\التصحيح**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **Commerce Scale Unit:** انسخ الملف إلى مجلد **\\bin\\ext** ضمن موقع Commerce Scale Unit لخدمات معلومات الإنترنت (IIS).
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ الملف إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **Commerce Scale Unit:** تمت تسمية الملف باسم **CommerceRuntime.ext.config**، وهو موجود في مجلد **bin\\ext** ضمن موقع Commerce Scale Unit لخدمات معلومات الإنترنت (IIS).‬
    - **CRT المحلي على نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود في مجلد **bin\\ext** ضمن موقع وسيط عميل CRT المحلي.

    > [!WARNING]
    > **لا** تقم بتحرير ملفات CommerceRuntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

5. ابحث عن ملحق CRT السابق وقم بإزالته من ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > لا تكمل هذه الخطوة حتى تقوم بتحديث جميع أجهزة نقاط البيع التي تعمل مع مثيل CRT هذا.

6. قم بتسجيل نموذج ملحقات CRT الحالية في ملف تكوين الملحق عن طريق إضافة الأسطر التالية.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>تحديث محطة الأجهزة

1. ابحث عن مشروع **HardwareStation.Extension.CleanCashSample**، وقم بإنشائه.
2. في مجلد **Extension.CleanCashSample\\الحاوية\\التصحيح**، ابحث عن ملفات التجميع **Contoso.Commerce.HardwareStation.CleanCashSample.dll** و **Interop.CleanCash\_1\_1.dll**.
3. انسخ ملفات التجميع إلى مجلد ملحقات محطة الأجهزة:

    - **محطة الأجهزة المشتركة** انسخ الملفات إلى مجلد **الحاوية** ضمن موقع محطة أجهزة IIS.
    - **محطة الأجهزة المخصصة لنقاط البيع الحديثة:** انسخ الملفات إلى موقع وسيط عميل نقاط البيع الحديثة.

4. ابحث عن ملف تكوين ملحق **HardwareStation.Extension.config**:

    - **محطة الأجهزة عن بُعد:** الملف موجود ضمن مكان موقع محطة أجهزة IIS.
    - **محطة الأجهزة المحلية على نقطة البيع الحديثة:** الملف موجود ضمن موقع وسيط عميل نقاط البيع الحديثة.

    > [!WARNING]
    > **لا** تقم بتحرير ملفات CommerceRuntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

5. ابحث عن ملحق محطة الأجهزة السابق وقم بإزالته من ملف تكوين الامتداد.

    # <a name="retail-73-and-earlier"></a>[الإصدار 7.3 من Retail والإصدارات السابقة](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[الإصدار 7.3.1 من Retail والإصدارات اللاحقة](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[الإصدار 10.0 من Retail والإصدارات اللاحقة](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. أضف السطر التالي إلى قسم **التأليف** في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>تحديث نقطة البيع الحديثة

1. افتح حل **CloudPOS.sln** ضمن **RetailSdk\\نقطة البيع**.
2. قم بتعطيل ملحق نقطة البيع السابق عن طريق إزالة الأسطر التالية من ملف **extensions.json**.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. قم بتمكين ملحق نموذج نقطة البيع الحالي بإضافة الأسطر التالية في ملف **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>تحديث نقطة بيع السحابة

1. افتح حل **ModernPOS.sln** ضمن **RetailSdk\\نقطة البيع**.
2. قم بتعطيل ملحق نقطة البيع السابق عن طريق إزالة الأسطر التالية من ملف **extensions.json**.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. قم بتمكين ملحق نموذج نقطة البيع الحالي بإضافة الأسطر التالية في ملف **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>الترحيل في بيئة إنتاج

#### <a name="update-crt"></a>تحديث CRT

1. قم بإزالة ملحق CRT السابق من ملفات التكوين **CommerceRuntime.ext.config** و **CommerceRuntime.MPOSOffline.Ext.config** ضمن مجلد **RetailSdk\\الأصول**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > لا تكمل هذه الخطوة حتى تقوم بتحديث جميع أجهزة نقاط البيع التي تعمل مع مثيل CRT هذا.

2. قم بتمكين نموذج ملحقات CRT الحالية عن طريق إجراء التغييرات التالية في ملفي التكوين **CommerceRuntime.ext.config** و **CommerceRuntime.MPOSOffline.Ext.config** ضمن مجلد **RetailSdk\\الأصول**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. في ملف تكوين تخصيص حزمة **Customization.settings** ضمن مجلد **BuildTools**، أضف السطر التالي لتضمين عينة ملحق CRT الحالية في الحزم القابلة للنشر.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>تحديث محطة الأجهزة

1. قم بإزالة ملحق محطة الأجهزة السابقة عن طريق تعديل ملف تكوين **HardwareStation.Extension.config**.

    # <a name="retail-73-and-earlier"></a>[الإصدار 7.3 من Retail والإصدارات السابقة](#tab/retail-7-3)

    قم بإزالة القسم التالي من ملفي التكوين **HardwareStation.Shared.config** و **HardwareStation.Dedicated.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[الإصدار 7.3.1 من Retail والإصدارات اللاحقة](#tab/retail-7-3-1)

    قم بإزالة القسم التالي من ملف التكوين **HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[الإصدار 10.0 من Retail والإصدارات اللاحقة](#tab/retail-10-0)

    قم بإزالة القسم التالي من ملف التكوين **HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

2. قم بتمكين ملحق محطة الأجهزة النموذجية الحالية عن طريق إضافة السطر التالي إلى قسم **التأليف** في ملف تكوين **HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

3. قم بإجراء التغييرات التالية في ملف تكوين تخصيص حزمة **Customization.settings** ضمن مجلد **BuildTools**:

    - قم بإزالة السطر التالي لاستبعاد ملحق محطة الأجهزة السابقة من الحزم القابلة للنشر.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />
        ```

    - أضف الأسطر التالية لتضمين نموذج ملحق محطة الأجهزة الحالي في الحزم القابلة للنشر.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

#### <a name="update-modern-pos"></a>تحديث نقطة البيع الحديثة

1. افتح حل **CloudPOS.sln** في **RetailSdk\\نقطة البيع**.
2. تعطيل ملحق نقطة البيع السابقة:

    - في ملف **tsconfig.json**، أضف مجلد **FiscalRegisterSample** إلى قائمة الاستبعاد.
    - قم بإزالة الأسطر التالية من ملف **extensions.json** ضمن مجلد **RetailSDK\\نقطة البيع\\الملحقات**.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. قم بتمكين عينة محلق نقطة البيع الحالية عن طريق إضافة الأسطر التالية في ملف **extensions.json** ضمن مجلد **RetailSDK\\نقطة البيع\\الملحقات**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>تحديث نقطة بيع السحابة

1. افتح حل **ModernPOS.sln** ضمن **RetailSdk\\نقطة البيع**.
2. تعطيل ملحق نقطة البيع السابقة:

    - في ملف **tsconfig.json**، أضف مجلد **FiscalRegisterSample** إلى قائمة الاستبعاد.
    - قم بإزالة الأسطر التالية من ملف **extensions.json** ضمن مجلد **RetailSDK\\نقطة البيع\\الملحقات**.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. قم بتمكين عينة محلق نقطة البيع الحالية عن طريق إضافة الأسطر التالية في ملف **extensions.json** ضمن مجلد **RetailSDK\\نقطة البيع\\الملحقات**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="create-deployable-packages"></a>إنشاء حزم قابلة للنشر

قم بتشغيل **msbuild** لحزمه البرامج النهائية للبيع بأكملها لإنشاء حزم قابله للنشر. قم بتطبيق الحزم من خلال LCS أو يدويًا. لمزيد من المعلومات، راجع [تعبئة Retail SDK](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
