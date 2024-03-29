---
title: التحصيلات في الحسابات المدينة
description: تتم إدارة معلومات تحصيلات الحسابات المدينة في طريقة عرض مركزية واحدة باستخدام صفحة "التحصيلات" في Microsoft Dynamics 365 Finance. بإمكان مدراء الائتمانات والتحصيلات استخدام طريقة العرض المركزية هذه لإدارة التحصيلات. وبإمكان وكلاء التحصيلات بدء عملية التحصيل من قوائم العملاء التي يتم إنشاؤها باستخدام معايير التحصيل المعرفة مسبقًا أو من صفحة العملاء.
author: ShivamPandey-msft
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustAgingSnapshot, CustBankAccounts, CustCollections, CustCollectionsActivitiesListPage, CustCollectionsAgent, CustCollectionsCaseListPage, CustCollectionsPool, CustCollectionsPoolsListPage, CustTable
audience: Application User
ms.reviewer: kfend
ms.custom: 3061
ms.assetid: fd851520-8d93-434b-845b-be127d6ac3a6
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 00e536241710fc8a75158472688757320abf4247
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067197"
---
# <a name="collections-in-accounts-receivable"></a>التحصيلات في الحسابات المدينة

[!include [banner](../includes/banner.md)]

تتم إدارة معلومات تحصيلات الحسابات المدينة في طريقة عرض مركزية واحدة باستخدام صفحة "التحصيلات" في Microsoft Dynamics 365 Finance. بإمكان مدراء الائتمانات والتحصيلات استخدام طريقة العرض المركزية هذه لإدارة التحصيلات. وبإمكان وكلاء التحصيلات بدء عملية التحصيل من قوائم العملاء التي يتم إنشاؤها باستخدام معايير التحصيل المعرفة مسبقًا أو من صفحة العملاء.

قبل البدء في إعداد أو العمل مع المجموعات، يجب عليك فهم المفاهيم التالية:
-   لقطات تأخر العميل تحتوي على معلومات الرصيد القديمة عند نقطة في وقت
-   أوعية عملاء التحصيلات تساعدك في تنظيم العمل
-   عوامل التحصيلات قد تشمل أوعية العملاء الخاصة بها
-   صفحات القوائم تنظم حالات وأنشطة وعملاء التحصيلات
-   توجد كافة معلومات التحصيلات لعميل في صفحة واحدة ويمكنك اتخاذ إجراء من هذه الصفحة
-   التنازل عن أو إعادة المطالبة بـ أو عكس الفائدة والرسوم من الممكن أن يتم في خطوة واحدة
-   يمكن إنشاء حركات الشطب في خطوة واحدة
-   يمكن أن تتم معالجة مدفوعات الأموال غير الكافية (NSF) في خطوة واحدة

توضح الأقسام التالية كل مفهوم.

## <a name="customer-aging-snapshots"></a>لقطات تأخر العميل 
تحتوي لقطة تأخر على الأرصدة القديمة المحسوبة لعميل عند نقطة زمنية واحدة. وتظهر معلومات لقطة التأخر في صفحة قائمة الأرصدة القديمة وفي صفحة التحصيلات. ويجب إنشاء لقطة تأخر قبل أن يمكنك عرض المعلومات في صفحات قائمة التحصيلات. 

ولكل عميل، تحتوي لقطة تأخر على رأس لقطة تأخر وسجلات التفاصيل التي تتوافق مع كل فترة تأخر في تعريف فترة التأخر. 

يحتوي رأس لقطة التأخر على مجموع المبلغ المستحق، والحد الائتماني، وإيصال التعبئة، ومبلغ أمر المبيعات، وعدد الحركات المتنازع عليها، والمبلغ الإجمالي للحركات المتنازع عليها لحساب العميل. ويتم تضمين كافة الحركات للعميل في عملية حساب هذه المبالغ. ويتم عرض مجموع المبلغ المستحق، وحد الائتمان، ومبلغ إيصال التعبئة، ومبلغ أمر المبيعات في مربع حقائق معلومات الائتمان في صفحة التحصيلات. 

بالنسبة لكل فترة تأخر في تعريف فترة التأخر، يتم إنشاء سجل تفاصيل لقطة التأخر. ويحتوي كل سجل تفاصيل للقطة التأخر على معرف فترة التقادم والمبلغ الإجمالي للحركات المشتملة على تواريخ في فترة التقادم. ويتم تعيين الحركات إلى فترة تقادم، مثل 30 يومًا بعد الاستحقاق. يتعلق التاريخ بالتأخر اعتبارًا من التاريخ الذي تم تحديده عند إنشاء لقطة التأخر. وتظهر هذه المعلومة في صفحة قائمة الأرصدة القديمة وفي مربع حقائق الأرصدة القديمة في صفحة التحصيلات.

