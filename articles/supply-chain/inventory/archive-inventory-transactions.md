---
title: أرشفة حركات المخزون
description: يوضح هذا الموضوع كيفية أرشفة بيانات حركة المخزون للمساعدة في تحسين أداء النظام.
author: yufeihuang
ms.date: 05/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8b766d306f31fc531f33aa29e1f96048bbd90085
ms.sourcegitcommit: e18ea2458ae042b7d83f5102ed40140d1067301a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/10/2022
ms.locfileid: "8736050"
---
# <a name="archive-inventory-transactions"></a>أرشفة حركات المخزون

[!include [banner](../../includes/banner.md)]

بمرور الوقت، سيستمر جدول حركات المخزون (`InventTrans`) في النمو وزيادة الحجم واستهلاك مساحة قاعدة البيانات. وبالتالي، ستصبح الاستعلامات التي يتم إجراؤها على الجدول أبطأ تدريجياً. يصف هذا الموضوع كيف يمكنك استخدام ميزة *أرشيف حركات المخزون* لأرشفة البيانات حول حركات المخزون للمساعدة في تحسين أداء النظام.

> [!NOTE]
> يمكن أرشفة حركات المخزون التي تم تحديثها ماليًا فقط في فترة دفتر الأستاذ المُقفلة المحددة. ولكي تتم أرشفتها، ينبغي أن تكون لحركات المخزون الصادرة المحدثة ماليًا في حالة إصدار *مُباع*، وينبغي أن تكون حركات المخزون الواردة في حالة استلام *مشتراة*.

عند أرشفة حركات المخزون، يتم نقل جميع الحركات ذات الصلة إلى الجدول `InventTransArchive` . تتم أرشفة حركات إصدار المخزون وحركات استلام المخزون بشكل منفصل، استنادًا إلى مجموعة معرّف الصنف (`itemId`) ومعرف بُعد المخزون (`inventDimId`)، ويتم وضعها في الإصدار الملخص وحركات الاستلام الملخصة.

إذا احتوت مجموعة `itemId` و `inventDimId` على حركة استلام أو إصدار واحدة فقط، فلن تتم أرشفة الحركة.

## <a name="turn-on-the-feature-in-your-system"></a>تشغيل الميزة في النظام

إذا لم يتضمن نظامك الميزات الموضحة في هذا الموضوع بالفعل، فانتقل إلى [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)، وقم بتشغيل ميزة *أرشيف حركات المخزون*. لاحظ أن هذه الميزة لا يمكن تعطيلها بمجرد تمكينها.

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>الأشياء الواجب مراعاتها قبل أرشفة حركات المخزون

قبل أرشفة حركات المخزون، ينبغي مراعاة سيناريوهات الأعمال التالية، لأنها ستتأثر بالعملية:

- عند تدقيق حركات المخزون من المستندات ذات الصلة، مثل بنود أمر الشراء، سيتم عرضها على أنها مؤرشفة. لمراجعه الحركات المؤرشفة، ينبغي الانتقال إلى **إدارة المخزون\> المهام الدورية \> مسح \> أرشيف حركات المخزون**.
- لا يمكن إلغاء إقفال المخزون للفترات المؤرشفة. قبل أن تتمكن من إلغاء إقفال المخزون، ينبغي عليك عكس أرشيف حركة المخزون للفترة ذات الصلة.
- لا يمكن اجراء تحويل التكاليف القياسية‬ للفترات المؤرشفة. قبل أن تتمكن من إجراء تحويل التكاليف القياسية، يتعين عكس أرشيف حركة المخزون للفترة ذات الصلة.
- ستتأثر تقارير المخزون التي يتم الحصول عليها من حركات المخزون عند أرشفة حركات المخزون. تتضمن هذه التقارير تقرير تقادم المخزون وتقارير قيمة المخزون.
- قد تتأثر التنبؤ بالمخزون إذا تم تشغيله خلال الفترة الزمنية للفترات المؤرشفة.

## <a name="prerequisites"></a>المتطلبات الأساسية

يمكن أرشفة حركات المخزون فقط خلال الفترات التي يتم فيها استيفاء الشروط التالية:

- يتعين إقفال فترة دفتر الأستاذ.
- ينبغي تشغيل إقفال المخزون في أو بعد تاريخ الفترة الخاصة بالأرشيف.
- ينبغي أن تكون الفترة قبل عام واحد على الأقل من تاريخ فترة بدء الأرشيف.
- يتعين ألا يكون هناك أي عمليات إعادة حساب المخزون الحالية.

## <a name="archive-inventory-transactions"></a>أرشفة حركات المخزون

