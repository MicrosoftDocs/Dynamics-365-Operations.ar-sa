---
title: إرشادات النشر لآلات تسجيل المدفوعات النقدية للنرويج (قديمة)
description: هذا المقال هو دليل النشر الذي يوضح كيفيه تمكين ترجمة Microsoft Dynamics 365 Commerce للنرويج.
author: EvgenyPopovMBS
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-2-28
ms.openlocfilehash: fb597add48ac3508a88142e63d80f405b6b5f8b4
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346035"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>إرشادات النشر لآلات تسجيل المدفوعات النقدية للنرويج (قديمة)

[!include [banner](../includes/banner.md)]

> [!WARNING]
> لا تستفيد وظيفة التكامل المالي النموذجية هذه من [إطار عمل التكامل المالي](./fiscal-integration-for-retail-channel.md) وسيتم إهماله في التحديثات اللاحقة. وينبغي عليك استخدام الوظيفة التي [تستند إلى اطار عمل](./emea-nor-fi-deployment.md) التكامل المالي بدلا من ذلك.

هذا المقال هو دليل النشر الذي يوضح كيفيه تمكين ترجمة Microsoft Dynamics 365 Commerce للنرويج. تتكون الترجمة من عده ملحقات من مكونات Commerce. على سبيل المثال، تتيح لك الملحقات طباعة الحقول المخصصة على الإيصالات وتسجيل أحداث تدقيق إضافية ومعاملات المبيعات ومعاملات الدفع في نقاط البيع (POS) وتوقيع معاملات المبيعات رقميًا وطباعة تقارير X وZ بالتنسيقات المحلية. لمزيد من المعلومات حول الترجمة الخاصة بالنرويج، راجع [وظيفة تسجيل النقد للنرويج](./emea-nor-cash-registers.md).

تعد هذه العينة جزءا من مجموعه تطوير برامج البيع بالتجزئة (SDK). للحصول على مزيد من المعلومات حول SDK، راجع [بنية مجموعة تطوير برنامج Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md).

يتكون هذا النموذج من ملحقات Commerce Runtime (CRT)، وخادم Retail، ونقطة البيع. لتشغيل هذا النموذج، يجب تعديل مشاريع CRT وخادم Retail ونقاط البيع وإنشائها. نوصي باستخدام Retail SDK غير معدل لإجراء التغييرات الموضحة في هذا المقال. نوصي أيضًا باستخدام نظام تحكم بالمصادر مثل Microsoft Visual Studio Online (VSO)، حيث لم يتم تغيير أي ملفات حتى الآن.

> [!NOTE]
> في Commerce 10.0.8 والإصدارات الأحدث، يُعرف خادم Retail باسم Commerce Scale Unit. نظرًا لأن هذا المقال ينطبق على إصدارات سابقة متعددة من التطبيق، يتم استخدام *خادم Retail* في جميع أنحاء المقال.
>
> تختلف بعض الخطوات في الإجراءات الموجودة في هذا المقال استنادا إلى إصدار Commerce الذي تستخدمه. لمزيد من المعلومات، راجع [ما هو الجديد أو المتغير في Dynamics 365 Retail](../get-started/whats-new.md).

### <a name="using-certificate-profiles-in-commerce-channels"></a>استخدام ملفات تعريف الشهادات في قنوات Commerce

في إصدار Commerce رقم 10.0.15 والإصدارات الأحدث، يمكنك استخدام ميزة [ملفات تعريف الشهادة المحددة من قِبل المستخدم لمتاجر البيع بالتجزئة](./certificate-profiles-for-retail-stores.md) التي تدعم تجاوز الفشل في وضع عدم الاتصال عندما لا يتوفر المخزن الرئيسي أو مقر Commerce الرئيسي. وتعمل هذه الميزة على توسيع ميزة [إدارة الأسرار لقنوات البيع بالتجزئة](../dev-itpro/manage-secrets.md)".

