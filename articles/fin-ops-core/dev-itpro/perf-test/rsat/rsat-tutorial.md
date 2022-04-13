---
title: البرنامج التعليمي للأداة Regression Suite Automation Tool
description: يوضح هذا الموضوع كيفية استخدام أداة Regression suite automation tool (RSAT). وهو يصف ميزات مختلفة ويوفر أمثلة تستخدم البرمجة النصية المتقدمة.
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: e2273aefb98880a1ae746ef7ec65b4f2262f3560
ms.sourcegitcommit: 49c97b0c94e916db5efca5672d85df70c3450755
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/29/2022
ms.locfileid: "8492909"
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

2. حفظ تسجيل المهمة على أنه **تسجيل مطور** وأرفقه بحالة الاختبار في Azure DevOps.
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

![الإنتاج - إخطار البدء.](./media/use_rsa_tool_05.png)

يمكنك التحقق من صحة هذه الرسالة عن طريق RSAT وذلك بإدخال نص الرسالة في علامة التبويب **MessageValidation** في ملف معلمة Excel للتسجيل المناسب.

![علامة تبويب التحقق من الرسالة.](./media/use_rsa_tool_06.png)

بعد تشغيل حالة الاختبار، تتم مقارنة الرسالة الموجودة في ملف معلمة Excel بالرسالة المعروضة. في حالة عدم تطابق الرسائل، ستفشل حالة الاختبار.

> [!NOTE]
> يمكنك إدخال أكثر من رسالة واحدة في علامة تبويب **MessageValidation** في ملف معلمة Excel. يمكن أن تكون الرسائل أيضا رسائل خطا أو تحذيرات بدلا من الرسائل الإخبارية.

### <a name="snapshot"></a>اللقطة

تقوم هذه الميزة بأخذ لقطات شاشة الخطوات التي تم إجراؤها أثناء تسجيل المهام. وهي مفيدة لأغراض للتدقيق أو التصحيح.

- لاستخدام هذه الميزة أثناء تشغيل RSAT مع واجهة المستخدم، افتح ملف **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**، تحت مجلد تثبيت RSAT (على سبيل المثال، **C:\\Program Files (x86)\\Regression Suite Automation Tool**)، وقم بتغيير القيمة في العنصر التالي من **خطأ** إلى **صواب**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

- لاستخدام هذه الميزة أثناء تشغيل RSAT بواسطة CLI (على سبيل المثال، Azure DevOps)، افتح الملف **Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe.config** تحت مجلد تثبيت RSAT (على سبيل المثال، **C:\\Program Files (x86)\\Regression Suite Automation Tool**)، وقم بتغيير القيمة في العنصر التالي من **خطأ** إلى **صواب**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

عند تشغيل حالات الاختبار، ينشئ RSAT لقطات (صور) للخطوات ويحفظها في مجلد التشغيل لحالات الاختبار في الدليل الفعال. في مجلد التشغيل، يتم إنشاء مجلد فرعي منفصل باسم **StepSnapshots**. يحتوي هذا المجلد على لقطات لحالات الاختبار التي يتم تشغيلها.

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

![سير عمل السيناريو التوضيحي.](./media/use_rsa_tool_14.png)

يبين الرسم التوضيحي التالي التسلسل الهرمي للعمليات التجارية لهذا السيناريو في أداة تكوين عمليات الأعمال في LCS.

![العمليات التجارية للسيناريو التوضيحي.](./media/use_rsa_tool_15.png)

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
        downloadsuite
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitebyid
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        playbacksuitebyid
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>؟

يسرد كافة الأوامر أو يظهر تعليمات حول أمر معين إلى جانب المعلمات المتوفرة.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: معلمات اختيارية

`command`: Where ``[command]`` هو أحد الأوامر الموجودة في القائمة السابقة.

#### <a name="about"></a>حول

يعرض إصدار RSAT المثبت.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

يمسح الشاشة.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>تنزيل

يقوم بتنزيل المرفقات (ملفات التسجيل والتنفيذ والمعلمات) لحالة الاختبار المحددة من Azure DevOps إلى دليل الإخراج. يمكنك استخدام الأمر ``list`` للحصول علي كافة حالات الاختبار المتوفرة، واستخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="download-optional-switches"></a>تنزيل: مفاتيح التبديل الاختيارية

