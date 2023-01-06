---
title: نظرة عامة على Dynamics 365 Payment Connector لـ Adyen
description: يوفر هذا المقال نظرة عامة على موصل دفع Microsoft Dynamics 365لـ Adyen.
author: rassadi
ms.date: 11/16/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.openlocfilehash: 58d88e023b73ce19331bd6f54644a62d8f6f35af
ms.sourcegitcommit: 3aa3dedc3123cb079614762e2718841c2f7d7d35
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812076"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>نظرة عامة على Dynamics 365 Payment Connector لـ Adyen

[!include [banner](../includes/banner.md)]

يقدم هذا المقال نظرة عامة علي موصل دفع Microsoft Dynamics 365 لـ Adyen ويشتمل على قائمة شاملة بالوظائف والميزات المدعومة. تغطي المقالات ذات الصلة إعداد Adyen، وتكوين الموصل والأسئلة المتداولة وإرشادات استكشاف الأخطاء وإصلاحها لبعض المشكلات الشائعة.

## <a name="key-terms"></a>المصطلحات الأساسية

| المصطلح | ‏‏الوصف‬ |
|---|---|
| موصل المدفوعات | ملحق يسهل الاتصال بين Microsoft Dynamics 365 Commerce (والمكونات المقترنة) وخدمة دفع. تم تنفيذ الموصل الموضح في هذا المقال باستخدام مجموعة تطوير برامج (SDK) المدفوعات القياسية. |
| البطاقة موجودة | يشير إلى معاملات الدفع حيث يتم تقديم بطاقة فعلية واستخدامها في موصل وحدة طرفية للدفع بنقطة بيع Dynamics 365. |
| البطاقة غير موجودة | يشير إلى معاملات الدفع في حالة عدم وجود بطاقة فعلية، مثل سيناريوهات مركز الاتصال أو التجارة الإلكترونية. في هذه السيناريوهات، يتم إدخال المعلومات المتعلقة بالدفع يدويًا على موقع التجارة الإلكترونية، أو في تدفق مركز الاتصال، أو على نقطة البيع أو محطة الدفع. |

## <a name="supported-features-functionality-versions-and-terminals"></a>الوحدات الطرفية والإصدارات والوظائف والميزات المدعومة

موصل دفع Dynamics 365 الجاهز لـ Adyen يستخدم مجموعة تطوير برامج (SDK) المدفوعات القياسية. وبالتالي، لا يكون لديه قدرات خاصه لا تتوفر أيضًا لموصلات الدفع الأخرى.

### <a name="supported-versions"></a>الإصدارات المدعومة

#### <a name="microsoft-dynamics-365-supported-versions"></a>إصدارات Microsoft Dynamics 365 المدعومة
موصل دفع Dynamics 365 لـ Adyen المقدم من الطرف الأول مدعوم في Microsoft Dynamics 365 Finance الإصدار 8.1.3 (يناير 2019) أو الأحدث، وفي Microsoft Dynamics 365 Retail الإصدار 8.1.3 أو الأحدث. ومع ذلك، لا يزال بإمكان الجهات الخارجية تطوير موصلات دفع أخرى لـ Adyen للإصدارات السابقة من Microsoft Dynamics 365.

#### <a name="supported-adyen-firmware-versions"></a>إصدارات برامج Adyen الثابتة المدعومة

توضح القائمة أدناه الإصدارات الأدنى والأقصى لبرامج Adyen الثابتة المدعومة لكل إصدار من إصدارات Microsoft Dynamics 365 Retail POS.

---

# <a name="10025"></a>[10.0.25](#tab/10-0-25)
### <a name="dynamics-365-retail-pos-version-10025"></a>الإصدار 10.0.25 من Dynamics 365 Retail POS
| الحد الأدنى لإصدار برامج Adyen الثابتة | الحد الأقصى لإصدار برامج Adyen الثابتة |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_73p6 |

