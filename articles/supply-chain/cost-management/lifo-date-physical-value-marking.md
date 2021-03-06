---
title: تاريخ ما يرد أخيرًا يصرف أولاً‬ (LIFO) بالقيمة الفعلية والتمييز
description: تاريخ ما يرد أخيرًا يصرف أولاً‬ (تاريخ LIFO) هو نموذج مخزون مستند إلى مبدأ LIFO. وتتم تسوية الإصدارات من المخزون في مقابل عمليات الاستلام الأخيرة في المخزون، استنادًا إلى تاريخ حركة المخزون‬. ومن خلال استخدام تاريخ LIFO، إذا لم يوجد أية عملية استلام قبل عملية الإصدار، فستتم تسوية عملية الإصدار مقابل أية عمليات استلام تحدث بعد تاريخ الإصدار. وقد يتم تسوية عمليات إصدار عديدة في نفس التاريخ حسب ترتيب عملية الإصدار الأخيرة، وعملية الاستلام الأخيرة.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51592
ms.assetid: d9f13274-3268-444f-85c8-b686fd39286d
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2c06443532519ad5d6c36a6f4ed1f1c4d136664
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967623"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>تاريخ ما يرد أخيرًا يصرف أولاً‬ (LIFO) بالقيمة الفعلية والتمييز

[!include [banner](../includes/banner.md)]

تاريخ ما يرد أخيرًا يصرف أولاً‬ (تاريخ LIFO) هو نموذج مخزون مستند إلى مبدأ LIFO. وتتم تسوية الإصدارات من المخزون في مقابل عمليات الاستلام الأخيرة في المخزون، استنادًا إلى تاريخ حركة المخزون‬. ومن خلال استخدام تاريخ LIFO، إذا لم يوجد أية عملية استلام قبل عملية الإصدار، فستتم تسوية عملية الإصدار مقابل أية عمليات استلام تحدث بعد تاريخ الإصدار. وقد يتم تسوية عمليات إصدار عديدة في نفس التاريخ حسب ترتيب عملية الإصدار الأخيرة، وعملية الاستلام الأخيرة. 

عندما تستخدم تاريخ ما يرد أخيرًا يصرف أولاً‬ (تاريخ LIFO)، إذا لم يوجد أية عملية استلام قبل عملية الإصدار، يتم تسوية عملية الإصدار مقابل أية عمليات استلام تحدث بعد تاريخ الإصدار. ويمكن تسوية عمليات إصدار عديدة في نفس التاريخ حسب ترتيب عملية الإصدار الأخيرة، وعملية الاستلام الأخيرة. عند استخدام تاريخ LIFO، لا يلزمك استخدام قاعدة تاريخ LIFO. ويمكنك وضع علامة على حركات المخزون لكي تتم تسوية عملية محددة من عمليات استلام أحد الأصناف مقابل عملية إصدار معينة. 

يُفضّل إجراء إقفال دوري للمخزون عند استخدام نموذج مخزون تاريخ LIFO. 

توضح الأمثلة التالية أثر استخدام تاريخ LIFO في التكوينات الثلاثة:

-   تاريخ LIFO بدون خيار **تضمين القيمة الفعلية**
-   تاريخ LIFO مع خيار **تضمين القيمة الفعلية**
-   تاريخ LIFO مع وضع علامة

## <a name="lifo-date-without-the-include-physical-value-option"></a>تاريخ LIFO بدون خيار تضمين القيمة الفعلية
في هذا المثال، لا يتم وضع علامة على مجموعة نموذج المخزون لتضمين القيمة الفعلية. يبين الرسم التوضيحي التالي هذه الحركات:

-   1أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 10.00.
-   1ب. الإيصال المالي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 10 ريالات سعودي
-   2أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 20.00.
-   2ب. الإيصال المالي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 20 ريالاً سعوديًا.
-   3أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 25.00.
-   4أ. الصرف الفعلي للمخزون لكمية قيمتها 1 بسعر تكلفة يبلغ 15.00 ر. س. (متوسط تشغيل الحركات التي تم تحديثها ماليًا).
-   4ب. الصرف المالي للمخزون لكمية قيمتها 1 بسعر تكلفة يبلغ 15.00 ر. س. (متوسط تشغيل الحركات التي تم تحديثها ماليًا).
-   5أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 30.00.
-   5ب. الإيصال المالي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 30 ريالاً سعوديًا.
-   6. يتم إجراء إغلاق المخزون. ووفقًا لطريقة تاريخ LIFO، ستتم تسوية آخر صرف تم تحديثه ماليًا مع آخر استلام تم تحديثه ماليًا حسب التاريخ. وسيتم إجراء تعديل بقيمة 5.00 ر. س. في حركة الصرف. حيث ستتم تسوية هذه الحركات مع بعضها البعض.

