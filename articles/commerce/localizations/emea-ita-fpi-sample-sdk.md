---
title: إرشادات النشر لعينة تكامل الطابعة المالية لإيطاليا (قديمة)
description: يوفر هذا المقال إرشادات لنشر نموذج التكامل الطابعة المالية لإيطاليا من مجموعة تطوير برامج Microsoft Dynamics 365 Commerce ‏Retail ‏(SDK).
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 46d42a2c2a5f8f40fc8b9693f26a182c8f2e6352
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336624"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>إرشادات النشر لعينة تكامل الطابعة المالية لإيطاليا (قديمة)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> يجب عليك اتباع الإرشادات الموجودة في هذه المقالة فقط إذا كنت تستخدم Microsoft Dynamics 365 Commerce الإصدار 10.0.28 أو إصدارا سابقا. اعتبارًا من الإصدار 10.0.29 من Commerce ، تتوفر عينة تكامل الطابعة المالية لإيطاليا في مجموعة تطوير برامج التجارة (SDK). لمزيد من المعلومات، راجع [تكوين مكونات القناة‬](./emea-ita-fpi-sample.md#configure-channel-components).

توفر هذه المقالة إرشادات لنشر نموذج تكامل الطابعة المالي لإيطاليا من Dynamics 365 Commerce Retail SDK على جهاز ظاهري للمطور (VM) بتنسيق Microsoft Dynamics خدمات دورة الحياة (LCS). لمزيد من المعلومات حول نموذج التكامل المالي هذا، راجع [عينة تكامل الطابعة المالية لإيطاليا](emea-ita-fpi-sample.md). 

تعد عينة التكامل المالي لإيطاليا جزءًا من Retail SDK. للحصول على مزيد من المعلومات حول كيفية تثبيت واستخدام SDK، راجع [بنية مجموعة تطوير برنامج Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). يتكون هذا النموذج من ملحقات Commerce Runtime (CRT) ومحطة الأجهزة. لتشغيل هذا النموذج، يجب تعديل مشاريع CRT ومشاريع محطة الأجهزة وإنشائها. نوصي باستخدام Retail SDK غير معدل لإجراء التغييرات الموضحة في هذا المقال. نوصي أيضًا باستخدام نظام تحكم بالمصادر مثل Azure DevOps حيث لم يتم تغيير أي ملفات حتى الآن.

## <a name="development-environment"></a>بيئة التطوير

اتبع هذه الخطوات لإعداد بيئة تطوير بحيث يمكنك اختبار العينة وتوسيعها.

### <a name="commerce-runtime-extension-components"></a>مكونات ملحق Commerce Runtime

تم تضمين مكونات ملحق CRT في Retail SDK. لإكمال الإجراءات التالية، افتح حل **CommerceRuntimeSamples.sln** ضمن **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. ابحث عن مشروع **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**، وقم بإنشائه.
2. في مجلد **Extensions.DocumentProvider.EpsonFP90IIISample\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **Commerce Scale Unit:** انسخ الملف إلى مجلد **\\bin\\ext** ضمن موقع Commerce Scale Unit لخدمات معلومات الإنترنت (IIS).
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ الملف إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **Commerce Scale Unit:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهو موجود في مجلد **bin\\ext** ضمن موقع Commerce Scale Unit لخدمات معلومات الإنترنت (IIS).‬
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. إعادة تشغيل Commerce Scale Unit:

    - **Commerce Scale Unit:** أعد تشغيل موقع Commerce Scale Unit من مدير IIS.
    - **وسيط العميل:** قم بإنهاء عملية **dllhost.exe** في أداره المهام، ثم قم باعاده تشغيل Modern POS.

### <a name="hardware-station-extension-components"></a>مكونات ملحقات محطة الأجهزة

تم تضمين مكونات ملحق محطة الأجهزة في Retail SDK. لإكمال الإجراءات التالية، افتح حل **HardwareStationSamples.sln** ضمن **RetailSdk\\SampleExtensions\\HardwareStation**.

