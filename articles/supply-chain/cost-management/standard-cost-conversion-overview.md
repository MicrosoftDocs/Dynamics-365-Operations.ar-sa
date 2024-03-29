---
title: نظرة عامة حول تحويل التكاليف القياسية
description: توفر هذه المقالة نظرة عامة على العملية لمساعدتك على إعداد وتشغيل تحويل تكلفة المعيارية. يجب إكمال الخطوات المذكورة بعد أن تستكمل المتطلبات الأساسية لتحويل تكلفة المعيارية.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "78212"
- intro-internal
ms.assetid: d601d9d5-1de3-4868-aff4-534dca01d624
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7b7973acedcfd0c0e74e47b82f2344c4eb63b50
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679460"
---
# <a name="standard-cost-conversion-overview"></a>نظرة عامة حول تحويل التكاليف القياسية

[!include [banner](../includes/banner.md)]

توفر هذه المقالة نظرة عامة على العملية لمساعدتك على إعداد وتشغيل تحويل تكلفة المعيارية. يجب إكمال الخطوات المذكورة بعد أن تستكمل المتطلبات الأساسية لتحويل تكلفة المعيارية. 

استخدم صفحة **عمليات تحويل التكلفة المعيارية‬** لتحويل نموذج المخزون لمجموعة من الأصناف المحددة من مبدأ التكلفة الفعلية إلى التكلفة المعيارية. وتتضمن عملية التحويل إغلاق المخزون كخطوة أساسية، وإجراء عدة خطوات أثناء فترة انتقالية، وهي فترة محددة بتاريخ بدء المرحلة الانتقالية وتاريخ تحويل مخطط، ثم إجراء التحويل وإغلاق المخزون المرتبط.

-   إغلاق المخزون قبل الفترة الانتقالية - يمثل إغلاق المخزون خطوة أساسية، إذ يعمل على تسوية الحركات المفتوحة للأصناف باستخدام أسلوب التقييم القديم. وخلال الفترة الانتقالية، يمكنك إدخال حركات ذات تواريخ قديمة وترحيلها، مثل الفواتير، لكي تتمكن من إغلاق الفترة السابقة. يجب أن يكون تاريخ إغلاق المخزون سابقًا بيوم واحد لتاريخ بدء الفترة الانتقالية، وذلك لضمان الانفصال التام عن الأسلوب القديم لتقييم المخزون.
-   خطوات التحويل أثناء الفترة الانتقالية - استخدم صفحة **عمليات تحويل التكلفة المعيارية‬** لإنشاء سجل تحويل يحتوي أيضًا على معرف محدد من قبل المستخدم لإصدار تكاليف جديد. وستقوم أنت بتعريف الأصناف التي تحتاج إلى تحويل، ثم ستدخل التكاليف المعيارية المعلقة للصنف في إصدار التكاليف الجديد. وستجري عملية فحص للأصناف المحددة للتعرف على المشكلات التي قد تحول دون إتمام عملية التحويل، وستحل هذه المشكلات ثم تجري عملية فحص أخرى. بعد أن تجتاز الأصناف عمليات الفحص بنجاح، ستغيّر حالة سجل التحويل إلى **جاهز‬**. في تاريخ التحويل المخطط، يمكنك إجراء التحويل مع إغلاق المخزون اختياريًا. يتم ترحيل حركات مخزون الصنف وتقييمها أثناء الفترة الانتقالية وفقًا لنموذج المخزون القديم. وبعد ذلك، بعد إتمام عملية التحويل بنجاح، يعاد تقييم حركات المخزون إلى التكلفة المعيارية.
-   إغلاق المخزون قبل التحويل - يمكن تضمين عملية إغلاق المخزون كجزء من عملية التحويل في تاريخ التحويل المخطط، أو يمكن تنفيذها كخطوة منفصلة قبل التحويل.

بعد استكمال عملية التحويل بنجاح، يصبح نموذج المخزون لكل صنف مستندًا إلى التكلفة المعيارية، وسيتم تمكين التكلفة المعيارية للصنف. وسوف يتم تقييم حركات المخزون اللاحقة وفقًا للتكلفة المعيارية للصنف. فضلاً عن ذلك، يقوم النظام بتحويل حركات المخزون الفعلية للصنف الخاصة بعمليات الاستلام والإصدار إلى التكلفة المعيارية بالاستناد إلى تاريخ التحويل. ويحوّل النظام أيضًا المخزون الفعلي المالي للصنف إلى التكلفة المعيارية، ويرحّل فرق القيمة كإعادة تقييم للمخزون. يتم تقييم أية حركات تحدث بعد التحويل وفقًا للتكلفة المعيارية للصنف. ولا يمكن إدخال حركات تاريخها أقدم من تاريخ التحويل، نظرًا لأنه يجب إجراء إغلاق المخزون قبل يوم واحد من تاريخ التحويل. ويمكن تنفيذ التحويل فقط إذا تم تنفيذ عملية إغلاق المخزون قبل يوم واحد.‬ ولا يمكن إلغاء إغلاق المخزون هذا.