+ `/retry[=seconds]`: إذا تم تحديد رمز التبديل هذا، وتم حظر حالات اختبار الحالة بواسطة مثيلات RSAT الأخرى، فستنتظر عملية التنزيل العدد المحدد من الثواني ثم المحاولة مرة أخرى. وتكون القيمة الافتراضية \[120\] ثانية. بدون هذا المفتاح، سيتم إلغاء العملية على الفور إذا تم حظر حالات الاختبار.

##### <a name="download-required-parameters"></a>تنزيل: المحددات المطلوبة

+ `test_case_id`: تمثل معرف حالة الاختبار.

##### <a name="download-optional-parameters"></a>تنزيل: معلمات اختيارية

+ `output_dir`: تمثل دليل عمل الإخراج. الدليل يجب أن يكون موجودًا. سيتم استخدام دليل العمل من الإعدادات إذا لم يتم تحديد هذه المعلمة.

##### <a name="download-examples"></a>تنزيل: أمثله

`download 123 c:\temp\rsat`

`download /retry=240 765`

#### <a name="downloadsuite"></a>downloadsuite

يقوم بتنزيل المرفقات (ملفات التسجيل والتنفيذ والمعلمات) لجميع حالات الاختبار في مجموعة الاختبار المحددة من Azure DevOps إلى دليل الإخراج. يمكنك استخدام الأمر ``listtestsuitenames`` للحصول على جميع مجموعات الاختبار المتاحة، واستخدام أي قيمة كمعلمة **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``downloadsuite``**``[/retry[=<seconds>]] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="downloadsuite-optional-switches"></a>downloadsuite: مفاتيح التبديل الاختيارية

+ `/retry[=seconds]`: إذا تم تحديد رمز التبديل هذا، وتم حظر حالات اختبار الحالة بواسطة مثيلات RSAT الأخرى، فستنتظر عملية التنزيل العدد المحدد من الثواني ثم المحاولة مرة أخرى. وتكون القيمة الافتراضية \[120\] ثانية. بدون هذا المفتاح، سيتم إلغاء العملية على الفور إذا تم حظر حالات الاختبار.
+ `/byid`: يشير رمز التبديل هذا إلى أن مجموعة الاختبار المطلوبة يتم تحديدها من خلال معرف Azure DevOps الخاص بها بدلاً من اسم مجموعة الاختبار.

##### <a name="downloadsuite-required-parameters"></a>downloadsuite: المعلمات المطلوبة

+ `test_suite_name`: تمثل اسم مجموعة الاختبار. تكون هذه المعلمة مطلوبة إذا كان رمز التبديل /byid **غير** محدد. يكون هذا الاسم هو اسم مجموعة اختبار Azure DevOps.
+ `test_suite_id`: تمثل معرف مجموعة الاختبار. تكون هذه المعلمة مطلوبة إذا كان رمز التبديل /byid **محددًا**. يكون هذا المعرف هو معرف مجموعة Azure DevOps الاختبارية.

##### <a name="downloadsuite-optional-parameters"></a>downloadsuite: معلمات اختيارية

+ `output_dir`: تمثل دليل عمل الإخراج. الدليل يجب أن يكون موجودًا. سيتم استخدام دليل العمل من الإعدادات إذا لم يتم تحديد هذه المعلمة.

##### <a name="downloadsuite-examples"></a>downloadsuite: أمثلة

`downloadsuite NameOfTheSuite c:\temp\rsat`

`downloadsuite /byid 123 c:\temp\rsat`

`downloadsuite /retry=240 /byid 765`

`downloadsuite /retry=240 /byid 765 c:\temp\rsat`

#### <a name="edit"></a>تحرير

يسمح لك بفتح ملف المعلمات في برنامج Excel وتحريره.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>edit: المعلمات المطلوبة

+ `excel_file`: يجب أن يحتوي على مسار كامل لملف Excel موجود.

##### <a name="edit-examples"></a>edit: أمثله

