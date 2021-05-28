---
title: حساب TDS على المدفوعات والسندات الإذنية
description: يوفر هذا الموضوع معلومات مرجعية حول حركات الدفع المختلفة التي يتم حساب الضريبة المخصومة من المصدر (TDS) عليها.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: ea57963e41b90bbc11efa00b85aad8bc60c2357d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023000"
---
# <a name="tds-calculation-on-payments-and-promissory-notes"></a>حساب TDS على المدفوعات والسندات الإذنية

[!include [banner](../includes/banner.md)]

يوفر هذا الموضوع معلومات مرجعية حول حركات الدفع المختلفة التي يتم حساب الضريبة المخصومة من المصدر (TDS) عليها.

| الرقم المسلسل | نوع المعاملة | مبلغ الحركة | اسم الصفحة والمسار | نوع الحساب ونوع الحساب المقابل |
|---------------|------------------|--------------------|--------------------|--------------------------------------|
| 1             | الدفع/الدفع المقدم مقابل الفاتورة (TDS مستحقة الدفع) | المدين أو الدائن | <ul><li>دفتر اليومية العام (**دفتر الأستاذ العام \> إدخالات دفتر اليومية \> دفاتر اليومية العامة**‬)</li><li>دفتر يومية الفواتير (**الحسابات الدائنة \> الفواتير \>دفتر يومية الفواتير**)</li><li>دفتر يومية المدفوعات (**الحسابات الدائنة \> المدفوعات \> دفتر يومية المدفوعات للمورد**)</li></ul> | المورد (Dr.)، البنك (Cr.) |
| 2             | الدفع/الدفع المقدم مقابل الفاتورة (الشراء الذي تم إجراؤه من عميل – TDS مستحقة الدفع) | المدين أو الدائن | <ul><li>دفتر اليومية العام (**دفتر الأستاذ العام \> إدخالات دفتر اليومية \> دفاتر اليومية العامة**‬)</li><li>دفتر يومية الفواتير (**الحسابات الدائنة \> الفواتير \>دفتر يومية الفواتير**)</li><li>دفتر يومية المدفوعات (**الحسابات الدائنة \> المدفوعات \> دفتر يومية المدفوعات للمورد**)</li></ul> | العميل (Dr.)، البنك (Cr.) |
| 3             | السندات الإذنية | مدين | دفتر يومية سحب السندات الإذنية (**الحسابات الدائنة \> المدفوعات \> السندات الإذنية \> دفتر يومية سحب السند الإذني**) | المورد (Dr.)، دفتر الأستاذ (Cr.) |
| 4             | الدخل المتنوع (TDS مستحق القبض) | المدين أو الدائن | دفتر اليومية العام (**دفتر الأستاذ العام \> إدخالات دفتر اليومية \> دفاتر اليومية العامة**‬) | البنك (Dr.)، دفتر الأستاذ (Cr.) |
| 5             | مصروفات أخرى (TDS مستحق الدفع) | المدين أو الدائن | دفتر اليومية العام (**دفتر الأستاذ العام \> إدخالات دفتر اليومية \> دفاتر اليومية العامة**‬) | البنك (Dr.)، دفتر الأستاذ (Cr.) |

اتبع هذه الخطوات لحساب TDS على المدفوعات والسندات الإذنية.

1. في صفحات دفتر اليومية، قم بإنشاء بنود دفتر اليومية. حدد نوع الحساب ونوع الحساب المقابل.
2. حدد **الوظائف \> التسوية** لفتح الصفحة **تحرير الحركة المفتوحة**. ثم حدد فاتورة معينة يجب تسويتها. إذا تم حساب TDS بالفعل على مستوى الفاتورة، يعرض الحقل **أصل المبلغ** المبلغ الأساسي الذي تم حساب TDS عليه. يعرض الحقل **مبلغ TDS** – مبلغ TDS الذي تم حسابه للحركة. يعرض الحقل **المبلغ** يظهر صافي مبلغ الدفع (أي، مبلغ الدفع بعد خصم TDS).

    > [!NOTE]
    > بالنسبة للدفعات التي تمت في مقابل الفاتورة، فإنه يتم تطبيق الشروط التالية:
    >
    > - في حالة ما إذا كان مبلغ الدفع هو نفس مبلغ الفاتورة، فلن يتم احتساب TDS إذا تم حسابه بالفعل على مستوى الفاتورة.
    > - إذا كان مبلغ الفاتورة بعد اقتطاع مبلغ TDS أكثر من مبلغ الدفع، فلن يتم حساب TDS.
    > - إذا كان مبلغ الفاتورة بعد خصم مبلغ TDS أقل من مبلغ الدفع، فإنه سيتم حساب TDS على المبلغ الذي يتجاوز مبلغ الفاتورة.

