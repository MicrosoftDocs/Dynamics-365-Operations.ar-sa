---
title: أنواع الأصل
description: يشرح هذا المقال كيفية إنشاء أنواع الأصول في إدارة الأصول. كما يصف العناصر المرتبطة بأنواع الأصول.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectJobType, EntAssetObjectType, EntAssetObjectTypeDefaultSparePart, EntAssetObjectTypeDefaultSparePartApprove, EntAssetObjectTypeDefaultCreateCombinations, EntAssetObjectTypeDefault, EntAssetObjectTypeDefaultCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d3a51fdb55e9158e88e89549e3d0049e699c233e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887620"
---
# <a name="asset-types"></a>أنواع الأصل

[!include [banner](../../includes/banner.md)]



يشرح هذا المقال كيفية إنشاء أنواع الأصول. كما يصف العناصر المرتبطة بأنواع الأصول. تُستخدم أنواع الأصول كفئات عامة للأصول. ومن الأمثلة على ذلك آلات CNC، ومعدات القياس، ومحركات الشاحنات. يتم استخدام أنواع مهام الصيانة (مهام الصيانة)، وحالات دورة حياة الأصول، والعدادات، وسمات الأصول، وقوالب تقييم الحالة، ونماذج الأصول التي يمكن تحديدها لأصل معين. عندما تنشئ أصلاً، يتعين عليك تحديد نوع الأصل.‬

لكل نوع من أنواع الأصول، يمكن إنشاء أشكال مختلفة من إعداد نوع الأصل. على سبيل المثال، إذا كان لديك نوع أصل يسمى **شاحنات**، يمكنك إنشاء أشكال مختلفة من نوع الأصل هذا لمختلف الشركات المصنعة للأصول ونماذج الأصول. لكل إعداد نوع أصل، يمكنك إضافة قطع الغيار وخطط الصيانة المطلوبة.

أولاً، يمكنك إعداد أنواع الأصول المطلوبة. بعد ذلك، يمكنك إنشاء نماذج الأصول التي يجب أن تكون مرتبطة بأنواع الأصول. وأخيراً، في صفحة **الإعدادات الافتراضية لأنواع الأصول**، يمكنك إنشاء كافة الأشكال المختلفة من أنواع الأصول المطلوبة لمعداتك.

## <a name="create-an-asset-type"></a>إنشاء نوع أصل

1. حدد **إدارة الأصول** > **الضبط** > **أنواع الأصول** > **أنواع الأصول**.
2. حدد **جديد** لإنشاء نوع أصل.
3. في حقل **نوع الأصل**، أدخل معرف نوع أصل.
4. في حقل **الاسم**، أدخل اسمًا.
5. في الحقل **نموذج دورة حياة الأصول**، حدد نموذج دورة حياة الأصول‏‎. لمزيد من المعلومات حول حالات دورة حياة الأصول ونماذج دورة حياة الأصول، راجع [حالات دورة حياة الأصول](object-stages.md).
6. عيّن الخيار **الإجمالي** إلى **نعم** إذا كان يجب حساب قيم مؤشر الأداء الأساسي‬ (KPI) الملخص للأصول التي لديها نوع الأصل هذا.
7. حدد **حفظ**.
8. على علامة التبويب السريعة **أنواع مهام الصيانة**، حدد أنواع مهام الصيانة التي يجب أن تكون مرتبطة بنوع الأصل:

    - لتحديد نوع وظيفة الصيانة، حدده في الحقل **أنواع وظائف الصيانة المتبقية**، ثم حدد زر السهم إلى اليمين ![زر السهم إلى اليمين](media/29-setup-for-objects.png) لنقله إلى قسم **أنواع وظائف الصيانة المحددة**.
    - لتحديد جميع أنواع وظائف الصيانة المتوفرة، حدد زر ![سهم إعادة توجيه الكل](media/30-setup-for-objects.png) . يتم تحويل جميع أنواع مهام الصيانة من الحقل **أنواع مهام الصيانة المتبقية** إلى الحقل **أنواع مهام الصيانة المحددة**.
    - لإلغاء تحديد نوع وظيفة الصيانة، حدده في الحقل **أنواع وظائف الصيانة المحددة**، ثم حدد زر السهم إلى اليسار ![زر السهم إلى اليسار](media/31-setup-for-objects.png) لنقله إلى قسم **أنواع وظائف الصيانة المتبقية**.

