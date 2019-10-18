---
title: تجربة المنتجات الموحدة
description: يصف هذا الموضوع تكامل بيانات المنتجات بين تطبيقات Finance and Operations وCommon Data Service.
author: t-benebo
manager: AnnBe
ms.date: 09/3/2019
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
ms.openlocfilehash: 9dc26e0e50c0b77555d09e4a50b846c80b1d5760
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249318"
---
# <a name="unified-product-experience"></a>تجربة المنتجات الموحدة

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

عندما يتكون النظام البيئي للشركة من تطبيقات Dynamics 365، مثل Finance وSupply Chain Management وSales، من الطبيعي أن يستخدم العملاء هذه التطبيقات لتوريد بيانات المنتجات. ويعود السبب في ذلك إلى أن هذه التطبيقات توفر بنية تحتية قوية للمنتجات تكملها مفاهيم تسعير معقدة وبيانات دقيقة تتعلق بالمخزون المتوفر. بإمكان العملاء الذين يستخدمون نظامًا خارجيًا لإدارة دورة حياة المنتج (PLM) لتوريد بيانات المنتجات توجيه المنتجات من تطبيقات Finance and Operations إلى تطبيقات Dynamics 365 أخرى. تقوم تجربة المنتجات الموحدة بإحضار نموذج بيانات المنتجات المتكاملة إلى Common Data Service، لتمكين جميع مستخدمي التطبيقات، بمن فيهم مستخدمو Power Platform من الاستفادة من بيانات المنتجات القادمة من تطبيقات Finance and Operations.

فيما يلي نموذج بيانات المنتجات من Sales.

![نموذج بيانات للمنتجات في Sales](media/dual-write-product-4.jpg)

فيما يلي نموذج بيانات المنتجات من تطبيقات Finance and Operations.

![نموذج بيانات للمنتجات في Finance and Operations](media/dual-write-products-5.jpg)

تم دمج نموذجي بيانات المنتجات في Common Data Service كما هو موضح أدناه.

![نموذج بيانات للمنتجات في تطبيقات Dynamics 365](media/dual-write-products-6.jpg)

تم تصميم تخطيطات كيان الكتابة المزدوجة لتمكين تدفق البيانات باتجاه واحد، وهي عبارة عن تجربة قريبة من الوقت الحقيقي من تطبيقات Finance and Operations إلى Common Data Service. ومع ذلك، فقد تم فتح البنية الأساسية للمنتجات لجعلها ثنائية الاتجاه إذا لزم الأمر. بإمكان العملاء تخصيصها، على مسؤوليتهم الخاصة، لأن Microsoft لا تنصح باتباع هذا الأسلوب.

## <a name="templates"></a>القوالب

تحتوي معلومات المنتج على كافة المعلومات المرتبطة بالمنتج وتعريفه، مثل أبعاد المنتج أو أبعاد التعقب والتخزين. كما يوضح الجدول التالي، يتم إنشاء مجموعة من مخططات الكيانات لمزامنة المنتجات والمعلومات المتعلقة بها.

Finance and Operations | تطبيقات Dynamics 365 الأخرى
-----------------------|--------------------------------
المنتجات الصادرة V2 | msdyn\_sharedproductdetails
المنتجات المميزة الصادرة‬ CDS | منتج
الكود الشريطي المحدد لرقم المنتج | msdyn\_productbarcodes
إعدادات الأوامر الافتراضية | msdyn\_productdefaultordersettings
إعدادات الأوامر الافتراضية الخاصة بالمنتج | msdyn_productspecificdefaultordersettings
مجموعات أبعاد المنتجات | msdyn\_productdimensiongroups
مجموعات أبعاد التخزين | msdyn\_productstoragedimensiongroups
مجموعات أبعاد التعقب | msdyn\_producttrackingdimensiongroups
الألوان | msdyn\_productcolors
الأحجام | msdyn\_productsizes
الأنماط | msdyn\_productsytles
التكوينات | msdyn\_productconfigurations
ألوان أصل المنتج | msdyn_sharedproductcolors
أحجام أصل المنتج | msdyn_sharedproductsizes
أنماط أصل المنتج | msdyn_sharedproductstyles
تكوينات أصل المنتج | msdyn_sharedproductconfigurations
كافة المنتجات | msdyn_globalproducts
الوحدة | uoms
تحويلات الوحدات | msdyn_ unitofmeasureconversions
تحويل وحدة قياس خاصة بالمنتج | msdyn_productspecificunitofmeasureconversion
المواقع | msdyn\_operationalsites
المستودعات | msdyn\_inventwarehouses

[!include [symbols](../includes/dual-write-symbols.md)]

## <a name="integration-of-products"></a>تكامل المنتجات

