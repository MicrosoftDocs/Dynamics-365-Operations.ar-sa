---
title: مسجل المهام ونظام التعليمات لكل من Retail Modern POS (MPOS) وCloud POS
description: يصف هذا المقال كيفية استخدام مسجل المهام في كل من Retail Modern POS وCloud POS.
author: josaw1
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.industry: Retail
ms.search.form: RetailTerminalTable, SystemParameters
ms.openlocfilehash: 32d5c959c044a628a6ed1044b6e30f3363680293
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267448"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a>مسجل المهام ونظام التعليمات لكل من Retail Modern POS (MPOS) وCloud POS

[!include [banner](includes/banner.md)]

يصف هذا المقال كيفية استخدام مسجل المهام في كل من Retail Modern POS وCloud POS.

## <a name="overview"></a>نظرة عامة

يُعتبر مسجل المهام في Retail Modern POS أو Cloud POS حلاً جديدًا تم بناؤه مع التركيز على الاستجابة العالية. إنه يوفر واجهة برمجة تطبيقات مرنة (API) مرنة لقابلية التوسعة والتكامل السلس مع عملاء لديهم تسجيلات لعمليات الأعمال. بالإضافة إلى ذلك، تم تقديم تكامل مسجل المهام مع أداة تكوين عمليات الأعمال (BPM) على Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)). لذلك، سيتمكن المستخدمون من متابعة إنتاج رسومات تخطيطية لعمليات الأعمال من التسجيلات إلى تحليل تطبيقاتهم وتصميمها.

## <a name="architecture"></a>الهندسة

باستطاعة مسجل المهام تسجيل إجراءات المستخدم في العميل بنفس الدقة. تم تجهيز كل عنصر تحكم لإعلام مسجل المهام عن تنفيذ إجراء من قبل المستخدم. يقوم عنصر التحكم بإعلام مسجل المهام بوقوع حدث ما، ويقوم بتمرير كافة المعلومات ذات الصلة حول إجراء المستخدم المناظر في الوقت الحقيقي. من خلال هذه المعلومات، يستطيع مسجل المهام التقاط نوع إجراء المستخدم (مثل النقر فوق الزر أو إدخال قيمة، أو التنقل) وأي بيانات مرتبطة بإجراء المستخدم (مثل قيمة بيانات الإدخال أو سياق النموذج أو سياق السجل). يلتزم مسجل المهام بالمعلومات مع تفاصيل كافية للمساعدة في ضمان قيام تشغيل التسجيل بتنفيذ الإجراءات المسجلة تمامًا كما نفذها المستخدم. (لم يتم بعد تطبيق ميزة التشغيل في نقطة بيع التجزئة الحديثة أو نقطة بيع المجموعة.)

## <a name="basic-configuration"></a>التكوين الأساسي

لتمكين تسجيل المهام في نقطة البيع، اتبع الخطوات التالية.

1. انقر فوق  **البيع بالتجزئة والتجارة** &gt; **إعداد القناة** &gt; **إعداد نقطة البيع** &gt; **السجلات**.
2. انقر فوق السجل لتمكين تسجيل المهام.
3. على علامة التبويب **سجل**، على علامة التبويب السريعة **عام**، عيّن الخيار **تمكين تسجيل المهام** إلى **نعم**.
4. انقر فوق **حفظ**.
5. انتقل إلى **Retail and Commerce** &gt; **تكنولوجيا معلومات البيع بالتجزئة والتجارة** &gt; **جدول التوزيع**.
6. حدد الوظيفة **سجلات (1090)**، ثم انقر فوق **تشغيل الآن**.

## <a name="create-a-recording"></a>إنشاء تسجيل

اتبع هذه الخطوات لإنشاء تسجيل جديد باستخدام مسجل المهام.

