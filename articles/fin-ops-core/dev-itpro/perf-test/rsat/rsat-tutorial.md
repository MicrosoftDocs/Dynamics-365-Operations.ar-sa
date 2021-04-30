---
title: البرنامج التعليمي للأداة Regression Suite Automation Tool
description: يوضح هذا الموضوع كيفية استخدام أداة Regression suite automation tool (RSAT). وهو يصف ميزات مختلفة ويوفر أمثلة تستخدم البرمجة النصية المتقدمة.
author: robinarh
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: a194e14c76827650e6752f331081ebe0c2130a13
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866146"
---
# <a name="regression-suite-automation-tool-tutorial"></a>البرنامج التعليمي للأداة Regression Suite Automation Tool

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> استخدم أدوات مستعرض الإنترنت لتنزيل هذه الصفحة وحفظها بتنسيق pdf.

يعرفك هذا البرنامج التعليمي على بعض الميزات المتقدمة الخاصة بأداة Regression suite automation tool (RSAT)، ويتضمن تعيين عرض توضيحي، ويصف الاستراتيجية ونقاط التعليم الأساسية.

## <a name="notable-features-of-rsat-and-task-recorder"></a>ميزات مهمة في RSAT ومسجل المهام

### <a name="validate-a-field-value"></a>التحقق من قيمة الحقل

يسمح لك RSAT بتضمين خطوات التحقق من الصحة داخل حالة اختبار بك للتحقق من صحة القيم المتوقعة. للحصول على معلومات حول هذه الميزة، راجع المقال [التحقق من صحة القيم المتوقعة](rsat-validate-expected.md).

يوضح المثال التالي كيفية استخدام هذه الميزة للتحقق مما إذا كان المخزون الفعلي أكبر من 0 (صفر).

1. في البيانات التوضيحية في شركة **USMF**، قم بإنشاء تسجيل مهام بالخطوات التالية:

    1. انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.
    2. استخدم عامل التصفية السريع للبحث عن السجلات. على سبيل المثال، قم بإجراء التصفية على قيمة **1000** للحقل **رقم الصنف**.
    3. حدد **المخزون الفعلي**.
    4. استخدم عامل التصفية السريع للبحث عن السجلات. على سبيل المثال، قم بإجراء التصفية على القيمة **1** لحقل **الموقع**.
    5. في القائمة، قم بوضع علامة للصف المحدد.
    6. تحقق من أن قيمة حقل **الإجمالي المتاح** هي **411.0000000000000000**.

2. حفظ تسجيل المهام **كتسجيل مطور** وأرفقه بحالة اختبارك في Azure Devops.
3. قم بإضافة حالة الاختبار إلى خطة الاختبار، وقم بتحميل حالة الاختبار إلى RSAT.
4. قم بفتح ملف معلمه Excel وانتقل إلى علامة التبويب **TestCaseSteps**.
5. للتحقق مما إذا كان المخزون الفعلي سيكون دائما أكبر من **0**، انتقل إلى **الخطوة الاجماليه للتحقق من الصحة** المتوفرة وقم بتغيير قيمتها من **411** إلى **0**. قم بتغيير قيمه حقل **عامل التشغيل** من علامة يساوي (**=**) إلى علامة أكبر من ( **\>**).
6. احفظ ملف معلمات Excel وأغلقه.
7. حدد **تحميل** لحفظ التغييرات التي أجريتها على ملف معلمات Excel إلى Azure DevOps.

والآن، إذا كانت قيمة حقل **الإجمالي المتوفر** للصنف المحدد في المخزون أكبر من 0 (صفر)، سيتم اجتياز الاختبارات، بغض النظر عن قيمة المخزون الفعلي.

### <a name="saved-variables-and-chaining-of-test-cases"></a>المتغيرات المحفوظة وتسلسل حالات الاختبار

إحدى الميزات الرئيسية لـ RSAT هي تسلسل حالات الاختبار، أي، قدرة الاختبار على تمرير المتغيرات إلى اختبارات أخرى. لمزيد من المعلومات، راجع المقال [نسخ المتغيرات إلى تسلسل حالات الاختبار](rsat-chain-test-cases.md).

### <a name="derived-test-case"></a>حالة الاختبار المشتقة