لتطبيق هذه الوظيفة في ملحق CRT، اتبع الخطوات التالية.

1. أنشئ مشروع ملحق CRT (نوع مشروع مكتبة فئة C#). استخدم نماذج القوالب من مجموعة أدوات تطوير برامج البيع بالتجزئة (SDK)‏ (RetailSDK\SampleExtensions\CommerceRuntime).

2. قم بإضافة معالج مخصص لـ CertificateSignatureServiceRequest في مشروع SequentialSignatureRegister.

3. لقراءة مكالمة سرية، `GetUserDefinedSecretCertificateServiceRequest` باستخدام مُنشئ مع معلمة profileId. سيبدأ ذلك وظيفة العمل مع الإعدادات من ملفات تعريف الشهادة. استنادًا إلى الإعدادات، سيتم استرداد الشهادة إما من Azure Key Vault أو تخزين الجهاز المحلي.

    ```csharp
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);

    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
    ```

4. عندما يتم استرداد الشهادة، تابع توقيع البيانات.

5. إنشاء مشروع ملحق CRT.

6. انسخ مكتبه فئة الإخراج والصقها في ..\RetailServer\webroot\bin\Ext للاختبار اليدوي.

7. في ملف CommerceRuntime.Ext.config، قم بتحديث قسم تكوين الملحق بمعلومات المكتبة المخصصة.

## <a name="development-environment"></a>بيئة التطوير

أكمل هذه الإجراءات لإعداد بيئة تطوير بحيث يمكنك اختبار العينة وتوسيعها.

### <a name="the-crt-extension-components"></a>مكونات ملحق CRT

تم تضمين مكونات ملحق CRT في نماذج CRT. لإكمال الإجراءات التالية، افتح حل CRT **CommerceRuntimeSamples.sln** ضمن **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="receiptsnorway-component"></a>مكون ReceiptsNorway

1. ابحث عن مشروع **Runtime.Extensions.ReceiptsNorway** وقم بإنشائه.
2. في مجلد **Extensions.ReceiptsNorway\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.ReceiptsNorway.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ Microsoft Internet Information Services (IIS).
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="salespaymenttransext-component"></a>مكون SalesPaymentTransExt

1. ابحث عن مشروع **Runtime.Extensions.SalesPaymentTransExt**، وقم بإنشائه.
2. في مجلد **Extensions.SalesPaymentTransExt\\bin\\Debug**، ابحث عن ملف تجميع **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="xzreportsnorway-component"></a>مكون XZReportsNorway

1. ابحث عن مشروع **Runtime.Extensions.XZReportsNorway**، وقم بإنشائه.
2. في مجلد **Extensions.XZReportsNorway\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.XZReportsNorway.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

# <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>مكون نموذج RegisterAuditEvent

1. ابحث عن مشروع **Runtime.Extensions.RegisterAuditEventSample**، وقم بإنشائه.
2. في مجلد **Extensions.RegisterAuditEventSample\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="salestransactionsignature-sample-component"></a>مكون نموذج SalesTransactionSignature

1. ابحث عن مشروع **Runtime.Extensions.SalesTransactionSignatureSample**.
2. قم بتعديل ملف **App.config** عن طريق تحديد بصمة الإبهام وموقع المتجر واسم المتجر للشهادة التي يجب استخدامها لتوقيع معاملات البيع.
3. أنشئ المشروع.
4. في مجلد **Extensions.SalesTransactionSignatureSample\\bin\\Debug**، ابحث عن الملفات التالية:

    - ملف التجميع **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - ملف التكوين **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. انسخ الملفات إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

6. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

7. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

# <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>مكون نموذج RegisterAuditEvent

1. ابحث عن مشروع **Runtime.Extensions.RegisterAuditEventSample**، وقم بإنشائه.
2. في مجلد **Extensions.RegisterAuditEventSample\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="salestransactionsignature-sample-component"></a>مكون نموذج SalesTransactionSignature

1. ابحث عن مشروع **Runtime.Extensions.SalesTransactionSignatureSample**.
2. قم بتعديل ملف **App.config** عن طريق تحديد بصمة الإبهام وموقع المتجر واسم المتجر للشهادة التي يجب استخدامها لتوقيع معاملات البيع.
3. أنشئ المشروع.
4. في مجلد **Extensions.SalesTransactionSignatureSample\\bin\\Debug**، ابحث عن الملفات التالية:

    - ملف التجميع **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - ملف التكوين **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. انسخ الملفات إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

6. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

7. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="salestransactionsignaturesamplemessages-component"></a>مكون SalesTransactionSignatureSample.Messages

1. ابحث عن مشروع **Runtime.Extensions.SalesTransactionSignatureSample.Messages** project.
2. في مجلد **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

# <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>مكون نموذج RegisterAuditEvent

1. ابحث عن مشروع **Runtime.Extensions.RegisterAuditEventSample**، وقم بإنشائه.
2. في مجلد **Extensions.RegisterAuditEventSample\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="salestransactionsignature-sample-component"></a>مكون نموذج SalesTransactionSignature

1. ابحث عن مشروع **Runtime.Extensions.SalesTransactionSignatureSample**.
2. قم بتعديل ملف **App.config** عن طريق تحديد بصمة الإبهام وموقع المتجر واسم المتجر للشهادة التي يجب استخدامها لتوقيع معاملات البيع.
3. أنشئ المشروع.
4. في مجلد **Extensions.SalesTransactionSignatureSample\\bin\\Debug**، ابحث عن الملفات التالية:

    - ملف التجميع **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - ملف التكوين **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. انسخ الملفات إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

6. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

7. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="sequentialsignatureregistercontracts-component"></a>مكون SequentialSignatureRegister.Contracts

1. ابحث عن مشروع **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. في مجلد **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

# <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>مكون نموذج RegisterAuditEvent

1. ابحث عن مشروع **Runtime.Extensions.RegisterAuditEventSample**، وقم بإنشائه.
2. في مجلد **Extensions.RegisterAuditEventSample\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="sequentialsignatureregister-component"></a>مكون SequentialSignatureRegister

1. ابحث عن مشروع **Runtime.Extensions.SequentialSignatureRegister**.
2. قم بتعديل ملف **App.config** عن طريق تحديد بصمة الإبهام وموقع المتجر واسم المتجر للشهادة التي يجب استخدامها لتوقيع معاملات البيع.
3. أنشئ المشروع.
4. في مجلد **Extensions.SequentialSignatureRegister\\bin\\Debug**، ابحث عن الملفات التالية:

    - ملف التجميع **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - ملف التكوين **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. انسخ الملفات إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

6. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

7. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="salestransactionsignaturenorway-component"></a>مكون SalesTransactionSignatureNorway

1. ابحث عن مشروع **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. في مجلد **Extensions.SalesTransactionSignatureNorway\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="sequentialsignatureregistercontracts-component"></a>مكون SequentialSignatureRegister.Contracts

1. ابحث عن مشروع **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. في مجلد **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

#### <a name="salespaymenttransextnorway-component"></a>مكون SalesPaymentTransExtNorway

1. ابحث عن مشروع **Runtime.Extensions.SalesPaymentTransExtNorway**، وقم بإنشائه.
2. في مجلد **Extensions.SalesPaymentTransExtNorway\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

# <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>مكون RegisterAuditEventNorway

1. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

2. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="sequentialsignatureregister-component"></a>مكون SequentialSignatureRegister

1. ابحث عن مشروع **Runtime.Extensions.SequentialSignatureRegister**.
2. قم بتعديل ملف **App.config** عن طريق تحديد بصمة الإبهام وموقع المتجر واسم المتجر للشهادة التي يجب استخدامها لتوقيع معاملات البيع.
3. أنشئ المشروع.
4. في مجلد **Extensions.SequentialSignatureRegister\\bin\\Debug**، ابحث عن الملفات التالية:

    - ملف التجميع **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - ملف التكوين **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. انسخ الملفات إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

6. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

7. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="salestransactionsignaturenorway-component"></a>مكون SalesTransactionSignatureNorway

1. ابحث عن مشروع **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. في مجلد **Extensions.SalesTransactionSignatureNorway\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="sequentialsignatureregistercontracts-component"></a>مكون SequentialSignatureRegister.Contracts

1. ابحث عن مشروع **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. في مجلد **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

#### <a name="salespaymenttransextnorway-component"></a>مكون SalesPaymentTransExtNorway

1. ابحث عن مشروع **Runtime.Extensions.SalesPaymentTransExtNorway**، وقم بإنشائه.
2. في مجلد **Extensions.SalesPaymentTransExtNorway\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

# <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>مكون RegisterAuditEventNorway

1. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

2. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="sequentialsignatureregister-component"></a>مكون SequentialSignatureRegister

1. ابحث عن مشروع **Runtime.Extensions.SequentialSignatureRegister**.
2. قم بتعديل ملف **App.config** عن طريق تحديد بصمة الإبهام وموقع المتجر واسم المتجر للشهادة التي يجب استخدامها لتوقيع معاملات البيع.
3. أنشئ المشروع.
4. في مجلد **Extensions.SequentialSignatureRegister\\bin\\Debug**، ابحث عن الملفات التالية:

    - ملف التجميع **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - ملف التكوين **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. انسخ الملفات إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

6. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

7. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="salestransactionsignaturenorway-component"></a>مكون SalesTransactionSignatureNorway

1. ابحث عن مشروع **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. في مجلد **Extensions.SalesTransactionSignatureNorway\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

#### <a name="sequentialsignatureregistercontracts-component"></a>مكون SequentialSignatureRegister.Contracts

1. ابحث عن مشروع **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. في مجلد **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

#### <a name="salespaymenttransextnorway-component"></a>مكون SalesPaymentTransExtNorway

1. ابحث عن مشروع **Runtime.Extensions.SalesPaymentTransExtNorway**، وقم بإنشائه.
2. في مجلد **Extensions.SalesPaymentTransExtNorway\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات CRT:

    - **خادم Retail:** انسخ التجميع إلى مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي على نقطة البيع الحديثة:** انسخ التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.

4. ابحث عن ملف تكوين الملحق لـ CRT:

    - **خادم Retail:** تمت تسمية الملف باسم **commerceruntime.ext.config**، وهي موجودة في مجلد **bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.
    - **CRT المحلي في نقطة البيع الحديثة:** تمت تسمية الملف باسم **CommerceRuntime.MPOSOffline.Ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

5. قم بتسجيل تغيير CRT في ملف تكوين الملحق.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **لاع** بتحرير ملفي commerceruntime.config وCommerceRuntime.MPOSOffline.config. هذه الملفات ليست مخصصة لأية تخصيصات.

---

### <a name="the-retail-server-extension-components"></a>مكونات ملحق خادم Retail

#### <a name="salestransactionsignature-retail-server-sample-component"></a>مكون نموذج خادم Retail لـ SalesTransactionSignature

1. في مجلد **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample**، ابحث عن **RetailServer.Extensions.SalesTransactionSignatureSample**، وقم بإنشائه.
2. في مجلد **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.RetailServer.SalesTransactionSignatureSample.dll**.
3. انسخ ملف التجميع إلى مجلد ملحقات خادم Retail.

    # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

    المجلد هو مجلد **\\bin** ضمن مكان موقع خادم Retail لـ IIS.

    # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

    المجلد هو مجلد **\\bin** ضمن مكان موقع خادم Retail لـ IIS.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    المجلد هو مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.

    # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

    المجلد هو مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.

    # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

    المجلد هو مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.

    # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

    المجلد هو مجلد **\\bin\\ext** ضمن مكان موقع خادم Retail لـ IIS.

    ---

4. ابحث عن ملف التكوين لخادم Retail. تمت تسمية الملف باسم **web.config**، وهو موجود ضمن مكان موقع خادم Retail لـ IIS.
5. قم بتسجيل ملحقات خادم Retail في قسم **extensionComposition** بملف التكوين.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. قم بتسجيل تبعيات ملحقات خادم Retail.

    # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4/)

    1. في مجلد **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**، ابحث عن الملفات التالية:

        - ملف التجميع **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
        - ملف التكوين **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

    2. انسخ الملفات إلى مجلد **\\bin** ضمن مكان موقع خادم Retail لـ IIS.
    3. قم بتسجيل تغيير CRT في ملف تكوين الملحق لـ CRT. تمت تسمية هذا الملف باسم **commerceruntime.ext.config**، وهو موجود في مجلد **bin** ضمن مكان موقع خادم Retail لـ IIS.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later/)

    1. في مجلد **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**.
    2. انسخ الملف إلى مجلد **\\bin** ضمن مكان موقع خادم Retail لـ IIS.
    3. قم بتسجيل تغيير CRT في ملف تكوين الملحق لـ CRT. تمت تسمية هذا الملف باسم **commerceruntime.ext.config**، وهو موجود في مجلد **bin** ضمن مكان موقع خادم Retail لـ IIS.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > لا يلزم اتخاذ أي إجراءات.

    # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

    > [!NOTE]
    > لا يلزم اتخاذ أي إجراءات.

    # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

    > [!NOTE]
    > لا يلزم اتخاذ أي إجراءات.

    # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

    > [!NOTE]
    > لا يلزم اتخاذ أي إجراءات.

    ---

