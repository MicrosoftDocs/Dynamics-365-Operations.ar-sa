---
title: تحسين أداء حلول التقارير الإلكترونية‬ عن طريق إضافة مصادر بيانات الحقول المحسوبة ذات معلمات
description: توضح هذه المقالة كيف يمكنك المساعدة على تحسين أداء حلول التقارير الإلكترونية عن طريق إضافة مصادر بيانات الحقول المحسوبة ذات المعلمات.
author: kfend
ms.date: 04/23/2021
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
ms.openlocfilehash: 34bb7c6256994f103c4da599157c06bd9d0795ef
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288247"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a>تحسين أداء حلول التقارير الإلكترونية‬ عن طريق إضافة مصادر بيانات الحقول المحسوبة ذات معلمات

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيف يمكنك أخذ [تتبعات الأداء](trace-execution-er-troubleshoot-perf.md) لتنسيقات [التقارير الإلكترونية](general-electronic-reporting.md) التي يتم تشغيلها، ثم استخدام المعلومات من هذه التتبعات للمساعدة على تحسين الأداء عن طريق تكوين مصدر بيانات **حقل محسوب** ذي المعلمات.

كجزء من عملية تصميم تكوينات التقارير الإلكترونية لإنشاء مستندات إلكترونية، يمكنك تحديد الطريقة المستخدمة لاسترداد البيانات من التطبيق وإدخالها في الإخراج الذي تم إنشاؤه. ومن خلال تصميم مصدر بيانات تقارير إلكترونية ذي معلمات من نوع **الحقل المحسوب**، يمكنك تقليل عدد استدعاءات قاعدة البيانات، والتخفيف بشكل ملحوظ من الوقت والتكلفة في جمع تفاصيل تنفيذ تنسيق التقارير الإلكترونية.

## <a name="prerequisites"></a>المتطلبات الأساسية

- لإكمال الأمثلة الموجودة في هذه المقالة، يجب أن يكون لديك حق الوصول إلى [المناصب التالية](../sysadmin/tasks/assign-users-security-roles.md):

    - مطور إعداد التقارير الإلكتروني
    - مستشار وظيفي لإعداد التقارير الإلكتروني
    - مسؤول النظام

