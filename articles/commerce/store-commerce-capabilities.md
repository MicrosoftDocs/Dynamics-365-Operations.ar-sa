---
title: قدرات تطبيق Store Commerce
description: توضح هذه المقالة الوظيفة المتوفرة في تطبيق Store Commerce لـ Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2022-09-30
ms.openlocfilehash: 58f2ab1f913d3629de7971c8eeb2d1821161e44f
ms.sourcegitcommit: 29d9a7573bdac004726da88a9d7b2cc9c383e9ca
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788502"
---
# <a name="store-commerce-app-capabilities"></a>قدرات تطبيق Store Commerce

[!include [banner](includes/banner.md)]

تطبيق Store Commerce عبارة عن تجربة نقطة البيع (POS) الحديثة لـ Microsoft Dynamics 365 Commerce. يمكّن التطبيق الشركات من معالجة الحركات في المتجر وإدارة عمليات مكتب الدعم مثل معالجة الأوامر والمخزون. كما يتيح التطبيق للشركات إمكانية إدارة علاقات العملاء مع الولاء وقاعدة العملاء. 

يتم تشغيل تطبيق Store Commerce بواسطة Commerce Scale Unit (CSU)، ويوفر التطبيق حل قناة متعددة الاتجاهات كاملاً . على سبيل المثال، يمكن للعميل شراء منتج عبر الإنترنت واستلامه في متجر قريب، وبالتالي متابعة رحلة التسوق عبر القنوات دون فقد أية بيانات. 

يقدم هذا المقال نظرة عامة حول قدرات تطبيق Store Commerce.