يعكس سعر تكلفة متوسط التشغيل متوسط الحركات التي تم تحديثها ماليًا عند 15.00 ريال سعودي. 

يُظهر التوضيح التالي آثار نموذج مخزون تاريخ LIFO عند عدم استخدام خيار **تضمين القيمة الفعلية**. ![تاريخ ما يرد أخيرًا يصرف أولاً‬ (LIFO) مع تضمين القيمة الفعلية](./media/lifodatewithoutincludephysicalvalue.gif) 

**مفتاح المخطط**

- تتمثل العمليات المخزنية في شكل أسهم رأسية.
- تتمثل عمليات الاستلام داخل المخزون في شكل أسهم رأسية فوق المخطط الزمني.
- تتمثل الإصدارات خارج المخزون في شكل أسهم رأسية تحت المخطط الزمني.
- تتحدد قيمة حركة المخزون أعلى (أو أسفل) كل سهم رأسي، في التنسيق Quantity@Unitprice.
- تشير قيمة حركة المخزون المحاطة بأقواس إلى أنه قد تم ترحيل حركة المخزون بالفعل إلى المخزون.
- تشير قيمة حركة المخزون غير المحاطة بأقواس إلى أنه قد تم ترحيل حركة المخزون إلى المخزون ماليًا.
- يتم وضع تسمية جديدة لكل حركة إصدار أو استلام جديدة.
- يتم وضع تسمية لكل سهم رأسي تشتمل على معرف متسلسل، مثل *1a*. تشير المعرفات إلى ترتيب ترحيل حركات المخزون في الجدول الزمني.
- تتمثل عمليات إقفال المخزون في شكل خط رأسي أحمر مقطع والتسمية *إقفال المخزون*.
- تتمثل التسويات، التي أجريت قبل إقفال المخزون، في شكل أسهم حمراء مائلة مقطعة تخرج من استلام إلى إصدار.

## <a name="lifo-date-with-the-include-physical-value-option"></a>تاريخ LIFO مع خيار تضمين القيمة الفعلية
يمكنك تحديد خانة الاختيار **تضمين القيمة الفعلية** لصنف في صفحة **مجموعات نماذج الصنف**. وفي هذه الحالة، يستخدم النظام كلاً من حركات الاستلام الفعلية والمالية لحساب سعر تكلفة متوسط التشغيل. وكلما كان ذلك ممكنًا، فسيجري النظام أيضًا تعديلات لحركة الصرف التي تم تحديثها فعليًا. وعند إلغاء تحديد خانة الاختيار **تضمين القيمة الفعلية**، يؤدي إقفال المخزون باستخدام نموذج مخزون تاريخ LIFO‬ إلى إجراء التسويات فقط على الحركات التي يتم تحديثها ماليًا. 

في هذا المثال، يتم وضع علامة على مجموعة نموذج المخزون لتضمين القيمة الفعلية. 

يبين الرسم التوضيحي التالي هذه الحركات:

-   1أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 10.00.
-   1ب. الإيصال المالي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 10 ريالات سعودي
-   2أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 20.00.
-   2ب. الإيصال المالي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 20 ريالاً سعوديًا.
-   3أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 25.00.
-   4أ. صرف فعلي للمخزون لكمية قيمتها 1 بسعر تكلفة يبلغ 18.33 ر. س. لكل كمية (متوسط التشغيل للحركات التي تم تحديثها ماليًا).
-   4ب. صرف مالي للمخزون لكمية قيمتها 1 بسعر تكلفة يبلغ 18.33 ر. س. لكل كمية (متوسط التشغيل للحركات التي تم تحديثها ماليًا).
-   5أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 30.00.
-   5ب. الإيصال المالي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 30 ريالاً سعوديًا.
-   6. يتم إجراء إغلاق المخزون. ووفقًا لطريقة تاريخ LIFO، ستتم تسوية آخر صرف تم تحديثه ماليًا أو تعديله مع آخر استلام تم تحديثه حسب التاريخ. ولن تتم تسوية هذه الحركات ببعضها البعض نظرًا لتعديل حركة الاستلام المالية وفقًا لحركة تحديث فعلية. فبدلاً من ذلك، سيتم فقط إجراء تعديل بقيمة 6.67 ر. س. لحركة الصرف.

