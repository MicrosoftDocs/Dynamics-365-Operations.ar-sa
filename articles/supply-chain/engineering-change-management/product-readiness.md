---
title: جاهزية المنتج
description: يشرح هذا المقال كيفيه استخدام عمليات التحقق من الاستعداد لضمان اكتمال البيانات الرئيسية المطلوبة لأحد المنتجات قبل استخدامها في الحركات.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a8e76d5fc786b6f4cac7cd0430399ca3ad13a7bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856211"
---
# <a name="product-readiness"></a>جاهزية المنتج

[!include [banner](../includes/banner.md)]

يمكنك استخدام فحوصات الاستعداد لضمان تحديد كل البيانات الرئيسية المطلوبة لأحد المنتجات قبل استخدامها في الحركات. عند استخدام عمليات فحص الاستعداد ، يتم إعداد مستخدم أو فريق كمسؤول عن التحقق من صحة البيانات المتعلقة بالمنتج المحدد مسبقا.

يمكنك وضع علامة على خانة الاختيار **نشط** لمنتج هندسي أو متغير أو إصدار بعد إدخال كافة البيانات المطلوبة والتحقق منها، وبعد معالجة كافة فحوصات الاستعداد. إذا لم تتم معالجة عملية فحص أو أكثر للمنتج أو الإصدار أو المتغير، فستتلقى تحذيرًا عندما تحاول وضع علامة على خانة الاختيار **نشط** يشير إلى عدم استكمال جميع عمليات الفحص.

