---
title: إعداد قيم معلمات التكلفة
description: عند إعداد الوحدة النمطية ‬‏‫التكلفة شاملة التفريغ، يمكنك تحديد عدة مجموعات من القيم المشتركة التي ستتوفر عند تحديد أنواع معينة من قيم معلمات التكلفة في أجزاء أخرى من التطبيق. يشرح هذا المقال كيفية إعداد هذه المجموعات من القيم.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTypeTable, ITMCostTypeGroup, ITMCostTransferGroup, ITMCostTemplateTable, ITMVolumetricDivisorTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ca3633cd8a3fb053bda597b968003685aa2326ef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852320"
---
# <a name="costing-parameter-values-setup"></a>إعداد قيم معلمات التكلفة

[!include [banner](../../includes/banner.md)]

عند إعداد الوحدة النمطية **التكلفة شاملة التفريغ** ، يمكنك تحديد عدة مجموعات من القيم المشتركة والإعدادات ذات الصلة لكل قيمة. ستتوفر هذه القيم بعد ذلك عند تحديد أنواع معينة من قيم معلمات التكلفة في أجزاء أخرى من التطبيق. يشرح هذا المقال كيفية إعداد هذه المجموعات من القيم.

## <a name="set-up-cost-type-codes"></a>إعداد أكواد نوع التكلفة

تحدد أكواد نوع التكلفة نوع التكلفة التي يتم تكبدها عند وصول البضائع إلى المستودع، أو التكاليف شاملة التفريغ للرحلة. على الرغم من أنها عادة ما تزيد من قيمة البضائع، إلا أنه يمكن استخدامها أيضًا لتجميع المبالغ في دفتر الأستاذ. يتم استخدام تسويات دفتر الأستاذ عند استحقاق التكلفة علي مدار الوقت أو أثناء سلسلة من الرحلات والحساب المقابل لحركة واحدة.

> [!NOTE]
> إذا تمت مشاركة جدول نوع التكلفة عبر الكيانات القانونية، فينبغي أيضًا مشاركة مخطط الحسابات عبر الكيانات القانونية. وإلا، فلن تعمل حركات الترحيل بشكل صحيح.

لإعداد أكواد نوع التكلفة، انتقل إلى **التكلفة شاملة التفريغ \> إعداد التكلفة \> أكواد نوع التكلفة**. ويمكنك استخدام الأزرار الموجودة في جزء الإجراءات لإنشاء أكواد نوع تكلفة جديدة أو تحرير أكواد موجودة أو حذف نوع تكلفة محدد.

يصف الجدول التالي الحقول المتوفرة لكل كود نوع التكلفة.

