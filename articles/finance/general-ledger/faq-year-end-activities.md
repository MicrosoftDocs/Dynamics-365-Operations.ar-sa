---
title: الأسئلة المتداولة حول أنشطة نهاية السنة
description: يسرد هذا المقال الأسئلة التي يمكن أن تظهر عند إقفال السنة، والإجابات التي يمكن أن تساعد في أنشطة إقفال نهاية السنة.
author: moaamer
ms.date: 12/01/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2e33c1dcbfa4da74f2e8acc6e29f04fda3abd185
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853029"
---
# <a name="year-end-activities-faq"></a>الأسئلة المتداولة حول الأنشطة في نهاية السنة 

[!include [banner](../includes/banner.md)]

يسرد هذا المقال الأسئلة التي يمكن أن تظهر عند إقفال السنة، والإجابات التي يمكن أن تساعد في أنشطة إقفال نهاية السنة. تركز المعلومات الموجودة في هذا المقال بشكل أساسي على الأسئلة المتعلقة بأنشطة إقفال نهاية السنة لدفتر الأستاذ العام والحسابات الدائنة.

## <a name="general-ledger-year-end-enhancements"></a>تحسينات نهاية السنة لدفتر الأستاذ العام

قدم الإصدار 10.0.20 من Microsoft Dynamics 365 Finance تحسينًا لإقفال نهاية السنة. هذا التحسين ممكّن بشكل افتراضي اعتبارًا من الإصدار 10.0.25 وهو إلزامي اعتبارًا من الإصدار 10.0.29. إذا كانت مؤسستك تستخدم إصدارًا يسبق الإصدار 10.0.25، فمن المستحسن أن تقوم بتمكين هذه الميزة قبل أن تبدأ عملية إقفال نهاية السنة. قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام. بإمكان المسؤولين استخدام مساحة عمل **إدارة الميزات** للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة. هناك، يتم إدراج الميزة بالطريقة التالية:

- **الوحدة النمطية:** دفتر الأستاذ العام
- **اسم الميزة:** تحسينات نهاية السنة لدفتر الأستاذ العام

تم نقل إعداد قوالب إقفال نهاية السنة إلى صفحة إعداد جديدة، **إعداد قالب إقفال نهاية السنة**. سوف تصبح صفحة إقفال نهاية السنة الموجودة مماثلة لصفحة **إعادة تقييم العملة الأجنبية لدفتر الأستاذ العام**، حيث تظهر قائمة في كل مرة يتم فيها تشغيل إقفال نهاية السنة أو إلغائه. لن تعرض الصفحة معلومات قديمة حول عمليات إقفال نهاية السنة التي تمت قبل تمكين الميزة. وبإمكان مدير الحسابات بدء إقفال نهاية السنة من الصفحة الجديدة.

لعكس إقفال نهاية السنة، حدد أحدث سنة مالية للكيان القانوني المناسب، ثم حدد **إلغاء إقفال نهاية السنة‬**. ستؤدي عملية الإلغاء إلى حذف الإدخالات المحاسبية لإقفال نهاية السنة السابقة، ولن تعيد تشغيل إقفال نهاية السنة تلقائيًا. إذا قمت بتمكين الميزة **تحسينات نهاية السنة لدفتر الأستاذ العام‬** بعد إكمال إقفال نهاية السنة، وأردت إلغاء نتائج نهاية السنة القديمة، فعليك تشغيل إقفال نهاية السنة القديم من جديد بعد تمكين معلمة دفتر الأستاذ العام **حذف إقفالات نهاية السنة الموجودة عند إعادة إقفال السنة**.

يمكنك إعادة تشغيل إقفال نهاية السنة عن طريق إعادة تشغيل العملية للسنة المالية والكيان القانوني. ستواصل العملية استخدام إعداد معلمة دفتر الأستاذ العام لتحديد ما إذا كانت عملية إعادة تشغيل إقفال نهاية السنة ستأخذ في الحسبان الحركات الجديدة أو المتغيرة فقط، أو إذا كان سيُعاد تشغيل العملية لجميع الحركات وإلغاء الإقفال السابق بشكل تام.