يمكنك إنشاء عمليات فحص الاستعداد للمنتجات الهندسية والمتغيرات والإصدارات الجديدة. يمكنك أيضًا تطبيق عمليات الفحص على المنتجات القياسية (غير الهندسية) (انظر أيضًا [عمليات فحص الاستعداد على المنتجات القياسية](#standard-products)). 

يمكنك استخدام المنتجات القياسية في الحركات على الرغم من عدم إكمال جميع فحوصات الاستعداد. إذا كنت بحاجه إلى منع استخدام منتج معين في الحركات، فاستخدم حالة دورة حياته. يمكنك تعيين حالة دورة حياة تقوم بحظر استخدام منتج ما في الحركات، ثم بعد إكمال جميع فحوصات الاستعداد، تعيين حالة جديدة تسمح بالحركات المطلوبة.

## <a name="types-of-readiness-checks"></a>أنواع فحوصات الاستعداد

‏‫هناك ثلاثة أنواع من فحوصات الاستعداد:

- **فحص النظام** – يتحقق النظام مما إذا كان هناك سجل صالح ام لا. علي سبيل المثال ، قد يكون السجل قائمة مكونات صنف (BOM) نشطة.
- **فحص يدوي** - يقوم أحد المستخدمين بالتحقق مما إذا كان السجل صالحا ام لا. علي سبيل المثال ، قد يتطلب فحص الاستعداد التحقق من صحة إعدادات الأمر الافتراضية. في بعض الحالات ، كما هو الحال عندما لا يزال المنتج مصمما التالي لن يتم وضعه في المخزون ، فلا تكون هناك إعدادات افتراضيه للأمر مطلوبه. ومع ذلك ، فان إعدادات الأمر الافتراضية قد تكون مطلوبه لمنتج آخر من نفس النوع ، لأنه يمكن ان يكون المنتج موجودا في المخزون. ويكون المستخدم مسؤولا عن معرفه كيفيه اتخاذ القرار بشكل صحيح ما إذا كان فحص الاستعداد مطلوبا ام لا.
- **قائمه التحقق** – يجيب المستخدم علي سلسله من الاسئله من قائمه اختيار ، ويحدد النظام ما إذا كانت الإجابات تفي بتوقعات. يمكن ان يكون لقائمه الاختيار اي موضوع. علي سبيل المثال ، يمكن استخدامها لتحديد ما إذا كان قد تم إكمال مواد التسويق أو وثائق المنتج.

<a name="checks-engineering"></a>

## <a name="how-readiness-checks-are-created-for-a-new-engineering-product-variant-or-version"></a>كيفية إنشاء عمليات التحقق من الاستعداد لمنتج أو متغير أو إصدار جديد

يمكن تطبيق نهج فحص الاستعداد على مستوى المنتج الذي تم إصداره ومستوى المتغير الذي تم إصداره ومستوى الإصدار الهندسي.

عند إنشاء *منتج هندسي جديد*، يحدد النظام ما إذا كان [نهج فحص الاستعداد ينطبق](#assign-policy) عليه أم لا. في حالة تطبيق نهج فحص الاستعداد، يتم إجراء الأحداث التالية:

- يتم إنشاء عمليات فحص الاستعداد للمنتج ، وفقا للسياسة القابلة للتطبيق.
- تم تعيين الإصدار الهندسي علي غير نشط لحظر استخدام المنتج. يتم تعيين كافة الإصدارات الهندسية للمنتج إلى غير نشطة.

في حالة إنشاء *متغير* لأحد المنتجات، يقوم النظام بالتحقق مما إذا كان نهج فحص الاستعداد ينطبق عليه أم لا. (يمكن تطبيق نهج عمليات فحص الاستعداد على مستوى المنتج الذي تم إصداره ومستوى الإصدار الهندسي.) في حالة تطبيق نهج، يتم إجراء الأحداث التالية:

- يتم إنشاء عمليات فحص الاستعداد للمنتج ، وفقا للسياسة القابلة للتطبيق.
- يتم تعيين الإصدار الهندسي والمتغير على غير نشط لحظر استخدام المنتج.

في حالة إنشاء *الإصدار* الهندسي، يقوم النظام بالتحقق مما إذا كان نهج فحص الاستعداد ينطبق عليه أم لا. (يمكن تطبيق عمليات فحص الاستعداد على مستوى الإصدار الهندسي.) في حالة تطبيق نهج، يتم إجراء الأحداث التالية:

- يتم إنشاء عمليات فحص الاستعداد للمنتج ، وفقا للسياسة القابلة للتطبيق.
- تم تعيين الإصدار الهندسي علي غير نشط لحظر استخدام المنتج.

> [!NOTE]
> يمكنك أيضًا إعداد نُهج التحقق الاستعداد على المنتجات القياسية (غير الهندسية). لمزيد من المعلومات، راجع القسم [عمليات فحص الاستعداد على المنتجات القياسية](#standard-products) لاحقًا في هذا المقال.

## <a name="view-readiness-checks"></a>عرض فحوصات الاستعداد

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>عرض عمليات فحص الاستعداد المفتوحة لمنتج أو لإصدار منتج

للعثور علي عمليات التحقق من الاستعداد المفتوحة لأحد المنتجات، افتح الصفحة **تفاصيل المنتجات التي تم إصدارها**. بعد ذلك، في جزء الإجراءات، في علامة تبويب **المنتج** في مجموعة **عمليات فحص الاستعداد‬**، حدد **عمليات فحص الاستعداد**.

للعثور علي عمليات التحقق من الاستعداد المفتوحة لإصدار المنتج ، افتح صفحه **الإصدارات الهندسية** لمنتج تم إصداره واختر إصدارا. بعد ذلك، في جزء الإجراءات، في علامة تبويب **المنتج** في مجموعة **قائمة التحقق‬**، حدد **عمليات فحص الاستعداد**.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>عرض عمليات فحص الاستعداد المفتوحة التي تم تعيينها لك

لعرض عمليات التحقق من الاستعداد المفتوحة التي تم تعيينها لك ، اتبع أحدي هذه الخطوات.

- الانتقال إلى **أداره التغييرات الهندسيه \> عام \> استعداد المنتج \> عمليات فحص الاستعداد المفتوحة الخاصة بي**.
- انتقل إلى **أداره معلومات المنتج \> مساحات عمل \>جاهزيه المنتجات للتصنيع المنفصل**.

يتم إجراء الإعداد الذي يحدد من يتم تعيين فحص الاستعداد لنهج الاستعداد. يمكن تعيين عمليات التحقق من الجاهزية إلى شخص أو فريق. إذا تم تعيين فحص الاستعداد لفريق ما ، فهناك شخص واحد علي الفريق والذي يجب عليه معالجه فحص الاستعداد.

## <a name="process-open-readiness-checks"></a>معالجه عمليات فحص الاستعداد المفتوح

### <a name="process-system-and-manual-readiness-checks"></a>معالجه اختبارات الاستعداد اليدوية والخاصة بالنظام

بعد فتح صفحه **اختبارات الاستعداد**، يمكنك عرض موضوع عمليات فحص النظام والاستعداد يدويا عن طريق تحديد **المعلومات المتعلقة بالعرض** في جزء الإجراءات. يمكنك عندئذ إكمال و/أو التحقق من صحة البيانات للتحقق من الاستعداد. وتكون لفحوصات الاستعداد المفتوحة **حالة** بالقيمه *معلقه*. تشير هذه الحالة إلى انه يجب الاستمرار في معالجه التحقق من الاستعداد. لمعالجة عملية فحص الاستعداد، اتبع إحدى الخطوات التالية:

- في جزء الإجراءات ، حدد **التحقق/الإكمال** لمراجعه فحص الاستعداد وإكماله. عند الانتهاء ، يتم تحديث حقل **الحالة** إلى *ناجح*.
- في جزء الاجراء ، حدد **تخطي** إذا كنت تريد تخطي تحقق الاستعداد غير إلزامي. علي سبيل المثال ، قم بإعداد فحص الاستعداد لحسابات السعر. ومع ذلك ، فانك تقرر تخطي هذا الفحص اثناء كون المنتج لا يزال في مرحله التصميم. في هذه الحالة ، يتم تحديث الحقل **الحالة** إلى تم *التخطي*.

استنادا إلى تكوين نهج الاستعداد ، وعند تحديث حقل **الحالة** للتحقق من الاستعداد إلى *ناجح* ، فقد يلزم اجراء خطوه اضافيه لاعتماد فحص الاستعداد. في هذه الحالة ، حدد **اعتماد** لإكمال فحص الاستعداد. تكون خطوه الاعتماد هذه إلزاميه دائما عند تخطي فحص الاستعداد.

عندما تتم معالجه كافة عمليات فحص الاستعداد المفتوحة لمنتج أو متغير أو إصدار جديد وتم اعتمادها كما هو مطلوب ، سيصبح الصنف نشطا التالي يكون جاهزا للاستخدام.

### <a name="process-checklist-readiness-checks"></a>معالجه قائمة مراجعة فحص الاستعداد

لفتح أحدي قوائم التحقق، افتح الصفحة **فحوصات الاستعداد**، ثم في جزء الاجراء ، حدد **بدء قائمه الاختيار**. عند إكمال قائمه الاختيار ، يقوم النظام بالتحقق مما إذا كان فحص الاستعداد قد تم تمريره وفقا لإعدادات الاستبيان ام لا. في حاله نجاح عملية الفحص، يتم تحديث الحقل **الحالة** إلى *تم بنجاح*. إذا لم يكن التحقق من الاستعداد إلزاميا ، فيمكنك تخطيه. في هذه الحالة ، يتم تحديث الحقل **الحالة** إلى تم *التخطي*.

استنادا إلى تكوين نهج الاستعداد ، وعند تحديث حقل **الحالة** للتحقق من الاستعداد إلى *ناجح* ، فقد يلزم اجراء خطوه اضافيه لاعتماد فحص الاستعداد. في هذه الحالة ، حدد **اعتماد** لإكمال فحص الاستعداد. تكون خطوه الاعتماد هذه إلزاميه دائما عند تخطي فحص الاستعداد.

عندما تتم معالجه كافة عمليات فحص الاستعداد المفتوحة لمنتج أو متغير أو إصدار جديد وتم اعتمادها كما هو مطلوب ، سيصبح الصنف نشطا التالي يكون جاهزا للاستخدام.

## <a name="create-and-manage-product-readiness-policies"></a>إنشاء سياسات جاهزية المنتج وأدارتها

استخدم سياسة جاهزيه المنتجات لأداره عمليات التحقق من الاستعداد التي تنطبق علي أحد المنتجات. يحتوي كل سياسة جاهزيه علي مجموعه من فحوصات الاستعداد. عند تعيين سياسة الاستعداد إلى فئة منتج هندسي أو منتج مشترك، فإن كافة المنتجات المرتبطة بتلك الفئة أو المنتج المشترك ستكون لها فحوصات الاستعداد التي تم تضمينها في سياسة الاستعداد.

لاستخدام سياسات جاهزية المنتج ، انتقل إلى **أداره التغييرات الهندسية \>  إعداد \> سياسات جاهزية المنتج**. ثم اتبع إحدى الخطوات التالية.

- لإنشاء سياسة جديده ، حدد **جديد** " في جزء الإجراءات، ثم قم بتعيين الحقول كما هو موضح في الأقسام الفرعية التالية.
- لتحرير سياسة موجودة ، قم بتحديدها في جزء القائمة، حدد **تحرير** في جزء الإجراءات، ثم قم بتعيين الحقول كما هو موضح في الأقسام الفرعية التالية.
- لحذف سياسة موجودة، قم بتحديده في جزء القائمة ، وحدد **تحرير** في جزء الإجراءات، ثم في علامة التبويب السريعة **عام**، تاكد من تعيين الخيار **النشط** إلى *لا*. ثم حدد **حذف** في جزء الإجراءات.

### <a name="header"></a>الرأس

قم بتعيين الحقول التالية في راس سياسة جاهزي المنتج.

| الحقل | الوصف |
|---|---|
| الاسم | أدخل اسمًا للسياسة. |
| الوصف | أدخل وصفًا للسياسة. |

### <a name="general-fasttab"></a>علامة التبويب السريعة عام

قم بتعيين الحقول التالية في **عام** سياسة جاهزية المنتج.

| الحقل | الوصف |
|---|---|
| نوع المنتج | يتيح تحديد ما إذا كان النهج ينطبق علي منتجات *الصنف* أو نوع *الخدمة*. لا يمكنك تغيير هذا الإعداد بعد حفظ السجل. |
| نشط | استخدم هذا الخيار للمساعدة في الحفاظ علي سياسة الاستعداد لديك. قم بتعيينها إلى *نعم* لكافة سياسات الاستعداد التي تستخدمها. قم بتعيينها إلى *لا* لوضع علامة غير نشط لسياسة الاستعداد عند عدم استخدامها. لاحظ أنه لا يمكنك إلغاء تنشيط سياسة استعداد تم تعيينها إلى فئة منتج هندسي أو منتج مشترك، ويمكنك فقط حذف سياسة الاستعداد غير النشطة. |

### <a name="readiness-control-fasttab"></a>علام التبويب السريعة التحكم في الاستعداد

بالنسبة لكل نوع من تحققات الاستعداد التي تريد تضمينها في السياسة ، قم باضافه صف علي علامة التبويب السريعة **التحكم في الاستعداد**. استخدم الأزرار التالية الموجودة علي شريط أدوات علامة التبويب السريعة لأضافه الصفوف وأزالتها حسب ما تطلب:

- **أضافه عملية فحص** - أضافه تحقق من الاستعداد القياسي للسياسة. عند تحديد هذا الزر، يظهر مربع الحوار **أضافه تحقق**. هناك، يمكنك التحديد من قائمه عمليات الفحص المتاحة.
- **أضافه استبيان موجود** - أضافه صف فارغ إلى الشبكة. ويمكنك بعد ذلك تعيين استبيان موجود عن طريق تعيين الحقول الموجودة في الجدول التالي.
- **نسخ** - يستخدم في أضافه نسخه من الصف المحدد إلى الشبكة.
- **حذف** – حذف الصف المحدد من الشبكة.

بالنسبة لكل صف تقوم بإضافته، قم بتعيين الحقول التالية.

| الحقل | الوصف |
| --- | --- |
| منطقة العملية | حدد المنطقة التي ترتبط بها عملية الفحص. |
| النوع | يتيح تحديد ما إذا كانت عملية الفحص عبارة عن فحص النظام أو عملية فحص يدوي أو قائمه اختيار (استبيان). |
| الاسم | إذا كانت عملية الفحص قائمه اختيار ، ادخل اسما. بالنسبة لعمليات الفحص اليدوية والنظام ، يتم تعيين هذا الحقل تلقائيا. |
| الوصف | إذا كانت عملية الفحص قائمه اختيار ، ادخل وصفًا. بالنسبة لعمليات الفحص اليدوية والنظام ، يتم تعيين هذا الحقل تلقائيا ، ويوضح الوصف التركيز علي عملية الفحص. |
| تطبيق عمليات التحقق علي | حدد ما إذا كان يجب ان يقوم الصف بإنشاء عمليات فحص الاستعداد كاستجابة لمنتج تم إصداره جديد أو متغير تم إصداره أو إصدار تم إصداره. |
| تنفيذ في | حدد ما إذا كانت الاستعداد يقوم بالتحقق من ان الصف سيتم تطبيقه علي كافة الشركات أو شركه واحده. |
| الشركة | إذا قمت بتعيين **التنفيذ في** الحقل إلى *شركه مفرده*، فحدد الشركة. |
| نوع المالك | حدد ما إذا كان الاستعداد يقوم بإنشاء الصف لكي يتم تعيين الصف لشخص أو لفريق. |
| المالك | حدد الشخص أو الفريق الذي يجب تعيين الصف، الذي تم إنشاؤه من خلال عمليات فحص الاستعداد، له. |
| الاستبيان | حدد الاستبيان الذي ينبغي استخدامه لقائمه الاختيار. تعد قائمه الاختيار بمثابه قائمه اختيار محليه في الشركة التي يتم فيها اجراء فحص الاستعداد. يجب ان يكون النظام قادرا علي تقييم ما إذا كان قد تم الرد علي قائمه الاختيار بشكل صحيح ام لا. التالي ، يجب إعداد قائمه الاختيار بحيث يتم اجراء تقييم استنادا إلى الإجابات الصحيحة. لمزيد من المعلومات حول كيفيه إنشاء استبيانات ، راجع [استخدام الاستبيانات](/dynamicsax-2012/appuser-itpro/using-questionnaires) والمقالات ذات الصلة. |
| اعتماد تلقائي | تتضمن سجلات التحقق من الاستعداد خانه اختيار **معتمده** تشير إلى حاله الاعتماد. حدد خانه الاختيار **الاعتماد التلقائي** عمليات الفحص التي يجب تعيينها ليتم قبولها فورا بعد قيام المستخدم المعين بإكمالها. قم بإلغاء تحديد خانه الاختيار هذه لطلب اعتماد صريح كخطوه اضافيه. |
| إلزامي | حدد خانه الاختيار هذه للشيكات التي يجب إكمالها بواسطة المستخدم المعين. لا يمكن تخطي عمليات الفحص الإلزاميه. |

<a name="assign-policy"></a>

## <a name="assign-readiness-policies-to-standard-and-engineering-products"></a>تعيين سياسات الاستعداد للمنتجات القياسية والهندسية

عند إنشاء منتج جديد استنادًا إلى فئة هندسية، فإنك تقوم بإنشاء كل من *منتج تم إصداره* و *منتج مشترك* مرتبط. تتوقف الطريقة التي يتم بها حل سياسات الجهوزية لمنتج صادر على ما إذا كانت الميزة *عمليات فحص جاهزية المنتج‬* قيد التشغيل لنظامك (راجع القسم [عمليات فحص الجاهزية على المنتجات القياسية‬](#standard-products) لاحقًا في هذا المقال للحصول عل تفاصيل حول هذه الميزة وكيفية تشغيلها أو إيقاف تشغيلها).

- عند *إيقاف تشغيل* الميزة *عمليات فحص الاستعداد للمنتج* على النظام الخاص بك، فإنه يتم تعيين سياسة الاستعداد وعرضها فقط على سجلات [الفئة الهندسية](engineering-versions-product-category.md). لمعرفة السياسة التي تنطبق على منتج تم إصداره، يقوم النظام بالتحقق من الحقل **سياسة استعداد المنتج** لفئة الهندسة ذات الصلة. يمكنك تغيير سياسة الاستعداد لأحد المنتجات الموجودة عن طريق تحرير الفئة الهندسية ذات الصلة (وليس المنتج المشترك).
- عند *تشغيل* الميزة *عمليات فحص الاستعداد للمنتج*، فإنها تضيف الحقل **سياسة استعداد المنتج** إلى الصفحة **المنتج** (حيث يتم إعداد المنتجات المشتركة) والصفحة **المنتج الذي تم إصداره** (حيث تكون القيمة للقراءة فقط ومأخوذة من المنتج المشترك المرتبط). يبحث النظام عن سياسة الاستعداد للحصول على منتج تم إصداره من خلال التحقق من المنتج المشترك المرتبط. عند استخدام فئة هندسية لإنشاء منتج هندسي جديد، يقوم النظام بإنشاء منتج مشترك ومنتج تم إصداره، ونسخ أي إعداد **سياسة استعداد المنتج** لفئة الهندسة إلى المنتج المشترك الجديد. يمكنك حينها تغيير سياسة الاستعداد لأحد المنتجات الموجودة عن طريق تحرير المنتج المشترك ذا الصلة (وليست الفئة الهندسية التي تم إصدارها).

لتعيين سياسة الاستعداد لمنتج مشترك، اتبع الخطوات التالية.

1. انتقل إلى **معلومات المنتج \> المنتجات \> المنتجات**.
1. افتح المنتج الذي ترغب في تعيين سياسة الاستعداد له أو قم بإنشاءه.
1. في علامة التبويب السريعة **عام**، قم بتعيين الحقل **سياسة استعداد المنتج** إلى اسم السياسة الذي ينبغي تطبيقه على المنتج.

لتعيين سياسة الاستعداد لفئة هندسية، اتبع الخطوات التالية.

1. انتقل إلى **إدارة التغيير الهندسي \> إعداد \> تفاصيل فئة المنتج الهندسي**.
1. افتح الفئة الهندسية التي ترغب في تعيين سياسة الاستعداد لها أو قم بإنشائها.
1. في علامة التبويب السريعة **سياسة استعداد المنتج**، قم بتعيين الحقل **سياسة استعداد المنتج** إلى اسم السياسة الذي ينبغي تطبيقه على الفئة الهندسية.

<a name="standard-products"></a>

## <a name="readiness-checks-on-standard-products"></a>عمليات فحص الاستعداد على المنتجات القياسية

يمكنك تمكين عمليات التحقق استعداد المنتجات للمنتجات القياسية (غير الهندسية) عن طريق تشغيل الميزة *عمليات فحص استعداد المنتج* في إدارة الميزات. تقوم هذه الميزة بإجراء بعض التغييرات الصغيرة على نظام التحقق من الاستعداد بحيث يدعم المنتجات القياسية.

### <a name="enable-or-disable-readiness-checks-on-standard-products"></a>تمكين عمليات فحص الجهازية على المنتجات القياسية أو تعطيلها

تتطلب هذه الميزة تشغيل الميزتين *إدارة التغييرات الهندسية* و *عمليات فحص جاهزية المنتج* في النظام. للحصول علي تفاصيل حول كيفية تشغيل هذه الميزات أو إيقاف تشغيلها، راجع [نظرة عامة حول إدارة التغييرات الهندسية](product-engineering-overview.md).

### <a name="create-readiness-policies-for-standard-products"></a>إنشاء سياسات الاستعداد للمنتجات القياسية

تقوم بإنشاء سياسات الاستعداد للمنتجات القياسية تمامًا كما تفعل مع المنتجات الهندسية. راجع المعلومات السابقة في هذا المقال.

### <a name="assign-readiness-policies-to-standard-products"></a>تعيين سياسات الاستعداد للمنتجات القياسية

لتعيين سياسة الاستعداد لمنتج قياسي، افتح المنتج المشترك المرتبط، وقم بتعيين الحقل **سياسة استعداد المنتجات** إلى اسم السياسة التي يجب تطبيقها. لمزيد من المعلومات، راجع القسم [تعيين سياسة الاستعداد إلى المنتجات القياسية والهندسية](#assign-policy) سابقًا في هذا المقال.

### <a name="view-and-process-readiness-checks-on-standard-products"></a>عرض ومعالجة عمليات فحص الاستعداد على المنتجات القياسية

عند تشغيل هذه الميزة، يمكنك عرض عمليات فحص الاستعداد ومعالجتها للمنتجات القياسية تمامًا كما هو الحال بالنسبة للمنتج الهندسي. راجع المعلومات السابقة في هذا المقال.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