| الحقل | الوصف |
|---|---|
| كود نوع التكلفة | أدخل اسمًا لكود نوع التكلفة. |
| الوصف | يتيح إدخال وصف لكود نوع التكلفة. |
| استخدام سعر الشحن | يتم تعيين هذا الخيار علي *نعم* إذا تم استخدام سعر صرف الرحلة (يُشار إليه أحيانًا بسعر الإدارة) لحساب قيمة هذه التكاليف. وفي هذه الحالة، سيتم استخدام سعر الشحن بدلاً من سعر الصرف الافتراضي القياسي أو الفعال لفواتير صرف العملات الأجنبية. |
| فئة إعداد التقارير | ينشئ هذا الحقل فئة تقرير لنوع التكلفة. يمكن طباعة التقارير إما عن طريق فئات التقارير أو حسب نوع التكلفة. |
| نوع المدين | تحديد ما إذا كان ينبغي خصم نوع التكلفة للصنف أو حساب دفتر الأستاذ أو المورد. |
| ترحيل المدين | إذا تم تعيين الحقل **نوع المدين** على *حساب دفتر الأستاذ*، فحدد وصف الترحيل. |
| حساب مدين | إذا تم تعيين الحقل **نوع المدين** على *حساب دفتر الأستاذ*، فحدد حساب دفتر الأستاذ المراد استخدامه. |
| نوع الائتمان | تحديد ما إذا كان ينبغي إضافة نوع التكلفة للصنف أو حساب دفتر الأستاذ أو المورد. |
| ترحيل الدائن | إذا تم تعيين الحقل **‬‏‫نوع الدائن** على *حساب دفتر الأستاذ*، فحدد وصف الترحيل. |
| حساب دائن | إذا تم تعيين الحقل **‬‏‫نوع الدائن** على *حساب دفتر الأستاذ*، فحدد حساب دفتر الأستاذ المراد استخدامه. |
| حساب مقاصة. | تحديد حساب المقاصة لنوع التكلفة. نوصي بتحديد حساب مقاصة منفصل لكل نوع تكلفة للمساعدة في التسوية. |
| نوع ترحيل التكلفة القياسية | إذا كنت تستخدم التكاليف القياسية، فحدد وصف الترحيل. |
| حساب فرق التكلفة القياسية. | <p>إذا كنت تستخدم التكاليف القياسية، سيتم استخدام الحساب المحدد هنا لترحيل أي نسبة فرق. يستخدم هذا الحساب تفاصيل تكلفة البضائع شاملة التفريغ في صفحة **أسعار الأصناف** . يتم إنشاء التصنيف التفصيلي هذا باستخدام الروتين الدوري لتحديث الأسعار.</p><p>على سبيل المثال، تكون التكلفة القياسية لصنف ما هي 15.00 دولارًا أمريكيًا، وتكون التكلفة عند التسليم على ظهر السفينة هي 13.00 دولارًا أمريكيًا، وتكون أجرة الشحن 2.00 دولار أمريكي. عند استلام فاتورة المخزون، يتم استلام الصنف بسعر 15.00 دولارًا أمريكيًا، ولكن هناك فرق سعر قياسي قدره 2.00 دولار أمريكي للصنف، لأن قيمة التسليم الفعلي على ظهر السفينة تساوي 13.00 دولارًا أمريكيًا. يتم ترحيل هذا الفرق إلى حساب فرق السعر القياسي الذي تم إعداده في ملف تعريف ترحيل الصنف. ونظرًا لأن أجرة الشحن المقدرة تبلغ 2.00 دولارًا أمريكيًا، فلا يوجد فرق عند ترحيل فاتورة المخزون. ومع ذلك، عند استلام فاتورة الشحن، يكون الشحن 2.50 دولارًا لكل وحدة. وبالتالي، يتم ترحيل نسبة فرق 0.50 دولار إلى التكلفة المحددة. |
| حساب فرق المتوسط المتحرك‬ | <p>إذا كنت تستخدم متوسط تكلفة النقل، سيتم استخدام الحساب المحدد هنا لترحيل أي نسبة فرق.</p><p>علي سبيل المثال، تكون أجرة الشحن المقدرة 2.00 دولار. ومع ذلك، عند استلام فاتورة الشحن، يكون الشحن 2.50 دولارًا لكل وحدة. وبالتالي، يتعين ترحيل فرق 0.50 دولارًا أمريكياً.</p><p>عند تعيين الخيار **تسويات الترحيل كفرق** على *نعم* في صفحة **معلمِات التكلفة شاملة التفريغ** ، سيتم ترحيل جميع الفروق بين تكاليف الشحن المقدرة والفعلية إلى حساب فرق متوسط النقل المحدد هنا. عند تعيين الخيار **تسويات الترحيل كفرق** على *لا*، سيتم استخدام الوظيفة القياسية، وسيتم تطبيق الفرق إما على المخزون أو على حساب فرق متوسط ​​النقل المحدد هنا، اعتمادًا على المخزون المتوفر.</p> |
| حساب تجميع التكاليف | تحديد الحساب الذي يتم استخدامه لاستحقاق تقديرات التكلفة عند ترحيل فاتورة الشراء. يتم استخدام هذا الحقل فقط عند تعيين الخيار **استخدام حساب تراكم التكاليف من نوع التكلفة** على *نعم* في علامة التبويب السريعة **التكلفة** في علامة التبويب **عام** لصفحة **معلمات التكلفة شاملة التفريغ** . |
| حساب التكلفة | تحديد الحساب المستخدم لالتقاط تكاليف النقل الداخلي التي قام أحد الموردين بفوترتها. ويتم ترحيل المبلغ كمدين. ويكون الحساب المقابل هو حساب فرق المخزون. يتم استخدام هذا الترحيل فقط عندما يتم تعيين خيار **رحيل إلى حساب مصاريف في دفتر الأستاذ** على *نعم* في صفحة **معلمات الحسابات الدائنة**. |
| حساب الفرق | الحساب الذي سيتم استخدامه للحساب المقابل للتكاليف المستحقة عند ترحيل فاتورة الشراء. يتم استخدام هذا الحقل فقط عند تعيين الخيار **استخدام حساب تراكم التكاليف من نوع التكلفة** على *نعم* في علامة التبويب السريعة **التكلفة** في علامة التبويب **عام** لصفحة **معلمات التكلفة شاملة التفريغ** . |

