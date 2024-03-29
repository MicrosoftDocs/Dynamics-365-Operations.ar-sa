---
title: إرشادات النشر لعينة تكامل الطابعة المالية لبولندا (قديمة)
description: يوفر هذا المقال إرشادات لنشر نموذج التكامل الطابعة المالية لبولندا من مجموعة تطوير برامج Microsoft Dynamics 365 Commerce ‏Retail ‏(SDK).
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: b19c8d7a80ac772ae238191d1285a1ad80e6f611
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473948"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>إرشادات النشر لعينة تكامل الطابعة المالية لبولندا (قديمة)

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> يجب عليك اتباع الإرشادات الموجودة في هذه المقالة فقط إذا كنت تستخدم Microsoft Dynamics 365 Commerce الإصدار 10.0.28 أو إصدارا سابقا. اعتبارا من الإصدار التجاري ال10.0.29 ، يتوفر نموذج تكامل الطابعة المالية لبولندا في مجموعه تطوير برامج التجارة (SDK). لمزيد من المعلومات، راجع [تكوين مكونات القناة‬](./emea-pol-fpi-sample.md#configure-channel-components).

توفر هذه المقالة إرشادات لنشر نموذج تكامل الطابعة المالي لبولندا من Dynamics 365 Commerce Retail SDK على جهاز ظاهري للمطور (VM) بتنسيق Microsoft Dynamics Lifecycle Services (LCS). لمزيد من المعلومات حول نموذج التكامل المالي هذا، راجع [عينة تكامل الطابعة المالية لبولندا](emea-pol-fpi-sample.md). 

تعد عينة التكامل المالي لبولندا جزءًا من Retail SDK. للحصول على مزيد من المعلومات حول كيفية تثبيت واستخدام SDK، راجع [بنية مجموعة تطوير برنامج Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). يتكون هذا النموذج من ملحقات Commerce Runtime (CRT) ومحطة الأجهزة. لتشغيل هذا النموذج، يجب تعديل مشاريع CRT ومشاريع محطة الأجهزة وإنشائها. نوصي باستخدام Retail SDK غير معدل لإجراء التغييرات الموضحة في هذا المقال. نوصي أيضًا باستخدام نظام تحكم بالمصادر مثل Azure DevOps حيث لم يتم تغيير أي ملفات حتى الآن.

## <a name="development-environment"></a>بيئة التطوير

اتبع هذه الخطوات لإعداد بيئة تطوير بحيث يمكنك اختبار العينة وتوسيعها.

### <a name="commerce-runtime-extension-components"></a>مكونات ملحق Commerce Runtime

تم تضمين مكونات ملحق CRT في Retail SDK. لإكمال الإجراءات التالية، افتح حل **CommerceRuntimeSamples.sln** ضمن **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. ابحث عن مشروع **Runtime.Extensions.DocumentProvider.PosnetSample**، وقم بإنشائه.
2. في مجلد **Extensions.DocumentProvider.PosnetSample\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll**.
3. انسخ ملف التجميع إلى مجلد ملحق CRT:

    - **Commerce Scale Unit:** انسخ الملف إلى مجلد **\\bin\\ext** ضمن موقع Commerce Scale Unit لخدمات معلومات الإنترنت (IIS).
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ الملف إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **Commerce Scale Unit:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهو موجود في مجلد **bin\\ext** ضمن موقع Commerce Scale Unit لخدمات معلومات الإنترنت (IIS).‬
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. أعد تشغيل خدمة Commerce:

    - **Commerce Scale Unit:** أعد تشغيل موقع خدمة Commerce من مدير IIS.
    - **وسيط العميل:** قم بإنهاء عملية **dllhost.exe** في أداره المهام، ثم قم باعاده تشغيل Modern POS.

### <a name="hardware-station-extension-components"></a>مكونات ملحقات محطة الأجهزة

تم تضمين مكونات ملحق محطة الأجهزة في Retail SDK. لإكمال الإجراءات التالية، افتح حل **HardwareStationSamples.sln** ضمن **RetailSdk\\SampleExtensions\\HardwareStation**.

1. ابحث عن مشروع **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**، وقم بإنشائه.
2. في مجلد **Extension.Posnet.ThermalFVFiscalPrinterSample\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll**.
3. نسخ ملف التجميع إلى جهاز محطه الاجهزه الموزعة:

    - **محطة الأجهزة البعيدة** انسخ الملف إلى مجلد **الحاوية** ضمن موقع محطة أجهزة IIS. انسخ مكتبات برنامج تشغيل الطابعة (**libposcmbth.dll**، و **libcmbth\_serial.dll**، و **cmbth\_pl.lng**).

4. ابحث عن ملف تكوين لملحقات محطة الأجهزة. تمت تسمية الملف باسم **HardwareStation.Extension.config**:

    - **محطة الأجهزة البعيدة:** الملف موجود ضمن مكان موقع محطة أجهزة IIS.

5. أضف السطر التالي إلى قسم **التأليف** في ملف التكوين.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. قم باعاده تشغيل خدمه محطه الاجهزه:

    - **محطه الاجهزه البعيدة:** أعد تشغيل موقع محطه الاجهزه من مدير IIS.

## <a name="production-environment"></a>بيئة الإنتاج

في الإجراء السابق، قمت بتمكين الامتدادات التي تشكل مكونات نموذج تكامل خدمة التسجيل المالي. بالإضافة إلى ذلك، يجب اتباع هذه الخطوات لإنشاء حزم قابلة للنشر تحتوي على مكونات التجارة، ولتطبيق هذه الحزم في بيئة إنتاج.

1. قم بإجراء التغييرات التالية في ملفات تكوين الحزمة ضمن مجلد **RetailSdk\\Assets**:

    - في ملفات تكوين **commerceruntime.ext.config** و **CommerceRuntime.MPOSOffline.Ext.config**، أضف السطر التالي إلى قسم **التأليف**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - في ملف تكوين **HardwareStation.Extension.config**، أضف السطر التالي إلى قسم **التأليف**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. قم بإجراء التغييرات التالية في ملف تكوين تخصيص حزمة **Customization.settings** ضمن مجلد **BuildTools**:

    - أضف السطر التالي لتضمين ملحق CRT في الحزم القابلة للنشر.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - أضف السطر التالي لتضمين ملحق محطة الأجهزة في الحزم القابلة للنشر.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. أبدا تشغيل موجه الأوامر MSBuild للحصول على أداة Visual Studio المساعدة، وقم بتشغيل **msbuild** ضمن مجلد Retail SDK لإنشاء الحزم القابلة للنشر.
1. قم بتطبيق الحزم من خلال LCS أو يدويًا. لمزيد من المعلومات، راجع [إنشاء الحزم القابلة للنشر](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>تصميم الملحقات

تعتمد عينة تكامل الطابعة المالية لبولندا في [وظيفة التكامل المالي](fiscal-integration-for-retail-channel.md). لمزيد من المعلومات حول تصميم حل التكامل المالي، راجع [نظرة عامة على تصميم نموذج التكامل](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>تصميم ملحق Commerce Runtime

الغرض من الملحق الذي يمثل موفر المستندات المالية هو إنشاء مستندات خاصة بالطابعة والتعامل مع الاستجابات من الطابعة المالية.

ملحق CRT هو **Runtime.Extensions.DocumentProvider.PosnetSample**. ينشئ هذا الملحق مجموعة من الأوامر الخاصة بالطابعة بتنسيق JavaScript Object Notation (JSON) التي تم تحديدها بواسطة مواصفة POSNET رقم 19-3678.

لمزيد من المعلومات حول تصميم حل التكامل المالي، راجع [عينات عملية التسجيل المالي التكامل المالي للأجهزة والخدمات المالية](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>معالج الطلب

إن معالج طلب **DocumentProviderPosnetProtocol** هو نقطه الإدخال الخاصة بالطلب لإنشاء مستندات من الطابعة المالية.

المعالج موروث من واجهة **INamedRequestHandler**. طريقة **HandlerName** مسؤولة عن إرجاع اسم المعالج. يجب أن يتطابق اسم المعالج مع اسم موفر مستند الموصل المحدد في مقر Commerce الرئيسي.

يدعم الموصل الطلبات التالية:

- **GetFiscalDocumentDocumentProviderRequest** – يحتوي هذا الطلب على معلومات حول المستند الذي يجب إنشاؤه. تقوم بإرجاع مستند خاص بالطابعة يجب تسجيله في الطابعة المالية.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – يعيد هذا الطلب قائمة الأحداث للاشتراك فيها. حاليًا، يتم دعم الأحداث التالية: المبيعات وطباعة تقرير X وطباعة تقرير Z.

#### <a name="configuration"></a>تكوين

ملف التكوين موجود في مجلد **التكوين** لمشروع الملحق. الغرض من الملف هو تمكين إعدادات موفر المستندات ليتم تكوينها من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي. تمت إضافة الإعدادات التالية:

- تعيين معدلات ضريبة القيمة المضافة
- تعيين نوع طريقة الدفع
- نوع دفع الإيداع

### <a name="hardware-station-extension-design"></a>تصميم ملحقات محطة الأجهزة

الغرض من الملحق الذي يمثل رابطًا ماليًا هو الاتصال بالطابعة المالية.

ملحق محطة الأجهزة هو **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**. يستدعي هذا الملحق وظائف برنامج تشغيل POSNET لإرسال الأوامر التي ينشئها ملحق CRT للطابعة المالية. كما يعالج أخطاء الجهاز.

#### <a name="request-handler"></a>معالج الطلب

معالج الطلب **FiscalPrinterHandler** هو نقطة الإدخال لمعالجة الطلب للجهاز المالي الطرفي.

المعالج موروث من واجهة **INamedRequestHandler**. طريقة **HandlerName** مسؤولة عن إرجاع اسم المعالج. يجب أن يتطابق اسم المعالج مع اسم الموصل المالي المحدد في مقر Commerce الرئيسي.

يدعم الموصل الطلبات التالية:

- **SubmitDocumentFiscalDeviceRequest** – يرسل هذا الطلب المستندات إلى الطابعات ويعيد الاستجابة من الطابعة المالية.
- **IsReadyFiscalDeviceRequest** – يستخدم هذا الطلب لإجراء فحص سلامة الجهاز.
- **InitializeFiscalDeviceRequest** – يستخدم هذا الطلب لتهيئة الطابعة.

#### <a name="configuration"></a>تكوين

ملف التكوين موجود في مجلد **التكوين** لمشروع الملحق. الغرض من الملف هو تمكين إعدادات الموصل ليتم تكوينه من مقر Commerce الرئيسي. يتوافق تنسيق الملف مع متطلبات تكوين التكامل المالي. تمت إضافة الإعدادات التالية:

- **سلسله الاتصال** – سلسله تصف تفاصيل الاتصال بالجهاز بأحد التنسيقات التي يدعمها برنامج التشغيل. لمزيد من المعلومات، راجع وثائق برنامج تشغيل POSNET.
- **مزامنة التاريخ والوقت** - قيمه تحدد ما إذا كان يجب مزامنة تاريخ الطابعة ووقتها مع محطه الاجهزه المتصلة.
- **مهلة الجهاز** – مقدار الوقت، بالمللي ثانية، الذي سينتظر فيه برنامج التشغيل استجابة من الجهاز. لمزيد من المعلومات، راجع وثائق برنامج تشغيل POSNET.
