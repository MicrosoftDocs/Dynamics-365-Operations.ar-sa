---
title: تأجيل الإيرادات والمصروفات في فواتير الاشتراكات
description: توضح هذه المقالة كيفية إعداد تأجيلات الإيرادات والمصروفات في فواتير الاشتراك.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 209afd08c0c7e3cbd63ed95613b1d1dec94856f5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908085"
---
# <a name="revenue-and-expense-deferrals-in-subscription-billing"></a>تأجيل الإيرادات والمصروفات في فواتير الاشتراكات

توضح هذه المقالة كيفية إعداد واستخدام تأجيلات الإيرادات والمصروفات في فواتير الاشتراك. تستند جداول التأجيل دائمًا إلى مستند منشأ أساسي أو جدول فوترة وتعتمد عليه. نظرًا لأنه تم إنشاؤها استنادًا إلى القيم الافتراضية، فلا يمكن إدخالها أو إنشاؤها بشكل منفصل.

تحدث عملية إعداد واستخدام تأجيلات الإيرادات والمصروفات في صفحات متعددة:

- في صفحة **معامِلات تأجيل الإيرادات والمصروفات**،، يمكنك تحديد تفضيلات الشركة.
- في صفحة **الإعدادات الافتراضية للتأجيل**، يمكنك إعداد الحسابات والقوالب الافتراضية المستخدمة في جداول التأجيل.
- في صفحتي **قوالب التأجيل** و **قوالب التأجيل على أساس الحدث**، يمكنك تحديد القوالب المستخدمة لجداول التأجيل.
- في صفحة **كل جداول التأجيل**، يمكنك عرض جدول التأجيل وتحريره.

يمكن استخدام تأجيلات الإيرادات والمصروفات جنبًا إلى جنب مع إعداد فواتير العقد المتكررة.

## <a name="revenue-and-expense-deferral-parameters"></a>معلمات تأجيل المصروفات والإيرادات

تحتوي صفحة **معامِلات تأجيل الإيرادات والمصروفات** على الحقول التالية.