3. في الصفحة **إيصال دفتر اليومية** على علامة التبويب **نظرة عامة**، في الحقل **مجموعات TDS**، قم بمراجعة أو تغيير مجموعة TDS الافتراضية التي يتم تحديدها للمورد أو العميل. يعتمد TDS الذي يتم حسابه في بنود دفتر اليومية على المعادلة المحددة لأكواد الضريبة TDS المدرجة في الحقل مجموعة TDS.

    > [!NOTE]
    > يتم حساب TDS فقط إذا تم تعيين الخيار **حساب ضريبة الخصم** إلى **نعم** للمورد في الصفحة **جميع الموردون**.

4. من علامة التبويب **معلومات الضريبة**، في القسم **معلومات الشركة**، في الحقل **الاسم**، يمكنك تحديد اسم الشركة لعنوان بديل يتم إعداده للشركة.

    في الحقل **ضريبة الخصم**، يعرص الحقل **طبيعة المقيم** طبيعة المقيم لفئة مقيم المورد أو العميل. يعرض الحقل **رقم حساب الضريبة (TAN)** رقم حساب الضريبة (TAN) للشركة المحددة.

5. حدد **زر ضريبة الخصم \> ضريبة الخصم** لفتح الصفحة **حركات ضريبة الخصم المؤقتة**. يحتوي الجزء العلوي من هذه الصفحة على الحقول التالية:

    - **إجمالي مبلغ ضريبة الخصم** – إجمالي TDS المحسوب للحركة لمجموعة TDS.
    - **القيمة** – النسبة المئوية الإجمالية المستخدمة لحساب TDS الخاصة بالحركة. يستند إجمالي النسبة المئوية إلى المعادلة التي يتم تحديدها لأكواد الضريبة TDS المرتبطة بمجموعة TDS.
    - **إجمالي مبلغ ضريبة الخصم المعدل** – إجمالي مبلغ TDS المعدل لكافة أكواد الضريبة في مجموعة TDS.
    - **TDS** – تشير خانة الاختيار المحددة إلى أنه تم إرفاق مجموعة TDS بالحركة.

    تعرض الحقول الموجودة على علامات التبويب **نظرة عامة** و **عام** و **تسوية** مبلغ TDS المحسوب وتفاصيل مبلغ TDS المعدل لكل كود ضريبة TDS مرفق بالمجموعة TDS.

6. حدد **الحد** لفتح الصفحة **الحد**، حيث يمكنك مراجعة الحد الذي يتم تحديده لمكون الضريبة TDS الذي تم إرفاقه بكود ضريبة TDS محدد.
7. حدد **مصمم المعادلة** لفتح الصفحة **مصمم المعادلة**، حيث يمكنك مراجعة المعادلة التي يتم تحديدها لكود ضريبة TDS محدد.
8. قم بإغلاق الصفحات **مصمم المعادلة** و **حركات ضريبة الخصم المؤقتة** للرجوع إلى الصفحة **إيصال دفتر اليومية**.
9. تحقق من صحة دفتر اليومية وقم بترحيله. يتم ترحيل مبلغ TDS الذي تم حسابه إلى الحساب الدائن الذي يتم تحديده لكل كود ضريبة TDS في المجموعة TDS. يتم تحديد الحسابات المدينة لأكواد ضريبة TDS في الصفحة **أكواد ضريبة الخصم**.
10. حدد **ضريبة الخصم المرحلة** لفتح الصفحة **حركات ضريبة الخصم**. يعرض الحقل **القيمة** النسبة المئوية الإجمالية المستخدمة لحساب TDS الخاصة بالحركة.

    تعرض الحقول الموجودة على علامات التبويب **نظرة عامة** و **عام** و **المبلغ** مبالغ TDS التي تم حسابها لمجموعة TDS المرفقة بالحركة.

11. قم بمراجعة معلومات حساب TDS لكل كود ضريبة TDS مرفق بالمجموعة TDS.

## <a name="generate-payments"></a>إنشاء المدفوعات

لإنشاء المدفوعات، اتبع الخطوات التالية:

1. اتبع إحدى الخطوات التالية:

    - انتقل إلى **الحسابات الدائنة \> المدفوعات \> دفتر يومية المدفوعات للمورد**.
    - انتقل إلى **الحسابات المدينة \> المدفوعات \> دفتر يومية المدفوعات للعميل**.
    - انتقل إلى **الحسابات الدائنة \> المدفوعات \> السندات الإذنية \> دفتر يومية سحب السند الإذني**.
    - انتقل إلى **الحسابات المدينة \> المدفوعات \> الكمبيالة \> دفتر يومية سحب الكمبيالات**.
    - انتقل إلى **الحسابات المدينة \> المدفوعات \> الكمبيالة \> دفتر يومية إعادة سحب الكمبيالات**.

2. حدد **البنود**.
3. حدد **الوظائف \> إنشاء مدفوعات**.