1. ابحث عن مشروع **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample**، وقم بإنشائه.
2. في مجلد **Extensions.EpsonFP90IIIFiscalDeviceSample\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll**.
3. نسخ ملف التجميع إلى جهاز محطه الاجهزه الموزعة:

    - **محطة الأجهزة البعيدة** انسخ الملف إلى مجلد **الحاوية** ضمن موقع محطة أجهزة IIS.
    - **محطة الأجهزة المحلية:** انسخ الملف إلى موقع وسيط عميل Modern POS.

4. ابحث عن ملف تكوين لملحقات محطة الأجهزة. تمت تسمية الملف باسم **HardwareStation.Extension.config**:

    - **محطة الأجهزة البعيدة:** الملف موجود ضمن مكان موقع محطة أجهزة IIS.
    - **محطة الأجهزة المحلية:** الملف موجود ضمن موقع وسيط عميل Modern POS.

5. أضف القسم التالي إلى قسم **التأليف** في ملف التكوين.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. قم باعاده تشغيل خدمه محطه الاجهزه:

    - **محطه الاجهزه البعيدة:** أعد تشغيل موقع محطه الاجهزه من مدير IIS.
    - **محطة الأجهزة المحلية:** قم بإنهاء عملية **dllhost.exe** في أداره المهام، ثم قم باعاده تشغيل Modern POS.

## <a name="production-environment"></a>بيئة الإنتاج

لإنشاء حزم قابلة للنشر تحتوي على مكونات Commerce، وطبق هذه الحزم في بيئة إنتاج، اتبع هذه الخطوات.

