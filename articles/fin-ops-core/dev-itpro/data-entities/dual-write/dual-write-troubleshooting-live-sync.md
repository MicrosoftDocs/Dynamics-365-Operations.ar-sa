---
title: استكشاف مشكلات المزامنة المباشرة وإصلاحها
description: توفر هذه المقالة معلومات استكشاف الأخطاء وإصلاحها الذي يمكن أن تساعدك على إصلاح مشكلات المزامنة المباشرة.
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 1211f7da15686f1c55a4c942f04c73d671e0ba6b
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111412"
---
# <a name="troubleshoot-live-synchronization-issues"></a>استكشاف مشكلات المزامنة المباشرة وإصلاحها

[!include [banner](../../includes/banner.md)]



توفر هذه المقالة معلومات استكشاف الأخطاء وإصلاحها في تكامل الكتابة المزدوجة بين تطبيقات التمويل والعمليات وMicrosoft Dataverse. على وجه التحديد، يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح مشكلات المزامنة المباشرة.

> [!IMPORTANT]
> قد تتطلب بعض المشكلات التي تتناولها هذه المقالة إما دور إدارة النظام أو بيانات اعتماد مسؤول المستأجر Azure Active Directory (Azure AD). يوضح كل قسم ما إذا كانت هناك حاجة إلى بيانات عتماد لدور محدد أو بيانات اعتماد خاصة.

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>تظهر المزامنة المباشرة خطأ عند إنشاء صف

قد تظهر رسالة الخطأ التالية عند إنشاء صف في تطبيق التمويل والعمليات:

*\[{\\"الخطأ\\":{\\"الكود\\":\\"0x80072560\\"،\\"الرسالة\\":\\"المستخدم ليس عضوا في المؤسسة.\\"}}\]، أرجع الخادم البعيد الخطأ: (403) ممنوع."}}".*

لإصلاح هذه المشكلة، اتبع الخطوات الموجودة في [متطلبات النظام والمتطلبات الأساسية](requirements-and-prerequisites.md). لإكمال هذه الخطوات، يجب أن يكون لدى مستخدمي تطبيق الكتابة الثنائية الذين تم إنشاؤهم في Dataverse دور مسؤول النظام. يجب أن يكون لدى الفريق المالك الافتراضي دور مسؤول النظام أيضًا.

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>تظهر المزامنة المباشرة خطأ عندما تحاول حفظ بيانات الجدول

**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام

قد تظهر رسالة الخطأ التالية عندما تحاول حفظ بيانات الجدول في تطبيق التمويل والعمليات:

*لا يمكن حفظ التغييرات التي تم اجراؤها علي قاعده البيانات. ولا يمكن لوحدة العمل تنفيذ الحركة. وتتعذر كتابة البيانات إلى وحدات قياس الكيانات. وفشلت عمليات الكتابة إلى UnitOfMeasureEntity مع ظهور رسالة الخطأ "تتعذر المزامنة مع وحدات قياس الكيانات.*

لإصلاح المشكلة، يجب التأكد من وجود بيانات مرجع المتطلبات الأساسية في كل من تطبيق التمويل والعمليات وDataverse. على سبيل المثال، إذا كان سجل العميل ينتمي إلى مجموعة عملاء محددة، فتأكد من وجود سجل مجموعة العملاء في Dataverse.

في حالة وجود بيانات في كلا المكانين، وقمت بالتأكد من أن المشكلة غير مرتبطة بالبيانات، فاتبع الخطوات التالية.

1. افتح كيان **DualWriteProjectConfigurationEntity** باستخدام المكون الإضافي لـ Excel. لاستخدام الوظيفة الإضافية، قم بتمكين وضع التصميم في وظيفة Excel الإضافية التمويل والعمليات وإضافة **DualWriteProjectConfigurationEntity** إلى ورقة عمل. لمزيد من المعلومات، راجع [عرض بيانات الكيان وتحديثها باستخدام Excel](../../office-integration/use-excel-add-in.md).
2. حدد واحذف السجلات التي بها مشاكل في خريطة الكتابة المزدوجة والمشروع. سيكون هناك سجلان لكل تعيين للكتابة المزدوجة.
3. قم بنشر التغييرات باستخدام وظيفة Excel الإضافية. هذه الخطوة هامة لأنها تحذف السجلات من الكيان والجداول الأساسية.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>معالجة أخطاء امتيازات القراءة أو الكتابة عند إنشاء بيانات في تطبيق التمويل والعمليات