### <a name="the-modern-pos-extension-components"></a>مكونات ملحقات نقاط البيع الحديثة

#### <a name="implement-the-proxy-code-for-offline-mode"></a>تنفيذ رمز الوكيل لوضع عدم الاتصال

هذا الجزء مكافئ لوحدة تحكم خادم البيع بالتجزئة، لكنه يمتد إلى CRT المحلي الذي يتم استخدامه عندما لا يكون العميل متصلاً.

1. في ملف **customization.settings**، قم بتغيير قسم **@(RetailServerLibraryPathForProxyGeneration)** بحيث يستخدم تجميع خادم Retail الجديد لإنشاء الوكيل.
2. نفذ طرق الواجهة التالية في فئة **StoreOperationsManager**. بالنسبة للتكرار الأول، أضف الكود التالي:

    # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > لا تنطبق هذه الخطوة على هذا الإصدار.

    # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

    > [!NOTE]
    > لا تنطبق هذه الخطوة على هذا الإصدار.

    # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

    > [!NOTE]
    > لا تنطبق هذه الخطوة على هذا الإصدار.

    # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

    > [!NOTE]
    > لا تنطبق هذه الخطوة على هذا الإصدار.

    ---

3. لإعادة إنشاء كود الوكيل، أنشئ مجلد **الوكلاء** من سطر الأوامر باستخدام أمر **msbuild /t:Rebuild**.
4. قم بحل تبعيات مشروع **Proxies.RetailProxy**:

    # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

    افتح **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**، وأضف مشروع **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** إلى الحل، واضف مرجع المشروع إلى مشروع **RetailProxy** للرجوع إلى **SalesTransactionSignatureSample**.

    # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

    افتح **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**، وأضف مشروع **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** إلى الحل، وأضف مرجع مشروع إلى مشروع **RetailProxy** للرجوع إلى **SalesTransactionSignatureSample.Messages**.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > لا تنطبق هذه الخطوة على هذا الإصدار.

    # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

    > [!NOTE]
    > لا تنطبق هذه الخطوة على هذا الإصدار.

    # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

    > [!NOTE]
    > لا تنطبق هذه الخطوة على هذا الإصدار.

    # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

    > [!NOTE]
    > لا تنطبق هذه الخطوة على هذا الإصدار.

    ---

