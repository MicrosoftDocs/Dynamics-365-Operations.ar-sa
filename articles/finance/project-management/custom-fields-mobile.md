---
title: تنفيذ الحقول المخصصة لتطبيق Microsoft Dynamics 365 Project Timesheet للأجهزة المحمولة على iOS وAndroid
description: يوفر هذا الموضوع أنماطًا شائعة لاستخدام الامتدادات لتنفيذ الحقول المخصصة.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 48854c15e429d51dcf30ea804eb636dee7965443
ms.sourcegitcommit: a356299be9a593990d9948b3a6b754bd058a5b3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/21/2020
ms.locfileid: "3080762"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>تنفيذ الحقول المخصصة لتطبيق Microsoft Dynamics 365 Project Timesheet للأجهزة المحمولة على iOS وAndroid

[!include [banner](../includes/banner.md)]

يوفر هذا الموضوع أنماطًا شائعة لاستخدام الامتدادات لتنفيذ الحقول المخصصة. يتم تناول الموضوعات التالية:

- أنواع البيانات المختلفة التي يدعمها إطار الحقل المخصص
- كيفية إظهار الحقول القابلة للقراءة فقط أو القابلة للتحرير على إدخالات الجدول الزمني ، وحفظ القيم التي يوفرها المستخدم مرة أخرى إلى قاعدة البيانات
- كيفية إظهار الحقول للقراءة فقط في رأس الجدول الزمني
- كيفية دمج منطق عمل مخصص آخر لإدخال القيم الافتراضية في الحقول والقيام بالتحقق من الصحة الإضافي

## <a name="audience"></a>الجمهور

تم إعداد هذا الموضوع للمطورين الذين يقومون بدمج الحقول المخصصة في تطبيق Microsoft Dynamics 365 Project Timesheet للأجهزة المحمولة المتوفر لـ Apple iOS وAndroid Google. الافتراض هو أن القراء على دراية بتطوير X ++ ووظائف الجدول الزمني للمشروع.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>عقد البيانات – فئة TSTimesheetCustomField X++

إن فئة **TSTimesheetCustomField** هي فئة عقد بيانات X ++ التي تمثل معلومات حول حقل مخصص لوظيفة الجدول الزمني. يتم تمرير قوائم كائنات الحقل المخصص في كلٍّ من عقد بيانات TSTimesheetDetails وعقد بيانات TSTimesheetEntry لإظهار الحقول المخصصة في تطبيق الأجهزة المحمولة.

- **TSTimesheetDetails** - عقد رأس الجدول الزمني.
- **TSTimesheetEntry** - عقد حركة الجدول الزمني. تشكل مجموعات من هذه الكائنات التي لها نفس معلومات المشروع وقيمة **timesheetLineRecId** بندًا.

### <a name="fieldbasetype-types"></a>fieldBaseType (الأنواع)

تحدد خاصية **FieldBaseType** في كائن **TsTimesheetCustom** نوع الحقل الذي يظهر في التطبيق. قيم **الأنواع** التالية التي يتم دعمها.

| قيمة الأنواع | ‏‏النوع              | ملاحظات |
|-------------|-------------------|-------|
| 0           | السلسلة (والتعداد) | يظهر الحقل كحقل نص. |
| 1           | عدد صحيح           | تظهر القيمة كرقم بدون المنازل العشرية. |
| 2           | حقيقي              | تظهر القيمة كرقم يشتمل على المنازل العشرية.<p>لإظهار القيمة الفعلية كعملة في التطبيق، استخدم خاصية **fieldExtenededType**. يمكنك استخدام خاصية **numberOfDecimals** لتعيين رقم المنازل العشرية المبين.</p> |
| 3           | التاريخ              | يتم تحديد تنسيقات التاريخ حسب إعداد **التاريخ، والأوقات، وتنسيق الأرقام** الخاص بالمستخدم والمحدد ضمن **تفضيلات البلد/المنطقة واللغة‬** في **خيارات المستخدم**. |
| 4           | منطقي           | |
| 15          | GUID              | |
| 16          | Int64             | |

