---
title: التوزيع التلقائي للمصاريف
description: تُساعد ميزة المصاريف في Dynamics 365 Supply Chain Management من Microsoft في تخصيص المصاريف تلقائيًا لأوامر الشراء أو أوامر التوريد.
author: dasani-madipalli
manager: tfehr
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 818affc7591577b69309928eb9b0e71130884cec
ms.sourcegitcommit: 3feccc9facb33e3dee18f04e202f7b20785df0a8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998866"
---
# <a name="automatic-allocation-of-charges"></a>التوزيع التلقائي للمصاريف

[!include [banner](../includes/banner.md)]

استنادًا إلى العميل الذي تعمل به أو الصنف الذي تقوم ببيعه، فقد ترغب في تطبيق مصاريف إضافية محددة. تُساعد ميزة *المصاريف* في Dynamics 365 Supply Chain Management Microsoft في تخصيص المصاريف تلقائيًا لأوامر الشراء أو أوامر التوريد.

المصاريف التلقائية، أو الرسوم التلقائية، يتم تطبيقها تلقائيًا عند إنشاء أمر مبيعات أو أمر شراء. يمكنك تعريف المصاريف التلقائية لموردين أو عملاء معينين أو مجموعات من الموردين أو الأصناف. يمكنك أيضًا تعريف المصاريف التلقائية التي تنطبق على جميع الموردين أو العملاء أو الأصناف.

## <a name="set-up-charges-codes"></a>إعداد أكواد المصاريف

لتخصيص المصاريف، يجب عليك أولاً تحديد أكواد المصاريف.

1. اتبع إحدى الخطوات التالية:

    - بالنسبة لأوامر الشراء: انتقل إلى **حسابات الدائنة \> إعداد المصاريف \> كود المصاريف**.
    - بالنسبة لأوامر الشراء: انتقل إلى **حسابات مدينة \> إعداد المصاريف \> كود المصاريف**.

1. في جزء الإجراء، حدد **جديد** لإنشاء كود المصاريف.
1. في رأس السجل الجديد، عيِّن الحقول التالية:

    - **كود المصاريف** – أدخل كود المصاريف.
    - **الوصف** ، أدخل وصفًا للمصاريف.
    - **مجموعة ضريبة المبيعات للأصناف‬** – حدد مجموعة ضريبة المبيعات للأصناف، إن كان ذلك ممكنًا.
    - **التقسيم بالتناسب** – قم بتعيين هذا الخيار إلى *نعم* إذا كنت تريد تقسيم المصاريف بالتناسب. يتوفر هذا الخيار فقط لأوامر المبيعات.
    - **الحد الأقصى للمبلغ** – أدخل الحد الأقصى المسموح به لكود المصاريف. يستخدم هذا الحقل للتحقق من صحة المصاريف الخاصة بفواتير المورد. وهي متاحة لأوامر الشراء فقط.

        > [!NOTE]
        > لتشغيل وظيفة التحقق من صحة المصاريف لأوامر الشراء، انتقل إلى **الحسابات الدائنة \> الإعداد \> معلمات الحسابات الدائنة**. في علامة التبويب السريعة **التحقق من صحة الفاتورة** ، في القسم **التحقق من صحة الفاتورة** ، قم بتعيين الخيار **تمكين التحقق من صحة مطابقة الفاتورة‬‬‬‬‏‫** إلى *نعم*.

1. تشتمل العملية علامة التبويب السريع **الترحيل** على القسمين **المدين** و **الائتمان**. قم بتعيين الحقول التالية استنادًا إلى دفتر الأستاذ الذي ترغب في ترحيل المصاريف إليه:

    - **النوع** – حدد نوع الحساب الذي تقوم بترحيل ( *دفتر الأستاذ* أو *العميل* أو *الصنف* ).
    - **الترحيل** – حدد نوع الترحيلات المطلوب إنشاؤها (مثل *رسم الوسيط* أو *تسوية العميل* ).
    - **الحساب** – حدد الحساب المراد ترحيل المصاريف إليه.

1. في جزء الإجراءات، حدد **حفظ**.

## <a name="create-charge-groups"></a>إنشاء مجموعات المصاريف

تقوم مجموعات المصاريف تلقائيًا بتخصيص المصاريف الخاصة على مجموعة من العملاء أو الموردين. تصف الأقسام الفرعية التالية كيفية إنشاء مجموعات المصاريف هذه وتعيينها.