5. قم بتعديل طرق الواجهة في فئة **StoreOperationsManager**:

    # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > لا تنطبق هذه الخطوة على هذا الإصدار.

    # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

    > [!NOTE]
    > لا تنطبق هذه الخطوة على هذا الإصدار.

    # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

    > [!NOTE]
    > لا تنطبق هذه الخطوة على هذا الإصدار.

    # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

    > [!NOTE]
    > لا تنطبق هذه الخطوة على هذا الإصدار.

    ---

6. قم بتحديث ملف **dllhost.exe.config** بحيث يقوم وسيط العميل بتحميل مجموعة RetailProxy الجديدة.

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>مكون ملحق وكيل Retail ‏(‏‏Retail 7.3.1 والإصدارات الأحدث)

أكمل الإجراء التالي فقط إذا كنت تستخدم Retail 7.3.1 والإصدارات الأحدث.

1. في مجلد **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample**، ابحث عن مشروع **RetailServer.Extensions.SalesTransactionSignatureSample** وقم بإنشائه.
2. في مجلد **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug**، ابحث عن ملف التجميع **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample**.
3. انسخ ملفات التجميع إلى مجلد **\\ext** ضمن موقع وسيط عميل CRT المحلي.
4. قم بتسجيل تغيير وكيل Retail في ملف تكوين الملحق. تمت تسمية الملف باسم **RetailProxy.MPOSOffline.ext.config**، وهو موجود ضمن موقع وسيط عميل CRT المحلي.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>مكونات ملحقات نقاط البيع الحديثة

