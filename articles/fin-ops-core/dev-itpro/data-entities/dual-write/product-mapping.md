---
title: تجربة المنتجات الموحدة
description: يوضح هذا الموضوع تكامل بيانات المنتج بين تطبيقات Finance and Operations وCommon Data Service.
author: t-benebo
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ed8f0351d1e16cceb6c9749f434a8980ef2be29d
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835844"
---
# <a name="unified-product-experience"></a>تجربه المنتج الموحدة

[!include [banner](../../includes/banner.md)]



عندما يتكون النظام البيئي للشركة من تطبيقات Dynamics 365، مثل Finance وSupply Chain Management وSales، من الطبيعي أن تستخدم الشركات هذه التطبيقات لتوريد بيانات المنتجات. ويعود السبب في ذلك إلى أن هذه التطبيقات توفر بنية تحتية قوية للمنتجات تكملها مفاهيم تسعير معقدة وبيانات دقيقة تتعلق بالمخزون المتوفر. بإمكان الشركات التي تستخدم نظامًا خارجيًا لإدارة دورة حياة المنتج (PLM) لتوريد بيانات المنتجات توجيه المنتجات من تطبيقات Finance and Operations إلى تطبيقات Dynamics 365 الأخرى. تقوم تجربة المنتجات الموحدة بإحضار نموذج بيانات المنتجات المتكاملة إلى Common Data Service، لتمكين جميع مستخدمي التطبيقات، بمن فيهم مستخدمي Power Platform من الاستفادة من بيانات المنتجات القادمة من تطبيقات Finance and Operations.

فيما يلي نموذج بيانات المنتجات من Sales.

![نموذج بيانات للمنتجات في CE](media/dual-write-product-4.jpg)

فيما يلي نموذج بيانات المنتجات من تطبيقات Finance and Operations.

![نموذج البيانات للمنتجات في Finance and Operations](media/dual-write-products-5.jpg)

تم دمج نموذجي بيانات المنتجات في Common Data Service كما هو موضح أدناه.

![نموذج بيانات للمنتجات في تطبيقات Dynamics 365](media/dual-write-products-6.jpg)

تم تصميم تخطيطات كيان الكتابة المزدوجة لتمكين تدفق البيانات باتجاه واحد، وهي عبارة عن تجربة قريبة من الوقت الحقيقي من تطبيقات Finance and Operations إلى Common Data Service. ومع ذلك، فقد تم فتح البنية الأساسية للمنتجات لجعلها ثنائية الاتجاه إذا لزم الأمر. وعلى الرغم من ذلك، يمكنك تخصيصها على مسؤوليتك الخاصة، لأن Microsoft لا تنصح باتباع هذا الأسلوب.

## <a name="templates"></a>القوالب

تحتوي معلومات المنتج على كافة المعلومات المرتبطة بالمنتج وتعريفه، مثل أبعاد المنتج أو أبعاد التعقب والتخزين. كما يوضح الجدول التالي، يتم إنشاء مجموعة من مخططات الكيانات لمزامنة المنتجات والمعلومات المتعلقة بها.

