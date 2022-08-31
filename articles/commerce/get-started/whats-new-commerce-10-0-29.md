---
title: إصدار أولي Dynamics 365 Commerce 10.0.29 (أكتوبر 2022)
description: تصف هذه المقالة الميزات الجديدة أو المتغيرة في 10.0.29. Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 08/17/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 1e05f53f9ecb0a1994828172f6999a0bd5c208bc
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306222"
---
# <a name="preview-of-dynamics-365-commerce-10029-october-2022"></a>إصدار أولي Dynamics 365 Commerce 10.0.29 (أكتوبر 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يصف هذا المقالا الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Commerce إصدار 10.0.29. رقم بنية هذا الإصدار هي 10.0.1326، وهو يتوفر وفق الجدول التالي:

- **إصدار أولي الإصدار:** أغسطس 2022
- **التوفر العام للإصدار (تحديث ذاتي):** سبتمبر 2022
- **التوفر العام للإصدار (تحديث تلقائي):** أكتوبر 2022

## <a name="features-included-in-this-release"></a>الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي الميزات المضمنة في هذا الإصدار. قد نقوم بتحديث هذا الموضوع ليشمل الميزات التي تمت إضافتها إلى البنية بعد نشر هذا الموضوع.

| منطقة الميزة | الميزة | معلومات إضافية | تم التمكين بواسطة |
|---------|------------------|----------------|--------------| 
| من شركة إلى شركة | [تمكين الدعم لاتفاقية المبيعات عبر القنوات](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-b2b-sales-agreement-contract-based-pricing) | تعمل هذه الميزة علي تمكين مؤسسات البائع الخاصة باعمال business (B2B) لاستخدام اتفاقيات البيع في Commerce headquarters لتحديد التسعير المستند إلى العقد لمشتريات الخاصة بها. عند قيام أحدي المشتريين من B2B بموقع ويب الخاص بالتجارة الكترونيه ، يتم تطبيق التسعير المستند إلى العقد الذي تم تكوينه لمؤسسه المشتريين لشركات المشتريين تلقائيا علي تجربه اكتشاف المنتج والشراء والسحب بأكملها. | إدارة الميزات<p>*الدعم لاتفاقية المبيعات عبر قنوات التجارة* |
| Customer Service | [قم بتمكين Customer Service باستخدام Dynamics 365لقناة متعددة الاتجاهات لـ Customer Service](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/chat-dynamics-365-commerce-omnichannel-customer-service) | تجربه دعم العميل من الفئة الاولي هي الأمر لتوفير خبره تجاريه مخصصه وديلايتفوله للعملاء. توجد العديد من التوتشبوينتس التجارية حاليا ، مثل المخازن الفعلية والقناات الفورية والقناات الاجتماعية. يتوقع العملاء تجربه دعم مخصصه في جميع هذه التوتشبوينتس. تساعد هذه الميزة في زيادة تحويلات السلة إلى المبيعات ، وزيادة التفاوض الشخصي مع العملاء ، وتحسين خدمه العملاء من خلال التكامل مع Dynamics 365 أومنيتشانيل لخدمه العملاء. | تم التمكين بواسطة المسؤول/المتخذ |
| التجارة الإلكترونية | دعم لمقارنه المنتجات في التجارة الكترونيه | قم بتمكين شوبيرس لمقارنه المنتجات عبر نطاق واسع من الفئات حتى يمكنهم جعل قرار الشراء الصحيح لأنفسهم. تتوفر هذه الميزة لكل من مواقع المستهلك (B2C) ومواقع B2B. | موقع البناء | 
| بطاقات الهدايا | دعم جداول بطاقات هدايا البيع بالتجزئة لمشاركه البيانات عبر الشركات | تدعم Dynamics headquarters القدرة علي تمكين مشاركه البيانات عبر الشركة لجداول محدده في بنيه Dynamics. في هذه الميزة ، Dynamics 365 Commerce يضيف دعمًا لمشاركة البيانات عبر الشركات لجداول بطاقات هدايا البيع بالتجزئة. التالي ، يمكن الآن لبطاقة الهدايا الموجودة في أحدي الشركات ان تكون البيانات الخاصة بها مكرره بشركه أخرى في البيئة. ستتم مشاركه التغييرات التي يتم اجراؤها علي جدول بطاقة الهدايا الخاص بالشركة الاصليه إلى جدول بطاقة الهدايا الخاص بالشركة المكرر. | المطورون |
| العولمة | [تمكين ميزات التعريب التجاري لمجموعه تطوير برامج التجارة الجديدة](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-commerce-localization-features-new-commerce-sdk) | توفر الميزة الجديدة امكانيه تمكين ميزات التعريب التجاري من Commerce headquarters باستخدام اطار العمل أو المعلمات الخاصة باداره الميزات. يتم تضمين نماذج التكامل المالي في SDK الخاص بالتجارة الجديدة ودعم التحزيم المعتمد. كما تتيح هذه الميزة امكانيه الاعتماد علي تطبيق التجارة المتجر بواسطة العملاء التجاريين العالميين.<p><p>يتضمن هذا الإصدار ميزات تعريب التجارة ونماذج التكامل المالي لـ [النمسا](../localizations/emea-aut-fi-sample.md), [الجمهورية التشيكية](../localizations/emea-cze-fi-sample.md), [فرنسا](../localizations/emea-fra-cash-registers.md), [ألمانيا](../localizations/emea-deu-fi-sample.md), [إيطاليا](../localizations/emea-ita-fpi-sample.md), [النرويج](../localizations/emea-nor-cash-registers.md), و [بولندا](../localizations/emea-pol-fpi-sample.md). | تم التمكين بواسطة المسؤول/المتخذ |
| الأداء | أزاله تبعية RTS لسيناريوهات "تحرير العميل" | التوافر العالي والأداء العالي هما توقعات افتراضيه لنقطه بيع (POS) وقناات التجارة الكترونيه. للمساعدة في الوفاء بهذه التوقعات ، لم يعد من الضروري اعتماد القناات Dynamics 365 Commerce علي الاتصالات في الوقت الحقيقي مع "Commerce headquarters" عند تحرير معلومات العميل. ويمكن لامكانيه تحرير معلومات العملاء بشكل غير متزامن للعملاء غير المتزامنين وغير المتزامنين المساعدة في تقليل المكالمات في الوقت الحقيقي لCommerce headquarters. | تم التمكين بواسطة المسؤول/المتخذ |