1. افتح الحل في **RetailSdk\\POS\\ModernPOS.sln**، وتأكد من إمكانية تجميعه بدون أخطاء. بالإضافة إلى ذلك، تأكد من أنه يمكنك تشغيل نقطة البيع الحديثة من Microsoft Visual Studio باستخدام أمر **تشغيل**.

    > [!NOTE]
    > يجب عدم تخصيص نقطة البيع الحديثة. يجب عليك تمكين التحكم في حساب المستخدم (UAC)، ويجب عليك إلغاء تثبيت مثيلات نقطة البيع الحديثة المثبتة مسبقًا كما هو مطلوب.

2. قم بتضمين مجلدات التعليمات البرمجية المصدر الموجودة التالية في مشروع **Pos.Extensions**.

    # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. قم بتمكين الملحقات ليتم تحويلها في **tsconfig.json** عن طريق أزاله المجلدات التالية من قائمه الاستبعاد.

    # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. قم بتمكين الملحقات المراد تحميلها في **extensions.json** عن طريق إضافة الأسطر التالية في المكان المناسب.

    # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > لمزيد من المعلومات، وللحصول على نماذج توضح كيفية تضمين مجلدات التعليمات البرمجية المصدر وتمكين تحميل الامتدادات، راجع الإرشادات الموجودة في ملف readme.md في مشروع **Pos.Extensions**.