## <a name="vendor-cost-type-groups"></a>مجموعات أنواع تكاليف المورّد

تساعد مجموعات مجموعة نوع تكلفة المورد في تحديد كيفية العثور على رسوم *التكلفة التلقائية* وتطبيقها على الرحلة. ويتم ربط الموردين الذين لديهم تكاليف استيراد متشابهة معًا. على سبيل المثال، يدفع جميع الموردين من الأسواق الناشئة نفس النسبة المئوية للرسوم لنفس النوع من المنتجات التي يتم شراؤها من سوق قائمة.

يمكنك إجراء التعديلات على مجموعات نوع تكلفة المورد من خلال الانتقال إلى **التكلفة شاملة التفريغ \> إعداد التكلفة \> مجموعات نوع تكلفة المورد**. توفر صفحة **مجموعات نوع تكلفه المورد** شبكة تسرد كافة مجموعات نوع تكلفة المورد الموجودة. يمكنك استخدام الأزرار الموجودة في جزء الإجراءات لإضافة صفوف في الشبكة وإزالها وتحريرها.

يصف الجدول التالي الحقول المتاحة في كل صف في الشبكة.

| الحقل | الوصف |
|---|---|
| مجموعات أنواع تكاليف المورّد | أدخل اسمًا فريدًا لمجموعة نوع تكلفة المورد (مثل *الأسواق الناشئة*). |
| الوصف | أدخل وصفًا لمجموعة نوع تكلفة المورد. ويمكن أن يوفر هذا الوصف تفاصيل حول مستوى أو نوع الرسوم المرتبطة بمجموعة الموردين. |

## <a name="item-cost-type-groups"></a>مجموعات أنواع تكاليف الصنف

تساعد مجموعات نوع تكلفة الصنف في تحديد كيفية العثور على رسوم *التكلفة التلقائية* وتطبيقها على الرحلة. يتم ربط الأصناف المتشابهة معًا. على سبيل المثال، قد تنتمي جميع العناصر التي لها معدل رسوم بنسبة 5 بالمائة إلى مجموعة نوع تكلفة معينة.

يمكنك إجراء التعديلات على مجموعات نوع تكلفة الصنف من خلال الانتقال إلى **التكلفة شاملة التفريغ \> إعداد التكلفة \> مجموعات نوع تكلفة الصنف**. توفر صفحة **مجموعات نوع تكلفه الصنف** شبكة تسرد كافة مجموعات نوع تكلفة المورد الموجودة. يمكنك استخدام الأزرار الموجودة في جزء الإجراءات لإضافة صفوف في الشبكة وإزالها وتحريرها.

