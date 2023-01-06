---
title: التطبيق Store Commerce للانظمه المحمولة
description: توضح هذه المقالة كيفيه البدء في استخدام تطبيق Store Commerce Microsoft Dynamics 365 Commerce ل Android و iOS.
author: stuharg
ms.date: 11/30/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2018-10-29
ms.openlocfilehash: dc952698a2a3301aff312e8310c58cbbb9cfe290
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815773"
---
# <a name="store-commerce-app-for-mobile-platforms"></a>التطبيق Store Commerce للانظمه المحمولة

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

توضح هذه المقالة كيفيه البدء في استخدام تطبيق Store Commerce Microsoft Dynamics 365 Commerce ل Android و iOS.

تقوم تطبيقات الهاتف Dynamics 365 Commerce الجوال الخاصة Android ب و iOS باجراء عمليه نشر أجهزه البيع بالبالكامل (POS) لبيئة البيع بالتجزئة مباشره والبسيطة. توفر تطبيقات Store Commerce للهاتف المحمول جميع إمكانيات ومزايا [تطبيق Store Commerce لنظام Windows](store-commerce.md)، وتعمل بشكل جيد على مجموعة واسعة من iOS وهواتف Android وأجهزة الكمبيوتر اللوحية. يمكن تثبيت تطبيقات المحمول Store Commerce مباشره من مخازن تطبيقات Apple , Google Play ، ولا تتطلب ان يقوم المطور بإنشاء حزمه تطبيق جديده لنشرها أو تحديثها. 

تحتفظ تطبيقات الاجهزه المحمولة Store Commerce بالتماثل الوظيفي الكامل مع التطبيقات المختلطة الحالية. بالاضافه إلى ذلك ، فان Store Commerce ب iOS يتضمن دعما لمحطه الاجهزه المخصصة ، بحيث يمكن لأجهزه iOS الاتصال بالوحدات الطرفية للدفع عبر الشبكة ، وطابعات الاستلام ، والادراج النقدية دون الحاجة إلى نشر محطه الاجهزه المشتركة. 

> [!IMPORTANT]
> تطبيقات Store Commerce الخاصة ب Windows و Android و iOS هي الجيل التالي من تطبيقات Dynamics 365 Commerce لنقاط البيع. تقدم تطبيقات Store Commerce العديد من التحسينات على سابقاتها مع الحفاظ على تكافؤ الوظائف والميزات بشكل كامل. ستقوم Microsoft بإيقاف تطبيقات MPOS وAndroid وiOS Retail POS hybrid في أواخر عام 2023، وتوصي باستخدام Store Commerce أو Cloud POS (CPOS) لجميع عمليات نشر نقاط البيع الجديدة. يجب أن يخطط العملاء الموجودين للترحيل من التطبيقات المختلطة للبيع بالتجزئة Store Commerce. لمزيد من المعلومات، راجع [ترحيل نقاط البيع الحديثة إلى Store Commerce](pos-extension/migrate-mpos-store-commerce.md). 

## <a name="app-architecture"></a>هندسة التطبيق

تستخدم تطبيقات الجوالStore Commerce نفس الطبولوجيا التي يستخدمها تطبيق Store Commerce ل Windows عند نشره في الوضع المختلط. تطبيقات الاجهزه المحمولة Store Commerce تطبيقات shell التي تقدم CPOS مباشره من Commerce Scale Unit (CSU) ، واتصل بتجاره الهيادليس Commerce headquarters عبر الكسو. ويمكن طراز تطبيق shell تخزين التطبيقات Store Commerce الاجهزه المخصصة للحصول علي التكامل المباشر مع محطه دفع طرفيه ، وطابعه ، ودرجات نقديه ، وأجهزه طرفيه أخرى. لا يلزم اعداد محطه الاجهزه المشتركة لاستخدام الاجهزه. 