| الحقل | ‏‏الوصف‬ |
|---|---| 
| علامة التبويب **الجدول** | |
| متساوي لكل فترة | <p>حدد ما إذا كان عدد الأيام في فترة ما يتم استخدامه عند حساب المبلغ لكل فترة لجدول تأجيل:</p><ul><li>**نعم** – المبلغ لكل فترة هو نفسه، بغض النظر عن عدد الأيام في الفترة. سيتم تقسيم الفترات الجزئية (مثل الفترات في بداية أو نهاية جدول التأجيل) بالتناسب.</li><li>**لا** – يتم حساب المبلغ بناءً على عدد الأيام في كل فترة.</li></ul><p>يمكنك تجاوز هذا الإعداد على مستوى الصفقة.</p> |
| خيار تأجيل خصم المبيعات | <p>حدد ما إذا كان قد تم إنشاء جداول تأجيل منفصلة للخصم ومبالغ أوامر المبيعات:</p><ul><li>**جدول منفصل للخصم** – يتم الاحتفاظ بمبلغ الخصم منفصلاً عن مبلغ الإيرادات.<p>في هذه الحالة، يتم إنشاء جدولين للتأجيل عند إنشاء أمر مبيعات ثم ترحيله. سيتم ترحيل مبالغ الخصم والإيرادات إلى حسابات تأجيل مختلفة.</p></li><li>**دمج الخصم مع الإيرادات** – يتم دمج مبلغ الخصم مع مبلغ الإيرادات. يتم إنشاء جدول تأجيل واحد، ويتم ترحيل كل من مبلغ الخصم ومبلغ الإيرادات إلى نفس حساب التأجيل.<p>في هذه الحالة، يتم إنشاء جدول تأجيل واحد عند إنشاء أمر مبيعات ثم ترحيله. يتم ترحيل كل من مبلغ الخصم ومبلغ الإيرادات إلى نفس حساب التأجيل.</p></li></ul><p>**ملاحظة:** لتطبيق الخصومات على العناصر التي تستخدم ميزة الإيرادات غير المفوترة، حدد خيار **جدول منفصل للخصم**. يمكن بعد ذلك تطبيق الخصومات على جميع العناصر، بغض النظر عما إذا كانت ميزة الإيرادات غير المسددة مستخدمة أم لا. إذا تم تحديد الخيار **دمج الخصم مع الإيرادات**، فلا يمكن تطبيق الخصومات على العناصر التي تستخدم ميزة الإيرادات غير المفوترة.</p> |
| خيار تأجيل خصم الشراء | <p>حدد ما إذا كان يتم إنشاء جداول تأجيل منفصلة لمبالغ الخصم وأمر الشراء:</p><ul><li>**جدول منفصل للخصم** – يتم الاحتفاظ بمبلغ الخصم منفصلاً عن مبلغ المصاريف.<p>في هذه الحالة، يتم إنشاء جدولين للتأجيل عند إنشاء أمر الشراء ثم ترحيله. يتم ترحيل مبالغ الخصم والمصروفات إلى حسابات تأجيل مختلفة.</p></li><li>**دمج الخصم مع الإيرادات** – يتم دمج مبلغ الخصم مع مبلغ المصاريف. يتم إنشاء جدول تأجيل واحد، ويتم ترحيل كل من مبلغ الخصم ومبلغ المصروفات إلى نفس حساب التأجيل.<p>في هذه الحالة، يتم إنشاء جدول تأجيل واحد عند إنشاء أمر شراء ثم ترحيله. يتم ترحيل كل من مبلغ الخصم ومبلغ المصاريف إلى نفس حساب التأجيل.</p></li></ul> |
| التجميع قبل الفترات | <p>حدد ما إذا كانت بنود جدول التأجيل للفترات السابقة مجمعة أم لا:</p><ul><li>**نعم** – إذا كان تاريخ بدء التأجيل في فترة ما قبل تاريخ المعاملة، يتم دمج جميع المبالغ خلال فترة تاريخ المعاملة في سطر جدول تأجيل واحد.</li><li>**لا** – يتم الاحتفاظ بالمبالغ من جميع الفترات في بنود جدول تأجيل منفصلة.<p>إذا كان تاريخ بدء التأجيل في نفس الفترة أو فترة لاحقة من تاريخ المعاملة، فلن يكون لهذا الخيار أي تأثير.</p></li></ul><p>يمكن تحديث هذا الإعداد على مستوى المعاملة.</p> |
| تاريخ بدء التأجيل الافتراضي | <p>حدد القاعدة المستخدمة لتحديد تاريخ بدء جدول التأجيل:</p><ul><li>**تاريخ الحركة** – استخدم تاريخ المعاملة كتاريخ البدء.</li><li>**بداية الشهر الحالي** – استخدم اليوم الأول من الشهر الحالي كتاريخ البدء. إذا كان تاريخ المعاملة هو الأول من أي شهر، فإن أول الشهر الحالي هو تاريخ البدء.</li><li>**بداية الشهر التالي** – استخدم اليوم الأول من الشهر التالي كتاريخ البدء. إذا كان تاريخ المعاملة في الأول، فسيتم استخدام تاريخ المعاملة. بخلاف ذلك، يتم استخدام الأول من الشهر التالي.</li><li>**القاعدة 15** – إذا كان تاريخ المعاملة بين اليوم الأول والخامس عشر، فاستخدم اليوم الأول من الشهر الحالي كتاريخ البدء. إذا كان تاريخ المعاملة هو السادس عشر أو بعد ذلك، فاستخدم اليوم الأول من الشهر التالي كتاريخ البدء.</li></ul><p>يمكنك تحديث هذا الإعداد على مستوى الحركة.</p> |
| طريقة التأجيل قصير الأجل | <p>حدد طريقة التأجيل قصيرة المدى: **لا شيء**، أو **فترات التداول‬**، أو **سنة ثابتة**.</p><p>|
| طريقة ترحيل التأجيل | <p>حدد الطريقة المستخدمة لإنشاء معاملات التأجيل:</p><ul><li>**الميزانية العمومية** – استخدم طريقة ترحيل الميزانية العمومية لإنشاء معاملات التأجيل.</li><li>**الربح والخسارة** – استخدم طريقة ترحيل الأرباح والخسائر لإنشاء معاملات التأجيل. عند ترحيل الحركات، يمكنك مراجعة إيصال الفاتورة لرؤية الإدخالات الإضافية التي توازن الاعتراف الأولي ومبالغ الإقرار.</li></ul> |
| عكس الربح والخسارة في الائتمان | <p>**ملاحظة:** يتوفر هذا الحقل فقط عند تعيين حقل **طريقة تأجيل الترحيل** إلى **الربح والخسارة**.</p><p>حدد ما إذا كان يتم عكس مبالغ الأرباح والخسائر عند تطبيق عكس أو إنهاء أو استرداد على جدول الفواتير أو أمر المبيعات:</p><ul><li>**نعم** – إلغاء مبالغ الأرباح والخسائر، وتطبيق مبلغ تعديل الائتمان على جدول التأجيل.<p>إذا حدث الإلغاء في منتصف الطريق خلال فترة الفوترة، فسيتم تقسيم المبالغ بالتناسب.</p></li><li>**لا** – لا يتم إنشاء حركة عكسية للأرباح والخسائر عند تطبيق عكس أو إنهاء أو استرداد على جدول الفواتير أو أمر المبيعات.</li></ul> |
| علامة التبويب **الإقرار** | |
| نشر دفاتر اليومية العامة تلقائيًا | <p>حدد ما إذا كان يتم ترحيل إدخالات دفتر اليومية التي تم إنشاؤها بواسطة تأجيلات الإيرادات والمصروفات تلقائيًا أم لا:</p><ul><li>**نعم** – قم تلقائيًا بترحيل إدخالات دفتر اليومية التي تم إنشاؤها بواسطة تأجيلات الإيرادات والمصروفات.<p>**تلميح:** من خلال تحديد **نعم**، يمكنك المساعدة في منع التناقضات المحاسبية التي تنتج عن التغييرات اليدوية في الإيصالات.</p></li><li>**لا** – لا يتم ترحيل إدخالات دفتر اليومية التي تم إنشاؤها بواسطة تأجيلات الإيرادات والمصروفات تلقائيًا. يجب عليك نشر أي دفاتر يومية يدويًا.</li></ul> |
| تلخيص دفتر يومية الإقرار | <p>حدد ما إذا كانت قسائم الإقرار مجمعة بشكل افتراضي أم لا:</p><ul><li>**نعم** – قم بإنشاء إيصال واحد لجميع بنود الإقرار التي لها نفس التاريخ. يتم دمج جميع بنود الإيصال التي لها نفس الحساب في بند واحد.</li><li>**لا** – قم بإنشاء إيصال لكل بند من بنود الإقرار.</li></ul><p>يمكنك تحديث هذا الإعداد في صفحة **معالجة الإقرار**.</p> |
| اسم دفتر اليومية الافتراضي | حدد اسم دفتر اليومية لدفاتر اليومية التي تم إنشاؤها من عمليات تأجيل الإيرادات والمصروفات، مثل معالجة الإقرار. |
| وصف بند دفتر يومية الإقرار | <p>حدد الوصف الذي يظهر في وصف بند إيصال دفتر اليومية:</p><ul><li>**تواريخ بنود الجداول‬** – إظهار تواريخ سطر الجدول في وصف بند دفتر اليومية.</li><li>**إنشاء تفاصيل الحركة** – إظهار معلومات الحركة الأصلية في وصف بند دفتر اليومية.<p>**مثال:** ‏USMF-0001،‏ CIV-00839، إيرادات البرامج</p></li></ul> |
| علامة التبويب **التسلسلات الرقمية** | استخدم علامة التبويب هذه لتعيين القيم الافتراضية لتسلسلات أرقام الإيجار. يتم استخدام معالج إنشاء التسلسل الرقمي لإنشاء تسلسل رقمي وتعيينه تلقائيًا. لا يتعين عليك تغيير التسلسل الرقمي إلا إذا كنت تريد إجراء تغييرات يدوية على التسلسلات الرقمية التي تم إنشاؤها. |
| رقم الجدول | الرقم المتسلسل المستخدم لجداول التأجيل. |

