---
title: إظهار إعلامات الأوامر في نقطة البيع (POS)
description: يصف هذا المقال كيفية تمكين إخطارات الأوامر في نقطة البيع وإطار عمل الإخطار.
author: ShalabhjainMSFT
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: a9e646d6bf48461e78dc75c8a154f2fbf1443393
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853944"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>إظهار إعلامات الأوامر في نقطة البيع (POS)

[!include [banner](includes/banner.md)]

يمكن تعيين عدة مهام لموظفي المتجر في المتجر الخاص بهم، مثل استيفاء الطلبات أو اجراء عمليات استلام المخزون أو عمليات الجرد. يقدم عميل نقطة البيع تطبيقًا واحدًا يمكن فيه إخطار الموظفين بهذه المهام. يساعد إطار عمل الإخطار في نقطة البيع عن الطريق السماح لبائعي التجزئة بتكوين الإخطارات القائمة على الدور. بدء من Dynamics 365 Retail مع تحديث التطبيق 5، يمكن تكوين هذه الإخطارات لعمليات نقطة البيع.

يمكن للنظام إظهار إخطارات لعملية *استيفاء الأوامر*، وبدء من الإصدار 10.0.18 من Commerce يمكن أيضًا إظهار الإخطارات لعملية *استدعاء الأوامر*. ومع ذلك، ونظرًا لأنه تم تصميم إطار العمل ليكون قابلًا للتوسعة، فسوف يكون المطورن في نهاية الأمر قادرون على [كتابة مُعالج الإخطار](dev-itpro/extend-pos-notification.md) لأي عملية، وعرض الإخطارات لهذه العملية في نقطة البيع.

## <a name="enable-notifications-for-order-fulfillment-or-recall-order-operations"></a>تمكين الإخطارات لعمليات استيفاء الطلبات أو استدعاء الطلبات

لتمكين الإخطارت الخاصة بعمليات استيفاء الطلبات أو استدعاء الطلبات، اتبع الخطوات التالية:

1. انتقل إلى **Retail وCommerce \> إعداد القناة \> إعداد نقطة البيع \> نقطة البيع \> العمليات**.
1. ابحث عن عملية **استيفاء الطلب** أو عملية **استدعاء الطلب**، ثم حدد خانة اختيار **تمكين الإخطارات** للعملية لتحديد أن إطار عمل الإخطار يجب أن يستمع إلى مُعالج هذه العملية. إذا تم تنفيذ المعالج، سيتم عرض الإخطارات الخاصة بهذه العملية بعد ذلك في نقطة البيع.
1. انتقل إلى **Retail وCommerce \> الموظفون \> العامون**.
1. حدد علامة التبويب **Commerce**، وحدد صف العامل، ثم حدد **أذونات نقطة البيع**. حدد علامة التبويب السريعة **الإخطارات** لتوسيعها، ثم أضف العمليات التي قمت بتمكين إخطاراتها لها. في حاله تكوين إخطار واحد للعامل، تأكد من تعيين قيمة **ترتيب العرض** إلى **1**. في حاله تكوين أكثر من عملية واحدة، قم بتعيين قيم **ترتيب العرض** للإشارة إلى الترتيب الذي يجب أن يتم عرض الإخطارات به. 

      يتم عرض الإخطارات فقط للعمليات التي تمت إضافتها في علامة التبويب السريعة **الإخطارات**. يمكنك إضافة عمليات هناك فقط في حالة تحديد خانات الاختيار **تمكين الإخطارات** الخاصة بهذه العمليات في صفحة **عمليات نقطة البيع**. بالإضافة إلى ذلك، يتم عرض الإخطارات الخاصة بإحدي العمليات فقط للعاملين إذا تمت إضافة العملية إلى أذونات نقطة البيع لهؤلاء العمال.

    > [!NOTE]
    > يمكن تجاوز الإخطارات على مستوى المستخدم. للقيام بذلك، افتح سجل العامل، ثم حدد **أذونات نقطة البيع**، ثم قم بتحرير اشتراك إخطار المستخدم.

