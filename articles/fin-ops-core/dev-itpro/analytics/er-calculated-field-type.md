---
title: دعم استدعاءات ذات معلمات لمصادر بيانات التقارير الإلكترونية لنوع الحقل المحسوب‬
description: توفر هذه المقالة معلومات عن كيفية استخدام نوع الحقل المحسوب لمصادر بيانات التقارير الإلكترونية.
author: kfend
ms.date: 01/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 512ef44d0b0867227ebdc56f83cd6560be64c026
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276007"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a>دعم استدعاءات ذات معلمات لمصادر بيانات التقارير الإلكترونية لنوع الحقل المحسوب‬

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية تصميم مصدر بيانات التقارير الإلكترونية باستخدام نوع **الحقل المحسوب** . قد يحتوي مصدر البيانات هذا على تعبير التقارير الإلكترونية الذي، عند تنفيذه، يمكن التحكم به بواسطة قيم وسيطات المعلمة التي تم تكوينها في الربط الذي يستدعي مصدر البيانات هذا. ومن خلال تكوين استدعاءات ذات معلمات لمصدر البيانات هذا، يمكنك إعادة استخدام مصدر بيانات واحد في العديد من عمليات الربط، مما يقلل العدد الإجمالي لمصادر البيانات التي يجب تكوينها في تعيينات نماذج التقارير الإلكترونية أو تنسيقاتها. ويقوم أيضا بتبسيط مكون التقارير الإلكترونية الذي تم تكوينه، مما يقلل من تكاليف الصيانة وتكلفة الاستخدام من قبل العملاء الآخرين.

## <a name="prerequisites"></a>المتطلبات الأساسية
لإكمال الأمثلة في هذا البرنامج التعليمي، يجب أن تتمتع بالوصول التالي:

- الوصول إلى أحد هذه الأدوار:

    - مطور إعداد التقارير الإلكتروني
    - مستشار وظيفي لإعداد التقارير الإلكتروني
    - مسؤول النظام

- يمكنك الوصول إلى مثيل Regulatory Configuration Services (RCS) التي تم تزويدها لنفس المستأجر مثل التمويل والعمليات، لأحد الأدوار التالية:

    - مطور إعداد التقارير الإلكتروني
    - مستشار وظيفي لإعداد التقارير الإلكتروني
    - مسؤول النظام

يجب عليك أيضًا تنزيل الملفات التالية وتخزينها محليًا.