يعكس سعر تكلفة متوسط التشغيل متوسط الحركات التي تم تحديثها ماليًا عند 20.00 ريال سعودي. 

يُظهر التوضيح التالي آثار نموذج مخزون LIFO عند استخدام خيار **تضمين القيمة الفعلية**. ![تاريخ ‏‫ما يرد أخيرًا يصرف أولاً‬ (LIFO) مع تضمين القيمة الفعلية](./media/lifodatewithincludephysicalvalue.gif) 

**مفتاح المخطط**

- تتمثل العمليات المخزنية في شكل أسهم رأسية.
- تتمثل عمليات الاستلام داخل المخزون في شكل أسهم رأسية فوق المخطط الزمني.
- تتمثل الإصدارات خارج المخزون في شكل أسهم رأسية تحت المخطط الزمني.
- تتحدد قيمة حركة المخزون أعلى (أو أسفل) كل سهم رأسي، في التنسيق Quantity@Unitprice.
- تشير قيمة حركة المخزون المحاطة بأقواس إلى أنه قد تم ترحيل حركة المخزون بالفعل إلى المخزون.
- تشير قيمة حركة المخزون غير المحاطة بأقواس إلى أنه قد تم ترحيل حركة المخزون إلى المخزون ماليًا.
- يتم وضع تسمية جديدة لكل حركة إصدار أو استلام جديدة.
- يتم وضع تسمية لكل سهم رأسي تشتمل على معرف متسلسل، مثل *1a*. تشير المعرفات إلى ترتيب ترحيل حركات المخزون في الجدول الزمني.
- تتمثل عمليات إقفال المخزون في شكل خط رأسي أحمر مقطع والتسمية *إقفال المخزون*.
- تتمثل التسويات، التي أجريت قبل إقفال المخزون، في شكل أسهم حمراء مائلة مقطعة تخرج من استلام إلى إصدار.

## <a name="lifo-date-with-marking"></a>تاريخ LIFO مع وضع علامة
وضع العلامة هي عملية تسمح لك بربط حركة الإصدار بحركة الاستلام، أو وضع علامة عليهما. يمكن وضع العلامة سواء قبل ترحيل الحركة أو بعده. يمكنك وضع علامات إذا أردت التأكد من التكلفة الدقيقة للمخزون عند ترحيل الحركة أو عند إقفال المخزون. 

على سبيل المثال، قبِل قسم خدمة العملاء أمرًا متسرعًا من عميل مهم. نظرًا لأن هذا أمر عاجل، سيتعين عليك إنفاق المزيد على هذا الصنف لاستيفاء طلب العميل. يجب أن تتأكد من انعكاس تكلفة صنف المخزون هذا في الهامش، أو تكلفة البضائع المبيعة (COGS)، لفاتورة أمر المبيعات هذا. 

عند ترحيل أمر الشراء، يتم استلام المخزون بتكلفة 120.00 دولارًا أمريكيًا. إذا تم وضع علامة على مستند أمر المبيعات هذا لأمر الشراء قبل ترحيل كشف التعبئة أو الفاتورة، ستكون تكلفة البضائع المبيعة هي 120.00 دولارًا أمريكيًا وليست متوسط التكلفة الحالية لهذا الصنف. وإذا كان قد تم ترحيل كشف التعبئة أو الفاتورة قبل وضع العلامة، فسوف يتم ترحيل تكلفة البضائع المبيعة بالمتوسط الساري لسعر تكلفة. 

قبل إجراء إغلاق المخزون، ما يزال يمكن ربط هاتين الحركتين مع بعضهما بعلامة. 