## <a name="1-define-a-standard-cost-conversion-record-and-the-associated-costing-version"></a>1. تعريف سجل تحويل التكلفة المعيارية وإصدار التكاليف المقترن
استخدم صفحة **عمليات تحويل التكلفة المعيارية‬** لإنشاء سجل تحويل. يمكنك إنشاء سجل تحويل جديد فقط عند استكمال سجلات التحويلات الحالية. يتم تعريف طول فترة الانتقال المخطط بواسطة تاريخ بدء الانتقال وتاريخ التحويل المخطط. بإمكان الفترة الانتقالية المخططة أن تدوم ليوم واحد فقط. تساعد الفترة الانتقالية المخططة على التأكد من وجود الوقت الكافي لكي تتمكن عملية التحويل من استكمال كافة الخطوات. يجب تنفيذ عملية إغلاق المخزون في تاريخ يسبق تاريخ بدء الفترة الانتقالية بيوم واحد، وذلك من أن أجل المساعدة على ضمان استكمال التسويات قبل بدء عملية التحويل. للتأكد من توافق تاريخ بدء المرحلة الانتقالية وتاريخ إغلاق المخزون بشكل صحيح، يمكنك إما تغيير تاريخ بدء المرحلة الانتقالية إلى يوم واحد يلي إغلاق المخزون الحالي أو تنفيذ عملية إغلاق المخزون. عندما تدخل سجل تحويل، ستقوم أيضًا بإدخال معرف محدد من قبل المستخدم لإصدار تكاليف جديد سيحتوي على التكاليف المعيارية للأصناف المحوّلة. يتم إنشاء إصدار التكاليف تلقائيًا عند حفظ سجل التحويل.

## <a name="2-review-and-change-the-new-costing-version-for-the-conversion-record"></a>2. مراجعة إصدار التكاليف الجديد لسجل التحويل وتغييره
يتم تخصيص إصدار التكاليف الجديد لسجل التحويل، كما يشير إليه نوع تكلفة **التحويل**. يُعد إصدار التكاليف المخصص مماثلاً لإصدار التكاليف المعيارية، وهو يحتوي على سجلات تكلفة الصنف للأصناف المقترنة بسجل التحويل. يتضمن إصدار التكاليف المخصص لسجل التحويل الإعدادات التالية، والتي يجب مراجعتها وتعديلها على مختلف علامات التبويب، كما هو مطلوب:

-   **نوع التكلفة:** يجب أن يتم تعيين هذا الحقل إلى **التكلفة المعيارية**.
-   **الإصدار:** يعكس المعرّف المعلومات التي يتم إدخالها على سجل التحويل لمعرّف إصدار التكلفة.
-   **الاسم:** بشكل افتراضي، يكون حقل الاسم فارغًا. يمكنك إدخال اسم، بشكل اختياري.
-   **حظر:** يجب أن يتم تعيين هذا الحقل إلى **لا**. يمكنك إدخال سجلات التكلفة في إصدار التكاليف حتى تقوم بتغيير حالة سجل التحويل إلى **جاهز**. تشير الحالة **جاهز** إلى أنه تم فحص الأصناف المحددة، وأنه لا ينبغي السماح بالتغييرات في سجلات التكلفة.
-   **حظر التنشيط‬** يجب أن يتم تعيين هذا الحقل إلى **لا**. لا يمكن تنشيط سجل التكلفة المعلق يدويًا داخل إصدار التكاليف المخصص. ويحدث التنشيط عند إجراء التحويل.
-   **من تاريخ:** يعكس "من تاريخ" قيمة تاريخ التحويل المخطط الذي يتم إدخاله في سجل التحويل.
-   **الموقع:** اترك هذا الحقل فارغًا، بحيث يمكن إدخال سجلات التكلفة لأي موقع.
-   **مجموعة حقل السماح بنوع السعر‬:** عيّن هذا الحقل إلى **نعم**، بحيث يمكن إدخال سجلات سعر التكلفة فقط.
-   **مبدأ الاحتياطي‬:** يتم تعيين هذا الحقل إلى **بلا**. غيّر مبدأ الاحتياطي إلى **نشط** عند مطالبتك بمعلومات التكلفة التي تم تنشيطها في إصدارات تكلفة أخرى. على سبيل المثال، قد تكون معلومات التكلفة حول المكونات وفئات التكلفة والتكاليف غير المباشرة مطلوبة لحساب تكاليف الأصناف التي تم تصنيعها.
-   **إصدار تكاليف الاحتياطي:** اترك هذا الحقل فارغًا.

