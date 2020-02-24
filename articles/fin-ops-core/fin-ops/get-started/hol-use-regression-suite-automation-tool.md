---
title: استخدام برنامج Regression suite automation tool التعليمي
description: يوضح هذا الموضوع كيفية استخدام أداة Regression suite automation tool (RSAT). وهو يصف ميزات مختلفة ويوفر أمثلة تستخدم البرمجة النصية المتقدمة.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 026d1d743b5150f152ef70aa642dcf6841a4e398
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025794"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a>استخدام البرنامج التعليمي للأداة Regression Suite Automation Tool

[!include [banner](../includes/banner.md)]

> [!NOTE]
> استخدم أدوات مستعرض الإنترنت لتنزيل هذه الصفحة وحفظها بتنسيق pdf. 

يعرفك هذا البرنامج التعليمي على بعض الميزات المتقدمة الخاصة بأداة Regression suite automation tool (RSAT)، ويتضمن تعيين عرض توضيحي، ويصف الاستراتيجية ونقاط التعليم الأساسية.

## <a name="features-of-rsattask-recorder"></a>ميزات RSAT/مسجل المهام

### <a name="validate-a-field-value"></a>التحقق من قيمة الحقل

للحصول على معلومات حول هذه الميزة، راجع [إنشاء تسجيل مهمة جديدة يحتوي وظيفة التحقق من الصحة](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).

### <a name="saved-variable"></a>المتغير المحفوظ

للحصول على معلومات حول هذه الميزة، راجع [تعديل تسجيل مهمة موجودة لإنشاء متغير محفوظ](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).

### <a name="derived-test-case"></a>حالة الاختبار المشتقة

1. افتح أداة Regression suite automation tool (RSAT)، وحدد كلا من حالتي الاختبار التي أنشأتها في [إعداد وتثبيت أداة Regression suite automation Tool](./hol-set-up-regression-suite-automation-tool.md).
2. حدد **جديد \> إنشاء حالة اختبار مشتقة**.

    ![أمر إنشاء أمر حالة اختبار مشتق في القائمة جديد](./media/use_rsa_tool_01.png)

