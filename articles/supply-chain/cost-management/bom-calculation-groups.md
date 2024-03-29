---
title: مجموعات حسابات قوائم مكونات الأصناف‬
description: توفر هذه المقالة معلومات حول مجموعات الحساب لقائمة مكونات الصنف وكيفية إعدادها. لتشغيل حساب قائمة مكونات الصنف، يجب إما إعداد مجموعات الحساب وتعيينها إلى أصناف فردية، أو تعيين مجموعة حساب افتراضية. ويتم عندئذٍ استخدام إعدادات الحساب من مجموعة الحساب كقيم افتراضية في صفحة حساب قائمة مكونات الصنف عند حساب قائمة مكونات الصنف.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcGroup, BOMCalcTable, BOMCalcTrans, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94063
ms.assetid: 63e1b7dc-c2c5-41b0-81ed-e3e02d1b39e0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2581d35fa02d800b07fcb40efb9d238685233898
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669813"
---
# <a name="bom-calculations-groups"></a>مجموعات حسابات قوائم مكونات الأصناف‬

[!include [banner](../includes/banner.md)]

توفر هذه المقالة معلومات حول مجموعات الحساب لقائمة مكونات الصنف وكيفية إعدادها. لتشغيل حساب قائمة مكونات الصنف، يجب إما إعداد مجموعات الحساب وتعيينها إلى أصناف فردية، أو تعيين مجموعة حساب افتراضية. ويتم عندئذٍ استخدام إعدادات الحساب من مجموعة الحساب كقيم افتراضية في صفحة حساب قائمة مكونات الصنف عند حساب قائمة مكونات الصنف. 

يجب أن تتوفر مجموعة حساب افتراضية في صفحة **محددات إدارة المستودعات والمخزون‬**، أو مجموعة حساب خاصة بالمنتجات في صفحة **تفاصيل المنتجات الصادرة**. يبحث النظام أولاً عن إعداد مجموعة الحساب في صفحة **تفاصيل المنتجات الصادرة**. وإذا لم يعثر على مجموعة حساب، فسيبحث في صفحة **محددات إدارة المستودعات والمخزون‬**. وإذا لم يعثر النظام على مجموعة حساب، فسيتلقى المستخدم رسالة خطأ أثناء الحساب. تحتوي مجموعة حساب على سياسات لنموذج سعر التكلفة ونموذج سعر المبيعات وقائمة اختيار التحذيرات. ويتم استخدام إعدادات الحساب من مجموعة الحساب كقيم افتراضية في صفحة **حساب قائمة مكونات الصنف** عند حساب قائمة مكونات الصنف.

## <a name="purposes-of-bom-calculation-groups"></a>أغراض مجموعات حساب قائمة مكونات الصنف
ستعيّن مجموعة حساب قائمة مكونات الصنف لعدة أسباب:

-   من خلال تعيين حقل **نموذج سعر التكلفة**، ستشير إلى مصدر بيانات مساهمة التكلفة لمكون تم شراؤه أثناء حساب التكلفة المخططة لصنف مصنّع. تقوم بعض الجهات المصنعة بحساب التكاليف المخططة باستخدام الاتفاقيات التجارية لسعر الشراء للمكونات التي تم شراؤها أو باستخدام أساس آخر، مثل سجلات سعر الشراء في إصدار التكاليف.
-   من خلال تعيين حقل **نموذج سعر المبيعات**، ستشير إلى الطريقة التي يتم بها استخدام بيانات الصنف لحساب سعر مبيعات مقترح. يمكنك تحديد إما سعر مبيعات الصنف أو مجموعة التكاليف. ترغب بعض الجهات المصنعة في حساب سعر مبيعات مقترح للأصناف المصنعة. بإمكان سعر المبيعات المحتسب أن يعكس طريقة تحديد كل عناصر التكلفة التي تستند إلى سجل سعر المبيعات المحدد للمكون. أو، بإمكان سعر المبيعات المحتسب أن يعكس طريقة حساب التكلفة زائد القيمة المضافة التي تستند إلى تكلفة المكون ونسبة الربح القابلة للتطبيق، والتي تقترن بمجموعة تكاليف الصنف.
-   باستخدام الحقل **إيقاف عملية تحديد إجمالي المكونات المطلوبة‬**، ستشير إلى وجوب معاملة الصنف المصنع كصنف مشترىً لأغراض تحديد كل عناصر التكلفة أثناء حساب قائمة مكونات الصنف. تتضمن السيناريوهات النموذجية صنفًا تم شراؤه وهو عبارة عن صنف مصنّع أحيانًا أو صنف مصنّع يتم شراؤه الآن. يتم تعيين الصنف أولاً كصنف مصنّع لتحديد قائمة مكونات الصنف ومعلومات المسار، ولدعم أوامر الإنتاج الخاصة بالصنف. ومع ذلك، تمنع علامة **إيقاف عملية تحديد إجمالي المكونات المطلوبة‬** حسابات التكلفة من استخدام قائمة مكونات الصنف الخاصة بالصنف ومساره. بدلاً من ذلك، يستخدم حساب قائمة مكونات الصنف تكاليف الصنف المحددة.