يصف الجدول التالي الحقول المتاحة في كل صف في الشبكة.

| الحقل | الوصف |
|---|---|
| مجموعات أنواع تكاليف الصنف | أدخل اسمًا فريدًا لمجموعة نوع تكلفة المصنف (مثل *رسوم 5%*). |
| الوصف | أدخل وصفًا لمجموعة نوع تكلفة الصنف. ويمكن أن يوفر هذا الوصف تفاصيل حول مستوى أو نوع الرسوم المرتبطة بمجموعة الصنف. |

> [!NOTE]
> يرتبط نوع تكلفة الصنف بالصنف من خلال الحقل **مجموعة نوع التكلفة** في علامة التبويب السريعة **شراء** لصفحة **‏‫المنتج الذي تم إصداره‬** الخاصة بالصنف.

## <a name="transfer-order-cost-type-groups"></a>أمر تحويل مجموعات نوع التكلفة

يساعد أمر تحويل مجموعات نوع التكلفة في تحديد كيفية العثور على رسوم *التكلفة التلقائية* . يتم ربط الأصناف المتشابهة معًا. على سبيل المثال، قد تنتمي جميع العناصر التي لها معدل رسوم بنسبة 7 بالمائة إلى مجموعة نوع تكلفة معينة.

يمكنك إجراء التعديلات على أمر تحويل مجموعات نوع التكلفة من خلال الانتقال إلى **التكلفة شاملة التفريغ \> إعداد التكلفة \> أمر تحويل مجموعات نوع التكلفة**. توفر صفحة **أمر تحويل مجموعات نوع التكلفة** شبكة تسرد كافة أمر تحويل مجموعات نوع التكلفة الموجودة. يمكنك استخدام الأزرار الموجودة في جزء الإجراءات لإضافة صفوف في الشبكة وإزالها وتحريرها.

يصف الجدول التالي الإعدادات المتاحة في كل صف في الشبكة.

| الحقل | الوصف |
|---|---|
| أمر تحويل مجموعات نوع التكلفة | أدخل اسمًا فريدًا لأمر تحويل مجموعات نوع التكلفة (مثل *رسوم 7%*). |
| الوصف | أدخل وصفًا لأمر تحويل مجموعات نوع التكلفة. ويمكن أن يوفر هذا الوصف تفاصيل حول مستوى أو نوع الرسوم المرتبطة بأمر تحويل مجموعات نوع التكلفة. |

> [!NOTE]
> يرتبط أمر تحويل مجموعات نوع التكلفة بالصنف من خلال الحقل **أمر تحويل مجموعات التكلفة** في علامة التبويب السريعة **شراء** لصفحة **‏‫المنتج الذي تم إصداره‬** الخاصة بالصنف.

## <a name="cost-templates"></a>قوالب التكلفة

يمكنك استخدام قوالب التكلفة لتعيين القيم الافتراضية للإعدادات التي قد لا يعرفها المستخدمون الذين يحصلون علي تقدير التكلفة. يمكن ان تساعد قوالب التكلفة علي تقليل التعقيد في عمليه التقدير وذلك بتقليل التحديدات التي ينبغي أن يقوم بها المستخدمون للحصول علي تقدير دقيق.

للعمل باستخدام قوالب التكلفة، انتقل إلى **التكلفة شاملة التفريغ \> إعداد التكاليف \> قوالب التكلفة**. في صفحة **قوالب التكلفة** ، يعرض جزء القائمة الموجود علي اليسار كافة قوالب التكلفة الحالية. يمكنك استخدام الأزرار الموجودة في جزء الإجراءات لإضافة القوالب وإزالتها وتحريرها.

يصف الجدول التالي الإعدادات المتوفرة لكل قالب.

