---
title: الأسئلة الشائعة حول الأنشطة في نهاية السنة
description: تم تجميع هذا الموضوع برمجيًا للمساعدة في أنشطة إقفال نهاية السنة.
author: kweekley
manager: tfehr
ms.date: 01/25/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6d10f54913ca8dff56a59ea597a9bd7c3e69d4bc
ms.sourcegitcommit: bd4763cc6088e114818e80bb1c27c6521b039743
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/02/2021
ms.locfileid: "5107686"
---
# <a name="year-end-activities-faq"></a>الأسئلة الشائعة حول الأنشطة في نهاية السنة 

تم تجميع هذا الموضوع برمجيًا للمساعدة في أنشطة إقفال نهاية السنة. تركز المعلومات الموجودة في هذا الموضوع أساسًا على الأسئلة المتعلقة بأنشطة إغلاق نهاية السنة لدفتر الأستاذ العام والحسابات الدائنة.

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>دفتر الأستاذ العام: كيف أعرف أننا نقوم بتشغيل إنهاء السنة وعدم التراجع عن الإغلاق في نهاية السنة؟
لقد اطلعنا على المؤسسات وهي تحاول تشغيل إغلاق نهاية السنة، ولكنها لم تنفذ تراجعًا عن إغلاق نهاية السنة. إذا تم إنهاء إغلاق نهاية السنة بشكل سريع أو لم ينتج عن إغلاق نهاية السنة الأرصدة الافتتاحية، فقم بالتحقق من صحة الإعداد **التراجع عن الإغلاق السابق** في **‏‫إقفال نهاية السنة‬** (**دفتر الأستاذ العام > إقفال الفترة > ‏‫إقفال نهاية السنة‬ > إجراء الإقفال المالي**). 