## <a name="deferral-templates"></a>قوالب التأجيل

استخدم صفحة **قوالب التأجيل** لتعريف قوالب البند الثابت المستخدمة لجداول التأجيل.

فيما يلي بعض مزايا استخدام قالب:

* يتم حساب طول التأجيل تلقائيًا.
* أنت تسمح بجداول التأجيل التي تحتوي على فترات يتم فيها تخطي الإقرار.
* يمكنك أتمتة عمليات التأجيل من خلال تعيين النموذج لمنتج أو مجموعة منتجات أو فئة منتج أو عملاء أو مجموعة عملاء. يتم تعيين القالب من صفحة **الافتراضات المؤجلة**.

تتوفر عدة فترات زمنية للقوالب: يومية أو شهرية أو فترات مالية.

تتكون بنود القالب من نوع (**تم الإقرار به** أو **تم التخطي**) وطول الفترة. تحتوي البنود التي تم تخطيها على مبلغ 0 (صفر) في بنود جدول التأجيل. يمكن أن يكون هذا السلوك مفيدًا إذا كنت لا تريد التعرف على الإيرادات في جميع الفترات.

### <a name="create-a-deferral-template"></a>إنشاء قالب تأجيل

لإنشاء قالب تأجيل، اتبع هذه الخطوات.