## <a name="general-ledger-the-general-ledger-year-end-enhancements-feature-is-enabled-why-cant-i-view-my-previous-year-closings-in-the-history-section-of-the-year-end-close-page"></a>دفتر الأستاذ العام: تم تمكين ميزة ‏‫تحسينات نهاية السنة لدفتر الأستاذ العام‬. لماذا يتعذّر عليّ عرض عمليات إقفال السنة السابقة في قسم المحفوظات في صفحة إقفال نهاية السنة؟

قبل تمكين الميزة **تحسينات نهاية السنة لدفتر الأستاذ العام‬**، يتم تعقب التاريخ والوقت اللذين تم فيهما تشغيل عملية إقفال نهاية السنة الأخير. ولا يتم تعقب المحفوظات لكل مرة تم فيها تنفيذ إقفال نهاية السنة. وعلى هذا النحو، لن تكون تفاصيل كل عملية تشغيل لإقفال نهاية السنة غير متاحة للعرض. بعد تمكين الميزة، تتم المحافظة على معلومات عملية إقفال نهاية السنة اللاحقة. ويمكن عرض الإيصالات من جميع عمليات إقفال نهاية السنة، حتى تلك التي تم تشغيلها قبل تمكين الميزة، في صفحه **حركات الإيصال**. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-cant-be-run-because-one-or-more-ledger-transactions-posted-into-the-fiscal-year-that-you-are-closing-were-settled-to-a-ledger-transaction-in-a-different-fiscal-year-what-does-this-error-mean"></a>دفتر الأستاذ العام: تفضل عملية إقفال نهاية السنة بسبب الخطأ التالي: "لا يمكن تشغيل إقفال نهاية السنة لأن حركة أو أكثر من حركات دفتر الأستاذ التي تم ترحيلها إلى السنة المالية التي تعمل على إقفالها تمت تسويتها إلى حركة دفتر الأستاذ في سنة مالية مختلفة." ماذا يعني هذا الخطأ؟

نظرًا لتمكين الميزة **الوعي بين تسوية دفتر الأستاذ وإقفال نهاية السنة‬**، تُستبعد من الرصيد الافتتاحي فقط حركات دفتر الأستاذ التي تمت تسويتها من السنة المالية الجاري إقفالها. ويؤدي هذه السلوك إلى عدم وجود رصيد فيما يخص المبالغ المدينة‬ والدائنة. لمزيد من المعلومات، راجع [الوعي بين تسوية دفتر الأستاذ وإقفال نهاية السنة‬](awareness-between-ledger-settlement-year-end-close.md).

## <a name="general-ledger-reversal-of-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-for-112022-cant-be-reversed-because-beginning-balance-transaction-have-been-ledger-settled-in-fiscal-year-112023-what-does-this-error-mean"></a>دفتر الأستاذ العام: فشل إلغاء عملية إقفال نهاية السنة بسبب الخطأ التالي: "لا يمكن إلغاء إقفال نهاية السنة 1/1/2022 نظرًا لتسوية حركة الرصيد في دفتر الأستاذ في السنة المالية 1/1/2023." ماذا يعني هذا الخطأ؟

نظرًا لتمكين الميزة **الوعي بين تسوية دفتر الأستاذ وإقفال نهاية السنة‬**، لا يُسمح بإلغاءات لمعالجة نهاية السنة إذا تمت تسوية الحركات الافتتاحية في السنة المالية الجديدة. قم بإلغاء تسوية دفتر الأستاذ في السنة المالية 2023 الجديدة قبل إلغاء إقفال نهاية السنة في 1 يناير 2022. بدلاً من ذلك، أعد إقفال السنة لتاريخ 1 يناير 2022، ولكن فقط من أجل إدخالات تسوية جديدة. لإعادة إقفال السنة للتسويات فقط، عطّل معلمة دفتر الأستاذ العام **حذف إدخالات نهاية السنة الموجودة عند إعادة إقفال السنة**.

