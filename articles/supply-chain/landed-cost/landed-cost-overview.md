---
title: الوحدة النمطية للتكلفة المستلمة
description: تساعد الوحدة النمطية التكلفة المستلمة الشركات في تسهيل عمليات الشحن الواردة وذلك بإعطاء المستخدمين التحكم المالي واللوجيستي الكامل بالشحن الذي تم استيراده، من الشركة المصنعة إلى المستودع.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 2ac62678ca9bf7250271727fe83b8a8ba2fca59b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907424"
---
# <a name="landed-cost-module"></a>الوحدة النمطية للتكلفة المستلمة

[!include [banner](../../includes/banner.md)]

تساعد الوحدة النمطية **التكلفة المستلمة** الشركات في تسهيل عمليات الشحن الواردة وذلك بإعطاء المستخدمين التحكم المالي واللوجيستي الكامل بالشحن الذي تم استيراده، من الشركة المصنعة إلى المستودع. بالنسبة للسلع المستوردة، يمكن للتكاليف المستلمة الحساب للنسبة المئوية 40 بالمائة أو أكثر من التكلفة الإجمالية لكل صنف تم استيراده. وبالتالي، فإن التحدي هو تقديم تقديرات دقيقة للتكاليف المستلمة.

يمكن للشركات استخدام التكلفة المستلمة لإكمال المهام التالية:

- تقدير التكاليف المستلمة وقت إنشاء الرحلة.
- خصص التكاليف المستلمة إلى أصناف متعددة وأوامر شراء أو أوامر التحويل في رحلة واحدة.
- قم بدعم تحويل السلع بين المواقع الفعلية عن طريق التعرف على التكاليف المستلمة.
- التعرف على استحقاقات البضائع في البضاعة بالطريق.

توفر التكلفة المستلمة تقديرات التكلفة دقيقة ومناسبة للتكاليف المستلمة الزائدة. وفي نفس الوقت، فإنها توفر رؤية مالية ولوجيستية متزايدة في سلسلة التوريد الملحقة. كما يساعد أيضًا في تقليل إدارة أخطاء التكاليف.

## <a name="highlights"></a>النقاط الرئيسية

### <a name="voyages"></a>الرحلات البحرية

وفي التكلفة المستلمة، تعتبر الرحلة حركة مميزة من موقع خارجي، من خلال مجموعة محددة من الوجهات عبر فترة محددة، إلى موقع مستودع وارد محدد. يمكن إضافة أوامر الشراء وبنود الأوامر إلى إما حاوية واحدة أو عدة حاويات لرحلة، ويتم تخصيص التكاليف بشكل صحيح مرة أخرى لبند الصنف. 

### <a name="item-ownership"></a>ملكية الصنف

في Microsoft Dynamics 365 Supply Chain Management، يتم استلام البضائع بشكل نموذجي عند وجهة المستودع ثم فوترتها. ومع ذلك، بموجب معظم الاتفاقيات التجارية الدولية، تحصل الشركة على ملكية البضائع من الوقت الذي تغادر فيه المنفذ الأصلي، قبل أن يتم استلامها بالفعل. تعمل التكلفة المستلمة على تمكين الشركات من فوترة البضائع قبل استلامها بالفعل. يُعرف هذا المفهوم بالسلع بأمر النقل. ويقوم بإنشاء نوع جديد من الأمر لإدارة استلام السلع بعد فوترة أمر الشراء الأصلي.

### <a name="costs"></a>تكاليف

عند إنشاء رحلة في التكلفة المستلمة، يمكن إضافة التكاليف تلقائيًا إليها. يتم إعداد هذه التكاليف بالتكلفة المستلمة، وتتوفر في العديد من خيارات التكلفة وقواعد التكلفة لها. يمكن إعداد كل تكلفة لمستويات الرحلات المختلفة التقسيم إلى مستوى الصنف من خلال قواعد التقسيم التي تدعم الكمية والحجم والوزن والمبلغ والمقسومات الحجمية المحددة. تقدم هذه التكاليف التقديرية تقدير دقيق لكافة التكاليف لرحلة.

ثم تقوم التكلفة المستلمة بتشغيل الترحيل/الاستحقاق المبدئي للتكاليف المستلمة المقدرة لضمان توفير حساب دقيق للتكاليف التقديرية في وقت إنشاء الرحلة. وعند فوترة هذه التكاليف التلقائية، يتم عكس التكاليف التقديرية واستبدالها بالتكاليف الفعلية، استنادًا إلى فواتير التكلفة.

