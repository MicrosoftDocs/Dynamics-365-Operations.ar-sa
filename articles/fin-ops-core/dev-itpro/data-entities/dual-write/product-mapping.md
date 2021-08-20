---
title: تجربة المنتجات الموحدة
description: يوضح هذا الموضوع تكامل بيانات المنتج بين تطبيقات Finance and Operations وDataverse.
author: t-benebo
ms.date: 12/12/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 328791cc321eeaf8f032a1eecedbe50cf9498eccd442c718d2e44e246915bc9d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726177"
---
# <a name="unified-product-experience"></a>تجربه المنتج الموحدة

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

عندما يتكون النظام البيئي للشركة من تطبيقات Dynamics 365، مثل Finance وSupply Chain Management وSales، من الطبيعي أن تستخدم الشركات هذه التطبيقات لتوريد بيانات المنتجات. ويعود السبب في ذلك إلى أن هذه التطبيقات توفر بنية تحتية قوية للمنتجات تكملها مفاهيم تسعير معقدة وبيانات دقيقة تتعلق بالمخزون المتوفر. بإمكان الشركات التي تستخدم نظامًا خارجيًا لإدارة دورة حياة المنتج (PLM) لتوريد بيانات المنتجات توجيه المنتجات من تطبيقات Finance and Operations إلى تطبيقات Dynamics 365 الأخرى. تقوم تجربة المنتجات الموحدة بإحضار نموذج بيانات المنتجات المتكاملة إلى Dataverse، لتمكين جميع مستخدمي التطبيقات، بمن فيهم مستخدمي Power Platform من الاستفادة من بيانات المنتجات القادمة من تطبيقات Finance and Operations.

فيما يلي نموذج بيانات المنتجات من Sales.

![نموذج بيانات للمنتجات في CE.](media/dual-write-product-4.jpg)

فيما يلي نموذج بيانات المنتجات من تطبيقات Finance and Operations.

![نموذج البيانات للمنتجات في Finance and Operations.](media/dual-write-products-5.jpg)

تم دمج نموذجي بيانات المنتجات في Dataverse كما هو موضح أدناه.

![نموذج بيانات للمنتجات في تطبيقات Dynamics 365.](media/dual-write-products-6.jpg)

تم تصميم تخطيطات جدول الكتابة المزدوجة لتمكين تدفق البيانات باتجاه واحد، وهي عبارة عن تجربة قريبة من الوقت الحقيقي من تطبيقات Finance and Operations إلى Dataverse. ومع ذلك، فقد تم فتح البنية الأساسية للمنتجات لجعلها ثنائية الاتجاه إذا لزم الأمر. وعلى الرغم من ذلك، يمكنك تخصيصها على مسؤوليتك الخاصة، لأن Microsoft لا تنصح باتباع هذا الأسلوب.

## <a name="templates"></a>القوالب

تحتوي معلومات المنتج على كافة المعلومات المرتبطة بالمنتج وتعريفه، مثل أبعاد المنتج أو أبعاد التعقب والتخزين. كما يوضح الجدول التالي، يتم إنشاء مجموعة من مخططات الجداول لمزامنة المنتجات والمعلومات المتعلقة بها.