### <a name="charge-groups-for-purchase-orders"></a>مجموعات المصاريف لأوامر الشراء

لإنشاء مجموعات المصاريف لأوامر الشراء، اتبع الخطوات التالية.

1. انتقل إلى **الحسابات الدائنة \> إعداد المصاريف \> مجموعة المصاريف للمورد**.
1. في جزء الإجراء، حدد **جديد** لإضافة صف إلى الشبكة، ثم قم بتعيين الحقول التالية:

    - **مجموعة المصاريف** – أدخل اسم مجموعة المصاريف.
    - **الوصف** ، أدخل وصفًا لمجموعة المصاريف.

1. في جزء الإجراءات، حدد **حفظ**.
1. انتقل إلى **الحسابات الدائنة \> الموردون \> جميع الموردين** ، وافتح إما مورد حالي أو قم بإنشاء مورد جديد.
1. في علامة التبويب السريعة **القيم الافتراضية لأمر الشراء** ، في القسم **أمر الشراء** ، قم بتعيين الحقل **مجموعة المصاريف** إلى مجموعة المصاريف التي قمت بإنشاءها.

### <a name="charge-groups-for-sales-orders"></a>مجموعات المصاريف لأوامر المبيعات

لإنشاء مجموعات المصاريف لأوامر المبيعات، اتبع الخطوات التالية.

1. انتقل إلى **الحسابات المدينة \> إعداد التكاليف \> مجموعات مصاريف العملاء**.
1. في جزء الإجراء، حدد **جديد** لإضافة صف إلى الشبكة، ثم قم بتعيين الحقول التالية:

    - **مجموعة المصاريف** – أدخل اسم مجموعة المصاريف.
    - **الوصف** ، أدخل وصفًا لمجموعة المصاريف.

1. في جزء الإجراءات، حدد **حفظ**.
1. انتقل إلى **الحسابات المدينة \> العملاء \> جميع العملاء** ، وافتح إما عميل أو قم بإنشاء عميل جديد.
1. في علامة التبويب السريعة **القيم الافتراضية لأمر الشراء** ، في القسم **أمر المبيعات** ، قم بتعيين الحقل **مجموعة المصاريف** إلى مجموعة المصاريف التي قمت بإنشاءها.

## <a name="define-auto-charges"></a>تحديد المصاريف التلقائية

بعد إعداد أكواد المصاريف، اتبع الخطوات التالية لتحديد المصاريف التلقائية.

1. اتبع إحدى الخطوات التالية:

    - بالنسبة لأوامر الشراء: انتقل إلى **التدبير وتحديد الموارد \> الإعداد \> المصاريف \> المصاريف التلقائية**.
    - بالنسبة لأوامر الشراء: انتقل إلى **الحسابات المدينة \> إعداد \> إعداد المصاريف \> المصاريف التلقائية**.

1. في جزء القائمة، في الحقل **المستوى** ، حدد المستوى الذي ينطبق عليه المصاريف التلقائية:

    - *الرئيسي* – قم بتطبيق المصاريف على رأس الأمر.
    - *البند* – قم بتطبيق الرسوم على بنود الأمر.

1. حدد المصاريف التلقائية الموجودة لتحريرها، أو حدد **جديدة** لتحديد مصاريف تلقائية جديدة.
1. في القائمة **كود الحساب** ، حدد إحدى القيم التالية لتحديد نطاق الحسابات التي ستتأثر:

    - *الجدول* – قم بتعيين المصاريف لعميل أو مورد معين.
    - *المجموعة* – قم بتعيين المصاريف لمجموعة مصاريف متنوعة.
    - *الكل* – قم بتعيين المصاريف لكافة العملاء أو الموردين.

1. في الحقل **علاقة العميل** أو **علاقة المورد** ، حدد عميل أو مورد معين إذا قمت بتعيين الحقل **كود الحساب** إلى *الجدول*. إذا كنت بتعيين الحقل **كود الحساب** إلى *المجموعة* ، حدد مجموعة مصاريف العميل أو المورد.
1. في الحقل **كود الصنف** ، حدد إحدى القيم التالية لتحديد نطاق الأصناف التي ستتأثر. يمكنك تحديد كود صنف فقط عندما تقوم بتعريف الرسوم التلقائية على مستوى البند.

    - *الجدول* – قم بتعيين المصاريف إلى صنف معين.
    - *المجموعة* – قم بتعيين المصاريف إلى مجموعة مصاريف عنصر.
    - *الكل* – قم بتعيين المصاريف إلى جميع الأصناف.