على سبيل المثال، يتم وضع علامة على حركة الاستلام لحركة إصدار. وفي هذه الحالة، سيتم تجاهل طريقة التقييم المحددة في مجموعة نماذج الصنف للصنف، ويقوم النظام بتسوية هذه الحركات مع بعضها البعض. 

يمكنك وضع علامة على حركة إصدار لتلقيها قبل ترحيل الحركة. ويمكنك القيام بذلك من بند أمر مبيعات في صفحة **تفاصيل أمر المبيعات**. ويمكنك عرض حركات الاستلام المفتوحة في صفحة **وضع العلامات**. 

كما يمكنك وضع علامة على حركة إصدار لتلقيها بعد ترحيل الحركة. يمكنك مطابقة أو وضع علامة على حركة إصدار لحركة إيصال مفتوحة لأحد الأصناف المخزنة من دفتر يومية تسوية مخزون تم ترحيله. 

يبين الرسم التوضيحي التالي هذه الحركات:

-   1أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 10.00.
-   1ب. الإيصال المالي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 10 ريالات سعودي
-   2أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 20.00.
-   2ب. الإيصال المالي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 20 ريالاً سعوديًا.
-   3أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 25.00.
-   4أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 30.00.
-   4ب. الإيصال المالي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 30 ريالاً سعوديًا.
-   5أ. الإصدار الفعلي للمخزون لكمية مقدارها 1 بسعر تكلفة 21.25 دولارًا أمريكيًا لكل وحدة (المتوسط الساري للحركات التي تم تحديثها ماليًا وفعليًا).
-   5ب. يتم تمييز الإصدار المالي للمخزون للكمية 1 إلى إيصال استلام المخزون 2b قبل ترحيل الحركة. يتم ترحيل هذه الحركة مقابل سعر تكلفة يبلغ 20.00 ريال سعودي للواحدة.
-   6أ. الإصدار الفعلي للمخزون لكمية قدرها 1 بسعر تكلفة مقداره 21.25 دولارً أمريكيًا لكل وحدة.
-   7. يتم إجراء إغلاق المخزون. ونظرًا لأنه تم وضع علامة على حركة نموذج المخزون ما يرد أولاً يصرف أولاً (FIFO) المحدثة ماليًا وربطها باستلام موجود، فسوف تتم تسوية هذه الحركات ببعضها البعض ولا يتم القيام بأي تعديل.

يعكس متوسط سعر تكلفة التشغيل متوسط الحركات التي تم تحديثها ماليًا وفعليًا عند 27.50 دولارًا أمريكيًا. 

يُظهر التوضيح التالي آثار نموذج مخزون LIFO عند استخدام التمييز بين عمليات الإصدار وعمليات الاستلام. ![تاريخ LIFO مع وضع علامة](./media/lifodatewithmarking.gif) 

**مفتاح المخطط**

- تتمثل العمليات المخزنية في شكل أسهم رأسية.
- تتمثل عمليات الاستلام داخل المخزون في شكل أسهم رأسية فوق المخطط الزمني.
- تتمثل الإصدارات خارج المخزون في شكل أسهم رأسية تحت المخطط الزمني.
- تتحدد قيمة حركة المخزون أعلى (أو أسفل) كل سهم رأسي، في التنسيق Quantity@Unitprice.
- تشير قيمة حركة المخزون المحاطة بأقواس إلى أنه قد تم ترحيل حركة المخزون بالفعل إلى المخزون.
- تشير قيمة حركة المخزون غير المحاطة بأقواس إلى أنه قد تم ترحيل حركة المخزون إلى المخزون ماليًا.
- يتم وضع تسمية جديدة لكل حركة إصدار أو استلام جديدة.
- يتم وضع تسمية لكل سهم رأسي تشتمل على معرف متسلسل، مثل *1a*. تشير المعرفات إلى ترتيب ترحيل حركات المخزون في الجدول الزمني.
- تتمثل عمليات إقفال المخزون في شكل خط رأسي أحمر مقطع والتسمية *إقفال المخزون*.
- تتمثل التسويات، التي أجريت قبل إقفال المخزون، في شكل أسهم حمراء مائلة مقطعة تخرج من استلام إلى إصدار.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]