1. في صفحة **قوالب التأجيل**، حدد **جديد**.
2. في حقل **القالب**، أدخل اسمًا.
3. في الحقل **الوصف**، أدخل وصفًا.
4. في حقل **تكرار الفترة**، حدد تكرار الفترة.
5. حدد **إضافة** لإضافة بند إلى أعلى قائمة البنود، أو حدد **إلحاق** لإضافة بند إلى أسفل القائمة.
6. في الحقل **النوع**، حدد نوع الفترة.
7. في حقل **طول الفترة**، حدد طول الفترة.
8. كرر الخطوات من 5 إلى 7 لكل بند إضافي تطلبه.
9. حدد **حفظ**.

## <a name="deferral-defaults"></a>افتراضيات التأجيل

استخدم صفحة **افتراضيات التأجيل** لإعداد حسابات التأجيل الافتراضية للعناصر وتعيين قوالب افتراضية للعناصر القابلة للتأجيل. يمكنك أيضًا إعداد حسابات مؤجلة للرسوم وتعيين قوالب للرسوم القابلة للتأجيل.

**تأجيل حسب الصنف**

بالنسبة للحركات التي تحتوي على عنصر (على سبيل المثال، أوامر المبيعات)، يمكنك تعيين حسابات وقوالب لعناصر وعملاء محددين. سيتم استخدام هذه الإعدادات كقيم افتراضية عند تأجيل الحركة. لجعل المعاملة قابلة للتأجيل بشكل افتراضي، يجب عليك إعداد العناصر في صفحة **العناصر القابلة للتأجيل**.

**التأجيل حسب الحساب**

بالنسبة للمعاملات التي لا تحتوي على عناصر (على سبيل المثال، دفاتر اليومية العامة)، يمكنك تحديد حسابات التأجيل. عند استخدام هذه الحسابات في بند معاملة، يتم تلقائيًا تمييز المعاملة على أنها مؤجلة. سيتم تعيين القالب المقابل وحساب الاعتراف إلى سطر المعاملة.

**جميع أنواع المعاملات (على سبيل المثال، في علامات التبويب أوامر المبيعات والمشتريات ودفتر اليومية العامة)**

الحسابات الموجودة في الصفحة هي الحسابات الرئيسية التي ليس لها أبعاد مالية. الأبعاد المالية لحساب الاعتراف مأخوذة من العميل أو العنصر، بناءً على مؤسستك.

يجب أن يكون لكل بند قالب إما قالب ذو خط مستقيم أو قالب قائم على الحدث. لا يمكن أن يكون كليهما.

### <a name="for-sales-orders"></a>بالنسبة لأوامر المبيعات

لتحديد القيم الافتراضية المؤجلة لأوامر المبيعات، اتبع هذه الخطوات.

1. في علامة التبويب **أمر المبيعات**، حدد نوع التأجيل.
2. حدد **إضافة** لإضافة سطر.
3. في **رمز الصنف**، حدد رمز الصنف. يحدد كود الصنف كيفية تطبيق القيم الافتراضية للتأجيل.
4. حدد كيفية تطبيق كود الصنف:

    * إذا تم تعيين **كود الصنف** إلى **الجدول** أو **المجموعة**، فحدد علاقة الصنف في حقل **علاقة الصنف**.
    * في حالة تعيين حقل **رمز الصنف** إلى **الفئة**، حدد علاقة الفئة في **علاقة الفئة**.
    * في حالة تعيين حقل **رمز الصنف** إلى **الكل**، تنطبق القيم الافتراضية على كل السجلات القابلة للتطبيق.