1. في الحقل **علاقة الصنف** ، حدد صنف معين إذا كنت تقوم بتعيين الحقل **كود الصنف** إلى *الجدول*. إذا قمت بتعيين الحقل **كود الصنف** إلى *المجموعة* ، حدد مجموعة مصاريف الأصناف.
1. **بالنسبة لأوامر المبيعات فقط:** في الحقل **كود وضع التسليم** ، حدد إحدى القيم التالية لتحديد نطاق أوضاع التسليم التي ستتأثر:

    - *الجدول* – قم بتعيين المصاريف لوضع تسليم معين.
    - *المجموعة* – قم بتعيين المصاريف إلى وضع مجموعة التسليم.
    - *الكل* – قم بتعيين المصاريف إلى كل أوضاع التسليم.

1. **بالنسبة لأوامر المبيعات فقط:** في الحقل **وضع علاقة التسليم** ، حدد وضع تسليم محدد إذا قمت بتعيين الحقل **وضع كود التسليم** إلى *الجدول*. إذا قمت بتعيين الحقل **وضع كود التسليم** إلى *المجموعة* ، حدد وضع مجموعة التسليم.
1. في علامة التبويب السريعة **البنود** ، حدد المصاريف ومعدلات المصاريف التي سيتم استخدامها عند تطبيق المصاريف التلقائية الحالية. يمكنك استخدام شريط الأدوات الموجود على علامة التبويب السريع هذه لإضافة العديد من البنود التي تحتاجها. بالنسبة لكل بند، قم بتعيين الحقول التالية:

    - **العملة** – حدد العملة التي يجب استخدامها لحساب المصاريف.
    - **كود المصاريف** – حدد كود المصاريف..
    - **الفئة** – حدد إحدى القيم التالية:

        - *مبلغ ثابت* – يتم إدخال الرسوم كمبلغ ثابت في البند. يمكن استخدام الرسوم الثابتة للرسوم الموجودة في كلاً من البيانات الرئيسية للأمر وفي بنود الأمر.
        - *أصناف دعم الترحيل* – الرسوم تستند إلى الوحدة. يمكن استخدام هذه المصاريف في بنود الأمر فقط. ستظهر عند حساب إجمالي الأمر.
        - *النسبة المئوية* – يتم إدخال المصاريف كنسبة مئوية في البند. يمكن استخدام المصاريف بالنسبة المئوية للمصاريف الموجودة في كلاً من البيانات الرئيسية للأمر وفي بنود الأمر.
        - *النسبة المئوية بين الشركات الشقيقة* - يتم إدخال المصاريف كنسبة مئوية في البند الخاص بالأوامر بين الشركات الشقيقة. يمكن استخدام المصاريف بين الشركات الشقيقة هذه في بنود الأمر فقط.
        - *خارجي* – يتم حساب المصاريف بخدمة جهات أخرى المقترنة بواحد أو أكثر من شركات الشحن.

    - **قيمه المصاريف** – إدخال قيمه المصاريف، استنادًا إلى الفئة التي قمت بتحديدها.
    - **كود عملة المصاريف** – حدد عملة للمصاريف إذا كنت تريد استخدام عملة غير العملة التي قمت بتحديدها في الحقل **عملة**. يمكنك استخدام عملة مختلفة فقط إذا تم تعيين الحقل **نوع المدين** أو **نوع الدائن** على إما *حساب دفتر الأستاذ* أو *الصنف* لكود المصاريف المحددة.
    - **من المبلغ** – حدد مبلغ البدء‬ لتطبيق المصاريف التلقائية عليه. في هذا السياق، المبلغ في يشير إلى إجمالي الأمر.
    - **إلى المبلغ** – حدد مبلغ النهاية لتطبيق المصاريف التلقائية عليه. في هذا السياق، المبلغ في يشير إلى إجمالي الأمر.
    - **مجموعة ضريبة المبيعات** – تحديد مجموعة ضريبة المبيعات.
    - **الموقع** و **المستودع** – حدد موقعًا ومستودعًا إذا كان ينبغي تطبيق المصاريف على موقع ومستودع محددين فقط.
    - **الاحتفاظ** – حدد خانة الاختيار للاحتفاظ بحركات المصاريف بعد الفوترة، حتى يتم تطبيق المصاريف في كل مرة تقوم فيها بإنشاء فاتورة جديدة لحساب العميل المحدد.