## <a name="collections-customer-pools"></a> أوعية عملاء التحصيلات
أوعية العملاء هي استعلامات تحدد مجموعة سجلات العملاء التي يمكن عرضها وإدارتها لعمليات التحصيلات أو التأخر. واستخدم أوعية العملاء لتصفية المعلومات في صفحة قوائم الأرصدة القديمة، وأنشطة التحصيلات، وحالات التحصيلات. ويمكنك أيضًا استخدام أوعية العملاء لتصفية حسابات العملاء التي تم تضمينها عند إنشاء لقطات التأخر.

## <a name="collections-agents"></a>وكلاء التحصيلات
بشكل افتراضي، بإمكان المستخدمين عرض كافة معلومات العملاء في صفحات قوائم التحصيلات. ويمكنك استخدام سجلات وكلاء التحصيلات لتحديد أوعية العملاء المتوفرة لتصفية المعلومات في صفحات قوائم التحصيلات وفي صفحة التحصيلات. 

وكيل التحصيلات هو شخص يعمل مع العملاء للتأكد من أنه يتم جمع المدفوعات في الوقت مناسب. وكلاء التحصيلات هم عاملون يتم تعيينهم للمستخدمين في صفحة "إعداد المستخدم".

## <a name="collections-list-pages"></a>صفحات قوائم المجموعات
تساعدك صفحات القوائم التالية في تنظيم معلومات التحصيلات.
-   الأرصدة القديمة‬ - تعرض الأعمدة الموجودة في صفحة القائمة أرصدة العملاء والمبالغ المتأخرة حسب فترة التأخر. يتم تخزين هذه المعلومات في لقطة التأخر. يتم تحديد فترات التأخر من خلال تعريف فترة التأخر المستخدمة. يتم أخذ تعريف فترة التأخر من وعاء العملاء، إذا تم تحديد وعاء لاستعلام الوعاء. وإذا لم يتضمن الوعاء تعريف فترة التقادم، يتم استخدام تعريف فترة التقادم الافتراضي المحدد في صفحة معلمات الحسابات المدينة. في حالة عدم تحديد أي تعريف افتراضي لفترة التقادم، فإنه يتم استخدام أول تعريف لفترة التقادم في صفحة تعريفات فترة التقادم.
-   أنشطة التحصيلات - تعرض الأعمدة في صفحة القوائم الأنشطة التي تم تحديدها كأنشطة تحصيلات. يتم إنشاء هذه الأنشطة باستخدام صفحة "التحصيلات". استخدم الأنشطة لتتبع العمل الذي تقوم به المرتبط بالتحصيلات.
-   حالات التحصيلات – تعرض الأعمدة في صفحة القوائم معلومات للحالات التي تحتوي على فئة حالة باستخدام نوع حالة التحصيلات.

> [!NOTE]
> ويجب إنشاء لقطة تأخر قبل أن يمكنك عرض المعلومات في صفحات القوائم هذه. لا يتم عرض المعلومات إلا للعملاء الذين تم إنشاء لقطة تأخر لهم. يمكن إضافةً إلى ذلك تصفية السجلات التي تظهر في صفحة القائمة، كما يلي:
> <li>بشكل افتراضي، يصل مستخدم التمويل والعمليات إلى جميع العملاء الذين لديهم لقطة تأخر.</li>
> <li>في حالة وجود أوعية العملاء، يجب إعداد مستخدم كوكيل تحصيلات لاستخدام التأوعية لتصفية المعلومات الموجودة في صفحات قوائم التحصيلات. وتقتصر المعلومات على العملاء الموجودين في وعاء العملاء المحدد.</li>
> <li>إذا تم تعيين مستخدم كوكيل تحصيلات، تتوفر فقط الأوعية التي تم تحديدها لوكيل التحصيلات هذا في صفحة القائمة. في حالة تحديد "‏‫تبديل السماح للوكيل بعرض كافة أوعية العملاء‬" في صفحة وكيل التحصيلات الخاصة بوكيل التحصيلات، تتوفر كافة الأوعية لهذا الوكيل.</li>


## <a name="collections-page"></a> صفحة التحصيلات
استخدم صفحة التحصيلات لعرض وإدارة واتخاذ إجراء في معلومات التحصيلات وأنشطتها وحالاتها لعميل. 

يعرض الجزء العلوي حالات للعميل المحدد. يعرض الجزء الأوسط حركات للعميل. يعرض الجزء السفلي أنشطة للعميل. ويمكنك إنشاء حالات التحصيلات لتعقب معلومات التحصيلات لواحد أو أكثر من الحركات والأنشطة. ويمكن تصفية المعلومات الواردة في الجزئين العلوي والسفلي حسب الحالة. 