- إذا لم يتم توفير خاصية **stringOptions** في كائن **TSTimesheetCustomField**، يتم توفير حقل نص فارغ للمستخدم.

    يمكن استخدام خاصية **stringLength** لتعيين الحد الأقصى لطول السلسلة التي يمكن للمستخدمين إدخالها.

- إذا تم توفير خاصية **stringOptions** في كائن **TSTimesheetCustomField**، تكون عناصر القائمة هذه هي القيم الوحيدة التي يمكن للمستخدمين تحديدها باستخدام أزرار الخيارات (أزرار الاختيار).

    في هذه الحالة ، يمكن أن يعمل حقل السلسلة كقيمة تعداد لغرض إدخال المستخدم. لحفظ القيمة في قاعدة البيانات كتعداد، قم يدويًا بتعيين قيمة السلسلة مرة أخرى إلى قيمة التعداد قبل حفظها في قاعدة البيانات باستخدام سلسلة الأوامر (راجع قسم "استخدام سلسلة الأوامر في فئة TSTimesheetEntryService لحفظ إدخال جدول زمني من التطبيق مرة أخرى إلى قسم قاعدة البيانات" في وقت لاحق في هذا الموضوع للحصول على مثال).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

يمكنك استخدام هذه الخاصية لتنسيق القيم الحقيقية كعملة. يكون هذا النهج قابلاً للتطبيق فقط عندما تكون قيمة **fieldBaseType** هي **حقيقية**.

- **TSCustomFieldExtendedType:None** – لا يتم استخدام أي تنسيق.
- **TSCustomFieldExtendedType::Currency** – تنسيق القيمة كعملة.

    عندما يكون تنسيق العملة نشطًا يمكن استخدام حقل **stringValue** لتمرير كود العملة الذي يجب أن يظهر في التطبيق. القيمة هي قيمة للقراءة فقط.

    يحتوي حقل **realValue** على المبلغ النقدي الذي يجب حفظه إلى قاعده البيانات.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

يمكنك استخدام هذه الخاصية لتحديد المكان الذي يجب أن يظهر فيه الحقل المخصص في التطبيق.

- **TSCustomFieldSection::Header** – سيظهر هذا الحقل في قسم **عرض مزيد من التفاصيل** في التطبيق. هذه الحقول هي دائما للقراءة فقط.
- سطر **TSCustomFieldSection::** – سيظهر الحقل بعد كل حقول الأسطر الخارجية في إدخالات الجدول الزمني. يمكن أن تكون هذه الحقول قابلة للتحرير أو للقراءة فقط.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

تحدد هذه الخاصية الحقل عندما يتم حفظ القيم التي يوفرها التطبيق مرة أخرى إلى قاعدة البيانات.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

تحدد هذه الخاصية الحقل عندما يتم حفظ القيم التي يوفرها التطبيق مرة أخرى إلى قاعدة البيانات.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

قم بتعيين هذه الخاصية إلى **نعم** لتحديد أن الحقل الموجود في قسم إدخال الجدول الزمني يجب أن يكون قابلاً للتحرير من قِبل المستخدمين. قم بتعيين الخاصية إلى **لا** لجعل الحقل للقراءة فقط.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

قم بتعيين هذه الخاصية إلى **نعم** لتحديد أن الحقل الموجود في قسم إدخال الجدول الزمني يجب أن يكون إلزاميًا.

### <a name="label-str"></a>التسمية (السلسلة)

تحدد هذه الخاصية التسمية التي تظهر بجانب الحقل في التطبيق.

### <a name="stringoptions-list-of-strings"></a>stringOptions (قائمة السلاسل)

