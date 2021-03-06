---
title: تكوين أنواع أحداث الحياة
description: تستخدم Microsoft Dynamics 365 Human Resources أنواع الأحداث الحياتية لتحديد الأحداث التي تكون صالحة لتحديث تسجيل ميزات الموظفين.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c382299014e3f823bc2cd210749aae8c091c5f23
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111362"
---
# <a name="configure-life-event-types"></a>تكوين أنواع أحداث الحياة

تستخدم Microsoft Dynamics 365 Human Resources أنواع الأحداث الحياتية لتحديد الأحداث التي تكون صالحة لتحديث تسجيل ميزات الموظفين. على سبيل المثال، الزواج أو إنجاب طفل. يمكن ربط كل معرف نوع حدث حياتي بنوع حدث حياتي واحد. على سبيل المثال، إذا قمت بإنشاء معرف حدث حياتي يسمي تغيير العنوان المقترن بتغيير عنوان موظف نوع الحدث، فإنه يمكنك إنشاء معرف آخر يسمى تغيير عنوان الموظف وربطه بتغيير عنوان موظف نوع الحدث الحياتي. 

بعد أن تقوم بإنشاء أنواع الأحداث الحياتية، فإنه يجب عليك ربطها بأنواع الخطط. لمزيد من المعلومات، راجع [إنشاء أنواع الخطط](hr-benefits-setup-plan-types.md).

   > [!NOTE]
   > عندما تقوم بإنشاء حدث حياتي، فإنه يجب عليك ربطه بنوع خطة. لمزيد من المعلومات، راجع [إنشاء أنواع الخطط](hr-benefits-setup-life-event-types.md).

## <a name="create-a-life-event-type"></a>إنشاء نوع الحدث الحياتي

1. في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **أنواع الأحداث الحياتية**.

2. حدد **جديد**.

3. حدد قيمًا للحقول التالية:

   | الحقل | ‏‏الوصف |
   | --- | --- |
   | **معرف نوع حدث الحياة** | المعرف الفريد لنوع الحدث الحياتي. |
   | **‏‏الوصف** | وصف نوع الحدث الحياتي. |
   | **نوع حدث الحياة** | حافز لتحديث تسجيل مزايا الموظف. للحصول على قائمة بالأحداث الحياتية، راجع [الأحداث الحياتية](hr-benefits-setup-payment-frequencies.md?life-events) أدناه. |

4. حدد **حفظ**.

## <a name="view-attached-plans"></a>عرض الخطط المرفقة

يمكنك عرض قائمة بالخطط المرفقة بنوع الحدث الحياتي المحدد. يتم إرفاق الأحداث الحياتية بنوع خطة، كما ترتبط أنواع الخطط بخطة. 

1. في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **أنواع الأحداث الحياتية**.

2. حدد **الإجراءات**.

3. حدد **الخطط المرفقة**.

## <a name="life-events"></a>أحداث الحياة

يمكنك الاختيار من بين الأحداث الحياتية التالية عند إنشاء نوع حدث حياتي:

| حدث الحياة | الموقع | المشغل |
| --- | --- | --- |
| **تغيير الحالة الاجتماعية** | عامل > ملف التعريف > المعلومات الشخصية > الحالة الاجتماعية| تغيير في الحالة الاجتماعية |
| **تغيير حالة التوظيف** | <ul><li>عامل > توظيف</li><li>صفحة سجل التوظيف</li></ul> | تغيير في حالة التوظيف |
| **تغيير عنوان الموظف** | <ul><li>عامل > ملف التعريف > العناوين </li><li>العامل > المعلومات الشخصية > جهات الاتصال الشخصية > العنوان</li></ul> العنوان الذي تمت إضافته أو تحريره أو حذفه |
| **تغيير المعال** | <ul><li>عامل > ملف التعريف > المعلومات الشخصية > جهات الاتصال الشخصية > إضافة معال أو حذفه</li><li>خدمة الموظف الذاتية</li></ul> | المعال الذي تمت إضافته أو حذفه. يجب أن تكون علاقة جهة الاتصال الشخصية طفل أو زوج/زوجة أو شريك محلي أو زوج/زوجة سابق. يؤدي تحديث التاريخ **صالح من** إلى تشغيل الحدث الحياتي. وإذا لم تقم بتحديث ذلك التاريخ، فلن يتم تشغيل أي حدث حياتي. |
| **الميلاد أو التبني (معال)** | <ul><li>عامل > ملف التعريف > المعلومات الشخصية > جهات الاتصال الشخصية > تفاصيل المعال</li><li>خدمة الموظف الذاتية</li></ul> | تم تعبئة حقل **تاريخ التبني**. تاريخ ميلاد الطفل مطلوب. |
| **فقدان التغطية (الزوج أو الزوجة/الشريك المحلي)** | عامل > ملف التعريف > المعلومات الشخصية > جهات الاتصال الشخصية > تفاصيل المعال > فقد التغطية | **فقد التغطية** المحددة لجهة اتصال شخصية، بالإضافة إلى **تاريخ السريان** |
| تغيير توظيف الشريك المحلي | عامل > ملف التعريف > المعلومات الشخصية > جهات الاتصال الشخصية > تفاصيل المعال > موظف. | <ul><li>تم إنشاء سجل تفاصيل المعال والخانة **تم توظيف الجهة الشخصية** = نعم</li><li>تم تغيير الخانة **تم توظيف الجهة الشخصية** (نعم أو لا)</li></ul> |
| **إذن الغياب (الزوج أو الزوجة/الشريك المحلي)** | عامل > ملف التعريف > المعلومات الشخصية > جهات الاتصال الشخصية > تفاصيل المعال > إذن غياب | <ul><li>تم إنشاء سجل تفاصيل المعال وتم تعبئة **EhrLOAEffectiveDate**</li><li>تم تغيير **personPrivateDetails.EhrIsLOA** (نعم أو لا)</li><li>تم تغيير **personPrivateDetails.EhrLOAEffectiveDate**</li></ul> |
| **تغيير في التغطية (منصب)** | <ul><li>عامل > تعيين المنصب > تعيينات منصب العامل</li><li>المناصب > المناصب</li></ul> | <ul><li>التغيير إلى المنصب في سجلات تعيين منصب العامل</li><li>تغيير تعيين العامل في المنصب</li></ul> |
| **الرعاية الطبية (موظف / معال)** | عامل > ملف التعريف > المعلومات الشخصية > جهات الاتصال الشخصية > تفاصيل المعال > تاريخ سريان الرعاية الطبية | لا يتم تشغيله تلقائيًا عندما تقوم جهة اتصال شخصية بإدخال تاريخ سريان. |
| **دعم الحكم القضائي** | عامل > ملف التعريف > المعلومات الشخصية > جهات الاتصال الشخصية > المعال > ‏‫دعم المحكمة (أمر إعالة الطفل الطبية المؤهلة/أمر العلاقات المحلية المؤهلة وتواريخ السريان) | لا يقوم بتشغيل أية تحديثات تلقائية. ولا يؤثر ذلك على الأهلية؛ يسجل حدث حياتي. |
| **وفاة** | عامل > ملف التعريف > المعلومات الشخصية > تاريخ الوفاة | يتم إدخال تاريخ الوفاة |
| **دليل التأمين** | <ul><li>عامل > عامل > الإصدارات > سجل التوظيف > مدير التاريخ > تفاصيل الميزات</li><li> عامل > توظيف > تفاصيل الميزات > تاريخ التحقق من الصحة</li></ul> | <ul><li>يدخل عامل في تاريخ التحقق من الصحة</li><li>يقوم عامل بتعيين الحقل EvidenceOfInsurability إلى **نعم**</li></ul> |
| **المستفيد** | العامل > ملف التعريف > المعلومات الشخصية > جهات الاتصال الشخصية | تتم إضافة جهة اتصال شخصية ويتم ملء خانة **المستفيد** و **تاريخ السريان**. يجب أن تكون جهة الاتصال الشخصية من نوع **الطفل** أو **الزوج/الزوجة** أو **شريك محلي** أو **نسيب** أو **جهة اتصال أسرية** أو **جهة اتصال أخرى** أو **أب/أم** أو **ممتلكات مستفيد** أو **مؤسسة مستفيدة** أو **صندوق ائتمان مستفيد**. |
| **الرعاية الطبية للموظف** | عامل > عامل > الإصدارات > سجل التوظيف > مدير التاريخ > تفاصيل الميزات | <ul><li>تم تغيير **EhrMedicareEligibilityDate**</li><li>تم تعيين **MedicareEligibile** إلى **نعم**</li></ul> |
| **تاريخ الميلاد** | عامل > ملف التعريف > المعلومات الشخصية > جهات الاتصال الشخصية > تفاصيل المعال > تاريخ الميلاد | تتم إضافة تاريخ الميلاد أو تحديثه (وليس بعد معالجة التغيير في الحدث الحياتي). مثال: إذا كانت **خيارات أهلية جهات الاتصال الشخصية‬‏‫** لطفل معينة إلى العمر: 26 سنة في الإعداد > المزايا > خيارات أهلية جهات الاتصال الشخصية، وإذا قام موظفو الموارد البشرية بتشغيل معالجة تغيير أحداث الحياة في أي يوم بعد أن يصبح عمر المعال 26 سنة، تظهر رسالة تنبيه تفيد بأن المعاد لم يعد متأهلاً للاستفادة من التغطية. |
| **تغيير أهلية العامل (غير خاص بالولايات المتحدة)** | <ul><li>عامل > توظيف</li><li>عامل > عامل > إصدارات > سجل التوظيف</li></ul> | <ul><li>تغيير نوع الموظف أو فئة التوظيف أو الحقول الخمسة للأهلية التي يمكن للمستخدم تحديدها</li><li>يعمل **HcmEmploymentDetail.EhrEmploymentType** على تغيير (معالج فقط بواسطة سجلات تفاصيل التوظيف *التي تم تغييرها*، لم تتم المعالجة لسجلات التوظيف *الجديدة*، مثل إعادة التعيين والإنهاء)</li></ul> |
| **تجاوز أهلية جديدة (غير خاص بالولايات المتحدة)** | الموارد البشرية المتقدمة> ميزات > خطط > ميزات > تجاوز قاعدة الأهلية | استخدام معالجة حدث الحياتي | EhrBenefitEligibilityRuleOverride.ValidFrom |
| **تغيير تجاوز قاعدة الأهلية (غير خاص بالولايات المتحدة)** | الموارد البشرية المتقدمة> ميزات > خطط > ميزات > تجاوز قاعدة الأهلية | استخدام معالجة الحدث الحياتي (فقط يأخذ بالتغييرات على الحقول **ValidFrom** و **ValidTo** عند تجاوز القاعدة الأهلية) |
| **انتهاء صلاحية تجاوز قاعدة الأهلية (غير خاص بالولايات المتحدة)** | الموارد البشرية المتقدمة> ميزات > خطط > ميزات > تجاوز قاعدة الأهلية | استخدام معالجة تغيير حدث حياتي. على سبيل المثال، إذا قمت بتحرير تاريخ انتهاء صلاحية قاعدة أهلية الخطة ليكون اليوم عند الساعة 5:00 مساءً أو في أي وقت بعد الساعة 5:00 مساءً أو في الأيام التالية، ثم إجراء معالجة تغيير الحدث الحياتي، تظهر سالة تذكر أنه قد تم انتهاء صلاحية قاعدة الأهلية. |
| **خطة الميزة الجديدة (غير خاص بالولايات المتحدة)** | الموارد البشرية المتقدمة > ميزات > خطط > جديد | <ul><li>تتم إضافة خيارات الأهلية إلى خطة حالية</li><li>تتم إضافة خطة جديدة بخيارات أهلية مرفقة</li></ul></br></br>يجب أن يقوم موظفو الموارد البشرية بتشغيل معالجة أهليه الحدث الحياتي في هذا المثيل. |
| **تغيير قاعدة الأهلية (غير خاص بالولايات المتحدة)** | الموارد البشرية المتقدمة> ميزات > قواعد/خيارات > قواعد الأهلية | استخدام معالجة أهلية حدث حياتي. يتم التسجيل عندما تحتوي سجلات **EhrBenefitEligibilityRule** على القواعد التالية المتغيرة: **UseEmplCategory** أو **UseEmplStatus** أو **UseEmplType**. يقوم فقط بتحديث حركات الحدث الحياتي الموجود بالفعل لقاعدة أو معايير أهلية تم تغييرها. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]