وتعرض مربعات الحقائق الأرصدة القديمة ومعلومات حد الائتمان للعميل المحدد. ويتم تخزين هذه المعلومات في لقطة التأخر. إذا لزم الأمر، يمكنك تحديث لقطة التأخر بالمعلومات الحالية. 

ويحتوي جزء الإجراء على أزرار تعرض المعلومات ذات الصلة للعميل المحدد أو الحالة أو الحركة أو النشاط. يمكنك أيضًا تنفيذ الإجراءات الشائعة، مثل تغيير حالة التحصيلات لحركة، وإرسال رسائل البريد الإلكتروني من خلال التكامل مع مزود البريد الإلكتروني، وتعويض العملاء، ومعالجة مدفوعات NSF، وشطب الأرصدة غير القابلة للتحصيل.

## <a name="waive-reinstate-or-reverse-interest-and-fees"></a> التنازل عن الفائدة والرسوم أو إعادة المطالبة بهما أو إلغاؤهما 
يمكنك التنازل عن أو إلغاء أو إعادة المطالبة بإشعارات الفائدة الكاملة، أو الرسوم وفائدة الحركة التي هي جزء من إشعارات الفائدة. يمكنك ذلك من علامة التبويب "تحصيل" في "جزء الإجراءات" في صفحة قائمة كافة العملاء بالنقر فوق إشعار الفائدة أو فائدة الحركة أو الرسوم. 

وتؤثر هذه التسويات على إشعارات الفائدة فقط، والفائدة والرسوم التي تشملها. استخدم الخطوات في قسم "إنشاء حركات الشطب في خطوة واحدة" لشطب كافة التكاليف التي يمتلكها عميل.

لمزيد من المعلومات، راجع [إنشاء رمز فائدة مع نطاق‬](tasks/create-interest-code-range.md) و[معالجة الفائدة](tasks/process-interest.md). 

## <a name="create-writeoff-transactions"></a>إنشاء حركات الشطب
يمكنك شطب الديون المشكوك فيها عن طريق النقر فوق "شطب" في نموذج التحصيلات، وفي صفحات قوائم الأرصدة القديمة، والعملاء، وفواتير العملاء المفتوحة. 

وعند قيامك بشطب حركات عميل، يتم تمييز كافة حركات العميل تلقائياً للتسوية. ويعتمد المبلغ الذي يتم شطبه على المبلغ الصافي للحركات المميزة. يتم إنشاء شطب الحركة في دفتر يومية عام ويمكن أن يحتوي على ثلاثة أنواع من بنود دفتر اليومية.

-   يحتوي النوع الأول من بند دفتر اليومية على إدخال شطب العميل. وإذا كانت الحركات المميزة تحتوي على مجموعات متعددة من كود العملة، والبعد، وملف تعريف الترحيل، فإنه يتم إنشاء بند دفتر يومية منفصل لكل مجموعة.
-   يحتوي النوع الثاني من بند دفتر اليومية على إدخال شطب دفتر الأستاذ العام. وإذا كانت الحركات المميزة تحتوي على مجموعات متعددة من كود العملة، والبعد، وملف تعريف الترحيل، فإنه يتم إنشاء بند دفتر يومية منفصل لكل مجموعة.
-   يحتوي النوع الثالث من بند دفتر اليومية على معلومات شطب دفتر الأستاذ العام لضرائب المبيعات. ويتم إنشاء بند دفتر اليومية هذا فقط إذا تم تحديد تبديل ضريبة المبيعات المنفصلة في صفحة معلمات الحسابات المدينة. وإذا كانت الحركات المميزة تحتوي على مجموعات متعددة من الحساب الدائن لضريبة المبيعات، والبعد، وكود ضريبة المبيعات، فإنه يتم إنشاء بند دفتر يومية منفصل لكل مجموعة.

يتم إنشاء حركة الشطب بعملة الحركة.

لمزيد من المعلومات، راجع [إنشاء دفتر يومية شطب لعميل](tasks/create-write-off-journal-customer.md).

## <a name="process-not-sufficient-funds-nsf-payments"></a> معالجة دفعات الأرصدة غير الكافية (NSF)  

يمكنك معالجة مدفوعات NSF بالنقر فوق دفع NSF في صفحة التحصيلات. وعند النقر فوق هذا الزر، يتم إلغاء الدفع. إذا تم تطبيق رسوم NSF للعميل، فإنه يتم إنشاء حركة مصاريف في دفتر يومية الدفع. يعتمد مبلغ الرسوم على إعدادات الرسوم التلقائية. يتم تحديد الرسوم التلقائية التي تنطبق على مدفوعات NSF من خلال مجموعة المصاريف التي يتم اختيارها في صفحة الحسابات البنكية للحساب البنكي المتأثر.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

