---
title: استخدام أكواد إرجاع الدُفعة‬ لوضع علامة على الدُفعات على أنها متوفرة أو غير متوفرة
description: توضح هذه المقالة كيفيه إعداد أكواد إرجاع الدُفعة واستخدامها لتمييز الدُفعات على أنها متوفرة أو غير متوفرة للاستخدام في التخطيط الرئيسي و/أو الحجز و/أو الانتقاء و/أو الشحن.
author: t-benebo
ms.date: 09/16/2022
ms.topic: article
ms.search.form: PdsDispositionMaster, InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-16
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cfb0743a573550de93d75063df517e0c143f2568
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542462"
---
# <a name="use-batch-disposition-codes-to-mark-batches-as-available-or-unavailable"></a>استخدام أكواد إرجاع الدُفعة‬ لوضع علامة على الدُفعات على أنها متوفرة أو غير متوفرة

توضح هذه المقالة كيفية إعداد *أكواد إرجاع الدُفعة‬‬* واستخدامها. يكون لكل كود من أكواد إرجاع الدُفعة حالة إما *متوفر* أو *غير متوفر*. يمكن تعيين أكواد إرجاع الدُفعة إلى دُفعات المخزون للإشارة إلى ما إذا كانت كل دُفعة متاحة للتخطيط الرئيسي و/أو الحجز و/أو الانتقاء و/أو الشحن.

لاستخدام أكواد إرجاع الدُفعة، يجب عليك إعداد الأكواد وتعيينها إلى الدُفعات التي تريد إدارتها.

## <a name="set-up-batch-disposition-codes"></a>قم بإعداد أكواد إرجاع الدُفعة

يجب عليك إعداد كل كود من أكواد إرجاع الدُفعة الذي ترغب في استخدامه في نظامك. يمكنك إنشاء العديد من الأكواد كما تريد. (علي سبيل المثال، يمكنك إنشاء أكواد لتحديد الأسباب المختلفة التي تجعل الدُفعة متوفرة أو غير متوفرة). ومع ذلك، سيكون لديك غالبًا كودين: واحد *متوفر* وآخر *غير متوفر*. يمكنك أيضًا إنشاء أكواد مخصصة تمكّن الدُفعة من استخدامها في بعض العمليات دون غيرها.

اتبع هذه الخطوات لإعداد أكواد إرجاع الدُفعة.

1. انتقل إلى **إدارة المخزون \> إعداد \> الدُفعة \> ‏‫إرجاع الدُفعة الرئيسي‬**.
1. تسرد صفحة **‏‫إرجاع الدُفعة الرئيسي** أكواد إرجاع الدُفعة الحالية وتتيح لك إنشاءها وحذفها وتحريرها. اتبع إحدى الخطوات التالية:

    - لتحرير كود موجود، حدده في جزء القائمة.
    - لإنشاء كود جديد، حدد **جديد** في جزء الإجراءات.

1. عيّن الحقول التالية في عنوان الكود الجديد أو المحدد:

    - **رمز إرجاع الدُفعة**– أدخل اسم العرض للكود.
    - **الوصف** – صِف الكيفية التي يجب بها استخدام الكود.
    - **حالة إرجاع الدُفعة** – حدد الحالة التي تنطبق علي الدُفعات التي تم تعيين الكود لها:

        - *غير متوفر* – لا يمكن استخدام الدُفعات للتخطيط الرئيسي أو الحجز أو الانتقاء أو الشحن. عند تحديد هذه القيمة، يتم تعيين كافة خيارات **الحظر** الموجودة في ‏‫علامة التبويب السريعة **إلإعداد** على *نعم* ويتم تعيين كافة خيارات **قابل للتصفية** على *‎لا*. ومع ذلك، يمكنك تغيير بعض هذه الإعدادات لإضافة استثناءات.
        - *متوفر* – يمكن استخدام الدُفعات للتخطيط الرئيسي و/أو الحجز و/أو الانتقاء و/أو الشحن. عند تحديد هذه القيمة، يتم تعيين كافة خيارات **الحظر** الموجودة في ‏‫علامة التبويب السريعة **إلإعداد** على *لا* ويتم تعيين كافة خيارات **قابل للتصفية** على *‎نعم*. ستكون هذه الإعدادات للقراءة فقط عندما يتم تعيين حقل **‏‫حالة إرجاع الدُفعة** علي *متوفرة*.