5. أعد إنشاء الحل.
6. قم بتشغيل Modern POS في مصحح الأخطاء، واختبر الوظيفة.

### <a name="cloud-pos-extension-components"></a>مكونات ملحقات نقطة بيع المجموعة

1. افتح الحل في **RetailSdk\\POS\\CloudPOS.sln**، وتأكد من إمكانية تجميعه بدون أخطاء.
2. قم بتضمين مجلدات التعليمات البرمجية المصدر الموجودة التالية في مشروع **Pos.Extensions**.

    # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. قم بتمكين الملحقات ليتم تحويلها في **tsconfig.json** عن طريق أزاله المجلدات التالية من قائمه الاستبعاد.

    # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. قم بتمكين الملحقات المراد تحميلها في **extensions.json** عن طريق إضافة الأسطر التالية في المكان المناسب.

    # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > لمزيد من المعلومات، وللحصول على نماذج توضح كيفية تضمين مجلدات التعليمات البرمجية المصدر وتمكين تحميل الامتدادات، راجع الإرشادات الموجودة في ملف readme.md في مشروع **Pos.Extensions**.

5. أعد إنشاء الحل.
6. قم بتشغيل الحل باستخدام أمر **التشغيل** واتباع الخطوات الموجودة في دليل Retail SDK.
7. اختبر الوظيفة.

