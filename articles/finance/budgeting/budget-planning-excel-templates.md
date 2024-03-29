---
title: قوالب تخطيط الموازنة لـ Excel
description: توضح هذه المقالة كيفية إنشاء قوالب Microsoft Excel التي يمكن استخدامها مع خطط الموازنة.
author: panolte
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: kfend
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8996ad5d03327b9273be7860a3905dc25efa7e90
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070653"
---
# <a name="budget-planning-templates-for-excel"></a>قوالب تخطيط الموازنة لـ Excel

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية إنشاء قوالب Microsoft Excel التي يمكن استخدامها مع خطط الموازنة.

توضح هذه المقالة كيفية إنشاء قوالب Excel التي سيتم استخدامها مع خطط الموازنة باستخدام مجموعة بيانات العرض التقديمي القياسية وتسجيل دخول المستخدم المسؤول. لمزيد من المعلومات حول تخطيط الموازنة، راجع [نظرة عامة حول تخطيط الموازنة](budget-planning-overview-configuration.md). يمكنك أيضًا متابعة البرنامج التعليمي [تخطيط الموازنة](budget-plan.md) لمعرفة تكوين الوحدة الأساسية ومبادئ الاستخدام.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>إنشاء ورقة عمل باستخدام تخطيط مستند خطة الموازنة

يمكن عرض مستندات خطة الموازنة وتحريرها باستخدام تخطيط واحد أو أكثر. يمكن أن يكون لكل تخطيط قالب مستند خطة موازنة مقترن لعرض وتحرير بيانات خطة الموازنة في ورقة عمل Excel. في هذه المقالة، سيتم إنشاء قالب مستند خطة الموازنة باستخدام تكون تخطيط موجود. 

1. افتح **قائمة خطط الموازنة** (**الموازنة** &gt; **خطط الموازنة**). 
2. انقر فوق **جديد** لإنشاء مستند خطة موازنة جديد. 

   [![قائمة خطط الموازنة.](./media/bpt11-1024x552.png)](./media/bpt11.png) 

3. استخدم خيار سطر **إضافة** لإضافة السطور. انقر فوق **تخطيطات** لعرض تكوين تخطيط مستند خطة الموازنة. 

   [![إضافة خطط الموازنة.](./media/bpt2-1024x274.png)](./media/bpt2.png) 

يمكنك مراجعة تكوين التخطيط وتعديله وفقًا لما هو مطلوب. 
1. انتقل إلى **قالب** &gt; **إنشاء** لإنشاء ملف Excel لهذا التخطيط. 
2. بعد إنشاء القالب، انتقل إلى **قالب** &gt; **عرض** لفتح ومراجعة قالب مستند خطة الموازنة. يمكنك حفظ ملف الـ Excel في المحرك المحلي. 

[![حفظ باسم.](./media/bpt3-1024x545.png)](./media/bpt3.png)

> [!NOTE] 
> تعذر تحرير تخطيط مستند خطة الموازنة بعد اقتران قالب Excel بالمستند. لتعديل التخطيط، احذف ملف قالب Excel المقترن، وقم بإعادة الإنشاء. يتطلب هذا الاحتفاظ بالحقول في التخطيط، ومزامنة ورقة العمل. 

سوف يحتوي قالب Excel على جميع العناصر من تخطيط مستند خطة الموازنة، عندما يتم تعيين عمود **متوفر في ورقة العمل** على وضع "صواب". لا يسمح بعناصر التداخل في قالب Excel. على سبيل المثال، إذا كان التخطيط يحتوي على أعمدة طلب ربع1، وطلب ربع2، وطلب ربع3 وطلب ربع4، وعمود الطلب الإجمالي والذي يمثل مجموع الأربعة أعمدة الربع سنوية، يتاح استخدام الأعمدة الربع سنوية أو العمود الإجمالي فقط في قالب Excel. يتعذر على ملف Excel تحديث أعمدة التداخل أثناء التحديث لأن البيانات في الجدول قد تصبح قديمة وغير دقيقة.

