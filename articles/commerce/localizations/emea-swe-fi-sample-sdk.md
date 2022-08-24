---
ms.openlocfilehash: a20971ac9a44c409363bbce6cd8b8343f16d800f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274195"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>إرشادات النشر لعينة تكامل وحدة التحكم في السويد (قديمة)
---

العنوان: إرشادات النشر لعينة تكامل وحدة التحكم في السويد (قديمة) [!include [banner](../includes/banner.md)]
الوصف: يوفر هذا المقال إرشادات لنشر نموذج تكامل وحدة التحكم للسويد من Retail SDK

المؤلف: EvgenyPopovMBS يوفر هذا المقال إرشادات لنشر نموذج تكامل وحدة التحكم للسويد من مجموعة أدوات تطوير برامج البيع بالتجزئة (SDK) على جهاز ظاهري للمطور (VM) في Microsoft Dynamics ‏Lifecycle Services ‏(LCS). لمزيد من المعلومات حول نموذج التكامل المالي هذا، راجع [عينة تكامل وحدة التحكم للسويد](emea-swe-fi-sample.md). التاريخ: 12/20/2021

العنوان: المقال، تعد عينة التكامل المالي للسويد جزءًا من Retail SDK. للحصول على مزيد من المعلومات حول كيفية تثبيت واستخدام SDK، راجع [بنية مجموعة تطوير برنامج Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). يتكون هذا النموذج من ملحقات Commerce Runtime (CRT)، محطة الأجهزة ونقطة البيع (POS). لتشغيل هذا النموذج، يجب تعديل مشاريع CRT ومحطة الأجهزة ونقاط البيع وإنشائها. نوصي باستخدام Retail SDK غير معدل لإجراء التغييرات الموضحة في هذا المقال. نوصي أيضًا باستخدام نظام تحكم بالمصادر مثل Azure DevOps حيث لم يتم تغيير أي ملفات حتى الآن.
الجمهور: مستخدم التطبيق ، المطور ، محترف تكنولوجيا المعلومات

المراجع: v-chgriffin
## <a name="development-environment"></a>بيئة التطوير
منطقه البحث: عالمية

المؤلف: josaw، اتبع هذه الخطوات لإعداد بيئة تطوير بحيث يمكنك اختبار العينة وتوسيعها.
البحث صالح من: 2019-03-01

### <a name="enable-crt-extensions"></a>تمكين ملحقات CRT
---


تم تضمين مكونات ملحق CRT في نماذج CRT. لإكمال الإجراءات التالية، افتح حل **CommerceRuntimeSamples.sln** ضمن **RetailSdk\\SampleExtensions\\CommerceRuntime**.
2. قم بتمكين ملحق محطة الأجهزة النموذجية الحالية عن طريق إضافة السطر التالي إلى قسم **التأليف** في ملف تكوين **HardwareStation.Extension.config**.


#### <a name="documentprovidercleancashsample-component"></a>مكون DocumentProvider.CleanCashSample
    ``` xml

    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
1. ابحث عن مشروع **Runtime.Extensions.DocumentProvider.CleanCashSample**، وقم بإنشائه.
    ```
2. In the **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** assembly file.

3. Copy the assembly file to the CRT extensions folder:
3. Make the following changes in the **Customization.settings** package customization configuration file under the **BuildTools** folder:


    - **Commerce Scale Unit:** Copy the file to the **\\bin\\ext** folder under the Internet Information Services (IIS) Commerce Scale Unit site location.
    - Remove the following line to exclude the earlier Hardware station extension from deployable packages.
    - **Local CRT on Modern POS:** Copy the file to the **\\ext** folder under the local CRT client broker location.


        ``` xml
4. Find the extension configuration file for CRT:
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />

        ```
    - **Commerce Scale Unit:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Commerce Scale Unit site location.

    - **Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.
    - Add the following lines to include the current sample Hardware station extension in deployable packages.