يتيح لك RSAT استخدام تسجيل المهام نفسه مع حالات اختبار متعددة، مما يمكّن تشغيل مهمة باستخدام تكوينات مختلفة للبيانات. راجع المقال [حالات الاختبار المشتقة](rsat-derived-test-cases.md) لمزيد من المعلومات.

### <a name="validate-notifications-and-messages"></a>التحقق من صحة الإعلامات والرسائل

يمكن استخدام هذه الميزة للتحقق مما إذا كان الإجراء قد حدث أم لا. على سبيل المثال، عند إنشاء أمر إنتاج وتقديره ثم بدء تشغيله، يعرض التطبيق الرسالة "الإنتاج – بدء" لإعلامك بأنه قد تم بدء أمر الإنتاج.

![إخطار الإنتاج - بدء](./media/use_rsa_tool_05.png)

يمكنك التحقق من صحة هذه الرسالة عن طريق RSAT وذلك بإدخال نص الرسالة في علامة التبويب **MessageValidation** في ملف معلمة Excel للتسجيل المناسب.

![علامة تبويب التحقق من الرسالة](./media/use_rsa_tool_06.png)

بعد تشغيل حالة الاختبار، تتم مقارنة الرسالة الموجودة في ملف معلمة Excel بالرسالة المعروضة. في حالة عدم تطابق الرسائل، ستفشل حالة الاختبار.

> [!NOTE]
> يمكنك إدخال أكثر من رسالة واحدة في علامة تبويب **MessageValidation** في ملف معلمة Excel. يمكن أن تكون الرسائل أيضا رسائل خطا أو تحذيرات بدلا من الرسائل الإخبارية.

### <a name="snapshot"></a>اللقطة

تقوم هذه الميزة بأخذ لقطات شاشة الخطوات التي تم إجراؤها أثناء تسجيل المهام. وهي مفيدة لأغراض للتدقيق أو التصحيح.

- لاستخدام هذه الميزة، افتح ملف **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**، تحت مجلد تثبيت RSAT (على سبيل المثال، **C:\\Program Files (x86)\\Regression Suite Automation Tool**)، وقم بتغيير القيمة للعنصر التالي من **false** إلى **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

عند تشغيل حالة الاختبار، ينشئ RSAT لقطات (صور) للخطوات في مجلد التشغيل لحالات الاختبار في الدليل الفعال. إذا كنت تستخدم إصدارًا أقدم من RSAT، فسيتم حفظ الصور في **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**، ويتم إنشاء مجلد منفصل لكل حالة اختبار قيد التشغيل.

## <a name="assignment"></a>تعيين

### <a name="scenario"></a>سيناريو

1. يقوم مصمم المنتج بإنشاء منتج جديد تم إصداره.
2. تقوم إدارة الإنتاج بتهيئة أمر إنتاج لجعل مستوى المخزون من جزئين.
3. ويبدأ التصنيع أمر الإنتاج وينهيه، ويتحقق من أن الكمية الفعلية من جزئين.
4. يتلقى فريق المبيعات طلبا بأربعة أجزاء من المنتج الجديد. بالتالي، يقوم فريق المبيعات بتحديث صافي المتطلبات عبر الخطة الديناميكية. وبسبب عدم توفر سعة إضافية، يتم تعيين سياسة الترتيب الافتراضي إلى "الشراء بدلا من الصنع". بالتالي، يتم إنشاء أمر شراء مخطط
5. يقوم المشتري بإضافة مورد، ويؤكد أمر الشراء المخطط، ثم يقوم بتأكيد أمر الشراء.
6. عند وصول البضائع التي تم شراؤها إلى المتجر، يقوم مشغل المتجر بالبحث في أمر الشراء المرتبط ويستلم البضائع. نظرا لأن الأمر مكتمل الآن، فيمكن انتقاء البضائع وتعبئتها مقابل أمر التوريد.
7. ينشر تطبيق المالية فاتورة الشراء وفاتورة المبيعات.

يعرض الرسم التوضيحي التالي سير العمل لهذا السيناريو.

![سير عمل السيناريو التوضيحي](./media/use_rsa_tool_14.png)

يبين الرسم التوضيحي التالي التسلسل الهرمي للعمليات التجارية لهذا السيناريو في أداة تكوين عمليات الأعمال في LCS.