> [!NOTE] 
> لتجنب المشاكل المحتملة في عرض وتحرير بيانات خطة الموازنة باستخدام Excel، يجب على المستخدم نفسه تسجيل دخوله إلى كل من Microsoft Dynamics 365 Finance وموصل بيانات وظيفة Office الإضافية لـ Microsoft Dynamics.

## <a name="add-a-header-to-budget-plan-document-template"></a>إضافة عنوان إلى قالب مستند خطة الموازنة
لإضافة معلومات العنوان، حدد الصف العلوي في ملف Excel، ثم قم بإدراج صفوف فارغة. انقر فوق **تصميم** في **موصل البيانات** لإضافة حقول العنوان إلى ملف Excel.

على علامة التبويب **تصميم**، انقر فوق حقول **إضافة**، ثم حدد **BudgetPlanHeader** كمصدر بيانات الكيان.

وجّه المؤشر إلى الموقع المطلوب في ملف Excel. انقر فوق **إضافة تسمية** لإضافة تسمية الحقل إلى الموقع المحدد. حدد **"إضافة قيمة"** لإضافة قيمة الحقل إلى الموضع المحدد. انقر فوق **تم** لإغلاق المصمم.

## <a name="select-add-valuemediabpt7png"></a>[![تحديد إضافة قيمة.](./media/bpt7.png)](./media/bpt7.png)

## <a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>إضافة عمود محسوب إلى جدول قالب مستند خطة الموازنة

التالي، سوف تتم إضافة الأعمدة المحسوبة إلى قالب مستند خطة الموازنة الذي تم إنشاؤه. عمود **إجمالي الطلب**، والذي يلخص طلب ربع1: أعمدة طلب ربع4، وعمود **التسوية**، والذي يقوم بإعادة حساب عمود **"إجمالي الطلب"** من خلال عامل محدد مسبقًا.

انقر فوق **تصميم** في **موصل البيانات** لإضافة الأعمدة إلى الجدول. انقر فوق **تحرير** الموجود بجوار مصدر بيانات **BudgetPlanWorksheet** لبدء إضافة أعمدة.

[![بدء إضافة الأعمدة.](./media/bpt8-1024x301.png)](./media/bpt8.png) 

تعرض مجموعة الحقل المحدد الأعمدة المتوفرة في القالب. انقر فوق **معادلة** لإضافة عمود جديد. قم بتسمية العمود الجديد، ثم قم بلصق المعادلة داخل حقل **المعادلة**. انقر فوق **تحديث** لإدراج عمود.