في هذا النموذج، يتم تمثيل المنتج بواسطة مجموعة مكونة من كيانين في Common Data Service: **المنتج** و**msdyn\_sharedproductdetails**. بينما يحتوي الكيان الأول على تعريف منتج (المعرف الفريد للمنتج واسم المنتج والوصف)، يحتوي الكيان الثاني على الحقول المخزنة على مستوي المنتج. يتم استخدام مجموعة هذين الكيانين لتحديد المنتج وفقًا لمفهوم وحدة حفظ المخزون (SKU). سيكون لكل منتج تم إصداره معلومات خاصة به في الكيانات المذكورة (تفاصيل المنتج والمنتج المشترك). لتعقب جميع المنتجات (الصادرة وغير الصادرة)، يتم استخدام كيان **المنتجات العامة**. 

وبسبب تمثيل المنتج على أنه وحدة SKU، يمكن تسجيل مفاهيم المنتجات المميزة وأصول المنتجات ومتغيرات المنتجات في Common Data Service بالطريقة التالية:

- **منتجات مع نوع فرعي للمنتج** هي منتجات يتم تعريفها بنفسها. لا يجب تعريف أي أبعاد لها. على سبيل المثال، دفتر خاص. بالنسبة إلى هذه المنتجات، يتم إنشاء‏‎ سجل في كيان **المنتج**، ويتم إنشاء سجل في كيان **msdyn\_sharedproductdetails**. لا يتم إنشاء سجل لمجموعة المنتجات.
- تُستخدم **أصول المنتجات** كمنتجات عامه تحتفظ بالتعريف والقواعد التي تحدد السلوك في العمليات التجارية. استنادًا إلى هذه التعريفات، يمكن إنشاء المنتجات المميزة المعروفة على أنها متغيرات المنتجات. على سبيل المثال، يعد القميص هو أصل المنتج، واللون والحجم هما أبعاده. يمكن إصدار متغيرات المنتجات التي لديها مجموعات مختلفة من هذه الأبعاد، مثل قميص أزرق صغير الحجم أو قميص أخضر متوسط الحجم. في عملية التكامل، يتم إنشاء سجل واحد لكل متغير في جدول المنتجات. يحتوي هذا السجل على المعلومات الخاصة بالمتغير، مثل الأبعاد المختلفة. يتم تخزين المعلومات العامة الخاصة بالمنتج في الكيان **msdyn\_sharedproductdetails**. (يتم الاحتفاظ بهذه المعلومات العامة في أصل المنتج.) علاوةً على ذلك، يتم إنشاء سجل مجموعة منتجات واحد لكل أصل منتج. تتم مزامنة معلومات أصل للمنتج مع Common Data Service عند إنشاء أصل المنتج الصادر (ولكن قبل إصدار المتغيرات).
- تشير **المنتجات المميزة** إلى كافة منتجات النوع الفرعي للمنتجات وكافة متغيرات المنتجات. 

![نموذج بيانات للمنتجات](media/dual-write-product.png)

مع تمكين وظيفة الكتابة المزدوجة، ستتم مزامنة التطبيقات من Finance and Operations مع تطبيقات Dynamics 365 أخرى في حالة **المسودة**. وتُضاف إلى قائمة الأسعار الأولى بالعملة نفسها. بمعنى آخر، تُضاف إلى أول قائمة أسعار في تطبيق Dynamics 365 التي تتطابق مع عملة الكيان القانوني حيث يتم إصدار المنتج في تطبيق Finance and Operations. 

لمزامنة المنتج مع الحالة **النشطة**، بحيث يمكنك استخدامه مباشرة في عروض أسعار أوامر المبيعات، على سبيل المثال، يجب اختيار الإعداد التالي: ضمن **النظام > الإدارة > إدارة النظام> إعدادات النظام > Sales‎** حدد **إنشاء منتجات في الحالة النشطة = نعم**. 

### <a name="cds-released-distinct-products-to-product"></a>المنتجات المميزة الصادرة من CDS إلى المنتج

يحتوي كيان‏‎ **المنتج** على الحقول التي تعرّف المنتج. ويتضمن منتجات فردية (منتجات مع نوع فرعي للمنتج) ومتغيرات المنتج. يعرض الجدول التالي التعيينات.

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
PRODUCTNUMBER | >> | productnumber
PRODUCTNAME | >> | name
PRODUCTDESCRIPTION | >> | الوصف
ITEMNUMBER | >> | msdyn_itemnumber
CURRENCYCODE | >> | transactioncurrencyid.isocurrencycode
SALESUNITSYMBOL | >> | defaultuomid.msdyn_symbol
SALESPRICE | >> | سعر
UNITCOST | >> | currentcost
PRODUCTTYPE | >> | producttypecode
SALESUNITDECIMALPRECISION | >> | quantitydecimal
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTCOLORID | >> | msdyn_productcolor.msdyn_productcolorname
PRODUCTCONFIGURATIONID | >> | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | >> | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | >> | msdyn_productstyle.msdyn_productstyle