[![تشغيل إقفال نهاية السنة مقابل التراجع عن إغلاق نهاية السنة](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

في حالة تعيين القسم **تراجع عن الإغلاق السابق‬‏‫** إلى **نعم**، يتم التراجع عن إغلاق السنة السابقة. عند تشغيل التراجع، سيتم حذف كافة الإدخالات الخاصة برصيد الاقفال والرصيد الافتتاحي، كما لو أنه لم يتم تشغيل إغلاق نهاية السنة. يتم حذف الإيصالات. لن يتم تشغيل إغلاق نهاية السنة تلقائيًا مرة أخرى. يجب عليك بدء العملية مرة أخرى، ولكن هذه المرة بتغيير **تراجع عن الإغلاق السابق‬‏‫** إلى **لا**. 

> [!NOTE]
> اختياريًا، يتم إنشاء إدخال رصيد الإقفال في السنة التي يتم إغلاقها. يحدث ذلك فقط إذا كانت معلمة دفتر الأستاذ العام **‏‫إنشاء حركات إغلاق أثناء التحويل‬** معيّنة إلى **نعم**. دائمًا ما يتم إنشاء إدخال الرصيد الافتتاحي، نظرًا لأنه يكون رصيد البداية للسنه التالية.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>دفتر الأستاذ العام: ما الفرق بين التراجع عن وحذف معلمة الأستاذ العام فيما يتعلق بإقفال نهاية السنة؟
قد يكون هناك التباس في الفرق بين معلمة **تراجع عن الإغلاق السابق‬‏‫‬‏‫**، والتي توجد في مربع الحوار **إغلاق نهاية السنة**، ومعلمة **‏‫حذف قيود الإقفال السنوية أثناء التحويل‬** في دفتر الأستاذ العام (**دفتر الأستاذ العام > إقفال الفترة > ‏‫إقفال نهاية السنة‬ > إجراء الإقفال المالي**).  

[![الفرق بين التراجع عن وحذف معلمة الأستاذ العام فيما يتعلق بإقفال نهاية السنة](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

حدد **تراجع عن الإغلاق السابق** في قائمة الحوار المنسدلة عند تشغيل عملية إغلاق نهاية السنة لحذف جميع إدخالات الرصيد الختامي والرصيد الافتتاحي، كما لو أنه لم يتم تشغيل إغلاق نهاية العام. سيتم حذف الإيصالات. لن يتم تشغيل إغلاق نهاية السنة تلقائيًا مرة أخرى. لتشغيل إقفال نهاية السنة، يجب أن تبدأ هذه العملية مرة أخرى، وبذلك بتغيير **تراجع عن الإغلاق السابق** إلى **لا** (**دفتر الأستاذ العام> إعداد دفتر الأستاذ > معلمات دفتر الأستاذ العام‬‏‫**). 

[![إعداد معلمات دفتر الأستاذ العام](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

يتم استخدام معلمة **‏‫حذف قيود الإقفال السنوية أثناء التحويل‬** في دفتر الأستاذ العام فقط عند تشغيل (دون التراجع عنها) إغلاق نهاية السنة (يتم تعيين **تراجع عن الإغلاق السابق** إلى **لا**). وفي حالة تعيين هذه المعلمة على **نعم**، سيتم حذف كافة إدخالات رصيد الإقفال والرصيد الافتتاحي وسيتم تشغيل إغلاق نهاية السنة مرة أخرى. يتم استخدام هذه العملية عندما تريد المؤسسة إدخال كافة الحركات، بما في ذلك التعديلات منذ آخر نهاية لإقفال السنة، والتي سيتم ترحيلها في إدخال محاسبة واحد لإدخالات رصيد الإقفال والرصيد الافتتاحي. 

إذا تم تعيين هذا الخيار على **لا**، فستبقى جميع إدخالات الرصيد الختامي والرصيد الافتتاحي. ولا يتم حذف الحركات. بدلاً من ذلك، سيتم إنشاء إدخال رصيد إقفال ورصيد افتتاحي جديد فقط لدلتا أو الحركات الجديدة التي تم ترحيلها منذ آخر نهاية للسنه المالية.  

> [!NOTE]
> يتم إنشاء إدخال رصيد الإقفال في السنة التي يتم إغلاقها. يحدث ذلك فقط إذا كانت معلمة **‏‫إنشاء حركات إغلاق أثناء التحويل‬** في دفتر الأستاذ العام معيّنة إلى **نعم**. دائمًا ما يتم إنشاء إدخال الرصيد الافتتاحي، نظرًا لأنه يكون رصيد البداية للسنه التالية. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>دفتر الأستاذ العام: ما الذي يمكن تغييره لتحسين أداء معالجة نهاية السنة؟ 
يمكنك إجراء عدد من التغييرات لتحسين أداء إغلاق نهاية العام. نوصي بتقييم هذه التغييرات المقترحة لمراعاة ما إذا كان التغيير مناسبًا لمؤسسك.  

### <a name="dimension-sets"></a>مجموعات الأبعاد
عند تشغيل إغلاق نهاية السنة، تتم إعادة بناء كل رصيد من مجموعة الأبعاد، مع وجود تأثير مباشر على الأداء. تقوم بعض المؤسسات بإنشاء مجموعات أبعاد بدون داع لأنه تم استخدامها في نقطة واحدة أو ربما تستخدم في مرحلة معينة.  وتستمر إعادة إنشاء مجموعات الأبعاد غير الضرورية هذه أثناء إغلاق نهاية السنة، والذي يضيف وقتًا للعملية. خذ وقتًا لتقييم مجموعات الأبعاد الخاصة بك وحذف أية مجموعات أبعاد غير ضرورية.

تؤثر مجموعات الأبعاد غير الضرورية أيضًا على وظيفة المجموعة **BudgetDimensionFocusInitializeBalance‎** (**دفتر الأستاذ العام > دليل الحسابات > الأبعاد > مجموعات الأبعاد المالية**).

[![مجموعات الأبعاد المالية](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>تكوين قالب إغلاق نهاية السنة
يسمح لك قالب إقفال نهاية السنة للمؤسسات بتحديد مستوى البعد المالي المطلوب الحفاظ عليه عند تحويل أرصدة الأرباح والخسائر إلى الإيرادات المحفوظة. تتيح الإعدادات للمؤسسة الحفاظ على الأبعاد المالية التفصيلية (**إغلاق الكل**) عند نقل الأرصدة إلى الإيرادات المحتجزة أو اختيار تلخيص المبالغ لقيمة بعد واحدة ( **إغلاق مفرد**). ويمكن تحديد ذلك لكل بعد مالي. لمزيد من المعلومات حول هذه الإعدادات، راجع موضوع [إغلاق نهاية السنة](year-end-close.md).

نوصي بتقييم متطلبات مؤسستك وإذا أمكن ذلك، قم بإغلاق أكبر قدر ممكن من الأبعاد باستخدام خيار إغلاق نهاية السنة **إغلاق مفرد‬‏‫** لتحسين الأداء. ومن خلال الإغلاق إلى قيمة بعد واحد (والتي يمكن أن تكون قيمة فارغة أيضًا)، يقوم النظام بحساب تفاصيل أقل عند تحديد الأرصدة لإدخالات حساب الإيرادات المحتجزة.

### <a name="10013-update-or-later"></a>تحديث 10.0.13 أو إصدار لاحق
إذا كنت قد قمت بالتحديث إلى الإصدار الـ 10.0.13 أو الأحدث منذ آخر مرة شغلّت فيها مؤسستك إقفال نهاية السنة، قد يستغرق إجراء إغلاق نهاية السنة مدة أطول نتيجة [لتطبيق ميزة HashV2](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/verify-hash-function-changes-after-update-to-dynamics-365-finance-2020-release-wave-2). (يشير المصطلح *التجزئة* إلى حقل يتم حسابه من حقول سلاسل أخرى. تم تحديث API الخاص بحساب قيمة GUID للتجزئة لتحسين الأمان) لزيادة سرعة عملية إغلاق نهاية السنة، نوصي بإعادة إنشاء أرصدة مجموعات الأبعاد قبل تشغيل إغلاق نهاية السنة. إذا كنت قد قمت بالفعل بإعادة إنشاء أرصدة مجموعة الأبعاد بعد الحصول على تحديث 10.0.13، فليس من الضروري تشغيل عملية إعادة البناء مرة أخرى.
 
## <a name="general-ledger--what-does-the-period-close--year-end-close-do"></a>دفتر الأستاذ العام - ما الذي ينتج عن إقفال الفترة - ‏‫إقفال نهاية السنة‬؟
 
[![إقفال الفترة، إقفال نهاية السنة](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets-new-feature"></a>تحسينات الأداء لإعادة إنشاء مجموعات الأبعاد المالية (ميزة جديدة)
ميزة جديدة تمت إضافتها في الإصدار 10.0.16 تعمل على تحسين أداء عمليات الدمج وإقفال نهاية السنة. تسمى الميزة، تحسينات الأداء لإعادة إنشاء مجموعات الأبعاد المالية. تعمل هذه الميزة على تغيير طريقة إعادة إنشاء مجموعات الأبعاد بحيث يتم إعادة إنشائها لإطار زمني ذي صلة فقط. في الإصدارات السابقة، تمت إعادة إنشاء مجموعات الأبعاد لكافة التواريخ. على سبيل المثال، إذا كنت تقوم بإغلاق السنة 2020، سيقوم النظام فقط بإعادة إنشاء الأرصدة للمعاملات الموجودة في السنة المالية 2020. إذا كنت تقوم بتشغيل الدمج لنطاق تاريخ من 1 نوفمبر 2020 إلى 30 نوفمبر 2020، فان النظام سيقوم بإعادة إنشاء الأرصدة لنطاق التاريخ هذا فقط.

ونظرًا لاعتبار هذه الميزة تغييرًا في الفصل، ستحتاج إلى تمكينها باستخدام مساحة العمل **إدارة الميزات‬**.
 
[![إقفال نهاية السنة](./media/faq-2020-yr-end-06.png)](./media/faq-2020-yr-end-06.png)

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2020"></a>الحسابات الدائنة: ما التغييرات التي تم إجراؤها لدعم تقارير نهاية العام 1099 لـ 2020؟

تمت إضافة ميزتين تنظيميتين جديدتين لتغييرات 1099 نهاية العام في 2020. الميزة الأولي، **تطبق التغييرات على نماذج 1099-NEC ونماذج 1099-MISC لعام 2020**، تم إصدارها من منتصف السنة كميزة إلزامية. والغرض منها هو التأكد من أن بيانات المعاملات لـ 1099 للعام 2020 يمكن تعقبها لنموذج 1099-NEC الجديد. أضافت هذه الميزة حقول 1099 المطلوبة لدعم 1099-NEC الجديد وتحديث حقول 1099-MISC. من خلال هذا التحديث تمت كذلك ترقية بيانات سجل المورد لمعلومات مربع 1099. 

الميزة التنظيمية الثانية، **تم تحديث 1099 عبارة على قانون 2020 الضريبي**، تحتوي على التغييرات التالية.

- 1099-OID - قامت IRS بتحويل النموذج إلى استخدام مستمر.
   - يجب ملء الرقم الثالث والرقم الرابع لسنة التقرير عند الطباعة. استخدم الرقمين الثالث والرابع لحقل **سنة التقرير** من **خيارات طباعه الضرائب 1099**. 

- 1099-NEC - نموذج جديد لعام 2020. يسجل هذا تعويض البطالة. 

-   1099-MISC - بسبب إنشاء نموذج 1099-NEC، قامت IRS بمراجعة النموذج 1099-MISC وأرقام الخانات المُعاد ترتيبها للإبلاغ عن دخل معين.
يتم سرد التغييرات في تقرير الدخل وأرقام الخانات الخاصة بالنموذج أدناه.
   - الممول قام بعمل مبيعات مباشره لمبلغ 5000 دولار أمريكي أو أكثر (خانة اختيار) في الخانة 7.
   - يتم الإبلاغ عن عائدات تأمين المحاصيل في الخانة 9.
   - يتم الإبلاغ عن إجمالي العائدات للنائب في الخانة 10.
   - يتم الإبلاغ عن تأجيلات القسم 409A في الخانة 12.
   - يتم الإبلاغ عن إيراد التعويض المؤجل غير المؤهل في الخانة 14.
   - تُستخدم الخانات 15 و16 و17 للإبلاغ عن ضرائب الولاية المقتطعة ورقم تعريف الولاية ومبلغ الدخل المُحصّل في الولاية على التوالي.

- ولم يتم إجراء أية تغييرات على 1099-DIV أو 1099-INT في 2020.

- ملء إلكتروني – تم تغيير التنسيق ليتوافق مع نموذج NEC الجديد وتغييرات الخانة المتنوعة الموضحة أعلاه. للحصول على معلومات محددة حول متطلبات الملء الإلكتروني، راجع [منشور IRS 1220](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>الحسابات الدائنة: 1099-كيف يمكنني تغيير خانة 1099والقيم لمورد لم يقم بتعقب معلومات 1099 العمل طوال العمل؟
استخدم وظيفة التحديث 1099 (**الحسابات الدائنة > الموردين > كافة الموردين > ‏‫حدد موردًا > علامة تبويب المورد في الشريط > تحديث 1099**) للانتقال خلال معاملات الفاتورة المدفوعة مسبقًا لإعادة تعيين بيانات 1099 بشكلٍ مناسب وفقًا لإعدادات علامة التبويب **ضريبة 1099** في صفحة **المورد**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>هل يمكنني تشغيل التحديث 1099 لكافة الموردين في الوقت نفسه؟
الرقم يتم تنفيذ التحديث 1099 مقابل مورد واحد في كل مرة. إذا كانت هذه المتطلبات مطلوبة من قبل مؤسستك، الرجاء التصويت للفكرة التي تحمل عنوان [العملية المجمّعة لتحديث بيانات 1099 الخاصة بالمورد](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-vs-update-all-in-the-update-1099-utility"></a>الحسابات الدائنة: 1099 – "إعادة حساب مبالغ 1099 الموجودة" في مقابل "تحديث الكل" في أداة مساعدة التحديث 1099.
ستعمل خانة الاختيار **إعادة حساب مبالغ 1099 الموجودة** على إعادة تعيين المبلغ 1099 إلى القيم الإجمالية المدفوعة، عند استخدامها بالاشتراك مع خانة الاختيار **تحديث الكل**. 

[![معاملات الضريبة 1099: قبل تشغيل روتين التحديث](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

وتدخل خانه الاختيار **إعادة حساب المبالغ 1099 الموجودة** فقط في حالة التشغيل عند وجود قيم 1099 جزئية في الفاتورة أو في حاله تعديلها في نموذج الضريبة 1099. على سبيل المثال، افترض أن لديك فاتورة تم تقييمها بقيمة $1000.00، ولكن يقوم المستخدم يدويًا بكتابة مبلغ 1099 في فاتورة بقيمة $500.00.

[![معاملات الضريبة 1099: وضع علامة على "تحديث الكل" و"إعادة حساب مبالغ 1099 الموجودة"](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

عند دفع هذا المبلغ، سيكون مبلغ $500.00 هو المبلغ المدفوع لـ 1099. إذا قمت بإجراء روتين إعادة حساب، سيقوم النظام بتغيير مبلغ 1099 ليصبح $1000.00، وهو الإجمالي الذي تم دفعه.

[![معاملات الضريبة 1099: بعد تشغيل روتين 1099](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>الحسابات الدائنة: 1099 – إنشاء معاملة 1099 يدويًا
قد تحتاج المؤسسة إلى إنشاء معاملات 1099 غير مقترنة بالفاتورة يدويًا. يمكنك إضافة معاملات 1099 اليدوية من خلال الانتقال إلى **الحسابات الدائنة > المهام الدورية > الضريبة 1099 > تسوية المورد لمبالغ 1099**. حدد الزر **معاملات 1099 اليدوية**. 

لا يتم تحديث معاملات 1099 التي تم إنشاؤها يدويًا باستخدام عملية **تحديث الكل** أو **عملية إعادة حساب مبالغ 1099 الموجودة** في الأداة المساعدة **تحديث 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>الحسابات الدائنة: 1099 – هل يدعم Dynamics 365 Finance نموذج 1096؟ 

لا يقوم Dynamics 365 Finance بطباعة التلخيص السنوي 1096 ونموذج إحالة إقرارات المعلومات الأمريكي.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>الحسابات الدائنة: 1099 – هل هناك أية ميزات جديدة تدعم تقرير 1099 للقطاع العام؟ 
تمت إضافة ميزة جديدة للقطاع العام، وهي **تحديث معلومات 1099 بواسطة الحساب الرئيسي** والتي يمكن تفعيلها في مساحة العمل **إدارة المميزات**. تتيح لك هذه الميزة ربط قيم 1099 الخاصة بمورد بالحساب الرئيسي في التوزيع المحاسبي، بدلاً من الحساب الافتراضي في سجل المورد.

لمزيد من المعلومات، راجع [إعداد الموردين لتقارير 1099](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]