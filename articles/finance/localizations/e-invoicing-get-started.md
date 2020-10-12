---
title: بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية
description: يوفر هذا الموضوع معلومات تساعدك على بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في Microsoft Dynamics 365 Finance وفي Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 61933bb846383932d7dd73e9c4d3c2db7a515a98
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835899"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

يوفر هذا الموضوع معلومات تساعدك على بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية. إنه يقوم أولاً بإرشادك عبر خطوات التكوين في Microsoft Dynamics Lifecycle Services (LCS) وRegulatory Configuration Services (RCS) وDynamics 365 Finance. وبعد ذلك، يصف عملية إرسال المستندات من خلال الخدمة باستخدام Dynamics 365 Finance أو Dynamics 365 Supply Chain Management. ستتعلم أيضًا كيفيه ترجمة سجلات التسليم.

## <a name="availability"></a>التوفر

تتوفر الوظيفة الإضافية الفوترة الإلكترونية‬ بشكل أولي في عدة بلدان. تدعم الوظيفة الإضافية إنشاء الفواتير الإلكترونية وإرسال مستندات العمل التالية:

| البلد/المنطقة  | مستند أعمال                          |
|-----------------|--------------------------------------------|
| النمسا         | فواتير المبيعات والمشروع                 |
| بلجيكا         | فواتير المبيعات والمشروع                 |
| البرازيل          | نموذج المستند المالي الإلكتروني 55 (NF-e) |
| الدنمارك         | فواتير المبيعات والمشروع                 |
| إستونيا         | فواتير المبيعات والمشروع                 |
| فنلندا         | فواتير المبيعات والمشروع                 |
| فرنسا          | فواتير المبيعات والمشروع                 |
| ألمانيا         | فواتير المبيعات والمشروع                 |
| إيطاليا           | فواتير المبيعات والمشروع                 |
| المكسيك          | فاتورة CFDI                               |
| هولندا     | فواتير المبيعات والمشروع                 |
| النرويج          | فواتير المبيعات والمشروع                 |
| إسبانيا           | فواتير المبيعات والمشروع                 |
| أوروبا          | فواتير المبيعات والمشروع PEPPOL          |
    
## <a name="licensing"></a>الترخيص

يمكنك استخدام الوظيفة الإضافية الفوترة الإلكترونية مع ترخيصك الحالي. لا حاجة إلى تراخيص إضافية لاستخدام الخدمة.

## <a name="prerequisites"></a>المتطلبات الأساسية

قبل أن تتمكن من استكمال الخطوات في هذا الموضوع، يجب إتمام المهام اللازمة التالية:

- الوصول إلى حسابك في LCS.
- مشروع نشر LCS يتضمن Finance أو Supply Chain Management الإصدار 10.0.12 أو أحدث.
- الوصول إلى حسابك في RCS.
- تشغيل ميزة العولمة لحساب RCS من خلال الوحدة النمطية **إدارة الميزات**. لمزيد من المعلومات، راجع [Regulatory Configuration Services (RCS) - ميزات العولمة](rcs-globalization-feature.md)
- إنشاء مورد مخزن رئيسي وحساب تخزين في Azure. لمزيد من المعلومات، راجع [إنشاء حساب تخزين وKey Vault في Azure](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="overview"></a>نظرة عامة

يبين الرسم التوضيحي التالي الخطوات الخمس الأساسية التي ستقوم بإكمالها في هذا الموضوع.

![نظرة عامة على الخطوات الخمس في هذا الموضوع](media/e-invoicing-services-get-started-overview-5-steps.png)

1. **إعداد موارد Azure:** تكوين مساحة تخزين Azure وتحميل الشهادات الرقمية في Azure Key Vault.
2. **إعداد LCS:** تثبيت الوظيفة الإضافية للخدمات المصغرة.
3. **إعداد RCS:** إعداد البيئة ووصول المستخدم وميزات الفوترة الإلكترونية.
4. **إعداد العميل:** إعداد الاتصال بين العميل والوظيفة الإضافية الفوترة الإلكترونية، وإيقاف تشغيل الميزات القديمة لإرسال الاستجابات واستلامها للمستندات الإلكترونية.
5. **إرسال الفواتير:** إرسال المستندات الإلكترونية من خلال الوظيفة الإضافية الفوترة الإلكترونية، واستلام الاستجابات.

> [!NOTE]
> تُعد بعض خطوات التكوين في هذا الموضوع عامة وغير محددة ببلد/منطقة. تم وصف الخطوات وإجراءات الإعدادات الخاصة ببلد/منطقة في المواضيع الخاصة بالبلد/المنطقة.

## <a name="lcs-setup"></a>إعداد LCS

1. سجل دخولك إلى حساب LCS.
2. حدد مشروع نشر LCS. قبل أن تتمكن من تحديد المشروع، يجب أن يكون قيد التشغيل.
3. على علامة التبويب السريعة **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.
4. حدد **إرسال مستندات العمل**.
5. في مربع الحوار **إعداد الوظيفة الإضافية**، في الحقل **معرف تطبيق AAD** ، أدخل **091c98b0-a1c9-4b02-b62c-7753395ccabe**. هذه القيمة هي قيمة ثابتة.
6. في الحقل **معرف مستأجر AAD**، أدخل معرف حساب اشتراك Azure.

    ![مربع الحوار "إعداد الوظيفة الإضافية" في LCS](media/e-invoicing-services-get-started-lcs-addin-setup.png)

7. حدد خانة الاختيار لقبول البنود والشروط.
8. حدد **تثبيت**.

## <a name="rcs-setup"></a>إعداد RCS

اثناء إعداد RCS، ستقوم بإكمال المهام التالية:

1. إعداد المخزن الرئيسي في RCS.
2. إعداد تكامل RCS باستخدام خادم الوظيفة الإضافية الفوترة الإلكترونية.
3. إنشاء بيئة الوظيفة الإضافية الفوترة الإلكترونية لمؤسستك.

### <a name="set-up-the-key-vault-in-rcs"></a>إعداد المخزن الرئيسي في RCS

1. سجل دخولك إلى حساب RCS.
2. في مساحة العمل **ميزات العولمة**، في قسم **البيئات**، حدد الإطار المتجانب **الفوترة الإلكترونية**.
3. حدد **بيئات الخدمة**.

    ![تحديد بيئات الخدمة](media/e-invoicing-services-get-started-select-service-environments.png)

> [!NOTE]
> يمنح الخيار **التطبيقات المتصلة** حق الوصول للتكوين التلقائي للوظيفة الإضافية الفوترة الإلكترونية في Finance أو Supply Management من خلال RCS. ولكن هذه الميزة لا تزال قيد التطوير حاليًا.

4. في جزء الإجراءات، حدد **معلمات المخزن الرئيسي**.

    ![تحديد معلمة المخزن الرئيسي](media/e-invoicing-services-get-started-select-key-vault-parameters.png)

5. في جزء الإجراءات، حدد **جديد** لإضافة مخزن رئيسي.
6. في الحقل **URI‏‎ المخزن الرئيسي**، أدخل قيمة السمة **اسم DNS** لمورد المخزن الرئيسي الذي قمت بتكوينه في Azure. للحصول على معلومات حول المكان حيث يمكن العثور على قيمة **اسم DNS**، راجع [إنشاء حساب تخزين وKey Vault في Azure](e-invoicing-create-azure-storage-account-key-vault.md).

    ![حقل URI المخزن الرئيسي](media/e-invoicing-services-get-started-enter-key-vault-uri.png)

7. علي علامة التبويب السريعة **الشهادات**، حدد **إضافة**، وأدخل أسماء الشهادات الرقمية وأسرار المخزن الرئيسي. يتم تكوين مجموعتي القيم في مورد المخزن الرئيسي في Azure.

    ![إضافة الشهادات](media/e-invoicing-services-get-started-add-digital-certificates.png)

8. إذا كانت الفاتورة الخاصة ببلدك/منطقتك تتطلب تطبيق سلسلة من الشهادات على توقيع رقمي، فحدد **سلسلة الشهادات** في جزء الإجراءات، ثم أدخل تسلسل الشهادات أو أسرار المخزن الرئيسي التي تشكّل السلسلة.

### <a name="set-up-the-rcs-integration-with-the-electronic-invoicing-add-on-server"></a>إعداد تكامل RCS باستخدام خادم الوظيفة الإضافية الفوترة الإلكترونية

1. في مساحة عمل **ميزات العولمة**، في قسم **الارتباطات‬ ذات الصلة**، حدد **معلمات التقارير الإلكترونية**.
2. حدد **انقر هنا للاتصال بـ Lifecycle Services**. إذا لم ترغب في الاتصال بـ LCS، فحدد **إلغاء الأمر**.
3. على علامة التبويب **الوظيفة الإضافية الفوترة الإلكترونية**، في الحقل **URI‏‎ نقطة نهاية الخدمة**، أدخل `https://businessdocumentsubmission.us.operations365.dynamics.com/`.
4. في الحقل **معرف التطبيق**، تأكد من أنه يعرض المعرف **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. هذه القيمة هي قيمة ثابتة.
5. في الحقل **معرف بيئة LCS**، أدخل معرف حساب اشتراك LCS.

![إدخال معلمات الوظيفة الإضافية الفوترة الإلكترونية](media/e-invoicing-services-get-started-enter-e-invoicing-parameters.png)

### <a name="add-an-electronic-invoicing-add-on-environment"></a>إضافة بيئة الوظيفة الإضافية الفوترة الإلكترونية

يمكنك إنشاء بيئات مختلفة للوظيفة الإضافية الفوترة الإلكترونية، مثل بيئات التطوير أو الاختبار أو التشغيل.

1. في مساحة العمل **ميزات العولمة**، في قسم **البيئات**، حدد الإطار المتجانب **الفوترة الإلكترونية**.
2. حدد **جديد** لإنشاء بيئة.
3. في الحقل **حساب رمز SAS المميز لمساحة التخزين**، أدخل سر المخزن الرئيسي الذي قمت بتكوينه في المخزن الرئيسي في RCS.

    ![حقل حساب رمز SAS المميز لمساحة التخزين](media/e-invoicing-services-get-started-enter-sas-token-secret.png)

4. على علامة التبويب السريعة **المستخدمون**، حدد **جديد** لمنح المستخدمين حق الوصول إلى هذه البيئة.

    ![إضافة مستخدمي الخدمة](media/e-invoicing-services-get-started-enter-service-users.png)

5. في جزء الإجراءات، حدد **نشر** لنشر البيئة على خادم الوظيفة الإضافية الفوترة الإلكترونية.

    ![الزر "نشر"](media/e-invoicing-services-get-started-publish-service-environment.png)

### <a name="e-invoicing-feature-setup"></a>إعداد ميزة الفوترة الإلكترونية

"ميزة الفوترة الإلكترونية" هي الاسم العام للمورد الذي تم تكوينه ونشره لاستهلاك خادم الوظيفة الإضافية الفوترة الإلكترونية. يجمع إعداد ميزة الفوترة الإلكترونية، من ضمن أشياء أخرى، استخدام تنسيقات تكوين التقارير الإلكترونية لإنشاء ملفات تصدير واستيراد قابلة للتكوين، واستخدام إجراءات وسير مهام إجراءات لتمكين إنشاء قواعد قابلة للتكوين لإرسال الطلبات واستيراد الاستجابات وتحليل محتويات الاستجابات.

نظرا للتباينات في تنسيقات الفواتير وسير مهام الإجراءات، يعتمد إعداد ميزة الفوترة الإلكترونية على البلد/المنطقة.

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>إعداد الوظيفة الإضافية الفوترة الإلكترونية في Finance أو Supply Chain Management 

خلال عملية الإعداد هذه، ستُكمل المهام التالية:

1. فتح ميزة ذات إصدار للتقييم
2. تشغيل ميزة تكامل الوظيفة الإضافية الفوترة الإلكترونية لتمكين التكامل مع Finance.
3. إعداد عنوان URL لنقطة نهاية الوظيفة الإضافية الفوترة الإلكترونية.
4. استيراد تكوينات التقارير الإلكترونية المرتبطة بميزة الفوترة الإلكترونية الخاصة بالبلد/المنطقة.
5. تشغيل ميزة الفوترة الإلكترونية القابلة للتطبيق الخاصة بالبلد/المنطقة.
6. استيراد تكوينات التقارير الإلكترونية وإعداد أنواع الاستجابات المطلوبة لتحديث مستند الفاتورة الخاص بالبلد/المنطقة كنتيجة لعملية الإرسال.

### <a name="open-flighted-feature"></a>فتح ميزة ذات إصدار للتقييم
يتم تمكين ميزة تكامل الفاتورة الإلكترونية من خلال عرض إصدار للتقييم. عرض إصدار للتقييم هو مفهوم يسمح بتشغيل الميزة أو إيقاف تشغيلها بشكل افتراضي. تتيح الخطوات التالية إصدارًا للتقييم في بيئة غير خاصة بالإنتاج. 

1. قم بتنفيذ أمر SQL التالي:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)
    