قد تستلم رسالة الخطأ "طلب غير صحيح" عند إنشاء البيانات في تطبيق التمويل والعمليات:

![مثال لرسالة الخطأ "طلب غير صحيح".](media/error_record_id_source.png)

لإصلاح هذه المشكلة، يجب عليك تمكين الامتياز المفقود من خلال تعيين دور الأمان الصحيح إلى فريق Dynamics 365 Sales المعين أو وحدة الأعمال الخاصة بـ Dynamics 365 Customer Service.

1. في تطبيق التمويل والعمليات، ابحث عن وحدة الأعمال التي تم تعيينها في مجموعة اتصال تكامل البيانات.

    ![تعيين المؤسسة.](media/mapped_business_unit.png)

2. في تطبيق Customer Engagement، قم بتسجيل الدخول إلى البيئة، وانتقل إلى **الإعداد \> الأمان**، وابحث عن فريق وحدة الأعمال المعيّنة.

    ![فريق وحدة الأعمال المعيّنة.](media/setting_security_page.png)

3. افتح الصفحة الخاصة بالفريق للتحرير ، ثم حدد **إدارة الأدوار**.

    ![الزر إدارة الأدوار.](media/manage_team_roles.png)

4. في مربع الحوار **إدارة أدوار الفريق**، قم بتعيين الدور الذي يحتوي على امتياز القراءة/الكتابة للجداول ذات الصلة، ثم حدد **موافق**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>إصلاح مشكلات المزامنة في بيئة تحتوي على بيئة Dataverse تم تغييرها مؤخرًا

**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام

قد تظهر رسالة الخطأ التالية عند إنشاء بيانات في تطبيق التمويل والعمليات:

*{"entityName":"CustCustomerV3Entity"،"executionStatus":2,"fieldResponses":\[\]،"recordResponses":\[{"errorMessage":"**يتعذر إنشاء الحمولة للكيان CustCustomerV3Entity** فشل إنشاء logDateTime":"2019-08-27T18:51:52.5843124Z"،"verboseError":"Payload"،" مع ظهور الخطأ عنوان URL غير صالح: عنوان URI فارغ."}\]،"isErrorCountUpdated":true}*

فيما يلي رسالة الخطأ في تطبيق Customer Engagement:

> حدث خطأ غير متوقع من رمز ISV. (ErrorType = ClientError) استثناء غير متوقع من المكون الإضافي (تنفيذ): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: فشلت معالجة حساب الكيان - (فشلت محاولة الاتصال لأن الطرف المتصل لم يستجب بشكل صحيح بعد فترة من الوقت أو فشل الاتصال القائم لأن المضيف المتصل فشل في الاستجابة.

يحدث هذا الخطأ إذا تمت إعادة تعيين بيئة Dataverse بشكل غير صحيح عندما تحاول إنشاء البيانات في تطبيق التمويل والعمليات.

> [!IMPORTANT]
> إذا قمت بإعادة ربط البيئات، فيجب عليك إيقاف كافة تعيينات الكيانات قبل المتابعة في خطوات تقليل المخاطر.

لإصلاح المشكلة، يجب إكمال الخطوات في كل من تطبيق Dataverse والتمويل والعمليات.

1. في التطبيق التمويل والعمليات، اتبع الخطوات التالية:

    1. افتح كيان **DualWriteProjectConfigurationEntity** باستخدام المكون الإضافي لـ Excel. لاستخدام الوظيفة الإضافية، قم بتمكين وضع التصميم في وظيفة Excel الإضافية التمويل والعمليات وإضافة **DualWriteProjectConfigurationEntity** إلى ورقة عمل. لمزيد من المعلومات، راجع [عرض بيانات الكيان وتحديثها باستخدام Excel](../../office-integration/use-excel-add-in.md).
    2. حدد واحذف السجلات التي بها مشاكل في خريطة الكتابة المزدوجة والمشروع. سيكون هناك سجلان لكل تعيين للكتابة المزدوجة.
    3. قم بنشر التغييرات باستخدام وظيفة Excel الإضافية. هذه الخطوة هامة لأنها تحذف السجلات من الكيان والجداول الأساسية.
    4. للمساعدة في منع حدوث أخطاء عند إعادة ربط بيئات التمويل والعمليات أو Dataverse، تأكد من عدم بقاء أي تكوينات للكتابة المزدوجة.

2. في Dataverse، اتبع الخطوات التالية:

    1. قم بتسجيل الدخول إلى بيئة Dataverse الخاصة بك (على سبيل المثال، `https://*****.crm.dynamics.com/`).
    2. انتقل إلى **إعدادات متقدمة** \> **بحث متقدم**.
    3. حدد **تكوين وقت تشغيل الكتابة المزدوجة**.
    4. حدد العمود المراد عرضه.
    5. حدد **النتائج** لعرض التكوينات.
    6. احذف كافة المثيلات.

3. في التطبيق التمويل والعمليات، اتبع الخطوات التالية:

    1. افتح كيان **DualWriteProjectConfigurationEntity** باستخدام المكون الإضافي لـ Excel. لاستخدام الوظيفة الإضافية، قم بتمكين وضع التصميم في وظيفة Excel الإضافية التمويل والعمليات وإضافة **DualWriteProjectConfigurationEntity** إلى ورقة عمل. لمزيد من المعلومات، راجع [عرض بيانات الكيان وتحديثها باستخدام Excel](../../office-integration/use-excel-add-in.md).
    2. حدد واحذف السجلات التي بها مشاكل في خريطة الكتابة المزدوجة والمشروع. سيكون هناك سجلان لكل تعيين للكتابة المزدوجة.
    3. قم بنشر التغييرات باستخدام وظيفة Excel الإضافية. هذه الخطوة هامة لأنها تحذف السجلات من الكيان والجداول الأساسية.
    4. للمساعدة في منع حدوث أخطاء عند إعادة ربط بيئات التمويل والعمليات أو Dataverse، تأكد من عدم بقاء أي تكوينات للكتابة المزدوجة.

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>خطأ في المزامنة المباشرة بعد إجراء نسخ كامل لقاعدة البيانات

قد تتلقي رسالة الخطأ التالية بعد تشغيل النسخ الكامل لقاعدة البيانات من نظام إلى آخر ثم محاولة تشغيل عملية قاعدة البيانات:

*مؤسسة SecureConfig (???) لا تطابق مؤسسة CRM الفعلية (???).*

يتم عرض رسالة الخطأ من المكون الإضافي لوقت التشغيل الكتابة المزدوجة للتأكد من أن تكوين الكتابة المزدوجة الذي تم إعداده في أحد الأنظمة لا يمكن استخدامه في نظام آخر.

لإصلاح هذه المشكلة، قم بحذف كافة السجلات الموجودة في جدول **msdyn_dualwriteruntimeconfig** بعد استعادة قاعدة البيانات. لمزيد من المعلومات ، راجع [إلغاء ارتباط بيئات الكتابة المزدوجة وإعادة ربطها](relink-environments.md).

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>مشكلات المزامنة المباشرة التي تنتج عن بناء جملة عامل تصفية استعلام غير صحيح في خرائط الكتابة المزدوجة

على الرغم من أن تعبير الاستعلام لعامل تصفية خريطة الكتابة المزدوجة صحيح من ناحية البناء، لكنه قد لا يعمل كما هو متوقع. يكون تعبير عامل التصفية قيد التشغيل في أحد الكيانات، وليس على مصدر بيانات مفرد لكائن استعلام. لذلك، لا يقوم استعلام SQL الذي تم إنشاؤه بإرجاع النتائج المتوقعة.

فيما يلي مثال على ذلك.

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

قد تتوقع أن يتم استبعاد المشاريع التي ليس لها أصل. ومع ذلك، لا يعمل عامل التصفية لأنه تتم ترجمته إلى استعلام يشبه المثال التالي.

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

وتصبح النتيجة الفعلية أن حقل `parentProject` يتم تقييمه إلى `null`. مع ذلك، فإن `null` لا يماثل السلسلة الفارغة. بسبب عدم التطابق هذا، لا يرجع عامل تصفية الاستعلام نتائج صحيحة.

لإصلاح المشكلة، اتبع هذه الخطوات.

1. قم بإضافة عمود محسوب يمكن إضافته في نموذج ملحق، والذي يتم دعمه بمنطق يحول `null` إلى سلسلة فارغة.

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. استخدم عامل التصفية في العمود المحسوب الجديد بدلاً من العمود الافتراضي.

لتقييم عامل التصفية في بيئة تطوير، يمكنك استخدام كود X++ التالي للتحقق من صحة النتائج. قم بتشغيل هذا الكود كبرنامج مستقل. يمكنك استخدامه لتقييم أنواع مختلفه من عوامل التصفية التي تنطبق على أحد الكيانات قبل استخدام عوامل التصفية هذه في خرائط الكتابة المزدوجة. يمكن تشغيل الاستعلام مقابل قاعدة البيانات لتقييم الاختلافات.

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>لم تتم مزامنة البيانات من تطبيقات التمويل والعمليات مع Dataverse

أثناء المزامنة المباشرة، قد تواجه مشكله حيث تتم مزامنة جزء من البيانات فقط من تطبيقات التمويل والعمليات إلى Dataverse، أو عدم مزامنة البيانات على الإطلاق.

> [!NOTE]
> يجب إصلاح هذه المشكلة أثناء التطوير.

وقبل البدء في إصلاح المشكلة، راجع المتطلبات الأساسية التالية:

+ تأكد من كتابة التغييرات المخصصة الخاصة بك في نطاق حركة مفرد.
+ ولا تعالج أحداث الأعمال وإطار عمل الكتابة المزدوجة عمليات `doinsert()` و`doUpdate()` و`recordset()`، أو السجلات التي تم وضع علامة `skipBusinessEvents(true)` عليها. إذا كان الكود الخاص بك داخل هذه الوظائف، فلن يتم تشغيل الكتابة المزدوجة.
+ يجب تسجيل أحداث الأعمال لمصدر البيانات الذي تم تعيينه. قد تستخدم بعض مصادر البيانات صلة خارجية وقد يتم وضع علامة للقراءة عليها فقط في تطبيقات التمويل والعمليات. لا يتم تعقب مصادر البيانات هذه.
+ سيتم تشغيل التغييرات فقط إذا كانت التعديلات موجودة في الحقول المعينة. لا تقوم تعديلات الحقول غير المعينة بتشغيل الكتابة المزدوجة.
+ تأكد من أن تقييمات عامل التصفية توفر نتيجة صحيحة.

### <a name="troubleshooting-steps"></a>خطوات استكشاف الأخطاء وإصلاحها

1. راجع تعيينات الحقول على صفحة إدارة الكتابة المزدوجة. إذا لم يتم تعيين حقل من تطبيقات التمويل والعمليات إلى Dataverse، فلن يتم تتبعه. على سبيل المثال، في التوضيح التالي، يتم تتبع حقل **الوصف** من Dataverse، ولكن ليس من تطبيقات التمويل والعمليات. لن يتم تعقب أي تغييرات تطرأ على هذا الحقل داخل تطبيقات التمويل والعمليات.

    ![تم تتبع الحقل.](media/live-sync-troubleshooting-1.png)

2. حدد ما إذا كان يتم تتبع مصدر البيانات في تعريف أحداث الأعمال. على سبيل المثال، في التوضيح التالي ، لن يتم تتبع أي حقل من جدول **DefaultDimensionDAVs** والجداول الأساسية للتغييرات. لا يتم تتبع مصادر البيانات التي تستخدم صلة خارجية والتي وضعت لها علامة للقراءة فقط.

    ![لم يتم تتبع الحقل.](media/live-sync-troubleshooting-2.png)

3. حدد ما إذا كانت حقول الجدول المعين تظهر في جدول **BUSINESSEVENTSDEFINITION**، كما هو مبين في التوضيح التالي أم لا. إذا لم تعثر على الحقل الذي تبحث عنه في نتيجة الاستعلام، فلن يتم تشغيله بواسطة الكتابة المزدوجة.

    ![يتم تتبع الحقل في الجدول.](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>سيناريو كمثال

في تطبيقات التمويل والعمليات، يوجد تحديث لعنوان سجل جهة الاتصال، ولكن لم تتم مزامنة تغيير العنوان مع Dataverse. يحدث هذا السيناريو لأنه لا يوجد سجل في الجدول **BusinessEventsDefinition** يحتوي على مجموعة من الجداول المتأثرة والكيان. وبشكل خاص ، لا يعد الجدول **LogisticsPostalAddress** مصدر البيانات المباشر لكيان **smmContactpersonCDSV2Entity**. تحتوي الوحدة **smmContactpersonCDSV2Entity** على **smmContactPersonV2Entity** كمصدر بيانات، و **smmContactPersonV2Entity**، بدوره، يحتوي على **LogisticsPostalAddressBaseEntity** كمصدر بيانات. يعد **LogisticsPostalAddress** مصدر البيانات لـ **LogisticsPostalAddressBaseEntity**.

يمكن أن يحدث موقف مشابه في بعض الأنماط غير القياسية، مثل الحالات التي لا يرتبط فيها الجدول الذي يتم تعديله في تطبيقات التمويل والعمليات بشكل واضح بالكيان الذي يحتويه. على سبيل المثال، يتم حساب بيانات العنوان الرئيسي في كيان **smmContactPersonCDSV2Entity**. ويحاول إطار عمل الكتابة المزدوجة تحديد كيفية تعيين التغيير للجدول الأساسي إلى الكيانات مرة أخرى. عادة، يكون هذا الأسلوب كافياً. ومع ذلك، في بعض الحالات، يكون الارتباط معقداً ومن ثم يجب أن تكون محدداً. يجب التأكد من أن **RecId** للجدول المرتبط متوفر مباشرة في الكيان. ثم قم بإضافة أسلوب ثابت لمراقبة التغيرات التي تحدث على الجدول.

على سبيل المثال، قم بمراجعة الأسلوب **smmContactPersonCDSV2Entity::getEntityDataSourceToFieldMapping()**. تم تعديل **CustCustomerV3entity** و **VendVendorV2Entity** لمعالجة هذا الموقف.

لإصلاح المشكلة، اتبع هذه الخطوات.

1. قم بإضافة حقل **PrimaryPostalAddressRecId** إلى الكيان **smmContactPersonV2Entity** . اجعله داخلياً.

    ![تمت إضافة الحقل إلى الكيان smmContactPersonV2Entity.](media/Troubleshoot_live_sync_issue_1.png)

2. أضف نفس الحقل إلى الكيان **smmContactPersonCDSV2Entity**.

    ![تمت إضافة الحقل إلى الكيان smmContactPersonCDSV2Entity.](media/Troubleshoot_live_sync_issue_2.png)

3. قم بإضافة الأسلوب التالي إلى الفئة **smmContactPersonCDSV2Entity**.

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. قم بمزامنة قاعدة البيانات وإنشاء التطبيق.
5. أوقف كافة خرائط الكتابة المزدوجة التي تم إنشاؤها في الكيان **smmContactPersonCDSV2Entity**.
6. ابدأ الخريطة. يجب أن تشاهد الجدول الجديد (**LogisticsPostalAddress** في هذاالمثال) الذي بدأت تتبعه باستخدام العمود **RefTableName** للصف الذي تكون فيه قيمة **refentityname** مساوية لـ **smmContactPersonCDSV2Entity** في الجدول **BusinessEventsDefinition**.

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>حدوث خطأ عند إنشاء سجل حيث يتم إرسال سجلات متعددة من أحد تطبيقات التمويل والعمليات إلى Dataverse في نفس الدفعة

مع أي حركة، يقوم تطبيق التمويل والعمليات بإنشاء البيانات في دفعة وإرسالها كدفعة إلى Dataverse. إذا تم إنشاء سجلين كجزء من نفس الحركة، وقاما بالإشارة إلى بعضهما البعض، فقد تتلقي رسالة خطأ تشبه المثال التالي في تطبيق التمويل والعمليات:

*يتعذر كتابة البيانات إلى الكيان aaa_fundingsources. يتعذر البحث عن ebecsfs_contracts بالقيم {PC00...}. يتعثر البحث عن aaa_fundingsources بالقيم {PC00...}. فشلت الكتابة إلى aaa_fundingsources مع رسالة خطأ رسالة الاستثناء: أرجع الخادم البعيد الخطأ: (400) طلب غير صحيح.*

لإصلاح المشكلة، قم بإنشاء علاقات الكيان في تطبيق التمويل والعمليات للإشارة إلى كيانين مرتبطين ببعضهما البعض، وأنه تجري معالجة السجلات المرتبطة في نفس الحركة.

## <a name="enable-verbose-logging-of-error-messages"></a>تمكين التسجيل المطول لرسائل الخطأ

في تطبيق التمويل والعمليات، قد تواجه أخطاء متعلقة ببيئة Dataverse. قد لا تحتوي رسالة الخطأ على النص الكامل للرسالة أو البيانات الأخرى ذات الصلة. للحصول على مزيد من المعلومات، يمكنك تمكين التسجيل المطول بتعيين العلامة **IsDebugMode** الموجودة على الكيان **DualWriteProjectConfigurationEntity** في جميع تكوينات المشروع في تطبيقات التمويل والعمليات.

1. افتح كيان **DualWriteProjectConfigurationEntity** باستخدام المكون الإضافي لـ Excel. لاستخدام الوظيفة الإضافية، قم بتمكين وضع التصميم في وظيفة Excel الإضافية التمويل والعمليات وإضافة **DualWriteProjectConfigurationEntity** إلى ورقة عمل. لمزيد من المعلومات، راجع [عرض بيانات الكيان وتحديثها باستخدام Excel](../../office-integration/use-excel-add-in.md).
2. قم بتعيين علامة **IsDebugMode** إلى **نعم** في المشروع.
3. تشغيل السيناريو.
4. تتوفر السجلات المطولة للأخطاء في الجدول **DualWriteErrorLog**. للبحث عن البيانات باستخدام مستعرض الجداول، استخدم عنوان URL التالي: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`.
5. للتقاط مزيد من السجلات في وضع التصحيح، قم بتثبيت التحديث في [KB 4595434 (إصلاح القيم الفارغة الجاري نشرها في المزامنة المباشرة للكتابة المزدوجة) ](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9).

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>حدوث خطأ عند إضافة عنوان لعميل أو جهة اتصال

قد تتلقي رسالة الخطأ التالية عند محاولة إضافة عنوان لعميل أو جهة اتصال في تطبيقات التمويل والعمليات أو Dataverse:

*يتعذر كتابة البيانات إلى الكيان msdyn_partypostaladdresses. فشلت الكتابة إلى DirPartyPostalAddressLocationCDSEntity مع رسالة الخطأ فشل الطلب مع رمز الحالة BadRequest ورمز خطأ CDS: 0x80040265 رسالة الاستجابة: حدث خطأ في المكون الإضافي. السجل الذي يتضمن قيم سمة "معرف الموقع" موجود بالفعل. مفتاح معرف موقع مفتاح الكيان يتطلب أن تحتوي مجموعة السمات هذه على قيم فريدة. حدد قيمًا فريدة وأعد المحاولة.*

لإصلاح هذه المشكلة، قم بتثبيت الإصدار (2.2.2.60) من حزمة تنسيق الكتابة المزدوجة، بحيث يتم تعريف المفاتيح في جدول **العناوين** كما هو موضح في الجدول التالي.

| الخاصية | قيمة |
|---|---|
| الاسم المعروض | **مفتاح الموقع** |
| الاسم | **msdyn_locationkey** |
| الحقول | **msdyn_locationid**, **parentid** |
| الحالة | **نشط** |
| وظيفة النظام | فارغ |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>حدوث خطأ عند إضافة عميل في Dataverse

قد تظهر رسالة الخطأ التالية عندما تحاول إضافة عميل في Dataverse:

*"RecordError0":"فشلت الكتابة إلى الكيان Customers V3 مع استثناء غير معروف - لم يتم العثور على سجل الطرف للنوع الطرف 'مؤسسة'"}.*

عند إنشاء عميل في Dataverse، يتم إنشاء رقم طرف جديد. يتم عرض رسالة الخطأ عند مزامنة سجل العميل، إلى جانب الطرف، مع تطبيقات التمويل والعمليات، ولكن يوجد بالفعل سجل عميل له رقم طرف مختلف.

لإصلاح هذه المشكلة، ابحث عن العميل من خلال البحث عن الطرف. إذا لم يكن العميل موجودًا بالفعل، فقم بإنشاء سجل عميل جديد. إذا كان العميل موجودًا، فاستخدم الطرف الموجود لإنشاء سجل العميل الجديد.

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>حدوث خطأ عند إنشاء عميل أو مورد أو جهة اتصال جديدة في Dataverse

قد تتلقي رسالة الخطأ التالية عند محاولة إنشاء عميل أو مورد أو جهة اتصال جديدة في Dataverse:

*لا يمكن تحديث نوع الطرف من 'DirOrganization' إلى 'DirPerson'، ويجب إجراء حذف للطرف الموجود متبوعاً بإدخال نوع جديد بدلا من ذلك.*

في Dataverse، يوجد تسلسل رقمي في الجدول **msdyn_party**. عند إنشاء حساب في Dataverse، يتم إنشاء طرف جديد (على سبيل المثال **Party-001** من النوع **مؤسسة**). يتم إرسال هذه البيانات إلى تطبيق التمويل والعمليات. إذا تمت إعادة تعيين بيئة Dataverse، أو إذا كانت بيئة التمويل والعمليات مرتبطة ببيئة Dataverse مختلفة، ثم تم إنشاء سجل جهة اتصال جديد في Dataverse، فسيتم إنشاء قيمة طرف جديدة تبدا **Party-001**. وفي هذه المرة، سيكون سجل الطرف الذي تم إنشاؤه هو **Party-001** من النوع **شخص**. عند مزامنة هذه البيانات، تعرض تطبيقات التمويل والعمليات رسالة الخطأ السابقة، لأن سجل الطرف **Party-001** من النوع **مؤسسة** موجود بالفعل.

لإصلاح هذه المشكلة، قم بتغيير التسلسل الرقمي التلقائي للحقل **msdyn_partynumber** بالجدول **msdyn_party** في Dataverse إلى تسلسل رقمي تلقائي مختلف.

## <a name="performance-issue-with-customer-or-contact-mappings"></a>مشكلة في الأداء مع تعيينات العملاء أو جهات الاتصال

يمكنك تحسين الأداء هامشيًا في المزامنة المباشرة للعملاء وجهات الاتصال من خلال تخصيص الأسلوب **getEntityDataSourceToFieldMapping** (في الكيان **CustCustomerV3Entity**) والأسلوب **getEntityDataSourceToFieldMapping** (في الكيان **smmContactPersonCDSV2Entity**). تقلل هذه التخصيصات من عدد السجلات في الجدول **BusinessEventsDefinition**. ويقلل هذا التخفيض في عدد السجلات، بدوره، عدد الأحداث التي يتم رفعها.

يعمل الأسلوب **getEntityDataSourceToFieldMapping** في الكيان **CustCustomerV3Entity** على التأكد من أن تحديث العنوان الإلكتروني أو العنوان البريد للعميل يشغل أحداث الأعمال، لذا يتم إرسال البيانات المحدّثة إلى Dataverse. إذا لم تستخدم كافة الحقول ولا تحتاج للمعلومات في الكتابة المزدوجة، فقم بالتعليق على البنود المناسبة في الأسلوب. يضيف كل حقل وجدول متتبع تتم إضافته في هذا الأسلوب سجلا في جدول **BusinessEventsDefinition** لمجموعة الجداول المتتبعة والكيان المتتبع.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

بطريقة مماثلة يعمل الأسلوب **getEntityDataSourceToFieldMapping** في الكيان **smmContactPersonCDSV2Entity** على التأكد من أن أي تحديث للعنوان الإلكتروني أو العنوان البريد للعميل يشغل أحداث الأعمال، لذا يتم إرسال البيانات المحدّثة إلى Dataverse. في الأسلوب، يمكنك التعليق على البنود الخاصة بأي حقول لا تستخدمها.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

بعد تحديث الأساليب، اتبع الخطوات التالية.

1. قم بمزامنة قاعدة البيانات وإنشاء التطبيق.
2. أوقف كافة خرائط الكتابة المزدوجة في الكيان **smmContactPersonCDSV2Entity** و **CustCustomerV3Entity** .
3. ابدأ الخرائط. يجب أن تشاهد سجلات أقل في الكيانات **smmContactPersonCDSV2Entity** و **CustCustomerV3Entity** وفي الجدول **BusinessEventsDefinition**، وقد يتحسن الأداء هامشيًا.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

