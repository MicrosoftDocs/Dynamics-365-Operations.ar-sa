---
title: تقييم نموذج التوقع بالدفع الأولي للعميل
description: تصف هذه المقالة الخطوات التي يمكنك اتخاذها لفهم نموذج التوقع لمدفوعات العميل وتقييم الفعالية الخاصة به.
author: ShivamPandey-msft
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: fcdf276505cf58267a38e9d6174a155ad307653b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846991"
---
# <a name="evaluate-the-initial-customer-payment-prediction-model"></a>تقييم نموذج التوقع بالدفع الأولي للعميل

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية تقييم نموذج التوقع بعد تشغيل Finance Insights ثم إنشاء النموذج الأول وتدريبه. تتناول هذه المقالة نماذج التوقع بمدفوعات العميل. إنه يصف الخطوات التي يمكنك اتخاذها لفهم نموذج التوقع بدفع العميل وتقييم الفعالية الخاصة به.

## <a name="getting-details-about-the-model"></a>الحصول على تفاصيل حول النموذج

في الصفحة **معلمات Finance Insights** في Microsoft Dynamics 365 Finance، يظهر ارتباط **تحسين دقة النموذج** بجوار درجة الدقة.

[![تحسين ارتباط دقة النموذج.](./media/prediction-model.png)](./media/prediction-model.png)

ينقلك هذا الارتباط إلى AI Builder، حيث يمكنك معرفة المزيد حول النموذج الحالي وأيضًا اتخاذ خطوات لتحسينه. يبين الشكل التوضيحي التالي الصفحة التي يتم فتحها.

[![AI Builder.](./media/what-to-predict.png)](./media/what-to-predict.png)

تبين الصفحة التي يتم فتحها المعلومات التالية:

- في القسم **الأداء**، توفر درجة أداء النموذج منظورًا لجودة النموذج. لمزيد من المعلومات حول هذه الدرجة، راجع [أداء نموذج التنبؤ](/ai-builder/prediction-performance) في وقائق AI Builder.
- يعرض القسم **البيانات الأكثر تأثيرًا** مدى أهمية اختلاف أنواع الإدخال المختلفة للنموذج الخاص بك. يمكنك تقييم هذه القائمة والنسب المئوية المقابلة لها لتحديد ما إذا كانت المعلومات متسقة مع ما تعرفه فيما يتعلق بأعمالك والسوق.

    [![قسمي الأداء والبيانات الأكثر تأثيرًا لنموذج التنبؤ.](./media/models.png)](./media/models.png)

- في القسم **الأداء**، حدد **عرض التفاصيل** لمعرفة المزيد حول الدرجة والاعتبارات الأخرى. في الرسم التوضيحي التالي، تبين التفاصيل أن النموذج يستخدم معلومات أقل مما هو مُوصى به. وبالتالي، قام النظام بإظهار رسالة تحذير.

    [![تحذيرات حول أداء النموذج.](./media/details.png)](./media/details.png)

## <a name="digging-deeper"></a>التعمق

على الرغم من أن الدقة هي نقطه بداية جيدة لتقييم أحد النماذج، وتوفر درجة الأداء المنظور، إلا أن AI Builder يوفر مقاييس أكثر تفصيلاً يمكنك استخدامها لتقييمك, لتنزيل التفاصيل، في القسم **الأداء**، حدد زر علامة الحذف (**...**) بجانب الزر **استخدام نموذج**، ثم حدد **تحميل المقاييس التفصيلية**.

[![أمر تحميل المقاييس التفصيلية.](./media/performance.png)](./media/performance.png)

يبين الرسم التوضيحي التالي التنسيق الذي يمكنك تنزيل البيانات به.

[![تنسيق البيانات التي تم تنزيلها.](./media/data-format.png)](./media/data-format.png)

للحصول على تحليل أعمق للنتائج، نقطة بداية جيدة لمراجعة المقياس "مقياس الالتباس". على سبيل المثال، فيما يلي البيانات التي يتم عرضها لهذا المقياس في الرسم التوضيحي السابق.

`{"name": "Confusion Matrix", "value": {"schema_type": "confusion_matrix", "schema_version": "1.0.0", "data": {"class_labels": ["0", "1", "2"], "matrix": [[71, 9, 21], [5, 0, 27], [2, 0, 45]]}}, "type": "dictionaryNumericalList", "isGlobalScore": false}`

يمكنك توسيع هذه البيانات بالطريقة التالية.

| &nbsp;                   | متوقع في الموعد المحدد | متوقع متأخر | متوقع متأخر جدًا |
|--------------------------|-------------------|----------------|---------------------|
| الدفع في الوقت المحدد الفعلي   | **71**            | 0              | 21                  |
| الدفع المتأخر الفعلي      | 5                 | **0**          | 27                  |
| الدفع المتأخر جدًا الفعلي | 2                 | 0              | **45**              |

