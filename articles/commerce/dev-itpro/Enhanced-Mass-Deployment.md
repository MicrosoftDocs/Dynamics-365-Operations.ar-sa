---
title: التوزيع الجماعي لمكونات الخدمة الذاتية المختومة لـ Commerce
description: يشرح هذا المقال كيفية استخدام اطار العمل لمثبتات مكونات الخدمة الذاتية لتنفيذ التثبيت الصامت وعمليات نشر الخدمات.
author: jashanno
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2021-04-30
ms.openlocfilehash: 66a711aff90221e594f4b2a0df3735eac93d0c9b
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387009"
---
# <a name="mass-deployment-of-sealed-commerce-self-service-components"></a>التوزيع الجماعي لمكونات الخدمة الذاتية المختومة لـ Commerce

[!include [banner](../includes/banner.md)]

ينطبق هذا المقال على اطار العمل المحمي، ومثبتات المكونات التي يتم إصدارها كل شهر، اعتبارًا من الإصدار 10.0.18، والمتوفرة في مكتبه الأصول المشتركة في Microsoft Dynamics Lifecycle Services (LCS). لاحظ ان الإصدارات الأولى لهذه المثبتات الجديدة معينة على أنها **(إصدار أولي)**. ومع ذلك، فإن الغرض الوحيد من هذا التعيين هو التمييز بين المثبتات الجديدة بينما تحدد Microsoft ما إذا كانت هناك أي متطلبات وظيفية إضافية لاستخدامها. وهذا لا يعني أن المثبتات ليست صالحة للإنتاج. استنادًا إلى إصدار المثبتات الجديدة هذه، تخطط Microsoft لإيقاف العمل بالمثبتات القديمة في أكتوبر 2023 أو حوالي ذلك التاريخ. 

يشرح هذا المقال كيفية استخدام المثبتات الجديدة لتنفيذ عمليات التثبيت الصامت وتحديثات الخدمات باستخدام وسيطات سطر الأوامر. تتيح لك هذه الوسيطات بإجراء عملية نشر شاملة باستخدام عدة طرق مختلفة.

> [!NOTE]
> لن تتوفر المثبتات المحمية الجديدة للخدمة الذاتي في المقر الرئيسي ويمكن تنزيلها من خلال LCS فقط.

## <a name="delimiters-for-mass-deployment"></a>محددات النشر الشامل

يعرض الجدول التالي المحددات التي يمكن استخدامها في تنفيذ سطر الأوامر.