## <a name="feature-state-changes-in-this-release"></a>التغييرات في حالة الميزات في هذا الإصدار

يسرد الجدول التالي الميزات التي أصبحت إلزامية أو قيد التشغيل افتراضيًا في الإصدار 10.0.29. سيتم تشغيل كل هذه الميزات تلقائيًا لنظامك بمجرد التحديث إلى 10.0.29. لا يمكن إيقاف تشغيل الميزات الإلزامية، ولكن يمكن إيقاف تشغيل الميزات قيد التشغيل بشكل افتراضي باستخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

يسرد الجدول أيضًا الميزات التي كانت موجودة سابقًا في المعاينة العامة ولكنها تغيرت لتصبح متاحة بشكل عام في الإصدار 10.0.29. يشير هذا التغيير إلى ان الميزات مستحسنه الآن للاستخدام في بيئات الإنتاج. يتم إيقاف تشغيل هذه الميزات افتراضيًا ما لم يُذكر خلاف ذلك. لذلك ، يجب عليك استخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتمكينها إذا كنت تريد استخدامها.

| الميزة | العنوان‬ | حالة الميزة الجديدة |
| --- | --- | --- |
| BrazilRetailLocalizationFeature_BR |(البرازيل) وظائف Commerce الخاصة بالبرازيل | قيد التشغيل بشكل افتراضي |
| ريتايلادفانسيدجتيتاكسادجوستمينتفيتوري | (الهند) تطبيق GST المحسوبة لحركات البيع بالتجزئة في Retail POS إلى كشوف البيع بالتجزئة | قيد التشغيل بشكل افتراضي |
| RetailChronologicalInvoicePostingFeature_IT | (إيطاليا) تمكين فواتير البيع بالتجزئة المرحّلة من دون ترتيب زمني | قيد التشغيل بشكل افتراضي |
| RetailDiscountWithoutTaxAdjustingFeature_MX | (المكسيك) تعديل الخصم في CFDI العالمي للبيع بالتجزية | قيد التشغيل بشكل افتراضي |
| RetailFiscalIntegrationConfigurationEnhancementFeature | تجاوزات ملف التعريف الفني للتكامل المالي | قيد التشغيل بشكل افتراضي |
| RetailFiscalIntegrationConnectorLocationFeature | التكامل المالي المباشر من سجلات نقطة البيع | قيد التشغيل بشكل افتراضي |
| RetailFiscalIntegrationLocalStorageBackupEnableFeature | نسخ احتياطي للتخزين المحلي للتكامل المالي | قيد التشغيل بشكل افتراضي |
| RetailFiscalIntegrationPostponeFiscalRegistrationFeature | تسجيل المستندات المؤجل | قيد التشغيل بشكل افتراضي |
| RetailFiscalIntegrationRegistrationProcessTerminalExceptionFeature | حالة التسجيل المالي لسجلات نقطة البيع | قيد التشغيل بشكل افتراضي |
| RetailGSTInvoiceAddressTaxCalculationFeature_IN | (الهند) حساب GST بالاستناد إلى عنوان الفاتورة لأوامر التجارة الإلكترونية | قيد التشغيل بشكل افتراضي |
| RetailInvoicesDefaultSalesDocumentStatusFeature_PL | (بولندا) حالة مستند المبيعات الافتراضية‬ لفواتير البيع بالتجزئة | قيد التشغيل بشكل افتراضي |
| RetailRecalculateRoundingOfTaxBaseAmountsFeature_MX | (المكسيك) إعادة حساب التقريب لمبالغ وعاء الضريبة في الوظيفة العمومية CFDI في Retail. | قيد التشغيل بشكل افتراضي |
| RetailSupplementaryInvoiceFeature | تمكين الفواتير التكميلية‬ لحركات الدفع نقدًا والاستلام فورًا‬‬ التي تم استكمالها في متاجر البيع بالتجزئة | قيد التشغيل بشكل افتراضي |
| RetailInventoryBufferAndInventoryLevelEnableFeature   |  تمكين المخازن المؤقتة للمخزون ومستويات المخزون    |  قيد التشغيل بشكل افتراضي|
|RetailInboundOutboundInventoryValidationFeature|   تمكين التحقق من الصحة في عمليات المخزون الواردة والصادرة لنقطة البيع   |   قيد التشغيل بشكل افتراضي   |
|  RetailInventoryChannelCalculationConsolidationFeature    |  منطق التجارة الإلكترونية لحساب المخزون من جانب القناة |   قيد التشغيل بشكل افتراضي   |
|RetailInventoryAdjustmentsInPointOfSaleFeature|    تسويات المخزون في نقطة البيع   |  قيد التشغيل بشكل افتراضي  |
| RetailMultiplePickupDeliveryModeFeature |  دعم طرق تسليم انتقاء متعددة     |   إلزامي    |
|  ريتايلبرودوكتافايلابيليتيوبتيميزاتيونفيتوري |   حساب توفر المنتجات الأمثل  |  إلزامي |
|   RetailPricingDataManagerV2Feature   |   تحسين الأداء لمحرك التسعير في Commerce |   إلزامي |
|  RetailPricingPreventUnintendedRecalculationFeature   | منع حساب السعر غير المقصود لأوامر التجارة.    |  إلزامي  |
| تكامل فرق البيع بالتجزئة    |   تمكين تكامل Microsoft Teams| إلزامي   |  
| ConsumerEFDSyncProcessFeature_BR | (البرازيل) معالجة متزامنة لـ NFC-e | قيد التشغيل بشكل افتراضي |
| RetailFiscalIntegrationInternalAndExternalServicesEnableFeature | الدعم للموصلات الداخلية والخارجية في إطار عمل التكامل المالي | إلزامي |
| RetailTaxRegistrationIdEnableFeature_BR | (البرازيل) البحث عن العملاء في Retail POS بأرقام التسجيل الضريبي | إلزامي |
| RetailTaxRegistrationIdEnableFeature_IN | (الهند) البحث عن العملاء في Retail POS بأرقام التسجيل الضريبي | إلزامي |
| RetailTaxRegistrationIdEnableFeature_IT | (إيطاليا) إدارة معلومات العملاء في Retail POS | إلزامي |
| RetailTaxRegistrationIdEnableFeature_PL | (بولندا) إدارة معلومات العملاء في Retail POS | إلزامي |
| RetailUpdateReturnOriginalTransactionIdGlobalEnableFeature_IN | (GST للبيع بالتجزئة في الهند) تحديث إشعارات الدائن بمراجع إلى الفواتير الأصلية | إلزامي |
| RetailUserDefinedCertificateProfileFeature | ملفات تعريف الشهادات المعرفة من قِبل المستخدمين لمتاجر البيع بالتجزئة | إلزامي |
  