1. ابدأ تشغيل Retail Modern POS أو Cloud POS، وسجل دخولك.
2. في صفحة **الإعدادات**، في المقطع **مسجل المهام** ، انقر فوق **فتح مسجل المهام**. يظهر جزء **مسجل المهام**. يمكنك النقر فوق الزر **إغلاق** (**X**) في الزاوية العلوية اليسرى لإغلاق جزء **مسجل المهام** قبل بدء تسجيل جديد. لإعادة فتح الجزء، كرر الخطوة 2.

    [![جزء مسجل المهام.](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3. أدخل اسمًا ووصفًا للتسجيل، ثم انقر فوق **البدء‬**. تبدأ جلسة التسجيل بمجرد النقر فوق **البدء‬**.

    > [!NOTE]
    > إذا نقرت فوق الزر **إغلاق‏‎** (**X**) في الزاوية العلوية اليسرى بينما يكون التسجيل قيد التقدم، فسيتم إغلاق الجزء **مسجل المهام** ولكن من دون إنهاء جلسة التسجيل. لإعادة فتح جزء مسجل المهام، انقر فوق الزر **تعليمات** (علامة استفهام) في الجزء العلوي من الشاشة.
    >
    > [![علامة استفهام.](./media/help.jpg)](./media/help.jpg)

4. بعد النقر فوق **البدء**، يدخل مسجل المهام في وضع التسجيل. يعرض جزء **مسجل المهام** المعلومات وعناصر التحكم المرتبطة بعملية التسجيل.
5. نفّذ الإجراءات التي تريد تنفيذها في واجهة المستخدم في Retail Modern POS أو Cloud POS.
6. لإنهاء جلسة التسجيل، انقر فوق **إيقاف**.

## <a name="download-options"></a>خيارات التنزيل

بعد أن تقوم بإنهاء جلسة التسجيل، يظهر الكثير من الخيارات، بحيث يمكنك تنزيل التسجيل.

[![خيارات التنزيل.](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### <a name="save-to-this-pc"></a>حفظ إلى هذا الكمبيوتر الشخصي

يمكنك استخدام حزمة التسجيل لتشغيل دليل مهام أو المحافظة على التسجيل أو تحرير التعليقات التوضيحية في التسجيل. (لم يتم بعد تطبيق هذه الميزة في Retail Modern POS أو Cloud POS.)

### <a name="export-as-word-document"></a>تصدير كمستند Word

يمكنك حفظ التسجيل كمستند Microsoft Word. سوف يحتوي المستند على الخطوات المسجلة ولقطات الشاشة التي تم التقاطها.

### <a name="save-as-developer-recording"></a>حفظ كتسجيل مطور

سيكون ملف التسجيل الأولي مفيدًا لسيناريوهات المطور مثل إنشاء كود الاختبار. (لم يتم بعد تطبيق هذه الميزة.)

## <a name="recording-controls"></a>عناصر التحكم الخاصة بالتسجيل

[![عناصر التحكم الخاصة بالتسجيل.](./media/controls.jpg)](./media/controls.jpg)

### <a name="stop"></a>إيقاف

انقر فوق **إيقاف** لإنهاء جلسة التسجيل. لاحظ أنه لا يمكنك إعادة تشغيل جلسة عمل بعد إنهائها. لذلك، تأكد من إكمال التسجيل قبل إنهائه.

### <a name="pause"></a>توقف مؤقت

انقر فوق **إيقاف مؤقت** لإيقاف جلسة التسجيل مؤقتًا ومتابعة العملية. لا يتم تسجيل الخطوات التي تقوم بتنفيذها بعد النقر فوق **إيقاف مؤقت**.

### <a name="continue"></a>متابعة

لاستئناف جلسة التسجيل بعد إيقافها مؤقتًا، انقر فوق **متابعة**.

### <a name="capture-screenshots"></a>التقاط لقطات الشاشة

باستطاعة مسجل المهام التقاط لقطات الشاشة‬ لواجهة مستخدم Retail Modern POS بينما تقوم بتسجيل عملية تجارية. لتشغيل ميزة التقاط لقطات الشاشة‬، عيّن الخيار **التقاط لقطات الشاشة‬** إلى **نعم**، ثم قم بالتسجيل. بمجرد اكتمال التسجيل، انقر فوق **إيقاف** وقم بتنزيل مستند Word. سوف يحتوي المستند على الخطوات بلقطات الشاشة ذات الصلة.

> [!NOTE]
> وظيفة لقطه الشاشة غير معتمده في تجاره المتجر و POS التجارية الحديثة ونقطه السحابة.

### <a name="start-task-and-end-task"></a>بدء المهمة وإنهاء المهمة

يمكنك تحديد بداية ونهاية مجموعة من الخطوات المجمعة باستخدام الزرين **بدء المهمة‬** و **إنهاء** **المهمة**. انقر فوق **بدء المهمة** لإضافة خطوة "بدء المهمة"، ثم قم بتنفيذ الخطوات التي يجب تضمينها في المجموعة. بعد الانتهاء من تنفيذ الخطوات للمجموعة، انقر فوق **إنهاء المهمة**. تساعدك المهام في تنظيم إجراءاتك. ويمكن تضمين المهام ضمن مهام أخرى. بهذه الطريقة، يمكن تنظيم عمليات الأعمال الطويلة جدًا والبالغة التعقيد بشكل أفضل.

## <a name="adding-annotations"></a>إضافة تعليقات توضيحية

التعليق التوضيحي هو النص الإضافي الذي تضيفه إلى إحدى الخطوات في تسجيل. على سبيل المثال، يمكنك استخدام التعليقات التوضيحية لتقديم سياق إضافي أو إرشادات إضافية للمستخدم. يمكنك إضافة التعليقات التوضيحية قبل خطوة أو بعدها. يمكنك إضافة تعليق توضيحي لأي خطوة عن طريق النقر فوق الزر **تحرير** (رمز القلم) إلى يسار الخطوة.

[![الزر "تحرير" لخطوة.](./media/annotate.jpg)](./media/annotate.jpg)

### <a name="texts-and-notes"></a>النصوص والملاحظات

يمكنك استخدام الحقلين **نصوص** و **ملاحظات** لإضافة النص الذي يجب إقرانه بإحدى الخطوات في دليل مهام.

[![حقول النصوص والملاحظات.](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### <a name="text"></a>النص

يظهر النص الذي تدخله في حقل **النص** *فوق* نص الخطوة في دليل المهام. يُعتبر هذا الموقع مناسبًا للنص الذي تريد أن يقرأه المستخدم قبل أن يكمل الخطوة.

#### <a name="notes"></a>الملاحظات

يظهر النص الذي تدخله في حقل **الملاحظات** *تحت* نص الخطوة في دليل المهام. لقراءة نص الملاحظة، يجب على المستخدم توسيع نص الخطوة في النافذة المنبثقة. يُعتبر هذا الموقع مناسبًا لمواد القراءة الاختيارية أو المعلومات الأخرى التي قد تكون مفيدة للمستخدم، ولكن المستخدم لا يحتاجها لإكمال الإجراء.

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a>التعليمات في كل من Retail Modern POS وCloud POS

لإظهار تسجيلات المهام المخصصة الخاصة بك في جزء التعليمات في Retail Modern POS وCloud POS بحيث يمكن عرضها كنص، يجب عليك حفظ تسجيلات المهام إلى مكتبة BPM، ثم تحديث محددات نظام التعليمات‬ بحيث تشير إلى مكتبة BPM. لمزيد من المعلومات، راجع [الاتصال بنظام التعليمات](../fin-ops-core/fin-ops/get-started/help-connect.md). يبحث نظام التعليمات في Retail Modern POS وCloud POS في LCS في‬ الوقت الحقيقي. وهو يبحث عبر كافة مكتبات BPM التي تم تحديدها في محددات نظام تعليمات Commerce ويعرض النتائج ذات الصلة. للوصول إلى القائمة **تعليمات**، انقر فوق الزر **تعليمات** (علامة الاستفهام) في الجزء العلوي من الشاشة، ثم اكتب اسم عمليتك في مربع البحث واضغط الزر بحث.

[![الزر تعليمات.](./media/help.jpg)](./media/help.jpg)

عندما تنقر فوق دليل مهام في نتائج البحث، يمكنك عرض الخطوات كمقال تعليمات أو تصدير الخطوات إلى مستند Word.

> [!NOTE]
> لن يعرض نظام التعليمات في Retail Modern POS وCloud POS‬ دلائل المهام وفقًا للنموذج الذي تعمل عليه أو العملية التي تعمل على تنفيذها. يجب عليك كتابة اسم العملية في مربع البحث والنقر فوق **بحث**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