يمكن الحفاظ على معلومات تكلفة الصنف في إصدار التكلفة المخصص فقط من صفحة **عمليات تحويل التكلفة المعيارية‬**. لا يمكنك استخدام صفحة **إعداد إصدار حساب التكلفة‬** أو صفحة **صيانة إصدار حساب التكلفة‬** لحساب تكاليف إصدار التكاليف أثناء عملية التحويل. ولكن يمكنك استخدام هذه الصفحات للمحافظة على إصدار التكاليف المخصص بعد إكمال عملية التحويل.

## <a name="3-identify-the-items-to-convert-to-standard-cost"></a>3. تحديد الأصناف لتحويلها إلى تكلفة معيارية
استخدم صفحة **عمليات تحويل التكلفة المعيارية‬** لتحديد العناصر الفردية التي ينبغي تحويلها إلى تكلفة معيارية. يمكنك إضافة عدة أصناف باستخدام صفحة **إضافة أصناف إلى تحويل التكلفة المعيارية‬**. بشكل عام، ينبغي تضمين كافة الأصناف التي تم تصنيعها في سجل تحويل واحد للمساعدة على ضمان حساب التكاليف بشكل صحيح.

## <a name="4-enter-or-calculate-the-pending-standard-cost-for-each-item-that-is-being-converted"></a>4. إدخال التكلفة المعيارية المعلقة أو حسابها لكل صنف جارٍ تحويله
استخدم صفحة **سعر الصنف** لإدخال التكاليف المعيارية المعلقة في إصدار التكاليف المخصص للأصناف التي تم شراؤها ولنقل الأصناف. تكون سجلات التكلفة محددة بالموقع، كما يجب إدخال التكاليف المعلقة الخاصة بالصنف لكل موقع. استخدم صفحة **سعر الصنف** لحساب التكاليف المعيارية المخصصة للأصناف التي تم تصنيعها. وينبغي حساب التكاليف المعلقة للصنف الذي تم تصنيعه لكل موقع تصنيع، إلا إذا كان الموقع يمثل موقع تحويل. في هذه الحالة، يجب إدخال التكاليف المعلقة يدويًا. قد يكون لبعض الأصناف أبعاد منتج من حيث اللون أو الحجم أو التكوين. في صفحة **عمليات تحويل التكلفة المعيارية**، تُظهر خانة الاختيار **استخدام سعر التكلفة حسب المتغير‬** التكلفة المعيارية لكل مجموعة أبعاد المنتج. عند إلغاء تحديد خانة الاختيار هذه، يجب إدخال تكلفة معلقة للصنف فقط.

## <a name="5-check-and-resolve-any-issues-for-the-items-that-are-being-converted"></a>5. فحص المشكلات للأصناف الجاري تحويلها وحلها
استخدم تقرير **عمليات فحص تحويل التكلفة المعيارية‬** للتعرف على المشكلات الخاصة بالأصناف الجاري تحويلها. إذا لم يكن لدى الصنف أي مشكلات، فستتغيّر حالته في سجل التحويل إلى **تم فحصه**. إذا كان لدى الصنف مشكلات، فيجب حل هذه المشكلات ثم تشغيل التقرير مرة أخرى حتى تتغير حالة الصنف إلى **تم فحصه**. إذا تعذر عليك حل مشكلات الصنف في الوقت الملائم، فيمكنك حذف العنصر من سجل التحويل وتحويله في وقت لاحق اختياريًا.

## <a name="6-change-the-status-of-the-conversion-record-to-ready"></a>6. تغيير حالة سجل التحويل إلى جاهز
عندما تتغيّر حالة سجل التحويل إلى **جاهز**، يجري النظام إجراء فحصًا نهائيًا قبل تشغيل تحويل التكلفة المعيارية. وسوف تتغيّر الحالة إلى **جاهز** فقط عند تلبية الشروط التالية:

-   تكون حالة كل صنف في سجل التحويل **تم فحصه**.
-   تم تنفيذ إجراء إغلاق المخزون في تاريخ يسبق تاريخ بدء المرحلة الانتقالية بيوم واحد. للتأكد من توافق تاريخ بدء المرحلة الانتقالية وتاريخ إغلاق المخزون بشكل صحيح، يمكنك إما تغيير تاريخ بدء المرحلة الانتقالية إلى يوم واحد يلي إغلاق المخزون الحالي أو تنفيذ عملية إغلاق المخزون.

## <a name="7-back-up-the-database-before-conversion"></a>7. إنشاء نسخة احتياطية لقاعدة البيانات قبل التحويل
تسمح لك النسخة الاحتياطية باستعادة قاعدة البيانات إذا تمت مصادفة أخطاء أثناء عملية التحويل.