## <a name="general-ledger-why-isnt-the-ledger-settlement-automation-processing-decembers-ledger-settlement-transactions"></a>دفتر الأستاذ العام: لماذا لا يعالج التشغيل التلقائي لتسوية دفتر الأستاذ‬ حركات تسوية دفتر الأستاذ لشهر ديسمبر؟

ستقوم الميزة **التشغيل التلقائي لتسويات دفتر الأستاذ‬** بتشغيل التنفيذ التلقائي للحركات المؤرخة من اليوم الأول من السنة المالية إلى التاريخ الحالي عند تشغيل الحدوث‬. فيما يتعلق بالسنوات المالية التي تنتهي في 31 ديسمبر، قد تضطر إلى تعديل تاريخ الحدوث للتأكد من تشغيله في ديسمبر. علي سبيل المثال، تم إعداد التنفيذ التلقائي بحيث يعمل في اليوم الأول من كل شهر. وسيتم تشغيل التنفيذ التلقائي هذا في 1 ديسمبر 2022، وهو مجدول للعمل في 1 يناير 2023. ننصحك بتغيير الحدوث لتاريخ 1 يناير 2023، بحيث يتم تشغيله بدلاً من 31 ديسمبر 2022. سيضمن هذا التغيير أن تؤخذ في الاعتبار الحركات المؤرخة من 2 إلى 31 ديسمبر للتسوية التلقائية.

## <a name="general-ledger-whats-the-difference-between-the-reverse-year-end-close-action-and-the-delete-existing-year-end-entries-when-reclosing-parameter-for-year-end-close"></a>دفتر الأستاذ العام: ما الفرق بين إجراء "إلغاء إقفال نهاية السنة‬" والمعلمة "حذف إدخالات نهاية السنة الموجودة عند إعادة إقفال السنة‬" لإقفال نهاية السنة؟

قد يكون هناك التباس فيما يتعلق بالفرق بين الإجراء **عكس إقفال نهاية السنة** والمعلمة **حذف إدخالات نهاية السنة الموجودة عند إعادة إقفال السنة‬** في دفتر الأستاذ العام (**دفتر الأستاذ العام \> إعداد دفتر الأستاذ \> معلمات دفتر الأستاذ العام**).

حدد الإجراء **إلغاء إقفال نهاية السنة** عند تشغيل عملية إقفال نهاية السنة لحذف جميع إدخالات الرصيد الختامي والرصيد الافتتاحي، كما لو أن إقفال نهاية السنة لم يتم إطلاقًا. في هذه الحالة، سيتم حذف الإيصالات. ولن يتم تشغيل إقفال نهاية السنة تلقائيًا مرة أخرى. لتشغيل اقفال نهاية السنة، حدد الإجراء **تشغيل إقفال نهاية السنة**.

تُستخدم المعلمة **‏‫حذف إدخالات نهاية السنة الموجودة عند إعادة إقفال السنة‬** في دفتر الأستاذ العام فقط عندما تقوم بتشغيل (وليس إلغاء) إقفال نهاية السنة. إذا تم تعيين هذه المعلمة إلى **نعم**، فسيتم حذف جميع إدخالات الرصيد الختامي والرصيد الافتتاحي، وسيتم تشغيل إقفال نهاية السنة مرة أخرى. يُستخدم هذا الخيار عندما تريد المؤسسة ترحيل كافة الحركات، بما في ذلك التسويات منذ إقفال نهاية السنة الأخير، في إدخال محاسبي واحد لإدخالات الرصيد الختامي والرصيد الافتتاحي. أما إذا تم تعيين المعلمة إلى **لا**، فستبقى جميع إدخالات الرصيد الختامي والرصيد الافتتاحي. ولا يتم حذفها. بدلاً من ذلك، سيتم إنشاء إدخال رصيد ختامي ورصيد افتتاحي جديد فقط لدلتا أو الحركات الجديدة التي تم ترحيلها منذ إقفال نهاية السنة الأخير للسنة المالية.

> [!NOTE]
> يتم إنشاء إدخال الرصيد الختامي في السنة الجاري إقفالها. يحدث ذلك فقط إذا كانت معلمة **‏‫إنشاء حركات إغلاق أثناء التحويل‬** في دفتر الأستاذ العام معيّنة إلى **نعم**. يتم دائمًا إنشاء إدخال الرصيد الافتتاحي، لأنه الرصيد الافتتاحي للسنة التالية.