# <a name="10026"></a>[10.0.26](#tab/10-0-26)
### <a name="dynamics-365-retail-pos-version-10026"></a>الإصدار 10.0.26 من Dynamics 365 Retail POS
| الحد الأدنى لإصدار برامج Adyen الثابتة | الحد الأقصى لإصدار برامج Adyen الثابتة |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10027"></a>[10.0.27](#tab/10-0-27)
### <a name="dynamics-365-retail-pos-version-10027"></a>الإصدار 10.0.27 من Dynamics 365 Retail POS
| الحد الأدنى لإصدار برامج Adyen الثابتة | الحد الأقصى لإصدار برامج Adyen الثابتة |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10028"></a>[10.0.28](#tab/10-0-28)
### <a name="dynamics-365-retail-pos-version-10028"></a>الإصدار 10.0.28 من Dynamics 365 Retail POS
| الحد الأدنى لإصدار برامج Adyen الثابتة | الحد الأقصى لإصدار برامج Adyen الثابتة |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p22 |

# <a name="10029"></a>[10.0.29](#tab/10-0-29)
### <a name="dynamics-365-retail-pos-version-10029"></a>الإصدار 10.0.29 من Dynamics 365 Retail POS
| الحد الأدنى لإصدار برامج Adyen الثابتة | الحد الأقصى لإصدار برامج Adyen الثابتة |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

# <a name="10030"></a>[10.0.30](#tab/10-0-30)
### <a name="dynamics-365-retail-pos-version-10030"></a>الإصدار 10.0.30 من Dynamics 365 Retail POS
| الحد الأدنى لإصدار برامج Adyen الثابتة | الحد الأقصى لإصدار برامج Adyen الثابتة |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

---

> [!NOTE]
> قد تصدر Adyen إصدارات ثانوية بعد قيام Microsoft باختبار الإصدار الرئيسي. وطالما أن هناك إصدارًا رئيسيًا مدعومًا، فمن الضروري أن يكون لديك تحديثات إصدار ثانوي داخل نفس الإصدار الرئيسي. وعادة ما تكون هذه التحديثات إصلاحات مستهدفة بشكل كبير ولا تفي بالشريط لإعادة الاختبار الكامل، طالما أن إصدار البرنامج الثابت الرئيسي نفسه تم اختباره مسبقًا. يجب ألا تتجاوز التحديثات الحد الأقصى لإصدار البرامج الثابتة لـ Adyen الواردة في الوثائق. 
>
> يتطلب الترحيل من إصدار البرنامج الثابت لـ Adyen قبل الإصدار 53 إلى الإصدار 53، قاعدة معارف نقطة البيع **4577957** للتحديثات الشهرية الخاصة بـ Commerce، إصدارات 10.0.11 إلى 10.0.14. إذا كان أحد هذه الإصدارات قيد الاستخدام ولا يتضمن الإصلاح العاجل، فلن تسمح الترقية اللاحقة للوحدة الطرفية إلا بالمدفوعات عبر NFC. يعمل تطبيق الإصلاح العاجل على نقطة البيع على حل هذه المشكلة. في حالة ما إذا كان إصدار نقطة البيع أقدم من إصدار 10.0.11، فقم بتقديم طلب دعم مع التنويه على أن إصلاح قاعدة المعارف **4577957** مطلوب لـ MPOS خارج الخدمة.
> 
> بالنسبة لإصدارات البرامج الثابتة لـ Adyen من 59p7 وحتى 62p9، تتطلب العملية **السيولة النقدية لبطاقة الهدايا** إدخال رمز PIN مرتين في السيناريوهات التي يتم فيها إدخال بطاقة الهدايا يدويًا. لا تتم إعاده إنتاج هذه المشكلة عندما يتم تمرير بطاقة الهدايا. تقوم Adyen بالتحقق من الأمر. 