| الحقل | الوصف |
|---|---|
| قالب التكلفة | أدخل اسما مميزاً لقالب التكلفة. يصف الاسم عادةً العامل أو مضاعف التكلفة للقالب. |
| الوصف | إدخال وصف لقالب التكلفة. |
| شركة الشحن | .حدد حساب المورد الخاص بشركه الشحن لربطها بقالب التكلفة. |
| وضع التسليم | حدد وضع التسليم الذي يجب أن يستخدمه قالب التكلفة عند حساب التكلفة المقدرة للصنف. سيساعد هذا الحقل في تحديد التكاليف التلقائية المرتبطة بالبضائع في تقدير التكلفة. |
| نوع حاوية الشحن | حدد نوع حاوية الشحن لربطها بقالب التكلفة. سيساعد هذا الحقل في تحديد التكاليف التلقائية المرتبطة بالبضائع في تقدير التكلفة. |
| الوسيط الجمركي | حدد وسيط الجمارك (المورد) لإقرانه بقالب التكلفة. سيساعد هذا الحقل في تحديد التكاليف التلقائية المرتبطة بتقدير التكلفة. |
| العامل‬ | أدخل عاملاً لتطبيقه على تقدير التكلفة النهائية للبضائع. علي سبيل المثال، لإضافة 10 بالمائة إلى تقدير التكلفة المحسوبة، أدخل *1.10*. |

## <a name="volumetric-divisors"></a>قواسم حجمية

تستخدم المقسومات الحجمية لحساب الوزن الحجمي. تقوم كل شركة شحن بصياغة المقسومات الحجمية الخاصة بها. بالإضافة إلى ذلك، عادةً ما تختلف مقسومات الشركة اعتمادًا على وضع التسليم. على سبيل المثال، غالبًا ما يكون للجو والبحر قواسم مختلفة جدًا. ويمكن للشركة أيضًا أن تجعل قواعدها أكثر تعقيدًا، اعتمادًا على المكان الذي تشحن منه. يستخدم النظام الصيغة التالية للعثور على الوزن الحجمي: VolumetricWeight = Volume ÷ VolumetricDivisor.

على سبيل المثال، الحزمة التي يتم إرسالها عن طريق الجو ويكون حجمها 3 متر مكعب (م3). تتقاضى الشركة رسومًا بالوزن الحجمي وتطبق مقسومًا حجميًا على 6. يتم تقسيم هذا القاسم على الحجم لتحديد الوزن الحجمي. وبالتالي، فإن الوزن الحجمي لهذا المثال هو 3 ÷ 6 = 0.5 كيلوجرام (كجم).

لإعداد المقسومات الحجمية، انتقل إلي **التكلفة شاملة التفريغ \> إعداد التكلفة \> المقسومات الحجمية**. توفر صفحة **المقسومات الحجمية** شبكة تسرد جميع لمقسومات الحجمية الموجودة. يمكنك استخدام الأزرار الموجودة في جزء الإجراءات لإضافة صفوف في الشبكة وإزالها وتحريرها.

يصف الجدول التالي الحقول المتاحة في كل صف في الشبكة.

| الحقل | الوصف |
|---|---|
| شركة الشحن | حدد حساب المورد لشركة الشحن المرتبط بالمقسوم الحجمي. |
| كود نوع التكلفة | حدد كود نوع التكلفة المرتبط بالمقسوم الحجمي. استخدم هذا الحقل لوضع أنواع التكلفة في مجموعات التقارير. يمكن طباعة التقارير إما عن طريق فئات التقارير أو حسب نوع التكلفة. |
| مرفأ المغادرة | حدد المنفذ "من" الذي ينطبق عليه المقسوم الحجمي. |
| قاسم حجمي | أدخل قيمة المقسوم الحجمي التي تنطبق على الصف. سيتم تقسيم حجم كل حزمة حسب القيمة التي تقوم بإدخالها هنا لتحديد الوزن الحجمي لتلك الحزمة. |

> [!NOTE]
> سيقوم النظام باستخدام القيمة القصوى بين **الوزن الفعلي** و **الوزن الحجمي**.