## <a name="calculation-groups"></a>مجموعات الحساب
يمكنك تحديد مجموعات الحساب تحت **إعداد سياسات التكلفة المحددة مسبقًا‬** في إدارة التكلفة. تسمح لك مجموعات الحساب التي تم تعيينها إلى أصناف بتحديد كيفية توريد تكلفة المكونات أو سعر مبيعاتها لإجراء عملية الحساب، كما هو موضح بواسطة مجموعة الحساب. في صفحة **مجموعات الحساب**، يمكنك تعريف نموذج سعر التكلفة ونموذج سعر التكلفة البديل ونموذج سعر مبيعات والتحذيرات.

### <a name="cost-price-model"></a>نموذج سعر التكلفة

توجد أربعة خيارات في حقل **نموذج سعر التكلفة**:

-   **سعر تكلفة الصنف** – بتم استخدام سعر التكلفة من جدول **المنتج الذي تم إصداره‬**، أو يتم استخدام مجموعة من أبعاد الصنف كسعر تكلفة
-   **سعر الشراء للصنف** – يتم استخدام سعر الشراء من حقل **سعر التكلفة** على علامة التبويب **شراء** في صفحة **قائمة المنتجات الصادرة**.
-   **الاتفاقيات التجارية** – يمكنك تكوين اتفاقيا تجارية لمجموعات محددة من الأصناف والموردين، أو لمواقع محددة. بعد ذلك، عندما تحدد خيار **الاتفاقيات التجارية** هنا، سيتم استخدام الاتفاقية التجارية التي قمت بإنشائها لسعر الشراء إلى جانب الصنف الموقع.
-   **سعر المخزون** – يتم استخدام قيمة المخزون الحالي للصنف لحساب تكلفة الوحدة في قائمة مكونات الصنف. يتم حساب سعر تكلفة الوحدة فقط إذا كانت الكمية التي تم ترحيلها والكمية الفعلية أكبر من 0 (صفر).

### <a name="alternative-cost-price"></a>سعر التكلفة البديل

يتضمن حقل **سعر التكلفة البديل** الخيارات نفسها الموجودة في حقل **نموذج سعر التكلفة** الحقل. ومع ذلك، يتم استخدام هذا الحقل فقط عندما يتعذر العثور على سعر في نموذج سعر التكلفة الأساسي.

### <a name="sales-price-model"></a>نموذج أسعار البيع

هناك خياران لحساب حقل **أسعار المبيعات**:

-   **مجموعة التكاليف** – عندما يتم تحديد هذا الخيار، يتم حساب سعر المبيعات استنادًا إلى سعر التكلفة ونسبة إعداد الربح من مجموعة التكاليف.
-   **سعر المبيعات للصنف** – عندما يتم تحديد هذا الخيار، يتم استخدام سعر المبيعات على علامة التبويب السريعة **بيع** من جدول المنتجات الصادرة.

### <a name="stop-explosion"></a>إيقاف عملية تحديد إجمالي المكونات المطلوبة