## <a name="general-ledger-what-is-the-difference-between-close-all-and-close-single-options-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process"></a>دفتر الأستاذ العام: ما الفرق بين الخيارين "إقفال الكل" و"إقفال فردي" في القسم "‏‫تحويل أبعاد الأرباح والخسائر‬" في عملية إقفال نهاية السنة؟

يحافظ الخيار **إقفال الكل** على قيم الأبعاد المالية الأصلية من الحركات المرحّلة ويستخدمها لإنشاء الأرصدة الافتتاحية لحساب الأرباح المحتجزة. سيتم إنشاء أرصدة افتتاحية منفصلة للأرباح المحتجزة لكل مجموعة فريدة من قيم الأبعاد المالية. إذا تم تحديد **إقفال فردي**، فسيتم تلخيص جميع الحركات المرحّلة التي لديها هذا البعد المالي في رصيد افتتاحي للأرباح المحتجزة لقيمة البعد التي تم إدخالها في الحقل الذي يظهر بعد **إقفال فردي**. 

على سبيل المثال، تم ترحيل جميع الحركات للسنة المالية مع بنية الحساب "الحساب الرئيسي - القسم". من البعد المالي "القسم" على القالب، سيكون الخيار **إقفال فردي** محددًا، وتم إدخال الرقم 100 باعتباره قيمة البعد. إذا كان الدخل الإجمالي لجميع الحركات المرحّلة إلى الأقسام 200 و300 و400 هو 100,000 دولار أمريكي، فسيتم إنشاء رصيد افتتاحي واحد للأرباح المحتجزة - 100. إذا حددت **إقفال فردي**، ولكنك تركت قيمة البعد المالي فارغة، فسيتم ترحيل جميع الحركات إلى الأرباح المحتجزة، وستكون قيمة البعد فارغة.

## <a name="general-ledger-when-i-select-close-single-option-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process-will-my-detailed-transactional-information-be-lost"></a>دفتر الأستاذ العام: عندما أحدد الخيار "إقفال فردي" في القسم "‏‫تحويل أبعاد الأرباح والخسائر‬" في عملية إقفال نهاية السنة، هل سيتم فقدان معلومات الحركات المفصلة الخاصة بي؟

يتم استخدام الخيارين **إقفال الكل** و **إقفال فردي** لتحديد الأبعاد المالية في الحركات المرحّلة إلى حسابات الأرباح والخسائر التي سيتم تحويلها إلى الحساب الرئيسي للإيرادات المحتجزة. لا يتأثر الترحيل القديم والمفصل لحسابات الأرباح والخسائر وسيبقى تفصيلاً. يؤثر الخيار على مستوى التفاصيل التي يتم نقلها إلى حسابات الأرباح المحتجزة كرصيد افتتاحي في السنة الجديدة. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-the-reporting-currency-for-the-year-does-not-balance-what-does-this-mean"></a>دفتر الأستاذ العام: فشلت عمليه إقفال نهاية السنة بسبب عدم موازنة عملة التقارير الخاصة بالسنة. ما معنى ذلك؟