| محدِّد                 | Description |
|---------------------------|-------------|
| -AadTokenIssuerPrefix | بادئة جهة إصدار الرمز المميز لـ Microsoft Azure Active Directory (Azure AD). |
| -AsyncClientAadClientId | معرف عميل Azure AD الذي يجب أن يستخدمه Async Client أثناء الاتصال بالمقر الرئيسي. |
| -AsyncClientAppInsightsInstrumentationKey | مفتاح أدوات Async Client AppInsights. |
| -AsyncClientCertFullPath | مسار URN المنسق بالكامل الذي يستخدم بصمة الإبهام كمقياس بحث لموقع شهادة هوية Async Client الذي يجب استخدامه للمصادقة مع Azure AD للاتصالات بالمقر الرئيسي. على سبيل المثال، `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` عبارة عن URN منسق بشكل صحيح. سيتم استبدال القيمة **\<MyThumbprint\>** ببصمة إبهام الشهادة التي يجب استخدامها. لا تستخدم هذه المعلمة مع المعلمة **-AsyncClientCertThumbprint**. |
| -AsyncClientCertThumbprint | بصمة الإبهام لشهادة هوية Async Client التي يجب استخدامها للمصادقة مع Azure AD للاتصالات بالمقر الرئيسي.‬ سيتم استخدام بصمة الإبهام هذه للبحث عن اسم وموقع **LocalMachine/My store** للعثور على الشهادة الصحيحة التي يجب استخدامها. لا تستخدم هذه المعلمة مع المعلمة **-AsyncClientCertFullPath**. |
| -ClientAppInsightsInstrumentationKey | مفتاح أدوات Client AppInsights. |
| -CloudPosAppInsightsInstrumentationKey | مفتاح أدوات Cloud POS AppInsights. |
| -Config | ملف التكوين الذي يجب استخدامه أثناء التثبيت. هناك مثال عن اسم ملف وهو **Contoso.CommerceScaleUnit.xml**. |
| -CposAadClientId | معرف عميل Azure AD الذي يجب استخدامه من قبل Cloud POS أثناء تنشيط الجهاز. هذه المعلمة غير مطلوبة لعمليات النشر المحلية. |
| -Device | معرف الجهاز، كما هو موضح في صفحة **الأجهزة** في المقر الرئيسي. |
| -EnvironmentId | معرف البيئة. |
| -HardwareStationAppInsightsInstrumentationKey | مفتاح أدوات AppInsights لمحطة الأجهزة. |
| تثبيت | معلمة تحدد ما إذا كان يجب تثبيت المكون الذي يقدمه هذا المثبت. هذه المعلمة مطلوبة لإجراء تثبيت وليس لها حرف شرطة بادئة. |
| -InstallOffline | بالنسبة لنقطة البيع الحديثة، تحدد هذه المعلمة أنه يجب أيضًا تثبيت قاعدة البيانات غير المتصلة وتكوينها. استخدم المعلمة **-SQLServerName** أيضًا. وبخلاف ذلك، سيحاول المثبت العثور على مثيل افتراضي يلبي المتطلبات الأساسية. |
| -Port | المنفذ الذي ينبغي إقرانه بالدليل الظاهري لـ Retail Server والذي يجب أن يستخدمه هذا الدليل الظاهري. إذا تم تعيين المنفذ، فسيتم استخدام المنفذ الافتراضي، 443. |
| -Register | معرف السجل، كما هو موضح في صفحة **السجلات** في المقر الرئيسي. |
| -RetailServerAadClientId | معرف عميل Azure AD الذي يجب أن يستخدمه Retail Server أثناء الاتصال بالمقر الرئيسي. |
| -RetailServerAadResourceId | معرف مورد تطبيق Retail Server Azure AD الذي يجب استخدامها أثناء تنشيط الجهاز. هذه المعلمة غير مطلوبة لعمليات النشر المحلية. |
| -RetailServerCertFullPath | مسار URN المنسق بالكامل الذي يستخدم بصمة الإبهام كمقياس بحث لشهادة هوية Retail Server الذي يجب استخدامه للمصادقة مع Azure AD للاتصالات بالمقر الرئيسي. على سبيل المثال، `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` عبارة عن URN منسق بشكل صحيح حيث سيتم استبدال قيمة **\<MyThumbprint\>** ببصمة إبهام الشهادة التي سيتم استخدامها. لا تستخدم هذه المعلمة مع المعلمة **-RetailServerCertThumbprint**. |
| -RetailServerCertThumbprint | بصمة الإبهام لشهادة هوية Retail Server التي يجب استخدامها للمصادقة مع Azure AD للاتصالات بالمقر الرئيسي.‬ سيتم استخدام بصمة الإبهام هذه للبحث عن اسم وموقع متجر **LocalMachine/My** للعثور على الشهادة الصحيحة التي يجب استخدامها. لا تستخدم هذه المعلمة مع المعلمة **-RetailServerCertFullPath** parameter. |
| -RetailServerURL | عنوان URL لـ Retail Server الذي يجب أن يستخدمه المثبت. (يُعرف عنوان URL هذا أيضًا باسم Commerce Scale Unit \[CSU\] URL.) بالنسبة إلى نقطة البيع الحديثة، سيتم استخدام هذه القيمة أثناء تنشيط الجهاز. |
| -SkipAadCredentialsCheck| مفتاح تبديل يشير إلى ما إذا كان من الضروري تخطي عمليات فحص المتطلبات الأساسية لبيانات اعتماد Azure AD. القيمة الافتراضية هي **false**. |
| -SkipCertCheck | مفتاح تبديل يشير إلى ما إذا كان من الضروري تخطي عمليات فحص المتطلبات الأساسية للشهادة. القيمة الافتراضية هي **false**. |
| -SkipIisCheck | مفتاح تبديل يشير إلى ما إذا كان من الضروري تخطي عمليات فحص المتطلبات الأساسية لخدمات معلومات الإنترنت‬ (IIS). القيمة الافتراضية هي **false**. |
| -SkipNetFrameworkCheck | مفتاح تبديل يشير إلى ما إذا كان من الضروري تخطي عمليات فحص المتطلبات الأساسية لـ NET Framework. القيمة الافتراضية هي **false**. |
| -SkipScaleUnitHealthcheck | مفتاح تبديل يشير إلى ما إذا كان يجب تخطي عملية فحص السلامة على المكونات المثبتة. القيمة الافتراضية هي **false**. |
| -SkipSChannelCheck | مفتاح تبديل يشير إلى ما إذا كان من الضروري تخطي عمليات فحص المتطلبات الأساسية للقناة الآمنة. القيمة الافتراضية هي **false**. |
| -SkipSqlFullTextCheck | مفتاح تبديل يشير إلى ما إذا كان يجب تخطي عملية التحقق من صحة المتطلبات الأساسية لـ SQL Server التي تتطلب البحث عن كامل النص. القيمة الافتراضية هي **false**. |
| -SkipSqlServerCheck | مفتاح تبديل يشير إلى ما إذا كان من الضروري تخطي عمليات فحص المتطلبات الأساسية لـ SQL Server. القيمة الافتراضية هي **false**. |
| -SqlServerName | اسم SQL Server. إذا لم يتم تحديد الاسم، فسيحاول المثبت العثور على المثيل الافتراضي. |
| -SslcertFullPath | مسار URN المنسق بالكامل الذي يستخدم بصمة الإبهام كمقياس بحث عن موقع الشهادة الذي يجب استخدامه لتشفير حركة مرور HTTP إلى وحدة القياس. على سبيل المثال، `store:\/\/My\/LocalMachine\?FindByThumbprint\=\<MyThumbprint\>` عبارة عن URN منسق بشكل صحيح حيث سيتم استبدال قيمة **\<MyThumbprint\>** ببصمة إبهام الشهادة التي سيتم استخدامها. لا تستخدم هذه المعلمة مع المعلمة **-SslCertThumbprint**. |
| -SslCertThumbprint | بصمة إبهام الشهادة التي يجب استخدامها لتشفير حركو مرور HTTP إلى وحدة القياس. سيتم استخدام بصمة الإبهام هذه للبحث عن اسم وموقع **LocalMachine/My store** للعثور على الشهادة الصحيحة التي يجب استخدامها. لا تستخدم هذه المعلمة مع المعلمة **-SslCertFullPath** parameter. |
| -StoreSystemAosUrl | عنوان URL للمقر الرئيسي (AOS). |
| -StoreSystemChannelDatabaseId | معرف قاعدة بيانات القناة (الاسم). |
| -TenantId | معرف مستأجر Azure AD. |
| -TransactionServiceAzureAuthority | هيئة Transaction Service Azure AD. |
| -TransactionServiceAzureResource | مورد Transaction Service Azure AD. |
| -TrustSqlServerCertificate | مفتاح تبديل يشير إلى ما إذا كان يجب الوثوق بشهادة الخادم أثناء تأسيس اتصال بـ SQL Server. للمساعدة على تجنب مخاطر الأمان، يجب على عمليات نشر الإنتاج ألا توقن مطلقًا بتوفير قيمة **صواب** هنا. القيمة الافتراضية هي **false**. |
| -Verbosity | مستوى التسجيل المطلوب أثناء التثبيت. بشكل عام، يجب عدم استخدام هذه القيمة. |
| -WindowsPhoneAppInsightsInstrumentationKey | مفتاح أدوات AppInsights لمحطة الأجهزة. |