1. انتقل إلى **البيع بالتجزئة والتجارة \> إعداد القناة \> إعداد قناة البيع \> ملفات تعريف نقطة البيع \> ملفات تعريف الوظائف**. في حقل **الفاصل الزمني للإخطار**، قم بتحديد عدد مرات سحب الإخطارات. بالنسبة لبعض الإخطارات، يجب على نقطع البيع إجراء مكالمات في الوقت الحقيقي مع تطبيق مكتب الدعم. تستهلك هذه المكالمات القدرة الحوسبية لتطبيق مكتب الدعم. لذلك، عندما تقوم بتعيين الفاصل الزمني للإخطار، يجب عليك مراعاة كل من متطلبات العمل الخاص بك وأثر مكالمات الوقت الحقيقي لتطبيق مكتب الدعم. تقوم القيمة **0** (صفر) بإيقاف تشغيل الإخطارات.
1. انتقل إلى **البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**. حدد جدول **1060** (**فريق العمل**) لمزامنة إعدادات اشتراك الإخطارات، ثم حدد **تشغيل الآن**. بعد ذلك، قم بتحديد جدول **1070** (**تكوين القناة**) لمزامنة الفاصل الزمني للإذن، ثم حدد **تشغيل الآن**.

## <a name="view-notifications-in-the-pos"></a>عرض الإخطارات في نقطة البيع

بعد إكمال الخطوات السابقة، سوف يتمكن العاملون من عرض الإخطارات في نقطة البيع. لعرض الإخطارات، حدد رمز الإخطار في الزاوية العلوية اليمنى من نقطة البيع. تظهر لوحه الإخطار وتعرض الإخطارات للعمليات التي تم تكوينها للعامل. 

في عملية **استيفاء الطلبات**، تعرض لوحة الإخطار المجموعات التالية:

- **التقاط المتجر** – تعرض هذه المجموعة عدد سطور الطلبات الفردية التي تمت جدولة التقاطها من المتجر الحالي. يمكنك تحديد الرقم في المجموعة لفتح عملية **استيفاء الطلب** باستخدام عامل تصفية بحيث يعرض سطور الأمر النشطة فقط التي تم إعدادها للالتقاط من المتجر الحالي.
- **شحن من المتجر** - تعرض هذه المجموعة عدد بنود الأوامر الفردية التي تم تكوينها للشحن من المتجر الحالي للمستخدم. يمكنك تحديد الرقم في المجموعة لفتح عملية **استيفاء الطلب** باستخدام طريقة عرض مصفاة بحيث تعرض سطور الأمر النشطة فقط التي تم إعدادها للشحن من المتجر الحالي.

في عملية **استدعاء الطلبات**، تعرض لوحة الإخطار المجموعات التالية:

- **الطلبات المطلوب تنفيذها** – تعرض هذه المجموعة عدد الأوامر التي تم تكوينها إما لعمليات الانتقاء أو استيفاء الشحن للمتجر الحالي للمستخدم. يمكنك تحديد الرقم الموجود في المجموعة لفتح عملية **استدعاء الطلب** باستخدام طريقة عرض مصفاه والتي تعرض فقط الأوامر المفتوحة التي يجب استيفاءها بواسطة المتجر الحالي للمستخدم إما لانتقاءها في المتجر أو سيناريوهات الشحن من المتجر.
- **الطلبات المطلوب انتقاؤها** – تعرض هذه المجموعة عدد الطلبات التي تمت جدولة التقاطها من المتجر الحالي. يمكنك تحديد الرقم الموجود في المجموعة لفتح عملية **استدعاء الطلب** باستخدام طريقة عرض مصفاه والتي تعرض فقط الأوامر المفتوحة التي يجب استيفاءها لانتقاءها للعميل من المتجر الخاص بالمستخدم.
- **طلبات مطلوب شحنها** - تعرض هذه المجموعة عدد الطلبات المطلوب شحنها من المتجر الحالي للمستخدم. يمكنك تحديد الرقم الموجود في المجموعة لفتح عملية **استدعاء الطلب** باستخدام طريقة عرض مصفاه والتي تعرض فقط الأوامر المفتوحة التي يجب استيفاءها للشحن من المتجر الخاص بالمستخدم.