`edit c:\RSAT\123\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>إنشاء

يقوم بإنشاء ملفات تنفيذ تجريبي ومعلمات لحالة الاختبار المحددة في دليل الإخراج. يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة. استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] [test_case_id] [output_dir]``

##### <a name="generate-optional-switches"></a>إنشاء: مفاتيح التبديل الاختيارية

+ `/retry[=seconds]`: إذا تم تحديد رمز التبديل هذا، وتم حظر حالات اختبار الحالة بواسطة مثيلات RSAT الأخرى، فستنتظر عملية الإنشاء عدد الثواني المحدد ثم المحاولة مرة أخرى. وتكون القيمة الافتراضية \[120\] ثانية. بدون هذا المفتاح، سيتم إلغاء العملية على الفور إذا تم حظر حالات الاختبار.
+ `/dllonly`: إنشاء ملفات تنفيذ الاختبار فقط. لا تقم بإعادة إنشاء ملف معلمة Excel.
+ `/keepcustomexcel`: ترقيه ملف المعلمات الموجود. يمكنك أيضا إعادة إنشاء ملفات التنفيذ.

##### <a name="generate-required-parameters"></a>generate: المحددات المطلوبة

+ `test_case_id`: تمثل معرف حالة الاختبار.

##### <a name="generate-optional-parameters"></a>إنشاء: معلمات اختيارية

+ `output_dir`: تمثل دليل عمل الإخراج. الدليل يجب أن يكون موجودًا. سيتم استخدام دليل العمل من الإعدادات إذا لم يتم تحديد هذه المعلمة.

##### <a name="generate-examples"></a>generate: أمثله

`generate 123 c:\temp\rsat`

`generate /retry=240 765 c:\rsat\last`

`generate /retry=240 /dllonly 765`

`generate /retry=240 /keepcustomexcel 765`

#### <a name="generatederived"></a>generatederived

يقوم بإنشاء حالة اختبار مشتقة جديدة (حالة اختبار الفرع) لحالة الاختبار المقدمة. تتم أيضًا إضافة حالة الاختبار الجديدة إلى مجموعة الاختبار المحددة. يمكنك استخدام الأمر ``list`` للحصول علي كافة حالات الاختبار المتوفرة، واستخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[/retry[=<seconds>]] [parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-optional-switches"></a>generatederived: مفاتيح التبديل الاختيارية

+ `/retry[=seconds]`: إذا تم تحديد رمز التبديل هذا، وتم حظر حالات اختبار الحالة بواسطة مثيلات RSAT الأخرى، فستنتظر عملية الإنشاء عدد الثواني المحدد ثم المحاولة مرة أخرى. وتكون القيمة الافتراضية \[120\] ثانية. بدون هذا المفتاح، سيتم إلغاء العملية على الفور إذا تم حظر حالات الاختبار.

##### <a name="generatederived-required-parameters"></a>generatederived: المحددات المطلوبة

+ `parent_test_case_id`: تمثل معرف حالة الاختبار الأصلية.
+ `test_plan_id`: تمثل معرف خطة الاختبار.
+ `test_suite_id`: تمثل معرف مجموعة الاختبار.

##### <a name="generatederived-examples"></a>generatederived: أمثله

`generatederived 123 8901 678`

`generatederived /retry 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

يقوم بإنشاء ملفات التنفيذ التجريبي فقط لحالة الاختبار المحددة. لا يقوم بإنشاء ملف معلمة Excel. يتم إنشاء الملفات في دليل الإخراج المحدد. يمكنك استخدام الأمر ``list`` للحصول علي كافة حالات الاختبار المتوفرة، واستخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="generatetestonly-optional-switches"></a>generatetestonly: مفاتيح التبديل الاختيارية

+ `/retry[=seconds]`: إذا تم تحديد رمز التبديل هذا، وتم حظر حالات اختبار الحالة بواسطة مثيلات RSAT الأخرى، فستنتظر عملية الإنشاء عدد الثواني المحدد ثم المحاولة مرة أخرى. وتكون القيمة الافتراضية \[120\] ثانية. بدون هذا المفتاح، سيتم إلغاء العملية على الفور إذا تم حظر حالات الاختبار.

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: المحددات المطلوبة

+ `test_case_id`: تمثل معرف حالة الاختبار.

##### <a name="generatetestonly-optional-parameters"></a>generatetestonly: المعلمات الاختيارية

+ `output_dir`: تمثل دليل عمل الإخراج. الدليل يجب أن يكون موجودًا. سيتم استخدام دليل العمل من الإعدادات إذا لم يتم تحديد هذه المعلمة.