9. يمكنك أيضاً تحديد العدادات التي يجب أن تكون مرتبطة بنوع الأصل. على علامة التبويب السريعة **العدادات**، استخدم الطرق التي ورد وصفها لأنواع مهام الصيانة في الخطوة 8 لإجراء التحديدات. للحصول على المزيد من المعلومات حول إعداد العدادات، راجع [العدادات](counters.md).
10. يمكنك أيضاً تحديد أنواع السمات التي يجب أن تكون مرتبطة بنوع الأصل. على علامة التبويب السريعة **أنواع السمات**، استخدم الطرق التي ورد وصفها لأنواع مهام الصيانة في الخطوة 8 لإجراء التحديدات. بعد ذلك، لإنشاء التسلسل المفضل لأنواع السمات، حدد نوع سمة في الحقل **أنواع السمات المحددة**، واستخدم زري السهم لأعلى السهم ولأسفل لنقلها. سيتم عرض تسلسل أنواع السمات على الأصول التي تستخدم نوع الأصل هذا. لمزيد من المعلومات حول سمات الأصول، راجع [أنواع سمات الصيانة](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > عند إضافة أنواع سمات جديدة على علامة التبويب السريعة **أنواع السمات**، يتم تحديث الأصول الموجودة تلقائيًا بتلك المعلومات.

11. يمكنك أيضاً تحديد قوالب تقييمات الحالة التي يجب أن تكون مرتبطة بنوع الأصل. على علامة التبويب السريعة **تقييمات الحالة**، استخدم الطرق التي ورد وصفها لأنواع مهمة الصيانة في الخطوة 8 لإجراء التحديدات. لمزيد من المعلومات حول قوالب تقييم الحالة والتسجيلات، راجع [تقييم الحالة](../setup-for-objects/condition-assessment.md).
12. تعرض علامة التبويب السريعة **نموذج الأصل** كافة مجموعات الشركات المصنعة للأصول والنماذج التي تم إعدادها في نوع الأصل المحدد. لمشاهدة المجموعات مقسمة وفقًا للشركة المصنعة، حدد **نموذج الأصل** لفتح صفحة **نموذج الأصل**.

    في صفحة **نموذج الأصل**، يمكنك إضافة علاقات بين نوع الأصل ونموذج الأصل. بالإضافة إلى ذلك، في صفحة **أنواع الأصول**، يمكنك إضافة علاقات بين الشركة المصنعة للأصل ونموذج الأصل إلى نوع أصل بشكل مباشر. وأخيراً، في صفحة **نموذج الأصل** (**إدارة الأصول** \> **الإعداد** \> **الأصول‏‎** \> **نموذج الأصل**)، يمكنك إنشاء علاقات جديدة بين الشركة المصنعة للأصل ونموذج الأصل ونوع الأصل. وبالتالي، هناك ثلاث طرق لإعداد وتحرير العلاقات بين الشركة المصنعة للأصل ونموذج الأصل ونوع الأصل.‬ تظهر كافة المجموعات المتوفرة من منظورات مختلفة، ويمكنك تحديد نقطة الإدخال المفضلة لديك عند التعامل مع الإعداد.

> [!NOTE]
> - إذا قمت بتحديد عدادات في نوع أصل، فإنه سيتم تحديث التحديدات في الصفحة **العدادات** (**إدارة الأصول** > **الإعداد** > **الأصول** > **أنواع الأصول** > **العدادات**).
> - تعرض الحقول الموجودة في قسم  **التفاصيل** في علامة التبويب السريعة **عام** عدد مهام الصيانة، والعدادات، والسمات، وما إلى ذلك، التي تم إعدادها في نوع الأصل المحدد.

عادةً ما ترتبط أوامر العمل التي يتم إنشاؤها يدويًا بالصيانة التصحيحية، بينما ترتبط أوامر العمل التي يتم إنشاؤها تلقائيًا بالصيانة الوقائية. عند إنشاء أوامر العمل يدويًا، يمكن استخدام فقط أنواع مهام الصيانة المحددة على علامة التبويب السريعة **أنواع مهام الصيانة** في صفحة **أنواع الأصول**. ومع ذلك، بإمكان أوامر العمل التي تم إنشاؤها تلقائيًا استخدام جميع أنواع مهام الصيانة التي تقوم بإنشائها في صفحة **أنواع مهام الصيانة** (**إدارة الأصول** \> **الإعداد** \> **الوظائف** \> **أنواع الوظائف**).

## <a name="create-asset-type-setup-lines"></a>إنشاء بنود إعداد نوع الأصل

1. حدد **إدارة الأصول** \> **الإعداد‏‎** \> **الأصول‏‎** \> **أنواع الأصول** \> **إعداد نوع الأصل**. أو حدد **إدارة‏‎ الأصول** \> **الإعداد** \> **الأصول‏‎** \> **أنواع الأصول‏‎** \> **أنواع الأصول**، وحدد نوع أصل، ثم حدد **إعداد نوع الأصل‏‎**.
2. في المرة الأولى التي تستخدم فيها صفحة **إعداد نوع الأصل**، قد تجد الزر **إنشاء مجموعات** مفيدًا. يمكنك استخدام هذا الزر لإنشاء كافة مجموعات نموذج الأصل بسرعة على نوع أصل. حدد **إنشاء مجموعات**، وحدد نوع الأصل لإنشاء مجموعات له، ثم حدد **موافق**.

    > [!NOTE]
    > إذا كنت لن تستخدم كافة مجموعات إعداد نوع الأصل التي تم إنشاؤها تلقائيًا، فيمكنك حذف إعداد عن طريق تحديده ثم تحديد **حذف**.

3. حدد **جديد** لإنشاء إعداد نوع أصل بشكل يدوي.
4. وبحسب درجة التحديد التي تريدها لإعداد نوع الأصل، يمكنك إجراء التحديدات في حقول **نوع الأصل** و **الشركة المصنعة** و **النموذج**.
5. إذا كانت اتفاقية الضمان مرتبطة بنوع الأصل، فحدد‏‎ الاتفاقية في الحقلين **ضمان المورّد** و **ضمان العميل**. 
6. في علامة التبويب السريعة **قطع الغيار**، حدد **إضافة** لإضافة قطع غيار إلى إعداد نوع الأصل المحدد.
7. للموافقة على قطعة غيار، حدد بند قطعة الغيار، ثم حدد **موافقة**. يمكنك تحديد بنود متعددة للموافقة عليها.
8. لمعرفة إن كانت قطعة غيار مستخدمة في مكان آخر في إدارة الأصول (على سبيل المثال، فيما يتعلق بالأصول وأوامر العمل)، حدد بند قطعة الغيار، ثم حدد **مكان استخدام الصنف** لفتح الصفحة **مكان استخدام الصنف**. لرؤية كافة قطع الغيار النشطة في القائمة، حدد خانة الاختيار **نشطة**. لرؤية قطع الغيار الموافق عليها فقط، حدد خانة الاختيار **موافق عليها**.
9. في علامة التبويب السريعة **خطط الصيانة**، حدد **إضافة** لإضافة خطط الصيانة إلى إعداد نوع الأصل المحدد.
10. لنسخ إعداد نوع أصل إلى إعداد آخر، يمكنك استخدام الدالة "نسخ". حدد إعداد نوع الأصل لنسخ إعداد، وحدد **نسخ الإعداد**، ثم حدد إعداد نوع الأصل لنسخ الإعداد منه. تحدد إعدادات الخيارات المختلفة مقدار المعلومات المضمنة. عند الانتهاء، حدد **موافق** لنسخ الإعداد.

> [!NOTE]
> إذا كان لديك العديد من بنود قطع الغيار وبنود خطط الصيانة التي ستعيد استخدامها، تتيح لك الدالة "نسخ" إعداد البيانات بسرعة وسهولة للعديد من مجموعات إعداد نوع الأصل.

## <a name="spare-parts-on-the-asset-type-setup"></a>قطع الغيار في إعداد نوع الأصل

كما ورد وصفه في القسم "إنشاء بنود إعداد نوع الأصل"، يتم إعداد‏‎ قطع الغيار على نماذج الأصول في صفحة **إعداد نوع الأصل**. لذلك، عندما تفتح صفحة **إعداد نوع الأصل**، سترى فقط قطع الغيار المرتبطة بالمجموعة المحددة من نوع الأصل والشركة المصنعة للأصل ونموذج الأصل. للاطلاع على قائمة بجميع سجلات قطع الغيار، افتح صفحة **قطع الغيار** (**إدارة الأصول** \> **الاستعلامات** \> **قطع الغيار**).

في صفحة **قطع الغيار**، يمكنك أيضًا إنشاء قطع غيار جديدة للمجموعات الموجودة من نوع الأصل والشركة المصنعة للأصل ونموذج الأصل. يمكنك تقرير إن كنت تفضل إنشاء سجلات قطع الغيار في صفحة **إعداد نوع الأصل** أو صفحة **قطع الغيار**. توفر صفحة **إعداد نوع الأصل** نظرة عامة على البيانات المتعلقة بالمجموعة المحددة من نوع الأصل والشركة المصنعة للأصول ونموذج الأصل، حيث توفر صفحة **قطع الغيار** نظرة عامة كاملة على كافة بنود إعداد نوع الأصل. إذا احتوت صفحة **قطع الغيار** على الكثير من السجلات، فقد تقدم لك صفحة **إعداد نوع الأصل** نظرة عامة أفضل.

لمعرفة إن كانت قطعة الغيار على البند المحدد مستخدمة في مكان آخر في إدارة الأصول (على سبيل المثال، فيما يتعلق بالأصول وأوامر العمل)، حدد **مكان استخدام الصنف** لفتح الصفحة **مكان استخدام الصنف**. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]