## <a name="additional-resources"></a>الموارد الإضافية

### <a name="platform-updates-for-finance-and-operations-apps"></a>تحديثات النظام الأساسي لتطبيقات التمويل والعمليات

يتضمن الإصدار 10.0.29 من Microsoft Dynamics 365 Commerce تحديثات النظام الأساسي. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.29 من تطبيقات التمويل والعمليات (أكتوبر 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md). 

### <a name="bug-fixes"></a>إصلاح الأخطاء

للحصول على معلومات حول إصلاحات الأخطاء المضمنة في كل تحديث من التحديثات التي تعد جزءًا من نسخة 10.0.29، قم بتسجيل الدخول إلى Lifecycle Services (LCS) وعرض [مقالة قاعدة المعارف](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559&dbType=3&qc=ec3e3846199f5d3a27a0c4949e3902ffdbc87560f0cf928c4838b3bdd421633c). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 وسحابات الصناعة: خطة إصدار 2 لعام 2022

هل تتساءل عن الإمكانات القادمة والتي تم إصدارها حديثًا في أيٍّ من تطبيقات العمل أو النظام الأساسي الخاص بنا؟

راجع [Dynamics 365 وسحابات الصناعة: خطة إصدار 2 لعام 2022](/dynamics365-release-plan/2022wave2/). لقد التقطنا جميع التفاصيل بشكل شامل، ومن الأعلى إلى الأسفل، في مستند واحد يمكنك استخدامه للتخطيط.

### <a name="removed-and-deprecated-features"></a>الميزات التي تمت إزالتها وإهمالها

توضح الميزات التي [تمت ازالتها أو إهمالها في Dynamics 365 Commerce](removed-deprecated-features-commerce.md) المقالة الميزات التي تمت ازالتها أو إهمالها للتجارة.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

قبل إزالة أي ميزة من المنتج، سيتم إعلان إشعار إهمال في المقال [الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Commerce](removed-deprecated-features-commerce.md) 12 شهرًا قبل الإزالة.

بالنسبة للتغييرات الفاصلة التي تؤثر فقط على وقت التحويل البرمجي، ولكنها متوافقة ثنائيًا مع بيئة الاختبار المعزولة وبيئات الإنتاج، فسيكون وقت الإهلاك أقل من 12 شهرًا. بشكل عام، هذه هي التحديثات الوظيفية التي يجب إجراؤها للمحول البرمجي.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