5. حدد كيفية تطبيق رمز الحساب:

    * إذا تم تعيين **رمز الحساب** إلى **الجدول** أو **المجموعة**، فحدد علاقة الحساب في حقل **علاقة الحساب**.
    * في حالة تعيين حقل **رمز الحساب** إلى **الكل**، ينطبق الحساب على كل السجلات.

6. في حقل **الحساب الرئيسي**، حدد الحساب الرئيسي للتأجيل.
7. في حالة تعيين حقل **طريقة ترحيل التأجيل** إلى **الربح والخسارة**، فحدد حساب الإيرادات الأولي في حقل **حساب الإيرادات الأولي** وحساب الإيرادات المقابل في حقل **حساب الإيرادات المقابل**.
8. في حالة تعيين حقل **طريقة التأجيل قصير الأجل** إلى **فترات التداول** أو **سنة ثابتة**، حدد حساب التأجيل قصير الأجل في حقل **حساب التأجيل قصير الأجل**.
9. بالنسبة للقالب، يمكنك تحديد **إضافة** لإضافة بند.
10. في **رمز الصنف**، حدد رمز الصنف.
11. حدد كيفية تطبيق كود الصنف:

    * إذا تم تعيين **كود الصنف** إلى **الجدول** أو **المجموعة**، فحدد علاقة الصنف في حقل **علاقة الصنف**.
    * في حالة تعيين حقل **رمز الصنف** إلى **الفئة**، حدد علاقة الفئة في حقل **علاقة الفئة**.
    * في حالة تعيين حقل **رمز الصنف** إلى **الكل**، تنطبق القيم الافتراضية على كل السجلات القابلة للتطبيق.

12. حدد كيفية تطبيق رمز الحساب:

    * إذا تم تعيين **رمز الحساب** إلى **الجدول** أو **المجموعة**، فحدد علاقة الحساب في حقل **علاقة الحساب**.
    * في حالة تعيين حقل **رمز الحساب** إلى **الكل**، ينطبق الحساب على كل السجلات المتاحة.
    * حدد قالب البند المستقيم في حقل  **قالب البند المستقيم** أو القالب المستند إلى الحدث في حقل **القالب المستند إلى الحدث**.

13. حدد **حفظ**.

### <a name="for-purchase-orders"></a>بالنسبة لأوامر الشراء

لتحديد القيم الافتراضية المؤجلة لأوامر الشراء، اتبع هذه الخطوات.

1. في علامة التبويب **شراء**، حدد نوع التأجيل.
2. حدد **إضافة** لإضافة سطر.
3. في **رمز الصنف**، حدد رمز الصنف.
4. حدد كيفية تطبيق كود الصنف:

    * إذا تم تعيين **كود الصنف** إلى **الجدول** أو **المجموعة**، فحدد علاقة الصنف في حقل **علاقة الصنف**.
    * في حالة تعيين حقل **رمز الصنف** إلى **الفئة**، حدد علاقة الفئة في حقل **علاقة الفئة**.
    * في حالة تعيين حقل **رمز الصنف** إلى **الكل**، تنطبق القيم الافتراضية على كل السجلات القابلة للتطبيق.

5. حدد كيفية تطبيق رمز الحساب:

    * إذا تم تعيين **رمز الحساب** إلى **الجدول** أو **المجموعة**، فحدد علاقة الحساب في حقل **علاقة الحساب**.
    * في حالة تعيين حقل **رمز الحساب** إلى **الكل**، ينطبق الحساب على كل السجلات المتاحة.

6. في حقل **الحساب الرئيسي**، حدد الحساب الرئيسي للتأجيل.
7. في حالة تعيين حقل **طريقة ترحيل التأجيل** إلى **الربح والخسارة**، فحدد حساب الإيرادات الأولي في حقل **حساب الإيرادات الأولي** وحساب الإيرادات المقابل في حقل **حساب الإيرادات المقابل**.
8. في حالة تعيين حقل **طريقة التأجيل قصير الأجل** إلى **فترات التداول** أو **سنة ثابتة**، حدد حساب التأجيل قصير الأجل في حقل **حساب التأجيل قصير الأجل**.
9. بالنسبة للقالب، حدد **إضافة** لإضافة بند. 
10. في **رمز الصنف**، حدد رمز الصنف.
11. حدد كيفية تطبيق كود الصنف:

    * إذا تم تعيين **كود الصنف** إلى **الجدول** أو **المجموعة**، فحدد علاقة الصنف في حقل **علاقة الصنف**.
    * في حالة تعيين حقل **رمز الصنف** إلى **الفئة**، حدد علاقة الفئة في حقل **علاقة الفئة**.
    * في حالة تعيين حقل **رمز الصنف** إلى **الكل**، تنطبق القيم الافتراضية على كل السجلات القابلة للتطبيق.

