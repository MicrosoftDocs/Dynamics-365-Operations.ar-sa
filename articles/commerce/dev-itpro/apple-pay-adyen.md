---
title: إعداد دفع Apple Pay مع Adyen في Dynamics 365 Commerce
description: توضح هذه المقالة كيفية تهيئة Apple Pay مع Adyen بتنسيق Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: 896847cee696e221b2114f7f28a0b56e73fc911b
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838219"
---
# <a name="set-up-apple-pay-with-adyen-in-dynamics-365-commerce"></a>إعداد دفع Apple Pay مع Adyen في Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

توضح هذه المقالة كيفية تهيئة Apple Pay مع Adyen بتنسيق Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>المصطلحات الأساسية

| المصطلح | ‏‏الوصف‬ |
|---|---|
| Apple Pay | يُعرف Apple Pay أيضًا باسم زر Apple Pay، وهو عرض دفع للمحفظة يتم دعمه عبر موصل Adyen. إنه يتيح تجربة العميل والتكامل الذي يدعمه موصل Apple Pay Microsoft Dynamics 365. |
| المحفظة | نوع دفع لا يتضمن خصائص الدفع التقليدية، مثل نطاق رقم تعريف البنك (BIN) وتاريخ انتهاء الصلاحية الذي يتم استخدامه للتمييز بين أنواع بطاقات الائتمان والخصم. |

Dynamics 365 Commerce يقدم تكاملا جاهزا لدفع Apple Pay عند استخدام خدمة عبارة الدفع Adyen. تمثل Apple Pay طريقة دفع المحفظة الرقمية التي تستخدم حساب تاجر الدفع لـ Apple Pay بالتنسيق الموجود به خدمة الدفع Adyen. عند تكوينه، يتوفر الزر Apple Pay كطريقة دفع انتقائي وهي جزء من الخروج من أمر المتجر عبر الإنترنت. يتم تقديم الزر Apple Pay كخيار دفع فقط لأجهزة Apple Pay المعتمدة. عندما يقوم المستخدمون بتحديد **Apple Pay** في متصفح أو جهاز معتمد، يتم توجيههم لإكمال الدفع الخاص بهم مباشرة مع خدمة Apple Pay. ثم يتم إعادتهم إلى واجهة المتجر عبر الإنترنت لإكمال الطلب.

يتم استخدام مرجع موصل Dynamics 365 Payment Connector for Apple Pay بالإضافة إلى Dynamics 365 Payment Connector for Adyen لتمكين Apple Pay والدفع بواسطة بطاقة مدينة على موقع. ويمكن أيضًا تكوين Apple Pay للاستخدام في المتاجر التي أديين الأطراف الطرفية التي تستخدم موصل الدفع Dynamics 365 لأديين مع نقطة بيع التجارة (نقطة البيع). وفي هذه الحالة، يقوم موصل الدفع Dynamics 365 لأديين بمعالجه جهاز دفع Apple بالضغط على الوحدة الطرفية.

## <a name="prerequisites"></a>المتطلبات الأساسية