تقوم التكاليف الفعلية بعكس التكاليف المقدرة التي يتم ترحيلها في وقت فوترة التكلفة باستخدام مسح الحسابات التي يتم إعدادها لكل نوع من أنواع التكلفة (على سبيل المثال، الرسوم والشحن والتأمين). وتتبع هذه الترحيلات سلوك الترحيل المرتبط بالصنف المحدد. ويقومون تلقائيًا بتحديث ترحيل المخزون، بغض النظر عما إذا كان نوع الترحيل ما يرد أولاً يصرف أولاً (FIFO) أو ما يرد أخيرًا يصرف أولاً (LIFO) أو المتوسط المتحرك المرجح أو متوسط النقل. يتم اعتماد كافة أنواع ترحيل مجموعة نموذج المخزون. بالنسبة لمتوسط النقل وترحيل التكلفة القياسية، تتوفر حسابات نسبة فرق سعر الشراء لترحيل الفروق بين التكاليف التقديرية والتكاليف الفعلية.

### <a name="item-and-order-tracking"></a>تعقب الأصناف والأوامر

وبمجرد انتقال رحلة من الموقع الصادر المنشأ إلى مستودع الوجهة النهائي، يمكن للمستخدمين تحديث كل خطوة أو *المرحلة* للرحلة حسب الحاجة. بالنسبة لكل مرحلة، يتم تحديد وقت الإنتاج وحالة الشحن. يتم أيضًا تعريف تواريخ التسليم المؤكدة للحركة إلى المرحلة التالية للرحلة. ومعًا، توفر تواريخ التسليم هذه تاريخ تسليم المقدر للبضائع إلى المستودع الوارد. يمكن للمستخدمين تغيير تواريخ التسليم هذه. وفي هذه الحالة، يتم تحديث تاريخ التسليم المقدر للبضائع تلقائيًا، وذلك وفقًا لأوقات الإنتاج ومراحل الرحلة. تتوفر الرؤية في البضاعة بالطريق بواسطة الرحلة والسفينة على أساس كل حاوية قبل استلام البضائع. نظرًا لأنه يتم تحديث التواريخ في كل بند من بند أمر الشراء، فإن الشركات تتمتع بمزيد من التحكم في اللوجستية وتخطيط المستودع.

## <a name="landed-cost-concepts"></a>مفاهيم التكلفة المستلمة

يلخص الجدول التالي بعض المفاهيم الأساسية للتكلفة المستلمة.

| المفهوم | الوصف |
|---|---|
| الرحلة البحرية | عادةً ما تكون الرحلة عبارة عن سفينة واحدة. على الرغم من ذلك، استنادًا إلى ممارساتك وإجراءاتك، يمكن أن يكون أحد الموردين أو أحد أوامر الشراء. ولا توجد قيود على استخدام هذا المفهوم. |
| حافظة الأوراق | غالبًا ما يتم تحديد السجل بواسطة لوائح الجمارك. يمكن أن تتكون من سلع مورد واحد شركة/كيان واحد لكل شحنة. يمكن أن تكون السلع في السجل في حاوية واحدة أو حيز بين حاويات متعددة. |
| حاوية الشحن | حاويات الشحن تعمل على تخزين بنود أوامر الشراء. وإنها عبارة عن مستوى أقل من مستوى الشحن. ويتم استخدامها عادة إذا تم تقسيم التكاليف للبضائع حسب الحاوية، أو في حالة إكمال عملية الاستلام لكل حاوية. |
| نوع حاوية الشحن | يمكن لأنواع حاوية الشحن تحديد السعر لنوع تكلفة (على سبيل المثال، الشحن). كما تقدم أيضًا معلومات شحن مفيدة. |
| نوع التكلفة | تحدد أنواع التكلفة التكاليف المرتبطة بعمليات الاستيراد، مثل الرسوم والشحن والتأمين. |
| التكلفة التلقائية | تعمل التكاليف التلقائية مثل الاتفاقيات التجارية. يتم ربط التكلفة التلقائية بمستوى رحلة. |
| المنفذ | إن المنافذ هي المناطق التي يتم فيها استلام البضائع ونقلها منها. |
| الباخرة | إن السفينة هي الوسيلة المستخدمة لنقل البضائع، مثل الشحن أو الطائرة. |
| بضائع قيد النقل | وبناءً على الإعدادات، يتم وضع البضائع في المستودع بالطريق بعد تحديث الفاتورة. |
| النشاط | يمكن استخدام الأنشطة لتخزين كل خطوة من الخطوات الهامة للرحلة بين المنفذين. ويمكن استخدامها لتحديث التواريخ. |
| قالب الرحلة | إن قوالب الرحلة هي المسارات التي تسلكها السلع بين المنفذين. |

للحصول على مقارنه بين المصطلحات والسمات الخاصة بالوحدات النمطية **التكلفة المستلمة** و **إدارة النقل** (TMS)، راجع [التكلفة المستلمة مقابل إدارة النقل](landed-cost-vs-tms.md).
