---
title: محددات الإنتاج في تنفيذ التصنيع
description: يوفر هذا المقال معلومات حول إعداد محددات الإنتاج في تنفيذ التصنيع.
author: johanhoffmann
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6d440a0d0d95fe93ed633fa588e1c3a193757d9d
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070368"
---
# <a name="production-parameters-in-manufacturing-execution"></a>محددات الإنتاج في تنفيذ التصنيع

[!include [banner](../includes/banner.md)]

يوفر هذا المقال معلومات حول إعداد محددات الإنتاج في تنفيذ التصنيع.

إن وحدة **تنفيذ التصنيع** مخصصة بشكل أساسي لشركات التصنيع. ويمكن استخدام هذه الوحدة لتسجيل استهلاك الوقت في مهام أو مشاريع الإنتاج. قبل أن تبدأ استخدام "تنفيذ التصنيع" لتسجيلات الوظائف، يجب إعداد مختلف محددات الإنتاج التي تحدد كيف ومتى يتم ترحيل عمليات التسجيل أثناء عملية الإنتاج. تؤثر إعدادات محددات الإنتاج على إدارة المخزون وإدارة الإنتاج وحساب التكلفة.

‏‫يجب عليك التمعن في كافة الإعدادات في صفحة **‬‏‫محددات الإنتاج** قبل بدء العاملين في إجراء تسجيلات في وظائف الإنتاج. انقر فوق **التحكم بالإنتاج** &gt; **الإعداد** &gt; **تنفيذ التصنيع** &gt; **الإعدادات الافتراضية لأمر الإنتاج‬**. إذا كانت شركتك تستخدم وظيفة المواقع المتعددة، فقد تحتاج إلى إعداد محددات الإنتاج المختلفة لكل موقع.‬ يتم إعداد محددات التكامل مع وحدة **الإنتاج** على علامات التبويب التالية في صفحة **محددات الإنتاج**:

- **عام** - إعدادات محددات افتراضية عامة لوظائف الإنتاج في تنفيذ التصنيع.
- **بدء** – المحددات المستخدمة عند بدء عمليات الإنتاج.
- **المحددات** - المحددات التي يتم تطبيقها على عمليات الإنتاج والملاحظات حول العمليات أثناء عملية الإنتاج.
- **الإبلاغ كمنته‬** – المحددات المستخدمة عند الإبلاغ عن أصناف كمنتهية في آخر عملية في أمر الإنتاج.
- **التحقق من صحة الكمية** - المحددات المستخدمة للتحقق من صحة البدء والتعليق على الكميات في أوامر الإنتاج.

## <a name="types-of-production-jobs"></a>أنواع وظائف الإنتاج
في علامة التبويب **عمليات**، حدد أنواع وظائف الإنتاج التي تتطلب التسجيل في صفحة **تسجيل الوظائف**.

وبشكل عام، يُجري العاملون التسجيلات في وظائف الإعداد وظائف العملية. ومع ذلك، إذا تم استخدام جدولة الوظائف، فيمكنك تحديد أنواع الوظائف الأخرى، التي يجب على العاملين أيضًا إجراء التسجيلات فيها عند معالجة أوامر الإنتاج. على سبيل المثال، يمكنك أن تطلب التسجيلات في وظائف النقل.

> [!IMPORTANT]
> تأكد أن تحديد كافة أنواع الوظائف ذات الصلة. وإلا، قد لا تتوف الوظائف للتسجيل في صفحة **تسجيل الوظائف**. يجب أن تكون اختياراتك مطابقة للاختيارات في العمود **إدارة الوظائف‬** على علامة تبويب **الإعداد** في صفحة **مجموعات المسارات** (**التحكم بالإنتاج** &gt; **الإعداد** &gt; **المسارات** &gt; **مجموعات المسارات**).

