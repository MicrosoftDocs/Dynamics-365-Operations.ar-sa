---
title: إهلاك الرصيد المتناقص بنسبة 150 بالمائة
description: تقدم هذه المقالة نظرة عامة على أسلوب إهلاك الرصيد المتناقص بنسبة 150 بالمائة‬.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f3bccb9d64851901d43b55887bb66c9b1b4e5a70
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870209"
---
# <a name="150-percent-reducing-balance-depreciation"></a>إهلاك الرصيد المتناقص بنسبة 150 بالمائة

[!include [banner](../includes/banner.md)]

تقدم هذه المقالة نظرة عامة على أسلوب إهلاك الرصيد المتناقص بنسبة 150 بالمائة‬.

عند إعداد ملف تعريف إهلاك أصول ثابتة وتحديد **الرصيد المتناقص بنسبة 150%** في حقل **الطريقة** في صفحة **ملفات تعريف الإهلاك**، يتم إهلاك الأصول الثابتة التي تم تعيين ملف تعريف الإهلاك لها بنفس النسبة المئوية في كل فترة إهلاك. حيث يتم حساب هذه النسبة المئوية بناءً على مدة الخدمة للأصل. على سبيل المثال، إذا كانت مدة خدمة الأصل خمس سنوات، فإنه يتم حساب النسبة المئوية بنسبة 30% (150% ÷ 5). 

ولإعداد إهلاك الرصيد المتناقص بنسبة 150%، يجب عليك أيضًا تحديد الخيارات في حقل **سنة الإهلاك** وحقل **تكرار الفترة** في صفحة **ملفات تعريف الإهلاك**. وتختلف الخيارات المتوفرة في حقل **تكرار الفترة** استناداً إلى القيمة المحددة في حقل **سنة الإهلاك**.

## <a name="selection-of-depreciation-year"></a>حدد سنة الإهلاك
ويمكنك تحديد **تقويم** أو **مالي** في حقل **سنة الإهلاك** في صفحة **ملفات تعريف الإهلاك**. 

القيمة الافتراضية هي **تقويم**. ويعمل التحديد الذي قمت به على تحديد الخيارات المتوفرة في حقل **تكرار الفترة**. ويحدد هذا الحقل التواريخ الخاصة بترحيل استحقاق الإهلاك بالإضافة إلى المبالغ خلال سنة التقويم.

### <a name="calendar"></a>التقويم

يمكنك اختيار الاحتفاظ بالقيمة الافتراضية في حقل **سنة الإهلاك**، **التقويم**. 

ويقوم خيار **التقويم** بتحديث أساس الإهلاك في 1 كانون الثاني/يناير من كل عام. وبشكل عام، يعتبر أساس الإهلاك صافي القيمة الدفترية ناقص قيمة الخردة. في المثال الموضح أدناه في هذا المقال، يعتبر أساس الإهلاك هو البسط في التعبير الأول في عمود عمليات الحساب. 

وإذا قمت بتحديد **التقويم** كسنة إهلاك، تتوفر الخيارات التالية في حقل **تكرار الفترة**:

-   **السنوي** ترحيل مبلغ في 31 كانون الأول/ديسمبر.
-   **شهري** ترحيل مبلغ شهري في نهاية كل شهر في التقويم.
-   **ربع سنوي** مبلغ ربع سنوي في نهاية كل ربع عام بالتقويم (31 مارس و30 يونيو و30 سبتمبر و31 ديسمبر).
-   **نصف سنوي** ترحيل مبلغ نصف سنوي في كل نصف عام بالتقويم (30 يونيو و31 ديسمبر).
-   **يومي** ترحيل مبلغ الإهلاك لطريقة الإهلاك اليومية باستخدام حركة واحدة لكل يوم.

### <a name="fiscal"></a>مالي

إذا قمت بتحديد **مالية** في حقل **سنة الإهلاك**، يتم حساب إهلاك الرصيد المتناقص بنسبة 150% بحسب السنة المالية للتقويم المالي المحدد للدفتر، أو للتقويم المالي المحدد في صفحة **دفتر الأستاذ**. ويتم إعداد التقويمات المالية في صفحة **التقويمات المالية**. 

‏‫على سبيل المثال، بالنسبة للسنة المالية من 1 تموز/يوليو إلى 30 حزيران/يونيو، يبدأ حساب الإهلاك في 1 يوليو. قد تطول مدة السنة المالية عن 12 شهرًا أو قد تقل عن ذلك. وتتم تسوية الإهلاك لكل فترة. ويتم تحديد طول السنة المالية التالية بإعداد الفترات في صفحة **التقويمات المالية**. 

وإذا قمت بتحديد **مالية** كسنة إهلاك، تتوفر الخيارات التالية في حقل **تكرار الفترة**:

-   **سنوي** ترحيل إجمالي مبلغ الإهلاك المحسوب بالنسبة للسنة المالية كمبلغ واحد في آخر يوم في السنة المالية.
-   تقوم **الفترة المالية** بترحيل المبلغ الإجمالي للإهلاك للسنة المالية. ويُستحق هذا المبلغ في الفترات المالية التي يتم تحديدها في صفحة **التقويمات المالية**.

## <a name="example-of-150-reducing-balance-depreciation"></a>مثال على إهلاك القسط المتناقص بسبة 150 في المائة

| &nbsp;                         | &nbsp; |
|--------------------------------|--------|
| تكلفة الاستحواذ               | 11,000 |
| القيمة الباقية                  | 1,000  |
| أساس الإهلاك              | 10,000 |
| سنوات مدة الخدمة             | 5      |
| النسبة المئوية للإهلاك السنوي | 30%    |

تقوم طريقة الرصيد المتناقص بنسبة 150% بقسمة نسبة 150 في المائة على سنوات مدة الخدمة. وسيتم ضرب النسبة المئوية في صافي القيمة الدفترية للأصل لتحديد مبلغ الإهلاك في السنة.

| الفترة | حساب مبلغ الإهلاك السنوي | القيمة الدفترية             | صافي القيمة الدفترية في نهاية السنة |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| السنة الأولى | (11,000 – 1,000) × 30% = 3,000                | 11,000 – 3,000 = 8,000 | 11,000 – 1,000 – 3,000 = 7,000        |
| السنة الثانية | 7,000 × 30% = 2,100                           | 8,000 – 2,100 = 5,900  | 7,000 – 2,100 = 4,900                 |
| السنة الثالثة | 4,900 × 30% = 1,470                           | 5,900 – 1,470 = 4,430  | 4,900 – 1,470 = 3,430                 |

> [!NOTE]
> بشكل عام، عندما يصبح المبلغ الذي يتم حسابه باستخدام طريقة الإهلاك المتناقص بنسبة 150% أقل من المبلغ الذي يُحسب باستخدام طريقة القسط الثابت، يكون هناك تحويل لطريقة القسط الثابت للمدة المتبقية.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
