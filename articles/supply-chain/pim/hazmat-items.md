---
title: المواد الخطرة في المنتجات والأوامر والشحنات والأحمال
description: يوضح هذا المقال كيفية تعيين خصائص المواد الخطرة للمنتجات المُصدرة، وكيفية وضع حدود المخزون في الأصناف الخطرة، وكيفية تضمين المواد الخطرة في أمر مبيعات أو شحنة أو حمل.
author: t-benebo
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaae3ce4916465cd57da65eaa217c40f9c3ea88a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860685"
---
# <a name="hazardous-materials-in-products-orders-shipments-and-loads"></a>المواد الخطرة في المنتجات والأوامر والشحنات والأحمال

[!include [banner](../includes/banner.md)]

يوضح هذا المقال كيفية تعيين خصائص المواد الخطرة للمنتجات المُصدرة، وكيفية وضع حدود المخزون في الأصناف الخطرة، وكيفية تضمين المواد الخطرة في أمر مبيعات أو شحنة أو حمل.

## <a name="set-hazardous-material-specifications-for-products"></a>تعيين مواصفات المواد الخطرة للمنتجات

بعد أن قمت بتعيين لوائح المواد الخطرة وإعداد الرموز المرجعية ذات الصلة على النحو الموضح في [إعداد المواد الخطرة](hazmat-setup.md)، يُمكنك إقران هذه المعلومات بالأصناف المُصدرة. سوف يتم سحب نص الشحن لمستندات الشحن من معلومات المواد الخطرة للأصناف المُصدرة.

كجزء من عملية إقران الصنف المٌصدر بمواد خطرة، يجب عليك تحديد رمز اللائحة والمادة. قد يتم إقران رموز لوائح مختلفة بأحد الأصناف، وفقًا لطرق النقل، ويُمكنك إقران العديد من اللوائح ورموز المواد بكل صنف.

لإعداد مُنتج مُصدر كمادة خطرة، اتبع الخطوات التالية.

1. انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.
1. حدد منتجًا أو قم بإنشائه لفتح صفحة **تفاصيل المنتج الصادر** له.
1. في علامة التبويب السريعة **إدارة المخزون**، عيّن الخيار **المواد الخطرة** إلى **نعم**. يُحدد هذا الإعداد الصنف على أنه بضاعة خطرة ويتم استخدامه عند طباعة وثائق الشحن.
1. في جزء الإجراءات، في مفتاح التبويب **إدارة المخزون** ، في مجموعة **التوافق**، حدد **صنف المواد الخطرة**.
1. قم بملء صفحة **المواد الخطرة للصنفs** للصنف المُحدد باستخدام الحقول الموضحة في الأقسام الفرعية التالية.

### <a name="item-hazardous-materials-header"></a>رأس المواد الخطرة للصنفs 

يوضح الجدول التالي الحقول المتاحة في أعلى صفحة **المواد الخطرة للصنفs**. 

| الحقل | الوصف |
|---|---|
| رقم العنصر | المنتج المٌصدر الذي تعمل باستخدامه. |
| كود اللائحة | حدد لائحة المادة الخطرة التي تنطبق على المادة. تحدد اللائحة كيفية إنشاء نص الشحن المطبوع لصنف وأوضاع التسليم المقترنة. وبعد تعيينه، لا يُمكن تحرير الرمز على هذه الصفحة. ولكن، يُمكنك تعيين رمز لائحة جديد من خلال تحديد **جديد**. |
| كود المادة | (اختياري) حدد رمز المادة الخطرة الذي ينطبق على المنتج. يوفر رمز المادة قالبًا يتضمن قيمًا افتراضية للعديد من الحقول الأخرى في هذه الصفحة. عند تحديد رمز، فسوف يتم نسخ كافة مواصفات المواد الخطرة إلى المنتج الحالي. ولكن، يُطالبك النظام أولًا بالتأكيد على أنه يجب ملء بيانات مواد الصنف من رمز المادة. |
| كود المجموعة | (اختياري) حدد رمز مجموعة تصنيف المواد الخطرة الذي ينطبق على المنتج. أما بالنسبة لحقل **رمز المادة**، عندما تقوم بتحديد رمز، فسوف يتم نسخ جميع مواصفات المواد الخطرة الخاصة به إلى المنتج الحالي. ولكن، يُطالبك النظام أولًا بالتأكيد على أنه يجب ملء بيانات مجموعة فئة الصنف من رمز المجموعة. |