## <a name="general-overview"></a>نظرة عامة

يتميز اطار العمل الجديد لمثبتات الخدمة الذاتية بميزات وتحسينات متنوعة. يُنشئ إطار العمل الجديد حاليًا مثبتات فقط لكل من نقطة البيع الحديثة ومحطة الأجهزة وCSU (مستضافة ذاتيًا). ومن الضروري فهم استخدام سطر الأوامر الأساسي للمثبتات المحمية، والتي يجب أن تبدو مشابهة لتلك المستخدمة في المثال التالي. 
 
```Console
<Component Installer Name>.exe install -<Parameter Name> "<Parameter Information>"
```

يحتاج المثبت إلى المعلمة **تثبيت** (أو **إزالة تثبيت** لإزالة التثبيت) وأي معلمات تتعلق بهذا التثبيت. يجب أن يتضمن **اسم المعلمة** أي معلمات مطلوبة مثل السجل أو CSU URL أو معلومات الشهادة. ويجب أن تتضمن **معلومات المعلمة** أي معلومات إضافية حول المعلمات.

تم إنشاء اطار العمل المحمي للسماح بالتعديلات التالية:
- **محمي** – يفصل إطار عمل المثبت الجديد تمامًا مثبتات المكونات الأساسية الموزعة من Microsoft عن التخصيصات المستندة إلى قابلية التوسعة. سيتم تثبيت التخصيصات بعد ذلك، ولكن سيتم إلغاء ربطها فيما يتعلق بالتحديثات (بحيث يُسمح بالتحديثات فقط لمكون Microsoft الأساسي، أو للتخصيصات فقط، أو كليهما).
- **GUI-less** – لم يعد هناك وجود لواجهة المستخدم (UI). بدلاً من ذلك، يوجد ملف قابل للتنفيذ بالكامل قائم على سطر الأوامر لكل مثبت مكون. هذا التغيير هو أحد التغييرات أو الميزات الرئيسية العديدة التي تُستخدم للتركيز على إطار عمل المثبت الجديد للاستخدام مع عملية النشر الشاملة.
- **تسجيل عميق** – تسمح سجلات المثبّت المحسّنة بالتحقق بشكل أفضل من اكتمال التثبيت أو فشله والخطوات التي تم تنفيذها وأي تحذيرات أو أخطاء تم إنشاؤها.
- **التنظيف** – في إطار العمل الجديد، تعمل مثبتات المكونات بجهد أكبر للحفاظ على نظافة أدلة التثبيت، من خلال مسح المحتويات الكاملة لمجلد المكون قبل تثبيت المكونات الأحدث. يضمن هذا التنظيف عدم وجود ملفات متبقية قد تسبب مشكلات وتمنع التثبيت الناجح.