يمكن مواجهة هذا الخطأ بعد تمكين الميزة **الوعي بين تسوية دفتر الأستاذ وإقفال نهاية السنة‬** (ميزة الوعي). عند تمكين الميزة، لن يتم تضمين حركات دفتر الأستاذ التي تمت تسويتها في الرصيد الافتتاحي للسنة المالية التالية عند تشغيل إقفال نهاية السنة لدفتر الأستاذ العام. قد يمثل استبعاد حركات دفتر الأستاذ التي تمت تسويتها تحديًا للعملاء عند إقفال نهاية السنة إذا تم تعريف دفتر الأستاذ بعملة التقارير.   
يتم تنفيذ تسوية دفتر الأستاذ لعملة المحاسبة فقط.  عند تسوية حركات دفتر الأستاذ، تضمن عملية التحقق من الصحة فقط المساواة بين المبالغ المدينة لعملة المحاسبة والمبالغ الدائنة لعملة المحاسبة. لا يتم التحقق من صحة مبالغ عملة التقارير لحركات دفتر الأستاذ وقد لا يكون لديها مبالغ مدينة = مبالغ دائنة.  علاوةً على ذلك، لا تحسب تسوية دفتر الأستاذ الأرباح/الخسائر وترحيلها بعملة التقارير بشكل تلقائي.  بسبب هذه القيود، يلزم وجود حركة ربح/خسارة بعملة التقارير عند تنفيذ تسوية دفتر الأستاذ.  إذا لم يتم تضمين الربح/الخسارة في تسوية دفتر الأستاذ، فسينتج عن إقفال نهاية السنة رسالة "خارج الرصيد".  لمزيد من المعلومات، راجع [ميزة الوعي بين تسوية دفتر الأستاذ وعملة التقارير خارج الرصيد](reporting-currency-yec.md).

## <a name="general-ledger-what-can-be-changed-to-help-enhance-the-performance-of-year-end-processing"></a>دفتر الأستاذ العام: ما الذي يمكن تغييره للمساعدة في تحسين أداء معالجة نهاية السنة؟

يمكنك إجراء عدة تغييرات للمساعدة في تحسين أداء إقفال نهاية السنة. نوصي بتقييم هذه التغييرات المقترحة لتحديد ما إذا كانت مناسبة لمؤسسك.

### <a name="optimize-year-end-close-service"></a>تحسين خدمة إقفال نهاية السنة

تعمل خدمة **تحسين إقفال نهاية السنة** على تمكين عملاء Microsoft Dynamics 365 Finance من تسريع إقفال نهاية السنة عن طريق نقل معالجة نهاية السنة الكثيفة إلى خدمة مصغرة. يسمح الوقت الذي يتم توفيره من خلال إقفال نهاية السنة الفعال لكل فريق Finance بالاستجابة في الوقت المناسب على التسويات المطلوبة، ما يؤدي في النهاية إلى إصدار التقارير المالية. تسمح معالجة إقفال نهاية السنة على خدمة مصغرة بتحرير موارد قيّمة. ويؤدي ارتفاع المعالجة إلى تقليل حمل العمل على SQL Server ويمنح العملاء فرصة لتسريع معالجة إقفال نهاية السنة.

تتوفر الخدمة **تحسين إقفال نهاية السنة** في الإصدار 10.0.31، وبالتالي بإمكان المزيد من العملاء استخدام الخدمة الجديدة لموسم نهاية سنة 2022. علاوةً على ذلك، تم إجراء حمل عكسي للخدمة إلى الإصدارين 10.0.30 و10.0.29. لمزيد من المعلومات، راجع [تحسين إقفال نهاية السنة](optimize-year-end-close.md).

### <a name="dimension-sets"></a>مجموعات الأبعاد

عند تشغيل إقفال نهاية السنة، يُعاد بناء رصيد كل مجموعة أبعاد. يؤثر السلوك بشكل مباشر على الأداء. تقوم بعض المؤسسات بإنشاء مجموعات أبعاد بشكل غير ضروري، لأنها كانت مستخدمة في مرحلة ما أو ربما قد يتم استخدامها في مرحلة معينة. نظرًا لإعادة بناء مجموعات الأبعاد غير الضرورية هذه أثناء إقفال نهاية السنة، يُضاف وقت إلى العملية. خذ وقتك لتقييم مجموعات الأبعاد الخاصة بك واحذف تلك التي تعتبرها غير ضرورية.

تؤثر مجموعة الأبعاد غير الضرورية أيضًا على الوظيفة الدفعية **BudgetDimensionFocusInitializeBalance** (**دفتر الأستاذ العام \> دليل الحسابات \> الأبعاد \> مجموعات الأبعاد المالية**).