ويتطلب استخدام Apple الدفع مع أديين في التجارة حساب تاجر من Apple Pay. للحصول على معلومات حول كيفية إعداد Apple Pay في المنطقة الخاصة بعميل الاختبار، راجع [تكامل Apple Pay](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#set-up-apple-pay). للحصول على معلومات حول ما يجب القيام به عندما تكون مستعدا للاستمرار في بيئة التشغيل، راجع [الاستمرار](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).

يجب أيضا دمج طريقة دفع Apple Pay مع حساب أديين الخاص بك. يمكن ان تساعدك أديين في إعداد طريقة الدفع ويمكنك أيضًا التأكد من أن المجالات التي ستستخدم الشهادة لها معينة للاستخدام مع الشهادة.

لتمكين علامة ميزة المحفظة المحسّنة في Commerce headquarters، انتقل إلى إدارة ميزات **مساحات العمل \> ،** وابحث عن ميزة **دعم المحفظة المحسّن وتحسينات الدفع**. حدد الميزة، ثم حدد **تمكين**. بعد تمكين الميزة ، قم بتشغيل **جدول التوزيع 1110** أتاحه التغييرات في كافة القنوات.

## <a name="map-the-apple-pay-payment-method"></a>تعيين طريقة دفع مدفوعات Apple Pay

تمثل Apple Pay طريقة دفع المحفظة الرقمية. للحصول على معلومات حول كيفية إعداد تعيين الدفع للحصول على Apple Pay، راجع [دعم دفع المحفظة](../wallets.md).

لتعيين أسلوب دفع Apple Pay في Commerce headquarters، اتبع هذه الخطوات.

1. الانتقال إلى **البيع بالتجزئة والتجارة \> إعداد القناة \> أساليب الدفع \> أنواع البطاقات**.
1. حدد **جديد** لإضافة بند Apple Pay آخر، ثم قم بتعيين القيم التالية:

    - **المعرف:** ApplePay
    - **اسم الدفع الإلكتروني:** Apple Pay
    - **النوع:** محفظة
    - **المصدر:** Apple

1. حدد **تعيين المعالج** لفتح مربع حوار **أساليب تعيين مدفوعات المعالج**. يسرد العمود **طرق دفع المعالج غير المعينة** أساليب الدفع المعتمدة لكل موصل متوفر (Adyen, PayPal, and Apple).
1. قم بتعيين طرق الدفع المدعومة التي تريدها لكل من **موصل الدفع Dynamics 365 للموصل Adyen** (للاستخدام في POS) و **موصل Dynamics 365 Payment Connector for Apple Pay** (للقناة عبر الإنترنت).
1. لكل سطر تعيين، في العمود **طرق دفع المعالج غير المعينة**، حدد السطر الذي تريد دعمه، ثم حدد **إضافة** لنقل التحديدات إلى العمود **Mapped Processor Payment Methods**.
1. حدد **موافق**، ثم من الصفحة **أنواع البطاقات**، حدد **حفظ**.

## <a name="set-up-the-apple-pay-certificate-for-your-site"></a>اعداد شهادة Apple Pay للموقع الخاص بك

بالنسبة لكل موقع، يجب تحميل ملف اقتران المجال (المعروف أيضا بشهادة Apple Pay) كما هو موضح في وثائق [Apple Pay](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live). يمكنك استخدام منشئ موقع التجارة لتحميل ملف اقتران المجال إلى مكتبة الوسائط الخاصة بموقعك.

لإعداد شهادة Apple Pay في منشئ الموقع، اتبع هذه الخطوات.

1. قم بتنزيل الشهادة (ملف اقتران المجال) من [Adyen](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).
1. أضف الامتداد .txt إلى ملف اقتران المجال.
1. في منشئ الموقع، قم بتحميل [ملف اقتران المجال إلى مكتبة الوسائط الخاصة بموقعك](../upload-serve-static-files.md).
1. انتقل إلى **URLs**.
1. حدد **جديد \> عنوان URL جديد**.
1. في مربع الحوار **عنوان URL جديد**، حدد **أصول مكتبة الوسائط**.
1. في الحقل **مسار URL**، أدخل مسار URL (إذا لم يتم إدخاله بالفعل). بعد عنوان URL الخاص بالمجال، أدخل سلسلة Apple المطلوبة التالية: `<domain>/.well-known/apple-developer-merchantid-domain-association.txt`.
1. حدد **التالي**. تعرض مكتبة الوسائط جميع أصول الوسائط التي تم تحميلها من نوع **المستند** (.txt).
1. حدد ملف ارتباط المجال الذي يجب تقديمه للطلبات إلى عنوان URL الذي حددته سابقًا.
1. حدد **إنشاء**.

وفي هذه المرحلة، يكون عنوان URL الذي قمت بإنشائه في حالة المسودة. انشر عنوان URL لإكمال العملية. لن يتم إرجاع الملف الذي يشير إليه عنوان URL حتى تقوم بنشر عنوان URL.

## <a name="configure-a-commerce-online-store-for-apple-pay"></a>قم بتكوين متجر تجاري عبر الإنترنت لـ Apple Pay

لتكوين متجر تجاري عبر الإنترنت لـ Apple Pay، اتبع هذه الخطوات.

1. في مقر التجارة، انتقل إلى **البيع بالتجزئة والتجارة \> القنوات \> محلات نشطة**.
1. حدد قيمة **معرّف قناة البيع بالتجزئة** لقناة المتجر عبر الإنترنت لموقعك.
1. في علامة التبويب السريعة FastTab **حسابات الدفع** ، أضف موصل **Dynamics 365 Payment Connector لـ Adyen** ، إذا لم يكن كذلك بالفعل الإعداد، باتباع الإرشادات الواردة في [إعداد Dynamics 365 Payment Connector for Adyen](adyen-connector-setup.md).
1. بعد تكوين موصل Adyen، حدد **إضافة** لإضافة **Dynamics 365 Payment Connector for Apple Pay**.
1. أدخل قيمًا لخصائص تاجر الموصل.

    | الخاصية               | ‏‏الوصف‬ | مطلوب | يتم ضبطه تلقائيًا | قيمة العينة |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | اسم التجميع          | اسم تجميع Dynamics 365 Payment Connector for Apple Pay. | ‏‏نعم‬ | ‏‏نعم‬ | الاسم الثنائي |
    | معرف حساب الخدمة     | المعرف الفريد لإعداد خصائص التاجر. يتم ختم هذا المعرف في حركات الدفع ويقوم بتعريف خصائص التاجر التي يجب ان تستخدمها العمليات اللاحقة (مثل الفوترة). | ‏‏نعم‬ | ‏‏نعم‬ | Guid |
    | معرف حساب التاجر    | أدخل معرف تاجر Adyen الفريد. يتم توفير هذه القيمة عند التسجيل بأديين كما هو موضح [بالتسجيل لدي أديين](adyen-connector-setup.md#sign-up-with-adyen). | ‏‏نعم‬ | لا | MerchantIdentifier |
    | مفتاح API للمجموعة          | ادخل مفتاح API لأديين الخاص بالسحابة. يمكنك الحصول علي هذا المفتاح باتباع الإرشادات الخاصة بكيفية [الحصول على مفتاح](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key)API. | ‏‏نعم‬ | لا | أب ت ث ج ح خ |
    | بيئة البوابة    | أدخل بيئة بوابه Adyen للتعيين إليها. القيم المحتملة هي **اختبار** و **مباشره**. يجب تعيين هذا الحقل علي الوضع **مباشر** " فقط لأجهزه الإنتاج والحركات. | ‏‏نعم‬ | ‏‏نعم‬ | مباشر |
    | العملات المدعومة   | العملات التي يجب أن يعالجها الموصل. في سيناريوهات البطاقة الحالية، يمكن لـ Adyen اعتماد عملات إضافية من خلال [التحويل](https://www.adyen.com/pos-payments/dynamic-currency-conversion) الديناميكي للعملة بعد إرسال طلب الحركة إلى طرف الدفع الطرفي. اتصل بالدعم Adyen للحصول علي قائمه بالعملات المعتمدة. | ‏‏نعم‬ | ‏‏نعم‬ | دولار أمريكي، يورو |
    | أنواع طرق الدفع المدعومة | أدخل أنواع العطاء التي يجب على الموصل معالجتها. | ‏‏نعم‬ | ‏‏نعم‬ | ApplePay |

1. بعد إدخال معلومات التاجر، قم بتشغيل مهمة جدولة توزيع تكوين القناة **1070**.


### <a name="configure-content-security-policies-in-site-builder"></a>تكوين سياسات أمان المحتوى في منشئ الموقع

قبل تكوين الأجزاء أو الصفحات الخاصة بك لاستخدام Apple Pay، يجب عليك التأكد من تكوين سياسات أمان المحتوى (CSPs) في Commerce Site Builder لموقعك.

لتكوين سياسات أمان المحتوى في منشئ الموقع، اتبع هذه الخطوات.

1. انتقل إلى **إعدادات الموقع \> الملحقات**.
1. في علامة التبويب **سياسة أمان المحتوى**، حدد **إضافة** لإضافة سطر يحتوي على `https://applepay.cdn-apple.com/jsapi/v1/apple-pay-sdk.js` إلى أقسام **child-src**، و **connect-src**، و **frame-src**، و **img-src**، و **script-src**، و **style-src**.
1. عند الانتهاء ، حدد **حفظ ونشر** لتنفيذ التغييرات.

### <a name="set-up-apple-pay-as-a-checkout-payment-option"></a>قم بإعداد Apple Pay كخيار دفع بالدفع

لإعداد Apple Pay كخيار دفع بالدفع على صفحة الخروج (غير السريعة) بموقعك، اتبع هذه الخطوات.

1. في موقع البناء، انتقل إلى **الأجزاء**، وحدد جزء الخروج من موقعك.
1. حدد **تحرير**.
1. في **حاوية قسم السداد مع الخروج**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة‬‏‫**.
1. في مربع الحوار **تحديد وحدات**، حدد وحدة **Apple Pay**، ثم حدد **موافق**.
1. حدد **حفظ**.
1. حدد **إنهاء التحرير** لإيداع الجزء، ثم حدد **نشر** لنشره.

تم تضمين إعدادات الوحدة النمطية **Apple Pay** في الوحدة النمطية والاتصال بموصل الدفع Dynamics 365 المكوّن لموصل Apple Pay الذي تم إعداده للقناة عبر الإنترنت في Commerce headquarters.

### <a name="apple-pay-payment-behavior"></a>سلوك الدفع في Apple Pay

يظهر زر الدفع **Apple Pay** فقط على أجهزة Apple Pay المدعومة (متصفحات iPhones, iPads وSafari التي تدعم Apple Pay). إذا كان المستخدم لا يستخدم أحد هذه الأجهزة، فسيتم إخفاء زر الدفع **Apple Pay** عن العرض.

عندما يحدد المستخدم زر الدفع **Apple Pay**، يظهر مربع حوار **Apple Pay**. هناك، يمكن للمستخدم المصادقة على جهاز Apple Pay أو متصفحه. يظهر مربع الحوار **Apple Pay** ملخصا لمبلغ الأمر وطريقة الدفع التي قام المستخدم بتكوينها مقابل محفظه Apple الخاصة بهم. ويمكن للمستخدم مراجعة هذه التفاصيل ثم تحديد **الدفع** لإكمال الدفع. بعد إكمال عملية الدفع، يتم توجيه المستخدم إلى صفحة الموقع **الطلب اكتمل** التي تعرض ملخص أمر مفصل للحركة المكتملة.

## <a name="configure-commerce-pos-for-apple-pay"></a>تهيئة Commerce POS لـ Apple Pay

يستخدم تكوين نقطه البيع تكوين حقل الخدمة **EFT الخاص** بملف تعريف الأجهزة لـ Adyen الخاصة بموصل الدفع Dynamics 365. في Commerce headquarters، قم بتكوين خدمة التحويل الإلكتروني لـ Dynamics 365 Payment Connector for Adyen كما هو موضح في [إعداد ملف تعريف أجهزة Dynamics 365 POS](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

تأكد من إضافة **ApplePay** إلى قائمة أنواع العطاءات في حقل **أنواع العطاءات المدعومة**. استخدم الفاصلة المنقوطة (؛) لفصل أنواع العطاء في القائمة.

سيعمل تعيين المعالج لموصل Adyen على التقاط أنواع بطاقات المحفظة التي تستخدمها Apple Pay في محطة POS.

## <a name="additional-resources"></a>الموارد الإضافية

[الأسئلة المتداولة حول الدفعات](payments-retail.md)

[الوحدة النمطية للسداد مع الخروج](../add-checkout-module.md)

[وحدة للدفع](../payment-module.md)