## <a name="platform"></a>النظام الأساسي

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| القناة متعددة الاتجاهات | يقدم Dynamics 365 Commerce حلاً شاملاً للقناة متعددة الاتجاهات لتوحيد تجارب مركز الاتصالات والمتجر ومكتب الدعم والتجارب الرقمية. | [نظرة عامة](index.md) | [حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/dynamics-365-commerce-overview-november-2-2020) |
| التجارة بدون أجهزة ملحقة | تستضيف Commerce Scale Unit محرك التجارة بدون أجهزة ملحقة. يعمل محرك التجارة بدون أجهزة ملحقة كنقطة مركزية لمنطق كل أعمال التجارة ويؤسس حلاً كاملاً لقناة متعددة الاتجاهات. | <p>[نظرة عامة على الهندسة](commerce-architecture.md)</p><p>[بنية بدون أجهزة ملحقة](dev-itpro/retail-server-architecture.md)</p> | [حديث فني](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-commerce-architecture-overview-december-4-2020) |
| Commerce Headquarters | توفر Commerce headquarters إمكانيات مكتب الدعم التي تتيح تكوين المنتجات والموظفين وعمليات الأعمال والأسعار والوظائف الأخرى المطلوبة للأعمال. | [نظرة عامة على الهندسة](commerce-architecture.md) | |
| نقطة البيع (POS) | يعتبر تطبيق Store Commerce تجربة POS لـ Dynamics 365 Commerce. وهو يوفر إمكانيات نقطة البيع الغنية بالميزات والشاملة التي تساعد موظفي المبيعات وموظفي الكاشير والمديرين على توفير خدمة عملاء فائقة. بالإضافة إلى ذلك، يوفر خيارات توزيع متعددة لبائعي التجزئة، ويساعد على تحسين الأداء، كما يوفر إدارة مُحسّنة لدورة حياة التطبيقات (ALM). | [تطبيق Store Commerce](dev-itpro/store-commerce.md) | <p>[حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/modernize-the-dynamics-365-commerce-in-store-technology-using-the-new-store-commerce-app-march-30-2022)</p><p>[الفيديو](https://youtu.be/7B332XH_zfs)</p><p>[ترحيل من MPOS لـ Store Commerce](dev-itpro/pos-extension/migrate-mpos-store-commerce.md)</p> |
| التوزيع عبر السحابة | يمكن توزيع مثيلات متعددة من وحدات Commerce Scale Unit لتوزيع الحمل والتقارب الجغرافي. | [التوزيع عبر السحابة](../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md) | |
| التوزيع المحلي | باستخدام توزيع بيانات العمل المحلي، يمكن أن يكون لعملاء Commerce ملكية وإدارة بصورة أكبر لبيئات Dynamics 365. | [النشر المحلي](../fin-ops-core/dev-itpro/deployment/deploy-retail-onprem.md) | |

## <a name="device-management"></a>إدارة الجهاز

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| عوامل نماذج متعددة | يتم دعم تطبيق Store Commerce على العديد من عوامل نماذج الأجهزة، مثل أجهزه الكمبيوتر والأجهزة اللوحية والأجهزة المحمولة. وتقوم واجهة المستخدم (UI) المستجيبة بتمكين التخطيط ليتم تلقائيًا تغيير حجمه وضبطه وفق حجم الشاشة. | [التكوينات المرئية](pos-screen-layouts.md) |  |
| عبر الأنظمة الأساسية | تطبيق Store Commerce مدعوم على الويب وأنظمة Windows وiOS وAndroid الأساسية. | [الأنظمة الأساسية](dev-itpro/hybridapp.md) | |
| علامة تجارية | يتيح لك مصمم الشاشة تخصيص تخطيطات الشاشة لتفي بمتطلبات الأعمال الخاصة بك. بالإضافة إلى ذلك، يمكن إنشاء السمات والتخطيطات والألوان والصور استنادًا إلى أدوار الموظفين ويمكن بعد ذلك مشاركتها عبر المستخدمين لتناسق العلامة التجارية وسهوله الاستخدام. | [التكوينات المرئية](pos-screen-layouts.md) | [الفيديو](https://www.youtube.com/watch?v=ldqCw2wf5fY) |
| المخطط | يتم دعم تخطيطات المتجر المختلفة، استنادًا إلى توفر الشبكة. | <p>[المخطط](dev-itpro/retail-modern-pos-architecture.md)</p><p>[مخطط معلومات رسومية](dev-itpro/retail-in-store-topology.md)</p> | |
| إدارة متعددة الأجهزة | يمكن إدارة العديد من الأجهزة عبر المتاجر بسهولة من Commerce headquarters. | [تنشيط](set-up-activation-accounts-validate-devices-hq.md) | [حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/commerce-mass-deployment-with-sccm-system-center-configuration-manager-october-6-2022) |

## <a name="employee-management"></a>إدارة الموظفين

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| تسجيل الدخول | يمكن أن يكون لكل موظف متجر إمكانية تسجيل دخول مخصص. تتضمن أنواع تسجيل الدخول اسم المستخدم، والرمز الشريطي، وقارئ الشريط المغناطيسي (MSR) والمقاييس الحيوية، وAzure Active Directory (Azure AD). | <p>[Azure AD](aad-pos-logon.md)</p><p>[تسجيل الدخول الموسع](extended-logon.md)</p> | |
| الأذونات | يتم دعم مستويات مختلفة من الأذونات للموظفين، مثل الإذن بإنشاء أوامر وأذونات بتحرير الأوامر. | [الأذونات](tasks/create-pos-permission-groups.md) | |
| إدارة الوقت والحضور | يمكن إدارة الحضور باستخدام وظيفة ساعة الوقت. يمكن معالجة بيانات الحضور في كشف الرواتب باستخدام تطبيق Dynamics 365 Human Resources. | [إدارة الوقت](retail-time-attendance.md) | |
| عمولة المبيعات | يمكن تعقب المبيعات من خلال ممثل المبيعات لحساب العمولات أو غير ذلك من المكافآت التشجيعية. | [العمولة](pos-sales-groups-track-commissions.md) | |

## <a name="merchandising"></a>ترويج البضائع

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| إدارة المجموعات المنوعة | يمكن لمديري ترويج البضائع فرز المنتجات بحيث تكون متوفرة للبيع في قناة معينه وخلال فترة زمنية محددة. | [عمليات الفرز](assortments.md) | |
| الكتالوجات | يمكن لمديري ترويج البضائع إدارة الكتالوجات لتحديد المنتجات التي ترغب في تقديمها بالأسعار الخاصة بالكتالوج. | [الكتالوجات](/dynamicsax-2012/appuser-itpro/about-retail-product-catalogs) | |
| إدارة الفئات والمنتجات | في Commerce headquarters، يمكن لمديري ترويج البضائع إنشاء منتجات لها متغيرات، وسمات، ووحدة قياس، وهكذا. ويمكنهم أيضًا تحديد التدرج الهرمي للفئات لتنظيم المنتجات. | [المنتج](retail-hierarchies.md) | |
| المجموعات | يمكن لمديري ترويج البضائع تجميع المنتجات بحيث يتم بيعها كمجموعة أو مجموعة مواد. | [المجموعات](/dynamicsax-2012/appuser-itpro/about-setting-up-retail-product-kits) | |
| أكواد المعلومات | يمكن استخدام أكواد المعلومات لمطالبة الصراف بإدخال معلومات أثناء تنفيذ إجراءات مختلفة بنقطة البيع، مثل مبيعات الصنف أو مرتجعات الصنف أو تحديد العملاء. | [أكواد المعلومات](/dynamicsax-2012/appuser-itpro/about-info-codes-retail) | |
| الأصناف المرتبطة | يمكن استخدام الأصناف المرتبطة للبيع الإضافي للمنتجات عند إضافة صنف إلى الحركة. | [الأصناف المرتبطة](/dynamicsax-2012/appuser-itpro/set-up-products-for-cross-selling-and-up-selling) | |
| الضمانات | يمكن بيع الضمانات الموسعة مع المنتجات. | [الضمان](extended-warranty.md) | |
| طباعة التسمية | يمكن إنشاء التسميات التي تحتوي على معلومات المنتج مثل رقم الدفعة والرقم المسلسل وتاريخ انتهاء الصلاحية. | [طباعة التسمية](/dynamicsax-2012/appuser-itpro/create-and-print-labels-overview) | |

## <a name="assisted-selling"></a>البيع المساعد

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| استعراض المنتج | استعراض المنتجات حسب الفئة. | [التدرج الهرمي للمنتجات](retail-hierarchies.md) | |
| البحث عن منتج | يمكن البحث عن منتجات حسب الاسم، وتحسين عمليات البحث باستخدام سمات المنتج مثل العلامة التجارية والسعر والمادة. يتم تشغيل هذه القدرة بواسطة خدمة Azure Cognitive Search. | [البحث المشغل في السحابة](cloud-powered-search-overview.md) | |
| صفحة تفاصيل المنتج‬ | يمكن أن تتضمن صفحات تفاصيل المنتج الثري الصور والوصف وسمات المنتج والمنتجات الموصى بها. يتم تشغيل التوصيات بواسطة خدمة التوصيات. | | |
| مقارنة المنتجات | يمكن مقارنة منتجات متعددة، ومساعدة العملاء على اختيار منتج واحد وإضافته إلى حركة. | | |
| ممر لا نهاية له | يمكن البحث بسهولة في المخزون في المتاجر الأخرى، وإنشاء الأوامر. | [بحث في المخزون](pos-inventory-lookup-operation.md) | <p>[حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[الفيديو](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| التوصيات | البيع الإضافي والبيع التكميلي للمنتجات باستخدام خدمة التوصيات. تستخدم هذه الخدمة تقنية حاصلة على براءة اختراع لاقتراح التوصيات، وذلك استنادًا إلى اتجاهات الشراء، وخصائص مثل ما وصل مؤخرًا، والمظهر المشابه والأعلى مبيعًا. تتوفر هذه التوصيات في صفحات تفاصيل المنتج وصفحة **تفاصيل العميل** وصفحة **الحركات**. | [التوصيات](product-recommendations.md) | [حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-recommendations-march-2-2021) |

## <a name="customer-relationship"></a>علاقة العملاء

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| إدارة العملاء | إنشاء حسابات العميل وتحريرها وإدارتها. يمكن إدارة حسابات العملاء في وضع المزامنة لتجنب المعالجة في الوقت الحقيقي. | [الإدارة](customer-mgmt-stores.md) | |
| سمات العملاء | يمكّن إطار عمل سمات العميل من التقاط البيانات الإضافية المتعلقة بالعميل بناء على متطلبات الأعمال. | [السمات](dev-itpro/customer-attributes.md) | |
| صفحة تفاصيل العميل | توفر صفحة تفاصيل العميل الثرية عرض قناة متعددة الاتجاهات لتفاعلات العميل عبر كافة القنوات. وتتضمن هذه التفاعلات عمليات الشراء وقوائم الأمنيات ونقاط الولاء. | | |
| البحث عن العملاء المشغل في السحابة | يمكن البحث عن العملاء حسب الاسم ورقم الهاتف وعنوان البريد الإلكتروني وبطاقة الولاء والعنوان وما إلى ذلك. | [البحث المشغل في السحابة](pos-search-improvements.md#customer-search) | |
| الولاء والمكافآت | يمكن للعملاء ربط برامج الولاء والحصول على نقاط الولاء واسترجاعها عبر القنوات. | [الولاء](set-up-customer-loyalty-program.md) | [الفيديو](https://www.microsoft.com/en-us/videoplayer/embed/RE5c2wW) |
| قاعدة العملاء | يمكن إدارة العملاء الأساسيين باستخدام دفتر عميل، وتعقب الأنشطة والملاحظات في ملف تعريف العميل. يتيح تكامل Dynamics 365 Customer Insights لموظفي المتجر الحصول على رموز حول الإجراء الأفضل التالي لكل عميل. | [قاعدة العملاء](clienteling-overview.md#activities-and-notes) | [الفيديو](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSP) |

## <a name="pricing-and-discounts"></a>التسعير والخصومات

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| اتفاقيات تجارية | يمكن لمديري الأسعار استخدام اتفاقيات تجارية لتحديد أسعار خاصة، استنادًا إلى الصفقات طويلة الأجل للعملاء المحددين. | [التسعير](price-management.md)| [الفيديو](https://www.youtube.com/watch?v=r2VD8IxHesM) |
| اتفاقيات البيع | ويمكن لمديري الأسعار استخدام اتفاقيات المبيعات لتحديد الأسعار المستندة إلى العقد في سيناريوهات متاجرة عمل-عمل (B2B). | [التسعير](price-management.md) | |
| تعديلات الأسعار | يمكن لمديري الأسعار استخدام إمكانية تعديلات الأسعار لإنشاء وتعقب وإدارة فروق الأسعار بالانخفاض للمنتجات الخاصة بهم بمرور الوقت. | [تعديلات الأسعار](price-adjustments-discounts.md) | |
| الخصومات | يمكن لمديري الأسعار إعداد أنواع عديدة من الخصومات لتشغيل مجموعة متنوعة من الترقيات. هذه الخصومات تتضمن الخصومات البسيطة وخصومات الكمية وخصومات الحد والمنتجات المختلفة والمطابقة والخصومات المستندة إلى طريقة الدفع‬، وخصومات الشحن. | [الخصومات](retail-discounts-overview.md) | |
| القسائم | يمكن لمديري الأسعار إعداد أكواد القسيمة أو الأكواد الشريطية وربطها بالخصومات وتوزيعها علي العملاء. يمكن أن يقوم موظفو المبيعات بإضافة قسائم إلى حركات المبيعات أو إزالتها. | [القسائم](coupons.md) | |
| مجموعات الأسعار | يمكن لمديري الأسعار استخدام إمكانيه مجموعة الأسعار لتحديد الأسعار السياقية، استنادًا إلى القنوات أو الكتالوجات أو التبعيات أو برامج الولاء. | [التسعير](price-management.md) | |
| العروض الترويجية المتوفرة | يمكن لموظفي المبيعات البحث بسهولة عن العروض الترويجية المتاحة للمنتجات في المتجر، والمنتجات التي تمت إضافتها إلى الحركة وما إلى ذلك. | [وظائف الأسعار](pos-pricing-functions.md) | |
| عمليات التحقق من الأسعار | يمكن لموظفي المبيعات مراجعة أسعار المبيعات النشطة بسرعة في المتجر. | [وظائف الأسعار](pos-pricing-functions.md) | |
| تجاوز السعر | يمكن لموظفي المبيعات الذين يمتلكون الأذونات المطلوبة تجاوز الأسعار التي تم تكوينها بواسطة النظام أو المحسوبة. | [وظائف الأسعار](pos-pricing-functions.md) | |
| الخصومات اليدوية | يمكن لموظفي المبيعات الذين يمتلكون الأذونات المطلوبة تطبيق الخصومات اليدوية على حركات المبيعات أو بنود المبيعات. | [وظائف الأسعار](pos-pricing-functions.md) | |

## <a name="electronic-payments"></a>المدفوعات الإلكترونية

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| الدائن والمدين | يدعم تطبيق Store Commerce مدفوعات البطاقات المدينة والدائنة الرئيسية من خلال بوابة الدفع Adyen وتنفيذ الأمر من خلال PayPal. تسمح حزمة SDK للمدفوعات باتصالات البوابة الخارجية التي يتم دعمها بواسطة عمليات تكامل بائع البرامج المستقل (ISV). | <p>[Adyen](dev-itpro/adyen-connector.md?tabs=10-0-23)</p><p>[PayPal](paypal.md)</p><p>[المدفوعات](payment-methods.md)</p> | <p>[حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-configuration-february-9-2021)</p><p>[حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-overview-processing-february-4-2021)</p> |
| دعم المحفظة الرقمية | يدعم تطبيق Store Commerce المدفوعات من خلال طرق دفع المحفظة الرقمية التي لا تستخدم نطاقات رقم التعريف البنكي (BIN) كما تفعل البطاقات المدينة والدائنة التقليدية. يمكن تعيين طرق الدفع إلى مدفوعات المحفظة الرقمية مثل Adyen. | [المحفظة](wallets.md) | |
| دعم بطاقات الهدايا | بطاقة هدايا Dynamics 365 برقم التعريف البنكي، وحلول القيمة المخزنة (SVS)، وبطاقات هدايا Givex. يمكن شراء بطاقات الهدايا واسترجاعها بأحد الأوامر. | [بطاقات الهدايا](dev-itpro/gift-card.md) | [حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/d365-commerce-internal-gift-cards-november-16-2021) |
| الحماية من الاحتيال | يساعدك حل Dynamics 365 Fraud Protection على منع الأنشطة الاحتيالية وتحديد الأماكن التي قد يتم فيها الاحتيال بشكل غير ملحوظ. | [Fraud protection](dev-itpro/dfp.md) | [الفيديو](https://www.youtube.com/watch?v=j_1nEiq3LfM) |

## <a name="taxes-and-charges"></a>الضرائب والرسوم

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| الضرائب | يدعم تطبيق Store Commerce العديد من أنواع الضرائب غير المباشرة، مثل ضريبة المبيعات، وضريبة القيمة المضافة (VAT)، وضريبة السلع والخدمات (GST)، والرسوم على أساس الوحدة، وضريبة الخصم. | [الضرائب](/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json) | |
| التكاليف | يمكن تكوين الرسوم على مستوى البند، وعلى مستوى العنوان، وكرسوم تلقائية، وعلى حسب القناة وهكذا. | [المصاريف](omni-auto-charges.md) | |

## <a name="order-processing-and-fulfillment"></a>تنفيذ الأوامر ومعالجتها

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| إنشاء أمر | يمكن إنشاء أمر للشحن أو التسليم في متجر قريب. يمكن توفير الفترات الزمنية للتسليم. | [نظرة عامة](customer-orders-overview.md) | |
| تعديل الأمر | يمكن تعديل الأمر وإرجاعه وإلغاؤه وما إلى ذلك. | <p>[إلغاء](customer-orders-overview.md#cancel-a-customer-order)</p><p>[مرتجعات](pos-returns.md)</p> | |
| بحث | يمكن البحث عن الأوامر وتصفيتها باستخدام المعلومات الخاصة بالأمر. | [بحث](enhancedorderrecall.md) | |
| سمات الأوامر | يمكّن إطار عمل سمة الأمر من التقاط المعلومات الإضافية المتعلقة بالأمر بناء على متطلبات الأعمال. | [السمات](dev-itpro/order-attributes.md) | |
| تسليم مباشر | يمكن تمييز الأصناف للتسليم المباشر بواسطة أحد الموردين إلى عنوان العميل. يُعرف التسليم المباشر أيضًا بالشحن المباشر. | [تسليم مباشر](/dynamics365/supply-chain/sales-marketing/tasks/ship-orders-direct-deliveries) | |
| عرض الأسعار | يمكن لموظفي المتجر إنشاء عروض أسعار للعملاء، كما يمكنهم تحديد سعر خاص وخصومات يدوية وتاريخ صلاحية عرض الأسعار. | [عرض الأسعار](/dynamics365/supply-chain/sales-marketing/tasks/create-edit-sales-quotations) | |
| التنفيذ | يمكن أن تقوم المتاجر بانتقاء الأوامر وتعبئتها وشحنها. يمكن إضافة إيصال تعبئة إلى الحزم الجاهزة للشحن. | [التنفيذ](order-fulfillment-overview.md) | <p>[حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-supporting-buy-online-pickup-in-store-curbside-with-dynamics-365-commerce-pos-february-3-2021)</p> <p>[الفيديو](https://www.microsoft.com/videoplayer/embed/RE5bRXE)</p>|
| إدارة الأمر الموزع | يدعم تطبيق Store Commerce تحسين تنفيذ الأمر الذكي حيث يمكن تكوين إستراتيجيات العمل استنادًا إلى طبيعة العمل ونوع العميل وأصل الأمر وطريقة تسليم الأمر. | [نموذج كائن المستند](dom.md) | [الفيديو](https://www.microsoft.com/en-us/videoplayer/embed/RE5bRYl)|

## <a name="inventory-management"></a>إدارة المخزون

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| توزيع المشتريات | تسهيل توزيع المخزون المتوفر من مركز توزيع إلى متاجر أو مستودعات متعددة. | [توزيع المشتريات](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| توزيع البضائع | تسهيل توزيع المخزون في أوامر الشراء الواردة إلى متاجر أو مستودعات متعددة. | [توزيع البضائع](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| المخزون الوارد | استلام المخزون من مورد عبر أمر شراء أو من مستودع آخر باستخدام أمر تحويل. إنشاء أمر شراء وارد أو طلب أمر تحويل. | [وارد](pos-inbound-inventory-operation.md) | <p>[حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[الفيديو](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| المخزون الصادر | شحن المخزون إلى مستودع آخر بواسطة أمر تحويل، وإنشاء طلب أمر تحويل صادر. | [صادر](pos-outbound-inventory-operation.md) | <p>[حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[الفيديو](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| بحث في المخزون | فحص المخزون الفعلي للمنتجات عبر المتاجر والمستودعات، وفحص المخزون المتوفر حسب التعهد (ATP) حسب التواريخ المستقبلية. | [بحث في المخزون](pos-inventory-lookup-operation.md) | <p>[حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[الفيديو](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| تسوية المخزون | تعديل المخزون داخل أو خارج مستودع متجر لتلبية متطلبات العمل المحددة بدون استخدام عملية بيع أو إيصال أو إعادة الجرد. | [تسوية المخزون](work-with-store-inventory.md) | <p>[حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[الفيديو](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| عمليات جرد المخزون | جرد المخزون الفعلي، وتعديل مخزون محاسبة النظام ليطابقه. | [الجرد](work-with-store-inventory.md) | <p>[حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[الفيديو](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)<p> |
| حركة المخزون | نقل المخزون بين المواقع في أحد المتاجر. | [الحركة](work-with-store-inventory.md) | <p>[حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[الفيديو](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |

## <a name="financials"></a>الماليات

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| إدارة النقد | يدعم تطبيق Store Commerce إدارة النقد وطرق الدفع المحددة الأخرى في المتجر. بالإضافة إلى ذلك، يمكن تمكين تسوية الورديات في المتجر لقدرات إدارة النقد المتقدمة. | [النقد](cash-mgmt.md) | |
| القوائم المالية والتسوية المالية | يتم تسجيل الحركات التعاملية والنقدية لمتجر في Commerce headquarters من خلال عمليات ترحيل كشف الحساب. | [كشوف الحسابات](retail-statements.md) | |
| حركات الإيرادات والمصروفات | معالجة المصروفات النثرية في المتجر، وتسجيل الإيراد الذي لا يأتي بالطريقة التقليدية، مثل المال المفقود وتم العثور عليه، ومشاركة الإيراد من مقهى في ساحة الانتظار وخدمات تنظيف السجاد. | [كشوف الحسابات](retail-statements.md) | |
| مدفوعات الفاتورة | التقاط المدفوعات مقابل الفواتير. | [الفاتورة](payinvoice.md) | |

## <a name="employee-productivity"></a>إنتاجية الموظف

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| إدارة المهام | إنشاء قوائم المهام والمهام وتعيينها للمتاجر والموظفين. تعقب حالة المهام عبر المتاجر. يتوفر التكامل السلس مع Microsoft Teams. | <p>[إدارة المهام](task-mgmt-overview.md)</p><p>[Microsoft Teams](commerce-teams-integration.md)</p> | [الفيديو](https://www.youtube.com/watch?v=ES1whB4C2lU) |

## <a name="hardware-and-peripherals"></a>الأجهزة والأجهزة الطرفية

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| توصيل الأجهزة الطرفية | توصيل الأجهزة الطرفية مثل الطابعات والأدراج النقدية والماسحات الضوئية وأجهزة الدفع إلى محطة POS طرفية. | [الأجهزة الطرفية](retail-peripherals-overview.md) ||
| مشاركة الأجهزة الطرفية | يمكن مشاركة طابعات الاستلام والأدراج النقدية وأجهزة الدفع بين العديد من الأجهزة الطرفية بتوصيلها بمحطة أجهزة مشتركة. | <p>[‏محطة الأجهزة](retail-peripherals-overview.md) ||
| محاكي الأجهزة الطرفية ونقطة البيع | يدعم محاكي الأجهزة الطرفية اختبار السيناريوهات التي عادةً ما تتطلب وجود أجهزة طرفية مادية لنقطة البيع. يشتمل أيضًا على محاكي POS يمكن استخدامه لاختبار توافق الأجهزة الطرفية المادية دون الحاجة إلى توزيع عميل POS. | [المحاكي](dev-itpro/retail-peripheral-simulator.md) | |

## <a name="receipts"></a>الإيصالات

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| طباعة الإيصالات | يمكن طباعة أنواع متعددة من الإيصالات، مثل إيصالات المبيعات وإيصالات البطاقات المدينة وإيصالات الهدايا والفواتير، بشكل افتراضي أو بعد تأكيد الصراف عند السحب. كما يمكن إعادة الطباعة من دفتر اليومية. | [الطباعة](receipt-templates-printing.md) | |
| إرسال الإيصالات بالبريد الإلكتروني | يمكن إرسال الإيصالات بالبريد الإلكتروني من نقطة البيع بعد اكتمال السحب. | [البريد الإلكتروني](email-receipts.md) | |
| تصميم الإيصالات | يمكن تخصيص إيصالات المتاجر بحيث تُظهر البيانات والتخطيطات المناسبة لبائع التجزئة ونوع الحركة. يمكن أيضًا توسيع الإيصالات بحيث تُظهر البيانات المخصصة المطلوبة من قبل بائع التجزئة. | [التصميم](receipt-templates-printing.md) | |

## <a name="offline-support"></a>الدعم عند عدم الاتصال

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| وضع عدم اتصال سلس | يتيح لك وضع عدم الاتصال السلس الاستمرار في العمل حتى عند تحديد الاتصال بالإنترنت أو عدم توفره. يساعدك استبعاد البيانات في تقليل حجم بيانات قواعد البيانات غير المتصلة وزيادة الأداء. | [غير متصل](pos-operations.md) | |
| التبديل المستند إلى الأداء | التبديل إلى وضع عدم الاتصال عند اكتشاف انخفاض الأداء. | [غير متصل](dev-itpro/implementation-considerations-offline.md) | [الفيديو](https://youtu.be/sQU-2pgHToI) |
| لوحة معلومات دون اتصال | تُظهر لوحة معلومات **حالة وضع عدم الاتصال** حالة وضع عدم الاتصال والأخطاء وتفاصيل البيانات الخاصة بكل جهاز. وبالتالي، يكون من السهل إدارة حالة أجهزة متعددة. | [غير متصل](dev-itpro/implementation-considerations-offline.md) | [الفيديو](https://youtu.be/sQU-2pgHToI)|

## <a name="extensibility"></a>القابلية للتوسعة

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| Commerce Headquarters | يمكن تخصيص حلول Commerce headquarters عن طريق إضافة عمليات الأعمال أو تعديلها. تدعم Commerce headquarters استخدام بيانات التعريف ونموذج ملحق يستند إلى الأكواد لإضافة وظيفة مخصصة. يمكن دمجه بسهولة في الحلول الخارجية. | [نظرة عامة](dev-itpro/extend-customer-cdx-package.md) | [حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-unlock-the-power-of-dynamics-365-commerce-commerce-extensibility-overview-february-23-2021) |
| التجارة بدون أجهزة ملحقة | يمكن استخدام إطار عمل واجهة برمجة تطبيقات القناة متعددة الاتجاهات القابلة للتوسيع لتخصيص منطق عمل وإضافته. واجهات برمجة التطبيقات التي تحتوي على معالجات الطلبات وأنماط ملحقات المُشغلات المسبقة واللاحقة. | [CSU](dev-itpro/retail-server-customer-consumer-api.md) | [حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Commerce SDK | تتضمن Commerce SDK التعليمات البرمجية ونماذج التعليمات البرمجية والقوالب والأدوات المطلوبة لتوسيع وظيفة Dynamics 365 Commerce أو تخصيصها. يتم نشر SDK في مستودعات مختلفة في GitHub، وفقًا لمكونات الملحق. | [SDK](dev-itpro/retail-sdk/sdk-github.md) | [حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| نقطة البيع | يمكن تمديد تطبيق Store Commerce بشكل مستقل باستخدام ميزة ملحق نقطة البيع في Commerce SDK. يدعم إطار العمل تخصيص تجربة المستخدم (UX) ومهام سير العمل ومنطق العمل. | [POS](dev-itpro/pos-extension/pos-extension-overview.md) | [حديث فني](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |

## <a name="reporting"></a>إعداد التقارير

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| تقارير المبيعات | تتوفر لمديري المتاجر تقارير المبيعات حسب الموظفين والسجل ونوع الدفع والمرتجعات والمنتج وما إلى ذلك. يمكن للمديرين عرض هذه التقارير، واستخدامها لتخصيص العمولة وتحديد اتجاهات المنتج. | | |

## <a name="diagnostics"></a>عمليات تشخيص

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| Operational Insights | تتوفر مقاييس أداء وموثوقية حالة الخدمة المختارة للمتجر في اشتراك Application Insights الخاص بالعميل. تتوفر إمكانيات التنبيه والمراقبة المتقدمة. | | |
| فحص الصحة | يمكن التحقق من توفر الأجهزة الطرفية المتصلة بنقطة بيع بواسطة تشغيل عملية فحص الصحة. يمكن بعد ذلك إصلاح مشكلات الأجهزة الطرفية الفردية والتحقق منها. | [فحص الصحة](pos-healthcheck.md) | [الفيديو](https://www.youtube.com/watch?v=RfPDNmnqYvY) |

## <a name="globalization"></a>العولمة

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| الدعم متعدد الأسواق | يتم دعم الميزات الخاصة بالسوق مثل التكامل المالي وضريبة السلع والخدمات (GST) والفوترة المتقدمة والدفعات المقدمة خارج الصندوق. وتغطي هذه الإمكانية العديد من الأسواق في أوروبا و‏‫الأمريكتين‬ وروسيا وآسيا والمملكة العربية السعودية وهكذا. | [العولمة](localizations/fiscal-integration-for-retail-channel.md) | |

## <a name="compliance"></a>توافق

| القدرة | ‏‏الوصف‬ | الوثائق | محتوى إضافي |
|---|---|---|---|
| معايير Microsoft | يفي تطبيق Store Commerce بمعايير Microsoft للأمان والخصوصية وإمكانية وصول ذوي الاحتياجات الخاصة والقانون العام لحماية البيانات (GDPR) وحدود بيانات الاتحاد الأوروبي (EU) وما إلى ذلك. | | |