تُستخدم خانة الاختيار **إيقاف عملية تحديد إجمالي المكونات المطلوبة‬** للإشارة إلى الوقت الذي يجب فيه معاملة صنف مصنّع كصنف شراء. بشكل عام، ستترك خانة الاختيار **إيقاف عملية تحديد إجمالي المكونات المطلوبة‬** غير محددة. عندما تحدد خانة الاختيار هذه، ستشير إلى وجوب معاملة صنف مصنّع على أنه مكون مشترى بدلاً من مكون مصنّع، وذلك لأغراض حساب قائمة مكونات الصنف. وبحسب الموقع، لا يزال بالإمكان حساب تكلفة الصنف باستخدام عمليات قائمة مكونات الصنف. تتوقف عملية تحديد إجمالي المكونات المطلوبة‬ لأوامر الشراء المخططة وأوامر الإنتاج في قائمة مكونات الصنف ذات المكونات المقترنة بمجموعة الحساب التي تم تحديد خانة الاختيار **إيقاف عملية تحديد إجمالي المكونات المطلوبة‬** لها. وسوف تقوم عملية الجدولة الرئيسية بإنشاء الأوامر المخططة في قائمة مكونات الصنف بحد ذاتها، وليس في الأصناف التي تشتمل عليها قائمة مكونات الصنف. بشكل أساسي، من خلال تحديد خانة الاختيار هذه، ستحدد عدم إضافة التكلفة إلى حساب قائمة مكونات الصنف للأصناف التي لديها مجموعة الحساب هذه.

### <a name="warnings"></a>تحذيرات

على علامة التبويب السريعة **تحذيرات**، يمكنك تحديد الخيارات المتعلقة بأي رسائل تحذير من المفترض أن يتلقاها المستخدمون عند قيامهم بإجراء حسابات قائمة مكونات الصنف. 

على سبيل المثال، إذا حددت خانة الاختيار **لا توجد قائمة مكونات الصنف‬**، فسيتلقى المستخدم تحذيرًا إذا لم يتم العثور على إصدار قائمة مكونات الصنف النشطة لأحد المكونات أو الصنف الأصلي الذي تم تشغيل حساب قائمة مكونات الصنف له. وإذا حددت خانة الاختيار **‏‫لا يوجد مسار‬**، فسيتلقى المستخدم تحذيرًا إذا لم يتم العثور عل إصدار مسار نشط. إذا كنت تستخدم الموارد على المسارات والعمليات، فيمكنك توجيه النظام للتحقق من تلك الموارد. إذا لم يتم العثور عندئذٍ على مورد في كل بند في المسار النشط، فسيتلقى المستخدم تحذيرًا. 

يمكنك أيضًا التحقق من الاستهلاك‬ والتدقيق فيه. الاستهلاك‬ هو الكمية في مسار معين. وهو يمثل عادةً مقدار الوقت المطلوب لتنفيذ عملية محددة لعملية إنتاج. يمكنك التحقق من عدم وجود سعر تكلفة لأحد الأصناف. وفي حال عدم وجود سعر تكلفة نشط لأحد الأصناف، لن تتم إضافة أي تكلفة إلى حساب قائمة مكونات الصنف. 

يمكنك أيضا التحقق والتدقيق في عمر سعر التكلفة. على سبيل المثال، أدخل **60** للإشارة إلى أنه يجب إعادة تقييم سعر تكلفة الوحدة بعد 60 يومًا. إذا تم بلوغ هذا الحد، فسينشئ النظام تحذيرًا. على سبيل المثال، تم إدخال سعر تكلفة لكل صنف في شهر يناير من هذا العام. إذا وصلنا الآن إلى شهر أغسطس، وهي فترة تزيد عن 60 يومًا اعتبارًا من تاريخ إدخال سعر التكلفة، فسيتلقى المستخدم تحذيرًا عند تشغيل حساب قائمة مكونات الصنف. يمكنك إدخال نسبة مئوية في الحقل **الحد الأدنى لهامش المساهمة**. تشير هذه القيمة إلى النقطة التي لم يتم عندها تلبية الحد الأدنى لهامش المساهمة. إذا لم تتم تلبية هامش المساهمة لمكون معين، فسيتلقى المستخدم تحذيرًا. وبالتالي، يساعد هذا الحقل على ضمان عدم قيامك بتحجيم التكاليف وتكاليف النقل الإضافية التي قد تلزم لأصنافك.

### <a name="default-setup-in-inventory-and-warehouse-management-parameters"></a>الإعداد الافتراضي في محددات إدارة المستودعات والمخزون