لم يتم ترحيل ثلاثة مكونات إلى إطار العمل الجديد: Virtual Peripheral Simulator وAsync Server Connector Service (يُستخدم لدعم Dynamics AX 2012 R3) وReal-time Service Replacement (يُستخدم لدعم Dynamics AX 2012 R3).

> [!NOTE]
> يتم تخزين المثبتات والاحتفاظ بها محليًا.  مع مرور الوقت، من الضروري إدارة المثتبات التي تم الاحتفاظ بها أو حذفها لعدم هدر المساحة على القرص. يوصى بالاحتفاظ بالمثبت الحالي للمكون (المكونات) الأساسية وأي مثبتات للملحق للإصدارات الأحداث لأغراض الاسترداد من المواقف القصوى.

## <a name="migration"></a>الترحيل

يتطلب الترحيل من مثبتات مكونات إطار عمل الخدمة الذاتية القديمة إلى مثبتات مكونات إطار العمل الجديدة إزالة تثبيت المكونات القديمة.

- **نقطة البيع الحديثة** – تسبب إطار عمل المثبت الجديد في أن يتلقى التطبيق معرف توقيع تطبيق جديد. وبالتالي، يجب إزالة تثبيت المكونات القديمة بشكل كامل قبل تثبيت مكون نقطة البيع الحديثة لإطار العمل الجديد. بسبب متطلبات إزالة التثبيت الكاملة، سيكون تنشيط الجهاز مطلوبًا مرة أخرى. (إعادة تنشيط هذا الجهاز عبارة عن متطلب لمرة واحدة، شريطة عدم حدوث إزالة التثبيت من جديد.)
- **محطة الأجهزة** – كموقع IIS على الويب، يتطلب إطار عمل المثبت الجديد إعادة صياغة بنية المجلد الأساسي. وبالتالي، يجب إزالة تثبيت المكونات القديمة بشكل كامل قبل تثبيت مكون محطة الأجهزة لإطار العمل الجديد.
- **Commerce Scale Unit (CSU، مستضافة ذاتيًا)** – كسلسلة من مواقع IIS على الويب، يتطلب إطار عمل المثبت الجديد إعادة صياغة بنية المجلد الأساسي.  وبالتالي، يجب إزالة تثبيت المكونات القديمة بشكل كامل قبل تثبيت مكون CSU (مستضافة ذاتيًا) لإطار العمل الجديد.

## <a name="modern-pos"></a>نقطة البيع الحديثة

### <a name="before-you-begin"></a>قبل البدء

من الضروري إزالة مكون نقطة البيع الحديثة القديم ذاتي الخدمة. لمزيد من المعلومات، انظر خطوات الترحيل السابقة في هذا المقال.

