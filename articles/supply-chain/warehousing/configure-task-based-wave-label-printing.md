---
title: جدولة طباعة بطاقات الموجة أثناء الموجة
description: يوضح هذا الموضوع كيفية إعداد وظيفة طباعة تسمية الموجة المستندة إلى المهام واستخدامها.
author: MSFTGarm
ms.date: 06/09/2021
ms.topic: article
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-obaranov
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 32842c32599b3ca5d84cc9f715a1453d55e176dc
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301876"
---
# <a name="schedule-wave-label-printing-during-wave"></a>جدولة طباعة بطاقات الموجة أثناء الموجة

[!include [banner](../../includes/banner.md)]

استخدم الميزة *طباعة تسمية الموجة المستندة إلى المهام* كجزء من عملية إنشاء الموجات الخاصة بك للمساعدة في تحسين الكفاءة، ولجعل النظام يقوم بإنشاء تسميات الموجات والعمل في مهام منفصلة.

تعتبر عملية تكوين طباعة تسمية الموجة أمرًا معقدًا وتعتمد على التكوين الدقيق والبيانات الرئيسية. لا يكون غير شائع لإنشاء سجلات تسميات الموجة للفشل، وعند القيام بذلك، يتم التراجع عن معالجة الموجة بالكامل. تساعد الميزة *طباعة تسمية الموجة المستندة إلى المهام* في تجنب الحاجة إلى إعادة إنشاء العمل وبنود العمل في كل مرة يتم فيها طباعة تسمية الموجة بشكل غير صحيح.

عند استخدام الميزة *طباعة تسمية الموجة المستندة إلى المهام*، يقوم النظام أولاً بإنشاء العمل وبنود العمل. ثم يقوم بإنشاء تسميات الموجة وطباعتها. وأخيرًا، إذا كانت تسميات الموجات تم إنشاؤها بشكل صحيح، فإنها تصدر العمل والموجة للانتقاء.

## <a name="turn-on-the-task-based-wave-label-printing-feature-in-feature-management"></a>تشغيل ميزة طباعة تسمية الموجة المستندة إلى المهام في إدارة الميزات

لاستخدام الميزات الموضحة في هذا الموضوع، يجب تشغيلها للنظام الخاص بك. استخدم مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيل الميزات في الأمر التالي:

1. *طباعة تسمية الموجة* – هذه الميزة مطلوبة لتمكين أسلوب معالجة الموجة لطباعة بطاقة الموجة.
1. *حظر العمل على مستوى المؤسسة‬* – هذه الميزة مطلوبة لكل من التكوين اليدوي والتلقائي لإنشاء العمل المجدول.
1. *طباعة تسمية الموجة المستندة إلى المهام* – هذه الميزة مطلوبة لتقسيم طباعة تسمية الموجة إلى نطاق حركة منفصل.

## <a name="manually-enable-the-new-wave-step-method"></a>تمكين الطريقة الجديدة لخطوة الموجة يدويًا

يجب عليك أولاً إنشاء طريقة جديدة لخطوة الموجة وتمكينها لمعالجة المهام غير المتزامنة المتوازية.

1. انتقل إلى  **إدارة المستودعات \> إعداد \> الموجات \> أساليب عملية الموجة**.
1. في جزء الإجراءات، حدد **طريقة إعادة الإنشاء**. لاحظ أنه تتم إضافة *waveLabelPrinting* إلى قائمة أساليب معالجة الموجة التي يمكنك استخدامها في قوالب موجة الشحن الخاصة بك.
1. حدد السجل الذي يتم فيه تعيين الحقل **اسم الطريقة** إلى *waveLabelPrinting*، ثم في جزء الإجراءات، حدد **تكوين المهمة**.
1. في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة. ثم قم بتعيين الحقول التالية للصف الجديد:

    - **المستودع** – حدد المستودع الذي ستستخدمه لجدولة معالجة إنشاء العمل. (إذا كنت تستخدم البيانات التوضيحية لأغراض الاختبار، يمكنك تحديد المستودع *24*.)
    - **الحد الأقصى لعدد مهام المجموعات** – تحديد الحد الأقصى لعدد مهام الدفعات. في معظم الحالات، يجب أن تكون القيمة من *8* إلى *16*. ومع ذلك، نُوصي بالتجربة لإيجاد الإعداد الأمثل للسيناريوهات الخاصة بك.
    - **مجموعه الدفعة لمعالجة الموجة** - حدد مجموعة دفعات مخصصة لمعالجة الموجات لتحسين معالجة قائمة انتظار الدفعات الخاصة بك.