![العمليات التجارية للسيناريو التوضيحي](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>الاستراتيجية – التعليم الأساسي

### <a name="data"></a>البيانات

- تأكد أن لديك وحدات تخزين بيانات تمثيلية (نسخة من بيانات الإنتاج/التكوين الذهبي بالإضافة إلى بيانات تم ترحيلها).
- عند إنشاء البيانات الجديدة عبر مسجل المهام، قم بإنشاء أسماء الاختبارات التي لا تتعارض مع الأسماء الموجودة (على سبيل المثال، استخدم بادئة مثل **RSATxxx**).
- استخدم استعادة النقطة الزمنية في Azure لإعادة تشغيل الاختبارات في بيئات ليست من المستوي 1.
- على الرغم من أنه يمكنك استخدام دالتي Excel **RANDOM** و **NOW** لإنشاء مجموعة فريدة، فإن الجهد يكون مرتفعا بشكل كبير. فيما يلي مثال على ذلك.

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>مسجل المهام

- حدد السيناريوهات قبل بدء التسجيل. يحتوي المشروع جيد الإدارة على سيناريوهات اختبار معرفة مسبقا. لبناء حالة اختبار، ضع في الاعتبار مدي توقع نتيجة سيناريوهات الاختبار هذه.
- قسم التسجيلات في حالة تنفيذها بواسطة أدوار مختلفة، أو إذا كان هناك وقت انتظار أو حدث خارجي قبل الخطوة التالية.
- تجنب تحديد القيم في القوائم. بدلا من ذلك، استخدم تنسيقات نصية، مثل **FIFO** و **AudioRM** و **SiteWH**. عندم تحدد في القائمة، يتم تسجيل موضع القيمة في القائمة، وليس القيمة نفسها. إذا تمت إضافة عناصر إلى هذه القائمة، يمكن تغيير وضع القيمة. لذلك، سيقوم التسجيل الخاص بك باستخدام معلمة مختلفة، وقد يتأثر باقي السيناريو.
- فكر في سلوك المستخدمين المتعددين. على سبيل المثال، لا تفترض أن أمر التوريد الذي تم إنشاؤه حديثا سيتم دوما تحديده تلقائيا. بدلا من ذلك، استخدم عامل التصفية دائما للعثور على الطلب الصحيح.
- استخدم وظيفة النسخ في مسجل المهام لحفظ اسم منتج تم إنشاؤه حديثا بحيث يمكن استخدامه في حالات الاختبار المتسلسلة.
- استخدم وظيفة التحقق من الصحة في مسجل المهام لتعيين نقاط التحقق التي تتحقق من أن الخطوات تم تشغيلها بشكل صحيح.

### <a name="rsat"></a>RSAT

- لتشغيل الاختبار في شركة أخرى، يمكنك تغيير الشركة في علامة التبويب **عام** بملف معلمة Excel. تأكد من توفر الإعدادات والبيانات في الشركة المحددة حديثا.
- يمكنك تغيير مستخدم الاختبار في علامة التبويب **عام** بملف معلمة Excel. حدد معرف البريد الإلكتروني الخاص بالمستخدم الذي سيقوم بتشغيل حالة الاختبار. بهذه الطريقة، يمكن تشغيل حالة الاختبار باستخدام أذونات الأمان الخاصة بالمستخدم المحدد.
- للانتظار قبل بدء الاختبار، يمكنك تعريف توقف مؤقت في علامة التبويب **عام** بملف معلمة Excel. يمكن استخدام الإيقاف المؤقت هذا في وظيفة دفعية (على سبيل المثال، إذا كان من الضروري تشغيل سير عمل قبل إجراء الخطوة التالية.)

## <a name="advanced-scripting"></a>البرمجة المتقدمة

### <a name="cli"></a>CLI

يمكن استدعاء RSAT من نافذة **موجه الأوامر** أو **PowerShell**.

> [!NOTE]
> تحقق من تعيين متغير البيئة **TestRoot** على مسار تثبيت RSAT. (في Microsoft Windows، افتح **لوحة التحكم**، وحدد **النظام والأمان \> النظام \> إعدادات الأمان المتقدمة**، ثم حدد **متغيرات البيئة**.)

1. افتح نافذة **موجه الأوامر** أو **PowerShell** كمسؤول.
2. انتقل إلى دليل التثبيت RSAT.

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. اسرد كافة الأوامر.

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>؟

يظهر تعليمات حول كافة الأوامر المتوفرة والمعلمات الخاصة بها.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: معلمات اختيارية

`command`: حيث ``[command]`` يكون أحد الأوامر المحددة أدناه.

#### <a name="about"></a>حول

يعرض الإصدار الحالي.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

يمسح الشاشة.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>تنزيل

يقوم بتنزيل مرفقات لحالة الاختبار المحددة إلى دليل الإخراج.
يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة. استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a>تنزيل: المحددات المطلوبة

+ `test_case_id`: تمثل معرف حالة الاختبار.
+ `output_dir`: تمثل دليل الإخراج. الدليل يجب أن يكون موجودًا.

##### <a name="download-examples"></a>تنزيل: أمثله

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a>تحرير

يسمح لك بفتح ملف المعلمات في برنامج Excel وتحريره.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>edit: المعلمات المطلوبة

+ `excel_file`: يجب أن يحتوي على مسار كامل لملف Excel موجود.

##### <a name="edit-examples"></a>edit: أمثله

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>إنشاء

يقوم بإنشاء ملفات تنفيذ تجريبي ومعلمات لحالة الاختبار المحددة في دليل الإخراج. يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة. استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a>generate: المحددات المطلوبة

+ `test_case_id`: تمثل معرف حالة الاختبار.
+ `output_dir`: تمثل دليل الإخراج. الدليل يجب أن يكون موجودًا.

##### <a name="generate-examples"></a>generate: أمثله

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a>generatederived

يقوم بإنشاء حالة اختبار جديدة، مشتقة من حالة الاختبار المتوفرة. يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة. استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a>generatederived: المحددات المطلوبة

+ `parent_test_case_id`: تمثل معرف حالة الاختبار الأصلية.
+ `test_plan_id`: تمثل معرف خطة الاختبار.
+ `test_suite_id`: تمثل معرف مجموعة الاختبار.

##### <a name="generatederived-examples"></a>generatederived: أمثله

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

يقوم بإنشاء ملف تنفيذ تجريبي فقط لحالة الاختبار المحددة في دليل الإخراج. يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة. استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: المحددات المطلوبة

+ `test_case_id`: تمثل معرف حالة الاختبار.
+ `output_dir`: تمثل دليل الإخراج. الدليل يجب أن يكون موجودًا.

##### <a name="generatetestonly-examples"></a>generatetestonly: أمثله

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a>generatetestsuite

يقوم بإنشاء كافة حالات الاختبار للمجموعة المحددة في دليل الإخراج. يمكنك استخدام الأمر ``listtestsuitenames`` للحصول على كافة مجموعات الاختبار المتوفرة. استخدم أي قيمة من العمود كمعلمة **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: المحددات المطلوبة

+ `test_suite_name`: تمثل اسم مجموعة الاختبار.
+ `output_dir`: تمثل دليل الإخراج. الدليل يجب أن يكون موجودًا.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: أمثله

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a>تعليمات

مماثل لـ [?](#section) أمر.

#### <a name="list"></a>القائمة

يسرد كافة حالات الاختبار المتوفرة.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

يسرد كافة خطط الاختبار المتوفرة.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

يسرد حالات الاختبار لمجموعة الاختبار المحددة. يمكنك استخدام الأمر ``listtestsuitenames`` للحصول على كافة مجموعات الاختبار المتوفرة. استخدم أي قيمة من العمود الأول كمعلمة **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: المحددات المطلوبة

+ `suite_name`: اسم المجموعة المطلوبة.

##### <a name="listtestsuite-examples"></a>listtestsuite: أمثله

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a>listtestsuitenames

يسرد كافة مجموعات الاختبار المتوفرة.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>تشغيل

يقوم بتشغيل حالة اختبار باستخدام ملف Excel.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a>playback: المعلمات المطلوبة

+ `excel_file`: مسار كامل لملف Excel. يجب أن يكون الملف موجودًا.

##### <a name="playback-examples"></a>playback: أمثله

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

يقوم بتشغيل عدة حالات اختبار في الحال. يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة. استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: المعلمات المطلوبة

+ `test_case_id1`: معرف حالة اختبار موجودة.
+ `test_case_id2`: معرف حالة اختبار موجودة.
+ `test_case_idN`: معرف حالة اختبار موجودة.

##### <a name="playbackbyid-examples"></a>playbackbyid: أمثله

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

يقوم بتشغيل العديد من حالات الاختبار في الحال، باستخدام ملفات Excel.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a>playbackmany: المعلمات المطلوبة

+ `excel_file1`: مسار كامل لملف Excel. يجب أن يكون الملف موجودًا.
+ `excel_file2`: مسار كامل لملف Excel. يجب أن يكون الملف موجودًا.
+ `excel_fileN`: المسار الكامل إلى ملف Excel. يجب أن يكون الملف موجودًا.

##### <a name="playbackmany-examples"></a>playbackmany: أمثله

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

يقوم بتشغيل كافة حالات الاختبار من مجموعة الاختبار المحددة.
يمكنك استخدام الأمر ``listtestsuitenames`` للحصول على كافة مجموعات الاختبار المتوفرة. استخدم أي قيمة من العمود الأول كمعلمة **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: المعلمات المطلوبة

+ `suite_name`: اسم المجموعة المطلوبة.

##### <a name="playbacksuite-examples"></a>playbacksuite: أمثله

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a>إنهاء

يغلق التطبيق.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a>تحميل

يقوم بتحميل كل الملفات التي تنتمي لمجموعة الاختبار المحددة أو حالات الاختبار.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a>upload: المحددات المطلوبة

+ `suite_name`: سيتم تحميل كل الملفات التي تنتمي لمجموعة الاختبار المحددة.
+ `testcase_id`: سيتم تحميل كل الملفات التي تنتمي لحالة (حالات) الاختبار المحددة.

##### <a name="upload-examples"></a>upload: أمثله

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

يقوم بتحميل ملف تسجيل واحد ينتمي لحالات الاختبار المحددة.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: المحددات المطلوبة

+ `testcase_id`: سيتم تحميل ملف تسجيل واحد ينتمي لحالات الاختبار المحددة.

##### <a name="uploadrecording-examples"></a>uploadrecording: أمثله

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>استخدام

يظهر طريقتين لاستدعاء هذا التطبيق: واحد باستخدام ملف إعداد افتراضي، آخر يوفر ملف إعداد.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a>أمثلة Windows PowerShell

#### <a name="run-a-test-case-in-a-loop"></a>تشغيل حالة اختبار في حلقة

لديك برنامج اختبار نصي يقوم بإنشاء عميل جديد. بواسطة البرمجة النصية، يمكن تشغيل حالة الاختبار هذه في حلقة عن طريق الترتيب العشوائي للبيانات التالية قبل تشغيل كل تكرار:

- معرف العميل
- اسم العميل
- عنوان العميل

سيكون معرف العميل بالتنسيق *ATCUS\<number\>*، حيث \<number\> عبارة عن قيمة بين **000000001** و **999999999**.

يستخدم المثال التالي معلمة واحدة **البدء**، لتعريف الرقم الأول المستخدم. يستخدم معلمة ثانية، **nr**، لتحديد عدد العملاء الذين يجب إنشاؤهم. بالنسبة لكل تكرار، يتم تغيير المعلمات الموجودة في ملف معلمة Excel باستخدام دالة UpdateCustomer. بعد ذلك يتم استدعاء سطر أوامر RSAT في دالة RunTestCase.

افتح بيئة البرمجة المتكاملة (ISE) في Microsoft Windows PowerShell في وضع المسؤول، والصق الكود التالي في الإطار الذي يسمى **Untitled1.ps1**.

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>تشغيل برنامج نصي يعتمد على البيانات في Microsoft Dynamics 365

يستخدم المثال التالي استدعاء بروتوكول البيانات المفتوحة (OData) للعثور على حالة الأمر لأمر الشراء. إذا لم تتم **فوترة** الحالة، يمكنك، على سبيل المثال، استدعاء حالة اختبار RSAT التي ترحّل الفاتورة.

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]