[![مجموعات الأبعاد المالية.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>تكوين قالب إقفال نهاية السنة

يسمح قالب إقفال نهاية السنة للمؤسسات بتحديد مستوى البعد المالي المطلوب الحفاظ عليه عند تحويل أرصدة الأرباح والخسائر إلى الأرباح المحتجزة. تتيح الإعدادات للمؤسسة الحفاظ على الأبعاد المالية التفصيلية (**إغلاق الكل**) عند نقل الأرصدة إلى الإيرادات المحتجزة أو اختيار تلخيص المبالغ لقيمة بعد واحدة ( **إغلاق مفرد**). ويمكن تحديد ذلك لكل بعد مالي. لمزيد من المعلومات حول هذه الإعدادات، راجع مقال [إغلاق نهاية السنة](year-end-close.md).

نوصي بتقييم متطلبات مؤسستك وإذا أمكن ذلك، قم بإغلاق أكبر قدر ممكن من الأبعاد باستخدام خيار إغلاق نهاية السنة **إغلاق مفرد‬‏‫** لتحسين الأداء. ومن خلال الإقفال إلى قيمة بُعد واحد (والتي يمكن أن تكون قيمة فارغة أيضًا)، يقوم النظام بحساب تفاصيل أقل عند تحديد الأرصدة لإدخالات حساب الإيرادات المحتجزة.

### <a name="degenerate-dimensions"></a>الأبعاد المنحلة

يوفر البُعد المنحل القليل من إعادة الاستخدام أو عدم الاستخدام إطلاقًا من تلقاء نفسه وفي إطار مجموعة تضم أبعادًا أخرى. هناك نوعان من الأبعاد المنحلة. النوع الأول هو بُعد منحل بشكل فردي. سيظهر نوع البُعد المنحل هذا عادةً على حركة واحدة فقط، أو على مجموعات صغيرة من الحركات. أما النوع الثاني فهو بُعد يصبح منحلاً في مجموعة تضم بُعدًا واحدًا إضافيًا أو أكثر يعرض نفس الإمكانات بالاستناد إلى التبديلات المحتملة التي يمكن إنشاؤها. بإمكان البُعد المنحل أن يؤثر بشكل ملحوظ على أداء عملية إقفال نهاية السنة. لتقليل مشاكل الأداء، حدد جميع الأبعاد المنحلة باعتبارها **إقفال فردي** في إعداد إقفال نهاية السنة كما ورد وصفه في القسم السابق.

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2022"></a>الحسابات الدائنة: ما التغييرات التي تم إجراؤها لدعم إعداد تقارير نهاية السنة 1099 لعام 2022؟

#### <a name="update-to-all-1099-forms"></a>تحديث إلى كافة نماذج 1099

تم إجراء التغييرات التالية على جميع النماذج 1099 للسنة الضريبية 2022:

- في عام 2021، تم تعديل السنة على نماذج 1099. بدءًا من عام 2022، يتم ملء السنة بواسطة التقرير.

#### <a name="1099-misc"></a>1099-MISC

تم إجراء التحديثات التالية على النموذج 1099-MISC للسنة الضريبية 2022:

- المربع 13: يُشير الآن إلى ‏‫متطلبات حفظ قانون الامتثال الضريبي للحسابات الخارجية (FATCA)‬.
- المربع 14: يُستخدم الآن للإبلاغ عن مدفوعات المظلات الذهبية الزائدة.
- المربع 15: يُستخدم الآن للإبلاغ عن الدفع بموجب خطط التعويض المؤجل غير المؤهل (NQDC).
- المربع 16: يُستخدم الآن للإبلاغ عن الضرائب المقتطعة للولاية.
- المربع 17: يُستخدم الآن للإبلاغ عن رقم الولاية للدافع.
- المربع 18: يُستخدم الآن للإبلاغ عن دخل الولاية.

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>الحسابات الدائنة: 1099 - كيف يمكنني تغيير خانة 1099 والقيم لمورّد لم يتعقب معلومات 1099 طوال السنة؟

استخدم الوظيفة **تحديث 1099‬** للتنقل عبر حركات الفواتير التي تم تسديدها في السابق وإعادة تعيين بيانات 1099 بطريقة مناسبة، وفقًا للإعدادات على علامة التبويب **الضريبة 1099** في صفحة **المورّد**. لاستخدام الوظيفة **تحديث 1099**، انتقل إلى **الحسابات الدائنة‬ \> المورّدون \> جميع المورّدين**، وحدد مورّدًا، ثم، في جزء الإجراءات، على علامة التبويب **المورّد**، حدد **تحديث 1099**.

## <a name="can-i-run-the-update-1099-functionality-for-all-my-vendors-at-once"></a>هل يمكنني تشغيل الوظيفة "تحديث 1099" لجميع المورّدين لديّ في الوقت نفسه؟

يمكنك استخدام الصفحة **تحديث معلومات 1099 لعدة مورّدين‬** لتحديث المربع 1099 في سجل المورّد، ولتحديث الحركات بالمعلومات الموجودة في المربع 1099. لفتح هذه الصفحة، انتقل إلى **الحسابات الدائنة‬ \> مهمة دورية \> الضريبة 1099**. للوصول إلى الصفحة، يجب أن يكون امتياز الأمان **تحديث مربع وحركات 1099 لمورّدين متعددين** معينًا لك.

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>الحسابات الدائنة: 1099 – إعادة حساب مبالغ 1099 الموجودة في مقابل "تحديث الكل" في الأداة المساعدة للتحديث 1099.

ستعيد خانة الاختيار **إعادة حساب مبالغ 1099 الموجودة** تعيين المبلغ 1099 إلى القيم الإجمالية المدفوعة، عند استخدامها مع خانة الاختيار **تحديث الكل**.

[![حركات الضريبة 1099: قبل تشغيل روتين التحديث.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

لا يبدأ عمل خانة الاختيار **إعادة حساب مبالغ 1099** إلا عند وجود قيم 1099 جزئية في الفاتورة، أو إذا تم تعديل الفاتورة في نموذج الضريبة 1099. على سبيل المثال، لديك فاتورة تبلغ قيمتها 1,000.00 دولار أمريكي، ولكن المستخدم يُدخل يدويًا مبلغ 1099 من 500.00 دولار أمريكي على الفاتورة.

[![حركات الضريبة 1099: وضع علامة على كل من "تحديث الكل" و"إعادة حساب مبالغ 1099 الموجودة".](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

عند تسديل هذه الفاتورة، سيكون مبلغ 500.00 دولار مبلغ 1099 المدفوع. إذا قمت بتنفيذ روتين إعادة الحساب، فسيتغيّر مبلغ 1099 ليصبح 1,000.00 دولار أمريكي، وهو المبلغ الإجمالي الذي تم تسديده.

[![حركات الضريبة 1099: بعد تشغيل روتين 1099.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>الحسابات الدائنة: 1099 – إنشاء معاملات 1099 يدويًا

قد تحتاج المؤسسة إلى إنشاء معاملات 1099 غير مقترنة بالفاتورة يدويًا. يمكنك إضافة معاملات 1099 اليدوية من خلال الانتقال إلى **الحسابات الدائنة \> المهام الدورية \> الضريبة 1099 \> تسوية المورد لمبالغ 1099**. حدد الزر **حركات 1099 اليدوية**.

لا يتم تحديث حركات 1099 التي تم إنشاؤها يدويًا باستخدام عملية **تحديث الكل** أو **إعادة حساب مبالغ 1099 الموجودة** في الأداة المساعدة **تحديث 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>الحسابات الدائنة: 1099 – هل يدعم Dynamics 365 Finance نموذج 1096؟

لا يطبع Dynamics 365 Finance الملخص السنوي 1096 ونموذج إحالة إقرارات المعلومات الأمريكي.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>الحسابات الدائنة: 1099 – هل هناك أية ميزات جديدة تدعم تقرير 1099 للقطاع العام؟

تمت إضافة ميزة جديدة للقطاع العام، وهي **تحديث معلومات 1099 بواسطة الحساب الرئيسي** والتي يمكن تفعيلها في مساحة العمل **إدارة المميزات**. تتيح لك هذه الميزة ربط قيم 1099 الخاصة بمورد بالحساب الرئيسي في التوزيع المحاسبي، بدلاً من الحساب الافتراضي في سجل المورد.

لمزيد من المعلومات، راجع [إعداد الموردين لتقارير 1099](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