3. ستستلم رسالة توضح أنه سيتم إنشاء حالة اختبار مشتقة لكل حالة اختبار محددة في مجموعة الاختبار الحالية، وأن كل حالة اختبار مشتقة سيكون لها نسختها الخاصة من ملف معلمة Excel. حدد **موافق**.

    > [!NOTE]
    > عند تشغيل حالة اختبار مشتقة، فإنها تستخدم تسجيل المهمة لحالة الاختبار الرئيسية الخاصة بها ونسخة خاصة بها من ملف معلمة Excel. وبهذه الطريقة، يمكنك تشغيل نفس الاختبار مع معلمات مختلفة، دون الحاجة إلى الاحتفاظ بأكثر من تسجيل مهمة واحد. لا يجب أن تكون حالة الاختبار المشتقة جزءا من مجموعة الاختبار نفسها المتخذة كحالة اختبار الأصل لها.

    ![مربع الرسالة](./media/use_rsa_tool_02.png)

    يتم إنشاء حالتي اختبار مشتقين إضافيتين، مع تحديد خانة الاختيار **مشتق؟** لهما.

    ![حالات الاختبار المشتقة التي تم إنشاؤها](./media/use_rsa_tool_03.png)

    يتم إنشاء حالة اختبار مشتقة بشكل تلقائي Azure DevOps. وهي عنصر فرعي لحالة الاختبار **إنشاء منتج جديد** ويتم تعليمه بكلمة أساسية خاصة: **RSAT:DerivedTestSteps**. يتم أيضا إضافة حالات الاختبار هذه تلقائيا إلى خطة الاختبار في Azure DevOps.

    ![RSAT:الكلمة الأساسية DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > إذا كانت حالات الاختبار المشتقة التي تم إنشائها بترتيب غير صحيح لأي سبب، فاذهب إلى Azure DevOps، وأعد ترتيب حالات الاختبار في مجموعة الاختبار، بحيث يمكن لأداة RSAT تشغيلها بالترتيب الصحيح.

4. حدد حالات الاختبار المشتقة، ثم حدد **تحرير** لفتح ملفات معلمات Excel المطابقة.
5. حرر ملفات معلمات Excel هذه بنفس الطريقة التي تم بها تحرير الملفات الأصلية. بمعنى آخر، تأكد من تعيين معرف المنتج بحيث يتم إنشاؤه تلقائيا. وتأكد أيضا من نسخ المتغير المحفوظ إلى الحقول ذات الصلة.
6. في علامة التبويب **عام** لكل من ملفات معلمات Excel، قم بتحديث قائمة حقل **الشركة** إلى **USSI**، بحيث يتم تشغيل حالات الاختبار المشتقة مقابل كيان قانوني مختلف عن حالة الاختبار الأصلية. لتشغيل حالات الاختبار لمستخدم محدد (أو الدور المرتبط بمستخدم معين)، يمكنك تحديث قيمه حقل **اختبار المستخدم**.
7. حدد **تشغيل**، وتحقق من إنشاء المنتج في كل من الكيان القانوني USMF والكيان القانوني USSI.

### <a name="validate-notifications"></a>إخطارات التحقق

يمكن استخدام هذه الميزة للتحقق مما إذا كان الإجراء قد حدث أم لا. علي سبيل المثال، عند إنشاء أمر إنتاج وتقديره ثم بدء تشغيله، يعرض التطبيق الرسالة "الإنتاج – بدء" لإعلامك بأنه قد تم بدء أمر الإنتاج.

![إخطار الإنتاج - بدء](./media/use_rsa_tool_05.png)

يمكنك التحقق من صحة هذه الرسالة عن طريق RSAT وذلك بإدخال نص الرسالة في علامة التبويب **MessageValidation** في ملف معلمة Excel للتسجيل المناسب.

![علامة تبويب التحقق من الرسالة](./media/use_rsa_tool_06.png)

بعد تشغيل حالة الاختبار، تتم مقارنة الرسالة الموجودة في ملف معلمة Excel بالرسالة المعروضة. في حالة عدم تطابق الرسائل، ستفشل حالة الاختبار.

> [!NOTE]
> يمكنك إدخال أكثر من رسالة واحدة في علامة تبويب **MessageValidation** في ملف معلمة Excel. يمكن أن تكون الرسائل أيضا رسائل خطا أو تحذيرات بدلا من الرسائل الإخبارية.

### <a name="validate-values-by-using-operators"></a>التحقق من صحة القيم باستخدام عوامل التشغيل

في الإصدارات السابقة من RSAT، يمكنك التحقق من صحة القيم فقط إذا كانت قيمة العنصر التحكم مساوية لقيمة متوقعة. تتيح لك الميزة الجديدة التحقق من أن أحد المتغيرات لا يساوي أو أقل من أو أكبر من القيمة المحددة.

- لاستخدام هذه الميزة، افتح ملف **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**، تحت مجلد تثبيت RSAT (على سبيل المثال، **C:\\Program Files (x86)\\Regression Suite Automation Tool**)، وقم بتغيير القيمة في العنصر التالي من **false** إلى **true**.

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    في ملف معلمة Excel، يظهر حقل **عامل تشغيل** جديد.

    > [!NOTE]
    > إذا كنت تستخدم إصدارا قديما من RSAT، يجب إنشاء ملفات معلمات جديدة لـ Excel.

    ![حقل عامل التشغيل](./media/use_rsa_tool_07.png)

يوضح المثال التالي كيفية استخدام هذه الميزة للتحقق مما إذا كان المخزون الفعلي أكبر من 0 (صفر).

1. في البيانات التوضيحية في شركة **USMF**، قم بإنشاء تسجيل مهام بالخطوات التالية:

    1. انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.
    2. استخدم عامل التصفية السريع للبحث عن السجلات. على سبيل المثال، قم بإجراء التصفية على قيمة **1000** للحقل **رقم الصنف**.
    3. حدد **المخزون الفعلي**.
    4. استخدم عامل التصفية السريع للبحث عن السجلات. على سبيل المثال، قم بإجراء التصفية على القيمة **1** لحقل **الموقع**.
    5. في القائمة، قم بوضع علامة للصف المحدد.
    6. تحقق من أن قيمة حقل **الإجمالي المتاح** هي **411.0000000000000000**.

2. احفظ تسجيل المهام في مكتبة BPM في LCS، وقم بمزامنته مع Azure DevOps.
3. قم بإضافة حالة الاختبار إلى خطة الاختبار، وقم بتحميل حالة الاختبار إلى RSAT.
4. افتح ملف معلمة Excel. في علامة تبويب **InventOnhandItem**، سوف تشاهد قسم **التحقق من InventOnhandItem** الذي يتضمن حقل **عامل التشغيل**.

    ![حقل عامل التشغيل](./media/use_rsa_tool_08.png)

5. للتحقق مما إذا كان المخزون الفعلي سيكون دائمًا أكبر من 0، قم بتغيير القيمة في حقل **القيمة** من **411** إلى **0** وقيمة حقل **عامل التشغيل** من علامة يساوي (**=**) إلى أكبر من (**\>**).

    ![تم تغيير القيم لحقول القيمة وعامل التشغيل](./media/use_rsa_tool_09.png)

6. احفظ ملف معلمات Excel وأغلقه.
7. حدد **تحميل** لحفظ التغييرات التي أجريتها على ملف معلمات Excel إلى Azure DevOps.

والآن، إذا كانت قيمة حقل **الإجمالي المتوفر** للصنف المحدد في المخزون أكبر من 0 (صفر)، سيتم اجتياز الاختبارات، بغض النظر عن قيمة المخزون الفعلي.

### <a name="generator-logs"></a>سجلات المنشئ

تقوم هذه الميزة بإنشاء مجلد يحتوي على سجلات حالات الاختبار التي تم تشغيلها.

- لاستخدام هذه الميزة، افتح ملف **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**، تحت مجلد تثبيت RSAT (على سبيل المثال، **C:\\Program Files (x86)\\Regression Suite Automation Tool**)، وقم بتغيير القيمة في العنصر التالي من **false** إلى **true**.

    ```xml
    <add key="LogGeneration" value="false" />
    ```

بعد تشغيل حالات الاختبار، يمكنك العثور على ملفات السجل تحت **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.

![المجلد GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> إذا كانت هناك حالات اختبار موجودة قبل تغيير القيمة في ملف .config، لن يتم إنشاء السجلات لحالات الاختبار هذه حتى تقوم بإنشاء ملفات تنفيذ اختبار جديدة.
> 
> ![إنشاء أمر ملفات تنفيذ النص فقط في القائمة جديد](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a>لقطة

تقوم هذه الميزة بأخذ لقطات شاشة الخطوات التي تم إجراؤها أثناء تسجيل المهام.

- لاستخدام هذه الميزة، افتح ملف **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**، تحت مجلد تثبيت RSAT (على سبيل المثال، **C:\\Program Files (x86)\\Regression Suite Automation Tool**)، وقم بتغيير القيمة للعنصر التالي من **false** إلى **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

تحت **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**، يتم إنشاء مجلد منفصل لكل حالة اختبار يتم تشغيلها.

![مجلد اللقطات لحالة اختبار](./media/use_rsa_tool_12.png)

في كل من هذه المجلدات، يمكنك العثور على لقطات للخطوات التي تم تنفيذها أثناء تشغيل حالات الاختبار.

![ملفات اللقطات](./media/use_rsa_tool_13.png)

## <a name="assignment"></a>التعيين

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

يعرض الرسم التوضيحي التالي العمليات التجارية لهذا السيناريو في RSAT.

![العمليات التجارية للسيناريو التوضيحي](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>الاستراتيجية – التعليم الأساسي

### <a name="data"></a>البيانات

- تأكد أن لديك وحدات تخزين بيانات تمثيلية (نسخة من بيانات الإنتاج/التكوين الذهبي بالإضافة إلى بيانات تم ترحيلها).
- عند إنشاء البيانات الجديدة عبر مسجل المهام، قم بإنشاء أسماء الاختبارات التي لا تتعارض مع الأسماء الموجودة (علي سبيل المثال، استخدم بادئة مثل **RSATxxx**).
- استخدم استعادة النقطة الزمنية في Azure لإعادة تشغيل الاختبارات في بيئات ليست من المستوي 1.
- على الرغم من أنه يمكنك استخدام دالتي Excel **RANDOM** و**NOW** لإنشاء مجموعة فريدة، فإن الجهد يكون مرتفعا بشكل كبير. فيما يلي مثال على ذلك.

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>مسجل المهام

- حدد السيناريوهات قبل بدء التسجيل. يحتوي المشروع جيد الإدارة على سيناريوهات اختبار معرفة مسبقا. لبناء حالة اختبار، ضع في الاعتبار مدي توقع نتيجة سيناريوهات الاختبار هذه.
- قسم التسجيلات في حالة تنفيذها بواسطة أدوار مختلفة، أو إذا كان هناك وقت انتظار أو حدث خارجي قبل الخطوة التالية.
- تجنب تحديد القيم في القوائم. بدلا من ذلك، استخدم تنسيقات نصية، مثل **FIFO** و **AudioRM** و **SiteWH**. عندم تحدد في القائمة، يتم تسجيل موضع القيمة في القائمة، وليس القيمة نفسها. إذا تمت إضافة عناصر إلى هذه القائمة، يمكن تغيير وضع القيمة. لذلك، سيقوم التسجيل الخاص بك باستخدام معلمة مختلفة، وقد يتأثر باقي السيناريو.
- فكر في سلوك المستخدمين المتعددين. علي سبيل المثال، لا تفترض أن أمر التوريد الذي تم إنشاؤه حديثا سيتم دوما تحديده تلقائيا. بدلا من ذلك، استخدم عامل التصفية دائما للعثور على الطلب الصحيح.
- استخدم وظيفة النسخ في مسجل المهام لحفظ اسم منتج تم إنشاؤه حديثا بحيث يمكن استخدامه في حالات الاختبار المتسلسلة.
- استخدم وظيفة التحقق من الصحة في مسجل المهام لتعيين نقاط التحقق التي تتحقق من أن الخطوات تم تشغيلها بشكل صحيح.

### <a name="rsat"></a>RSAT

- لتشغيل الاختبار في شركة أخرى، يمكنك تغيير الشركة في علامة التبويب **عام** بملف معلمة Excel. تأكد من توفر الإعدادات والبيانات في الشركة المحددة حديثا.
- يمكنك تغيير مستخدم الاختبار في علامة التبويب **عام** بملف معلمة Excel. حدد معرف البريد الإلكتروني الخاص بالمستخدم الذي سيقوم بتشغيل حالة الاختبار. بهذه الطريقة، يمكن تشغيل حالة الاختبار باستخدام أذونات الأمان الخاصة بالمستخدم المحدد.
- للانتظار قبل بدء الاختبار، يمكنك تعريف توقف مؤقت في علامة التبويب **عام** بملف معلمة Excel. يمكن استخدام الإيقاف المؤقت هذا في وظيفة دفعية (علي سبيل المثال، إذا كان من الضروري تشغيل سير عمل قبل إجراء الخطوة التالية.)

## <a name="advanced-scripting"></a>البرمجة المتقدمة

### <a name="command-line"></a>سطر الأمر

يمكن استدعاء RSAT من إطار **موجه الأوامر**.

> [!NOTE]
> تحقق من تعيين متغير البيئة **TestRoot** على مسار تثبيت RSAT. (في Microsoft Windows، افتح **لوحة التحكم**، وحدد **النظام والأمان \> النظام \> إعدادات الأمان المتقدمة**، ثم حدد **متغيرات البيئة**.)

1. افتح إطار **موجه الأوامر** كمسؤول.
2. قم بتشغيل الأداة من دليل التثبيت.

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
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a>أمثلة Windows PowerShell

#### <a name="run-a-test-case-in-a-loop"></a>تشغيل حالة اختبار في حلقة

لديك برنامج اختبار نصي يقوم بإنشاء عميل جديد. بواسطة البرمجة النصية، يمكن تشغيل حالة الاختبار هذه في حلقة عن طريق الترتيب العشوائي للبيانات التالية قبل تشغيل كل تكرار:

- معرف العميل
- اسم العميل
- عنوان العميل

سيكون معرف العميل بالتنسيق *ATCUS\<رقم\>*، حيث يكون \<الرقم\> قيمة بين **000000001** و **999999999**.

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
$excelFilename = "full path to excel file parameter file"
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