يعرض مقياس الالتباس نتائج مجموعة بيانات اختبار محددة عشوائيًا من عملية التدريب. نظرًا لعدم استخدام هذه الفواتير المغلقة لتدريب النموذج، فإنها حالات اختبار جيدة للنموذج. بالإضافة إلى ذلك، نظرًا لأن الحالة الفعلية للفاتورة معروفة، فإنه يمكن مشاهدة أداء النموذج أيضًا.

الشيء الأول الذي يجب البحث عنه هو القيمة الفعلية الأكثر شيوعًا. على الرغم من أن هذه القيمة قد لا تتم محاذاتها بشكل تام مع مجموعة البيانات العامة، إلا إنها معقولة تقريبًا. في هذه الحالة، يحدث **‏‫الدفع في الوقت المحدد الفعلي** لعدد 92 من أصل 171 من الفواتير الإجمالية وإنها القيمة الفعلية الأكثر شيوعًا. وبالتالي، يُعد هذا خطًا أساسيًا جيدًا للنموذج الخاص بك. إذا كنت قد خمنت في الوقت الذي تكون فيه كافة الفواتير في الوقت المحدد، فإنك بذلك ستكون على حق في 92 من 171 مرة (أي نسبة 54 بالمائة في الوقت المحدد).

من المهم أن تفهم مدى موازنة مجموعة البيانات الخاصة بك. في هذه الحالة، تم دفع 92 فاتورة من أصل 171 في الوقت المحدد، ويتم دفع 32 متأخرة، ويتم دفع 47 فاتورة متأخرة جدًا. وتشير هذه القيم إلى مجموعة بيانات متوازنة بشكل معقول، نظرًا لوجود نتائج غير مبسطة في كل تصنيف. يمكن أن يمثل موقف حيث يكون لإحدى الحالات عدد قليل جدًا من النتائج تحديًا لنموذج التعلم الآلي.

تشير دقة النموذج إلى عدد من التوقعات الصحيحة لمجموعة بيانات الاختبار. وهذه التوقعات الصحيحة هي القيم التي تظهر بخط غامق في المثال السابق. في هذه الحالة، تعطي القيم دقة محسوبة تصل إلى 67.8 بالمائة (= \[71 + 0 + 45\] ÷ 171). تمثل هذه القيمة تحسين 14% بالمائة أعلى من تخمين الخط الأساسي الذي يبلغ 54 بالمائة ومؤشرًا واحدًا لجودة النموذج.

إذا نظرت بشكل أكثر قربًا على مقياس الالتباس، فإنك ستلاحظ أن النموذج يقوم بوظيفة جيدة لتوقع دفعات الفواتير التي تتم في الوقت المحدد والمتأخرة جدًا. ومع ذلك، فإنه يكون خاطئًا بخصوص كل الفواتير 32 جميعها التي تم دفعها بالفعل (لكن ليست متأخرة للغاية). وتقترح هذه النتيجة أن الاستكشاف والتحسين الإضافيين للنموذج مطلوبان.

الرقم الذي يمثل أداء النموذج أفضل من أن تكون الدقة هي نتيجة الماكرو F1. وتعتبر هذه النتيجة نتيجة لكل حالة تصنيف (في الوقت المحدد ومتأخرة ومتأخرة جدًا). على سبيل المثال، فيما يلي البيانات التي يتم عرضها للمقياس "ماكرو F1" في الرسم التوضيحي السابق.

`{"name": "F1 Macro", "value": 0.4927170868347339, "type": "percentage", "isGlobalScore": false}`

في هذه الحالة، النتيجة التالية لماكرو F1 تشير بشكل تقريبي بنسبة 49.3 بالمائة إلى أن نموذج لا يوفر توقعات فعالة عبر كل حالة، بالرغم من نقاط دقة إجمالية تبدو مرتفعة بشكل معقول.

## <a name="improving-the-model"></a>تحسين النموذج

بعد أن تفهم نتائج النموذج الأول الخاص بك بشكل أفضل، فإنك قد تحتاج إلى تحسين النموذج عن طريق إضافة أعمدة الميزات أو إزالتها أو عن طريق تصفية أية أجزاء من مجموعة البيانات التي لا تدعم توقعات الدقة. قم بإغلاق AI Builder، ثم استخدم الارتباط **تحسين النموذج** في Dynamics 365 Finance لإعادة تشغيل عملية AI Builder. يمكنك تجربة الخصائص المختلفة دون التأثير على النموذج المنشور. يتأثر النموذج المنشور فقط عند تحديد **نشر**. تذكر أنه يتم استخدام نموذج مفرد لمثيلك من Dynamics 365 Finance. لذلك، يجب مراجعة أي نموذج جديد بعناية قبل نشره.

## <a name="for-more-information"></a>لمزيد من المعلومات

لمزيد من المعلومات حول كيفية تقييم نماذج التوقعات، [نتائج نماذج التعلم الآلي](confusion-matrix.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