> [!NOTE]
> علي نظام علي جهاز كمبيوتر واحد مثل مخطط المطور أو بيئة العرض التوضيحي، أو عند تثبيت Commerce Scale Unit ونقطه البيع الحديثة علي نفس جهاز الكمبيوتر ، يمكن Store Commerce ان تكون غير قادره علي إكمال تنشيط الجهاز. تحدث هذه المشكلة نظرا لأنه لا يمكن Store Commerce اجراء مكالمات عبر الشبكة لنفس الكمبيوتر (اي الاستدعاءات إلى نفسها). وعلي الرغم من ان هذا يجب الا يكون سيناريو في اعداد الإنتاج ، الا انه يمكن ميتيجاتيد المشكلة عن طريق تمكين استثناء استرجاع AppContainer بحيث يمكن ان تحدث الاتصالات لنفس الكمبيوتر. تتوفر العديد من التطبيقات بشكل عام للمساعدة في تمكين هذه الاسترجاع. لمزيد من المعلومات حول الاسترجاع ، راجع [كيفية تمكين الاسترجاع واستكشاف أخطاء عزل الشبكة وإصلاحها](/previous-versions/windows/apps/hh780593(v=win.10)). من المهم ان تفهم ان الاسترجاع قد يشكل مخاطره أمنيه ، لذا لا يوصي باستخدام استرجاع الا في حاله الضرورة القصوى.

### <a name="examples-of-silent-deployment"></a>أمثلة عن النشر الصامت

يعرض هذا القسم أمثلة عن الأوامر التي يتم استخدامها لتثبيت نقطة البيع الحديثة.

#### <a name="silently-install-modern-pos"></a>تثبيت نقطة البيع الحديثة بصمت

يقوم الأمر التالي بتثبيت (أو تحديث) نقطة البيع الحديثة بصمت. وهو يتضمن بنية الأوامر القياسية المستخدمة لخدمة المكونات المثبتة حاليًا بشكل صامت. تستخدم البنية قيم **&lt;InstallerName&gt;.exe** الأساسية.

يعرض الأمر الأساسي التالي الخيارات المتوفرة إذا كان التثبيت مطلوبًا. من المستحسن استخدام هذا الأمر عند اختبار المثبت أو استخدامه للمرة الأولى.

```Console
CommerceModernPOS.exe -help install
```

> [!NOTE]
> ملف التكوين غير مطلوب لنقطة البيع الحديثة. يحتوي المثبت الآن على معلمات (تم عرضها سابقًا في هذا المقال) للقيم المختلفة المستخدمة أثناء تنشيط الجهاز.

يحدد الأمر التالي جميع المعلمات التي يجب استخدامها أثناء تنشيط الجهاز بعد تثبيت تطبيق نقطة البيع الحديثة. يستخدم هذا المثال السجل **Houston-3**، وهو عبارة عن قيمة شائعة الاستخدام في بيانات Dynamics 365 Commerce التجريبية.

```Console
CommerceModernPOS.exe install -Register "Houston-3" -Device "Houston-3" -RetailServerURL "https://MyDynamics365CommerceURL.dynamics.com/Commerce"
```

يحدد الأمر التالي المعلمات التي يجب استخدامها لتثبيت قاعدة البيانات غير المتصلة وتكوينها. يتم تحديد SQL Server مع ملف التكوين الذي ينبغي استخدامه.

```Console
CommerceModernPOS.exe install -InstallOffline -SQLServerName "SQLExpress" -Config "ModernPOS.Houston-3.xml"
```

يمكنك خلط هذه المفاهيم ومطابقتها لتحقيق نتائج التثبيت التي تريدها.

## <a name="hardware-station"></a>‏محطة الأجهزة

### <a name="before-you-begin"></a>قبل البدء

من الضروري إزالة مكون محطة الأجهزة القديم ذاتي الخدمة. لمزيد من المعلومات، انظر خطوات الترحيل السابقة في هذا المقال. لم تعد أداة معلومات حساب التاجر موجودة. بدلاً من ذلك، يتم تثبيت معلومات حساب التاجر عند إقران المحطة الطرفية لنقطة البيع بمحطة الأجهزة. عند اختبار هذا المثبت للمرة الأولى، من المستحسن أن تقوم بتشغيل الأمر التالي:

```Console
CommerceHardwareStation.exe -help install
```

### <a name="examples-of-silent-deployment"></a>أمثلة عن النشر الصامت

يعرض هذا القسم أمثلة عن الأوامر التي يتم استخدامها لتثبيت محطة الأجهزة.

#### <a name="silently-install-hardware-station"></a>تثبيت محطة الأجهزة بصمت:

يقوم الأمر التالي بتثبيت (أو تحديث) محطة الأجهزة بصمت. وهو يتضمن بنية الأوامر القياسية المستخدمة لخدمة المكونات المثبتة حاليًا. تستخدم البنية قيم **&lt;InstallerName&gt;.exe** الأساسية.