لأرشفة حركات المخزون، اتبع هذه الخطوات.

1. الانتقال إلى **إدارة المخزون** \> **المهام الدورية** \> **مسح** \> **أرشيف حركات المخزون**.

    تظهر صفحة **أرشيف حركات المخزون** وتعرض قائمة بسجلات العمليات المؤرشفة.

    ![صفحة أرشيف حركات المخزون.](media/archive-inventory-empty.png "صفحة أرشيف حركات المخزون")

1. في جزء الاجراء، حدد **أرشيف حركات المخزون** لإنشاء أرشيف حركات المخزون.
1. في مربع الحوار **أرشيف حركات المخزون** ، في علامة التبويب السريعة **المعلمات** ، عيّن الحقول التالية:

    - **من تاريخ إقفال فترة دفتر الاستاذ** - حدد تاريخ أول حركة لتضمينها في الأرشيف.
    - **إلى تاريخ إقفال فترة دفتر الاستاذ** - حدد تاريخ أخر حركة لتضمينها في الأرشيف.

    ![مربع حوار أرشيف حركات المخزون.](media/archive-inventory-dates.png "مربع حوار أرشيف حركات المخزون")

    > [!NOTE]
    > ستتوفر فقط الفترات التي تلبي [المتطلبات الأساسية](#prerequisites) للتحديد.

1. في علامة التبويب السريعة **تشغيل في الخلفية** ، قم بإعداد تفاصيل معالجة الدُفعات كما تريد. اتبع الخطوات المعتادة للوظائف الدفعية في Microsoft Dynamics 365 Supply Chain Management.
1. حدد **موافق**.
1. تظهر رسالة تُطالبك بتأكيد الرغبة في المتابعة. أقرا الرسالة بعناية، ثم حدد **نعم** إذا كنت ترغب في المتابعة.

    تتلقى رسالة توضح أنه تمت إضافة وظيفة أرشيف حركات المخزون إلى قائمه انتظار الدُفعة. ستبدا الوظيفة الآن في أرشفة حركات المخزون من الفترة المحددة.

## <a name="view-archived-inventory-transactions"></a>عرض حركات المخزون المؤرشفة

تعرض صفحة **أرشيف حركات المخزون** كامل محفوظات الأرشفة الخاصة بك. يعرض كل صف في الشبكة معلومات مثل تاريخ إنشاء الأرشيف والمستخدم الذي أنشأه وحالته.

![أرشفة المحفوظات في صفحة أرشيف حركات المخزون.](media/archive-inventory-full.png "أرشفة المحفوظات في صفحة أرشيف حركات المخزون")

في القائمة المنسدلة أعلى الصفحة، حدد إحدى القيم التالية لتصفية الأرشيفات التي تظهر في الشبكة:

- **نشط** -عرض الأرشيفات النشطة فقط، وليس الأرشيفات المعكوسة.
- **الكل** – عرض كافة الأرشيفات، النشطة والمعكوسة.

لكل أرشيف في الشبكة، يتم توفير المعلومات التالية:

- **نشط** – تشير علامة الاختيار إلى أن الأرشيف نشط.
- **من تاريخ** – تاريخ أقدم حركة يمكن تضمينها في الأرشيف.
- **إلى تاريخ** – تاريخ أخر حركة يمكن تضمينها في الأرشيف.
- **مُجدول بواسطة** - حساب المستخدم الذي قام بإنشاء الأرشيف.
- **تم التنفيذ** - تاريخ إنشاء الأرشيف.
- **عكسي** – تشير علامة الاختيار إلى أن الأرشيف قد تم عكسه.
- **إيقاف التحديث الحالي** – تشير علامة الاختيار إلى أن الأرشيف قيد التقدم، ولكن تم إيقافه مؤقتًا.
- **الحالة** – حالة معالجة الأرشيف. وتكون القيم المحتملة هي *الانتظار*، و *قيد التقدم*، و *منتهي*.

يوفر شريط الأدوات أعلى الشبكة الأزرار التالية التي يمكنك استخدامها للعمل مع أرشيف محدد:

- **الحركات المؤرشفة** – عرض التفاصيل الكاملة للأرشيف المحدد. تعرض صفحة **الحركات المؤرشفة** التي تعرض كافة الحركات في الأرشيف.

    ![صفحة الحركات المؤرشفة.](media/archive-inventory-transactions.png "صفحة الحركات المؤرشفة")

    لعرض مزيد من المعلومات حول حركة معينة في صفحة **الحركات المؤرشفة** ، حددها في الشبكة، ثم في جزء الإجراءات، حدد **تفاصيل الحركة المؤرشفة**. تعرض صفحة **تفاصيل الحركة المؤرشفة** معلومات مثل ترحيل دفتر الأستاذ ومراجع دفتر الأستاذ الفرعي ذات الصلة والأبعاد المالية.

- **إيقاف الأرشفة** - إيقاف مؤقت للأرشيف المحدد الذي تتم معالجته حاليًا. لا يسري الإيقاف المؤقت إلا بعد إنشاء مهمة الأرشفة. لذلك، قد يكون هناك تأخير قصير قبل تفعيل الإيقاف المؤقت. في حالة إيقاف الأرشيف بشكل مؤقت، تظهر علامة اختيار في الحقل **إيقاف التحديث الحالي** .
- **استئناف الأرشفة** - استئناف المعالجة لأرشيف محدد متوقف مؤقتًا حاليًا.
- **عكسي** - عكس الأرشيف المحدد. لا يمكنك عكس أرشيف إلا إذا تم تعيين حقل **الحالة** على *مُنتهي*. إذا تم عكس أحد الأرشيفات، فستظهر علامة اختيار في الحقل **عكسي** الخاص به.

## <a name="extend-your-code-to-support-custom-fields"></a>توسيع التعليمات البرمجية لدعم الحقول المخصصة

إذا كان الجدول `InventTrans` يحتوي على واحد أو أكثر من الحقول المخصصة، فقد تحتاج إلى توسيع التعليمات البرمجية لدعمها، بالاستناد إلى كيفية تسميتها.

- إذا كانت الحقول المخصصة من الجدول `InventTrans` بأسماء الحقول نفسها كما في الجدول `InventtransArchive`، فهذا يعني أنها معينة 1:1. وبالتالي، يمكنك فقط وضع الحقول المخصصة في مجموعة حقول `InventoryArchiveFields` التابعة للجدول `inventTrans`.
- إذا لم تتطابق أسماء الحقول المخصصة في الجدول `InventTrans` مع أسماء الحقول في الجدول `InventtransArchive`، فستحتاج إلى إضافة التعليمات البرمجية لتعيينها. على سبيل المثال، إذا كان لديك حقل نظام يسمى `InventTrans.CreatedDateTime`، فعليك إنشاء حقل في الجدول `InventTransArchive` باسم مختلف (مثل `InventtransArchive.InventTransCreatedDateTime`) وإضافة ملحقات إلى الفئتين `InventTransArchiveProcessTask` و`InventTransArchiveSqlStatementHelper`، كما يظهر في عينة التعليمات البرمجية التالية.

تعرض عينة التعليمة البرمجية التالية مثالاً عن كيفية إضافة الملحق المطلوب إلى الفئة `InventTransArchiveProcessTask`.

```xpp
[ExtensionOf(classStr(InventTransArchiveProcessTask))]
Final class InventTransArchiveProcessTask_Extension
{

    protected void addInventTransFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTrans, ModifiedBy))
            .add(fieldStr(InventTrans, CreatedBy)).add(fieldStr(InventTrans, CreatedDateTime));

        next addInventTransFields(_selectionObject);
    }


    protected void addInventTransArchiveFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTransArchive, InventTransModifiedBy))
            .add(fieldStr(InventTransArchive, InventTransCreatedBy)).add(fieldStr(InventTransArchive, InventTransCreatedDateTime));

        next addInventTransArchiveFields(_selectionObject);
    }
}
```

تعرض عينة التعليمة البرمجية التالية مثالاً عن كيفية إضافة الملحق المطلوب إلى الفئة `InventTransArchiveSqlStatementHelper`.

```xpp
[ExtensionOf(classStr(InventTransArchiveSqlStatementHelper))]
final class InventTransArchiveSqlStatementHelper_Extension
{
    private str     inventTransModifiedBy;  
    private str     inventTransCreatedBy;
    private str     inventTransCreatedDateTime;

    protected void initialize()
    {
        next initialize();
        inventTransModifiedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, ModifiedBy)).name(DbBackend::Sql);
        inventTransCreatedDateTime = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedDateTime)).name(DbBackend::Sql);
        inventTransCreatedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedBy)).name(DbBackend::Sql);
    }

    protected str buildInventTransArchiveSelectionFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransArchiveSelectionFieldsStatement();
        
        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransModifiedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedDateTime)).name(DbBackend::Sql));
        }

        return ret;
    }

    protected str buildInventTransTargetFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransTargetFieldsStatement();

        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransModifiedBy);
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedBy);
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedDateTime);
        }

        return ret;
    }
}
```