##### <a name="generatetestonly-examples"></a>generatetestonly: أمثله

`generatetestonly 123 c:\temp\rsat`

`generatetestonly /retry=240 765`

#### <a name="generatetestsuite"></a>generatetestsuite

يقوم بإنشاء ملفات التشغيل التلقائي للاختبار فيما يتعلق بجميع حالات الاختبار في مجموعة الاختبار المحددة. يمكنك استخدام الأمر ``listtestsuitenames`` للحصول على جميع مجموعات الاختبار المتاحة، واستخدام أي قيمة كمعلمة **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="generatetestsuite-optional-switches"></a>generatetestsuite: مفاتيح التبديل الاختيارية

+ `/retry[=seconds]`: إذا تم تحديد رمز التبديل هذا، وتم حظر حالات اختبار الحالة بواسطة مثيلات RSAT الأخرى، فستنتظر عملية الإنشاء عدد الثواني المحدد ثم المحاولة مرة أخرى. وتكون القيمة الافتراضية \[120\] ثانية. بدون هذا المفتاح، سيتم إلغاء العملية على الفور إذا تم حظر حالات الاختبار.
+ `/dllonly`: إنشاء ملفات تنفيذ الاختبار فقط. لا تقم بإعادة إنشاء ملف معلمة Excel.
+ `/keepcustomexcel`: ترقيه ملف المعلمات الموجود. يمكنك أيضا إعادة إنشاء ملفات التنفيذ.
+ `/byid`: يشير رمز التبديل هذا إلى أن مجموعة الاختبار المطلوبة يتم تحديدها من خلال معرف Azure DevOps الخاص بها بدلاً من اسم مجموعة الاختبار.

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: المحددات المطلوبة

+ `test_suite_name`: تمثل اسم مجموعة الاختبار. تكون هذه المعلمة مطلوبة إذا كان رمز التبديل /byid **غير** محدد. يكون هذا الاسم هو اسم مجموعة اختبار Azure DevOps.
+ `test_suite_id`: تمثل معرف مجموعة الاختبار. تكون هذه المعلمة مطلوبة إذا كان رمز التبديل /byid **محددًا**. يكون هذا المعرف هو معرف مجموعة Azure DevOps الاختبارية.

##### <a name="generatetestsuite-optional-parameters"></a>generatetestsuite: المعلمات الاختيارية

+ `output_dir`: تمثل دليل عمل الإخراج. الدليل يجب أن يكون موجودًا. سيتم استخدام دليل العمل من الإعدادات إذا لم يتم تحديد هذه المعلمة.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: أمثله

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite /retry Purchase c:\rsat\last`

`generatetestsuite /dllonly /byid 121`

`generatetestsuite /keepcustomexcel /byid 121`

#### <a name="help"></a>تعليمات

مماثل لـ [?](#section) أمر.

#### <a name="list"></a>القائمة

يسرد كافة حالات الاختبار المتاحة في خطة الاختبار الحالية.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

يسرد كافة خطط الاختبار المتوفرة.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

يسرد حالات الاختبار لمجموعة الاختبار المحددة. يمكنك استخدام الأمر ``listtestsuitenames`` للحصول على جميع مجموعات الاختبار المتاحة، واستخدام أي قيمة من القائمة كمعلمة **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[test_suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: المحددات المطلوبة

+ `test_suite_name`: اسم المجموعة المطلوبة.

##### <a name="listtestsuite-examples"></a>listtestsuite: أمثله

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitebyid"></a>listtestsuitebyid

يسرد حالات الاختبار لمجموعة الاختبار المحددة.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitebyid``**``[test_suite_id]``

##### <a name="listtestsuitebyid-required-parameters"></a>listtestsuitebyid: المعلمات المطلوبة

+ `test_suite_id`: المعرف الفريد للمجموعة المطلوبة.

##### <a name="listtestsuitebyid-examples"></a>listtestsuitebyid: الأمثلة

`listtestsuitebyid 12345`

#### <a name="listtestsuitenames"></a>listtestsuitenames

يسرد كافة مجموعات الاختبار المتاحة في خطة الاختبار الحالية.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>تشغيل

إعادة تشغيل حالة الاختبار المرتبطة بملف معلمة Excel المحدد. يستخدم هذا الأمر ملفات التشغيل التلقائي المحلية الموجودة ولا يقوم بتنزيل الملفات من Azure DevOps. هذا الأمر غير مدعوم لحالات اختبار التجارة في نقاط البيع.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file]``

##### <a name="playback-optional-switches"></a>التشغيل: مفاتيح التبديل الاختيارية

+ `/retry[=seconds]`: إذا تم تحديد رمز التبديل هذا، وتم حظر حالات اختبار الحالة بواسطة مثيلات RSAT الأخرى، فستنتظر عملية التشغيل عدد الثواني المحدد ثم المحاولة مرة أخرى. وتكون القيمة الافتراضية \[120\] ثانية. بدون هذا المفتاح، سيتم إلغاء العملية على الفور إذا تم حظر حالات الاختبار.
+ `/comments[="comment"]`: قم بتوفير سلسلة معلومات مخصصة سيتم تضمينها في الحقل **التعليقات** في الملخص وصفحات نتائج الاختبار لتشغيل حالة اختبار Azure DevOps.

##### <a name="playback-required-parameters"></a>playback: المعلمات المطلوبة

+ `excel_parameter_file`: المسار الكامل لملف معلمة Excel. يجب أن يكون الملف موجودًا.

##### <a name="playback-examples"></a>playback: أمثله

`playback c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playback /retry e:\temp\test.xlsx`

`playback /retry=300 e:\temp\test.xlsx`

`playback /comments="Payroll solution 10.0.0" e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