تطبيقات Finance and Operations | تطبيقات Dynamics 365 الأخرى | ‏‏الوصف
-----------------------|--------------------------------|---
المنتجات الصادرة V2 | msdyn\_sharedproductdetails | يحتوي الكيان **msdyn\_sharedproductdetails** على حقول من تطبيقات Finance and Operations التي تحدد المنتج، والتي تحتوي على معلومات مالية وإدارية خاصة بالمنتج. 
المنتجات المميزة الصادرة لـ Common Data Service | منتج | يحتوي كيان‏‎ **المنتج** على الحقول التي تعرّف المنتج. ويتضمن منتجات فردية (منتجات مع نوع فرعي للمنتج) ومتغيرات المنتج. يعرض الجدول التالي التعيينات.
الكود الشريطي المحدد لرقم المنتج | msdyn\_productbarcodes | يتم استخدام الأكواد الشريطية للمنتجات لتحديد المنتجات بشكل فريد.
إعدادات الأوامر الافتراضية | msdyn\_productdefaultordersettings
إعدادات الأوامر الافتراضية الخاصة بالمنتج | msdyn_productdefaultordersettings
مجموعات أبعاد المنتجات | msdyn\_productdimensiongroups | تقوم مجموعة أبعاد المنتج بتعريف أبعاد المنتج التي تعرّف المنتج. 
مجموعات أبعاد التخزين | msdyn\_productstoragedimensiongroups | تمثل مجموعة أبعاد تخزين المنتج الطريقة المستخدمة لتحديد وضع المنتج في المستودع.
مجموعات أبعاد التعقب | msdyn\_producttrackingdimensiongroups | تمثل مجموعة ابعاد تعقب المنتج الطريقة المستخدمة لتتبع المنتج في المخزون.
الألوان | msdyn\_productcolors
الأحجام | msdyn\_productsizes
الأنماط | msdyn\_productsytles
التكوينات | msdyn\_productconfigurations
ألوان أصل المنتج | msdyn_sharedproductcolors | يشير الكيان **لون المنتج المشترك** إلى الألوان التي يمكن أن تكون متوفرة في أصل منتج معين. تم ترحيل هذا المفهوم إلى Common Data Service للحفاظ على تناسق البيانات.
أحجام أصل المنتج | msdyn_sharedproductsizes | يشير الكيان **حجم المنتج المشترك** إلى الأحجام التي يمكن أن تكون متوفرة في أصل منتج معين. تم ترحيل هذا المفهوم إلى Common Data Service للحفاظ على تناسق البيانات.
أنماط أصل المنتج | msdyn_sharedproductstyles | يشير الكيان **نمط المنتج المشترك** إلى الأنماط التي يمكن أن تكون متوفرة في أصل منتج معين. تم ترحيل هذا المفهوم إلى Common Data Service للحفاظ على تناسق البيانات.
تكوينات أصل المنتج | msdyn_sharedproductconfigurations | يشير الكيان **تكوين المنتج المشترك** إلى التكوينات التي يمكن أن تكون متوفرة في أصل منتج معين. تم ترحيل هذا المفهوم إلى Common Data Service للحفاظ على تناسق البيانات.
كافة المنتجات | msdyn_globalproducts | يحتوي كيان جميع المنتجات على جميع المنتجات المتوفرة في تطبيقات Finance and Operations، وكلٍّ من المنتجات الصادرة والمنتجات غير الصادرة على حدٍ سواء.
الوحدة | uoms
تحويلات الوحدات | msdyn_ unitofmeasureconversions
تحويل وحدة قياس خاصة بالمنتج | msdyn_productspecificunitofmeasureconversion
فئات المنتج | msdyn_productcategories | يتم تضمين كل من فئات المنتجات والمعلومات المتعلقة ببنيته وخصائصه في كيان فئة المنتج. 
التدرجات الهرمية لفئات المنتجات | msdyn_productcategoryhierarhies | ويمكنك استخدام التدرجات الهرمية للمنتجات لتصنيف أو تجميع المنتجات. تتوفر التسلسلات الهرمية للفئات في Common Data Service باستخدام كيان التسلسل الهرمي لفئة المنتج. 
أدوار التدرجات الهرمية لفئات المنتجات | msdyn_productcategoryhierarchies | يمكن استخدام التدرجات الهرمية للمنتجات للأدوار المختلفة في D365 Finance and Operations. يُستخدم تحديد الفئة في كل دور يتم استخدام كيان دور فئة المنتج فيه. 
تعيينات فئات المنتج | msdyn_productcategoryassignments | لتعيين منتج إلى فئة، يمكن استخدام كيان تعيينات فئات المنتجات.

## <a name="integration-of-products"></a>تكامل المنتجات

في هذا النموذج، يتم تمثيل المنتج بواسطة مجموعة مكونة من كيانين في Common Data Service: **المنتج** و**msdyn\_sharedproductdetails**. بينما يحتوي الكيان الأول على تعريف منتج (المعرف الفريد للمنتج واسم المنتج والوصف)، يحتوي الكيان الثاني على الحقول المخزنة على مستوي المنتج. يتم استخدام مجموعة هذين الكيانين لتحديد المنتج وفقًا لمفهوم وحدة حفظ المخزون (SKU). سيكون لكل منتج تم إصداره معلومات خاصة به في الكيانات المذكورة (تفاصيل المنتج والمنتج المشترك). لتعقب جميع المنتجات (الصادرة وغير الصادرة)، يتم استخدام كيان **المنتجات العامة**. 