### <a name="supported-payment-terminals"></a>الوحدات الطرفية للدفع المدعومة
يستفيد موصل دفع Dynamics 365 لـ Adyen من [واجهة برمجة التطبيقات الوحدات الطرفية لدفع Adyen](https://www.adyen.com/blog/introducing-the-terminal-api) التشخيصية للجهاز. وهو يدعم كافة الوحدات الطرفية للدفع التي تدعمها واجهة برمجة التطبيقات (API) هذه. للحصول على قائمة كاملة بالوحدات الطرفية للدفع المدعومة، قم بزيارة [الوحدات الطرفية لنقطة بيع Adyen](https://www.adyen.com/pos-payments/terminals).

يصف الفيديو التالي قدرات الوحدة الطرفية لدفع Castles SE1 بنظام Android.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5bKeM]

### <a name="supported-payment-instruments"></a>أدوات الدفع المدعومة

#### <a name="supported-debit-and-credit-cards"></a>البطاقات المدينة والدائنة المدعومة

| العلامة التجارية | المتغير | البطاقة موجودة | التجارة الإلكترونية | مركز الاتصال |
|---|---|:-:|:-:|:-:|
| بطاقة ماستر كارد | دائن‬ | ✔ | ✔ | ✔ |
| بطاقة ماستر كارد | مدين | ✔ | ✔ | ✔ |
| بطاقة ماستر كارد | مكافأة بنك ألفا | ✔ | ✔ | ✔ |
| بطاقة ماستر كارد | Apple Pay | ✔ |  |  |
| بطاقة ماستر كارد | Samsung Pay | ✔ |  |  |
| بطاقة ماستر كارد | Maestro | ✔ | ✔ | ✔ |
| بطاقة ماستر كارد | Maestro Samsung Pay | ✔ |  |  |
| بطاقة ماستر كارد | Maestro UK | ✔ | ✔ | ✔ |
| VISA | دائن‬ | ✔ | ✔ | ✔ |
| VISA | مدين | ✔ | ✔ | ✔ |
| VISA | مكافأة بنك ألفا | ✔ | ✔ | ✔ |
| VISA | Android Pay | ✔ |  |  |
| VISA | Apple Pay | ✔ |  |  |
| VISA | Samsung Pay | ✔ |  |  |
| VISA | VISA Checkout | ✔ | ✔ | ✔ |
| VISA | VISA Dankort | ✔ | ✔ | ✔ |
| VISA | VISA Hipotecario | ✔ | ✔ | ✔ |
| VISA | بطاقة VISA Aravia | ✔ | ✔ | ✔ |
| AMEX | دائن‬ | ✔ | ✔ | ✔ |
| AMEX | مدين | ✔ | ✔ | ✔ |
| AMEX | Android Pay | ✔ |  |  |
| AMEX | Apple Pay | ✔ |  |  |
| AMEX | Samsung Pay | ✔ |  |  |
| AMEX | AMEX Commercial | ✔ | ✔ | ✔ |
| AMEX | AMEX Consumer | ✔ | ✔ | ✔ |
| AMEX | AMEX Corporate | ✔ | ✔ | ✔ |
| AMEX | AMEX Small Business | ✔ | ✔ | ✔ |
| ديسكفر | قياسي | ✔ | ✔ | ✔ |
| ديسكفر | Android Pay | ✔ |  |  |
| ديسكفر | Apple Pay | ✔ |  |  |
| ديسكفر | Samsung Pay | ✔ |  |  |
| بطاقة دينرز ماستر كارد | قياسي | ✔ | ✔ | ✔ |
| Dineromail | قياسي | ✔ | ✔ | ✔ |
| JCB | قياسي | ✔ | ✔ | ✔ |
| Union Pay\* | قياسي | ✔ |  |  |
| Interac Debit\* | قياسي | ✔ |  |  |

\*لم يتم توفير الرموز المميزة للبطاقات المتكررة Interac وUnion Pay بواسطة Adyen، وبالتالي لا يمكن أن تكون مدعومة لحركات البطاقات غير الموجودة.

#### <a name="supported-gift-cards"></a>بطاقات الهدايا المدعومة
| المخطط | البطاقة موجودة | البطاقة غير موجودة |
|---|:-:|---|
| Givex | ✔ | ✔ |
| SVS | ✔ | ✔ |