### <a name="released-products-v2-to-msdyn_sharedproductdetails"></a>المنتجات الصادرة من V2 إلى msdyn\_sharedproductdetails

يحتوي الكيان **msdyn\_sharedproductdetails** على حقول من تطبيقات Finance and Operations التي تحدد المنتج، والتي تحتوي على معلومات مالية وإدارية خاصة بالمنتج. يعرض الجدول التالي التعيينات.

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
PRODUCTNUMBER | > | msdyn_globalproduct.msdyn_productnumber
INTRASTATCHARGEPERCENTAGE | > | msdyn_intrastatchargepercentage
ITEMNUMBER | >> | msdyn_itemnumber
APPROXIMATESALESTAXPERCENTAGE | > | msdyn_approximatesalestaxpercentage
BESTBEFOREPERIODDAYS | > | msdyn_bestbeforeperioddays
CARRYINGCOSTABCCODE | >> | msdyn_carryingcostabccode
CONSTANTSCRAPQUANTITY | > | msdyn_constantscrapquantity
COSTCHARGESQUANTITY | > | msdyn_costchargesquantity
DEFAULTRECEIVINGQUANTITY | > | msdyn_defaultreceivingquantity
FIXEDPURCHASEPRICECHARGES | > | msdyn_fixedpurchasepricecharges
FIXEDSALESPRICECHARGES | > | msdyn_fixedsalespricecharges
GROSSDEPTH | > | msdyn_grossdepth
GROSSPRODUCTHEIGHT | > | msdyn_grossproductheight
GROSSPRODUCTWIDTH | > | msdyn_grossproductwidth
INVENTORYUNITSYMBOL | > | msdyn_inventoryunitsymbol.msdyn_symbol
ISDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_isdiscountposregistrationprohibited
ISEXEMPTFROMAUTOMATICNOTIFICATIONANDCANCELLATION | >> | msdyn_exemptautomaticnotificationcancel
ISINSTALLMENTELIGIBLE | >> | msdyn_isinstallmenteligible
ISINTERCOMPANYPURCHASEUSAGEBLOCKED | >> | msdyn_isintercompanypurchaseusageblocked
ISINTERCOMPANYSALESUSAGEBLOCKED | >> | msdyn_isintercompanysalesusageblocked
ISMANUALDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_ismanualdiscposregistrationprohibited
ISPHANTOM | >> | msdyn_isphantom
ISPOSREGISTRATIONBLOCKED | >> | msdyn_isposregistrationblocked
ISPOSREGISTRATIONQUANTITYNEGATIVE | >> | msdyn_isposregistrationquantitynegative
ISPURCHASEPRICEAUTOMATICALLYUPDATED | >> | msdyn_ispurchasepriceautomaticallyupdated
ISPURCHASEPRICEINCLUDINGCHARGES | >> | msdyn_ispurchasepriceincludingcharges
ISSALESWITHHOLDINGTAXCALCULATED | >> | msdyn_issaleswithholdingtaxcalculated
ISRESTRICTEDFORCOUPONS | >> | msdyn_isrestrictedforcoupons
ISSALESPRICEADJUSTMENTALLOWED | >> | msdyn_issalespriceadjustmentallowed
ISSALESPRICEINCLUDINGCHARGES | >> | msdyn_issalespriceincludingcharges
ISSCALEPRODUCT | >> | msdyn_isscaleproduct
ISSHIPALONEENABLED | >> | msdyn_isshipaloneenabled
ISUNITCOSTPRODUCTVARIANTSPECIFIC | >> | msdyn_isunitcostproductvariantspecific
ISVARIANTSHELFLABELSPRINTINGENABLED | >> | msdyn_isvariantshelflabelsprintingenabled
ISZEROPRICEPOSREGISTRATIONALLOWED | >> | msdyn_iszeropriceposregistrationallowed
KEYINPRICEREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinpricerequirementsatposregister
KEYINQUANTITYREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinquantityrequirementsatposregister
MARGINABCCODE | >> | msdyn_marginabccode
MAXIMUMPICKQUANTITY | > | msdyn_maximumpickquantity
MUSTKEYINCOMMENTATPOSREGISTER | >> | msdyn_mustkeyincommentatposregister
NECESSARYPRODUCTIONWORKINGTIMESCHEDULINGPROPERTYID | > | msdyn_necessaryproductionworkingtimeschedulingp
NETPRODUCTWEIGHT | > | msdyn_netproductweight
PACKINGDUTYQUANTITY | > | msdyn_packingdutyquantity
POSREGISTRATIONACTIVATIONDATE | > | msdyn_posregistrationactivationdate
POSREGISTRATIONBLOCKEDDATE | > | msdyn_posregistrationblockeddate
POSREGISTRATIONPLANNEDBLOCKEDDATE | > | msdyn_posregistrationplannedblockeddate
POTENCYBASEATTIBUTETARGETVALUE | > | msdyn_potencybaseattibutetargetvalue
POTENCYBASEATTRIBUTEVALUEENTRYEVENT | >> | msdyn_potencybaseattributevalueentryevent
PRODUCTTYPE | >> | msdyn_producttype
PRODUCTIONCONSUMPTIONDENSITYCONVERSIONFACTOR | > | msdyn_productionconsumptiondensityconversion
PRODUCTIONCONSUMPTIONDEPTHCONVERSIONFACTOR | > | msdyn_productionconsumptiondepthconversion
PRODUCTIONCONSUMPTIONHEIGHTCONVERSIONFACTOR | > | msdyn_productionconsumptionheightconversion
PRODUCTIONCONSUMPTIONWIDTHCONVERSIONFACTOR | > | msdyn_productionconsumptionwidthconversion
PRODUCTVOLUME | > | msdyn_productvolume
PURCHASECHARGESQUANTITY | > | msdyn_purchasechargesquantity
PURCHASEOVERDELIVERYPERCENTAGE | > | msdyn_purchaseoverdeliverypercentage
PURCHASEPRICE | > | msdyn_purchaseprice
PURCHASEPRICEDATE | > | msdyn_purchasepricedate
PURCHASEPRICINGPRECISION | > | msdyn_purchasepricingprecision
PURCHASEUNDERDELIVERYPERCENTAGE | > | msdyn_purchaseunderdeliverypercentage
RAWMATERIALPICKINGPRINCIPLE | >> | msdyn_rawmaterialpickingprinciple
SALESCHARGESQUANTITY | > | msdyn_saleschargesquantity
SALESOVERDELIVERYPERCENTAGE | > | msdyn_salesoverdeliverypercentage
SALESPRICE | > | msdyn_salesprice
SALESPRICECALCULATIONCHARGESPERCENTAGE | > | msdyn_salespricecalculationchargespercentage
SALESPRICECALCULATIONCONTRIBUTIONRATIO | > | msdyn_salespricecalculationcontributionratio
SALESPRICECALCULATIONMODEL | >> | msdyn_salespricecalculationmodel
SALESPRICEDATE | > | msdyn_salespricedate
SALESPRICINGPRECISION | > | msdyn_salespricingprecision
SALESUNDERDELIVERYPERCENTAGE | > | msdyn_salesunderdeliverypercentage
SALESUNITSYMBOL | > | msdyn_salesunitsymbol.msdyn_symbol
SCALEINDICATOR | >> | msdyn_scaleindicator
SELLSTARTDATE | > | msdyn_sellstartdate
SHELFADVICEPERIODDAYS | > | msdyn_shelfadviceperioddays
SHELFLIFEPERIODDAYS | > | msdyn_shelflifeperioddays
SHIPSTARTDATE | > | msdyn_shipstartdate
TAREPRODUCTWEIGHT | > | msdyn_tareproductweight
TRANSFERORDEROVERDELIVERYPERCENTAGE | > | msdyn_transferorderoverdeliverypercentage
TRANSFERORDERUNDERDELIVERYPERCENTAGE | > | msdyn_transferorderunderdeliverypercentage
UNITCOST | > | msdyn_unitcost
UNITCOSTDATE | > | msdyn_unitcostdate
UNITCOSTQUANTITY | > | msdyn_unitcostquantity
VARIABLESCRAPPERCENTAGE | > | msdyn_variablescrappercentage
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE1 | > | msdyn_warehousemobiledevicedescriptionline1
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE2 | > | msdyn_warehousemobiledevicedescriptionline2
WILLINVENTORYISSUEAUTOMATICALLYREPORTASFINISHED | >> | msdyn_willinventoryissueautoreportasfinished
WILLINVENTORYRECEIPTIGNOREFLUSHINGPRINCIPLE | >> | msdyn_willinventoryreceiptignoreflushing
WILLPICKINGWORKBENCHAPPLYBOXINGLOGIC | >> | msdyn_willpickingworkbenchapplyboxinglogic
WILLTOTALPURCHASEDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalpurchdiscountcalcincludeproduct
WILLTOTALSALESDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalsalesdiscountcalcincludeproduct
WILLWORKCENTERPICKINGALLOWNEGATIVEINVENTORY | >> | msdyn_willworkcenterpickingallownegativeinvent
YIELDPERCENTAGE | > | msdyn_yieldpercentage
ISUNITCOSTAUTOMATICALLYUPDATED | >> | msdyn_isunitcostautomaticallyupdated
PURCHASEUNITSYMBOL | > | msdyn_purchaseunitsymbol.msdyn_symbol
PURCHASEPRICEQUANTITY | > | msdyn_purchasepricequantity
ISUNITCOSTINCLUDINGCHARGES | >> | msdyn_isunitcostincludingcharges
FIXEDCOSTCHARGES | >> | msdyn_fixedcostcharges
MINIMUMCATCHWEIGHTQUANTITY | >> | msdyn_minimumcatchweightquantity
MAXIMUMCATCHWEIGHTQUANTITY | >> | msdyn_maximumcatchweightquantity
ALTERNATIVEITEMNUMBER | >> | msdyn_alternativeitemnumber.msdyn_itemnumber
BOMUNITSYMBOL | >> | msdyn_bomunitsymbol.msdyn_symbol
CATCHWEIGHTUNITSYMBOL | >> | msdyn_catchweightunitsymbol.msdyn_symbol
COMPARISONPRICEBASEUNITSYMBOL | >> | msdyn_comparisonpricebaseunitsymbol.msdyn_symbol
PRIMARYVENDORACCOUNTNUMBER | >> | msdyn_vendorid.msdyn_vendoraccountnumber
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTDIMENSIONGROUPNAME | >> | msdyn_productdimensiongroupid.msdyn_groupname

