---
title: ترحيل أمر المبيعات
description: توفر هذه المقالة معلومات عن علامة تبويب أمر المبيعات في صفحة ملف تعريف ترحيل المخزون.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 5ea1c3c90b32d18243615e3ff283e1e818ac23b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886302"
---
# <a name="sales-order-posting"></a>ترحيل أمر المبيعات

تُستخدم علامة تبويب **أمر المبيعات** في صفحة **ملفات تعريف ترحيل المخزون** للتحكم في كيفية ترحيل أوامر المبيعات إلى دفتر الأستاذ العام. يتم ترحيل نشاطين رئيسيين إلى دفتر الأستاذ العام لأمر المبيعات: 

- إيصال التعبئة
- الفاتورة

لكي يتم ترحيل حركة فعلية (إيصال التعبئة) إلى دفتر الأستاذ العام لأمر مبيعات، يجب استيفاء الشروط التالية:

- في الصفحة **معلمات إدارة المخزون والمستودعات**، يجب أن تكون خانة الاختيار **ترحيل إيصال التعبئة في دفتر الأستاذ‬** محددة.
- في صفحة **مجموعة نماذج الصنف‬** للصنف المحدد في بند أمر المبيعات، يجب أن تكون خانة الاختيار **ترحيل المخزون الفعلي في دفتر الأستاذ** محددة.
- في صفحة **ملف تعريف ترحيل المخزون**، يجب تحديد الحسابات الرئيسية لأنواع الترحيل التالية:
  - تكلفة الوحدات، التي تم تسليمها
  - تكلفة البضائع المبيعة، والتي تم تسليمها

لكي يتم ترحيل حركة مالية (فاتورة) إلى دفتر الأستاذ العام لأمر مبيعات، يجب استيفاء الشروط التالية:

- في صفحة **مجموعة نماذج الصنف‬** للصنف المحدد في بند أمر المبيعات، يجب أن تكون خانة الاختيار **ترحيل المخزون المادي في دفتر الأستاذ** محددة.
- يجب تحديد الحسابات الرئيسية في صفحة **ملف تعريف ترحيل المخزون**، لأنواع الترحيل التالية:
  - تكلفة الوحدات، المفوترة
  - تكلفة البضائع المبيعة، المفوترة
  - الإيراد
  - الخصم\*

> [!NOTE]
> حساب الخصم اختياري. يتطلب العديد من أنظمة المحاسبة، مثل GAAP وIFRS ، أن تؤدي الخصومات إلى تقليل إيرادات المبيعات، وبالتالي لا يتم استخدام هذه الحسابات في العديد من السيناريوهات. إذا كانت الأنظمة المحلية تسمح بذلك، فاستخدم حسابًا رئيسيًا منفصلاً لترحيل الجزء المخصوم من سعر المبيعات.

لترحيل قيمة الإيرادات المؤجلة (المقدرة) إلى دفتر الأستاذ العام عند إنشاء إيصال تعبئة لأمر مبيعات، يجب استيفاء الشروط التالية:

- في صفحة **مجموعة نماذج الصنف‬** للصنف المحدد في بند أمر المبيعات، يجب أن تكون خانة الاختيار **ترحيل المخزون الفعلي في دفتر الأستاذ** محددة.
- في الصفحة **مجموعة نماذج الصنف‬**، يجب أن تكون خانة الاختيار **ترحيل إلى حساب الإيراد المؤجل عند تسليم المبيعات‬** محددة.
- في الصفحة **معلمات إدارة المخزون والمستودعات**، يجب أن تكون خانة الاختيار **ترحيل إيصال التعبئة في دفتر الأستاذ‬** محددة.
- في الصفحة **معلمات إدارة المخزون والمستودعات**، يجب أن تكون خانة الاختيار **ترحيل ضريبة المبيعات الفعلية‬‬** محددة.
- في الصفحة **معلمات الحسابات المدينة‬**، يجب أن تكون خانة الاختيار **ترحيل إيصال التعبئة في دفتر الأستاذ‬** محددة.
- في صفحة **ملف تعريف ترحيل المخزون**، يجب تحديد الحسابات الرئيسية لأنواع الترحيل التالية:
  - الإيراد المؤجل عند التسليم
  - الإيراد المؤجل المقابل عند التسليم
  - ضريبة مبيعات مؤجلة عند التسليم

> [!NOTE]
> نحن ننصح بشكل عام بتمكين الخيارين **ترحيل المخزون الفعلي** و **ترحيل إيصال التعبئة في دفتر الأستاذ‬**. يمكن أن يساعد تمكين هذه الخيارات في تسريع إجراءات إقفال نهاية الشهر، بسبب عدم وجود تأجيلات يجب حسابها وترحيلها يدويًا. بالإضافة إلى ذلك، ستعكس البيانات المالية المبالغ المؤجلة تلقائيًا دون تدخل يدوي.

> [!IMPORTANT]
> لا يتم استخدام الخيار **ترحيل إلى حساب الإيراد المؤجل عند تسليم المبيعات‬** مع إقرار الإيرادات. لمزيد من المعلومات حول إقرار الإيرادات، انتقل إلى [نظرة عامة على إقرار الإيرادات](/accounts-receivable/revenue-recognition-overview.md)