إذا تم تحديد **إدارة الوظائف** في مجموعة المسارات، فسوف يتم الإبلاغ عن نوع الوظيفة هذه كمنتهٍ في أمر الإنتاج عند الإبلاغ عن الوظيفة كمنتهية في تنفيذ التصنيع. وعند الإبلاغ عن جميع أنواع الوظائف التي تم تحديد **إدارة الوظائف** لها كمنتهية في العملية، فستقوم عملية تنفيذ عملية التصنيع بالإبلاغ عن هذه العملية كمنتهية.

> [!NOTE]
> يمكن الإبلاغ عن بعض أنواع الوظائف يدويًا من خلال دفاتر يومية الإنتاج. وفي هذه الحالة، حدد **إدارة الوظائف** لنوع الوظيفة، ولكن لا تحدد نوع الوظيفة للتسجيل في علامة التبويب **عمليات** في صفحة **محددات الإنتاج** في تنفيذ التصنيع.

## <a name="bom-consumption-and-picking-list-journals"></a>دفاتر يومية قوائم الانتقاء واستهلاك قائمة مكونات الصنف
يُعتبر الإعداد المتسق لاستهلاك قائمة مكونات الصنف (BOM) مهمُا، لأنه يساعد في ضمان كفاءة إدارة المخزون. على سبيل المثال، إذا لم يتم إعداد محددات استهلاك قائمة مكونات الصنف بشكل صحيح في تنفيذ عملية التصنيع، قد يتم خصم المواد من المخزون مرتين أو قد لا يتم خصمها إطلاقًا.

في صفحة **محددات الإنتاج**، يتم إعداد استهلاك قائمة مكونات الصنف التلقائي على ثلاث مراحل:

- في بداية عملية الإنتاج. قم بإعداد هذه المرحلة في علامة التبويب **بدء**.
- أثناء عملية الإنتاج عند اكتمال عميلة ما. قم بإعداد هذه المرحلة في علامة التبويب **العمليات**.
- عند الإبلاغ عن أمر إنتاج كمنتهٍ. قم بإعداد هذه المرحلة في علامة التبويب **الإبلاغ كمنته‬**.

لكل مرحلة، يسمح لك حقل **استهلاك قائمة مكونات الصنف التلقائي‬"** لك بتحديد إحدى الطرق الثلاث لانتقاء الأصناف لأمر إنتاج:

- **قاعدة التفريغ** – يستخدم هذا الخيار مع خيار محدد لقائمة مكونات الصنف في وحدة **الإنتاج**. انقر فوق **التحكم بالإنتاج** &gt; **أوامر الإنتاج** &gt; **كافة أوامر الإنتاج**. في صفحة **جميع أوامر الإنتاج**، حدد أمر إنتاج في القائمة، ومن ثم في جزء "الإجراءات، انقر فوق **قائمة مكونات الصنف**. في صفحة **قائمة مكونات الصنف**، على علامة تبويب **الإعداد**، في حقل **قاعدة التفريغ**، حدد أحد الخيارات التالية:

  - **البدء**
  - **إنهاء**
  - **يدوي**
  - فارغ (لا يتم تحديد أي خيار.)
  - **متوفر في الموقع**

    في تصنيع التنفيذ، إذا تم تحديد **قاعدة التفريغ** في حقل **استهلاك قائمة مكونات الصنف التلقائي** على علامة تبويب **البدء**، يتم خصم كافة المواد التي تم تعيينها إلى **البدء** في قائمة مكونات الصنف من المخزون عند بدء العملية. يُستخدم الخيار **متوفر في الموقع** يُستخدم الخيار للمنتجات التي تم تمكينها لعمليات إدارة المستودعات (WMS). إذا حددت قاعدة التفريغ هذه، فسيتم تفريغ المواد عند اكتمال عمل المستودع لانتقاء المواد الخام. يتم أيضًا تفريغ المواد عندما يتم إصدار بند قائمة مكونات الصنف الذي يستخدم قاعدة التفريغ هذه إلى المستودع، وتكون المواد متوفرة في موقع إدخال الإنتاج.

    > [!NOTE]
    > إذا تم تعيين الحقل **قاعدة التفريغ‬** على علامة تبويب **البدء** في تنفيذ التصنيع‬، فيجب تحديد القاعدة نفسها إما على علامة التبويب **Operations** أو علامة التبويب **الإبلاغ كمنته‬**. يساعد هذا المطلب في ضمان خصم المواد من المخزون على قوائم مكونات الأصناف التي تستخدم **إنهاء** كقاعدة تفريغ في أمر الإنتاج.‬ إذا لم تكن قاعدة التفريغ نفسها محددة على علامة تبويب **العمليات** أو علامة التبويب **الإبلاغ كمنته‬**، فقد يتم خصم المواد من المخزون مرتين.