12. حدد كيفية تطبيق رمز الحساب:

    * إذا تم تعيين **رمز الحساب** إلى **الجدول** أو **المجموعة**، فحدد علاقة الحساب في **علاقة الحساب**.
    * في حالة تعيين حقل **رمز الحساب** إلى **الكل**، ينطبق الحساب على كل السجلات المتاحة.
    * حدد قالب البند المستقيم في حقل  **قالب البند المستقيم** أو القالب المستند إلى الحدث في حقل **القالب المستند إلى الحدث**.

13. حدد **حفظ**.

### <a name="for-general-journals"></a>بالنسبة لدفاتر اليومية العامة

لتحديد القيم الافتراضية المؤجلة لإدخالات دفتر اليومية العامة، اتبع هذه الخطوات.

1. حدد علامة التبويب **دفتر اليومية العام**.
2. بالنسبة للتأجيل، حدد **إضافة** لإضافة بند.
3. في حالة تعيين حقل **طريقة التأجيل قصير الأجل** إلى **فترات التداول** أو **سنة ثابتة**، حدد حساب التأجيل قصير الأجل في حقل **حساب التأجيل قصير الأجل**.
4. في الحقل **حساب التأجيل**، حدد حساب التأجيل.
5. في الحقل **حساب الإقرار**، حدد حساب الإقرار.
6. في حالة تعيين حقل **طريقة ترحيل التأجيل** إلى **الربح والخسارة**، فحدد حساب الإيرادات الأولي في حقل **حساب الإيرادات الأولي** وحساب الإيرادات المقابل في حقل **حساب الإيرادات المقابل**.
7. حدد قالب البند المستقيم في حقل  **قالب البند المستقيم** أو القالب المستند إلى الحدث في حقل **القالب المستند إلى الحدث**.
8. حدد **حفظ**.

### <a name="for-free-text-invoices"></a>بالنسبة للفواتير ذات النص الحر

لتحديد القيم الافتراضية المؤجلة لفواتير النص الحر، اتبع هذه الخطوات.

1. حدد علامة التبويب **الفاتورة ذات النص الحر**.
2. بالنسبة للتأجيل، حدد **إضافة** لإضافة بند.
3. حدد كيفية تطبيق رمز الحساب:

    * إذا تم تعيين **رمز الحساب** إلى **الجدول** أو **المجموعة**، فحدد علاقة الحساب في حقل **علاقة الحساب**.
    * في حالة تعيين حقل **رمز الحساب** إلى **الكل**، ينطبق رمز الحساب على كل السجلات المتاحة.

4. في الحقل **حساب التأجيل**، حدد حساب التأجيل.
5. في حالة تعيين حقل **طريقة التأجيل قصير الأجل** إلى **فترات التداول** أو **سنة ثابتة**، حدد حساب التأجيل قصير الأجل في حقل **حساب التأجيل قصير الأجل**.
6. في الحقل **حساب الإقرار**، حدد حساب الإقرار.
7. في حالة تعيين حقل **طريقة ترحيل التأجيل** إلى **الربح والخسارة**، فحدد حساب الإيرادات الأولي في حقل **حساب الإيرادات الأولي** وحساب الإيرادات المقابل في حقل **حساب الإيرادات المقابل**.
8. حدد قالب البند المستقيم في حقل  **قالب البند المستقيم** أو القالب المستند إلى الحدث في حقل **القالب المستند إلى الحدث**.
9. حدد **حفظ**.

### <a name="for-invoice-journals"></a>بالنسبة لدفاتر يومية الفواتير

لتحديد القيم الافتراضية المؤجلة لإدخالات دفتر يومية الفاتورة، اتبع هذه الخطوات.