- يجب تعيين الشركة علي **DEMF**.
- اتبع الخطوات الموجودة في [ملحق 1](#appendix1) لهذه المقالة لتنزيل مكونات العينة الخاصة بحل التقارير الإلكترونية من Microsoft المطلوبة لإكمال الأمثلة في هذه المقالة.
- اتبع الخطوات الموجودة في [ملحق 2](#appendix2) في هذه المقالة لتكوين الحد الأدنى لمجموعة معلمات التقارير الإلكترونية المطلوبة لاستخدام إطار عمل التقارير الإلكترونية للمساعدة على تحسين أداء العينة الخاصة بحل التقارير الإلكترونية من Microsoft.

## <a name="import-the-sample-er-solution"></a>استيراد عينة حل التقارير الإلكترونية

افترض انه يتعين عليك تصميم حل للتقارير الإلكترونية لإنشاء تقرير جديد يُظهر حركات المورّد. في الوقت الحالي، يمكنك العثور علي حركات مورّد محدد في صفحة **حركات المورّدين‬** (انتقل إلى **الحسابات الدائنة** \> **المورّدون** \> **جميع المورّدين**، حدد مورّدًا ، ثم على جزء الإجراءات، على علامة تبويب **المورّد** في مجموعة **الحركات**، حدد **الحركات**). ومع ذلك، تريد أن تضع معًا جميع حركات المورّدين في مستند إلكتروني واحد بتنسيق XML. سيتألف هذا الحل من العديد من تكوينات التقارير الإلكترونية التي تحتوي على مكونات نموذج البيانات والتعيين ومكونات التنسيق المطلوبة.

الخطوة الأولى هي استيراد عينة حل التقارير الإلكترونية لإنشاء تقرير لحركات المورّدين.

1. سجل دخولك إلى مثيل 365 Finance Microsoft Dynamics الذي تم تقديمه لشركتك.
2. في هذه المقالة، ستقوم بإنشاء تكوينات لعينة شركة **Litware, Inc.** وتعديلها. تأكد من إضافة موفر التكوين هذا إلى مثيل Finance ومن وضع علامة عليه كنشط. لمزيد من المعلومات، راجع [إنشاء موفري التكوين ووضع علامة عليهم كنشطين](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. في مساحة عمل **إعداد التقارير الإلكترونية**، حدد الإطار المتجانب **تكوينات إعداد التقارير**.
4. في صفحة **التكوينات**، قم باستيراد تكوينات التقارير الإلكترونية التي قمت بتنزيلها كشرط مسبق إلى Finance، بالترتيب التالي: نموذج البيانات، وبيانات التعريف، وتعيين النموذج، والتنسيق. بالنسبة لكل تكوين، اتبع هذه الخطوات:

    1. في جزء الإجراءات، حدد **التبادل** \> **تحميل من ملف XML**.
    2. حدد **استعراض**، وحدد الملف المناسب لتكوين التقارير الإلكترونية المطلوب بتنسيق XML.
    3. حدد **موافق**.

![التكوينات المستوردة على صفحة التكوينات.](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a>مراجعة عينة حل التقارير الإلكترونية

### <a name="review-the-model-mapping"></a>مراجعة تعيين النموذج

1. في صفحة **التكوينات**، في شجرة التكوين، وسَّع **نموذج تحسين الأداء**، ثم حدد **تعيين تحسين الأداء**.
2. في جزء الإجراءات، حدد **المصمم**.
3. في صفحة **تعيين النموذج إلى مصدر البيانات** في جزء الإجراءات، حدد **المصمم**.

    يتم تصميم تعيين نموذج إعداد التقارير الإلكترونية لتنفيذ الإجراءات التالية:

    - إحضار قائمة حركات المورّدين المخزنة في الجدول VendTrans (مصدر البيانات **Trans**).
    - لكل حركة، يمكنك إحضار، من الجدول VendTable، سجل مورّد تم ترحيل الحركة له (مصدر البيانات **\#‎Vend**).

    > [!NOTE]
    > يتم تكوين مصدر البيانات **\#Vend** لإحضار سجل المورّد المناظر باستخدام علاقة واحد إلى متعدد الموجودة **\@.'\>Relations'.VendTable\_AccountNum**.

    يقوم تعيين النموذج في هذا التكوين بتنفيذ نموذج البيانات الأساسي لأي من تنسيقات التقارير الإلكترونية التي تم إنشاؤها لهذا النموذج وتم تشغيلها في Finance. نتيجة لذلك، يتم كشف محتوى مصدر البيانات **Trans** لتنسيقات التقارير الإلكترونية مثل مصادر البيانات المجردة **النموذج**.

    ![مصدر البيانات Trans في صفحة مصمم تعيين النموذج.](media/er-calculated-field-ds-performance-mapping-1.png)

4. أغلق صفحة **مصمم تعيين النموذج**.
5. أغلق صفحة **تعيين النموذج إلى مصدر البيانات**.

### <a name="review-format"></a>مراجعة التنسيق

1. في صفحة **التكوينات**، في شجرة التكوين، وسَّع **نموذج تحسين الأداء**، ثم حدد **تنسيق تحسين الأداء**.
2. في جزء الإجراءات، حدد **المصمم**.
3. في الصفحة **مصمم التنسيق**، على علامة التبويب **التعيين**، حدد **توسيع/طي**.
4. قم بتوسيع عناصر **النموذج**، و **البيانات**، و **الحركة**.

    تم تصميم تنسيق التقارير الإلكترونية هذا لإنشاء تقرير حركات المورّد بتنسيق XML.

    ![مصادر بيانات التنسيق والروابط المكونة لعناصر التنسيق في صفحة مصمم التنسيق.](media/er-calculated-field-ds-performance-format.png)

5. أغلق صفحة **مصمم المعادلة**.

## <a name="run-the-sample-er-solution-to-trace-execution"></a>تشغيل حل التقارير الإلكترونية لتتبع التنفيذ

تخيّل أنك انتهيت من تصميم الإصدار الأول لحل التقارير الإلكترونية. وتريد الآن اختبار الحل في مثيل Finance وتحليل أداء التنفيذ.

### <a name="turn-on-the-er-performance-trace"></a>تشغيل تتبع أداء التقارير الإلكترونية

1. قم بتحديد شركة **DEMF**.
2. اتبع الخطوات في [تشغيل تتبع أداء التقارير الإلكترونية‬](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) لإنشاء تتبع أداء أثناء تشغيل تنسيق التقارير الإلكترونية.

    ![مربع حوار معلمات المستخدمين.](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a>تشغيل تنسيق التقارير الإلكترونية

1. انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.
2. في صفحة **التكوينات**، في شجرة التكوين، حدد **تنسيق تحسين الأداء**.
3. في جزء الإجراءات، حدد **تشغيل**.

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a>استخدام تتبع الأداء لتحليل أداء تعيين النموذج

1. في صفحة **التكوينات**، في شجرة التكوين، حدد **تعيين تحسين الأداء**.
2. في جزء الإجراءات، حدد **المصمم**.
3. في صفحة **تعيينات النموذج** في جزء الإجراءات، حدد **المصمم**.
4. في صفحة **مصمم تعيين النموذج**، في جزء الإجراءات، حدد **تتبع الأداء**.
5. حدد أحدث التتبعات التي تم إنشاؤها، ثم حدد **موافق**.

تتوفر الآن معلومات جديدة تصبح لبعض عناصر مصدر البيانات لتعيين النموذج الحالي:

- الوقت الفعلي الذي استغرقه إحضار البيانات باستخدام مصدر البيانات
- نفس الوقت معبر عنه كنسبة مئوية من إجمالي الوقت المستغرق في تشغيل تعيين النموذج بالكامل

![تفاصيل وقت التنفيذ على صفحة مصمم تعيين النموذج.](./media/er-calculated-field-ds-performance-mapping-2.png)

تُظهر شبكة **إحصائيات الأداء** أن مصدر البيانات **Trans** يستدعي الجدول VendTrans مرة واحدة. تشير القيمة **\[265\]\[Q:265\]** لمصدر البيانات **Trans** إلى إحضار حركات المورّد 265 من جدول التطبيق وتم إرجاعها إلى نموذج البيانات.

وتُظهر أيضًا شبكة **إحصائيات الأداء** أن تعيين النموذج الحالي يكرر طلبات قاعدة البيانات أثناء تشغيل مصدر البيانات **\#Vend**. يحدث هذا التكرار للأسباب التالية:

- يتم استدعاء جدول المورّد مرتين لكل حركة من حركات المورّد المكررة 265، لإجمالي 530 استدعاء:

    - يتم إجراء استدعاء واحد لإدخال رقم حساب المورّد.
    - يتم إجراء استدعاء واحد لإدخال اسم المورّد.

- ويتم استدعاء جدول المورّد لكل حركة من حركات المورّد المكررة، على الرغم من ترحيل الحركات التي تم إحضارها لخمسة مورّدين فقط. من بين 530 استدعاء، هناك 525 استدعاء مكرر. يبين الرسم التوضيحي التالي الرسالة التي تتلقاها حول الاستدعاءات المكررة (طلبات قواعد البيانات).

![رسالة حول طلبات قواعد البيانات المكررة في صفحة مصمم تعيينات النماذج.](./media/er-calculated-field-ds-performance-mapping-2a.png)

بالنسبة للوقت الإجمالي لتنفيذ تعيين النموذج (ثماني ثوان تقريبًا)، يمكنك الملاحظة أنه تم قضاء 80 بالمئة (ست ثوانٍ تقريبًا) في استرداد القيم من جدول التطبيق VendTable. هذه النسبة المئوية كبيرة جدًا لسمتين من خمسة مورّدين، مقارنةً بحجم المعلومات من جدول التطبيق VendTrans.

لتقليل عدد الاستدعاء التي يتم اجراؤها للحصول على تفاصيل المورّد لكل حركة، ولتحسين أداء تعيين النموذج، يمكنك استخدام التخزين المؤقت لمصدر البيانات **\#Vend**.

> [!NOTE]
> سيتم تخزين مصدر البيانات **Trans\\\#Vend** بشكل مؤقت في نطاق الحركة الحالية لمصدر البيانات **Trans** في وقت التشغيل.

ومن خلال التخزين المؤقت لمصدر البيانات **\#Vend**، ستقوم بتقليل عدد الاستدعاءات المكررة من 525 إلى 260، ولكن دون إزالة التكرار بشكل كامل. لإزالة التكرار بشكل كامل، يمكنك تكوين مصدر بيانات جديد ذي معلمات من نوع **الحقل المحسوب**.

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>تحسين تعيين النموذج استنادًا إلى المعلومات الواردة من تتبع التنفيذ

### <a name="change-the-logic-of-the-model-mapping"></a>تغيير منطق تعيين النموذج

اتبع الخطوات التالية لاستخدام التخزين المؤقت ومصدر بيانات من نوع **الحقل المحسوب**، للمساعدة على منع الاستدعاءات المكررة لقاعدة البيانات.

1. في صفحة **التكوينات**، في شجرة التكوين، حدد **تعيين تحسين الأداء**.
2. في جزء الإجراءات، حدد **المصمم**.
3. في صفحة **تعيينات النموذج** في جزء الإجراءات، حدد **المصمم**.
4. في صفحة **مصمم تعيين النموذج**، اتبع هذه الخطوات لإضافة مصدر بيانات من نوع **سجلات الجدول** للوصول إلى السجلات في جدول تطبيق VendTable:

    1. في الجزء **أنواع مصادر البيانات**، قم بتوسيع **Dynamics 365 for Operations**، وحدد **سجلات البيانات**.
    2. حدد **إضافة جذر**.
    3. في مربع الحوار، في الحقل **الاسم**، أدخل **Vend**.
    4. في حقل **الجدول**، أدخل **VendTable‎‎**.
    5. حدد **موافق**.

5. يمكن تعيين معلمات لاستدعاءات مصادر البيانات من نوع **الحقل المحسوب** الحقل إذا كانت مصادر البيانات هذه موجودة في حاوية. وبالتالي، اتبع الخطوات التالية لإضافة مصدر بيانات من نوع **الحاوية الفارغة** لاحتواء مصدر بيانات جديد ذي معلمات من نوع **الحقل المحسوب**:

    1. في الجزء **أنواع مصادر البيانات**، قم بتوسيع **عام** وحدد **حاوية فارغة**.
    2. حدد **إضافة جذر**.
    3. في مربع الحوار، في الحقل **الاسم**، أدخل **المربع**.
    3. حدد **موافق**.

    ![مصدر البيانات مربع في صفحة مصمم تعيين النموذج.](./media/er-calculated-field-ds-performance-mapping-3.png)

6. اتبع الخطوات التالية لإضافة مصدر بيانات ذي معلمات من نوع **الحقل المحسوب**:

    1. حدد **المربع** في جزء **مصادر البيانات** .
    2. في جزء **انواع مصادر البيانات**، قم بتوسيع عنصر **الوظائف**، وحدد **الحقل المحسوب**.
    3. حدد **إضافة**.
    4. في مربع الحوار، في الحقل **الاسم**، أدخل **Vend**.
    5. حدد **تحرير المعادلة**.
    6. في الصفحة **مصمم المعادلة**، حدد **المعلمات** لتحديد المعلمات التي يجب توفيرها عند استدعاء مصدر البيانات هذا.
    7. في مربع الحوار **المعلمات**، حدد **جديد**.
    8. في حقل **الاسم**، أدخل **parmVendAccNumber**.
    9. في حقل **النوع**، حدد **سلسلة**.
    10. حدد **موافق**.
    11. في حقل **المعادلة**، أدخل **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.
    12. حدد **حفظ** وأغلق صفحة **مصمم المعادلة**.
    13. حدد **موافق** لإضافة مصدر البيانات الجديد.

7. اتبع الخطوات التالية لوضع علامة على مصدر البيانات على أنه مخزن مؤقتًا أثناء التنفيذ:

    1. في جزء **مصادر البيانات**، حدد **Box\\Vend**.
    2. حدد **ذاكرة التخزين المؤقت**.

    > [!NOTE]
    > سيتم تخزين مصدر البيانات **Box\\Vend** بشكل مؤقت في نطاق جميع حركات المورّدين لمصدر البيانات **Trans** في وقت التشغيل.

8. اتبع هذه الخطوات لتحديث مصدر البيانات **Trans\\\#Vend** المتداخل بحيث يستخدم مصدر البيانات **Box\\Vend**:

    1. في جزء **مصادر البيانات**، قم بتوسيع **Trans** .
    2. حدد مصدر البيانات **Trans\\\#Vend**، ثم حدد **تحرير** \> **تحرير المعادلة**.
    3. في الصفحة **مصمم المعادلة**، في حقل **المعادلة‏‎**، أدخل **Box.Vend(\@.AccountNum)**.
    4. حدد **حفظ**، ثم أغلق صفحة **مصمم المعادلة**.
    5. حدد **موافق** لإكمال التغييرات التي أجريتها في مصدر البيانات المحدد.

9. حدد **حفظ**.

    ![مصدر البيانات Vend في صفحة مصمم تعيين النموذج.](./media/er-calculated-field-ds-performance-mapping-4.png)

10. أغلق صفحة **مصمم تعيين النموذج**.
11. أغلق صفحة **تعيينات النماذج**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>إكمال الإصدار المعدل من تعيين طراز التقارير الإلكترونية

1. في صفحة **التكوينات**، في علامة التبويب السريعة **الإصدارات**، حدد الإصدار **1.2** في تكوين **تعيين تحسين الأداء**.
2. حدد **تغيير الحالة** \> **إكمال**، ثم حدد **موافق**.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>تشغيل حل التقارير الإلكترونية المعدل لتتبع التنفيذ

كرر الخطوات الموجودة في قسم [تشغيل تنسيق التقارير الإلكترونية](#run-format) المذكور من قبل في هذه المقالة لإنشاء تتبع أداء جديد.

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a>استخدام تتبع الأداء لتحليل التعديلات في تعيين النموذج 

1. في صفحة **التكوينات**، في شجرة التكوين، حدد **تعيين تحسين الأداء**.
2. في جزء الإجراءات، حدد **المصمم**.
3. في صفحة **تعيينات النموذج** في جزء الإجراءات، حدد **المصمم**.
4. في صفحة **مصمم تعيين النموذج**، في جزء الإجراءات، حدد **تتبع الأداء**.
5. حدد أحدث التتبعات التي تم إنشاؤها، ثم حدد **موافق**.

لاحظ أن التسويات التي أجريتها على تعيين النموذج قد تقوم بإزالة الاستعلامات المكررة لقاعدة البيانات. يتم أيضًا تقليل عدد الاستدعاءات إلى جداول قاعدة البيانات ومصادر البيانات لتعيين هذا النموذج.

![تتبع المعلومات في صفحة مصمم تعيين النموذج 1.](./media/er-calculated-field-ds-performance-mapping-5.png)

تم تقليل وقت التنفيذ الإجمالي حوالي 20 مرة (من 8 ثوان إلى حوالي 400 مللي ثانية). وبالتالي، تم تحسين أداء حل التقارير الإلكترونية بالكامل.

![تتبع المعلومات في صفحة مصمم تعيين النموذج 2.](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a>الملحق 1: تنزيل مكونات عينة حل التقارير الإلكترونية من Microsoft

يجب عليك تنزيل الملفات التالية وتخزينها محليًا.

| ملف                                        | المحتوى |
|---------------------------------------------|---------|
| تحسين الأداء model.version.1     | [تكوين نموذج عينة بيانات التقارير الإلكترونية](https://download.microsoft.com/download/4/6/f/46f0f3fa-782b-414a-8f7b-b6c64a388661/Performance_improvement_model.version.1.xml) |
| تحسين الأداء mapping.version.1.1 | [تكوين تعيين نموذج عينة التقارير الإلكترونية](https://download.microsoft.com/download/8/9/1/8913a763-afb8-4bf4-aaf1-95ad793ffc5a/Performance_improvement_mapping.version.1.1.xml) |
| تحسين الأداء format.version.1.1  | [تكوين تنسيق عينة التقارير الإلكترونية](https://download.microsoft.com/download/9/0/c/90c75963-bc78-4edc-9096-556bbe281f10/Performance_improvement_format.version.1.1.xml) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a>الملحق 2: تكوين إطار عمل التقارير الإلكترونية

قبل أن تتمكن من بدء استخدام اطار عمل التقارير الإلكترونية لتحسين أداء عينة حل التقارير الإلكترونية من Microsoft‬، يجب عليك تكوين الحد الأدنى لمجموعة معلمات التقارير الإلكترونية.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>تكوين معلمات التقارير الإلكترونية

1. انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.
2. في الصفحة **تكوينات الترجمة**، في قسم **الارتباطات المتعلقة**، حدد **معلمات التقارير الإلكترونية**.
3. في صفحة **معلمات التقارير الإلكترونية**، على علامة التبويب **عام**، عيّن الخيار **تمكين وضع التصميم** إلى **نعم**.
4. في علامة التبويب **المرفقات**، عيّن المعلمات التالية:

    - في حقل **التكوينات**، حدد نوع **الملف** لشركة **DEMF**.
    - في حقول **أرشيف الوظيفة** و **المؤقت** و **الأساس** و **أخرى**، حدد نوع **الملف**.

لمزيد من المعلومات حول معلمات ER ، راجع [تكوين إطار عمل ER](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>تنشيط موفر تكوين ER

يتم تعليم كل تكوين ER تمت إضافته باعتباره مملوكا لموفر تكوين ER. يتم استخدام موفر تكوين ER الذي تم تنشيطه في مساحة عمل **التقارير الإلكترونية** لهذا الغرض. بالتالي، يجب عليك تنشيط موفر تكوين ER في مساحة عمل **التقارير الإلكترونية** قبل البدء في إضافة تكوينات ER أو تحريرها.

> [!NOTE]
> يمكن لمالك تكوين التقارير الإلكترونية فقط تحرير التكوين. بالتالي، قبل تحرير تكوين ER، يجب تنشيط موفر تكوين ER المناسب في مساحة عمل **التقارير الإلكترونية**.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>مراجعة قائمة موفري تكوين ER

1. انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.
2. في الصفحة **تكوينات الترجمة**، في قسم **الارتباطات المتعلقة**، حدد **موفري التكوين** .
3. في صفحة **جدول موفري التكوين**، يتضمن كل سجل موفر اسمًا وعنوان URL فريدين. راجع محتويات هذه الصفحة. في حالة وجود سجل **Litware, Inc.**، يمكنك تخطي الإجراء التالي [إضافة موفر تكوين تقارير إلكترونية جديد](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>إضافة موفر تكوين ER جديد

1. انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.
2. في الصفحة **تكوينات الترجمة**، في قسم **الارتباطات المتعلقة**، حدد **موفري التكوين** .
3. في صفحة **موفري التكوين**، حدد **جديد**.
4. في حقل **الاسم**، أدخل **Litware, Inc**.
5. في الحقل **عنوان الإنترنت**، أدخل `https://www.litware.com`.
6. حدد **حفظ**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>تنشيط موفر تكوين ER

1. انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.
2. في صفحة **تكوينات التعريب**، في القسم **موفري التكوين**، حدد تجانب **Litware, Inc.** ثم حدد **تعيين نشط**.

لمزيد من المعلومات حول موفري تكوين ER، راجع [إنشاء موفري التكوين ووضع علامة عليهم كنشطين](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="additional-resources"></a>الموارد الإضافية

- [نظرة عامة حول التقارير الإلكترونية](general-electronic-reporting.md)
- [تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها](trace-execution-er-troubleshoot-perf.md)
- [دعم استدعاءات ذات معلمات لمصادر بيانات التقارير الإلكترونية لنوع الحقل المحسوب‬](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