### <a name="descriptions-fasttab"></a>علامة تبويب أوصاف <a name="hazmat-description"></a>

يصف الجدول التالي الحقول المتاحة في علامة التبويب السريعة **الأوصاف**.

| الحقل | الوصف |
|---|---|
| اسم الشحن المناسب | ادخل الوصف القياسي للمادة، كما هو مُحدد بواسطة لائحة المطبقة. يُمكنك توفير ترجمات لهذه القيمة على علامة التبويب السريعة **ترجمة نص شحن الصنف** ، كما هو موضح في القسم التالي. |
| الاسم التقني | حدد الاسم المشترك أو العام للمادة. قد يكون هذا الاسم هو الاسم الذي تستخدمه شركتك داخليًا للمادة. |
| N.O.S. | حدد خانة الاختيار هذه للإشارة إلى أن القيمة **اسم الشحن الصحيح** ليست اسم شحن مُحدد بطريقة أخرى (N.O.S) للصنف. N.O.S. يتم استخدام أسماء الشحن لمجموعات المواد الكيميائية المتشابهة والمواد التي لها استخدامات نهائية مُحددة، ولكنها قد لا تكون مُدرجة بالاسم في جدول المواد الخطرة في لائحة مُعينة.  |

### <a name="item-ship-text-translation-fasttab"></a>علامة التبويب السريعة ترجمة نص شحن الصنف

تحتوي علامة التبويب السريعة **ترجمة نص شحن الصنف** على شبكة تعرض ترجمات لقيم **أسماء الشحن الصحيحة** المُحددة للغة الأساسية في علامة التبويب السريعة **الأوصاف**. يمكن استخدام هذه الترجمات في نص طباعه الشحن للغة واحدة أو أكثر من اللغات الإضافية.

يصف الجدول التالي الحقول المتاحة في علامة التبويب السريعة **ترجمة نص شحن الصنف**.


| الحقل | الوصف |
|---|---|
| اللغة | رمز اللغة المستخدم في الصف. على سبيل المثال، يُشير الرمز **pt-br** إلى اللغة البرتغالية البرازيلية. |
| طباعة نص الشحن | قيمة **اسم الشحن الصحيح** المُترجم باللغة التي يستخدمها الصف. |

لإضافة ترجمة أو تحريرها، حدد **ترجمات** فوق الشبكة لفتح صفحة **ترجمات النص**. ثم اتبع إحدى الخطوات التالية:

- لإضافة ترجمة جديدة، في جزء الإجراءات، حدد **إضافة**. حدد اللغة التي تريد إضافتها، ثم في حقل **النص المُترجم**، ادخل النص المترجم.
- لتحرير ترجمة موجودة، حدد اللغة المستهدفة في حقل **اللغة**، وقم بتحرير النص المترجم في حقل **النص المترجم**، كما هو مطلوب.

### <a name="material-management-fasttab"></a>علامة التبويب السريع إدارة المواد <a name="material-management"></a>

يصف الجدول التالي الحقول المتاحة في علامة التبويب السريعة **إدارة المواد**.