1. حدد علامة التبويب **دفتر يومية الفاتورة**.
2. بالنسبة للتأجيل، حدد **إضافة** لإضافة بند.
3. حدد كيفية تطبيق رمز الحساب:

    * إذا تم تعيين **رمز الحساب** إلى **الجدول** أو **المجموعة**، فحدد علاقة الحساب في حقل **علاقة الحساب**.
    * في حالة تعيين حقل **رمز الحساب** إلى **الكل**، ينطبق رمز الحساب على كل السجلات المتاحة.

4. في الحقل **حساب التأجيل**، حدد حساب التأجيل.
5. في حالة تعيين حقل **طريقة التأجيل قصير الأجل** إلى **فترات التداول** أو **سنة ثابتة**، حدد حساب التأجيل قصير الأجل في حقل **حساب التأجيل قصير الأجل**.
6. في الحقل **حساب الإقرار**، حدد حساب الإقرار.
7. في حالة تعيين حقل **طريقة ترحيل التأجيل** إلى **الربح والخسارة**، فحدد حساب الإيرادات الأولي في حقل **حساب الإيرادات الأولي** وحساب الإيرادات المقابل في حقل **حساب الإيرادات المقابل**.
8. حدد قالب البند المستقيم في حقل  **قالب البند المستقيم** أو القالب المستند إلى الحدث في حقل **القالب المستند إلى الحدث**.
9. حدد **حفظ**.

### <a name="items-that-are-deferred-by-default"></a>العناصر التي يتم تأجيلها بشكل افتراضي

استخدم صفحة **العناصر المؤجلة افتراضيًا** لتحديد العناصر المؤجلة افتراضيًا. يمكنك إعداد أنواع المعاملات التي سيتم تأجيل البنود من أجلها. يمكنك تحديد ما إذا كان سيتم تأجيل عنصر واحد، أو مجموعة عناصر كاملة أو فئة.

عند إعداد العناصر على أنها مؤجلة، حدد الحسابات والقوالب الافتراضية في صفحة **افتراضيات التأجيل**. إذا لم يتم تحديد الحسابات والقوالب، فلن يتم تأجيل بنود الحركة حيث يتم إدخال هذه العناصر.

بالنسبة للأصناف المؤجلة بناءً على فئة المبيعات أو الشراء المرتبطة بها، تستند إعدادات التأجيل إلى الفئة. ومع ذلك، إذا لم يتم تحديد الفئة في حقل **فئة العلاقة**، فإنه يتم استخدام إعدادات التأجيل للفئة الأعلى في الترتيب. على سبيل المثال، يمكنك إضافة فئة مبيعات **فيديو المنازل** وليس فئة مبيعات **التلفاز**. عند إضافة عنصر تأجيل مرتبط بفئة **التلفاز**، يتم استخدام إعدادات التأجيل لـ **فيديو المنازل** للصنف.

### <a name="set-up-deferred-items"></a>إعداد الأصناف المؤجلة

لإعداد العناصر المؤجلة افتراضيًا، اتبع هذه الخطوات.

1. في صفحة **الأصناف المؤجلة حسب الإعداد الافتراضي**، حدد علامة التبويب التي تريدها: **أمر المبيعات** أو **شراء**.
2. حدد **إضافة** لإضافة سطر.
3. في **رمز الصنف**، حدد رمز الصنف.
4. حدد كيفية تطبيق كود الصنف:

    * إذا تم تعيين **كود الصنف** إلى **المجموعة** أو **الجدول**، فحدد علاقة الصنف في حقل **علاقة الصنف**.
    * في حالة تعيين حقل **رمز الصنف** إلى **الفئة**، حدد علاقة الفئة في حقل **علاقة الفئة**.

5. كرر الخطوات من 2 إلى 4 لكل بند إضافي تطلبه.
6. حدد **حفظ**.

## <a name="deferred-charges"></a>التكاليف المؤجلة

استخدم صفحة **رسوم التأجيل** لتحديد المصاريف المؤجلة افتراضيًا.

> [!NOTE]
> * حاليًا، الرسوم القابلة للتأجيل متاحة لأوامر المبيعات فقط.
> * يمكن تأجيل الرسوم على مستوى البند فقط. لتأجيل مصاريف على مستوى رأس أمر المبيعات، يمكنك إعداد المصاريف كبند مؤجل في بند منفصل في أمر المبيعات.
> * لتأجيل رسم فاتورة نصية مجانية، يجب إدخال الرسوم كبند منفصل للفاتورة المؤجلة.
> * هذه الوظيفة غير متاحة لرسوم الدعم ووظيفة تقسيم الإيرادات.