[![إضافة عمود وإدراجه.](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> لتحديد المعادلة، قم بإنشاء المعادلة في جدول البيانات، ثم قم بنسخها إلى نافذة **تصميم**. عادة ما يتم تسمية جدول العمليات المرتبطة للتمويل والعمليات باسم "AXTable1". على سبيل المثال، لتلخيص طلب ربع1: أعمدة طلب ربع4 في جدول البيانات، المعادلة= AxTable1\[طلب ربع1\]+AxTable1\[طلب ربع2\]+AxTable1\[طلب ربع3\]+AxTable1\[طلب ربع4\].

كرر هذه الخطوات لإدراج عمود **تسوية**. استخدم المعادلة= AxTable1\[طلب إجمالي\]\*$I$1 لهذا العمود. وسوف تأخذ هذه القيمة في الخلية 1 ومضاعفة القيم في عمود **الطلب الإجمالي** لحساب مبالغ التسوية.

قم بحفظ ملف Excel وإغلاقه. في **التخطيطات**، انقر فوق **قالب &gt; تحميل** لتحميل قالب Excel المحفوظ ليتم استخدامه لخطة الموازنة. 

[![تحميل قالب Excel.](./media/bpt10-1024x352.png)](./media/bpt10.png) 

إغلاق شريط تمرير **تخطيطات**. في مستند **خطة الموازنة**، انقر فوق **ورقة عمل** لعرض وتحرير المستند في Excel. لاحظ أنه تم استخدام قالب Excel المعدل لإنشاء ورقة عمل خطة الموازنة هذه، ويتم تحديث الأعمدة المحسوبة باستخدام المعادلات التي تم تحديدها في الخطوات السابقة. 

[![عرض المستند وتحريره في Excel.](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>تلميحات ونصائح حول إنشاء قوالب خطة الموازنة
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>هل يمكنني إضافة واستخدام مصادر بيانات إضافية إلى قالب خطة الموازنة؟

نعم، يمكنك استخدام قائمة **تصميم** لإضافة كيانات إضافية لنفس الأوراق أو لأوراق أخرى في قالب Excel. على سبيل المثال، يمكنك إضافة مصدر بيانات **BudgetPlanProposedProject** لإنشاء والاحتفاظ بقائمة المشاريع المقترحة في نفس الوقت عند العمل مع بيانات خطة الموازنة في Excel. لاحظ أن تضمين مصادر بيانات كبيرة الحجم قد يؤثر على أداء مصنف Excel. 

يمكنك استخدام خيار **عامل تصفية** الموجود في **"موصل البيانات"** لإضافة عوامل التصفية المطلوبة إلى مصادر البيانات الإضافية.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>هل يمكن إخفاء خيار "تصميم" في "موصل البيانات" للمستخدمين الآخرين؟

نعم، قم بفتح خيارات **"موصل البيانات"** لإخفاء خيار **تصميم** من مستخدمين آخرين.

[![خيارات موصل البيانات المفتوحة.](./media/bpt13-1024x565.png)](./media/bpt13.png)

قم بتوسيع **خيارات موصل البيانات** ومسح خانة اختيار **تمكين التصميم**. وسوف يقوم هذا بإخفاء خيار **التصميم** من **موصل البيانات**.

[![إخفاء خيار التصميم من موصل البيانات.](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>هل يمكنني منع المستخدمين من إغلاق موصل البيانات عن طريق الخطأ أثناء العمل مع البيانات؟

نوصي بغلق القالب لمنع المستخدمين من إغلاقه. لتشغيل خاصية "التأمين"، انقر فوق **موصل البيانات**، سوف يظهر سهم في الزاوية اليمنى العليا. 

[![تشغيل التأمين.](./media/bpt15-1024x285.png)](./media/bpt15.png) 

انقر فوق السهم لقائمة إضافية. حدد **تأمين**.

### <a name="select-lockmediabpt16png"></a>[![تحديد تأمين.](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>هل يمكنني استخدام ميزات Excel الأخرى، مثل تنسيق الخلايا، والألوان والتنسيق الشرطي والمخططات مع قوالب خطة الموازنة؟

نعم، تعمل معظم إمكانيات Excel القياسية في قوالب خطة الموازنة. نوصي باستخدام ترميز الألوان للمستخدمين للتمييز بين أعمدة القراءة فقط والأعمدة التي يمكن تحريرها. يمكن استخدام التنسيق الشرطي لتمييز المناطق المثيرة للمشاكل في الموازنة. يمكن بسهولة عرض إجماليات الأعمدة باستخدام معادلات Excel القياسية الموجود أعلى الجدول.

يمكنك أيضا إنشاء واستخدام الرسوم البيانية والجداول المحورية للتجميعات الإضافية والرسوم المرئية لبيانات الموازنة. في علامة تبويب **البيانات**، في مجموعة **اتصالات**، انقر فوق **"تحديث الكل"**، ثم انقر فوق **"خصائص الاتصال"**. انقر فوق علامة تبويب **الاستخدام**. ضمن **تحديث**، حدد خانة الاختيار **تحديث البيانات عند فتح الملف**. 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