1. أكمل الخطوات الموضحة في [قسم بيئة التطوير](#development-environment) المذكور سابقا في هذا المقال.
2. قم بإجراء التغييرات التالية في ملفات تكوين الحزمة ضمن مجلد **RetailSdk\\Assets**:

    1. في ملفات تكوين **commerceruntime.ext.config** و **CommerceRuntime.MPOSOffline.Ext.config**، أضف السطر التالي إلى قسم **التأليف**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    1. في ملف تكوين **HardwareStation.Extension.config**، أضف السطر التالي إلى قسم **التأليف**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. قم بإجراء التغييرات التالية في ملف تكوين تخصيص حزمة **Customization.settings** ضمن مجلد **BuildTools**:

    1. أضف السطر التالي لتضمين ملحق CRT في الحزم القابلة للنشر.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    1. أضف السطر التالي لتضمين ملحق محطة الأجهزة في الحزم القابلة للنشر.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. قم بإجراء التغييرات في ملف **Sdk.ModernPos.Shared.csproj** ضمن مجلد **الحزم\_SharedPackagingProjectComponents** لتضمين ملفات الموارد لإيطاليا في حزم قابلة للنشر:

    1. أضف قسم **ItemGroup** الذي يحتوي على العقد التي تشير إلى ملفات الموارد للترجمات المطلوبة. تأكد من تحديد مساحات الأسماء ونماذج الأسماء الصحيحة. يضيف المثال التالي عقد الموارد للغتين المحليتين **it** و **it-CH**.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. في قسم **Target Name="CopyPackageFiles"**، أضف سطرًا واحدًا لكل لغة، كما هو موضح في المثال التالي.

        ```xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it-CH" SkipUnchangedFiles="true" />
        ```

5. قم بإجراء التغييرات في ملف **Sdk.RetailServerSetup.proj** ضمن مجلد **الحزم\_SharedPackagingProjectComponents** لتضمين ملفات الموارد لإيطاليا في حزم قابلة للنشر:

    1. أضف قسم **ItemGroup** الذي يحتوي على العقد التي تشير إلى ملفات الموارد للترجمات المطلوبة. تأكد من تحديد مساحات الأسماء ونماذج الأسماء الصحيحة. يضيف المثال التالي عقد الموارد للغتين المحليتين **it** و **it-CH**.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. في قسم **Target Name="CopyPackageFiles"**، أضف سطرًا واحدًا لكل لغة، كما هو موضح في المثال التالي.

        ``` xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it-CH" SkipUnchangedFiles="true" />
        ```

6. أبدا تشغيل موجه الأوامر MSBuild للحصول على أداة Visual Studio المساعدة، ثم قم بتشغيل **msbuild** ضمن مجلد Retail SDK لإنشاء الحزم القابلة للنشر.
7. قم بتطبيق الحزم من خلال LCS أو يدويًا. لمزيد من المعلومات، راجع [إنشاء الحزم القابلة للنشر](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>تصميم الملحقات

### <a name="commerce-runtime-extension-design"></a>تصميم ملحق Commerce Runtime

الغرض من الملحق الذي يمثل موفر المستندات المالية هو إنشاء مستندات خاصة بالطابعة والتعامل مع الاستجابات من الطابعة المالية.

ملحق CRT هو **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**.

لمزيد من المعلومات حول تصميم حل التكامل المالي، راجع [عينات عملية التسجيل المالي التكامل المالي للأجهزة والخدمات المالية](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>معالج الطلب

إن معالج طلب **DocumentProviderEpsonFP90III** هو نقطه الإدخال الخاصة بالطلب لإنشاء مستندات من الطابعة المالية.

المعالج موروث من واجهة **INamedRequestHandler**. طريقة **HandlerName** مسؤولة عن إرجاع اسم المعالج. يجب أن يتطابق اسم المعالج مع اسم موفر مستند الموصل المحدد في مقر Commerce الرئيسي.

يدعم الموصل الطلبات التالية:

- **GetFiscalDocumentDocumentProviderRequest** – يحتوي هذا الطلب على معلومات حول المستند الذي يجب إنشاؤه. تقوم بإرجاع مستند خاص بالطابعة يجب تسجيله في الطابعة المالية.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – يعيد هذا الطلب قائمة الأحداث للاشتراك فيها. حاليًا، يتم دعم الأحداث التالية: المبيعات وطباعة تقرير X وطباعة تقرير Z.

#### <a name="configuration"></a>تكوين

ملف التكوين موجود في مجلد **التكوين** لمشروع الملحق. الغرض من الملف هو تمكين إعدادات موفر المستندات ليتم تكوينها من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي. تمت إضافة الإعدادات التالية:

- تعيين أكواد ضريبة القيمة المضافة
- تعيين معدلات ضريبة القيمة المضافة
- تعيين نوع طريقة الدفع
- نوع الكود الشريطي لرقم الإيصال
- نوع دفع الإيداع

### <a name="hardware-station-extension-design"></a>تصميم ملحقات محطة الأجهزة

الغرض من الملحق الذي يمثل رابطًا ماليًا هو الاتصال بالطابعة المالية.

ملحق محطة الأجهزة هو **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample**. يستخدم هذا الملحق بروتوكول HTTP لإرسال المستندات التي ينشئها ملحق CRT للطابعة المالية. كما أنه يتعامل مع الاستجابات التي يتم تلقيها من الطابعة المالية.

#### <a name="request-handler"></a>معالج الطلب

معالج طلب **EpsonFP90IIISample** هو نقطه الإدخال لمعالجه الطلبات للجهاز المالي الطرفي.

المعالج موروث من واجهة **INamedRequestHandler**. طريقة **HandlerName** مسؤولة عن إرجاع اسم المعالج. يجب أن يتطابق اسم المعالج مع اسم الموصل المالي المحدد في مقر Commerce الرئيسي.

يدعم الموصل الطلبات التالية:

- **SubmitDocumentFiscalDeviceRequest** – يرسل هذا الطلب المستندات إلى الطابعات ويعيد الاستجابة من الطابعة المالية.
- **IsReadyFiscalDeviceRequest** – يستخدم هذا الطلب لإجراء فحص سلامة الجهاز.
- **InitializeFiscalDeviceRequest** – يستخدم هذا الطلب لتهيئة الطابعة.

#### <a name="configuration"></a>تكوين

ملف التكوين موجود في مجلد **التكوين** لمشروع الملحق. الغرض من الملف هو تمكين إعدادات الموصل ليتم تكوينه من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي. تمت إضافة الإعدادات التالية:

- **عنوان نقطة النهاية** – عنوان URL الخاص بالطابعة.
- **مزامنة التاريخ والوقت** - قيمه تحدد ما إذا كان يجب مزامنة تاريخ الطابعة ووقتها مع محطه الاجهزه المتصلة.