لا تنطبق هذه الخاصية إلا في حالة تعيين **fieldBaseType** إلى **سلسلة**. في حالة تعيين **stringOptions**، يتم تحديد قيم السلسلة المتاحة للتحديد عبر أزرار الخيارات (أزرار الاختيار) بواسطة السلاسل الموجودة في القائمة. إذا لم يتم توفير سلاسل ، يُسمح بإدخال نص حر في حقل السلسلة (راجع قسم "استخدام سلسلة الأوامر في فئة TSTimesheetEntryService لحفظ إدخال الجدول الزمني من التطبيق مرة أخرى إلى قاعدة البيانات" لاحقًا في هذا الموضوع للحصول على مثال).

### <a name="stringlength-int"></a>stringLength (int)

تحدد هذه الخاصية الحد الأقصى لطول حقل السلسلة. لا تنطبق هذه الخاصية إلا في حالة تعيين **fieldBaseType** إلى **سلسلة**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

تحدد هذه الخاصية عدد المنازل العشرية التي يتم عرضها لحقل حقيقي. لا تنطبق هذه الخاصية إلا في حالة تعيين **fieldBaseType** إلى **حقيقية**.

### <a name="ordersequence-int"></a>orderSequence (int)

تتحكم هذه الخاصية في الترتيب الذي تظهر به الحقول المخصصة في التطبيق عند تحديد أكثر من حقل مخصص. يتم عرض الحقول التي تحتوي على أرقام أقل أولاً.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

بالنسبة للحقول من نوع **Boolean**، تتجاوز هذه الخاصية القيمة المنطقية للحقل بين الخادم والتطبيق.

### <a name="guidvalue-guid"></a>guidValue (guid)

بالنسبة للحقول من نوع **GUID**، تتجاوز هذه الخاصية قيمة المعرف الفريد العالمي (GUID) للحقل بين الخادم والتطبيق.

### <a name="int64value-int64"></a>int64Value (int64)

بالنسبة للحقول من نوع **Int64**، تتجاوز هذه الخاصية قيمة Int64 للحقل بين الخادم والتطبيق.

### <a name="intvalue-int"></a>intValue (int)

بالنسبة للحقول من نوع **Int**، تتجاوز هذه الخاصية قيمة Int للحقل بين الخادم والتطبيق.

### <a name="realvalue-real"></a>realValue (real)

بالنسبة للحقول من نوع **Real**، تتجاوز هذه الخاصية القيمة الحقيقية للحقل بين الخادم والتطبيق.

### <a name="stringvalue-str"></a>stringValue (السلسلة)

بالنسبة للحقول من نوع **String**، تتجاوز هذه الخاصية قيمة السلسلة للحقل بين الخادم والتطبيق. وتُستخدم أيضًا في الحقول من نوع **Real** والتي تم تنسيقها كعملة. بالنسبة لتلك الحقول، يتم استخدام الخاصية لتمرير رمز العملة إلى التطبيق.

### <a name="datevalue-date"></a>dateValue (التاريخ)

بالنسبة للحقول من نوع **Date**، تمرر هذه الخاصية قيمة التاريخ للحقل بين الخادم والتطبيق.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>إظهار وحفظ حقل مخصص في قسم إدخال الجدول الزمني

يوجد أدناه لقطة شاشة من تطبيق الجوال لإنشاء إدخال الجدول الزمني. إنها تعرض الحقول الخارجية والحقل المخصص في قسم "إدخال الوقت" المسمى "سلسلة الاختبار" مع تعيين قيمة التعداد لـ "الخيار الثاني" بالفعل.

![اختبار حقل السلسلة المخصص في التطبيق](media/timesheet-entry.jpg)



يوجد أدناه لقطة شاشة من تطبيق الجوال للمستخدم يختار أحد خيارات التعداد المتاحة للحقل المخصص "سلسلة الاختبار".  الخياران هما "الخيار الأول" و"الخيار الثاني" ويظهران كأزرار اختيار. الخيار الثاني محدد حاليًا.