لتحديث تطبيقStore Commerce، قم فقط بتحديث كسو. سيتم تلقائيا انتقاء كافة وظائف retail POS وميزاته الجديدة بواسطة التطبيق. لمزيد من المعلومات حول كيفيه تحديث كسو ، راجع [تطبيق التحديثات والملحقات علي Commerce Scale Unit (مجموعه النظراء)](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md).

تتم معالجه تطبيقات shell عبر تحديثات "متجر التطبيقات". عندما يصل الإصدار الثانوي إلى التوفر العام (جا) ، ستقوم Microsoft بنشره علي متاجر التطبيق. وقد تقوم Microsoft أيضا بنشر التصحيحات بين التحديثات الثانوية لإصدار إصلاحات الأخطاء ذات الاولويه العالية.

## <a name="prerequisites"></a>المتطلبات الأساسية

تتطلب Dynamics 365 Commerce تطبيقات الاجهزه المحمولةStore Commerce وهي مكونات Commerce headquarters والكسو بشكل خاص. يسرد الجدول التالي الحد الأدنى لنظام التشغيل (OS) والإصدارات كسو المطلوبة من قبل تطبيقات وتطبيقات iOS للاجهزه المحمولة Android. 

| المتطلب الأساسي | Android      | iOS  |
| ------------ | ------------ | ---- |
| إصدار نظام التشغيل   | 7.0          | 15.0 |
| إصدار CSU  | 9.38.22266.8 | سيتم تحديده لاحقًا  |

## <a name="install-the-app"></a>تثبيت التطبيق

يمكنك تثبيت تطبيقات الجوال اStore Commerceمباشره من متجر Google Play أو متجر تطبيقات Apple. 