تطبيقات Finance and Operations | تطبيقات Dynamics 365 الأخرى | الوصف
-----------------------|--------------------------------|---
[كل المنتجات](mapping-reference.md#138) | msdyn_globalproducts | يحتوي جدول جميع المنتجات على جميع المنتجات المتوفرة في تطبيقات Finance and Operations، وكلٍّ من المنتجات الصادرة والمنتجات غير الصادرة على حدٍ سواء.
[المنتجات المميزة الصادرة‬ CDS](mapping-reference.md#213) | منتج | يحتوي الجدول **المنتج** على الأعمدة التي تعرّف المنتج. ويتضمن منتجات فردية (منتجات مع نوع فرعي للمنتج) ومتغيرات المنتج. يعرض الجدول التالي التعيينات.
[الألوان](mapping-reference.md#170) | msdyn\_productcolors
[التكوينات](mapping-reference.md#171) | msdyn\_productconfigurations
[إعدادات الأوامر الافتراضية](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[فئات المنتج](mapping-reference.md#166) | msdyn_productcategories | يتم تضمين كل من فئات المنتجات والمعلومات المتعلقة ببنيته وخصائصه في جدول فئة المنتج.
[تعيينات فئات المنتج](mapping-reference.md#167) | msdyn_productcategoryassignments | لتعيين منتج إلى فئة، يمكن استخدام جدول تعيينات فئات المنتجات.
[التدرجات الهرمية لفئات المنتجات](mapping-reference.md#168) | msdyn_productcategoryhierarchies | ويمكنك استخدام التدرجات الهرمية للمنتجات لتصنيف أو تجميع المنتجات. تتوفر التسلسلات الهرمية للفئات في Dataverse باستخدام جدول التسلسل الهرمي لفئة المنتج.
[أدوار التدرجات الهرمية لفئات المنتجات](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles | يمكن استخدام التدرجات الهرمية للمنتجات للأدوار المختلفة في D365 Finance and Operations. يُستخدم تحديد الفئة في كل دور يتم استخدام جدول دور فئة المنتج فيه.
[إعدادات الأوامر الافتراضية للمنتج V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |
[مجموعات أبعاد المنتجات](mapping-reference.md#173) | msdyn\_productdimensiongroups | تقوم مجموعة أبعاد المنتج بتعريف أبعاد المنتج التي تعرّف المنتج.
[ألوان أصل المنتج](mapping-reference.md#187) | msdyn_sharedproductcolors | يشير الجدول **لون المنتج المشترك** إلى الألوان التي يمكن أن تكون متوفرة في أصل منتج معين. تم ترحيل هذا المفهوم إلى Dataverse للحفاظ على تناسق البيانات.
[تكوينات أصل المنتج](mapping-reference.md#188) | msdyn_sharedproductconfigurations | يشير الجدول **تكوين المنتج المشترك** إلى التكوينات التي يمكن أن تكون متوفرة في أصل منتج معين. تم ترحيل هذا المفهوم إلى Dataverse للحفاظ على تناسق البيانات.
[أحجام أصل المنتج](mapping-reference.md#190) | msdyn_sharedproductsizes | يشير الجدول **حجم المنتج المشترك** إلى الأحجام التي يمكن أن تكون متوفرة في أصل منتج معين. تم ترحيل هذا المفهوم إلى Dataverse للحفاظ على تناسق البيانات.
[أنماط أصل المنتج](mapping-reference.md#191) | msdyn_sharedproductstyles | يشير الجدول **نمط المنتج المشترك** إلى الأنماط التي يمكن أن تكون متوفرة في أصل منتج معين. تم ترحيل هذا المفهوم إلى Dataverse للحفاظ على تناسق البيانات.
[عرض الأكواد الشريطية المحددة لأرقام المنتجات](mapping-reference.md#164) | msdyn\_productbarcodes | يتم استخدام الأكواد الشريطية للمنتجات لتحديد المنتجات بشكل فريد.
[تحويلات الوحدات‬ الخاصة بالمنتج](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[المنتجات الصادرة V2](mapping-reference.md#189) | msdyn\_sharedproductdetails | يحتوي الجدول **msdyn\_sharedproductdetails** على حقول من تطبيقات Finance and Operations التي تحدد المنتج، والتي تحتوي على معلومات مالية وإدارية خاصة بالمنتج.
[الأحجام](mapping-reference.md#174) | msdyn\_productsizes
[مجموعات أبعاد التخزين](mapping-reference.md#177) | msdyn_productstoragedimensiongroups | تمثل مجموعة أبعاد تخزين المنتج الطريقة المستخدمة لتحديد وضع المنتج في المستودع.
[الأنماط](mapping-reference.md#178) | msdyn\_productsytles
[مجموعات أبعاد التعقب](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups | تمثل مجموعة ابعاد تعقب المنتج الطريقة المستخدمة لتتبع المنتج في المخزون.
[الوحدات](mapping-reference.md#219) | uoms
[تحويلات الوحدات](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="integration-of-products"></a>تكامل المنتجات

في هذا النموذج، يتم تمثيل المنتج بواسطة مجموعة مكونة من جدولين في Dataverse: **المنتج** و **msdyn\_sharedproductdetails**. بينما يحتوي الجدول الأول على تعريف منتج (المعرف الفريد للمنتج واسم المنتج والوصف)، يحتوي الجدول الثاني على الأعمدة المخزنة على مستوي المنتج. يتم استخدام مجموعة هذين الجدولين لتحديد المنتج وفقًا لمفهوم وحدة حفظ المخزون (SKU). سيكون لكل منتج تم إصداره معلومات خاصة به في الجدولين المذكورة (تفاصيل المنتج والمنتج المشترك). لتعقب جميع المنتجات (الصادرة وغير الصادرة)، يتم استخدام الجدول **المنتجات العامة**.

وبسبب تمثيل المنتج على أنه وحدة SKU، يمكن تسجيل مفاهيم المنتجات المميزة وأصول المنتجات ومتغيرات المنتجات في Dataverse بالطريقة التالية:

- **منتجات مع نوع فرعي للمنتج** هي منتجات يتم تعريفها بنفسها. لا يجب تعريف أي أبعاد. على سبيل المثال، دفتر خاص. بالنسبة إلى هذه المنتجات، يتم إنشاء‏‎ سجل في الجدول **المنتج**، ويتم إنشاء سجل في كيان **msdyn\_sharedproductdetails**. لا يتم إنشاء صف لمجموعة المنتجات.
- تُستخدم **أصول المنتجات** كمنتجات عامه تحتفظ بالتعريف والقواعد التي تحدد السلوك في العمليات التجارية. استنادًا إلى هذه التعريفات، يمكن إنشاء المنتجات المميزة المعروفة على أنها متغيرات المنتجات. على سبيل المثال، يعد القميص هو أصل المنتج، واللون والحجم هما أبعاده. يمكن إصدار متغيرات المنتجات التي لديها مجموعات مختلفة من هذه الأبعاد، مثل قميص أزرق صغير الحجم أو قميص أخضر متوسط الحجم. في عملية التكامل، يتم إنشاء صف واحد لكل متغير في جدول المنتجات. يحتوي هذا الصف على المعلومات الخاصة بالمتغير، مثل الأبعاد المختلفة. يتم تخزين المعلومات العامة الخاصة بالمنتج في الجدول **msdyn\_sharedproductdetails**. ‏‫(يتم الاحتفاظ بهذه المعلومات العامة في أصل المنتج.) تتم مزامنة معلومات أصل للمنتج مع Dataverse عند إنشاء أصل المنتج الصادر (ولكن قبل إصدار المتغيرات).
- تشير **المنتجات المميزة** إلى كافة منتجات النوع الفرعي للمنتجات وكافة متغيرات المنتجات.

![نموذج بيانات للمنتجات.](media/dual-write-product.png)

مع تمكين وظيفة الكتابة المزدوجة، ستتم مزامنة المنتجات من Finance and Operations مع منتجات Dynamics 365 الأخرى في حالة **المسودة**. وتُضاف إلى قائمة الأسعار الأولى بالعملة نفسها. بمعنى آخر، تُضاف إلى أول قائمة أسعار في تطبيق Dynamics 365 التي تتطابق مع عملة الجدول القانوني حيث يتم إصدار المنتج في تطبيق Finance and Operations. في حاله عدم وجود قائمه أسعار للعملة المحددة، سيتم إنشاء قائمه أسعار تلقائيا سيتم تعيين المنتج اليها.

التنفيذ الحالي للوظائف الإضافية للكتابة المزدوجة التي تقوم بإقران قائمة الأسعار الافتراضية بالوحدة يبحث عن العملة المقترنة بتطبيق Finance and Operations ويعثر على قائمة الأسعار الأولى في تطبيق Customer Engagement باستخدام الفرز الأبجدي في اسم قائمة الأسعار. لتعيين قائمة أسعار افتراضية لعملة محددة عندما يكون لديك قوائم أسعار متعددة لهذه العملة، يجب تحديث اسم قائمة الأسعار إلى اسم موجود بترتيب أبجدي يسبق ترتيب أي قوائم أسعار أخرى لنفس تلك العملة.

وتتم مزامنة المنتجات الافتراضية من تطبيقات Finance and Operations مع تطبيقات Dynamics 365 الأخرى في حالة **المسودة**. لمزامنة المنتج مع الحالة **النشطة**، بحيث يمكنك استخدامه مباشرة في عروض أسعار أوامر المبيعات، على سبيل المثال، يجب اختيار الإعداد التالي: علامة التبويب **النظام > الإدارة > إدارة النظام> إعدادات النظام > Sales‎** حدد **إنشاء منتجات في الحالة النشطة = نعم**.

عند مزامنة المنتجات ، يجب إدخال قيمه لحقل **وحده المبيعات** في Finance and Operations التطبيق، نظرا لأنه حقل إلزامي في المبيعات.

لا يتم دعم إنشاء مجموعات المنتجات من Dynamics 365 Sales مع مزامنة المنتجات بالكتابة المزودوجة.

مزامنة المنتجات تحدث من تطبيقات Finance and Operations إلى Dataverse. وهذا يعني انه يمكن تغيير قيم حقول جدول المنتج في Dataverse، ولكن عند تشغيل المزامنة (عند تعديل حقل منتج في تطبيق Finance and Operations)، سيؤدي ذلك إلى الكتابة فوق القيم الواردة في Dataverse.

تطبيقات Finance and Operations | تطبيقات Customer Engagement |
---|---
[المنتجات المميزة الصادرة‬ CDS](mapping-reference.md#213) | منتج |
[المنتجات الصادرة V2](mapping-reference.md#189) | msdyn_sharedproductdetails |
[كل المنتجات](mapping-reference.md#138) | msdyn_globalproducts |

## <a name="product-dimensions"></a>أبعاد المنتجات

أبعاد المنتج هي الخصائص التي تحدد متغير المنتج. يتم أيضًا تعيين أبعاد المنتج الأربعة (اللون والحجم والنمط والتكوين) إلى Dataverse لتعريف متغيرات المنتج. يبين الرسم التوضيحي التالي نموذج البيانات لبعد المنتج "اللون". يتم تطبيق نفس النموذج على الأحجام والأنماط والتكوينات.

![نموذج البيانات لأبعاد المنتجات.](media/dual-write-product-two.png)

تطبيقات Finance and Operations | تطبيقات Customer Engagement |
---|---
[الألوان](mapping-reference.md#170) | msdyn\_productcolors
[الأحجام](mapping-reference.md#174) | msdyn\_productsizes
[الأنماط](mapping-reference.md#178) | msdyn\_productsytles
[التكوينات](mapping-reference.md#171) | msdyn\_productconfigurations

عندما يتضمن المنتج أبعاد منتج مختلفة (على سبيل المثال، يتضمن أصل المنتج الحجم واللون كأبعاد المنتج)، يتم تعريف كل منتج مميز (أي كل متغير منتج) كمجموعة من أبعاد المنتج هذه. على سبيل المثال، رقم المنتج B0001 هو قميص أسود صغير جدًا، ورقم المنتج B0002 هو قميص أسود صغير. وفي هذه الحالة، يتم تعرف مجموعات أبعاد المنتجات الموجودة. على سبيل المثال، بإمكان القميص المذكور في المثال السابق أن يكون أسود اللون وبحجم صغير جدًا أو أسود اللون وبحجم صغير أو أسود اللون وبحجم متوسط أو أسود اللون وبحجم كبير، ولكن لا يمكنه أن يكون أسود اللون وبحجم كبيرا جدًا. بمعنى آخر، يتم تحديد أبعاد المنتج التي يمكن ان يتخذها أصل المنتج، ويمكن إصدار المتغيرات استنادًا إلى هذه القيم.

لتعقب أبعاد المنتج التي يمكن ان يتخذها أصل المنتج، يتم إنشاء الجداول التالية وتعيينها في Dataverse لكل بعد منتج. لمزيد من المعلومات، راجع [نظرة عامة على معلومات المنتجات‬](../../../../supply-chain/pim/product-information.md).

تطبيقات Finance and Operations | تطبيقات Customer Engagement |
---|---
[ألوان أصل المنتج](mapping-reference.md#187) | msdyn_sharedproductcolors |
[تكوينات أصل المنتج](mapping-reference.md#188) | msdyn_sharedproductconfigurations |
[أحجام أصل المنتج](mapping-reference.md#190) | msdyn_sharedproductsizes |
[أنماط أصل المنتج](mapping-reference.md#191) | msdyn_sharedproductstyles |
[عرض الأكواد الشريطية المحددة لأرقام المنتجات](mapping-reference.md#164) | msdyn\_productbarcodes |

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>إعدادات الأوامر الافتراضية وإعدادات الأوامر الافتراضية الخاصة بالمنتج

تحدد إعدادات الأوامر الافتراضية الموقع والمستودع من حيث تؤخذ الأصناف أو حيث يتم تخزينها، والحد الأدنى من الكميات وحدها الأقصى ومضاعفاتها والكميات القياسية التي سيتم استخدامها للتجارة أو إدارة المخزون وزمن وصول البضاعة وعلامة الإيقاف وأسلوب التعهد بالأمر‬. تتوفر هذه المعلومات في Dataverse باستخدام كيان إعدادات الأوامر الافتراضية وإعدادات الأوامر الافتراضية الخاصة بالمنتج‬. يمكنك قراءة مزيد من المعلومات حول الوظائف في [موضوع إعدادات الأوامر الافتراضية](../../../../supply-chain/production-control/default-order-settings.md).

تطبيقات Finance and Operations | تطبيقات Customer Engagement |
---|---
[إعدادات الأوامر الافتراضية](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[إعدادات الأوامر الافتراضية للمنتج V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>وحدة القياس وتحويلات وحدة القياس

تتوفر وحدات القياس والتحويلات الخاصة بها في Dataverse باتباع لنموذج البيانات المعروض في الرسم التخطيطي.

![نموذج البيانات لوحدة القياس.](media/dual-write-product-three.png)

تم دمج مفهوم وحدة القياس بين تطبيقات Finance and Operations وتطبيقات Dynamics 365 الأخرى. لكل فئة وحدة في تطبيق Finance and Operations يتم إنشاء مجموعة وحدات في تطبيق Dynamics 365، تحتوي على الوحدات التي تنتمي إلى فئة الوحدة. كما يتم إنشاء وحدة أساسية افتراضية لكل مجموعة وحدات.

تطبيقات Finance and Operations | تطبيقات Customer Engagement |
---|---
[تحويلات الوحدات‬ الخاصة بالمنتج](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[الوحدات](mapping-reference.md#219) | uoms
[تحويلات الوحدات](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>المزامنة الأولية لمطابقة بيانات الوحدات بين Finance and Operations وDataverse

### <a name="initial-synchronization-of-units"></a>المزامنة الأولية للوحدات

عند تمكين الكتابة الثنائية، تتم مزامنة المنتجات من Finance and Operations إلى تطبيقات Dynamics 365 الأخرى. مجموعات الوحدات التي تتم مزامنتها من تطبيقات Finance and Operations في Dataverse تشتمل على مجموعة علامات تشير إلى أنها "محفوظة خارجيًا".

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>مطابقه بيانات الوحدات وفئات الوحدات/المجموعات من Finance and Operations وتطبيقات Dynamics 365 الأخرى

أولا، من المهم ملاحظه ان مفتاح التكامل الخاص بالوحدة هو msdyn_symbol. وبالتالي ، يجب ان تكون هذه القيمة فريدة في Dataverse أو تطبيقات Dynamics 365 الأخرى. ونظرا لوجودها في تطبيقات Dynamics 365 الأخرى ، فانها تمثل الزوج "معرف مجموعه الوحدات" و "الاسم" الذي يحدد تفرد الوحدة ، ويجب مراعاه سيناريوهات مختلفة لمطابقه بيانات الوحدة بين تطبيقات Finance and Operations وDataverse.

بالنسبة للوحدات المتطابقة/المتراكبه في تطبيقات Finance and Operations وتطبيقات Dynamics 365 الأخرى:

+ **تنتمي الوحدة إلى مجموعه وحدات في تطبيقات Dynamics 365 الأخرى التي تتوافق مع فئة الوحدة المرتبطة في تطبيقات Finance and Operations**. في هذه الحالة، يجب ملء العمود msdyn_symbol في تطبيقات Dynamics 365 الأخرى برمز الوحدة من تطبيقات Finance and Operations. وبالتالي ، عند مطابقة البيانات، سيتم تعيين مجموعه الوحدات على أنها "محفوظه خارجيًا" في تطبيقات Dynamics 365 الأخرى.
+ **تنتمي الوحدة إلى مجموعه وحدات في تطبيقات Dynamics 365 الأخرى التي لا تتوافق مع فئة الوحدة المقترنة في تطبيقات Finance and Operations (لا توجد فئة وحده موجودة في تطبيقات Finance and Operations الخاصة بفئة الوحدة في تطبيقات Dynamics 365 apps الأخرى).** في هذه الحالة ، يجب ان يتم ملء msdyn_symbol بسلسلة عشوائية. لاحظ أنه يجب ان تكون هذه القيمة فريدة في تطبيقات Dynamics 365 الأخرى.

بالنسبة للوحدات وفئات الوحدات في تطبيقات Finance and Operations غير الموجودة في تطبيقات Dynamics 365 الأخرى:

كجزء من الكتابة المزدوجة، يتم إنشاء ومزامنة مجموعات الوحدات من تطبيقات Finance and Operations ووحداتها المقابلة في تطبيقات Dynamics 365 الأخرى وDataverse وسيتم تعيين مجموعه الوحدات على أنها "محفوظة خارجيًا". لا يلزم وجود أي جهد تمهيد إضافي.

بالنسبة للوحدات في تطبيقات Dynamics 365 الأخرى وغير الموجودة في تطبيقات Finance and Operations:

يجب ملء العمود msdyn_symbol لكافة الوحدات. ويمكن دائما إنشاء الوحدات في تطبيقات Finance and Operations في فئة الوحدات المقابلة (إذا كانت موجودة). في حاله عدم وجود فئة الوحدة ، يجب أولا إنشاء فئة الوحدة (لاحظ انه لا يمكن إنشاء فئة وحده في تطبيقات Finance and Operations باستثناء الملحق إذا كنت تقوم بتوسيع التعداد) مع مطابقه مجموعه وحدات تطبيقات Dynamics 365 الأخرى. ويمكنك بعد ذلك إنشاء الوحدة. لاحظ أن رمز الوحدة في تطبيقات Finance and Operations يجب أن يكون msdyn_symbol المحدد مسبقًا في تطبيقات Dynamics 365 الأخرى للوحدة.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>سياسات المنتج: مجموعات الأبعاد والتعقب والتخزين

سياسات المنتج هي عبارة عن مجموعات من السياسات المستخدمة لتعريف المنتجات وخصائصها في المخزون. يمكن العثور على مجموعة أبعاد المنتج ومجموعة أبعاد تعقب المنتج ومجموعة أبعاد المنتج كسياسات المنتج.

تطبيقات Finance and Operations | تطبيقات Customer Engagement |
---|---
[مجموعات أبعاد المنتجات](mapping-reference.md#173) | msdyn\_productdimensiongroups |
[مجموعات أبعاد التخزين](mapping-reference.md#177) | msdyn_productstoragedimensiongroups |
[مجموعات أبعاد التعقب](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups |

## <a name="product-hierarchies"></a>التدرجات الهرمية للمنتجات

تطبيقات Finance and Operations | تطبيقات Customer Engagement |
---|---
[تعيينات فئات المنتج](mapping-reference.md#167) | msdyn_productcategoryassignments |
[التدرجات الهرمية لفئات المنتجات](mapping-reference.md#168) | msdyn_productcategoryhierarchies |
[أدوار التدرجات الهرمية لفئات المنتجات](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles |

## <a name="integration-key-for-products"></a>مفتاح تكامل المنتجات

لتحديد منتجات الهوية الفريدة بين  Dynamics 365 for Finance and Operations والمنتجات في Dataverse يتم استخدام مفاتيح التكامل.
بالنسبة للمنتجات، يكون **(productnumber)** هو المفتاح الفريد الذي يحدد منتجًا في Dataverse. ويتم تكوينه بواسطة سلسلة: **(company, msdyn_productnumber)**. تشير **الشركة** إلى الكيان القانوني في Finance and Operations و **msdyn_productnumber** إلى رقم المنتج الخاص بالمنتج المحدد في Finance and Operations.

بالنسبة لمستخدمي تطبيقات Dynamics 365 آخر، يتم تعريف المنتج في واجهة المستخدم بواسطة **msdyn_productnumber** (لاحظ ان تسميه العمود هي **رقم المنتج**). في نموذج المنتج، يتم عرض كل من الشركة وmsydn_productnumber. ومع ذلك، لا يتم عرض العمود (productnumber) والمفتاح الفريد لأحد المنتجات.

إذا قمت بإنشاء تطبيقات على Dataverse يجب عليك الانتباه إلى استخدام **productnumber‎** (معرف المنتج الفريد) كمفتاح تكامل. لا تستخدم **msdyn_productnumber**، لأنه ليس فريدا.

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>المزامنة الأولية للمنتجات وترحيل البيانات من Dataverse إلى Finance and Operations

### <a name="initial-synchronization-of-products"></a>المزامنة الأولية للمنتجات

عند تمكين الكتابة الثنائية، تتم مزامنة المنتجات من Finance and Operations إلى Dataverse وتطبيقات تفاعل العملاء الأخرى. المنتجات التي تم إنشاؤها في Dataverse وتطبيقات Dynamics 365 الأخرى قبل الكتابة الثنائية، لن يتم تحديثها أو مطابقتها مع بيانات المنتج من تطبيقات Finance and Operations.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>مطابقه بيانات المنتج من Finance and Operations وتطبيقات Dynamics 365 الأخرى

في حاله الاحتفاظ بنفس المنتجات (تراكب/مطابقه) في Finance and Operations وفي Dataverse وتطبيقات Dynamics 365 الأخرى، عند تمكين الكتابة المزدوجة ستحدث مزامنة المنتجات من Finance and Operations، وستظهر الصفوف المكررة في Dataverse لنفس المنتج.
لتجنب الموقف السابق، إذا كانت تطبيقات Dynamics 365 الأخرى لديها منتجات متداخلة/متطابقة مع Finance and Operations، فان المسؤول الذي يقوم بتمكين الكتابة الثنائية يجب ان يقوم بتمهيد الأعمدة **الشركة** (مثال: "USMF") و **msdyn_productnumber** (مثال: "1234:Black:S") قبل مزامنة المنتجات. بمعني آخر، يجب ان يتم ملء هذين العمودين الموجودين في المنتج في Dataverse بالشركة المعنية في Finance and Operations التي يحتاج اليها المنتج لتتم مطابقته مع ورقم المنتج الخاص به.

ثم عند تمكين المزامنة وحدوثها، ستتم مزامنة المنتجات من Finance and Operations مع المنتجات المتطابقة في Dataverse وتطبيقات Dynamics 365 الأخرى. ويكون هذا قابلا للتطبيق على كل من المنتجات المختلفة ومتغيرات المنتجتن.

### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>ترحيل بيانات المنتج من تطبيقات Dynamics 365 الأخرى إلى Finance and Operations

إذا كانت تطبيقات Dynamics 365 الأخرى تحتوي على منتجات غير موجودة في Finance and Operations، يمكن للمسؤول أولاً استخدام **EcoResReleasedProductCreationV2Entity** لاستيراد تلك المنتجات في Finance and Operations. وثانيًا، قم بمطابقه بيانات المنتج من Finance and Operations وتطبيقات Dynamics 365 الأخرى كما هو موضح أعلاه.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