## <a name="all-product-to-msdyn_global-products"></a>جميع المنتجات إلى منتجات msdyn_global

يحتوي كيان جميع المنتجات على جميع المنتجات المتوفرة في تطبيقات Finance and Operations، المنتجات الصادرة والمنتجات غير الصادرة على حدٍ سواء. تتوفر هذه المنتجات في Common Data Service باستخدام التعيينات التالية:

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
PRODUCTNAME | >> | msdyn_productname
PRODUCTNUMBER | >> | msdyn_productnumber

## <a name="product-dimensions"></a>أبعاد المنتجات 

أبعاد المنتج هي الخصائص التي تحدد متغير المنتج. يتم أيضًا تعيين أبعاد المنتج الأربعة (اللون والحجم والنمط والتكوين) إلى Common Data Service لتعريف متغيرات المنتج. يبين الرسم التوضيحي التالي نموذج البيانات لبعد المنتج "اللون". يتم تطبيق نفس النموذج على الأحجام والأنماط والتكوينات. 

![نموذج بيانات للمنتجات](media/dual-write-product-2.PNG)

### <a name="colors"></a>الألوان

تتوفر الألوان المحتملة في Common Data Service من خلال التعيينات التالية.

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
COLORID | \>\> | msdyn\_productcolorname

### <a name="sizes"></a>الأحجام