لدعم مخططات بطاقة الهدايا الخارجية هذه من خلال موصل دفع Dynamics 365 لـ Adyen، يجب إكمال الخطوات الإضافية. لمزيد من المعلومات، راجع [دعم بطاقات الهدايا الخارجية](/dynamics365/unified-operations/retail/dev-itpro/gift-card).

#### <a name="supported-wallets"></a>المحافظ المدعومة

| المخطط | البطاقة موجودة | البطاقة غير موجودة |
|---|---|---|
| Alipay | سوف يضاف الدعم في إصدار مستقبلي. | لا |
| WeChat | سوف يضاف الدعم في إصدار مستقبلي. | لا |

#### <a name="supported-card-present-input-methods"></a>طرق إدخال البطاقات الموجودة المدعومة
| طريقة الإدخال | مدعوم | الإشعارات |
|---|:-:|---|
| السحب | ✔ | |
| تمرير البطاقة | ✔ | |
| الضغط | ✔ | |
| إدخال يدوي من خلال واجهة مستخدم نقطة البيع. |  | غير مدعوم حاليًا |
| إدخال يدوي من خلال الوحدة الطرفية للدفع. | ✔ | يدعم الإدخال اليدوي للبطاقات المدينة والدائنة والهدايا بإدخال رمز pin. | 


#### <a name="supported-card-present-countries"></a>البلدان التي تدعم البطاقات الموجودة المدعومة

البلدان التالية لها مكونات Commerce متوفرة ودعم للبطاقات الموجودة من Adyen. للحصول على التوفر الدولي الحالي لـ Commerce، قم بزيارة [صفحة التوفر الدولي](/dynamics365/get-started/availability).

| البلد | مدعوم |
| --- | :-: |
| أستراليا | ✔ |
| النمسا | ✔ |
| بلجيكا | ✔ |
| كندا | ✔ |
| جمهورية التشيك | ✔ |
| الدنمارك | ✔ |
| إستونيا | ✔ |
| فنلندا | ✔ |
| فرنسا | ✔ |
| ألمانيا | ✔ |
| هونغ كونغ | ✔ |
| هنغاريا‬ | ✔ |
| أيسلندا | ✔ |
| أيرلندا | ✔ |
| إيطاليا | ✔ |
| اليابان | الإصدار المستقبلي |
| لاتفيا | ✔ |
| ليتوانيا | ✔ |
| ماليزيا | ✔ |
| هولندا | ✔ |
| نيوزيلندا | ✔ |
| النرويج | ✔ |
| بولندا | ✔ |
| سنغافورة | ✔ |
| سويسرا | ✔ |
| إسبانيا | ✔ |
| السويد | ✔ |
| سويسرا | ✔ |
| المملكة المتحدة | ✔ |
| الولايات المتحدة | ✔ |
| البرازيل | الإصدار المستقبلي |

#### <a name="supported-card-not-present-countries"></a>البلدان التي تدعم البطاقات غير الموجودة المدعومة

