---
title: عناصر سير العمل
description: توضح هذه المقالة العناصر المختلفة التي تشكّل سير عمل.
author: ChrisGarty
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e145a8ebb082aa2d59c9a05a0cbbf38e9936bae0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900089"
---
# <a name="workflow-elements"></a>عناصر سير العمل

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

توضح هذه المقالة العناصر المختلفة التي تشكّل سير عمل.

يتألف سير العمل من عناصر. توضح الأقسام التالية كل نوع عنصر.

## <a name="tasks"></a>مهام

تعتبر *المهمة* وحدة عمل يجب إجراؤها. يمكن إضافة نوعين من المهام لسير عمل: المهام اليدوية والمهام التلقائية.

### <a name="manual-task"></a>المهمة اليدوية

تعتبر *المهمة اليدوية* وحدة عمل يجب إجراؤها بواسطة المستخدم. على سبيل المثال، قد يشتمل سير عمل تقرير المصروفات على مهام يدوية تتطلب من المستخدمين المعينين إكمال الإجراءات التالية:

- مراجعة الإيصالات التي تم إرسالها إلى جانب تقرير مصروفات.
- الاتصال بمدير موظف.

### <a name="automated-task"></a>مهمة مؤتمتة

تعتبر *المهمة التلقائية* وحدة عمل يجب إجراؤها بواسطة النظام. لا يلزم أي تفاعل بشري. على سبيل المثال، قد يشتمل سير عمل أمر المبيعات على مهام تلقائية تتطلب من النظام إكمال الإجراءات التالية:

- تنفيذ فحص ائتمان.
- أنشئ سجل عميل للعميل، إذا لم يكن السجل موجودًا بالفعل.

## <a name="approval-processes"></a>عمليات الاعتماد

تعتبر *عملية الاعتماد* عملية تتألف من خطوات منفصلة. في كل خطوة من خطوات الاعتماد، يمكن للمستخدم تنفيذ الإجراءات التالية:

- اعتماد المستند.
- رفض المستند.
- طلب تغيير في المستند.
- تعيين المستند إلى مستخدم آخر للاعتماد.

## <a name="line-item-workflow-elements"></a>عناصر سير عمل عنصر البند

يمكن إنشاء سير عمل لمعالجة المستندات أو عناصر البنود الموجودة في مستند. على سبيل المثال، لقد قمت بإنشاء سير عمل اعتماد للجداول الزمنية. ‏‫(سنشير إلى سير العمل هذا بصفته *سير عمل المستند*.) يمكنك إضافة *‬‏‫سير العمل عنصر الصنف* إلى سير عمل المستند هذا.‬ وعند تشغيل صنف البند، يتم إرسال كل صنف بند في المستند للمعالجة. قد تحتاج إلى معالجة كافة أصناف البند بنفس بند سير عمل صنف البند، أو قد تحتاج إلى معالجة كل صنف بند بواسطة سير عمل صنف بند مختلف. تخيل أن موظف قام بتقديم جدول زمني يشبه الشكل التالي.

![سير العمل مع عناصر البند.](./media/workflow_lineitemworkflow.gif)

في هذا السيناريو، قد تحتاج إلى إنشاء مهام سير عمل لعناصر البنود التالية:

- **سير عمل عنصر البند 1** – يتم استخدام سير العمل هذا لمعالجة عناصر البند حيث يكون معرف المشروع هو 1111.
- **سير عمل عنصر البند 2** – يتم استخدام سير العمل هذا لمعالجة عناصر البند حيث يكون معرف المشروع هو 2222.
- **سير عمل عنصر البند 3** – يتم استخدام سير العمل هذا لمعالجة عناصر البند حيث يكون معرف المشروع هو 3333.

## <a name="flow-control-elements"></a>عناصر التحكم في التدفق

تتيح لك العناصر التالية تصميم مهام سير العمل التي لها فروع بديلة أو فروع يتم تشغيلها في نفس الوقت.

### <a name="manual-decision"></a>قرار يدوي

*القرار اليدوي* هو نقطة ينقسم عندها سير العمل إلى فرعين. يجب على المستخدم اتخاذ قرار، ويحدد هذا القرار أي فرع يتم استخدامه لمعالجة المستند الذي تم إرساله.

### <a name="conditional-decision"></a>قرار مشروط

*القرار المشروط* هو نقطة ينقسم عندها سير العمل إلى فرعين. ومع ذلك، يقرر النظام أي فرع يتم استخدامه لمعالجة المستند الذي تم إرساله. ولاتخاذ هذا القرار، يقوم النظام بتقييم المستند لتحديد ما إذا كان يستوفي الشروط المحددة أم لا.

### <a name="parallel-activity"></a>نشاط موازٍ

*النشاط الموازي* هو عنصر سير عمل يشمل فرعي سير عمل أو أكثر يتم تشغيلهم في نفس الوقت.

### <a name="subworkflow"></a>سير العمل الفرعي

*سير العمل الفرعي* هو سير عمل يتم تشغيله داخل سياق سير عمل آخر.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]