مع كل من إخطارات استيفاء الطلبات واستدعاء الطلبات، عندما انتقاء الطلبات بواسطة العملية، تتغير أيقونة الإخطار لتشير إلى وجود إخطارات جديدة، وعدد المجموعات المناسبة التي تم تحديثها. وعلى الرغم من تحديث المجموعات عند فترات زمنية منتظمة، بإمكان مستخدمي نقطة البيع تحديث المجموعات يدويًا في أي وقت من خلال تحديد **تحديث** بجوار المجموعة. وأخيرً، إذا كانت مجموعة تحتوي على صنف جديد ولم يقم العامل الحالي بعرضه، فمن ثم تُظهر المجموعة رمز اندفاع لتشير إلى المحتوى الجديد.

## <a name="enable-live-content-on-pos-buttons"></a>تمكين المحتوى المباشر على أزرار نقطة البيع

يمكن لأزرار نقطة البيع الآن عرض عملية الجرد لمساعدة العاملين بسهولة في تحديد المهام التي تحتاج إلى اهتمامهم الفوري. لإظهار هذا الرقم على زر نقطة البيع، يجب عليك إتمام إعداد الإخطار الموضح سابقًا في هذا المقال (بمعنى، يجب عليك تمكين الإخطارات الخاصة بإحدى العمليات، ثم قم بإعداد الفاصل الزمني للإخطار، وتحديث مجموعة إذن نقطة البيع للعامل). بالإضافة إلى ذلك، يجب عليك فتح مصمم شبكة الأزرار، وعرض خصائص الزر، ثم تحديد خانة اختيار **تمكين المحتوى المباشر**. في حقل **محاذاة المحتوى**، يمكنك تحديد ما إذا كانت عملية الجرد يتعين أن تظهر في الركن العلوي الأيسر من الزر (**أعلى اليمين**) أو في المركز (**مركز**).

> [!NOTE]
> يمكن تمكين المحتوى المباشر للخصائص فقط إذا تم تحديد خانة اختيار **تمكين الإخطارات** الخاصة بهم في صفحة **عمليات نقطة البيع**، كما هو موضح سابقا في هذا المقال.

يعرض الرسم التوضيحي التالي إعدادات المحتوى النشط في مصمم شبكة الأزرار.

![إعدادات المحتوى المباشرة في مصمم شريط الأزرار.](./media/ButtonGridDesigner.png "إعدادات المحتوى المباشرة في مصمم شريط الأزرار")

لإظهار عدد الإعلامات على زر، يجب التأكد من تحديث تخطيط الشاشة الصحيح. لتحديد تخطيط الشاشة المستخدم من قبل نقطه البيع ، حدد أيقونة **الإعدادات** في الركن العلوي الأيسر، وسجّل **معرّف تخطيط الشاشة** و **دقة التخطيط**. باستخدام مستعرض Edge، انتقل الآن إلى صفحة **تخطيط الشاشة** ، ابحث عن **مُعرّف تخطيط الشاشة** و **دقة الشاشة** المُحددة أعلاه، وحدد خانة الاختيار **تمكين المحتوى المباشر**. انتقل إلى **البيع بالتجزئة والتجارة\> تكنولوجيا معلومات البيع بالتجزئة والتجارة\> جدول التوزيع** وشغّل الوظيفة 1090 (سجلات) لمزامنة تغييرات التخطيط.

![البحث عن تخطيط الشاشة المستخدم بواسطة نقطة البيع.](./media/Choose_screen_layout.png "البحث عن تخطيط الشاشة")

يبين الرسم التوضيحي التالي تأثير تحديد **أعلى اليمين** في مقابل **المركز** في حقل **محاذاة المحتوى** لأزرار ذات أحجام مختلفة.

![المحتوى المباشر على أزرار نقطة البيع.](./media/ButtonsWithLiveContent.png "المحتوى المباشر على أزرار نقطة البيع")

[!INCLUDE[footer-include](../includes/footer-banner.md)]