- **دائمًا‬** -إذا قمت بتحديد هذا الخيار لمرحلة ما، فسيتم دائمًا‬ خصم المواد من المخزون في هذه المرحلة. على سبيل المثال، يتم خصم المواد للإنتاج عند بدء أمر الإنتاج. يتطلب هذا الإعداد تحديد **أبدًا‬** على علامتي تبويب **العمليات** و **الإبلاغ كمنته‬**. يساعد هذا المطلب في منع خصم الأصناف من المخزون مرتين.
- **أبدًا‬** -إذا قمت بتحديد هذا الخيار لمرحلة ما، فلن يحدث أي استهلاك لقائمة مكونات الصنف في هذه المرحلة. على سبيل المثال، إذا قمت بتحديد **أبدًا** في كافة علامات التبويب الثلاثة (**البدء** و **العمليات** و **الإبلاغ كمنته‬**)، فيجب‬ خصم المواد يدويًا من المخزون.

> [!IMPORTANT]
> تحقق بتأنٍ من إعداد محددات الإنتاج، وتأكد من أن المحددات التي تم تحديدها ضمن علامات التبويب المتعددة في صفحة **محددات الإنتاج** لا تتعارض مع بعضها البعض.

توضح الأمثلة التالية إعدادات المحددات التي تدعم مبادئ استهلاك قائمة مكونات الصنف المختلفة. يتم إعداد المحددات في صفحة **محددات الإنتاج** في تنفيذ التصنيع.

### <a name="example-1-backflushing-on-operations"></a>مثال 1: مسح العمليات

استخدم الإعدادات التالية في حالة وجوب إنشاء دفاتر يومية قائمة الانتقاء واستهلاك أصناف قائمة مكونات الصنف عند الإبلاغ عن الأصناف كمنتهية في إحدى العمليات.

| علامة تبويب                | الحقل                          | إعداد                             |
|--------------------|--------------------------------|-------------------------------------|
| البدء              | تحديث البدء عبر الإنترنت           | **الحالة** أو **الحالة + الكمية** |
| البدء              | استهلاك قائمة مكونات الصنف التلقائي      | **أبدًا**                           |
| Operations         | استهلاك قائمة مكونات الصنف التلقائي      | **دائمًا**                          |
| الإبلاغ كمنته | استهلاك قائمة مكونات الصنف التلقائي      | **أبدًا**                           |
| الإبلاغ كمنته | تحديث تقرير الانتهاء عبر الإنترنت | **الحالة + الكمية**               |

### <a name="example-2-backflushing-on-production"></a>مثال 2: مسح الإنتاج

استخدم الإعدادات التالية في حالة وجوب إنشاء دفاتر يومية قائمة الانتقاء واستهلاك أصناف قائمة مكونات الصنف عند الإبلاغ عن الأصناف كمنتهية في أمر الإنتاج.