### <a name="set-up-deferred-charges"></a>إعداد التكاليف المؤجلة

لإعداد المصاريف المؤجلة، اتبع هذه الخطوات.

1. في صفحة **المصاريف المؤجلة**، حدد **إضافة** لإضافة بند.
2. في حقل **رمز المصاريف**، حدد رمز المصاريف.
3. في حقل **علاقة المصاريف**، حدد علاقة المصاريف.
4. كرر الخطوات من 1 إلى 3 لكل بند إضافي تطلبه.
5. حدد **حفظ**.

## <a name="event-based-deferral-templates"></a>قوالب التأجيل المستندة إلى الأحداث

استخدم صفحة **قوالب التأجيل المستندة إلى الأحداث** لتحديد قوالب التأجيل المستندة إلى الحدث والتي يمكنك استخدامها في معاملات التأجيل والتعيين إلى صفحة **افتراضيات التأجيل**.

### <a name="create-an-event-based-template"></a>إنشاء قالب مستند إلى الحدث

لإنشاء قالب تأجيل مستند إلى الحدث، اتبع الخطوات التالية.

1. في صفحة **قوالب التأجيل المستندة إلى الأحداث**، حدد **جديد**.
2. في حقل **القالب**، قم بإدخال اسم فريد لمجموعة القالب.
3. في الحقل **الوصف**، أدخل وصفًا.
4. في حقل **نوع التخصيص**، حدد نوع التخصيص:

    * **المبلغ المتغير** – قم بتخصيص مبلغ محدد لكل بند يتم إدخاله.
    * **المبلغ المساوي** – قم بتخصيص نفس المبلغ لكل بند يتم إدخاله. 
    * **النسبة المئوية** – قم بتخصيص مبلغ بناءً على قيمة النسبة المئوية التي تم إدخالها لكل بند.
    * **النسبة المئوية للإكمال** – قم بتخصيص قيمة إكمال تراكمية لكل بند يتم إدخاله.
    * **الكمية المتغيرة** – قم بتخصيص كمية محددة لكل بند يتم إدخاله.

5. قم بتعيين الخيار **إنشاء الأحداث المنفصلة لكل وحدة** إلى **نعم**، إذا كنت تريد تقسيم كل سطر حدث بالتساوي على عدد الوحدات في حركة الفاتورة. قم بتعيينه إلى **لا** إذا كنت لا تريد تقسيم بنود الحدث.
6. في حقل **حساب انتهاء الصلاحية**، حدد حساب انتهاء الصلاحية.
7. حدد **إضافة** لإضافة بند إلى أعلى قائمة البنود، أو حدد **إلحاق** لإضافة بند إلى أسفل القائمة.
8. في حقل **الوصف**، أدخل وصفًا للحدث.
9. في حالة تعيين حقل **نوع التخصيص** إلى **النسبة المئوية**، فحدد النسبة المئوية للتخصيص في حقل **النسبة المئوية للتخصيص**. يجب أن تتراوح النسبة المئوية بين 0 (صفر) و100. إذا تركت حقل **النسبة المئوية للتخصيص** فارغًا، فسيتم اعتبار النسبة المئوية 0. يظهر مجموع جميع النسب المئوية في الحقل **النسبة المئوية الإجمالية** في أسفل الصفحة ويجب أن يساوي 100.
10. في الحقل **أشهر حتى انتهاء الصلاحية**، حدد عدد الأشهر التي يكون فيها الحدث صالحًا. يتم إدخال تاريخ انتهاء الصلاحية في تأجيل المعاملة تلقائيًا بناءً على هذه القيمة.
11. حدد خانة الاختيار **الإقرار عند الترحيل** للاعتراف بالإيرادات تلقائيًا عند ترحيل الحركة. إذا تركت خانة الاختيار بدون تحديد، فيجب الإقرار بالإيرادات يدويًا.
12. في حقل **حساب الإقرار**، حدد حساب الإقرار للحدث، إذا كان الحدث يستخدم حسابًا مختلفًا عن جدول التأجيل الكامل. يتم استخدام هذا الحقل مع مربع الاختيار **الإقرار عند الترحيل**.
13. كرر الخطوات من 7 إلى 12 لكل بند إضافي تطلبه.
14. حدد **حفظ**.