| الحقل | الوصف |
|---|---|
| الدرجة | حدد فئة المادة الخطرة التي ينتمي إليها المنتج، كما هو مُحدد بموجب اللائحة المطابقة للمنتج. يجب تعيين قسم وفئة لكل منتج يتضمن مواد خطرة. |
| الوصف | الوصف المُحدد للفئة المُحددة في حقل **الفئة**. هذا الحقل للقراءة فقط. |
| القسم | حدد قسم المادة الخطرة التي ينتمي إليها المنتج، كما هو مُحدد بموجب اللائحة المطابقة للمنتج. القسم عبارة عن مجموعة فرعية من الفئة. يجب تعيين قسم وفئة لكل منتج يتضمن مواد خطرة. |
| تعريف | حدد رمز تعريف المادة الخطرة. عادةً، يستند هذا الرمز على الوضع القياسي للأمم المتحدة (UN). |
| مجموعة التعبئة | حدد مجموعة التعبئة التي تنطبق على الصنف الحالي. |
| الوصف | الوصف المُحدد للمجموعة المُحددة في حقل **مجموعة التعبئة**. هذا الحقل للقراءة فقط. |
| أوصاف التعبئة | حدد رمز وصف التعبئة المنطبق. يشير هذا الرمز إلى وصف يوضح كيفية تعبئة المنتج. |
| تسميات المواد الخطرة | حدد رمزًا يشير إلى تسمية السلع الخطرة المنطبق الذي يجب تطبيقه على المنتج. |
| كمية محدودة | قم بتعيين هذا الخيار إلى **نعم** للإبلاغ عن إجمالي وزن المنتج المُضمن في كل حمل وفي كل بند من بنود الحمل. |
| الكمية | ادخل كمية المواد الخطرة في المنتج، بالوحدة المُحددة. سوف يتم استخدام هذه القيمة لحساب إجمالي مجموع المواد الخطرة للأحمال والشحنات التي تتضمن المنتج. |
| المضاعف | ادخل المُضاعف الذي سوف يتم تطبيقه عند حساب نتيجة المادة الخطرة لكل بند حمل يتضمنه المنتج. يتم تحديد هذه القيمة حسب اللائحة المنطبقة، وفقًا لنوع المادة الخطرة المضمنة في المنتج. |
| الوحدة | حدد وحدة القياس التي تنطبق على كمية المواد الخطرة في المنتج، على النحو المُحدد في حقل **الكمية**. سوف يتم استخدام هذه القيمة لحساب إجمالي مجموع المواد الخطرة للأحمال والشحنات التي تتضمن المنتج. |

#### <a name="how-the-hazardous-material-score-is-calculated"></a>كيف يتم حساب نقاط المادة الخطرة

يتم استخدام العديد من القيم المُحددة في علامة التبويب السريعة **إدارة المواد** لمنتج لحساب *نتيجة المادة الخطرة* لكل بند حمل يتضمنه ذلك المنتج. يتم حساب النتيجة باستخدام المعادلة التالية:

نتيجة المادة الخطرة = *&lt;LineQty&gt;* × *&lt;HazmatQty&gt;* × *&lt;UnitConversion&gt;* × *&lt;Multiplier&gt;*

فيما يلي مفتاح المعادلة:

- *&lt;LineQty&gt;* هو كمية المنتجات المُحددة لبند الحمل.
- *&lt;HazmatQty&gt;* هو كمية المواد الخطرة المُحدد لمنتج في حقل المواد الخطرة المُحدد لأحد المنتجات في حقل **الكمية** على علامة التبويب السريعة **إدارة المواد**.
- *&lt;UnitConversion&gt;* هو مُعامل التحويل للتحويل بين الوحدة المستخدمة لكمية بند الحمل والوحدة المُحددة لمنتج في حقل **الوحدة** على علامة التبويب السريعة **إدارة المواد**.
- *&lt;المُضاعف&gt;*  هو المُضاعف المُحدد لمنتج في حقل **المضاعف** في علامة التبويب السريعة **إدارة المواد**.