5. Register the CRT change in the extension configuration file.
        ``` xml

        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
    ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        ```
    ```


#### <a name="update-modern-pos"></a>تحديث نقطة البيع الحديثة
#### <a name="extension-configuration-file"></a>ملف تكوين الملحق


1. افتح حل **CloudPOS.sln** في **RetailSdk\\نقطة البيع**.
1. ابحث عن ملف تكوين الملحق لـ CRT:
2. تعطيل ملحق نقطة البيع السابقة:


    - **Commerce Scale Unit:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهو موجود في مجلد **bin\\ext** ضمن موقع Commerce Scale Unit لخدمات معلومات الإنترنت (IIS).‬
    - في ملف **tsconfig.json**، أضف مجلد **FiscalRegisterSample** إلى قائمة الاستبعاد.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.
    - قم بإزالة الأسطر التالية من ملف **extensions.json** ضمن مجلد **RetailSDK\\نقطة البيع\\الملحقات**.


2. قم بتسجيل تغيير CRT في ملف تكوين الملحق.
        ``` json

        {
    ``` xml
            "baseUrl": "FiscalRegisterSample"
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        }
    ```
        ```


### <a name="enable-hardware-station-extensions"></a>تمكين ملحقات محطة الأجهزة
3. قم بتمكين عينة محلق نقطة البيع الحالية عن طريق إضافة الأسطر التالية في ملف **extensions.json** ضمن مجلد **RetailSDK\\نقطة البيع\\الملحقات**.


يتم تضمين مكونات توسيع محطة الأجهزة في عينات محطة الأجهزة. لإكمال الإجراءات التالية، افتح حل **HardwareStationSamples.sln** ضمن **RetailSdk\\SampleExtensions\\HardwareStation**.
    ``` json

    {
#### <a name="cleancash-component"></a>مكون CleanCash
        "extensionPackages": [

            {
1. ابحث عن مشروع **HardwareStation.Extension.CleanCashSample**، وقم بإنشائه.
                "قيمة baseUrl": "Microsoft/AuditEvent.SE"
2. في مجلد **Extension.CleanCashSample\\الحاوية\\التصحيح**، ابحث عن ملفات التجميع **Contoso.Commerce.HardwareStation.CleanCashSample.dll** و **Interop.CleanCash\_1\_1.dll**.
            }
3. انسخ ملفات التجميع إلى مجلد ملحقات محطة الأجهزة:      ]

    }
    - **محطة الأجهزة المشتركة** انسخ الملفات إلى مجلد **الحاوية** ضمن موقع محطة أجهزة IIS.
    ```
    - **Dedicated hardware station on Modern POS:** Copy the files to the Modern POS client broker location.


#### Update Cloud POS
4. Find the extension configuration file for the Hardware station's extensions. The file is named **HardwareStation.Extension.config**.


1. Open the **ModernPOS.sln** solution under **RetailSdk\\POS**.
    - **Shared hardware station:** The file is under the IIS Hardware station site location.
2. Disable the earlier POS extension:
    - **Dedicated hardware station on Modern POS:** The file is under the Modern POS client broker location.


    - In the **tsconfig.json** file, add the **FiscalRegisterSample** folder to the exclude list.
5. Add the following line to the **composition** section of the configuration file.
    - Remove the following lines from the **extensions.json** file under the **RetailSDK\\POS\\Extensions** folder.


    ``` xml
        ``` json
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        {
    ```
            "baseUrl": "FiscalRegisterSample"

        }
### <a name="enable-modern-pos-extension-components"></a>تمكين مكونات ملحقات نقاط البيع الحديثة
        ```


1. افتح حل **ModernPOS.sln** ضمن **RetailSdk\\POS**، وتأكد من إمكانية تجميعه بدون أخطاء. بالإضافة إلى ذلك، تأكد من أنه يمكنك تشغيل نقطة البيع الحديثة Visual Studio باستخدام أمر **التشغيل**.
3. قم بتمكين عينة محلق نقطة البيع الحالية عن طريق إضافة الأسطر التالية في ملف **extensions.json** ضمن مجلد **RetailSDK\\نقطة البيع\\الملحقات**.


    > [!NOTE]
    ``` json
    > Modern POS must not be customized. You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.
    {

        "extensionPackages": [
2. Enable the extensions that must be loaded by adding the following lines in the **extensions.json** file.
            {

                "baseUrl": "Microsoft/AuditEvent.SE"
    ``` json
            }
    {
        ]
        "extensionPackages": [
    }
            {
    ```
                "baseUrl": "Microsoft/AuditEvent.SE"

            }
#### <a name="create-deployable-packages"></a>إنشاء حزم قابلة للنشر
        ]

    }
قم بتشغيل **msbuild** لحزمه البرامج النهائية للبيع بأكملها لإنشاء حزم قابله للنشر. قم بتطبيق الحزم من خلال LCS أو يدويًا. لمزيد من المعلومات، راجع [تعبئة Retail SDK](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
    ```

    > [!NOTE]
    > For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.

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