![أزرار الخيارات (أزرار الاختيار) للحقل المخصص لسلسلة الاختبار](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>توسيع جدول TSTimesheetLine بحيث يحتوي على حقل مخصص

في السيناريوهات النموذجية ، من المحتمل أن يتم حفظ البيانات الخاصة بحقل مخصص في قسم إدخال الجدول الزمني في جدول TSTimesheetLine. ومع ذلك، يمكن استخدام الجداول الأخرى إذا كان يمكن استرداد البيانات بناءً على سجل TSTimesheetTrans الذي يتم توفيره، أو إذا لم يكن لديه سياق سجل محدد (على سبيل المثال، إذا تم تعيين الحقل للقراءة فقط في معلمات المشروع) .

لاحظ أن الحقول المخصصة لا يجب أن يكون لها أي سجلات قاعدة بيانات احتياطية. يمكن إنشاؤها ديناميكيًا استنادًا إلى منطق X ++. يمكن أن يكون هذا النهج مفيدًا في سيناريوهات القراءة فقط (راجع قسم "استخدام سلسلة الأوامر في فئة TSTimesheetDetails، أسلوب buildCustomFieldListForHeader لملء تفاصيل الجدول الزمني" للحصول على مثال لقيم الحقل المخصص التي تم إنشاؤها ديناميكيًا.)

فيما يلي لقطة شاشة من Visual Studio لشجرة مكونات البرنامج. يعرض امتدادًا لجدول TSTimesheetLine مع إضافة حقل TestLineString كحقل مخصص.

![سلسلة السطر](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>استخدم سلسلة الأوامر في أسلوب buildCustomFieldList للفئة TSTimesheetSettings لإظهار حقل في قسم إدخال الجدول الزمني

يتحكم هذا الكود في إعدادات العرض للحقل في التطبيق. على سبيل المثال ، يتحكم في نوع الحقل والتسمية وما إذا كان الحقل إلزاميًا وفي القسم الذي يظهر فيه الحقل.

يوضح المثال التالي حقل سلسلة في إدخالات الوقت. يحتوي هذا الحقل على خيارين، **الخيار الأول** و**الخيار الثاني**، المتوفرين من خلال أزرار الخيار (أزرار الاختيار). والجقل الموجود في التطبيق مرتبط بحقل **TestLineString** الذي تمت إضافته إلى جدول TSTimesheetLine.

تجدر الإشارة إلى استخدام طريقة **TSTimesheetCustomField::newFromMetatdata()** لتبسيط تهيئة خصائص الحقول المخصصة: **fieldBaseType**، و**tableName**، و**fieldname**، و**label**، و**isEditable**، و**isMandatory**، و**stringLength**، و**numberOfDecimals**. يمكنك أيضًا ضبط هذه المعلمات يدويًا ، حسب رغبتك.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>استخدم سلسلة الأوامر في طريقة buildCustomFieldListForEntry للفئة TSTimesheetEntry لإدخال القيم في إدخال الجدول الزمني

يتم استخدام أسلوب **buildCustomFieldListForEntry** لإدخال القيم في أسطر الجداول الزمنية المحفوظة في تطبيق الأجهزه المحمولة. يأخذ سجل TSTimesheetTrans كمعلمة. يمكن استخدام الحقول من هذا السجل لملء قيمة الحقل المخصص في التطبيق.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>استخدم سلسلة الأوامر في فئة TSTimesheetEntryService لحفظ إدخال الجدول الزمني من التطبيق مرة أخرى إلى قاعدة البيانات

لحفظ حقل مخصص مرة أخرى إلى قاعدة البيانات في استخدام نموذجي ، يجب توسيع طرق متعددة:

- يتم استخدام أسلوب **timesheetLineNeedsUpdating** لتحديد ما إذا كان قد تم تغيير سجل السطر من قِبل المستخدم في التطبيق ويجب حفظه في قاعدة البيانات. إذا لم يكن الأداء مصدر قلق ، فيمكن تبسيط هذه الطريقة بحيث تعرض دائمًا **true**.
- يمكن توسيع الأسلوبين **populateTimesheetLineFromEntryDuringCreate** و**populateTimesheetLineFromEntryDuringUpdate** بحيث يقومان بإدخال قيم في سجل قاعدة بيانات TSTimesheetLine من سجل عقد بيانات TSTimesheetEntry الذي يتم توفيره. في المثال التالي ، لاحظ كيفية إجراء التعيين بين حقل قاعدة البيانات وحقل الإدخال يدويًا عبر رمز X ++.
- يمكن أيضًا توسيع أسلوب **populateTimesheetWeekFromEntry** إذا كان الحقل المخصص الذي تم تعيينه إلى كائن **TSTimesheetEntry** يجب إعادة كتابته لجدول قاعدة البيانات TSTimesheetLineweek.

> [!NOTE]
> يقوم المثال التالي بحفظ قيمة **firstOption** أو **secondOption** الذي يقوم المستخدم بتحديده لقاعدة البيانات كقيمة سلسلة بسيطة. إذا كان حقل قاعدة البيانات هو حقل من نوع **التعداد**، فإنه يمكن تعيين هذه القيم يدويًا إلى قيمه تعداد ثم حفظها إلى حقل تعداد في جدول قاعده البيانات.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>إظهار وحفظ حقل مخصص في قسم رأس الجدول الزمني

يوجد أدناه لقطة شاشة من تطبيق الجوال لمستخدم يشاهد جدولًا زمنيًا. تم تحديد زر "مزيد من المعلومات" في الزاوية العلوية اليمنى لإظهار خيار "عرض مزيد من التفاصيل".  

![أمر عرض المزيد من التفاصيل](media/show-more.png)

يوجد أدناه لقطة شاشة من تطبيق الجوال تعرض قسم "المزيد" في جدول زمني. تمت إضافة حقل مخصص يسمى "معدل استخدام الجدول الزمني هذا (حقل مخصص محسوب)" إلى قسم رأس الجدول الزمني. يتم تعيين قيمة للقراءة فقط "0.667" في الحقل المخصص.

![قسم المزيد](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>توسيع جدول TSTimesheetTable بحيث يحتوي على حقل مخصص

في السيناريوهات النموذجية ، من المحتمل أن يتم سحب البيانات الخاصة بحقل مخصص في قسم الرأس من جدول TSTimesheetHeader. ومع ذلك ، يمكن استخدام الجداول الأخرى إذا كان يمكن استرداد البيانات استنادًا إلى سجل TSTimesheetTable الذي تم توفيره ، أو إذا لم يكن لديه سياق سجل محدد (على سبيل المثال ، إذا تم تعيين الحقل للقراءة فقط في معلمات المشروع).

لاحظ أن الحقول المخصصة لا يجب أن يكون لها أي سجلات قاعدة بيانات احتياطية. يمكن إنشاؤها ديناميكيًا استنادًا إلى منطق X ++. يوضح المثال التالي هذا النهج.

تكون الحقول الموجودة في قسم الرأس دائمًا للقراءة فقط في التطبيق.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>استخدم سلسلة الأوامر في أسلوب buildCustomFieldList للفئة TSTimesheetSettings لإظهار حقل في قسم الرأس

يتحكم هذا الكود في إعدادات العرض للحقل في التطبيق. على سبيل المثال ، يتحكم في نوع الحقل والتسمية وما إذا كان الحقل إلزاميًا وفي القسم الذي يظهر فيه الحقل.

يوضح المثال التالي قيمة محسوبة في قسم الرأس في التطبيق.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>استخدم سلسلة الأوامر في أسلوب buildCustomFieldListForHeader للفئة TSTimesheetDetails لملء تفاصيل الجدول الزمني

يتم استخدام أسلوب **buildCustomFieldListForHeader** لملء تفاصيل رأس الجدول الزمني في تطبيق الجوال. يأخذ سجل TSTimesheetTable كمعلمة. يمكن استخدام الحقول من هذا السجل لملء قيمة الحقل المخصص في التطبيق. المثال التالي لا يقرأ أي قيم من قاعدة البيانات. بدلاً من ذلك، يستخدم منطق X ++ لإنشاء قيمة محسوبة تظهر في التطبيق.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>فرص إمكانية التكوين/إمكانية التوسيع الأخرى

### <a name="adding-additional-validation-for-the-app"></a>إضافة تحقق إضافي للتطبيق

المنطق الحالي لوظيفة الجدول الزمني على مستوى قاعدة البيانات سيظل يعمل كما هو متوقع. لمقاطعة إتمام حفظ أو إرسال العمليات وإظهار رسالة خطأ محددة، يمكنك إضافة **طرح خطأ ("رسالة إلى المستخدم")** إلى الكود عبر سلسلة من تمديد الأوامر. فيما يلي ثلاثة أمثلة للطرق القابلة للتوسعة المفيدة:

- إذا قام **validateWrite** في جدول TSTimesheetLine بإرجاع **false** أثناء عمليه حفظ لسطر جدول زمني، تظهر رسالة خطأ في تطبيق الأجهزه المحمولة.
- إذا قام **validateSubmit** في جدول TSTimesheetTable بإرجاع **false** أثناء إرسال الجدول الزمني في التطبيق، يتم عرض رسالة خطأ للمستخدم.
- المنطق الذي يعبئ الحقول (على سبيل المثال **خاصية السطر**) أثناء **إدخال** الأسلوب في جدول TSTimesheetLine سيظل يعمل.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>إخفاء الحقول الخارجية ووضع علامة عليها للقراءة فقط عبر التكوين

من معلمات المشروع ، يمكنك جعل الحقول الجاهزة للقراءة فقط أو مخفية في تطبيق الجوال. قم بتعيين الخيارات في قسم **الجداول الزمنية للأجهزة المحمولة** في علامة التبويب **الجدول الزمني** في صفحة **محددات إدارة المشاريع ومحاسبتها‬**.

![محددات المشروع](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>تغيير الأنشطة المتاحة للاختيار عبر التوسيعات

يتم ملء الأنشطة المتاحة للتحديد الخاص بأحد المشاريع من خلال أساليب **getActivitiesForProject()** and **getActivityQuery()** في فئة **TsTimesheetProjectService**. يمكنك استخدام سلسلة الأوامر لتغيير هذا السلوك لمطابقة سيناريو عملك للأنشطة المتاحة للاختيار لمشروع معين.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>إدخال فئة المشروع الافتراضية في إدخالات الجدول الزمني

يحدث إدخال فئة المشروع الافتراضية في إدخالات الجدول الزمني على ثلاثة مستويات. يمكنك استخدام سلسلة الأوامر لتوسيع السلوك في أي من هذه المستويات أو كلها لتحقيق السلوك المطلوب. يتم استخدام التدرج الهرمي التالي:

1. يحاول التطبيق وضع الفئة الافتراضية من مورد المشروع. يتم تعيين هذه الفئة الافتراضية في أسلوبي **getCurrentUserResource** و**getDelegatedResourcesForCurrentUser** في فئة **TSTimesheetSettingsService**.
2. إذا لم يتم توفير الفئة الافتراضية على مستوى مورد المشروع، فسيحاول التطبيق سحبها من نشاط المشروع. يتم تعيين هذه الفئة الافتراضية في أسلوب **getActivitiesForProject** في فئة **TSTimesheetProjectService**.
3. إذا لم يتم توفير الفئة الافتراضية على مستوى نشاط المشروع، فستكون الفئة الافتراضية مأخوذة من معلمات المشروع. يتم تعيين هذه الفئة الافتراضية في أسلوب **getProjectDetailsbyRule** في فئة **TSTimesheetProjectService**.