1. إذا قمت بتعيين حقل **حالة إرجاع الدُفعة** على *غير متوفر*، فيمكنك تخصيص حالة الحظر لكل عملية (الحجز والانتقاء والشحن) لكل نوع من أنواع الأوامر (المبيعات والترحيل والإنتاج). بالنسبة لأوامر الإنتاج، يمكنك اختيار حظر دفتر يوميه انتقاء الإنتاج أو إلغاء الحظر عنه. يمكنك أيضا اختيار حظر التخطيط الرئيسي أو إلغاء حظره. استخدم الخيارات الموجودة في علامة التبويب السريعة **الإعداد** لحظر أو إلغاء حظر كل عمليه حسب الحاجة. قم بتعيين الخيار **قابل للتصفية‬** على *نعم* لتمكين التخطيط الرئيسي أو قم بتعيينه إلى *لا* لحظر التخطيط الرئيسي.

## <a name="assign-batch-disposition-codes-to-batches"></a>قم بتعيين أكواد إرجاع الدُفعة‬ على الدُفعات

بعد تحديد أكواد إرجاع الدُفعة التي تطلبها، اتبع الخطوات التالية لتعيينها على الدُفعات.

1. انتقل إلى **إدارة المستودعات \> الإعداد \> المخزون \> الدُفعات**.
1. حدد دُفعة واحدة أو أكثر لتعيين كود إرجاع دُفعه لها.
1. في جزء الإجراءات، في علامة تبويب **إعادة التعيين** حدد **‏‫إعادة تعيين رمز إرجاع الدُفعة‬‬**.
1. في مربع الحوار **‏‫تغيير التقييدات الخاصة بدُفعة المخزون‬** قم بتعيين حقل **كود إرجاع دُفعة جديد‬** على اسم الكود الذي ترغب في تعيينه.
1. حدد **موافق** لتطبيق الإعداد الجديد وحفظ التغيير.

    في صفحة **الدُفعات** يتم تحديث القيم الموجودة في العمودين **‏‫كود إرجاع الدُفعة‬** **و‏‫حالة إرجاع الدُفعة‬** بحيث تعكس الإعدادات الجديدة للدُفعات المحددة.

## <a name="master-planning-example"></a>مثال على التخطيط الرئيسي

يوضح هذا المثال كيف يمكن أن تؤثر أكواد إرجاع الدُفعة على التخطيط الرئيسي.

في هذا المثال، يتم إعداد أكواد إرجاع الدُفعة بالطريقة التالية:

- *متوفر-P:*

    - **‏‫حالة إرجاع الدُفعة‬:** *متوفر*
    - **‬‏‫قابل للتصفية:** *نعم*

- *غير متوفر-P:*

    - **‏‫حالة إرجاع الدُفعة‬:** *غير متوفر*
    - **قابل للتصفية:** *لا*

يوجد منتج (*المنتج-1*) الذي يحتوي علي الدُفعتين: *الدفعة-أ* *والدُفعة-ب*. يتم إعداد هذه الدُفعات بالطريقة التالية:

- *الدُفعة-أ*

    - **‏‫حالة إرجاع الدُفعة‬:** *متوفر-P*
    - **‎الكمية الفعلية:** 1

- *الدُفعة-ب*

    - **‏‫حالة إرجاع الدُفعة‬:** *غير متوفر-P*
    - **‎الكمية الفعلية:** 1

يوجد أمر مبيعات (*SO1*) لكمية قيمتها "2" لمنتج *منتج-1*. يكون تاريخ التسليم ثلاثه أيام من اليوم.

يمكنك تشغيل التخطيط الرئيسي وتعيين القيم التالية المتعلقة بهذا المثال:

- **أمر مخطط له:** *أمر شراء*
- **استراتيجية التجديد:** *المتطلبات*
- **الحد الأدنى لوقت الإنتاج:** *0*

كنتيجة لعملية التخطيط، يستخدم النظام الدُفعة المتوفرة (*الدُفعة-أ*) لتغطية كمية مقدارها 1 من منتج *المنتج-1* لأمر المبيعات *SO1*. ومع ذلك، لا يمكنه استخدام الدُفعة *الدُفعة-ب* لأن هذه الدُفعة تم تمييزها على أنها غير متوفرة للتخطيط. بالتالي، لتغطيه الكمية المتبقية، يقوم النظام بإنشاء أمر شراء مخططًا (*PPO1*) لدُفعة جديدة من منتج *المنتج-1*.

يوضح الرسم التوضيحي التالي جدولاً زمنيًا لنتيجة التخطيط.

![مثال يوضح كيف يمكن أن تؤثر أكواد إرجاع الدُفعة على التخطيط الرئيسي.](media/batch-codes-planning-example.png "مثال يوضح كيف يمكن أن تؤثر أكواد إرجاع الدُفعة على التخطيط الرئيسي")