يقوم الأمر التالي بتشغيل مثبت الملف القابل للتنفيذ.

```Console
HardwareStation.exe install -Port 443 -StoreSystemAOSURL "https://MyDynamics365CommerceURL.dynamics.com/" -StoreSystemChannelDatabaseID "Houston" -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers"
```

> [!NOTE]
> ملف التكوين غير مطلوب لمحطة الأجهزة. يحتوي المثبت الآن على معلمات (تم عرضها سابقًا في هذا المقال) للقيم المختلفة المطلوبة.

يحدد الأمر التالي كافة المعلمات المطلوبة لتخطي عمليات فحص المتطلبات الأساسية أثناء التثبيت القياسي. 

> [!NOTE]
> لا ينصح بتخطي عمليات الفحص بدون اختبار شامل قبل الوقت أو في حالات التطوير.

```Console
HardwareStation.exe install -SkipFirewallUpdate -SkipOPOSCheck -SkipVersionCheck -SkipURLCheck -Config "HardwareStation.Houston.xml"
```

كما هي العادة، من الشائع خلط هذه المفاهيم ومطابقتها لتحقيق نتائج التثبيت التي تريدها.

## <a name="commerce-scale-unit-self-hosted"></a>Commerce Scale Unit (المستضافة ذاتيًا)

عند اختبار هذا المثبت للمرة الأولى، من المستحسن أن تقوم بتشغيل الأمر التالي:

```Console
CommerceStoreScaleUnitSetup.exe -help install
```

### <a name="before-you-begin"></a>قبل البدء

من الضروري إزالة مكون CSU (مستضافة ذاتيًا) القديم ذاتي الخدمة. لمزيد من المعلومات، انظر خطوات الترحيل السابقة في هذا المقال.

### <a name="examples-of-silent-deployment"></a>أمثلة عن النشر الصامت

يعرض هذا القسم أمثلة عن الأوامر التي يتم استخدامها لتثبيت CSU (مستضافة ذاتيًا).

#### <a name="silently-install-csu-self-hosted"></a>تثبيت CSU (مستضافة ذاتيًا)

يقوم الأمر التالي بتثبيت (أو تحديث) CSU (مستضافة ذاتيًا). وهو يتضمن بنية الأوامر القياسية المستخدمة لخدمة المكونات المثبتة حاليًا بشكل صامت. تستخدم البنية قيم **&lt;InstallerName&gt;.exe** الأساسية.

بالمقارنة مع مثبتات الخدمة الذاتية الأخرى، تعد Commerce Scale Unit (CSU) أكثر تعقيدًا وتتطلب قدرًا كبيرًا إلى حد ما من المعلومات الإضافية. الأمر التالي هو أمر الحد الأدنى (مع المعلمات) المطلوب لتشغيل مثبت الملف القابل للتنفيذ في حالة عدم وجود ملف تكوين.

```Console
CommerceScaleUnit.exe install -port 446 -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Config "Contoso.StoreSystemSetup.xml"
```

> [!NOTE]
> لا يزال ملف التكوين مطلوباً لوحدة CSU (مستضافة ذاتيًا).

يعتبر الأمر التالي أمرًا أكثر شمولية يقوم بتشغيل مثبت الملف القابل للتنفيذ مع بعض المعلمات البديلة.

```Console
CommerceScaleUnit.exe install -Port 446 -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Verbosity 0 -Config "Contoso.StoreSystemSetup.xml"
```

يحدد الأمر التالي المعلمات المطلوبة لتخطي عمليات فحص المتطلبات الأساسية أثناء التثبيت القياسي. 

> [!NOTE]
> لا ينصح بتخطي عمليات الفحص بدون اختبار شامل قبل الوقت أو في حالات التطوير.


```Console
CommerceScaleUnit.exe installer -skipscaleunithealthcheck -skipcertcheck -skipaadcredentialscheck -skipschannelcheck -skipiischeck -skipnetcorebundlecheck -skipsqlservercheck -skipnetframeworkcheck -skipversioncheck -skipurlcheck -Config "Contoso.StoreSystemSetup.xml" -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate
```

يمكنك خلط هذه المفاهيم ومطابقتها لتحقيق نتائج التثبيت التي تريدها.

<!--## Mass deployment examples using InTune

This section will be added in a future update.

## Mass deployment examples using System Center Configuration Manager (SCCM)

This section will be added in a future update.-->

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