| **المحتوى**                           | **اسم الملف**                                        |
|---------------------------------------|------------------------------------------------------|
| تكوين نموذج عينة بيانات التقارير الإلكترونية    | [Model to learn parameterized calls.version.1.xml](https://download.microsoft.com/download/e/5/c/e5c0d3f9-1818-47c7-ae75-46efcbb1314f/Modeltolearnparameterizedcallsversion.1.xml)     |
| تكوين بيانات تعريف عينة التقارير الإلكترونية      | [Metadata to learn parameterized calls.version.1.xml](https://download.microsoft.com/download/8/3/a/83a910a5-bf65-4509-bec4-6737a81ecc45/Metadatatolearnparameterizedcalls.version.1.xml)  |
| تكوين تعيين نموذج عينة التقارير الإلكترونية | [Mapping to learn parameterized calls.version.1.1.xml](https://download.microsoft.com/download/b/f/d/bfd8cbd8-0370-44d1-a1b1-66d021c580ca/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| تكوين تنسيق عينة التقارير الإلكترونية        | [Format to learn parameterized calls.version.1.1.xml](https://download.microsoft.com/download/8/1/d/81deb6d8-a768-4fcf-bbbe-8f84d2dac3eb/Formattolearnparameterizedcalls.version.1.1.xml)  |

## <a name="sign-in-to-your-rcs-instance"></a>تسجيل الدخول إلى مثيل RCS
في هذا المثال، سوف تنشئ تكوينًا للشركة النموذجية Litware, Inc. في RCS يجب عليك أولاً إكمال الخطوات الموجودة في الإجراء [‏‫إنشاء موفري التكوين ووضع علامة عليهم على أنهم نشيطون‬](tasks/er-configuration-provider-mark-it-active-2016-11.md):

1. في لوحة المعلومات الافتراضية، حدد **‏‫إعداد التقارير الإلكترونية**.
2. حدد **تكوينات إعداد التقارير‬**.
3. قم باستيراد التكوينات التي تم تنزيلها إلى RCS بالتسلسل التالي: نموذج البيانات، وبيانات التعريف، وتعيين النموذج، والتنسيق. أكمل الخطوات التالية لكل تكوين خاص بإعداد التقارير الإلكترونية:

    1. حدد **تبادل**.
    2. حدد **تحميل من ملف XML**.
    3. حدد **استعراض**، ثم حدد الملف المطلوب لتكوين التقارير الإلكترونية بالتنسيق XML.
    4. حدد **موافق**.

## <a name="review-the-provided-er-solution"></a>مراجعه الحل المتوفر لإعداد التقارير الإلكترونية

### <a name="review-model-mapping"></a>مراجعة تعيين النموذج

1. في شجرة التكوين، قم بتوسيع محتوى العنصر **نموذج للتعرف على الاستدعاءات ذات معلمات‬**.
2. حدد **تعيين للتعرف على الاستدعاءات ذات معلمات**.
3. حدد **المصمم**.
4. حدد **المصمم**.  
   
    يتم تصميم تعيين نموذج إعداد التقارير الإلكترونية هذا للقيام بما يلي:

    - إحضار قائمة بأكواد الضريبة (مصدر بيانات **الضريبة**) الموجودة في الجدول **TaxTable**.
    - إحضار قائمة بحركات الضريبة (مصدر بيانات **الحركة**) الموجودة في الجدول **TaxTrans**:
    
        - تجميع قائمة بالحركات التي تم إحضارها (مصدر بيانات **التجميع**) حسب كود الضريبة.
        - حساب الحركات المجمعة التي تتبع القيم المجمعة حسب كود الضريبة:

            - مجموع قيم أساس الضريبة.
            - مجموع قيم الضريبة.
            - الحد الأدنى لقيمة معدل الضريبة المطبق.

    يقوم تعيين النموذج في هذا التكوين بتنفيذ نموذج البيانات الأساسي لأي من تنسيقات التقارير الإلكترونية التي تم إنشاؤها لهذا النموذج وتنفيذها في التمويل والعمليات. نتيجة لذلك، يتم كشف محتوى مصادر بيانات **الضريبة** و **التجميع** لتنسيقات التقارير الإلكترونية مثل مصادر البيانات المجردة.

    ![صفحة مصمم تعيين النموذج التي تعرض مصادر بيانات الضريبة والتجميع.](media/er-calculated-field-type-01.png)

5.  أغلق صفحة **مصمم تعيين النموذج**.
6.  أغلق صفحة **تعيين النموذج**.

### <a name="review-format"></a>مراجعة التنسيق

1. في شجرة التكوين، قم بتوسيع محتوى العنصر **نموذج للتعرف على الاستدعاءات ذات معلمات‬**.
2. حدد **تنسيق للتعرف على الاستدعاءات ذات معلمات**.
3. حدد **المصمم**. يتم تصميم تنسيق إعداد التقارير الإلكترونية هذا للقيام بما يلي:

    - إنشاء بيان ضريبة بتنسيق XML.
    - تقديم المستويات التالية لفرض الضرائب في بيان الضريبة: العادي والمخفض ولا شيء.
    - تقديم تفاصيل متعدد في كل مستوى فرض ضرائب، مع وجود عدد مختلف من التفاصيل في كل مستوى.

    ![صفحة مصمم التنسيق‬.](media/er-calculated-field-type-02.png)

4. حدد **التعيين**.
5. قم بتوسيع عناصر **النموذج**، و **البيانات**، و **الملخص**. 

    يحتوي الحقل المحسوب **Model.Data.Summary.Level** على التعبير الذي يقوم بإرجاع كود مستوى فرض الضرائب (**العادي**، أو **المخفض**، أو **لا شيء**، أو **غير ذلك**) كقيمة نصية لأي كود ضريبة يمكن استرجاعه من مصدر البيانات **Model.Data.Summary** في وقت التشغيل.

    ![صفحة مصمم تنسيق تظهر تفاصيل نموذج لنموذج بيانات لمعرفة الاستدعاءات ذات معلمات.](media/er-calculated-field-type-03.png)

6. قم بتوسيع عنصر **Model**.**Data2**.
7. قم بتوسيع عنصر **Model**.**Data2.Summary2**.
   
    يتم تكوين مصدر البيانات **Model**.**Data2.Summary2** لتجميع تفاصيل حركة مصدر بيانات **Model.Data.Summary** حسب مستوى فرض الضرائب (الذي يتم إرجاعه بواسطة الحقل المحسوب **Model.Data.Summary.Level**) وحساب التجميعات.

    ![صفحة مصمم تنسيق تُظهر تفاصيل مصدر بيانات Model.Data2.Summary2.](media/er-calculated-field-type-04.png)

8. راجع الحقول المحسوبة **Model**.**Data2.Level1**، و **Model**.**Data2.Level2**، و **Model**.**Data2.Level3**. يتم استخدام هذه الحقول المحسوبة لتصفية قائمة سجلات **Model**.**Data2.Summary2** وإرجاع السجلات التي تمثل مستوى فرض ضرائب معين فقط.
9. أغلق صفحة **مصمم المعادلة**.

## <a name="create-a-derived-format"></a>إنشاء تنسيق مشتق
يمكنك تحسين التنسيق المتوفر عن طريق إضافة حقل محسوب واحد لتصفية مستوى فرض الضرائب المطلوب بدلاً من استخدام الحقول الثلاثة الموجودة: **Model**.**Data2.Level1**، و **Model**.**Data2.Level2**، و **Model**.**Data2.Level3**. يمكن تحديد مستوى فرض الضرائب المطلوب في الموقع الذي سيتم فيه استدعاء هذا الحقل الجديد المحسوب.

1. في شجرة التكوين، قم بتوسيع محتوى العنصر **نموذج للتعرف على الاستدعاءات ذات معلمات‬**.
2. حدد **تنسيق للتعرف على الاستدعاءات ذات معلمات**.
3. حدد **إنشاء التكوين**.
4. حدد **اشتقاق من الاسم: تنسيق للتعرف على الاستدعاءات ذات معلمات، Microsoft**.
5. في حقل **الاسم**، أدخل **تنسيق للتعرف على الاستدعاءات ذات معلمات (مخصص)**.
6. حدد **إنشاء التكوين**.

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a>تكوين حقل محسوب ذي معلمات يرجع قائمة سجلات

### <a name="start-adding-a-new-calculated-field"></a>بدء إضافة حقل محسوب جديد

1. حدد **المصمم**.
2. حدد **توسيع/طي** لتوسيع كافة عناصر التنسيق.
3. حدد **التعيين**.
4. قم بتوسيع عنصر **النموذج**.
5. حدد عنصر **Model.Data2**.
6. حدد **إضافة**.
7. حدد **الوظائف\\حقل محسوب**.
8. في حقل **الاسم**، أدخل **المستويات**.
9. حدد **تحرير المعادلة**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>تحديد معلمة لإضافة حقل محسوب

1. حدد **معلمات**.
2. حدد **جديد**.
3. في حقل **الاسم**، أدخل **مستوى فرض الضرائب**.
4. في حقل **النوع**، حدد **سلسلة**.

    يمكن استخدام أنواع البيانات الأولية فقط لتحديد نوع وسيطة المعلمة. ولهذا لا يمكن استخدام الأنواع **قائمة سجلات**، و **سجل**، و **التعداد** لهذا الغرض.

    الحد الأقصى لعدد المعلمات التي يمكن تحديدها لحقل محسوب واحد هو 8.

    ![قائمة مصادر بيانات المعلمات.](media/er-calculated-field-type-05.png)

5. حدد **موافق**.

بإضافة هذه المعلمة، فأنت تحدد الشرط الذي يجب توفره لاستدعاء هذا الحقل المحسوب. عند استدعاء هذا الحقل المحسوب، يجب تحديد وسيطة معلمة **مستوى فرض الضرائب** كقيمة بتنسيق **سلسلة**.

   تأكد من تعريف المعلمات فقط للحقول المحسوبة الموجودة في حاوية (إما **قائمة السجلات**، أو **السجل**، أو **الحاوية**).

   تتوفر المعلمة المكونة في قائمة مصادر البيانات لهذا الحقل المحسوب. يمكنك إضافة المعلمة إلى التعبير المكون عن طريق تحديد **إضافة مصدر بيانات**.

   ![حقول مصادر البيانات.](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a>تحديد تعبير لإضافة حقل محسوب

1. في حقل **المعادلة**، أدخل: 

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level =**
    
2. حدد معلمة **مستوى فرض الضرائب** في قائمة مصادر البيانات.
3. حدد **إضافة مصدر البيانات**.
4. في حقل **المعادلة**، أنجز التعبير كما يلي:  

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**

5. حدد **حفظ**.

    ![معلومات حقل مصدر البيانات.](media/er-calculated-field-type-07.png)

6. أغلق صفحة **مصمم المعادلة**.

### <a name="finish-adding-a-new-calculated-field"></a>إنهاء إضافة حقل محسوب جديد

- حدد **موافق**.

في صفحة **مصمم المعادلة**، يحتاج حقل **المستويات** المحسوب المكوّن ذو معلمات إلى وسيطة **سلسلة**.

![قائمة موسعة بمستويات الحقول المحسوبة.](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a>استخدام الحقل المحسوب المكون لربط عناصر التنسيق

1. حدد **Model.Data2.Levels** لتحديد الحقل المحسوب الذي تم تكوينه.
2. حدد عنصر التنسيق **Statement.Taxation.Regular**.
3. حدد **ربط**.
4. حدد **نعم** لتأكيد استبدال مصدر البيانات المستخدم حاليًا، **المستوى1**، بمصدر البيانات الجديد، **المستويات**، في كافة عناصر التنسيق المتداخلة لعنصر التنسيق المحدد.

    تم إنشاء الربط المطبق كاستدعاء للحقل المحسوب ذي معلمات. بشكل افتراضي، يتم استخدام اسم عنصر التنسيق المنضم كوسيطة للحقل المحسوب ذي معلمات تحت الشروط التالية:

      - يتم تكوين الحقل المحسوب لاستخدام معلمة واحدة.
      - يتم تعريف نوع بيانات هذه المعلمة **كسلسلة**.

    عندما يكون اسم عنصر التنسيق المنضم فارغًا، يتم استخدام اسم مصدر البيانات الخاص بهذا العنصر في الربط المطبق.

5. حدد عنصر التنسيق **Statement.Taxation.Reduced**.
6. حدد **ربط**.
7. حدد **نعم** لتأكيد استبدال مصدر البيانات المستخدم حاليًا، **المستوى2**، بمصدر البيانات الجديد، **المستويات**، في كافة عناصر التنسيق المتداخلة لعنصر التنسيق المحدد.
8. حدد عنصر التنسيق **Statement.Taxation.None**.
9. حدد **ربط**.
10. حدد **نعم** لتأكيد استبدال مصدر البيانات المستخدم حاليًا، **المستوى3**، بمصدر البيانات الجديد، **المستويات**، في كافة عناصر التنسيق المتداخلة لعنصر التنسيق المحدد.

   عند تعيين وسيطة الحقل المحسوب ذي المعلمات لعنصر XML الذي يمثل مستوى فرض الضرائب (على سبيل المثال **‎Model.Data2.Levels("Reduced")** كقيمة نصية)، لا تحتاج إلى القيام بنفس الإجراءات لسمات XML المتداخلة — سترث الارتباطات الخاصة بها تلقائيًا قيمة الوسيطة المعرفة في المستوى الأصل (**Model.Data2.Levels.aggregated.Base**، وليس **Model.Data2.Levels("Reduced").aggregated.Base**).

الاستدعاءات المتكررة لأي حقل محسوب ذي معلمات غير معتمدة.

يمكنك تحديد **تحرير المعادلة**، وتغيير الوسيطة المطبقة بشكل افتراضي للحقل المحسوب ذي المعلمات في الربط المحدد. إذا كانت هذه الوسيطة مفقودة، فقد تتسبب في حدوث أخطاء في وقت التشغيل — يتم إعلام المستخدمين بمثل هذا الموقف عند التحقق من صحة التنسيق الحالي.

![الإعلام عن تحذير التحقق من الصحة.](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a>تكوين حقل محسوب ذي معلمات لإرجاع سجل
عندما يقوم حقل محسوب ذو معلمات بإرجاع سجل، تحتاج إلى دعم ربط الحقول الفردية لهذا السجل بعناصر التنسيق. في مثل هذه الحالات لن يكون هناك ربط أصلي يحتوي على قيمة وسيطة لاستدعاء حقل محسوب ذي معلمات — يجب تعريف هذه القيمة في ربط حقل سجل واحد.

### <a name="start-adding-a-new-calculated-field"></a>بدء إضافة حقل محسوب جديد

1. حدد عنصر **Model.Data2**.
2. حدد **إضافة**.
3. حدد **الوظائف\\حقل محسوب**.
4. في حقل **الاسم**، أدخل **‏‫LevelRecord‬**.
5. حدد **تحرير المعادلة**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>تحديد معلمة لإضافة حقل محسوب

1. حدد **معلمات**.
2. حدد **جديد**.
3. في حقل **الاسم**، أدخل **مستوى فرض الضرائب**.
4. في حقل **النوع**، حدد **سلسلة**.
5. حدد **موافق**.

### <a name="define-an-expression-for-adding-a-calculated-field"></a>تحديد تعبير لإضافة حقل محسوب

1. في حقل **المعادلة**، أدخل ما يلي:  
    
    **FIRSTORNULL(\@.Levels(**

2. حدد المعلمة **مستوى فرض الضرائب**.
3. حدد **إضافة مصدر البيانات**.
4. في حقل **المعادلة**، قم بإلحاق **'مستوى فرض الضرائب'))** بما أدخلته في الخطوة 1 لإنهاء التعبير إلى:  
    
    **FIRSTORNULL(\@.Levels('Taxation Level'))**

5. حدد **حفظ**.
6. أغلق صفحة **مصمم المعادلة**.

### <a name="finish-adding-a-new-calculated-field"></a>إنهاء إضافة حقل محسوب جديد

-   حدد **موافق**.

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a>استخدام الحقل المحسوب المكون لربط عناصر التنسيق

1. قم بتوسيع **Model.Data2.LevelRecord** لتحديد الحقل المحسوب الذي تم تكوينه.
2. قم بتوسيع الحاوية **Model.Data2.LevelRecord.aggregated** للحقل المحسوب الذي تم تكوينه.
3. حدد الحقل **Model.Data2.LevelRecord.aggregated.Base**.
4. حدد عنصر التنسيق **Statement.Taxation.None**.
5. حدد **إلغاء الربط**.
6. حدد عنصر التنسيق **Statement.Taxation.None.Base**.
7. حدد **ربط**.
8. حدد **تحرير المعادلة**.
9. قم بتغيير التعبير إلى **Model.Data2.LevelRecord("None").aggregated.Base**.

![التعبير المحدّث.](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a>إزالة الحقول المحسوبة غير المستخدمة

1. حدد **Model.Data2.Level1**.
2. حدد **حذف**.
3. حدد **Model.Data2.Level2**.
4. حدد **حذف**.
5. حدد **Model.Data2.Level3**.
6. حدد **حذف**.
7. حدد **حفظ**.

  > [!NOTE]
  > لقد قمت بإعادة استخدام نفس الحقل المحسوب **Model.Data2.Levels** عدة مرات في روابط التنسيق. إن استخدام حقل محسوب واحد والاحتفاظ به أسهل بكثير من تنفيذ ذلك لعدة حقول متشابهة.

8. أغلق صفحة **مصمم المعادلة**.

## <a name="complete-adjusted-version-of-a-derived-format"></a>إكمال الإصدار المعدل لتنسيق مشتق

1. في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.
2. حدد **مكتمل**.

## <a name="export-completed-version-of-a-derived-format"></a>تصدير الإصدار المكتمل لتنسيق مشتق

1. حدد التنسيق **تنسيق للتعرف على الاستدعاءات ذات معلمات (مخصص)** في شجره التكوينات.
2. في علامة التبويب السريعة **الإصدارات**، حدد الإصدار المكتمل 1.1.1.
3. حدد **تبادل**.
4. حدد **تصدير كملف XML**.
5. قم بتخزين التكوين الذي تم تنزيله محليًا، بتنسيق XML.

## <a name="test-er-formats"></a>اختبار تنسيقات التقارير الإلكترونية 
يمكنك تشغيل تنسيقات التقارير الإلكترونية الأولية والمحسنة للتأكد من أن الحقول المحسوبة ذات معلمات والتي تم تكوينها تعمل بشكل صحيح.

### <a name="import-er-configurations"></a>استيراد تكوينات التقارير الإلكترونية
يمكنك استيراد التكوينات التي تمت مراجعتها من RCS باستخدام مستودع التقارير الإلكترونية الخاص بالنوع **RCS**. إذا كنت قمت بالفعل بالخطوات المذكورة في المقالة [استيراد تكوينات التقارير الإلكترونية (ER) من Regulatory Configuration Services‏ (RCS)](rcs-download-configurations.md)، فاستخدم مستودع التقارير الإلكترونية المكوّن لاستيراد التكوينات التي تمت مناقشتها سابقًا في هذه المقالة لبيئتك. وإلا، فاتبع هذه الخطوات:

1. حدد الشركة **DEMF** وفي لوحة المعلومات الافتراضية، حدد **التقارير الإلكترونية**.
2. حدد **تكوينات إعداد التقارير‬**.
3. قم باستيراد التكوينات من مركز التنزيل لـ Microsoft بالتسلسل التالي: نموذج البيانات، وتعيين النموذج، والتنسيق. أكمل الخطوات التالية لكل تكوين خاص بإعداد التقارير الإلكترونية:

    1. حدد **تبادل**.
    2. حدد **تحميل من ملف XML**.
    3. حدد **استعراض** لتحديد تكوين التقارير الإلكترونية المطلوب بالتنسيق XML.
    4. حدد **موافق**.

4. استيراد ما تم تصديره من RCS الإصدار المكتمل 1.1.1 من التنسيق **تنسيق للتعرف على الاستدعاءات ذات معلمات (مخصص)**:

    1. حدد **تبادل**.
    2. حدد **تحميل من ملف XML**.
    3. حدد **استعراض** لتحديد ملف التنسيق المخزن محليًا **تنسيق للتعرف على الاستدعاءات ذات معلمات (مخصص)** بتنسيق XML.
    4. حدد **موافق**.

### <a name="run-er-formats"></a>تشغيل تنسيقات التقارير الإلكترونية

1. في شجرة التكوين، قم بتوسيع محتوى العنصر **نموذج للتعرف على الاستدعاءات ذات معلمات‬**.
2. حدد **تنسيق للتعرف على الاستدعاءات ذات معلمات**.
3. حدد **تشغيل** في الشريط العلوي.
4. احفظ المخرجات التي تم إنشاؤها محليًا.
5. حدد الصنف **تنسيق للتعرف على الاستدعاءات ذات معلمات (مخصص)**.
6. حدد **تشغيل** في الشريط العلوي.
7. احفظ المخرجات التي تم إنشاؤها محليًا. 
8. قارن بين محتويات المخرجات التي تم إنشاؤها.

## <a name="additional-resources"></a>الموارد الإضافية

- [مصمم المعادلات في التقارير الإلكترونية](general-electronic-reporting-formula-designer.md)
- [تحسين أداء حلول التقارير الإلكتروني عن طريق إضافة مصادر بيانات الحقول المحسوبة ذات معلمات](er-calculated-field-ds-performance.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