يمكنك تشغيل عدة حالات اختبار في نفس الوقت. يتم تحديد حالات الاختبار من خلال معرفاتهم. سيقوم هذا الأمر بتنزيل الملفات من Azure DevOps. يمكنك استخدام الأمر ``list`` للحصول علي كافة حالات الاختبار المتوفرة، واستخدام أي قيمة من العمود الأول كمعلمة **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[/retry[=<seconds>]] [/comments[="comment"]] [test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-optional-switches"></a>playbackbyid: مفاتيح التبديل الاختيارية

+ `/retry[=seconds]`: إذا تم تحديد رمز التبديل هذا، وتم حظر حالات اختبار الحالة بواسطة مثيلات RSAT الأخرى، فستنتظر عملية التشغيل عدد الثواني المحدد ثم المحاولة مرة أخرى. وتكون القيمة الافتراضية \[120\] ثانية. بدون هذا المفتاح، سيتم إلغاء العملية على الفور إذا تم حظر حالات الاختبار.
+ `/comments[="comment"]`: قم بتوفير سلسلة معلومات مخصصة سيتم تضمينها في الحقل **التعليقات** في الملخص وصفحات نتائج الاختبار لتشغيل حالة اختبار Azure DevOps.

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: المعلمات المطلوبة

+ `test_case_id1`: معرف حالة اختبار موجودة.
+ `test_case_id2`: معرف حالة اختبار موجودة.
+ `test_case_idN`: معرف حالة اختبار موجودة.

##### <a name="playbackbyid-examples"></a>playbackbyid: أمثله

`playbackbyid 878`

`playbackbyid 2345 667 135`

`playbackbyid /comments="Payroll solution 10.0.0" 2345 667 135`

`playbackbyid /retry /comments="Payroll solution 10.0.0" 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

يمكنك تشغيل العديد من حالات الاختبار في نفس الوقت. يتم تحديد حالات الاختبار بواسطة ملفات معلمة Excel. يستخدم هذا الأمر ملفات التشغيل التلقائي المحلية الموجودة ولا يقوم بتنزيل الملفات من Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file1] [excel_parameter_file2] ... [excel_parameter_fileN]``

##### <a name="playbackmany-optional-switches"></a>playbackmany: مفاتيح التبديل الاختيارية

+ `/retry[=seconds]`: إذا تم تحديد رمز التبديل هذا، وتم حظر حالات اختبار الحالة بواسطة مثيلات RSAT الأخرى، فستنتظر عملية التشغيل عدد الثواني المحدد ثم المحاولة مرة أخرى. وتكون القيمة الافتراضية \[120\] ثانية. بدون هذا المفتاح، سيتم إلغاء العملية على الفور إذا تم حظر حالات الاختبار.
+ `/comments[="comment"]`: قم بتوفير سلسلة معلومات مخصصة سيتم تضمينها في الحقل **التعليقات** في الملخص وصفحات نتائج الاختبار لتشغيل حالة اختبار Azure DevOps.

##### <a name="playbackmany-required-parameters"></a>playbackmany: المعلمات المطلوبة

+ `excel_parameter_file1`: المسار الكامل لملف معلمة Excel. يجب أن يكون الملف موجودًا.
+ `excel_parameter_file2`: المسار الكامل لملف معلمة Excel. يجب أن يكون الملف موجودًا.
+ `excel_parameter_fileN`: المسار الكامل لملف معلمة Excel. يجب أن يكون الملف موجودًا.

##### <a name="playbackmany-examples"></a>playbackmany: أمثله

`playbackmany c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playbackmany e:\temp\test.xlsx f:\RSAT\sample1.xlsx c:\RSAT\sample2.xlsx`

`playbackmany /retry=180 /comments="Payroll solution 10.0.0" e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

يقوم بتشغيل كافة حالات الاختبار من مجموعة واحدة أو أكثر من مجموعات الاختبار المحددة. إذا تم تحديد مفتاح التبديل /local، فسيتم استخدام المرفقات المحلية للتشغيل. وإلا فسيتم تنزيل المرفقات من Azure DevOps. يمكنك استخدام الأمر ``listtestsuitenames`` للحصول على جميع مجموعات الاختبار المتاحة، واستخدام أي قيمة من العمود الأول كمعلمة **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] ([test_suite_name1] .. [test_suite_nameN] | [/byid] [test_suite_id1] .. [test_suite_idN])``