2. بعد إجراء التغيير المذكور أعلاه، نفّذ IISReset على جميع خوادم AOS

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>تشغيل ميزة تكامل الوظيفة الإضافية الفوترة الإلكترونية

1. سجل دخولك إلى Finance أو Supply Chain Management.
2. في مساحة عمل **إدارة الميزات**، ابحث عن الميزة الجديدة **تكامل الوظيفة الإضافية الفوترة الإلكترونية القابلة للتكوين**. إذا لم تظهر الميزة في صفحة إدارة الميزات، قم بتشغيل الوظيفة **التحقق من وجود تحديثات**
3. حدد الميزة، ثم حدد **تمكين الآن**.

### <a name="set-up-the-service-endpoint-url"></a>إعداد URL نقطة نهاية الخدمة

1. انتقل إلى **إدارة المؤسسة \> الإعداد \> معلمات المستندات الإلكترونية**.
2. على علامة التبويب **خدمة الإرسال**، في الحقل **URL‏‎ نقطة نهاية الخدمة**، أدخل `https://businessdocumentsubmission.us.operations365.dynamics.com/`.
3. في الحقل **البيئة**، أدخل اسم بيئة الوظيفة الإضافية الفوترة الإلكترونية التي أنشأتها أثناء إعداد RCS.