## <a name="8-perform-the-conversion-when-the-conversion-record-has-a-ready-status"></a>8. إجراء عملية التحويل عندما تكون حالة سجل التحويل جاهز
تتطلب عملية التحويل تنفيذ إجراء إغلاق المخزون في تاريخ يسبق تاريخ التحويل المخطط بيوم واحد. من شأن ذلك أن يساعد على ضمان عدم إدخال الحركات التي تعود إلى تاريخ سابق أثناء الفترة الانتقالية. وإذا لم يكن إجراء إغلاق المخزون قد تم تنفيذه بعد، فسيتم سؤالك عما إذا كنت ترغب في تنفيذه كجزء من عملية التحويل. تقوم عملية التحويل بمعالجة صنف واحد في كل مرة. وهي تبدأ بالأصناف الأدنى في بنية منتج، استنادًا إلى كود الصنف ذي المستوى المنخفض للصنف. عند تحويل أحد الأصناف بنجاح، تتغير حالته في سجل التحويل إلى **‏‫تم التحويل‬**. إذا تمت مقاطعة عملية التحويل، فإن أي أصناف لم يتم تحويلها بنجاح تبقى في حالة **تم فحصه**. ينطوي استكمال عملية التحويل بنجاح على التأثيرات التالية:

-   تتغير حالة سجل التحويل من **جاهز** إلى **مكتمل**، وتتغير حالة كل صنف محدد من **تم فحصه** إلى **تم التحويل**.
-   تتغير مجموعة نماذج الصنف حتى تعكس مجموعة جديدة ذات نموذج مخزون تكلفة معيارية.‬
-   تم تمكين التكاليف المعيارية للأصناف التي تم تحويلها في إصدار التكاليف المخصص.
-   يتغير نوع التكلفة الخاص بإصدار التكاليف من **تحويل** إلى **تكلفة معيارية**، ويعمل إصدار التكاليف الآن تمامًا كأي إصدار تكاليف آخر للتكاليف المعيارية.

## <a name="9-validate-and-reconcile-the-inventory-values-for-the-converted-items"></a>9. التحقق من صحة قيم المخزون للأصناف التي تم تحويلها وتسويتها
يسمح لك تقرير **كشف تحليل نسبة الفرق** بتحليل فرق إعادة التقييم، ويسمح لك تقرير **قيمة المخزون** بعرض قيمة المخزون في تاريخ محدد.

-   قم بتحليل نسب فرق إعادة التقييم. استخدم تقرير **كشف تحليل نسبة الفرق‬** لعرض فروقات إعادة تقييم المخزون للأصناف التي تم تحويلها. يمكنك أيضًا استخدام صفحة **حركات التكلفة القياسية‬** لعرض حركات إعادة تقييم المخزون للأصناف التي تم تحويلها ولديها مخزون.
-   حلل قيمة المخزون قبل تاريخ بدء المرحلة الانتقالية. استخدم التقرير **قيمة المخزون** لعرض قيم المخزون للأصناف التي تم تحويلها. بالنسبة إلى "إلى تاريخ" في التقرير، استخدم تاريخًا يقع قبل يوم واحد من تاريخ بدء المرحلة الانتقالية.
-   حلل قيمة المخزون قبل تاريخ التحويل. استخدم التقرير **قيمة المخزون** لعرض قيم المخزون للأصناف التي تم تحويلها. بالنسبة إلى "إلى تاريخ" في التقرير، استخدم تاريخًا يعكس يومًا واحدًا قبل تاريخ التحويل.
-   حلل قيمة المخزون في تاريخ التحويل. استخدم تقرير **قيمة المخزون** لعرض قيمة المخزون بدءًا من تاريخ التحويل. يجب أن يتطابق "من تاريخ" و"إلى تاريخ" في التقرير مع تاريخ التحويل. ينبغي أن تعكس معايير تحديد التقرير الأصناف التي تم تحويلها.
-   حلل حركات المخزون التي تعود إلى تاريخ سابق. استخدم التقرير **قيمة المخزون** لعرض حركات المخزون التي تعود إلى تاريخ سابق والتي تم إدخالها بعد التحويل. يجب أن يتطابق "من تاريخ" و"إلى تاريخ" في التقرير مع تاريخ بدء المرحلة الانتقالية وتاريخ التحويل (ناقص يوم واحد). ينبغي أن تعكس معايير تحديد التقرير الأصناف التي تم تحويلها. ويعرض التقرير حركات المخزون التي تمت بالتكلفة المعيارية خلال الفترة الانتقالية.


## <a name="additional-resources"></a>الموارد الإضافية

[متطلبات تحويل التكلفة المعيارية](prerequisites-standard-cost-conversion.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]