1. **بالنسبة لأوامر المبيعات فقط:** إذا كنت تريد حساب مصاريف مرتبطة، راجع [مصاريف مرتبطة على أوامر المبيعات](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders) للحصول على المعلومات.

## <a name="allocate-charges-from-the-header-to-a-line"></a>تخصيص المصاريف من الرأس إلى بند

يوضح الإجراء التالي كيفية تخصيص مصاريف على مستوى الرأس لأحد البنود. قبل البدء في هذا الإجراء، يجب أن يكون لديك بالفعل مصاريف على مستوي الرأس لنوع *المبلغ الثابت* والأمر الذي تنطبق عليه هذه المصاريف. بالإضافة إلى ذلك، يجب أن يتضمن الأمر بالفعل صنف بند واحد على الأقل.

1. افتح أمر الشراء أو أمر الشحن.
1. في جزء الإجراء، اتبع إحدى الخطوات التالية:

    - بالنسبة لأوامر الشراء: في علامة التبويب **شراء** ، في المجموعة **مصاريف** ، حدد **تخصيص المصاريف**.
    - بالنسبة لأوامر المبيعات: في علامة التبويب **بيع** ، في المجموعة **مصاريف** ، حدد **تخصيص المصاريف**.

1. في مربع الحوار **تخصيص المصاريف لبنود الأمر** ، قم بتعيين الحقول التالية:

    - **تخصيص المصاريف** – حدد إحدى القيم التالية لتحديد كيفية تخصيص المصاريف:

        - *المبلغ الصافي* - قم بتخصيص المصاريف وفقًا لكل مبلغ بند مرتبط بإجمالي المبلغ الصافي.
        - *الكمية* – قم بتخصيص المصاريف وفقًا لعدد الوحدات لكل بند مرتبط بإجمالي عدد الوحدات.
        - *للخط* – قم بتخصيص المصاريف بالتساوي بين إجمالي عدد البنود.

    - **تخصيص المصاريف على البنود** – حدد قيمة لتحديد ما إذا كان يجب تخصيص المصاريف لكافة البنود أم للبنود الموجبة فقط أم للبنود السالبة فقط.
    - **تخصيص الكل** – حدد خانة الاختيار هذه لتخصيص مصاريف لبنود أمر الشراء حتى إذا كان كود المصاريف المتنوعة يشتمل على نوع مدين غير *صنف*.
    - **مستلم** – حدد خانة الاختيار هذه لتخصيص مصاريف بنود الأوامر المستلمة فقط.
    - **مخزّن** – حدد خانة الاختيار هذه لتخصيص مصاريف بنود الأوامر المُسجلة في المخزون فقط.
    - **إظهار التحديدات ومسح بنود محددة** – حدد خانة الاختيار هذه لاستبعاد بنود محددة من هذا التخصيص. عند تحديد خانة الاختيار هذه، يتم فتح **اختيار بنود لاستبعادها من شبكة التخصيص**. تتضمن هذه الشبكة البنود التي تطابق المعايير التي يتم تعريفها بواسطة إعدادات **تخصيص المصاريف على البنود** و **المخزنة** فقط. على سبيل المثال، إذا قمت بتعيين الحقل **تخصيص المصاريف على البنود** إلى *البنود الموجبة* وحدد خانة الاختيار **مخزن** ، تظهر الشبكة البنود الموجبة والمسجلة في المخزون فقط. بالإضافة إلى ذلك، تقوم الشبكة تلقائيًا بتصفية أية بنود تم استلام الكمية الكاملة لها. إذا كانت الشبكة مفتوحة، قم بإلغاء تحديد خانة الاختيار **تضمين** لكل بند يجب استبعاده من التوزيع. 

        > [!IMPORTANT]
        > عند العمل باستخدام الشبكة **اختيار بنود لاستبعادها من شبكة التخصيص** ، تأكد من ترك الشبكة مفتوحة حتى تقوم بتحديد **تخصيص**. إذا أغلقت الشبكة قبل تحديد **تخصيص** ، سيتم فقد الإعدادات الخاصة بك في الشبكة. وبالتالي، سيتم تخصيص المصاريف استنادًا إلى المعايير التي قمت بتحديدها مسبقًا.

1. حدد **تخصيص** لتطبيق إعداداتك وأغلق مربع الحوار.