![إدخال معلمات الخدمة](media/e-invoicing-services-get-started-enter-service-endpoint.png)

### <a name="import-the-er-configurations"></a>استيراد تكوينات التقارير الإلكترونية

لتمكين تجميع بيانات العمل وإرسالها إلى الوظيفة الإضافية الفوترة الإلكترونية، يجب عليك استيراد نموذج بيانات التقارير الإلكترونية وتكوين نموذج بيانات التقارير الإلكترونية المرتبطين بميزة الفوترة الإلكترونية الخاصة بالبلد/المنطقة التي ترغب في استخدامها.

1. في مساحة عمل **إعداد التقارير الإلكترونية**، في قسم **موفرو التكوين**، حدد اللوحة **Microsoft**. تأكد من تعيين موفر التكوين هذا إلى **نشط**. لمزيد من المعلومات حول كيفية تعيين موفر إلى **نشط**، راجع [إنشاء موفري التكوين ووضع علامة نشط عليهم‬](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. حدد **المستودعات**.
4. حدد **المورد العمومي**، ثم حدد **فتح**.
5. في مربع الحوار **الاتصال بـ Lifecycle Services**، حدد **انقر هنا للاتصال بـ Lifecycle Service**.
6. استنادًا إلى البلد أو المنطقة حيث تريد استخدام ميزة الفوترة الإلكترونية، يجب عليك استيراد نموذج البيانات القابل للتطبيق وتعيين نموذج البيانات والتنسيقات. للحصول على معلومات حول تكوينات التقارير الإلكترونية التي يجب عليك استيرادها، راجع الموضوع الخاص بالبلد/المنطقة "بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية".
7. استورد **نموذج سياق فاتورة العميل**. يحتوي هذا النموذج على معلمات إضافية تصف، ضمن أشياء أخرى، البيئة في Finance التي يتم استخدامها لوظيفة الفوترة الإلكترونية اثناء إرسال بيانات العمل.

### <a name="turn-on-countryregion-specific-e-invoicing-features"></a><a name="region-specific"></a>تشغيل ميزات الفوترة الإلكترونية الخاصة بالبلد/المنطقة

لتشغيل تشغيل ميزات الفوترة الإلكترونية الخاصة بالبلد/المنطقة بحيث تعمل مع الوظيفة الإضافية الفوترة الإلكترونية، يجب تشغيل الميزة في كل كيان قانوني حيث تريد استخدامها. وبعد ذلك، سيتعذر استخدام تكامل الفوترة الإلكترونية القديمة، ويتم تشغيل التكامل مع الوظيفة الإضافية الفوترة الإلكترونية الجديدة.

1. انتقل إلى **إدارة المؤسسة \> الإعداد \> معلمات المستندات الإلكترونية**.
2. في علامة التبويب **الميزات**، في الصف الخاص بالميزة المرتبطة بميزة الفوترة الإلكترونية الخاصة بالبلد/المنطقة، حدد خانة الاختيار في العمود **ممكّن**. للحصول على معلومات حول الميزة التي يجب عليك تشغيلها، راجع الموضوع الخاص بالبلد/المنطقة "بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية".

![تشغيل ميزة الفوترة الإلكترونية](media/e-invoicing-services-get-started-enable-invoicing-feature.png)

> [!NOTE]
> إذا كانت لديك العديد من الكيانات القانونية التي تم تكوينها لبلدان أو مناطق مختلفة، فيمكنك تشغيل ميزة الفوترة الإلكترونية الخاصة بالبلد/المنطقة لكل كيان قانوني.

### <a name="import-er-configurations-and-set-up-the-response-types-to-update-your-countryregion-specific-invoice-document"></a>استيراد تكوينات التقارير الإلكترونية وإعداد أنواع الاستجابات لتحديث مستند الفاتورة الخاص بالبلد/المنطقة

إذا كان مستند الفاتورة المرسل يتطلب تحديثًا بعد الاستجابة لعملية الإرسال إلى خدمات التخويل الحكومية، فيجب استيراد نموذج بيانات التقارير الإلكترونية وتكوينات التقارير الإلكترونية لتميكن تحديث حالة مستند فاتورة أو أي حقل إضافي آخر.

1. في مساحة عمل **إعداد التقارير الإلكترونية**، في قسم **موفرو التكوين**، حدد اللوحة **Microsoft**.
2. حدد **المستودعات**.
3. حدد **المورد العمومي**، ثم حدد **فتح**.
4. استورد **نموذج رسالة الاستجابة** و**تنسيق استيراد رسالة الاستجابة** و**تعيين نموذج استجابة الرسالة إلى الوجهة** و**تنسيق استيراد محتويات الملف**.
5. انتقل إلى **إدارة المؤسسة \> الإعداد \> معلمات المستندات الإلكترونية**.
6. من علامة التبويب **المستند الإلكتروني**، حدد **إضافة** لإدخال اسم الجدول المرتبط بمستند الفاتورة الخاص بالبلد/المنطقة. للحصول على معلومات حول أسماء الجداول التي يجب عليك تحديدها، راجع الموضوع الخاص بالبلد/المنطقة "بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية".
7. حدد **أنواع الاستجابات** لتكوين أنواع الاستجابات. للحصول على معلومات حول أسماء الجداول التي يجب عليك تحديدها، راجع الموضوع الخاص بالبلد/المنطقة "بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية".

![إعداد أنواع الاستجابات](media/e-invoicing-services-get-started-set-up-response-types.png)

## <a name="e-invoicing-feature-names-by-country"></a>أسماء ميزة الفوترة الإلكترونية حسب البلد 
يصف الجدول التالي ميزات الفوترة الإلكترونية الأخرى المتوفرة للتنزيل من المستودع العمومي للتقارير الإلكترونية لإنشاء الفواتير الإلكترونية.
في RCS، يمكنك تنزيل ميزات الفوترة الإلكترونية المدرجة في هذا الجدول وتكوينات التقارير الإلكترونية وعمليات إعداد ميزة الفوترة الإلكترونية المتوفرة.
في Finance، يمكنك تمكين مراجع الميزة ذات الصلة في صفحة **معلمات المستند الإلكتروني** لإصدار فواتير إلكترونية لهذه البلدان. لمزيد من المعلومات، راجع القسم [تشغيل ميزات الفوترة الإلكترونية الخاصة بالبلد/المنطقة‬](#region-specific) سابقًا في هذا الموضوع.

| اسم الميزة                      | الوصف                                 | تكوينات التقارير الإلكترونية                                                                                                  | عمليات الإعداد                                                                                                                                                         | البلد/المنطقة  | مرجع الميزة      |
|-----------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|------------------------|
| الفواتير الإلكترونية النمساوية فواتير | فواتير المبيعات والمشروع في النمسا      | - فاتورة مبيعات OIOUBL <br>- فاتورة مشروع OIOUBL <br>- إشعار دائن للمبيعات OIOUBL <br>- إشعار دائن للمشروع OIOUBL | - إنشاء فاتورة المبيعات (AT) <br>- إنشاء فاتورة المشروع (AT) <br>- إنشاء اشعار دائن للمبيعات (AT) <br>- إنشاء اشعار دائن للمشروع (AT)         | النمسا         | EUR-00023              |
| الفاتورة الإلكترونية البلجيكية (BE)   | فواتير المبيعات والمشروع في بلجيكا      | - UBL فاتورة المبيعات BE <br>- UBL فاتورة المشروع BE <br>- UBL إشعار دائن للمشروع BE <br>- UBL إشعار دائن للمبيعات BE | - إنشاء فاتورة المبيعات (BE)<br>- إنشاء فاتورة المشروع (BE) <br>- إنشاء اشعار دائن للمبيعات (BE) <br>- إنشاء اشعار دائن للمشروع (BE)         | بلجيكا         | EUR-00023              |
| الفاتورة الإلكترونية الدانمركية    | فواتير المبيعات والمشروع في الدانمارك      | - فاتورة مبيعات OIOUBL <br>- فاتورة مشروع OIOUBL <br>- إشعار دائن للمبيعات OIOUBL <br>- إشعار دائن للمشروع OIOUBL | - إنشاء فاتورة المبيعات (DK) <br>- إنشاء فاتورة المشروع (DK) <br>- إنشاء اشعار دائن للمبيعات (DK)<br>- إنشاء اشعار دائن للمشروع (DK)         | الدنمارك         | EUR-00023<br> DK-00001 |
| الفاتورة الإلكترونية الهولندية     | فواتير المبيعات والمشروع في هولندا  | - UBL فاتورة المبيعات NL <br>- UBL فاتورة المشروع NL <br>- UBL إشعار دائن للمبيعات NL <br>- UBL إشعار دائن للمشروع NL | - إنشاء فاتورة المبيعات (NL) <br> - إنشاء فاتورة المشروع (NL) <br> - إنشاء اشعار دائن للمبيعات (NL) <br>- إنشاء اشعار دائن للمشروع (NL)          | هولندا | EUR-00023              |
| الفاتورة الإلكترونية الإستونية  | فواتير المبيعات والمشروع في إستونيا      | - فاتورة المبيعات (EE) <br> - فاتورة المشروع (EE)                                                                     | - إنشاء فاتورة المبيعات (EE) <br>- إنشاء فاتورة المشروع (EE)                                                                                           | إستونيا         | EUR-00023              |
| الفاتورة الإلكترونية الفنلندية (FI)   | فواتير المبيعات والمشروع في فنلندا      | - فاتورة المبيعات (FI) <br>- إنشاء فاتورة المشروع (FI)                                                          | - إنشاء فاتورة المبيعات (FI) <br>- إنشاء فاتورة المشروع (FI)                                                                                           | فنلندا         | EUR-00023              |
| الفاتورة الإلكترونية الفرنسية (FR)    | فواتير المبيعات والمشروع في فرنسا    | - UBL فاتورة المبيعات FR <br> - UBL فاتورة المشروع FR <br> - UBL إشعار دائن للمبيعات FR <br>- UBL إشعار دائن للمشروع FR | - إنشاء فاتورة المبيعات (FR) <br> - إنشاء فاتورة المشروع (FR) <br>- إنشاء اشعار دائن للمبيعات (FR) <br>- إنشاء اشعار دائن للمشروع (FR)         | فرنسا          | EUR-00023              |
| الفاتورة الإلكترونية الألمانية (DE)    | فواتير المبيعات والمشروع في ألمانيا      |- فاتورة المبيعات (DE) <br> - فاتورة المشروع <DE>                                                                     | - إنشاء فاتورة المبيعات (DE) <br>- إنشاء فاتورة المشروع (DE)                                                                                           | ألمانيا         | EUR-00023              |
| الفاتورة الإلكترونية النرويجية (NO) | فواتير المبيعات والمشروع في النرويج       | - فاتورة مبيعات OIOUBL <br>- فاتورة مشروع OIOUBL <br>- إشعار دائن للمبيعات OIOUBL <br>- إشعار دائن للمشروع OIOUBL | - إنشاء فاتورة المبيعات (NO) <br>- إنشاء فاتورة المشروع (NO) <br>- إنشاء اشعار دائن للمبيعات (NO) <br>- إنشاء اشعار دائن للمشروع (NO)          | النرويج          | EUR-00023<br> NO-00010 |
| الفاتورة الإلكترونية الإسبانية (ES)   | فواتير المبيعات والمشروع في إسبانيا        | - فاتورة المبيعات (ES) <br>- فاتورة المشروع (ES)                                                                     | - إنشاء فاتورة المبيعات (ES) <br>- إنشاء فاتورة المشروع (ES)                                                                                           | إسبانيا           | EUR-00023 <br>ES-00025 |
| الفاتورة الإلكترونية الإيطالية (IT)   | فواتير المبيعات والمشروع في إيطاليا        | - (معاينة) فاتورة المبيعات (IT) <br> - فاتورة المشروع (IT)                                                           | - فاتورة المبيعات <br> - فاتورة المشروع                                                                                                                           | إيطاليا           | EUR-00023 <br>IT-00036 |
| فاتورة إلكترونية PEPPOL         | إنشاء فواتير المبيعات والمشروع PEPPOL | - فاتورة مبيعات PEPPOL <br>- فاتورة مشروع PEPPOL <br>- إشعار دائن للمبيعات PEPPOL <br> - إشعار دائن للمشروع PEPPOL | - إنشاء فاتورة المبيعات PEPPOL <br>- إنشاء فاتورة المشروع PEPPOL <br>- إنشاء اشعار دائن للمبيعات PEPPOL <br>- إنشاء اشعار دائن للمشروع PEPPOL |                 | EUR-00023              |


## <a name="electronic-invoice-processing-in-finance-and-supply-chain-management"></a>معالجة الفاتورة الإلكترونية في Finance وفي Supply Chain Management

اثناء المعالجة، ستقوم بإكمال المهام التالية:

1. إرسال مستند عمل (فاتورة) من خلال الوظيفة الإضافية الفوترة الإلكترونية.
2. عرض سجلات تنفيذ الإرسال.

### <a name="submit-business-documents"></a>إرسال مستندات العمل

أثناء عملية الإرسال العادية، يكون الاتصال بين العميل والوظيفة الإضافية الفوترة الإلكترونية ثنائي الاتجاه. الغرض هو إنجاز مهمتين رئيسيتين أثناء إرسال المستندات الإلكترونية:

1. إرسال كافة المستندات الإلكتروني المعلقة بانتظار الإرسال من Finance، والتي لها الحالة الصحيحة للإرسال وتلبية معايير التحديد.
2. استيراد، إلى Finance، الاستجابة التي ترجعها الوظيفة الإضافية الفوترة الإلكترونية إلى المستندات الإلكترونية التي تم إرسالها في السابق. بعد الاستيراد، يتم تحليل الاستجابات وتحديث حالة مستندات العمل وفقًا لذلك.

يمكنك إرسال مستندات العمل إما يدويًا أو بالاستناد إلى متطلبات جدولك.

1. انتقل إلى **إدارة المؤسسة \> دوري \> المستندات الإلكترونية \> إرسال المستندات الإلكترونية**.
2. بالنسبة لعملية الإرسال الأولى لأي مستند، عيّن دائمًا الخيار **إعادة إرسال المستندات** إلى **لا**. إذا كان من الضروري إعادة إرسال مستند من خلال الخدمة، فقم بتعيين هذا الخيار إلى **نعم**.
3. على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**، حدد **تصفية** لفتح مربع الحوار **استعلام** حيث يمكنك إنشاء استعلام لتحديد مستندات لإرسالها.

![مربع الحوار إرسال المستندات الإلكترونية](media/e-invoicing-services-get-started-submission-form.png)

### <a name="filter-query"></a>استعلام تصفية

1. في مربع الحوار **استعلام**، على علامة تبويب **النطاق**، أدخل معايير التصفية باستخدام حقول **الجدول** و**الجدول المشتق** و**الحقل** و**المعايير**.
2. حدد **إضافة** لإضافة‏‎ العديد من المعايير الإضافية التي تحتاجها لتحديد مستندات العمل.

    ![إعداد معايير تصفية الإرسال](media/e-invoicing-services-get-started-set-up-submission-filter-criteria.png)

3. حدد **موافق** لإغلاق مربع الحوار **استعلام**.
4. حدد **موافق** لإرسال مستندات العمل المحددة إلى الوظيفة الإضافية الفوترة الإلكترونية.

    > [!NOTE]
    > أثناء محاولتك الأولى لإرسال مستند من خلال الخدمة، ستتم مطالبتك بتأكيد الاتصال بالوظيفة الإضافية الفوترة الإلكترونية. حدد **انقر هنا للاتصال بخدمة إرسال المستندات الإلكترونية**.
    >
    > ![مربع رسالة استدعاء خدمة إرسال المستندات الإلكترونية](media/e-invoicing-services-get-started-dialog-form-connect-e-Invoicing-services.png)
    >
    > إذا نجح الاتصال، تتلقى رسالة تأكيد.
    >
    > ![تأكيد على الاتصال بالوظيفة الإضافية الفوترة الإلكترونية](media/e-invoicing-services-get-started-confirmation-connection-e-invoicing-services.png)

5. أغلق مربع الحوار.

> [!NOTE]
> بعد كل عملية إرسال، يعرض مركز الإجراءات عدد المستندات التي تم إرسالها.
>
> ![رسائل مركز الإجراءات](media/e-invoicing-services-get-started-view-action-center-messages.png)

### <a name="submission-by-batch"></a>الإرسال على دُفعات

بدلاً من إرسال المستندات يدويًا، يمكنك تنفيذ عمليه التسليم وتشغيلها في الخلفية بشكل تلقائي، استنادًا إلى تكرار مكوّن للتنفيذ على دُفعات.

1. في مربع الحوار **إرسال المستندات الإلكترونية**، على علامة التبويب السريعة **تشغيل في الخلفية**، قم بتعيين خيار **معالجة الدفعات** إلى **نعم**.
2. من علامة التبويب **تكرار**، قم بتكوين تكرار معالجة الدُفعات.

![إعداد عملية الإرسال على دُفعات](media/e-invoicing-services-get-started-set-up-submission-batch.png)

### <a name="view-all-submission-logs"></a>عرض جميع سجلات الإرسال

1. انتقل إلى **إدارة المؤسسة \> دوري \> المستندات الإلكترونية \> سجل إرسال المستندات الإلكترونية**.
2. في الحقل **نوع المستند**، حدد نوع المستند المطلوب التصفية وفقًا له.

    ![تحديد نوع المستند لعرض سجلات الإرسال](media/e-invoicing-services-get-started-select-document-type-for-viewing-submission-log.png)

    > [!IMPORTANT]
    > تمثل القيمة التي تظهر في العمود **حالة الإرسال** الحالة المتعلقة بإكمال عملية الإرسال بحد ذاتها. إنها تشير إلى ما إذا كان قد تم تشغيل سير الإجراءات المكون في RCS حتى النهاية، بغض النظر عن الموافقة على المستند الإلكتروني أو رفضه. لا تمثل القيمة الموجودة في العمود **حالة الإرسال** الحالة الخاصة بالمستند المُرسل. يمكنك عرض حالة المستند المُرسل (أي سواء تمت الموافقة على المستند أو رفضه) على علامة التبويب السريعة **سجل إجراء المعالجة** في تفاصيل سجل الإرسال، كما تم وصفه فيما بعد.

3. في جزء الإجراءات، حدد **الاستعلامات \> تفاصيل الإرسال**.
4. استعرض تفاصيل سجل الإرسال.

    ![تفاصيل سجل الإرسال](media/e-invoicing-services-get-started-view-submission-log-form.png)

تعتمد النتائج التي تظهر في سجل الإرسال على كيفية إعداد ميزة الفاتورة الإلكترونية في RCS. ومع ذلك، بغض النظر عن الإعداد، يتضمن سجل الإرسال دائمًا ثلاث علامات تبويب سريعة:

- **إجراءات المعالجة** – تُظهر علامة التبويب السريعة هذه سجل التنفيذ للإجراءات التي تم تكوينها في إصدار الميزة الذي تم إعداده في RCS. يعرض عمود **الحالة** ما إذا كان قد تم تشغيل الإجراء بنجاح ام لا.
- **ملفات الإجراءات**، تُظهر علامة التبويب السريعة هذه الملفات الوسيطة التي تم إنشاؤها أثناء تنفيذ الإجراءات. يمكنك تحديد **عرض** لتنزيل الملف وعرض محتوياته.
- **سجل إجراء المعالجة** – تُظهر علامة التبويب السريعة هذه نتائج الاتصال بين الوظيفة الإضافية الفوترة الإلكترونية وخدمة الويب المستهدفة. وهو يعرض أيضًا ما تم إرجاعه بواسطة معالجة خدمة الويب.

## <a name="related-topics"></a>مواضيع مرتبطة

- [نظرة عامة على الوظيفة الإضافية الفوترة الإلكترونية](e-invoicing-service-overview.md)
- [بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في البرازيل](e-invoicing-bra-get-started.md)
- [بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في المكسيك](e-invoicing-mex-get-started.md)
- [بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في إيطاليا](e-invoicing-ita-get-started.md)
- [إعداد الوظيفة الإضافية الفوترة الإلكترونية](e-invoicing-setup.md)