يمكنك الآن تحديث قالب موجة موجود بحيث يستخدم أسلوب معالجة الموجة *طباعة تسمية الموجة*. وبدلاً من ذلك، يمكنك إنشاء قالب موجة جديد يستخدمه.

1. انتقل إلى  **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجة**.
1. في جزء الإجراءات، حدد **تحرير**.
1. في جزء القائمة، حدد قالب الموجة المراد تحديثه. (إذا كنت تستخدم البيانات التوضيحية لأغراض الاختبار، يمكنك تحديد *افتراضي الشحن 24*.)
1. في علامة التبويب السريعة **الطريق**، في العمود **الطرق المتبقية**، حدد الصف الذي تم فيه تعيين حقل **الاسم** إلى *waveLabelPrinting*.
1. حدد **إضافة** (زر سهم لليمين) لنقل الصف المحدد إلى العمود **الطرق المحددة**.
1. في الحقل **رمز خطوة الموجة**، أدخل رمز خطوة الموجة الذي سيتم استخدامه لربط قالب الموجة بقالب تسمية الموجة.

## <a name="set-wave-task-processing-threshold-data"></a>تعيين بيانات عتبه معالجه المهمة الموجهة

في المرة الأولى التي يتم فيها تشغيل عملية موجة باستخدام أية معالجة تستند إلى المهام، سيقوم النظام بإنشاء بيانات حد معالجة المهام الموجهة الافتراضية . يتم استخدام هذه البيانات للتحكم في الوقت الذي سيتم فيه تشغيل معالجة الموجات بشكل غير متزامن وتستند إلى المهام، مما يعمل على تمكين تسميات الموجة وإنشائها بالتوازي.

ستقوم البيانات الافتراضية في البداية باستخدام قيمه الحد *1* للحد الأدنى لعدد معرفات العمل (`MinimumWorkThresholdForLabelPrinting`). وبالتالي، عندما يقوم النظام بمعالجة موجة تحتوي على أكثر من معرف عمل واحد، فإنه سيستخدم معالجة تستند إلى المهام لتسميات الموجة في حركة منفصلة. يمكنك إدراج أو تحديث هذه البيانات في جدول `WHSWaveTaskProcessingThresholdParameters` في بيئات الاختبار الخاصة بك يدويًا. لتغيير الإعداد في بيئة الإنتاج، فيجب عليك الاتصال بدعم Microsoft لطلب التحديث.

## <a name="changes-to-the-wave-processing-logic-when-task-based-wave-label-printing-is-used"></a>تغيير منطق معالجة الموجة عند استخدام طباعة تسمية الموجة المستندة إلى المهام

إذا كانت معالجة تسمية الموجة تتجاوز حد معالجة مهمة الموجة، يتم بدء المعالجة المستندة إلى المهام. في المعالجة التالية للموجة والتي تلائم قالب الموجة، سيتم تشغيل طباعة تسمية الموجة في حركة *ttsbegin*/*ttscommit* مستقلة على الفور بعد إنشاء العمل. إذا تم تكوين إصدار العمل (إلغاء الحظر) على قالب الموجة للتشغيل تلقائيًا، فإنه يحدث فقط بعد إكمال عملية طباعة تسمية الموجة بنجاح.

في حالة فشل إنشاء تسمية الموجة (على سبيل المثال، في حالة فشل تحويل كمية العمل إلى كمية تسمية الموجة وعرض خطأ)، تفشل الحركة الملائمة فقط. يظل العمل الذي تم إنشاؤه سابقًا مجمدًا. لتصحيح الأخطاء وطباعة تسميات الموجة، اتبع الخطوات التالية.

1. انتقل إلى **إدارة المستودعات \> الموجات الصادرة‬ \> موجات الشحنة‬ \> كافة الموجات‬**.
1. حدد الموجة ذات الصلة في الشبكة.
1. في جزء الإجراءات، في علامة التبويب **الموجة**، في المجموعة **طباعة‏‎‬**، حدد **تسميات الموجات**.
1. اتبع الإرشادات التي تظهر على الشاشة لإرسال التسميات للطباعة.
1. في جزء الإجراءات، ضمن علامة التبويب **الموجة**، في المجموعة **موجة**، حدد **إصدار** لتحرير العمل للموجة المحددة يدويًا.

## <a name="additional-resources"></a>الموارد الإضافية

- [طباعة تسمية الموجة](configure-wave-label-printing.md)
- [جدولة إنشاء العمل أثناء الموجة](configure-wave-schedule-work-creation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]