يتم الإبلاغ عن هذه النتيجة لكل بند حمل يحتوي علي منتج  يتم تحديد هذه القيم فيه. لمزيد من المعلومات ، راجع أقسام [الشحنات التي تتضمن مواد خطرة](#hazmat-shipments) و [الأحمال التي تتضمن مواد خطرة](#hazmat-loads) لاحقًا في هذا المقال.

#### <a name="how-the-hazardous-material-weight-is-calculated"></a>كيف يتم حساب وزن المادة الخطرة

سوف يعرض الحمل وبنود الحمل الذي يحتوي على منتجات يتم فيها تعيين خيار **الكمية المحدودة** في علامة التبويب السريعة **إدارة المواد** إلى **نعم** إجمالي وزن المواد الخطرة على النحو المُحدد في الأقسام [الشحنات التي تتضمن مواد خطرة](#hazmat-shipments) و [الأحمال التي تتضمن مواد خطرة](#hazmat-loads) لاحقًا في هذا المقال. يتم حساب وزن المواد الخطرة باستخدام المعادلة التالية:

وزن المواد الخطرة = *&lt;LineQty&gt;* × *&lt;ProductWeight&gt;* × *&lt;UnitConversion&gt;*

فيما يلي مفتاح المعادلة:

- *&lt;LineQty&gt;* هو كمية المنتجات المُحددة لبند الحمل.
- *&lt;ProductWeight&gt;* هو صافي الوزن المُحدد للمنتج، في وحدة المخزون المُحددة للمنتج.
- *&lt;UnitConversion&gt;* هو معامل التحويل للتحويل بين الوحدة المستخدمة لكمية بند الحمل ووحدة المخزون المستخدمة لـ *&lt;ProductWeight&gt;*. 

### <a name="transport-information-fasttab"></a>علامة التبويب السريعة معلومات النقل

يصف الجدول التالي الحقول المتاحة في علامة التبويب السريعة **معلومات النقل**.

| الحقل | الوصف |
|---|---|
| فئة النقل | حدد فئة النقل ذات الصلة. |
| رمز النفق | حدد كود تقييد النفق ذو الصلة الخاص بالصنف. |
| تعبئة المادة الخطرة | حدد كود المرجع المستخدم لمناولة التستيف البحري عند شحن الصنف بحرًا. |
| نوع الطائرة | حدد قيود الطائرات المنطبقة على المادة عند شحنها جوًا. |
| التعبئة - طائرات الشحن فقط | بناءً على القيمة التي حددتها في حقل **نوع الطائرة**، حدد رز تعليمات التعبئة المنطبق عندما يكون شحن المنتج فقط من خلال طائرات البضائع. |
| التعبئة‬ - طائرة شحن وركاب | بناءً على القيمة التي حددتها في حقل **نوع الطائرة**، حدد رز تعليمات التعبئة المنطبق عندما يكون من الممكن شحن المنتج إما من خلال طائرات البضائع أو من خلال طائرات الركاب. |
| IATA Star | قم بتعيين هذا الخيار إلى **نعم** للإشارة إلى أن مواصفات النقل الجوي التي تم إدخالها في علامة التبويب السريعة هذه مرتبطة بمقياس البضائع الخطرة التابع لاتحاد النقل الجوي الدولي (IATA) هذا الحقل للأغراض المعلوماتية فقط. |
| استجابة الطوارئ | حدد الرمز الذي يشير إلى الإرشادات الخاصة بمناولة المواد في حالة الطوارئ. |

### <a name="environmental-information-fasttab"></a>علامة التبويب السريعة للمعلومات البيئية

يصف الجدول التالي الحقول المتاحة في علامة التبويب السريعة **المعلومات البيئية**.

| الحقل | الوصف |
|---|---|
| خطر على البيئة | قم بتعيين هذا الخيار إلى **نعم** للإشارة إلى أن المنتج خطر بيئيًا. استخدم هذا الحقل لأغراض إعداد التقارير الخاصة بك. |
| الملوثات البحرية | قم بتعيين هذا الخيار إلى **نعم** للإشارة إلى أن المنتج من الملوثات البحرية. استخدم هذا الحقل لأغراض إعداد التقارير الخاصة بك. |

## <a name="set-stock-limits-for-hazardous-products"></a><a name="stock-limits"></a> تعيين حدود المخزون للمنتجات الخطرة

لأسباب تتعلق بالسلامة، قد تضطر إلى تحديد إجمالي الكمية لمنتج مُعين يمكن تخزينه في موقع واحد. لتعيين حدود المخزون لمنتج مُصدر، اتبع الخطوات التالية.

1. انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.
1. حدد منتجًا لفتح صفحة **تفاصيل المنتج الصادر** له.
1. في جزء الإجراءات، في مفتاح التبويب **إدارة المخزون** ، في مجموعة **التوافق**، حدد **تفاصيل التقارير**.
1. في الحقول **حد مخزون المواد الخطرة** و **الحد التحذيري للمواد الخطرة**، قم بتعيين القيم المناسبة للمنتج المُحدد.

يتيح لك تقرير **حد مخزون المواد الخطرة** مراقبة مستويات مخزون المواد الخطرة في مواقع المخازن الخاصة بك، للتأكد من بقائها دائمًا ضمن الحدود الآمنة المُحددة هنا. لمزيد من المعلومات، راجع [تقرير حد مخزون المواد الخطرة](hazmat-reports.md#stock-limit-report).

## <a name="sales-order-transactions-that-include-hazardous-materials"></a>حركات أوامر المبيعات التي تتضمن مواد خطرة

لتضمين منتج تم تصنيفه كمادة خطرة في أمر مبيعات، يجب عليك إقران شركة شحن ذات صلة بأمر المبيعات. افتح أمر المبيعات، ثم من علامة التبويب السريعة **التسليم**، قم بتعيين الحقول **شركة الشحن** و **خدمة شركة النقل** كما هو مطلوب.

يتم أيضًا إقران شركة الشحن بوضع التسليم. بالتالي، يجب عليك التأكد من تماشي هذه المعلومات مع لائحة المواد الخطرة. وبمعني آخر، يجب أن يتطابق وضع التسليم المُحدد في لائحة المواد الخطرة مع المواصفات الموجودة في رأس أمر المبيعات. بهذه الطريقة، يتم ربط اللائحة وشركة الشحن والخدمة ببنود الشحن المستخدمة في أمر المبيعات.

بعد إنهاء أمر التوريد وتجهيزه ليتم شحنه، يُمكن إصداره إلى المستودع للإشارة إلى التحويل بين عمليات المبيعات والمستودع.

## <a name="shipments-that-include-hazardous-materials"></a><a name="hazmat-shipments"></a> شحنات تتضمن مواد خطرة

### <a name="view-hazardous-material-scores-for-each-shipment-line"></a>عرض نتائج المواد الخطرة لكل بند شحن

تعرض صفحة **تفاصيل الشحنة** الخاصة بالشحنة إجمالي وزن المواد الخطرة وقيم النقاط التي تم حسابها لكل بند تحميل تم تضمينه في هذه الشحنة. لعرض النقاط والأوزان، اتبع الخطوات التالية.

1. انتقل إلى **إدارة المستودعات \> الشحنات \> جميع الشحنات**.
1. حدد شحنة لفتح صفحة **تفاصيل الشحنة** الخاصة بها.
1. في علامة التبويب السريعة **بنود الحمل**، قم بفحص البنود. بالنسبة لكل بند، سوف ترى حسابات المواد الخطرة في الحقول التالية:

    - **نقاط المواد الخطرة** – يعرض هذا الحقل نقاط المواد الخطرة لبند الحمل. يتم حساب القيمة وفقًا للقواعد والقيم التي تم وضعها للائحة المنطبقة وفي إعداد المنتج المُصدر. تأخذ عملية الحساب الكمية الموجودة في بند الحمل وتشير إلى المضاعف في [إعداد إدارة المواد](#material-management) للمنتج المصدر.
    - **الوزن الصافي للكمية المحدودة** - للمنتجات التي تم وضع علامة منتجات محدودة الكمية عليها بسبب محتوياتها من المواد الخطرة، يظهر هذا الحقل إجمالي الوزن الصافي لمحتوى المواد الخطرة المُضّمن في بند الحمل. يستند الحساب إلى المنتجات التي تم وضع علامة مواد خطرة عليها في إعداد المنتج المُصدر. في حالة وضع علامة صنف محدود الكمية على أحد الأصناف، فسوف تقوم عملية الحساب بأخذ الكمية الموجودة في كل بند من بنود الحمل وتشير إلى الوزن في [إعداد إدارة المواد](#material-management) للمنتج المُصدر.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-shipment"></a>فحص التوافق بين المواد الخطرة المُضمنة في شحنة

يُمكن أن يقوم النظام بتقييم ما إذا كانت جميع المواد الخطرة المضمنة في شحنة ما مناسبة ليتم شحنها معًا. لتقييم التوافق، يقوم النظام بفحص مجموعة التوافق التي تم تعيينها لكل منتج مضمن في الشحنة. لمزيد من المعلومات، راجع [مجموعات توافق المواد الخطرة](hazmat-setup.md#compatibility-groups).

لتشغيل فحص التوافق، اتبع الخطوات التالية.

1. انتقل إلى **إدارة المستودعات \> الشحنات \> جميع الشحنات**.
1. حدد شحنة لفتح صفحة **تفاصيل الشحنة** الخاصة بها.
1. في جزء الإجراءات، في علامة التبويب **الشحنات**، في المجموعة **الإجراءات**، حدد **فحص التوافق**.

سوف تستلم رسالة لإعلامك بنتائج الفحص.

## <a name="loads-that-include-hazardous-materials"></a>أحمال <a name="hazmat-loads"></a> التي تتضمن مواد خطرة

### <a name="view-hazardous-material-scores-for-each-load-line"></a>عرض نتائج المواد الخطرة لكل بند حمل

تعرض صفحة **تفاصيل الحمل** الخاصة بالحمل إجمالي وزن المواد الخطرة وقيم النقاط التي تم حسابها لهذا الحمل ولكل بند حمل. لعرض النقاط والأوزان، اتبع الخطوات التالية.

1. انتقل إلى **إدارة المستودعات\>الشحنات\>جميع الأحمال**.
1. حدد حمل لفتح صفحة **تفاصيل الحمل** الخاصة به. (يُمكنك أيضًا فتح تفاصيل الحمل عن طريق تحديد ارتباط من شحنة ذات صلة.)
1. على علامة التبويب السريعة **الحمل**، يُمكن مراجعة إجمالي نتائج المواد الخطرة والأوزان الخاصة بالحمل بأكمله عن طريق فحص الحقول التالية:

    - **نقاط المواد الخطرة** – يعرض هذا الحقل نقاط المواد الخطرة للحمل. يتم حساب القيمة وفقًا للقواعد والقيم التي تم وضعها للائحة المنطبقة وفي إعداد المنتج المُصدر. تأخذ عملية الحساب الكمية المضمنة في الحمل وتشير إلى المضاعف في [إعداد إدارة المواد](#material-management) للمنتج المصدر.
    - **الوزن الصافي للكمية المحدودة** - للمنتجات التي تم وضع علامة منتجات محدودة الكمية عليها بسبب محتوياتها من المواد الخطرة، يُظهر هذا الحقل إجمالي الوزن الصافي لمحتوى المواد الخطرة المُضّمن في الحمل. يستند الحساب إلى المنتجات التي تم وضع علامة مواد خطرة عليها في إعداد المنتج المُصدر. في حالة وضع علامة صنف محدود الكمية على أحد الأصناف، فسوف تقوم عملية الحساب بأخذ الكمية الموجودة في كل بند من بنود الحمل وتشير إلى الوزن في [إعداد إدارة المواد](#material-management) للمنتج المُصدر.

1. لمراجعة النقاط والأوزان للبنود الفردية، حدد علامة التبويب السريعة **بنود الحمل**. تشبه القيم المتوفرة لكل بند القيم المتوفرة للحمل بالكامل، على النحو الموضح في الخطوة السابقة.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-load"></a>فحص التوافق بين المواد الخطرة المُضمنة في حمل

يُمكن أن يقوم النظام بتقييم ما إذا كانت جميع المواد الخطرة المضمنة في أحد الأحمال مناسبة ليتم شحنها معًا. لتقييم التوافق، يقوم النظام بفحص مجموعة التوافق التي تم تعيينها لكل منتج مضمن في الحمل. لمزيد من المعلومات، راجع [مجموعات توافق المواد الخطرة](hazmat-setup.md#compatibility-groups).

لتشغيل فحص التوافق، اتبع الخطوات التالية.

1. انتقل إلى **إدارة المستودعات\>الشحنات\>جميع الأحمال**.
1. حدد شحنة لفتح صفحة **تفاصيل الحمل** الخاصة بها. (يُمكنك أيضًا فتح تفاصيل الحمل عن طريق تحديد ارتباط من شحنة ذات صلة.)
1. في جزء الإجراءات، في علامة التبويب **الأحمال**، في مجموعة **الإجراءات**، حدد **فحص التوافق**.

سوف تستلم رسالة لإعلامك بنتائج الفحص.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]