| علامة تبويب                | الحقل                          | إعداد                             |
|--------------------|--------------------------------|-------------------------------------|
| البدء              | تحديث البدء عبر الإنترنت           | **الحالة** أو **الحالة + الكمية** |
| البدء              | استهلاك قائمة مكونات الصنف التلقائي      | **أبدًا**                           |
| Operations         | استهلاك قائمة مكونات الصنف التلقائي      | **أبدًا**                           |
| الإبلاغ كمنته | استهلاك قائمة مكونات الصنف التلقائي      | **دائمًا**                          |
| الإبلاغ كمنته | تحديث تقرير الانتهاء عبر الإنترنت | **الحالة + الكمية**               |

### <a name="example-3-flushing-principle"></a>المثال 3: قاعدة التفريغ

استخدم الإعدادات التالية في حالة وجوب إنشاء دفاتر يومية قائمة الانتقاء واستهلاك أصناف قائمة مكونات الصنف وفقًا لإعداد قاعدة التفريغ المحدد لأصناف قائمة مكونات الصنف.

| علامة تبويب                | الحقل                          | إعداد                |
|--------------------|--------------------------------|------------------------|
| البدء              | تحديث البدء عبر الإنترنت           | **الحالة + الكمية**  |
| البدء              | استهلاك قائمة مكونات الصنف التلقائي      | **قاعدة التفريغ** |
| Operations         | استهلاك قائمة مكونات الصنف التلقائي      | **قاعدة التفريغ** |
| الإبلاغ كمنته | استهلاك قائمة مكونات الصنف التلقائي      | **أبدًا**              |
| الإبلاغ كمنته | تحديث تقرير الانتهاء عبر الإنترنت | **الحالة + الكمية**  |

### <a name="example-4-deduction-of-materials-during-startup-of-a-production-order"></a>مثال 4: خص المواد أثناء بدء أمر الإنتاج

استخدم الإعدادات التالية في حالة وجوب إنشاء دفاتر يومية قائمة الانتقاء واستهلاك أصناف قائمة مكونات الصنف عند بدء عملية إنتاج.

| علامة تبويب                | الحقل                          | إعداد                             |
|--------------------|--------------------------------|-------------------------------------|
| البدء              | تحديث البدء عبر الإنترنت           | **الحالة + الكمية**               |
| البدء              | استهلاك قائمة مكونات الصنف التلقائي      | **دائمًا**                          |
| Operations         | استهلاك قائمة مكونات الصنف التلقائي      | **أبدًا**                           |
| الإبلاغ كمنته | استهلاك قائمة مكونات الصنف التلقائي      | **أبدًا**                           |
| الإبلاغ كمنته | تحديث تقرير الانتهاء عبر الإنترنت | **الحالة** أو **الحالة + الكمية** |

استنادًا إلى التحديدات الموضحة مسبقًا في هذا القسم، يتم ترحيل دفاتر يومية قائمة الانتقاء في مراحل متنوعة لعملية أمر الإنتاج:

- عند بدء عملية
- عند الإبلاغ عن ملاحظات الكمية في عملية
- عند الإبلاغ عن الأصناف كمنتهية في أمر الإنتاج

### <a name="example-5-manual-bom-consumption"></a>مثال 5: استهلاك قائمة مكونات الصنف اليدوي

يمكنك استخدام الإعدادات التالية إذا كان يجب أن يتم دائمًا خصم المواد يدويًا من المخزون. في هذه الحالة، لا يتم ترحيل دفاتر يومية قائمة الانتقاء.


|        علامة تبويب         |             الحقل              |         إعداد         |
|--------------------|--------------------------------|-------------------------|
|       البدء        |      تحديث البدء عبر الإنترنت      | <strong>الحالة</strong> |
|       البدء        |   استهلاك قائمة مكونات الصنف التلقائي    | <strong>أبدًا</strong>  |
|     Operations     |   استهلاك قائمة مكونات الصنف التلقائي    | <strong>أبدًا</strong>  |
| الإبلاغ كمنته |   استهلاك قائمة مكونات الصنف التلقائي    | <strong>أبدًا</strong>  |
| الإبلاغ كمنته | تحديث تقرير الانتهاء عبر الإنترنت | <strong>الحالة</strong> |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]