##### <a name="playbacksuite-optional-switches"></a>playbacksuite: مفاتيح التبديل الاختيارية

+ `/updatedriver`: إذا تم تحديد رمز التبديل هذا، فسيتم تحديث محرك الويب لمتصفح الإنترنت بالشكل المطلوب قبل تشغيل عملية التشغيل.
+ `/local`: يشير رمز التبديل هذا إلى وجوب استخدام المرفقات المحلية للتشغيل بدلاً من تنزيل الملفات من Azure DevOps.
+ `/retry[=seconds]`: إذا تم تحديد رمز التبديل هذا، وتم حظر حالات اختبار الحالة بواسطة مثيلات RSAT الأخرى، فستنتظر عملية التشغيل عدد الثواني المحدد ثم المحاولة مرة أخرى. وتكون القيمة الافتراضية \[120\] ثانية. بدون هذا المفتاح، سيتم إلغاء العملية على الفور إذا تم حظر حالات الاختبار.
+ `/comments[="comment"]`: قم بتوفير سلسلة معلومات مخصصة سيتم تضمينها في الحقل **التعليقات** في الملخص وصفحات نتائج الاختبار لتشغيل حالة اختبار Azure DevOps.
+ `/byid`: يشير رمز التبديل هذا إلى أن مجموعة الاختبار المطلوبة يتم تحديدها من خلال معرف Azure DevOps الخاص بها بدلاً من اسم مجموعة الاختبار.

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: المعلمات المطلوبة

+ `test_suite_name1`: تمثل اسم مجموعة الاختبار. تكون هذه المعلمة مطلوبة إذا كان رمز التبديل /byid **غير** محدد. يكون هذا الاسم هو اسم مجموعة اختبار Azure DevOps.
+ `test_suite_nameN`: تمثل اسم مجموعة الاختبار. تكون هذه المعلمة مطلوبة إذا كان رمز التبديل /byid **غير** محدد. يكون هذا الاسم هو اسم مجموعة اختبار Azure DevOps.
+ `test_suite_id1`: تمثل معرف مجموعة الاختبار. تكون هذه المعلمة مطلوبة إذا كان رمز التبديل /byid **محددًا**. يكون هذا المعرف هو معرف مجموعة Azure DevOps الاختبارية.
+ `test_suite_idN`: تمثل معرف مجموعة الاختبار. تكون هذه المعلمة مطلوبة إذا كان رمز التبديل /byid **محددًا**. يكون هذا المعرف هو معرف مجموعة Azure DevOps الاختبارية.

##### <a name="playbacksuite-examples"></a>playbacksuite: أمثله

`playbacksuite suiteName`