بما أن مجموعات الحساب مطلوبة لتشغيل الحسابات، يجب إعداد مجموعة حساب افتراضية في محددات إدارة المخزون‬. يتيح هذا الإعداد للشركات إنشاء إعداد مجموعة تكاليف معيارية وأرباح لجميع الأصناف. عندئذٍ، إذا كان لصنف معين متطلبات حساب خاصة، يستطيع المستخدم تعيين مجموعة حساب مختلفة لهذا الصنف. يمكنك عادةً تعيين مجموعات الحساب على أصناف مكونات قائمة مكونات الصنف بدلاً من أصناف قائمة مكونات الصنف. ومع ذلك، عندما تظهر رسائل التحذير، يمكن تطبيق مجموعات الحساب. تقوم مجموعة حساب تم تعيينها إلى الأصناف بإبطال القيمة الافتراضية التي تم إعدادها في محددات إدارة المخزون. 

يمكنك إعداد المحددة الافتراضية في **إدارة التكلفة** &gt; **إعداد سياسات محاسبة المخزون** &gt; **المحددات** &gt; **محاسبة المخزون** &gt; **مجموعة الحساب**. من خلال إعداد مجموعة تكوين افتراضية، يمكنك أيضًا تكوين شروط التحذير التي تظهر للمستخدمين أثناء عملية حساب قائمة مكونات الصن، إذا كانت المكونات المحددة قد تتسبب في حدوث أخطاء في الحساب.

### <a name="view-warning-messages-on-the-complete-page"></a>عرض رسائل التحذير في الصفحة "مكتمل"

يؤدي حساب قائمة مكونات الصنف إلى إنشاء رسائل تحذير. يمكنك عرض التحذيرات المتعلقة بصنف محدد. على سبيل المثال، في المبيعات والتسويق، أنشئ أمر مبيعات جديدًا للصنف D0001. ثم، في بند أمر المبيعات، في قائمة **تحديث البند‬**، انقر فوق **الحساب بالاستناد إلى قائمة مكونات الصنف/المعادلة** لعرض تفاصيل الحساب والتحذيرات. يمكنك أيضًا عرض نتائج حساب قائمة مكونات الصنف في الصفحة **مكتمل**. بالنسبة إلى رسائل التحذير، ينطبق شرطان تحذيريان فقط على الأصناف المصنّعة، في حين تنطبق أربعة شروط تحذيرية على أي صنف:
-   تحديد متى لا يحتوى صنف مصنّع على قائمة مكونات صنف نشطة.
-   تحديد متى لا يحتوى صنف مصنّع على مسار نشط.
-   تحديد متى تساوي كمية صنف في قائمة مكونات الصنف 0 (صفر).
-   تحديد متى تساوي تكلفة الصنف الموجود في قائمة مكونات الصنف 0 (صفر) أو متى لا يوجد سجل تكلفة لهذا الصنف.
-   تحديد متى تكون تكلفة الصنف في قائمة مكونات منتهية الصلاحية. يعكس التحذير مقارنةً بين تاريخ الحساب والأيام المحددة للحد الأقصى لعمر التكلفة.
-   تحديد متى تكون نسبة الربحية لصنف في قائمة مكونات الصنف أقل من النسبة التي تريدها.

يمكنك تحديد مجموعات حساب متعددة لقائمة مكونات الصنف، وهذا يتوقف على احتياجاتك فيما يتعلق بالتباينات في رسائل التحذير. على سبيل المثال، قد تكفي مجموعة واحدة من قائمة مكونات الصنف لديها شروط تحذيرية حول قائمة مكونات الصنف النشطة وكمية مكونات من 0 (صفر) وتكلفة مكونات من 0 (صفر) كافية. عندما تبدأ حساب قائمة مكونات الصنف، يمكنك إبطال الشروط التحذيرية المقترنة بمجموعة حساب قائمة مكونات الصنف. ويمكنك أيضًا إضافة الشروط التحذيرية أو إزالتها. على سبيل المثال، إذا لم تتضمن الحالة الحالية بيانات توجيه، فيمكنك إزالة الشرط التحذيري المتعلق بالمسار النشط. **ملاحظة:** يتضمن الوقت والحضور صفحة **مجموعات الحساب**، ولكن هذه الصفحة ليس لها أي علاقة بمجموعات حساب قائمة مكونات الصنف. في الوقت والحضور، يمكن تعيين العاملين لمجموعات الحساب التي تعكس مجموعة العمال المرتبطين بنفس المشرف أو المدير. ويمكن حساب تسجيلات العامل إما تلقائيًا أو يدويًا من قبل المشرف أو المدير.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]