## <a name="sample-posting-profile-configuration"></a>تكوين عينة ملف تعريف الترحيل 

يعرض الجدول التالي أمثلة لأنواع الترحيل الافتراضية مع عينة من الحسابات الرئيسية والأوصاف:
 
- يشير العمود **حساب المقاصة** إلى أن نوع الترحيل هو حساب مقاصة. يتم عكس المبلغ الذي تم ترحيله في هذا الحساب تلقائيًا عند ترحيل حركة لاحقة. 
- يشير العمود **P/F** إلى **P** للترحيل الفعلي و **F** للترحيل المالي. 
- يشير العمود **متابعة** إلى ما إذا كان الحساب الرئيسي لنوع ترحيل معين يتطابق مع نوع ترحيل آخر. تشير القيمة الموجودة في العمود إلى نوع الترحيل المستخدم بشكل عام.

> [!NOTE]
> تعتبر الحسابات الرئيسية وأسماء الحسابات الرئيسية هذه مجرد اقتراحات. نوصي بالعمل مع المحاسبين لتحديد التكوين الأفضل لاحتياجات عملك.


| نوع الترحيل | مثال على الحساب الرئيسي | مثال على اسم الحساب الرئيسي | نوع الحساب | مدين/دائن؟ | حساب مقاصة. | P/F | متابعة | ‏‏الوصف‬ |
|------------|------------------------|-------------------------|--------------|---------|-------------------|------------|------|-------------------------|
| تكلفة الوحدات، التي تم تسليمها | 140100</br>140101 | مخزون المواد</br>المواد المشحونة وغير المفوترة | الأصل | دائن‬ | ‏‏نعم‬ | P | تكلفة الوحدات، المفوترة | يستخدم عند ترحيل قسيمة تعبئة أمر مبيعات. الحساب المقابل لهذا الحساب هو تكلفة السلع المبيعة، التي تم تسليمها. يتم عكس المبلغ في هذا الحساب عند ترحيل فاتورة أمر مبيعات. قد ترغب في استخدام حساب المواد المشحونة غير المفوتر لتمثيل المخزون المادي، وحجز حساب مخزون المواد للتحديث المالي. |
| تكلفة البضائع المبيعة، والتي تم تسليمها | 500150 | تكلفة البضائع المبيعة المؤجلة | المصروفات | مدين | ‏‏نعم‬ | P  | يستخدم عند ترحيل قسيمة تعبئة أمر مبيعات. الحساب المقابل لهذا الحساب هو تكلفة الوحدات، التي تم تسليمها. يتم عكس المبلغ في هذا الحساب عند ترحيل فاتورة أمر مبيعات. |
| تكلفة الوحدات، المفوترة | 140100 | مخزون المواد | الأصل | دائن‬ | لا | الجمعة | تكلفة الوحدات، التي تم تسليمها | يستخدم عند ترحيل فاتورة أمر مبيعات. الحساب المقابل لهذا الحساب هو تكلفة السلع المبيعة، المفوترة. يمثل هذا الحساب المخزون في الميزانية العمومية. |
| تكلفة البضائع المبيعة، المفوترة | 500100 | مواد COGS | المصروفات | مدين | لا | الجمعة  | يستخدم عند ترحيل فاتورة أمر مبيعات. الحساب المقابل لهذا الحساب هو تكلفة الوحدات، المفوترة. يمثل هذا الحساب COGS على كشف P&amp;L. |
| الإيراد (إيراد أمر المبيعات*) | 400100 | مواد الإيرادات | الإيراد | دائن‬ | لا | الجمعة   | يستخدم عند ترحيل فاتورة أمر مبيعات. الحساب المقابل لهذا الحساب هو حساب الملخص (رصيد العميل*) على **ملف تعريف ترحيل الحسابات المدينة**. |
| العمولة (المبيعات، العمولة*) | 602150 | مصروفات العمولة | المصروفات | مدين | لا | الجمعة  | يُستخدم عند تمكين العمولة وحسابها للمبيعات وترحيلها أثناء عملية فوترة أمر المبيعات. الحساب المقابل لهذا الحساب هو العمولة مستحقة الدفع. |
| مقاصة العمولة‬ (المبيعات، مقاصة العمولة‬*) | 201110 | العمولات مستحقة الدفع | الالتزام | دائن‬ | ‏‏نعم‬ | الجمعة | يُستخدم عند تمكين العمولة وحسابها للمبيعات وترحيلها أثناء عملية فوترة أمر المبيعات. الحساب المقابل لهذا الحساب هو مصروفات العمولة. |
| الإيراد المؤجل عند التسليم‬ (المبيعات – إيراد إيصال التعبئة‬*) | 401400 | المبيعات المستحقة | الإيراد | دائن‬ | ‏‏نعم‬ | P  | يُستخدم عند تمكين "الإيراد المؤجل عند التسليم‬" ويتم ترحيله عند معالجة إيصال تعبئة أمر مبيعات. الحساب المقابل لهذا الحساب هو الإيراد المؤجل المقابل عند التسليم‬. يتم عكس المبالغ الموجودة في هذا الحساب تلقائيًا عند ترحيل فاتورة أمر مبيعات. |
| الإيراد المؤجل المقابل عند التسليم (المبيعات – مقابل إيراد إيصال التعبئة‬)* | 130400 | الحسابات المدينة – غير مفوترة | الأصل | مدين | ‏‏نعم‬ | P  | يُستخدم عند تمكين "الإيراد المؤجل عند التسليم‬" ويتم ترحيله عند معالجة إيصال تعبئة أمر مبيعات. الحساب المقابل لهذا الحساب هو الإيراد المؤجل عند التسليم‬. يتم عكس المبالغ الموجودة في هذا الحساب تلقائيًا عند ترحيل فاتورة أمر مبيعات. |
| ضريبة مبيعات مؤجلة عند التسليم‬ (المبيعات، ضريبة إيصال التعبئة‬*) | 250500 | ضريبة مبيعات مؤجلة | الالتزام | دائن‬ | ‏‏نعم‬ | P  | يُستخدم عند تمكين "الإيراد المؤجل عند التسليم‬" وتمكين "ترحيل ضريبة المبيعات الفعلية‬".‬ يتم ترحيل مبلغ الضريبة عند معالجة إيصال تعبئة أمر مبيعات. |