تتوفر الأحجام المحتملة في Common Data Service من خلال التعيينات التالية.

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
SIZEID | \>\> | msdyn\_productsize

### <a name="styles"></a>الأنماط

تتوفر الأنماط المحتملة في Common Data Service من خلال التعيينات التالية.

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
STYLEID | \>\> | msdyn\_productstyle

### <a name="configurations"></a>التكوينات

تتوفر التكوينات المحتملة في Common Data Service من خلال التعيينات التالية.

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
CONFIGURATIONID | \>\> | msdyn\_name

عندما يتضمن المنتج أبعاد منتج مختلفة (على سبيل المثال، يتضمن أصل المنتج الحجم واللون كأبعاد المنتج)، يتم تعريف كل منتج مميز (أي كل متغير منتج) كمجموعة من أبعاد المنتج هذه. علي سبيل المثال، رقم المنتج B0001 هو قميص أسود صغير جدًا، ورقم المنتج B0002 هو قميص أسود صغير. وفي هذه الحالة، يتم تعرف مجموعات أبعاد المنتجات الموجودة. على سبيل المثال، بإمكان القميص المذكور في المثال السابق أن يكون أسود اللون وبحجم صغير جدًا أو أسود اللون وبحجم صغير أو أسود اللون وبحجم متوسط أو أسود اللون وبحجم كبير، ولكن لا يمكنه أن يكون أسود اللون وبحجم كبيرا جدًا. بمعنى آخر، يتم تحديد أبعاد المنتج التي يمكن ان يتخذها أصل المنتج، ويمكن إصدار المتغيرات استنادًا إلى هذه القيم.