وبسبب تمثيل المنتج على أنه وحدة SKU، يمكن تسجيل مفاهيم المنتجات المميزة وأصول المنتجات ومتغيرات المنتجات في Common Data Service بالطريقة التالية:

- **منتجات مع نوع فرعي للمنتج** هي منتجات يتم تعريفها بنفسها. لا يجب تعريف أي أبعاد. على سبيل المثال، دفتر خاص. بالنسبة إلى هذه المنتجات، يتم إنشاء‏‎ سجل في كيان **المنتج**، ويتم إنشاء سجل في كيان **msdyn\_sharedproductdetails**. لا يتم إنشاء سجل لمجموعة المنتجات.
- تُستخدم **أصول المنتجات** كمنتجات عامه تحتفظ بالتعريف والقواعد التي تحدد السلوك في العمليات التجارية. استنادًا إلى هذه التعريفات، يمكن إنشاء المنتجات المميزة المعروفة على أنها متغيرات المنتجات. على سبيل المثال، يعد القميص هو أصل المنتج، واللون والحجم هما أبعاده. يمكن إصدار متغيرات المنتجات التي لديها مجموعات مختلفة من هذه الأبعاد، مثل قميص أزرق صغير الحجم أو قميص أخضر متوسط الحجم. في عملية التكامل، يتم إنشاء سجل واحد لكل متغير في جدول المنتجات. يحتوي هذا السجل على المعلومات الخاصة بالمتغير، مثل الأبعاد المختلفة. يتم تخزين المعلومات العامة الخاصة بالمنتج في الكيان **msdyn\_sharedproductdetails**. ‏‫(يتم الاحتفاظ بهذه المعلومات العامة في أصل المنتج.) تتم مزامنة معلومات أصل للمنتج مع Common Data Service عند إنشاء أصل المنتج الصادر (ولكن قبل إصدار المتغيرات).
- تشير **المنتجات المميزة** إلى كافة منتجات النوع الفرعي للمنتجات وكافة متغيرات المنتجات. 

![نموذج بيانات للمنتجات](media/dual-write-product.png)

مع تمكين وظيفة الكتابة المزدوجة، ستتم مزامنة المنتجات من Finance and Operations مع منتجات Dynamics 365 الأخرى في حالة **المسودة**. وتُضاف إلى قائمة الأسعار الأولى بالعملة نفسها. بمعنى آخر، تُضاف إلى أول قائمة أسعار في تطبيق Dynamics 365 التي تتطابق مع عملة الكيان القانوني حيث يتم إصدار المنتج في تطبيق Finance and Operations. 

وتتم مزامنة المنتجات الافتراضية من تطبيقات Finance and Operations مع تطبيقات Dynamics 365 الأخرى في حالة **المسودة**. لمزامنة المنتج مع الحالة **النشطة**، بحيث يمكنك استخدامه مباشرة في عروض أسعار أوامر المبيعات، على سبيل المثال، يجب اختيار الإعداد التالي: علامة التبويب **النظام > الإدارة > إدارة النظام> إعدادات النظام > Sales‎** حدد **إنشاء منتجات في الحالة النشطة = نعم**. 