- [تطبيق Store Commerce لـ Android](https://aka.ms/storecommerceandroid)
- [تطبيق Store Commerce لـ iOS](https://aka.ms/storecommerceios)

يمكن أيضا تحميل حزم التطبيق Android (أبك) و Apple app (إيبا) من مكتبه الأصول المشتركة في Lifecycle Services Microsoft Dynamics. 

## <a name="device-and-register-setup"></a>الجهاز وتسجيل الإعداد

قبل ان يمكن تنشيط الخزينة علي تطبيقات الاجهزه المحمولة Store Commerce ، يجب اعداد جهاز وتسجيل في Commerce headquarters. لمزيد من المعلومات، راجع [حذف تسجيلات الخدمة](../implementation-considerations-devices.md). 

### <a name="device-setup"></a>إعداد الجهاز

لإنشاء جهاز جديد وإعداده ، اتبع هذه الخطوات.

1. في إدارة Commerce headquarters، انتقل إلى **Retail وCommerce \> إعداد القنوات \> إعداد نقاط \> البيع**. 
1. قم بإنشاء جهاز جديد ، وحدد اما **الحديثة لنقطه Android** البيع أو **iOS** العصرية لشركه pos كنوع التطبيق ، اعتمادا علي تطبيق الاجهزه المحمولة الذي تقوم بنشره. 

    > [!NOTE] 
    > يتم أيضا استخدام أنواع التطبيقات الحديثة **الخاصة بنقطه البيع والحديثة Android** لنشر التطبيقات المختلطة **الحالية** ل Androidio  و ios. بعد ديبريكاتيون المبوس ، سيتم تحديث التسميات الخاصة بأنواع التطبيقات هذه لتخزين التجارة **والحديثة Android** في **retail POS**. 

### <a name="register-setup"></a>إعداد السجل

يمكنك إنشاء خزينه جديده واقرانها بالجهاز الذي قمت بإنشاءه ، أو يمكنك اقران سجل موجود بالجهاز الجديد. لمزيد من المعلومات حول السجلات ، راجع [إنشاء السجلات وربطها](../tasks/create-associate-registers.md).

### <a name="screen-layout-setup"></a>إعداد تخطيط الشاشة

إذا كنت ريبوربوسينج تخطيط شاشه مضمن في البيانات التوضيحية المتوفرة مع الترخيص Dynamics 365 Commerce ، سيقوم تطبيق التجارة المتجر تلقائيا بتحديد التخطيط المضغوط المضمن إذا كانت دقه الشاشة للجهاز اقل من 480 &times;85 3 بكسل في الاتجاه العمودي. ومع ذلك ، إذا كنت تقوم بإنشاء تخطيط شاشه من البداية ، أو إذا كان الجهاز المحمول الخاص بك يستخدم دقه أكبر من تلك التي يدعمها التخطيط المضغوط ، فتاكد من إنشاء دقه وشبكات أزرار مقترنة مناسبه للهاتف أو الكمبيوتر اللوحي الذي تخطط لنشره. لمزيد من المعلومات حول تكوينات تخطيط الشاشة ، راجع [التكوينات](../pos-screen-layouts.md)المرئية لواجهه مستخدم نقطه البيع. 

بعد تكوين الاجهزه والسجلات ، وفي المركز التجاري التجاري ، انتقل إلى البيع بالتجزئة والبيع **\>بالتجزئة ومعرفات \>** التجارة ، ثم قم بتشغيل وظيفة عمليات التسجيل.

## <a name="activate-a-device"></a>تنشيط الجهاز

لتنشيط جهاز في تطبيق الاجهزه المحمولة الخاص بالمتجر ، اتبع الخطوات التالية.

1. افتح التطبيق على الجهاز المحمول.
1. أدخل عنوان URL لـ CPOS ، والذي يمكنك العثور عليه في صفحة تفاصيل البيئة في Lifecycle Services ، أو في **ملامح القناة** الصفحة في مقر التجارة (**البيع بالتجزئة والتجارة \> إعداد القناة \> ملامح القناة**).
1. سجل الدخول باستخدام بيانات اعتماد العامل الذي لديه الاذن باداره الاجهزه.
1. يتيح تحديد المتجر المرتبط بالخزينة التي قمت بإنشاءها أو أعاده استخدامها في "الاداره التجارية".
1. حدد السجل الذي قمت بربطه بالجهاز الذي قمت بإنشائه في المقر التجاري.
1. يجب تنشيط جهازك الآن. يمكنك تسجيل الدخول إلى الخزينة باستخدام معرف عامل التشغيل وكلمه المرور للعامل المرتبط بالمتجر الذي قمت بتحديده. 

لمزيد من المعلومات حول تنشيط الجهاز ، راجع [التنشيط](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation) في جهاز نقطه البيع (POS).

## <a name="feature-parity-with-store-commerce-for-windows"></a>تماثل الميزات مع تجاره المتجر ل Windows

يقارن الجدول التالي قدرات تطبيق المتجر التجاري عبر Windows و Android و الانظمه الاساسيه iOS.

| الميزة                                                                               | Windows | Android | iOS |
| ------------------------------------------------------------------------------------- | ------- | ------- | --- |
| محطة أجهزة مخصصة                                                            | ‏‏نعم‬     | ‏‏نعم‬     | ‏‏نعم‬ |
| محطة أجهزة IIS المشتركة                                                               | ‏‏نعم‬     | ‏‏نعم‬     | ‏‏نعم‬ |
| الاتصال بالاجهزه الطرفية عبر الشبكة (وحده الدفع الطرفية والطابعة والدرج النقدي) | ‏‏نعم‬     | ‏‏نعم‬     | ‏‏نعم‬ |
| OLE for نقطه البيع (OPOS) الاجهزه الطرفية من خلال محطه جهاز محليه             | ‏‏نعم‬     | لا      | لا  |
| وضع دون الاتصال                                                                          | ‏‏نعم‬     | لا      | لا  |

## <a name="additional-resources"></a>الموارد الإضافية

[تطبيق Store Commerce](store-commerce.md)

[الاختيار بين Store Commerce وCloud POS](../mpos-or-cpos.md)

[استكشاف أخطاء اعداد Store Commerce ومشكلات التثبيت وإصلاحها](../troubleshoot/store-commerce-setup-installation.md)