لتعقب أبعاد المنتج التي يمكن ان يتخذها أصل المنتج، يتم إنشاء الكيانات التالية وتعيينها في Common Data Service لكل بعد منتج. لمزيد من المعلومات، راجع [نظرة عامة على معلومات المنتجات‬](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

### <a name="shared-product-color"></a>لون المنتج المشترك

يشير الكيان **لون المنتج المشترك** إلى الألوان التي يمكن أن تكون متوفرة في أصل منتج معين. تم ترحيل هذا المفهوم إلى Common Data Service للحفاظ على تناسق البيانات. يعرض الجدول التالي التعيينات.

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
PRODUCTCOLORID | \>\> | msdyn\_productcolorid.msdyn\_productcolorname
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_retaildisplayorder

### <a name="shared-product-size"></a>حجم المنتج المشترك

يشير الكيان **حجم المنتج المشترك** إلى الأحجام التي يمكن أن تكون متوفرة في أصل منتج معين. تم ترحيل هذا المفهوم إلى Common Data Service للحفاظ على تناسق البيانات. يعرض الجدول التالي التعيينات.

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
PRODUCTSIZEID | \>\> | msdyn\_productsizeid.msdyn\_productsize
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-style"></a>نمط المنتج المشترك

يشير الكيان **نمط المنتج المشترك** إلى الأنماط التي يمكن أن تكون متوفرة في أصل منتج معين. تم ترحيل هذا المفهوم إلى Common Data Service للحفاظ على تناسق البيانات. يعرض الجدول التالي التعيينات.

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailsid.msdyn\_itemnumber
PRODUCTSTYLEID | \>\> | msdyn\_productstyleintegration
PRODUCTSTYLEID | \>\> | msdyn\_productstyleid.msdyn\_productstyle
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-configuration"></a>تكوين المنتج المشترك

يشير الكيان **تكوين المنتج المشترك** إلى التكوينات التي يمكن أن تكون متوفرة في أصل منتج معين. تم ترحيل هذا المفهوم إلى Common Data Service للحفاظ على تناسق البيانات. يعرض الجدول التالي التعيينات.

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
CONTAINERUNITSYMBOL | \>\> | msdyn\_containerunitsymbol
PRODUCTCONFIGURATIONID | \>\> | msdyn\_productconfigurationid.msdyn\_productconfiguration
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

## <a name="product-number-identifier-bar-codes"></a>الأكواد الشريطية لمعرف رقم المنتج

يتم استخدام الأكواد الشريطية للمنتجات لتحديد المنتجات بشكل فريد. يتم استخدام التعيينات التالية لجعل هذه الأكواد الشريطية للمنتجات متوفرة في Common Data Service:

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
PRODUCTNUMBER | \> | msdyn\_productnumberid.productnumber
BARCODE | \> | msdyn\_name
BARCODE | \> | msdyn\_barcode
PRODUCTQUANTITY | \> | msdyn\_productquantity
PRODUCTDESCRIPTION | \> | msdyn\_productdescription
BARCODESETUPID | \> | msdyn\_barcodesetupid
PRODUCTQUANTITYUNITSYMBOL | \> | msdyn\_unitofmeasureid.name
ISDEFAULTSCANNEDBARCODE | \>\> | msdyn\_isdefaultscannedbarcode
ISDEFAULTPRINTEDBARCODE | \>\> | msdyn\_isdefaultprintedbarcode
ISDEFAULTDISPLAYEDBARCODE | \>\> | msdyn\_isdefaultdisplayedbarcode

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>إعدادات الأوامر الافتراضية وإعدادات الأوامر الافتراضية الخاصة بالمنتج

تحدد إعدادات الأوامر الافتراضية الموقع والمستودع من حيث تؤخذ الأصناف أو حيث يتم تخزينها، والحد الأدنى من الكميات وحدها الأقصى ومضاعفاتها والكميات القياسية التي سيتم استخدامها للتجارة أو إدارة المخزون وزمن وصول البضاعة وعلامة الإيقاف وأسلوب التعهد بالأمر‬. ستتوفر هذه المعلومات في CDS باستخدام كيان إعدادات الأوامر الافتراضية وإعدادات الأوامر الافتراضية الخاصة بالمنتج‬. يمكنك قراءة مزيد من المعلومات حول الوظائف في [صفحة إعدادات الأوامر الافتراضية](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

### <a name="default-order-settings"></a>إعدادات الأوامر الافتراضية

يتم استخدام التعيينات التالية لجعل إعدادات الأوامر الافتراضية متوفرة في Common Data Service:

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
INVENTWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory

### <a name="product-specific-default-order-settings"></a>إعدادات الأوامر الافتراضية الخاصة بالمنتج

يتم استخدام التعيينات التالية لجعل إعدادات الأوامر الافتراضية الخاصة بالمنتج‬ متوفرة في Common Data Service:

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
INVENTORYWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory
OPERATIONALSITEID | = | msdyn_operationalsite.msdyn_siteid
PRODUCTCOLORID | = | msdyn_productcolor.msdyn_productcolorname
PRODUCTCONFIGURATIONID | = | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | = | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | = | msdyn_productstyle.msdyn_productstyle

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>وحدة القياس وتحويلات وحدة القياس

ستتوفر وحدات القياس والتحويلات الخاصة بها في Common Data Service باتباع لنموذج البيانات المعروض في الرسم التخطيطي.

![نموذج بيانات للمنتجات](media/dual-write-product-3.PNG)

تم دمج مفهوم وحدة القياس بين تطبيقات Finance and Operations وتطبيقات Dynamics 365 الأخرى. لكل فئة وحدة في تطبيق Finance and Operations يتم إنشاء مجموعة وحدات في تطبيق Dynamics 365، تحتوي على الوحدات التي تنتمي إلى فئة الوحدة. كما يتم إنشاء وحدة أساسية افتراضية لكل مجموعة وحدات. 

### <a name="unit-of-measure"></a>وحدة القياس

يتم استخدام التعيينات التالية لجعل وحدات القياس في تطبيقات Finance and Operations متوفرة في Common Data Service.

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
UNITSYMBOL | >> | msdyn_symbol
UNITCLASS | >> | msdyn_externalunitclassname
DECIMALPRECISION | >> | msdyn_decimalprecision
ISBASEUNIT | >> | msdyn_isbaseunit
ISSYSTEMUNIT | >> | msdyn_issystemunit
SYSTEMOFUNITS | >> | msdyn_systemofunits
UNITSYMBOL | >> | name
UNITDESCRIPTION | >> | msdyn_description

### <a name="unit-of-measure-conversions"></a>تحويلات وحدة القياس

يتم استخدام التعيينات التالية لجعل تحويلات وحدات القياس في تطبيقات Finance and Operations متوفرة في Common Data Service.

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
DENOMINATOR | = | msdyn_denominator
NUMERATOR | = | msdyn_numerator
FACTOR | = | msdyn_factor
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
ROUNDING | >< | msdyn_rounding
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symbol

### <a name="product-specific-unit-of-measure-conversions"></a>تحويلات وحدات قياس خاصة بالمنتج

يتم استخدام التعيينات التالية لجعل تحويلات وحدات القياس الخاصة بالمنتج في تطبيقات Finance and Operations متوفرة في Common Data Service.

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
DENOMINATOR | = | msdyn_denominator
NUMERATOR | = | msdyn_numerator
FACTOR | = | msdyn_factor
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symbol
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
ROUNDING | >< | msdyn_rounding

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>سياسات المنتج: مجموعات الأبعاد والتعقب والتخزين

سياسات المنتج هي عبارة عن مجموعات من السياسات المستخدمة لتعريف المنتجات وخصائصها في المخزون. يمكن العثور على مجموعة أبعاد المنتج ومجموعة أبعاد تعقب المنتج ومجموعة أبعاد المنتج كسياسات المنتج. 

### <a name="product-dimension-group"></a>مجموعة أبعاد المنتجات

تقوم مجموعة أبعاد المنتج بتعريف أبعاد المنتج التي تعرّف المنتج. ‏‫مجموعات أبعاد المنتج المحتملة الأربع هي: الحجم واللون والنمط والتكوين. تتوفر مجموعات أبعاد المنتجات في Common Data Service باستخدام التعيينات التالية. 

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
WILLSALESPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willsalespricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willpurchasepricesearchuseproductsize
WILLSALESPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willsalespricesearchuseprodconfig
WILLSALESPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willsalespricesearchuseproductcolor
WILLPURCHASEPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willpurchasepricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willpurchpricesearchuseprodconfig
WILLPURCHASEPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willpurchpricesearchuseproductcolor
ISPRODUCTSTYLEACTIVE | >< | msdyn_isproductstyleactive
ISPRODUCTSIZEACTIVE | >< | msdyn_isproductsizeactive
ISPRODUCTCONFIGURATIONACTIVE | >< | msdyn_isproductconfigurationactive
ISPRODUCTCOLORACTIVE | >< | msdyn_isproductcoloractive
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
PRODUCTVARIANTNOMENCLATURENAME | = | msdyn_productvariantnomenclaturename
WILLSALESPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willsalespricesearchuseproductsize

### <a name="product-tracking-dimension-group"></a>مجموعة أبعاد تعقب المنتج

تمثل مجموعة ابعاد تعقب المنتج الطريقة المستخدمة لتتبع المنتج في المخزون. تتوفر هذه في Common Data Service باستخدام التعيينات التالية. 

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
SERIALNUMBERCAPTURINGOPERATION | >< | msdyn_serialnumbercapturingoperation
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISSERIALNUMBERENABLEDFORPRODUCTIONCONSUMPTIONPROCESS | >< | msdyn_issnenabledforpcprocess
ISSERIALNUMBERCONTROLENABLED | >< | msdyn_isserialnumbercontrolenabled
ISSERIALNUMBERENABLEDFORSALESPROCESS | >< | msdyn_isserialnumberenabledforsalesprocess
ISSERIALNUMBERACTIVE | >< | msdyn_isserialnumberactive
ISSALESPRICEBYSERIALNUMBER | >< | msdyn_issalespricebyserialnumber
ISSALESPRICEBYBATCHNUMBER | >< | msdyn_issalespricebybatchnumber
ISPURCHASEPRICEBYSERIALNUMBER | >< | msdyn_ispurchasepricebyserialnumber
ISPURCHASEPRICEBYBATCHNUMBER | >< | msdyn_ispurchasepricebybatchnumber
ISPRIMARYSTOCKINGENABLEDFORSERIALNUMBER | >< | msdyn_isprimarystockingenabledforsn
ISPRIMARYSTOCKINGENABLEDFORBATCHNUMBER | >< | msdyn_isprimarystockingenabledforbn
ISPHYSICALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isphysicalinventoryenabledforsn
ISPHYSICALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isphysicalinventoryenabledforbn
ISFINANCIALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isfinancialinventoryenabledforsn
ISFINANCIALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isfinancialinventoryenabledforbn
ISCOVERAGEPLANENABLEDFORSERIALNUMBER | >< | msdyn_iscoverageplanenabledforserialnumber
ISCOVERAGEPLANENABLEDFORBATCHNUMBER | >< | msdyn_iscoverageplanenabledforbatchnumber
ISBLANKRECEIPTALLOWEDFORSERIALNUMBER | >< | msdyn_isblankreceiptallowedforserialnumber
ISBLANKRECEIPTALLOWEDFORBATCHNUMBER | >< | msdyn_isblankreceiptallowedforbatchnumber
ISBLANKISSUEALLOWEDFORSERIALNUMBER | >< | msdyn_isblankissueallowedforserialnumber
ISBLANKISSUEALLOWEDFORBATCHNUMBER | >< | msdyn_isblankissueallowedforbatchnumber
ISBATCHNUMBERACTIVE | >< | msdyn_isbatchnumberactive
ISINVENTORYOWNERACTIVE | >< | msdyn_isinventoryowneractive

### <a name="product-storage-dimension-group"></a>مجموعة أبعاد تخزين المنتج

تمثل مجموعة أبعاد تخزين المنتج الطريقة المستخدمة لتحديد وضع المنتج في المستودع. تتوفر هذه في Common Data Service باستخدام التعيينات التالية. 

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
WILLSALESPRICESEARCHUSEWAREHOUSE | >< | msdyn_willsalespricesearchusewarehouse
WILLSALESPRICESEARCHUSESITE | >< | msdyn_willsalespricesearchusesite
WILLSALESPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willsalespricesearchuseinventorystatus
WILLPURCHASEPRICESEARCHUSEWAREHOUSE | >< | msdyn_willpurchasepricesearchusewarehouse
WILLPURCHASEPRICESEARCHUSESITE | >< | msdyn_willpurchasepricesearchusesite
WILLPURCHASEPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willpurchpricesearchuseinventstatus
WILLCOVERAGEPLANNINGUSEWAREHOUSE | >< | msdyn_willcoverageplanusewarehouse
WILLCOVERAGEPLANNINGUSELOCATION | >< | msdyn_iscoverageplanenabledforlocation
WILLCOVERAGEPLANNINGUSEINVENTORYSTATUS | >< | msdyn_willcoverageplanuseinventorystatus
AREADVANCEDWAREHOUSEMANAGEMENTPROCESSESENABLED | >< | msdyn_areadvancedwmprocessesenabled
ISWAREHOUSEPRIMARYSTORAGEDIMENSION | >< | msdyn_iswarehouseprimarystoragedimension
ISWAREHOUSEMANDATORY | >< | msdyn_iswarehousemandatory
ISPHYSICALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isphysicalinventoryenabledforwarehouse
ISPHYSICALINVENTORYENABLEDFORLOCATION | >< | msdyn_isphysicalinventoryenabledforlocation
ISLOCATIONACTIVE | >< | msdyn_islocationactive
ISFINANCIALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isfinancialinventoryenabledforwarehouse
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISBLANKRECEIPTALLOWEDFORLOCATION | >< | msdyn_isblankreceiptallowedforlocation
ISBLANKISSUEALLOWEDFORLOCATION | >< | msdyn_isblankissueallowedforlocation

