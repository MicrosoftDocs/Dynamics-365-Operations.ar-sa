---
title: إهلاك القسط المتناقص
description: تقدم هذه المقالة نظرة عامة على أسلوب تقليل الرصيد للإهلاك.
author: moaamer
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52bf9d4e9cbc9cabda5d5ab17c1a00ecea0d0348
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883260"
---
# <a name="reduce-balance-depreciation"></a>إهلاك القسط المتناقص

[!include [banner](../includes/banner.md)]

تقدم هذه المقالة نظرة عامة على أسلوب تقليل الرصيد للإهلاك.

عند إعداد ملف تعريف إهلاك أصل ثابت وتحديد "الرصيد المتناقص في الحقل **الطريقة** في صفحة **ملفات تعريف الإهلاك**، يتم إهلاك الأصول التي تم تخصيص ملف تعريف الإهلاك هذا لها، وذلك بنفس النسبة المئوية في كل فترة إهلاك.

ولإعداد إهلاك الرصيد المتناقص، يجب عليك أيضًا عمل تحديدات في بعض الحقول الموجودة في علامة التبويب السريع **عام** الموجودة في صفحة **ملفات تعريف الإهلاك**. أولاً، حدد سنة في حقل **سنة الإهلاك**. وبناءً على التحديد، تظهر خيارات مختلفة في الحقل **تكرار الفترة**، كما هو موضح في الأقسام التالية. 

ويجب عليك أيضًا إدخال قيمة في الحقل **النسبة المئوية** لملف تعريف الإهلاك. وفي حالة تحديد الخيار **الإهلاك الكامل**، فسيتم تحصيل أساس الإهلاك المتبقي في فترة آخر إهلاك وقد يكون مبلغًا كبيرًا. ولا تستخدم بعض البلاد/المناطق بديلاً لطريقة القسط الثابت. ويتم استخدام البديل عندما يكون مبلغ الإهلاك البديل أكبر من أو مساويًا لمبلغ ملف تعريف الإهلاك الأساسي، فإن مبلغ الإهلاك المأخوذ يكون مبلغ الطريقة البديلة. 

ولأنه لن يتم مطلقًا إهلاك الأصل بالكامل بناءً على حساب النسبة المئوية، فيجب عليك تحديد الخيار **الإهلاك الكامل** لإهلاك أصل بالكامل.

## <a name="select-a-depreciation-year"></a>تحديد سنة الإهلاك
ويمكنك تحديد **تقويم** أو **مالي** في حقل **سنة الإهلاك** في صفحة **ملفات تعريف الإهلاك**. ويعمل هذا التحديد على تحديد الخيارات المتوفرة في حقل **تكرار الفترة**. والخيار الافتراضي هو **تقويم**.

### <a name="calendar"></a>التقويم

يقوم **خيار التقويم** بتحديث أساس الإهلاك، الذي عادةً ما يكون صافي القيمة الدفترية ناقص قيمة الخردة، في 1 يناير من كل عام. وفي مثال إهلاك الرصيد المتناقص الموضح لاحقًا في هذه المقالة، يعتبر أساس الإهلاك هو البسط في التعبير الأول في عمود عمليات الحساب. 

في حالة قيامك بتحديد **تقويم**، تتوفر الخيارات التالية في حقل **تكرار الفترة**، الذي يحدد التواريخ الخاصة بترحيل استحقاق الإهلاك بالإضافة إلى المبالغ خلال سنة التقويم:

- الترحيلات السنوية في 31 ديسمبر.
- شهري ترحيل مبلغ شهري في نهاية كل شهر في التقويم.
- ربع سنوي مبلغ ربع سنوي في نهاية كل ربع عام بالتقويم (31 مارس و30 يونيو و30 سبتمبر و31 ديسمبر).
- يقوم خيار الترحيل نصف السنوي بترحيل مبلغ نصف سنوي في كل نصف عام بالتقويم (30 يونيو و31 ديسمبر).
- يقوم خيار الترحيل اليومي بترحيل مبلغ الإهلاك لطريقة الإهلاك اليومية باستخدام حركة واحدة لكل يوم.

على سبيل المثال، إذا قمت بتحديد **سنوي**، يتم ترحيل الإهلاك السنوي مرة واحدة فقط في 31 ديسمبر من كل عام. أما إذا حددت **شهري**، فإنه يتم ترحيل الإهلاك الشهري في كل شهر بمعدل 1/12 من قيمة المبلغ الإجمالي السنوي.

### <a name="fiscal"></a>مالي

في حالة تحديد **مالي** في حقل **سنة الإهلاك**، فسيتم استخدام طريقة إهلاك القسط الثابت. ويتم حساب ذلك على أساس السنة المالية، التي تم إعدادها في صفحة **التقويمات المالية** للتقويم المالي المحدد في صفحة **دفتر الأستاذ**. ‏‫على سبيل المثال، بالنسبة للسنة المالية من 1 تموز/يوليو إلى 30 حزيران/يونيو، يبدأ حساب الإهلاك في 1 يوليو. قد تطول مدة السنة المالية عن 12 شهرًا أو قد تقل عن ذلك. وتتم تسوية الإهلاك لكل فترة مالية. ويعتمد طول السنة المالية التالية على الفترات المالية التي تقوم بإعدادها عند قيامك بإنشاء سنة مالية جديدة في صفحة **التقويمات المالية**.


إذا قمت بتحديد **مالي**، تتوفر الخيارات التالية في حقل **تكرار الفترة**:

- يقوم الخيار "سنوي" بترحيل إجمالي مبلغ الإهلاك المحسوب بالنسبة للسنة المالية كمبلغ واحد في آخر يوم في السنة المالية.
- تقوم الفترة المالية بترحيل المبلغ الإجمالي للإهلاك المحسوب للسنة المالية، والذي يتراكم في الفترات المالية التي تم تعريفها للتقويم المالي المحدد في صفحة **دفتر الأستاذ**، أو للتقويم المالي المحدد لدفتر أصل ثابت.

## <a name="example-of-reducing-balance-depreciation"></a>مثال لإهلاك القسط المتناقص

افترض أن سعر امتلاك الأصل الثابت هو 11000، وقيمة الخردة هي 1000، وعامل النسبة المئوية للإهلاك هو 30. 

باستخدام طريقة "تقليل الرصيد‬"، سيتم حساب 30 بالمئة من أساس الإهلاك (صافي القيمة الدفترية ناقص قيمة الخردة) في نهاية فترة الإهلاك السابقة. والإهلاك بالنسبة لأول ثلاث سنوات مبين في الجدول التالي.

| الفترة | حساب مبلغ الإهلاك السنوي | صافي القيمة الدفترية في نهاية السنة |
|--------|-------------------------------------------|---------------------------------------|
| السنة الأولى | (11000 - 1000) \* 30% =‏ 3000           | (11000 - 1000) - 3000 = 7000      |
| السنة الثانية | (7000 - 1000) \* 30% =‏ 1800            | (7000 -1800) = 5200                |
| السنة الثالثة | (5200 - 1000) \* 30% =‏ 1260            | (5200 - 1260) = 3940               |










[!INCLUDE[footer-include](../../includes/footer-banner.md)]
