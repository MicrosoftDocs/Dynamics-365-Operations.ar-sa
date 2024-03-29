---
title: تسجيل إهلاك حق استخدام الأصل‬ (معاينة)
description: توضح هذه المقالة كيفية إنشاء إدخال دفتر اليومية لإطفاء الدين المطلوب في عقود الإيجار التي يتم الإقرار بها في الميزانية العمومية للمؤسسة.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseAssetSchedule
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 93e521cf409af4c01d625f27bdd7a7564e471bd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903265"
---
# <a name="record-right-of-use-asset-depreciation-preview"></a>تسجيل إهلاك حق استخدام الأصل‬ (معاينة)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


بالنسبة لعقود الإيجار التي يتم الإقرار بها في الميزانية العمومية للمؤسسة، فإنه يتم استهلاك حق استخدام الأصل على أساس شهري. توضح هذه المقالة كيفية إنشاء إدخال دفتر اليومية الخاص بإطفاء الدين. يقوم إطفاء الدين بخصم حساب دفتر أستاذ المصروفات ويقيد حساب دفتر أستاذ الإهلاك التراكمي وفقًا لإعداد ملف تعريف الترحيل ونوع عقد الإيجار. يمكن إنشاء هذه الإدخالات لكل عقد إيجار، أو يمكن إنشاؤها للعديد من عقود الإيجار باستخدام وظيفة دفتر يومية الدُفعة.

## <a name="asset-depreciation-schedule"></a>جدول إهلاك الأصول