لاحظ أن مزامنة المنتجات تحدث من تطبيقات Finance and Operations إلى Common Data Service. وهذا يعني انه يمكن تغيير قيم حقول كيان المنتج في Common Data Service، ولكن عند تشغيل المزامنة (عند تعديل حقل منتج في تطبيق Finance and Operations)، سيؤدي ذلك إلى الكتابة فوق القيم الواردة في Common Data Service. 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [products](includes/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](includes/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](includes/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>أبعاد المنتجات 

أبعاد المنتج هي الخصائص التي تحدد متغير المنتج. يتم أيضًا تعيين أبعاد المنتج الأربعة (اللون والحجم والنمط والتكوين) إلى Common Data Service لتعريف متغيرات المنتج. يبين الرسم التوضيحي التالي نموذج البيانات لبعد المنتج "اللون". يتم تطبيق نفس النموذج على الأحجام والأنماط والتكوينات. 

![نموذج بيانات للمنتجات](media/dual-write-product-two.png)

[!include [product colors](includes/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](includes/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](includes/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](includes/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

عندما يتضمن المنتج أبعاد منتج مختلفة (على سبيل المثال، يتضمن أصل المنتج الحجم واللون كأبعاد المنتج)، يتم تعريف كل منتج مميز (أي كل متغير منتج) كمجموعة من أبعاد المنتج هذه. على سبيل المثال، رقم المنتج B0001 هو قميص أسود صغير جدًا، ورقم المنتج B0002 هو قميص أسود صغير. وفي هذه الحالة، يتم تعرف مجموعات أبعاد المنتجات الموجودة. على سبيل المثال، بإمكان القميص المذكور في المثال السابق أن يكون أسود اللون وبحجم صغير جدًا أو أسود اللون وبحجم صغير أو أسود اللون وبحجم متوسط أو أسود اللون وبحجم كبير، ولكن لا يمكنه أن يكون أسود اللون وبحجم كبيرا جدًا. بمعنى آخر، يتم تحديد أبعاد المنتج التي يمكن ان يتخذها أصل المنتج، ويمكن إصدار المتغيرات استنادًا إلى هذه القيم.

لتعقب أبعاد المنتج التي يمكن ان يتخذها أصل المنتج، يتم إنشاء الكيانات التالية وتعيينها في Common Data Service لكل بعد منتج. لمزيد من المعلومات، راجع [نظرة عامة على معلومات المنتجات‬](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

[!include [product colors](includes/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](includes/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](includes/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](includes/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](includes/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>إعدادات الأوامر الافتراضية وإعدادات الأوامر الافتراضية الخاصة بالمنتج

تحدد إعدادات الأوامر الافتراضية الموقع والمستودع من حيث تؤخذ الأصناف أو حيث يتم تخزينها، والحد الأدنى من الكميات وحدها الأقصى ومضاعفاتها والكميات القياسية التي سيتم استخدامها للتجارة أو إدارة المخزون وزمن وصول البضاعة وعلامة الإيقاف وأسلوب التعهد بالأمر‬. تتوفر هذه المعلومات في Common Data Service باستخدام كيان إعدادات الأوامر الافتراضية وإعدادات الأوامر الافتراضية الخاصة بالمنتج‬. يمكنك قراءة مزيد من المعلومات حول الوظائف في [موضوع إعدادات الأوامر الافتراضية](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

[!include [product sizes](includes/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](includes/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>وحدة القياس وتحويلات وحدة القياس

تتوفر وحدات القياس والتحويلات الخاصة بها في Common Data Service باتباع لنموذج البيانات المعروض في الرسم التخطيطي.

![نموذج بيانات للمنتجات](media/dual-write-product-three.png)

تم دمج مفهوم وحدة القياس بين تطبيقات Finance and Operations وتطبيقات Dynamics 365 الأخرى. لكل فئة وحدة في تطبيق Finance and Operations يتم إنشاء مجموعة وحدات في تطبيق Dynamics 365، تحتوي على الوحدات التي تنتمي إلى فئة الوحدة. كما يتم إنشاء وحدة أساسية افتراضية لكل مجموعة وحدات. 

[!include [unit of measure](includes/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](includes/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product-specific unit of measure conversions](includes/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-common-data-service"></a>المزامنة الأولية لمطابقة بيانات الوحدات بين Finance and Operations وCommon Data Service

### <a name="initial-synchronization-of-units"></a>المزامنة الأولية للوحدات

عند تمكين الكتابة الثنائية، تتم مزامنة المنتجات من Finance and Operations إلى تطبيقات Dynamics 365 الأخرى. مجموعات الوحدات التي تتم مزامنتها من تطبيقات Finance and Operations في Common Data Service تشتمل على مجموعة علامات تشير إلى أنها "محفوظة خارجيًا".

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>مطابقه بيانات الوحدات وفئات الوحدات/المجموعات من Finance and Operations وتطبيقات Dynamics 365 الأخرى

أولا، من المهم ملاحظه ان مفتاح التكامل الخاص بالوحدة هو msdyn_symbol. وبالتالي ، يجب ان تكون هذه القيمة فريدة في Common Data Service أو تطبيقات Dynamics 365 الأخرى. ونظرا لوجودها في تطبيقات Dynamics 365 الأخرى ، فانها تمثل الزوج "معرف مجموعه الوحدات" و "الاسم" الذي يحدد تفرد الوحدة ، ويجب مراعاه سيناريوهات مختلفة لمطابقه بيانات الوحدة بين تطبيقات Finance and Operations وCommon Data Service.

بالنسبة للوحدات المتطابقة/المتراكبه في تطبيقات Finance and Operations وتطبيقات Dynamics 365 الأخرى:

+ **تنتمي الوحدة إلى مجموعه وحدات في تطبيقات Dynamics 365 الأخرى التي تتوافق مع فئة الوحدة المرتبطة في تطبيقات Finance and Operations**. في هذه الحالة، يجب ملء الحقل msdyn_symbol في تطبيقات Dynamics 365 الأخرى برمز الوحدة من تطبيقات Finance and Operations. وبالتالي ، عند مطابقة البيانات، سيتم تعيين مجموعه الوحدات على أنها "محفوظه خارجيًا" في تطبيقات Dynamics 365 الأخرى.
+ **تنتمي الوحدة إلى مجموعه وحدات في تطبيقات Dynamics 365 الأخرى التي لا تتوافق مع فئة الوحدة المقترنة في تطبيقات Finance and Operations (لا توجد فئة وحده موجودة في تطبيقات Finance and Operations الخاصة بفئة الوحدة في تطبيقات Dynamics 365 apps الأخرى).** في هذه الحالة ، يجب ان يتم ملء msdyn_symbol بسلسلة عشوائية. لاحظ أنه يجب ان تكون هذه القيمة فريدة في تطبيقات Dynamics 365 الأخرى.

بالنسبة للوحدات وفئات الوحدات في تطبيقات Finance and Operations غير الموجودة في تطبيقات Dynamics 365 الأخرى:

كجزء من الكتابة المزدوجة، يتم إنشاء ومزامنة مجموعات الوحدات من تطبيقات Finance and Operations ووحداتها المقابلة في تطبيقات Dynamics 365 الأخرى وCommon Data Service وسيتم تعيين مجموعه الوحدات على أنها "محفوظة خارجيًا". لا يلزم وجود أي جهد تمهيد إضافي.

بالنسبة للوحدات في تطبيقات Dynamics 365 الأخرى وغير الموجودة في تطبيقات Finance and Operations:

يجب ملء الحقل msdyn_symbol لكافة الوحدات. ويمكن دائما إنشاء الوحدات في تطبيقات Finance and Operations في فئة الوحدات المقابلة (إذا كانت موجودة). في حاله عدم وجود فئة الوحدة ، يجب أولا إنشاء فئة الوحدة (لاحظ انه لا يمكن إنشاء فئة وحده في تطبيقات Finance and Operations باستثناء الملحق إذا كنت تقوم بتوسيع التعداد) مع مطابقه مجموعه وحدات تطبيقات Dynamics 365 الأخرى. ويمكنك بعد ذلك إنشاء الوحدة. لاحظ أن رمز الوحدة في تطبيقات Finance and Operations يجب أن يكون msdyn_symbol المحدد مسبقًا في تطبيقات Dynamics 365 الأخرى للوحدة.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>سياسات المنتج: مجموعات الأبعاد والتعقب والتخزين

سياسات المنتج هي عبارة عن مجموعات من السياسات المستخدمة لتعريف المنتجات وخصائصها في المخزون. يمكن العثور على مجموعة أبعاد المنتج ومجموعة أبعاد تعقب المنتج ومجموعة أبعاد المنتج كسياسات المنتج. 

[!include [product dimension group](includes/EcoResProductDimensionGroup-msdyn-productdimensiongroups.md)]

[!include [product tracking dimension group](includes/EcoResTrackingDimensionGroup-msdyn-producttrackingdimensiongroups.md)]

[!include [product storage dimension group](includes/EcoResStorageDimensionGroup-msdyn-productstoragedimensiongroups.md)]

## <a name="product-hierarchies"></a>التدرجات الهرمية للمنتجات

[!include [product category hierarchy](includes/EcoResProductCategoryHierarchyEntity-msdyn-productcategoryhierarchy.md)]

[!include [product category](includes/EcoResProductCategoryEntity-msdyn-productcategory.md)]

[!include [product category assignments](includes/EcoResProductCategoryAssignmentEntity-msdyn-productcategoryassignment.md)]

[!include [product category role](includes/EcoResProductCategoryHierarchyRoleEntity-msdyn-productcategoryhierarchyrole.md)]


## <a name="integration-key-for-products"></a>مفتاح تكامل المنتجات 

لتحديد منتجات الهوية الفريدة بين  Dynamics 365 for Finance and Operations والمنتجات في Common Data Service يتم استخدام مفاتيح التكامل. بالنسبة للمنتجات، يكون **(productnumber)** هو المفتاح الفريد الذي يحدد منتجًا في Common Data Service. ويتم تكوينه بواسطة سلسلة: **(company, msdyn_productnumber)**. تشير **الشركة** إلى الكيان القانوني في Finance and Operations و**msdyn_productnumber** إلى رقم المنتج الخاص بالمنتج المحدد في Finance and Operations. 

بالنسبة لمستخدمي تطبيقات Dynamics 365 آخر، يتم تعريف المنتج في واجهة المستخدم بواسطة **msdyn_productnumber** (لاحظ ان تسميه الحقل هي **رقم المنتج**). في نموذج المنتج، يتم عرض كل من الشركة وmsydn_productnumber. ومع ذلك، لا يتم عرض الحقل (productnumber) والمفتاح الفريد لأحد المنتجات. 

إذا قمت بإنشاء تطبيقات على Common Data Service يجب عليك الانتباه إلى استخدام **productnumber‎** (معرف المنتج الفريد) كمفتاح تكامل. لا تستخدم **msdyn_productnumber**، لأنه ليس فريدا. 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-common-data-service-to-finance-and-operations"></a>المزامنة الأولية للمنتجات وترحيل البيانات من Common Data Service إلى Finance and Operations

### <a name="initial-synchronization-of-products"></a>المزامنة الأولية للمنتجات 

عند تمكين الكتابة الثنائية، تتم مزامنة المنتجات من Finance and Operations إلى Common Data Service والتطبيقات المستندة إلى الطراز الأخرى في Dynamics 365. المنتجات التي تم إنشاؤها في Common Data Service وتطبيقات Dynamics 365 الأخرى قبل الكتابة الثنائية، لن يتم تحديثها أو مطابقتها مع بيانات المنتج من تطبيقات Finance and Operations.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>مطابقه بيانات المنتج من Finance and Operations وتطبيقات Dynamics 365 الأخرى

في حاله الاحتفاظ بنفس المنتجات (تراكب/مطابقه) في Finance and Operations وفي Common Data Service وتطبيقات Dynamics 365 الأخرى، عند تمكين الكتابة المزدوجة ستحدث مزامنة المنتجات من Finance and Operations، وستظهر السجلات المكررة في Common Data Service لنفس المنتج.
لتجنب الموقف السابق، إذا كانت تطبيقات Dynamics 365 الأخرى لديها منتجات متداخلة/متطابقة مع Finance and Operations، فان المسؤول الذي يقوم بتمكين الكتابة الثنائية يجب ان يقوم بتمهيد الحقول **الشركة** (مثال: "USMF") and **msdyn_productnumber** (مثال: "1234:Black:S") قبل مزامنة المنتجات. بمعني آخر، يجب ان يتم ملء هذين الحقلين الموجودين في المنتج في Common Data Service بالشركة المعنية في Finance and Operations التي يحتاج اليها المنتج لتتم مطابقته مع ورقم المنتج الخاص به. 

ثم عند تمكين المزامنة وحدوثها، ستتم مزامنة المنتجات من Finance and Operations مع المنتجات المتطابقة في Common Data Service وتطبيقات Dynamics 365 الأخرى. ويكون هذا قابلا للتطبيق على كل من المنتجات المختلفة ومتغيرات المنتجتن. 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>ترحيل بيانات المنتج من تطبيقات Dynamics 365 الأخرى إلى Finance and Operations

إذا كانت تطبيقات Dynamics 365 الأخرى تحتوي على منتجات غير موجودة في Finance and Operations، يمكن للمسؤول أولاً استخدام **EcoResReleasedProductCreationV2Entity** لاستيراد تلك المنتجات في Finance and Operations. وثانيًا، قم بمطابقه بيانات المنتج من Finance and Operations وتطبيقات Dynamics 365 الأخرى كما هو موضح أعلاه. 
