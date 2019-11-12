---
title: استخدم مصادر بيانات JOIN في تعيينات نماذج التقارير الإلكترونية للحصول على البيانات من جداول التطبيقات المتعددة.
description: يشرح لك هذا الموضوع كيفية استخدام مصادر البيانات من النوع JOIN في التقارير الإلكترونية (ER).
author: NickSelin
manager: AnnBe
ms.date: 10/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: 224acc19ee5dda430cd9471aa50e9d870a4f8c60
ms.sourcegitcommit: 564aa8eec89defdbe2abaf38d0ebc4cca3e28109
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/28/2019
ms.locfileid: "2667944"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a>استخدم مصادر بيانات JOIN للحصول على البيانات من جداول التطبيقات المتعددة في تعيينات نموذج التقارير الإلكترونية (ER).

[!include[banner](../includes/banner.md)]

أثناء تكوين تعيينات أو تنسيقات نموذج التقارير الإلكترونية (ER)، يُمكنك [إضافة](#review) مصادر البيانات المطلوبة من النوع **JOIN**. في وقت التصميم، يتم تكوين مصدر بيانات **Join** كمجموعة من العديد من مصادر البيانات تقوم كل منها بإرجاع قائمة السجلات. لكل مصدر بيانات باستثناء الأول، فسوف تحتاج إلى تحديد الشروط اللازمة لربط سجلات مصادر البيانات الحالية والسابقة. في وقت التشغيل، يقوم مصدر البيانات المُكون لنوع **JOIN** [بإرجاع](#executeERformat) قائمة سجلات مرتبطة واحدة للسجلات التي تحتوي على حقول من سجلات مصادر البيانات المتداخلة.

يتم حاليًا اعتماد أنواع الصلات التالية:

- صلة خارجية (يُسرى):
    - ربط كافة السجلات الخاصة بمصدر البيانات الأول (أقصى اليسار) ثم أي مطابقة وفقًا لسجلات الشروط المكونة من مصدر البيانات الثاني (أقصى اليمين).
- الربط الداخلي (الأيمن):
    - ربط فقط السجلات الخاصة بمصدر البيانات الأول (أقصى اليسار) وسجلات مصدر البيانات الثاني (أقصى اليمين) المتطابقة مع بعضها البعض وفقًا للشروط المكونة.

في مصدر بيانات **الربط** الذي تم تكوينه، عندما تكون كافة مصادر البيانات هي من النوع **سجلات الجدول** ، ويمكن أداء تنفيذ مصدر بيانات الربط على [مستوي قاعدة البيانات](#analyze) باستخدام عبارة SQL مفردة. يؤدي ذلك إلى تقليل عدد استدعاءات قواعد البيانات، التي تعمل علي تحسين أداء تعيين النموذج. وبخلاف ذلك، يتم إجراء تنفيذ مصدر **بيانات الربط** في الذاكرة.

> [!NOTE]
> لم يتم تدعيم استخدام الوظيفة **VALUEIN** بعد في تعبيرات التقارير الإلكترونية التي تحدد شروط سجلات الربط في مصادر البيانات لنوع الربط. قم بزيارة الصفحة [مصمم التركيبة في التقارير الإلكترونية‬](general-electronic-reporting-formula-designer.md) للمزيد من التفاصيل حول هذه الوظيفة.

لمعرفة المزيد حول هذه الميزة، أكمل المثال في هذا الموضوع.

## <a name="example-use-join-data-sources-in-er-model-mappings"></a>مثال: استخدام مصادر بيانات JOIN في تعيينات نموذج التقارير الإلكترونية

توضح الخطوات التالية كيفية قيام مسؤول النظام أو مطور التقارير الإلكترونية بتكوين تعيين نموذج التقارير الإلكترونية (ER) للحصول علي البيانات من جداول التطبيقات المتعددة مرة واحدة باستخدام مصادر البيانات من النوع **JOIN** لتحسين أداء الوصول إلى البيانات. يمكن تنفيذ هذه الخطوات في أي شركة Dynamics 365 Finance أو خدمات التكوين التنظيمية (RCS)‬.

### <a name="prerequisites"></a>المتطلبات الأساسية

لإكمال الأمثلة الموجودة في هذا الموضوع، يجب أن يكون لديك حق الوصول إلى أي مما يلي اعتمادًا على الخدمة المستخدمة للتنافس على هذه الخطوات:

**الوصول إلى Finance لأحد الأدوار التالية:**

- مطور إعداد التقارير الإلكتروني
- مستشار وظيفي لإعداد التقارير الإلكتروني
- مسؤول النظام

**الوصول إلى RCS لأحد الأدوار التالية:**

- مطور إعداد التقارير الإلكتروني
- مستشار وظيفي لإعداد التقارير الإلكتروني
- مسؤول النظام

يجب أولاً إكمال الخطوات المذكورة في الإجراء [إنشاء موفر تكوين ووضع علامة عليه على أنه نشط](tasks/er-configuration-provider-mark-it-active-2016-11.md).

مقدمًا، يجب أيضا تنزيل من [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=000000) وحفظ نموذج ملفات تكوين التقارير الإلكترونية التالي محليًا:

| **وصف المحتوى**  | **اسم الملف**   |
|--------------------------|-----------------|
| نموذج لملف تكوين **نموذج بيانات التقارير الإلكترونية** ، الذي يستخدم كمصدر بيانات لهذه الأمثلة.| [نموذج لمعرفة مصادر بيانات JOIN.الإصدار1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| نموذج لملف تكوين **تعيين نموذج‬ التقارير الإلكترونية** ، الذي يُطبق نموذج بيانات التقارير الإلكترونية لهذه الأمثلة. | [تعيين لمعرفة مصادر بيانات JOIN.الإصدار1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| نموذج ملف تكوين **تنسيق التقارير الإلكترونية** . يصف هذا الملف البيانات المطلوبة لملء مكون تنسيق التقارير الإلكترونية للأمثلة. | [تنسيق لمعرفة مصادر بيانات JOIN.الإصدار1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="activate-a-configurations-provider"></a>تنشيط موفر تكوينات

1. الوصول إما إلى Finance أو RCS في الجلسة الأولي لمستعرض الويب الخاص بك.
2. انتقل إلى **إدارة المؤسسة \> مساحات العمل \> إعداد التقارير الإلكترونية**.
3. في الصفحة **ترجمة التكوينات** ، في قسم **موفري التكوين** ، تحقق من أن موفر التكوين لنموذج الشركة Litware, Inc. (http://www.litware.com) مُدرج ومعلم كـ **نشط**. إذا لم تطلع على موفر التكوين هذا، فاتبع الخطوات في إجراء [إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬](tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![مساحة عمل إعداد التقارير الإلكترونية](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a>استيراد نموذج ملفات تكوين التقارير الإلكترونية .

1. حدد **تكوينات إعداد التقارير‬**.
2. استيراد ملف تكوين نموذج بيانات التقارير الإلكترونية.
    1. حدد **تبادل**.
    2. حدد **تحميل من ملف XML**.
    3. حدد **استعراض** للاطلاع علي ملف **نموذج لمعرفة مصادر بيانات JOIN.الإصدار1.1.xml** .
    4. حدد **موافق**.
3. استيراد ملف تكوين تعيين نموذج التقارير الإلكترونية.
    1. حدد **تبادل**.
    2. حدد **تحميل من ملف XML**.
    3. حدد **استعراض** للعثور علي ملف **تعيين لمعرفة مصادر بيانات JOIN.الإصدار1.1.xml** .
    4. حدد **موافق**.
4.  استيراد ملف تكوين تنسيق التقارير الإلكترونية.
    1. حدد **تبادل**.
    2. حدد **تحميل من ملف XML**.
    3. حدد **استعراض** للعثور علي ملف **تنسيق لمعرفة مصادر بيانات JOIN.الإصدار1.1.xml** .
    4. حدد **موافق**.
5.  في شجرة التكوينات، قم بتوسيع عنصر **نموذج لمعرفة مصادر بيانات JOIN** بالإضافة إلى عناصر النموذج الأخرى (عند توافرها).
6.  لاحظ قائمة تكوينات التقارير الإلكترونية في الشجرة بالإضافة إلى تفاصيل الإصدار في علامة التبويب السريعة **الإصدارات** – سيتم استخدامها كمصدر للبيانات الخاصة بنموذج التقرير الخاص بك.

    ![صفحة تكوينات إعداد التقارير الإلكترونية](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a>تشغيل خيارات تتبع التنفيذ
1.  تحديد **تكوينات**.
2.  تحديد **معلمات المستخدم**.
3.  قم بتعيين معلمات تتبع التنفيذ كما هو موضح في لقطه الشاشة أدناه.

    ![صفحة معلمات إعداد التقارير الإلكترونية](./media/GER-JoinDS-Parameters.PNG)

    مع تشغيل هذه المعلمات، لكل عمليه تنفيذ لملف تنسيق إعداد التقارير الإلكترونية المستوردة، سيتم إنشاء تتبع التنفيذ. باستخدام تفاصيل تتبع التنفيذ الذي تم إنشاؤه، يمكنك تحليل تنفيذ تنسيق إعداد التقارير الإلكترونية ومكونات تعيين نموذج إعداد التقارير الإلكترونية. قم بزيارة صفحة [تنفيذ تتبع تنسيق إعداد التقارير الإلكترونية لاستكشاف الأخطاء في المشكلة وإصلاحها](trace-execution-er-troubleshoot-perf.md) للحصول على المزيد من التفاصيل حول ميزه تتبع تنفيذ إعداد التقارير الإلكترونية.

### <a name="review-er-model-mapping-part-1"></a>مراجعة تعيين نموذج إعداد التقارير الإلكترونية (الجزء 1)

مراجعة إعدادات مكون تعيين نموذج إعداد التقارير الإلكترونية. يتم تكوين المكون للوصول إلى معلومات حول إصدارات تكوينات إعداد التقارير الإلكترونية وتفاصيل التكوينات وموفري التكوين دون استخدام مصادر بيانات من نوع **الربط** .

1.  حدد تكوين **تعيين لمعرفة مصادر بيانات JOIN** .
2.  حدد **المصمم** لفتح قائمة التعيينات.
3.  حدد **المصمم** لمراجعة تفاصيل التعيين. 
4.  حدد **إظهار التفاصيل**.
5.  في شجره التكوينات، قم بتوسيع عناصر نموذج بيانات **Set1** و **Set2.Details** :

    1. يُشير ربط **تفاصيل: قائمه السجلات = الإصدارات** إلى ربط العنصر **Set1.Details** بمصدر بيانات **الإصدارات** التي تُرجع سجلات الجدول **ERSolutionVersionTable** . يمثل كل سجل في هذا الجدول إصدارا واحدًا لتكوين التقارير الإلكترونية. يتم تقديم محتوي هذا الجدول في علامة التبويب السريعة **إصدارات** في الصفحة **تكوينات** .
    2. يُقصد بربط **ConfigurationVersion: String = @.PublicVersionNumber** أن قيمه الإصدار العام لكل إصدار من تكوين التقارير الإلكترونية مأخوذ من الحقل **PublicVersionNumber** الموجود في جدول **ERSolutionVersionTable** ويتم وضعه في العنصر **ConfigurationVersion** .
    3. يُشير الربط **ConfigurationTitle: String = @.'>Relations'.Solution.Name** إلى أن اسم تكوين التقارير الإلكترونية مأخوذ من حقل **Name** الخاص بجدول **ERSolutionTable** مُقيمًا باستخدام علاقة العديد إلى واحد (**'>Relations'**) بين الجدولين **ERSolutionVersionTable** و **ERSolutionTable** . يتم تقديم أسماء تكوينات التقارير الإلكترونية لمثيل التطبيق الحالي في شجرة التكوينات في الصفحة **تكوينات** .
    4. يُقصد بالربط **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** أن اسم موفر التكوين المالك للتكوين الحالي مأخوذ من حقل **Name** الخاص بجدول **ERVendorTable** مُقيمًا باستخدام علاقة العديد إلى واحد بين الجدولين **ERSolutionTable** و **ERVendorTable** . يتم تقديم أسماء مقدمي تكوينات التقارير الإلكترونية في شجرة التكوينات في الصفحة **تكوينات** على رأس الصفحة لكل تكوين. يمكن الاطلاع علي قائمة موفري تكوينات التقارير الإلكترونية بالكامل من الصفحة **‏‫إدارة المؤسسة \> التقارير الإلكترونية \> موفر التكوين** .

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/GER-JoinDS-Set1Review.PNG)

6.  في شجره التكوينات، قم بتوسيع عنصر نموذج البيانات **Set1.Summary** :

    1. يُشير ربط **VersionsNumber: عدد صحيح = VersionsSummary.aggregated.VersionsNumber** إلى ربط العنصر **Set1.Summary.VersionsNumber** بحقل تجميع **VersionsNumber** لمصدر بيانات **VersionsSummary** لنوع **GroupBy** الذي تم تكوينه لإرجاع عدد السجلات للجدول **ERSolutionVersionTable** من خلال مصدر بيانات **الإصدارات** .

    ![صفحه معلمات مصدر البيانات GROUPBY](./media/GER-JoinDS-Set1GroupByReview.PNG)

7.  قم بإغلاق الصفحة.

### <a name="review"></a> مراجعة تعيين نموذج التقارير الإلكترونية (الجزء 2)

مراجعة إعدادات مكون تعيين نموذج إعداد التقارير الإلكترونية. يتم تكوين المكون للوصول إلى معلومات حول إصدارات تكوينات التقارير الإلكترونية وتفاصيل التكوينات وموفري التكوين مع استخدام مصادر بيانات نوع **JOIN** .

1.  في شجره التكوينات، قم بتوسيع عناصر نموذج بيانات **Set2** و**Set2.Details** : لاحظ أن الربط **تفاصيل: قائمة السجل = تفاصيل** تشير إلى أنه تم ربط عنصر **Set2.Details** بمصدر البيانات **التفاصيل** الذي تم تكوينه كمصدر بيانات لنوع **Join** .

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/GER-JoinDS-Set2Review.PNG)

    يمكن إضافة مصدر بيانات **Join** بتحديد مصدر بيانات **‏‫Functions/Join** :

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/GER-JoinDS-AddJoinDS.PNG)

2.  حدد مصدر بيانات **تفاصيل**.
3.  حدد **تحرير** في جزء **مصادر البيانات** .
4.  حدد **تحرير الربط**.
5.  حدد **إظهار التفاصيل**.

    ![صفحة معلمات مصدر البيانات JOIN](./media/GER-JoinDS-JoinDSEditor.PNG)

    تستخدم هذه الصفحة لتصميم مصدر البيانات المطلوب لـ **نوع الربط**. في وقت التشغيل، سيقوم مصدر البيانات هذا بإنشاء قائمة سجلات مرتبطة مفردة من مصادر البيانات في شبكة **القائمة المرتبطة**. يتم بدء ربط السجلات من مصدر البيانات **ConfigurationProviders** الموجود في الشبكة كأول عمود (في عمود **النوع** الفارغ المخصص له). سوف يتم ربط سجلات كل مصدر بيانات آخر بسجلات مصدر البيانات الأصلي تبعًا لذلك استنادًا إلى ترتيبها في هذه الشبكة. يتم تكوين كل مصدر بيانات ربط كمصدر بيانات متداخل تحت مصدر البيانات الهدف (يتم تضمين مصدر بيانات**1Versions** تحت **1Configurations** واحد، ويتم تضمين مصدر بيانات **1Configurations** تحت **ConfigurationProviders** واحد). يحتوي كل مصدر بيانات تم تكوينه علي شروط الربط. في مصدر البيانات لهذا **الربط**المعين، يتم تعريف الصلات التالية:

    - يُربط كل سجل من مصدر البيانات **ConfigurationProviders** (يُشير إلى الجدول **ERVendorTable** ) مع السجلات **1Configurations** واحدة (يُشار اليها في الجدول **ERSolutionTable** ) ويكون له نفس القيمة في الحقلين **SolutionVendor** و **RecId** . يُستخدم نوع **الربط الداخلي** لهذا الربط بالإضافة إلى الشروط التالية لمطابقه السجلات: 

    FILTER (تكوينات، Configurations.SolutionVendor = onfigurationProviders.RecId)

    - يتم ربط كل سجل من مصدر البيانات **1Configurations** (يُشير إلى الجدول **ERSolutionTable** ) مع السجلات **1Versions** الأولى فقط (يُشار اليها في الجدول **ERSolutionVersionTable** ) ويكون له نفس القيمة في الحقول **Solution** و **RecId** . يُستخدام نوع **الربط الداخلي** لهذا الربط بالإضافة إلى الشروط التالية لمطابقة السجلات:

    FILTER (ConfigurationVersions، ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)

    - تم تكوين خيار **تنفيذ** كمعني **استعلام**، سوف يتم تنفيذ مصدر بيانات الربط هذا له في وقت التشغيل علي مستوي قاعدة البيانات كاستدعاء مباشر لـ SQL.

    لاحظ أنه لربط سجلات مصادر البيانات التي تمثل جداول التطبيق، يمكنك تحديد شروط الربط باستخدام أزواج من الحقول بخلاف تلك الموجودة في علاقات AOT بين هذه الجداول. يمكن تكوين هذا النوع من الربط لينفذ علي مستوي قاعدة البيانات أيضًا.

6.  قم بإغلاق الصفحة.
7.  حدد **إلغاء الأمر**.
8.  في شجره التكوينات، قم بتوسيع عنصر نموذج البيانات **Set2.Summary** :

    - يُشير ربط **VersionsNumber: عدد صحيح = DetailsSummary.aggregated.VersionsNumber** إلى أنه يتم ربط العنصر **Set2.Summary.VersionsNumber** بحقل تجميع **VersionsNumber** لمصدر بيانات **DetailsSummary** لنوع **GroupBy** الذي تم تكوينه لإرجاع عدد السجلات المرتبطة لمصدر البيانات **Details** من النوع **Join** .
    - لاحظ تكوين خيار موقع **تنفيذ** كمعني **استعلام** يتم تنفيذ مصدر بيانات **GroupBy** هذا في وقت التشغيل كاستدعاء مباشر لـ SQL على مستوى قاعدة البيانات. ويعد ذلك ممكنًا بسبب تكوين مصدر البيانات الأساسي **Details** لنوع **Join** علي أنه تم تنفيذه علي مستوي قاعدة البيانات.

    ![صفحه معلمات مصدر البيانات GROUPBY](./media/GER-JoinDS-Set2GroupByReview.PNG)

9.  قم بإغلاق الصفحة.
10. حدد **إلغاء الأمر**.

### <a name="executeERformat"></a> تنفيذ تنسيق التقارير الإلكترونية

1.  يمكنك الوصول إلى Finance أو RCS في الجلسة الثانية لمستعرض الويب الخاص بك باستخدام نفس بيانات الاعتماد والشركة كما في الجلسة الاولي.
2.  انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.
3.  توسيع تكوين **نموذج لمعرفة مصادر بيانات JOIN** .
4.  حدد تكوين **تنسيق لمعرفة مصادر بيانات JOIN** .
5.  حدد **المصمم**.
6.  حدد **إظهار التفاصيل**.
7.  حدد **التعيين**.
8.  حدد **التوسيع/الطي**.

    لاحظ أن هذا التنسيق تم تصميمه لملء الملف النصي الذي تم إنشاؤه بسطر جديد لكل إصدار من تكوين التقارير الإلكترونية (تسلسل**الإصدار** ). سوف يحتوي كل سطر يتم إنشاؤه علي اسم موفر تكوين مالك للتكوين الحالي، واسم التكوين وإصدار التكوين المفصولين بعلامة الفاصلة المنقوطة. سوف يحتوي السطر الأخير من الملف الذي تم إنشاؤه علي عدد الإصدارات التي تم اكتشافها لتكوينات التقارير الإلكترونية (تسلسل**الملخص** ).

    ![صفحة مصمم تنسيق‬ التقارير الإلكترونية](./media/GER-JoinDS-FormatReview.PNG)

    يتم استخدام مصادر بيانات **التاريخ** و **الملخص** لملء تفاصيل إصدار التكوين للملف الذي تم إنشاؤه:

    - يتم استخدام المعلومات من نموذج بيانات Set1 عند **اختيار** **لا** لمصدر البيانات **مُحدد** في وقت التشغيل في صفحة مربع حوار المستخدم عند تشغيل تنسيق التقارير الإلكترونية.
    - يتم استخدام المعلومات من نموذج بيانات **Set2** عند اختيار **نعم** لمصدر البيانات **مُحدد** في وقت التشغيل في صفحة مربع حوار المستخدم عند تشغيل تنسيق التقارير الإلكترونية.

    ![صفحة مصمم تنسيق‬ التقارير الإلكترونية](./media/GER-JoinDS-FormatMappingReview.PNG)

9.  حدد **تشغيل**.
10. في صفحه الحوار ، حدد **لا** في الحقل **استخدام مصدر بيانات JOIN** .
11. حدد **موافق**.
12. مراجعة الملف الذي تم إنشاؤه.

    ![صفحه مربع حوار مستخدم التقارير الإلكترونية](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a>تحليل تتبع تنفيذ تنسيق التقارير الإلكترونية

1.  في جلسة العمل الاولي من Finance أو RCS، حدد **المصمم**.
2.  حدد **تتبع الأداء**.
3.  في شبكة **تتبع الأداء** ، حدد السجل الأعلى لأحدث تتبع للتنفيذ الخاص بتنسيق التقارير الإلكترونية التي تستخدم مكون تعيين النموذج الحالي.
4.  حدد **موافق**.

    لاحظ أن إحصائيات التنفيذ تُعلمك بالاستدعاءات المكررة لجداول التطبيق:

    - تم استدعاء**ERSolutionTable** عدة مرات لسجلات إصدار التكوين في جدول **ERSolutionVersionTable** ، بينما يمكن تقليل عدد هذه الاستدعاءات في أوقات تحسين الأداء.
    - تم استدعاء**ERVendorTable** مرتين لكل سجل إصدار التكوين الذي تم اكتشافه في جدول **ERSolutionVersionTable** ، بينما يمكن تقليل عدد هذه الاستدعاءات أيضًا.

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/GER-JoinDS-Set1Run2.PNG)

5.  قم بإغلاق الصفحة.

### <a name="execute-er-format"></a>تنفيذ تنسيق التقارير الإلكترونية

1.  قم بالتبديل إلى علامة تبويب مستعرض الويب باستخدام جلسة العمل الثانية لـ Finance أو RCS.
2.  حدد **تشغيل**.
3.  في صفحه الحوار، حدد **نعم** في الحقل **استخدام مصدر بيانات JOIN** .
4.  حدد **موافق**.
5.  مراجعة الملف الذي تم إنشاؤه.

    ![صفحه مربع حوار مستخدم التقارير الإلكترونية](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze"></a> تحليل تتبع تنفيذ تنسيق التقارير الإلكترونية

1.  في جلسة العمل الاولي من Finance أو RCS، حدد **المصمم**.
2.  حدد **تتبع الأداء**.
3.  في شبكة **تتبع الأداء** ، حدد السجل الأعلى الذي يمثل أحدث تتبع للتنفيذ الخاص بتنسيق التقارير الإلكترونية التي تستخدم مكون تعيين النموذج الحالي.
4.  حدد **موافق**.

    لاحظ ان إحصائيات التنفيذ تُعلمك بما يلي:

    - تم استدعاء قاعدة بيانات التطبيق مرة واحدة للحصول علي سجلات من الجداول **ERVendorTable**، و **ERSolutionTable**، و **ERSolutionVersionTable** للوصول إلى الحقول المطلوبة.

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/GER-JoinDS-Set2Run2.PNG)

    - تم استدعاء قاعدة بيانات التطبيق مرة واحدة لحساب عدد إصدارات التكوين باستخدام الروابط التي تم تكوينها في مصدر بيانات **التفاصيل** .

    ![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="additional-resources"></a>الموارد الإضافية

[مصمم المعادلات في التقارير الإلكترونية](general-electronic-reporting-formula-designer.md)

[تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها](trace-execution-er-troubleshoot-perf.md)