\*تمثل القيم التي تظهر بين أقواس في هذا الجدول القيمة المستخدمة في حقل **نوع الترحيل** في صفحة **حركات الإيصال**. يمكنك عرض **نوع الترحيل** في صفحة علامة التبويب **حركات الإيصال** على علامة التبويب **عام**.

## <a name="sales-category-posting"></a>ترحيل فئة المبيعات

كبديل لإعداد ترحيل المخزون لجميع الأصناف أو مجموعة من الأصناف أو صنف واحد، يمكنك إعداد الفئات والتحكم في ترحيل دفتر الأستاذ حسب فئات المبيعات. لمزيد من المعلومات حول إعداد التدرج الهرمي للفئات وتعيين الفئات للمنتجات، انتقل إلى [إنشاء تدرج هرمي لتصنيف منتج‬](/supply-chain/pim/tasks/create-hierarchy-product-classification.md) و[تصنيف منتج باستخدام التدرجات الهرمية للفئات‬](/supply-chain/pim/tasks/classify-product-category-hierarchies.md).

بعد إنشاء التدرج الهرمي للفئات، يجب تعيين التدرج الهرمي لنوع واحد أو أكثر. لاستخدام التدرج الهرمي للفئات في أوامر المبيعات، يجب تعيين الفئة إلى نوع التدرج الهرمي لفئات المبيعات. لمزيد من المعلومات، انتقل إلى [حول التدرجات الهرمية للفئات](/dynamicsax-2012/appuser-itpro/about-category-hierarchies.md).

## <a name="create-revenue-posting-by-sales-category"></a>إنشاء ترحيل الإيرادات حسب فئة المبيعات

لتعيين ترحيلات دفتر الأستاذ لأمر مبيعات بالاستناد إلى فئة مبيعات، اتبع الخطوات التالية:

1. انتقل إلى **إدارة المخزون** > **إعداد** > **ترحيل** > **ترحيل**.
2. حدد علامة التبويب **المبيعات**.
3. حدد الزر التبادلي لنوع الترحيل الذي ترغب في تكوينه (على سبيل المثال، **الإيراد**).
4. حدد **جديد**.
5. في حقل **كود الصنف**، حدد **فئة**.
6. استخدم حقل **علاقة الفئة** لتحديد الفئة لملف تعريف الترحيل.
7. في الحقل **كود الحساب**، حدد خيارًا لكل من **الجدول** أو **المجموعة** أو **الكل**. على سبيل المثال، لتطبيق ملف تعريف الترحيل على كافة العملاء ، حدد **الكل**.
   - إذا قمت بتحديد **جدول** في الخطوة 6، فحدد **رقم المورّد** المحدد لملف تعريف الترحيل في الحقل **علاقة الحساب**.
   - إذا قمت بتحديد **مجموعة** في الخطوة 6، فحدد **مجموعة المورّد** المحدد لملف تعريف الترحيل في الحقل **علاقة الحساب**.
   - إذا قمت بتحديد **الكل** في الخطوة 6، فسيُترك حقل **علاقة الحساب** فارغًا.

8. لربط مجموعة ضريبة محددة بنوع الترحيل المُحدد، حدد **مجموعة ضرائب المبيعات**‬. إذا تركت هذا الحقل خاليًا، يتم تطبيق نوع الترحيل على كافة مجموعات الضرائب الموجودة. يتم تطبيق الترحيل المُحدد لمجموعات الضرائب فقط على الحركات التي تم إجراؤها للمبيعات وعمليات الشراء.

9. في حقل **الحساب الرئيسي**، حدد رقم الحساب الذي سيتم ترحيل نوع الحساب إليه. حدد واحدًا من أرقام الحساب الموجودة في دليل الحسابات لديك.