`playbacksuite suiteName suiteNameToo`

`playbacksuite /updatedriver /local /retry=180 /byid 151 156`

`playbacksuite /updatedriver /local /comments="Payroll solution 10.0.0" /byid 150`

#### <a name="playbacksuitebyid"></a>playbacksuitebyid

يقوم بتشغيل جميع حالات الاختبار في مجموعة اختبارات Azure DevOps المحددة.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuitebyid``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] [test_suite_id]``

##### <a name="playbacksuitebyid-optional-switches"></a>playbacksuitebyid: مفاتيح التبديل الاختيارية

+ `/retry[=seconds]`: إذا تم تحديد رمز التبديل هذا، وتم حظر حالات اختبار الحالة بواسطة مثيلات RSAT الأخرى، فستنتظر عملية التشغيل عدد الثواني المحدد ثم المحاولة مرة أخرى. وتكون القيمة الافتراضية \[120\] ثانية. بدون هذا المفتاح، سيتم إلغاء العملية على الفور إذا تم حظر حالات الاختبار.
+ `/comments[="comment"]`: قم بتوفير سلسلة معلومات مخصصة سيتم تضمينها في الحقل **التعليقات** في الملخص وصفحات نتائج الاختبار لتشغيل حالة اختبار Azure DevOps.
+ `/byid`: يشير رمز التبديل هذا إلى أن مجموعة الاختبار المطلوبة يتم تحديدها من خلال معرف Azure DevOps الخاص بها بدلاً من اسم مجموعة الاختبار.

##### <a name="playbacksuitebyid-required-parameters"></a>playbacksuitebyid: المعلمات المطلوبة

+ `test_suite_id`: يمثل معرف مجموعة الاختبار كما هو موجود في Azure DevOps.

##### <a name="playbacksuitebyid-examples"></a>playbacksuitebyid: الأمثلة

`playbacksuitebyid 2900`

`playbacksuitebyid /retry 2099`

`playbacksuitebyid /retry=200 2099`

`playbacksuitebyid /retry=200 /comments="some comment" 2099`

#### <a name="quit"></a>إنهاء

غلق التطبيق. يكون هذا الأمر مفيدًا فقط عند تشغيل التطبيقات في الوضع التفاعلي.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

##### <a name="quit-examples"></a>quit: الأمثلة

`quit`

#### <a name="upload"></a>تحميل

تحميل ملفات المرفقات (ملفات التسجيل والتنفيذ والمعلمات) التي تنتمي إلى مجموعة اختبار محددة أو حالات اختبار إلى Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``([test_suite_name] | [test_case_id1] .. [test_case_idN])``

##### <a name="upload-required-parameters"></a>upload: المحددات المطلوبة

+ `test_suite_name`: سيتم تحميل جميع الملفات التي تخص مجموعة الاختبار المحددة.
+ `test_case_id1`: يمثل معرّف حالة الاختبار الأول الذي يجب تحميله. استخدم هذه المعلمة فقط في حالة عدم تقديم اسم مجموعة اختبار.
+ `test_case_idN`: يمثل آخر معرف حالة اختبار يجب تحميله. استخدم هذه المعلمة فقط في حالة عدم تقديم اسم مجموعة اختبار.

##### <a name="upload-examples"></a>upload: أمثله

`upload sample_suite`

`upload 2900`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

يقوم بتحميل فقط ملف التسجيل الذي يخص حالة اختبار محددة أو أكثر إلى Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[test_case_id1] .. [test_case_idN]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: المحددات المطلوبة

+ `test_case_id1`: يمثل معرّف حالة الاختبار الأول للتسجيل الذي يجب تحميله إلى Azure DevOps.
+ `test_case_idN`: يمثل معرّف حالة الاختبار الأول للتسجيل الذي يجب تحميله إلى Azure DevOps.

##### <a name="uploadrecording-examples"></a>uploadrecording: أمثله

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>استخدام

يعرض ثلاثة أوضاع لاستخدام هذا التطبيق.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

تشغيل التطبيق بشكل تفاعلي:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``

تشغيل التطبيق بتحديد أمر:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp ``**``[command]``**

تشغيل التطبيق من خلال توفير ملف إعدادات:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``/settings [drive:\Path to\file.settings] [command]``**

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

```powershell
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