يتم دعم البلدان التالية بواسطة Adyen لحركات البطاقات غير الموجودة. [اتصل بـ Adyen](https://www.adyen.com/contact/sales) للحصول على تفاصيل حول دعم بلد معين. للحصول على التوفر الدولي الحالي لـ Commerce، قم بزيارة [صفحة التوفر الدولي](/dynamics365/get-started/availability).

| البلد | 
| --- |
| الأرجنتين |
| أرمينيا |
| أستراليا |
| النمسا |
| البحرين |
| بلجيكا |
| البرازيل |
| بلغاريا |
| كندا |
| تشيلي |
| الصين |
| كولومبيا |
| كرواتيا |
| قبرص |
| جمهورية التشيك  |
| الدنمارك |
| مصر |
| إستونيا |
| فنلندا |
| فرنسا |
| جورجيا |
| ألمانيا |
| جبل طارق |
| اليونان |
| غويرنسي |
| هونغ كونغ |
| هنغاريا‬ |
| أيسلندا |
| الهند |
| إندونيسيا |
| أيرلندا |
| جزيرة مان |
| إسرائيل |
| إيطاليا |
| اليابان |
| جيرسي |
| كوريا |
| الكويت |
| لاتفيا |
| ليتوانيا |
| لكسمبورج |
| ماليزيا |
| مالطا |
| المكسيك |
| المغرب |
| هولندا |
| نيوزيلندا |
| النرويج |
| بيرو |
| بولندا |
| البرتغال |
| قطر |
| رومانيا |
| السعودية |
| صربيا |
| سنغافورة |
| سلوفاكيا |
| سلوفينيا |
| جنوب أفريقيا |
| أسبانيا |
| السويد |
| سويسرا |
| تايوان |
| تنزانيا |
| تايلاند |
| Türkiye |
| الإمارات العربية المتحدة (UAE) |
| المملكة المتحدة |
| الولايات المتحدة الأمريكية، بما في ذلك بورتوريكو  |

#### <a name="supported-dynamics-365-payment-features"></a>ميزات دفع Dynamics 365 المدعومة

يعرض الجدول التالي مجموعة من الميزات التي يدعمها موصل دفع Dynamics 365 لـ Adyen. تستخدم هذه الميزات التحسينات التي تم تقديمها في SDK للمدفوعات وبعض المكونات في 2018 ديسمبر. وهي غير حصرية لموصل دفع Dynamics 365 لـ Adyen. لمزيد من المعلومات حول كيفية استخدام هذه التحسينات لموصل دفع مختلف، راجع [إنشاء تكامل دفع شامل لوحدة دفع طرفية](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension).

| المخطط | البطاقة موجودة | البطاقة غير موجودة |
|---|:-:|:-:|
| [صرف رصيد بطاقة الهدايا](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [حماية الدفعات المكررة](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| الترميز المميز للقناة متعددة الاتجاهات | ✔ | ✔ |
| المبالغ المستردة المرتبطة | ✔<br>(تبدأ بالإصدار 10.0.1) | ✔<br>(تبدأ بالإصدار 10.0.1) |
| [حفظ المدفوعات عبر الإنترنت](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>(تبدأ بالإصدار 10.0.2) | 
| [بطاقات الهدايا الخارجية لمركز الاتصالات والتجارة الإلكترونية](./gift-card.md) | ✔<br>(تبدأ بالإصدار 10.0.10) | 
| [إعادة توجيه مدفوعات SCA](../adyen_redirect.md) | | ✔<br>(تبدأ بالإصدار 10.0.12) |
| [وحدات دفع طرفية مخصصة ومطالبات لطابعة ودرج الأوراق النقدية](../pos-multi-hws.md) | ✔<br>(تبدأ بالإصدار 10.0.12) | |
| [دعم تقديم البقشيش على مستوى SDK من خلال موصل Adyen](tipping.md) | ✔<br>(تبدأ بالإصدار 10.0.14) | |
| [التقاط تزايدي لفوترة الأوامر](incremental-capture.md) |  | ✔<br>(تبدأ بالإصدار 10.0.18) |
| [مدفوعات المحفظة](../wallets.md) |  | ✔<br>(تبدأ بالإصدار 10.0.20) |
| [Google Pay مع Adyen](google-pay-adyen.md) |  | ✔<br>(تبدأ بالإصدار 10.0.27) |

## <a name="next-steps"></a>الخطوات التالية

للحصول على معلومات حول كيفية تسجيل الدخول إلى موصل دفع Dynamics 365 لـ Adyen وتكوينه، راجع [موصل دفع Dynamics 365 لـ Adyen](adyen-connector-setup.md).

## <a name="additional-resources"></a>الموارد الإضافية

[إعداد Dynamics 365 Payment Connector لـ Adyen](adyen-connector-setup.md)

[الأسئلة الشائعة حول Dynamics 365 Payment Connector لـ Adyen](adyen-connector-faq.md)

[استكشاف مشكلات Dynamics 365 Payment Connector لـ Adyen وإصلاحها](adyen-connector-troubleshoot.md)

[الأسئلة المتداولة حول الدفعات](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]