### <a name="set-up-required-parameters-in-headquarters"></a>إعداد المعلمات المطلوبة في المقرات الرئيسية

للحصول على مزيد من المعلومات، راجع [وظيفة تسجيل النقد للنرويج](./emea-nor-cash-registers.md).

## <a name="production-environment"></a>بيئة الإنتاج

اتبع هذه الخطوات لإنشاء حزم قابلة للنشر تحتوي على مكونات Commerce، ولتطبيق هذه الحزم في بيئة إنتاج.

1. أكمل الخطوات الواردة في قسم [مكونات ملحقات نقطة بيع المجموعة](#cloud-pos-extension-components) أو [مكونات توسيع نقطة البيع الحديثة](#modern-pos-extension-components) سابقًا في هذا المقال.
2. قم بإجراء التغييرات التالية في ملفات تكوين الحزمة ضمن مجلد **RetailSdk\\Assets**:

    1. في ملفات تكوين **commerceruntime.ext.config** **CommerceRuntime.MPOSOffline.Ext.config** أضف الأسطر التالية إلى قسم **التأليف**:

        # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. تمكين تخصيص وكيل Commerce:

        # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

        في ملف تكوين **dllhost.exe.config** أضف الأسطر التالية إلى القسم الفرعي **appSettings** لقسم **التكوين**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

        في ملف تكوين **dllhost.exe.config** أضف الأسطر التالية إلى القسم الفرعي **appSettings** لقسم **التكوين**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        في ملف تكوين **RetailProxy.MPOSOffline.ext.config** أضف الأسطر التالية إلى قسم **التأليف**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

        في ملف تكوين **RetailProxy.MPOSOffline.ext.config** أضف الأسطر التالية إلى قسم **التأليف**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

        في ملف تكوين **RetailProxy.MPOSOffline.ext.config** أضف الأسطر التالية إلى قسم **التأليف**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

        في ملف تكوين **RetailProxy.MPOSOffline.ext.config** أضف الأسطر التالية إلى قسم **التأليف**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. قم بإجراء التغييرات التالية في ملف تكوين تخصيص حزمة **Customization.settings**.

    1. تمكين تخصيص وكيل Retail.

        # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

        أضف البنود التالية إلى قسم **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;**.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

        أضف البنود التالية إلى قسم **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;**.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        أضف الأسطر التالية إلى قسم **ItemGroup** لتضمين ملحق Retail في الحزم القابلة للنشر:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

        أضف الأسطر التالية إلى قسم **ItemGroup** لتضمين ملحق Retail في الحزم القابلة للنشر:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

        أضف الأسطر التالية إلى قسم **ItemGroup** لتضمين ملحق Retail في الحزم القابلة للنشر:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

        أضف الأسطر التالية إلى قسم **ItemGroup** لتضمين ملحق Retail في الحزم القابلة للنشر:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. أضف الأسطر التالية إلى قسم **ItemGroup** لتضمين ملحقات CRT في الحزم القابلة للنشر:

        # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. أضف الأسطر التالية إلى قسم **ItemGroup** لتضمين ملحق خادم Retail في الحزم القابلة للنشر:

        # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. قم بتعديل الملفات التالية لتضمين ملفات الموارد الخاصة بالنرويج في الحزم القابلة للنشر:
    - Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Packages\RetailServer\Sdk.RetailServerSetup.proj
  
  - بالنسبة إلى ملف **Sdk.ModernPos.Shared.csproj** 
    - إضافة سطر إلى قسم **ItemGroup**
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > بدلاً من <File_name> حدد اسم ملف المورد. نفس الشيء ينطبق على الأمثلة الأخرى الواردة أدناه.
 
    - إضافة سطر إلى قسم **Target Name="CopyPackageFiles"**
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - بالنسبة إلى ملف **Sdk.RetailServerSetup.proj** 
    - إضافة سطر إلى قسم **ItemGroup**
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - إضافة سطر إلى قسم **Target Name="CopyPackageFiles"**
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. قم بتعديل ملف تكوين الشهادة عن طريق تحديد بصمة الإبهام وموقع المتجر واسم المتجر للشهادة التي يجب استخدامها لتوقيع معاملات المبيعات. وبعد ذلك، انسخ ملف التكوين إلى مجلد **المراجع**.

    # <a name="application-update-4"></a>[تحديث التطبيق 4](#tab/app-update-4)

    تمت تسمية هذا الملف باسم **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**، وهو موجود ضمن **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="application-update-5-and-later"></a>[تحديث التطبيق 5 والإصدارات الأحدث](#tab/app-update-5-and-later)

    تمت تسمية هذا الملف باسم **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**، وهو موجود ضمن **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    تمت تسمية هذا الملف باسم **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**، وهو موجود ضمن **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-732-and-later"></a>[الإصدار 7.3.2 من Retail والإصدارات اللاحقة](#tab/retail-7-3-2)

    تمت تسمية الملف باسم **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**، وهو موجود ضمن **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-735-and-later"></a>[الإصدار 7.3.5 من Retail والإصدارات اللاحقة](#tab/retail-7-3-5)

    تمت تسمية الملف باسم **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**، وهو موجود ضمن **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-811-and-later"></a>[الإصدار 8.1.1 من Retail والإصدارات اللاحقة](#tab/retail-8-1-1)

    تمت تسمية الملف باسم **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**، وهو موجود ضمن **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    ---

6. قم بتحديث ملف تكوين خادم Retail. في ملف **RetailSDK\\Packages\\RetailServer\\Code\\web.config**، أضف الأسطر التالية إلى قسم **extensionComposition**.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. قم بتشغيل **msbuild** لحزمه البرامج النهائية للبيع بأكملها لإنشاء حزم قابله للنشر.
8. قم بتطبيق الحزم من خلال Microsoft Dynamics Lifecycle Services (LCS) أو يدويًا. لمزيد من المعلومات، راجع [إنشاء الحزم القابلة للنشر](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>تمكين التوقيع الرقمي في وضع عدم الاتصال لنقاط البيع الحديثة

لتمكين التوقيع الرقمي في وضع عدم الاتصال لـ Modern POS، يجب اتباع هذه الخطوات بعد تنشيط Modern POS على جهاز جديد.

1. سجل الدخول إلى POS.
2. في صفحة **حالة اتصال قاعدة البيانات**، تاكد من مزامنة قاعده البيانات غير المتصلة بشكل كامل. عندما تكون قيمه حقل **التنزيلات المعلقة** هي **0** (صفر)، تتم مزامنة قاعده البيانات بالكامل.
3. قم بتسجيل الخروج من نقطة البيع.
4. انتظر قليلاً حتى تتم مزامنة قاعدة البيانات دون اتصال بشكل كامل.
5. سجل الدخول إلى POS.
6. في صفحة **حالة اتصال قاعدة البيانات**، تاكد من مزامنة قاعده البيانات غير المتصلة بشكل كامل. عندما تكون قيمه حقل **الحركات المعلقة في قاعدة البيانات غير المتصلة** هي **0** (صفر)، تتم مزامنة قاعده البيانات بالكامل.
7. أعد تشغيل Modern POS.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