1. في الصفحة **ملخص عقد الإيجار**، حدد عقد إيجار. ثم حدد **الدفاتر \> جدول إهلاك الأصول** لفتح الصفحة **جدول إهلاك الأصول**.

    يستند إدخال دفتر يومية مصروفات إهلاك حق استخدام الأصل إلى المبلغ الموجود في العمود **مصروفات الإهلاك**. للحصول على مثال على التوافق مع مقياس المحاسبة، راجع [حساب مصروفات إطفاء دين الأصول لعقود الإيجار المالية](#calculation-of-rou-asset-amortization-expense-for-finance-leases) لاحقًا في هذه المقالة.
    
2. حدد فترة الإهلاك، ثم حدد **إنشاء دفتر اليومية**. تظهر رسالة توضح أنه تم إنشاء دفتر اليومية الذي سيتم استخدامه لتسجيل الإهلاك.
3. حدد **دفاتر اليومية \> دفاتر يومية إيجار الأصول** لفتح الصفحة **دفتر يومية تأجير الأصول**، حيث يمكنك عرض إدخال دفتر يومية مصروفات الإهلاك الذي تم إنشاؤه.

   يقوم النظام بتأمين حقول مالية معينة من التحرير لمنع أي تباينات بين الحركات والجداول. تتضمن بعض الحقول التي تم تأمينها: **الحساب** و **المبالغ** و **الأبعاد المالية** و **العملة** و **ونوع الحركة**. بالإضافة إلى ذلك، لن تتمكن من إضافة أو حذف بنود إدخال دفتر اليومية في أي إدخالات دفتر يومية تأجير الأصول، لأن ذلك قد يسبب تباينات بين الجداول والحركات.

4. حدد إدخال دفتر اليومية، ثم حدد **ترحيل** لتسجيل إدخال الإهلاك إلى دفتر الأستاذ العام.

## <a name="calculation-of-rou-asset-amortization-expense-for-operating-leases"></a>حساب مصروفات إطفاء الدين لحق استخدام الأصل لعقود الإيجار التشغيلية

يتم حساب مصروفات الإهلاك الخاصة بعقد الإيجار التشغيلي لأن الفرق بين نفقات عقد القسط الثابت الشهري ونفقات الفوائد الخاصة بالتزامات الإيجار الشهري، وفقًا لموضوع صياغة مقاييس المحاسبة 842 (ASC 842)، وهو المقياس في المبادئ المحاسبية المقبولة بشكل عام في الولايات المتحدة (US GAAP). يتم حساب مصروفات إيجار القسط الثابت كمجموع لكافة دفعات الإيجار مقسومة على فترة الإيجار بالشهور. (يتضمن مجموع دفعات الإيجار أية مقابل دفعات مقدمة وتكاليف مباشرة لعقد الإيجار وتكاليف التفكيك وحوافز في الإيجار.) يعرض الجدول التالي مثالاً على مصروفات إطفاء الدين لعقد الإيجار التشغيلي.

### <a name="example-of-rou-asset-amortization-expense-for-operating-leases"></a>مثال على مصروفات إطفاء الدين لحق استخدام الأصل لعقود الإيجار التشغيلية

| الحقل                                          | قيمة       |
|------------------------------------------------|-------------|
| مبلغ الدفع                                 | 1,000       |
| تكرار الدفع                              | شهري     |
| فترة الإيجار (أشهر)                            | 24          |
| إجمالي دفعات الإيجار                           | 24,000      |
| سعر الفائدة على الاقتراض الإضافي                     | 5%          |
| نوع الاستحقاق السنوي                                   | الاستحقاق السنوي المستحق |
| فاصل متراكب                           | شهري     |
| القيمة الحالية للحد الأدنى لدفعات الإيجار المستقبلية | 22,888.87   |

كما قيل سابقًا، يتم حساب مصروفات إيجار القسط الثابت كمجموع لكافة دفعات الإيجار مقسومة على فترة الإيجار بالشهور. يقوم النظام تلقائيًا بحساب نفقات الفائدة الشهرية في جدول الاستهلاك إطفاء الدين. يتم حساب مصروفات الفوائد باستخدام طريقة سعر الفائدة الفعالة. سيقوم النظام باستخدام مصروفات إيجار القسط الثابت لطرح نفقات الفوائدة لكل شهر. يتم استخدام القيمة لتقليل حق استخدام الأصل.

| الشهر | مصروفات إيجار القسط الثابت | مصروفات الفائدة                        | حساب مصروفات إطفاء الدين لحق استخدام الأصل |
|-------|--------------------------|-----------------------------------------|-----------------------------------------------|
| 1     | (24.000 ÷ 24) = 1.000.00 | (22.888.87 – 1.000) × (5% ÷ 12) = 91.20 | 1.000 – 91.20 = 908.80                        |
| 2     | (24.000 ÷ 24) = 1.000.00 | (21.980.08 – 1.000) × (5% ÷ 12) = 87.42 | 1.000 – 87.42 = 912.58                        |
| 3     | (24.000 ÷ 24) = 1.000.00 | (21.067.49 – 1.000) × (5% ÷ 12) = 83.62 | 1.000 – 83.62 = 916.39                        |

> [!NOTE]
> وفقًا لـ ، يتم تصنيف إهلاك حق استخدام الأصل لعقد إيجار تشغيلي كمصروفات عقد إيجار في كشف الدخل. للرؤية، يصف إيجار الأصل الإدخال كإهلاك حق استخدام الأصل. ومع ذلك، يجب تعيين إدخال دائن لحساب مصروفات عقد الإيجار التشغيلي، كما يجب تعيين إدخال الدائن مباشرة إلى حق استخدام الأصل لعقد الإيجار التشغيلي. ومع ذلك، في معلمات عقد الإيجار، يمكنك تحديد وجوب إجراء إدخالات الائتمان لحساب الإهلاك التراكمي لحق استخدام الأصل للعقد التشغيلي.

وإذا تم تصنيف التأجير كعقد إيجار تشغيلي، فسيتم حساب الإهلاك الشهري بعد انخفاض القيمة باستخدام الإهلاك الثابت.

## <a name="calculation-of-rou-asset-amortization-expense-for-finance-leases"></a>حساب مصروفات إطفاء الدين لحق استخدام الأصل لعقود الإيجار المالية

بالنسبة لعقود الإيجار التي تحتوي على تصنيف مالي، يقوم النظام بحساب إطفاء دين حق استخدام الأصل على أساس القسط الثابت. وبالتالي، ستكون مصروفات الإهلاك متماثلة لكل شهر.

بالتوافق مع مقاييس Financial Reporting الدولية 16 (IFRS 16) وASC 842، سيتم استهلاك الأصل إما حسب فترة الإيجار أو العمر الإنتاجي للأصل، أيهما أقل. بالإضافة إلى ذلك، في حالة تشغيل المعلمة **تحويل الملكية** لعقد إيجار، فإنه سيتم إهلاك عقد الإيجار تلقائيًا على مدار العمر الإنتاجي للأصل.

### <a name="example-of-rou-asset-amortization-expense-for-finance-leases"></a>مثال على مصروفات إطفاء الدين لحق استخدام الأصل لعقود الإيجار المالية

| الحقل                                | قيمة                                   |
|--------------------------------------|-----------------------------------------|
| بدء رصيد حق استخدام الأصل‬ | 22,889.87                               |
| فترة الإيجار (أشهر)                  | 24                                      |
| العمر الإنتاجي للأصل (أشهر)           | 36                                      |
| الشهر                                | مصروفات إطفاء دين حق استخدام الأصل‬ |
| 1                                    | 22.889.87 ÷ 24 = 953.74                 |
| 2                                    | 22.889.87 ÷ 24 = 953.74                 |
| 3                                    | 22.889.87 ÷ 24 = 953.74                 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
