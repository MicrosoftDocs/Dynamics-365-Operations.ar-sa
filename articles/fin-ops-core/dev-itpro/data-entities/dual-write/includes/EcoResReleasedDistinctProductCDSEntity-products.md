## <a name="cds-released-distinct-products-to-products"></a>منتجات مميزة صادرة من CDS إلى المنتجات

يقوم هذا القالب بمزامنة البيانات بين تطبيقات Finance and Operations وCommon Data Service.

حقل Finance and Operations | نوع التعيين | حقل Dynamics 365 الآخر | القيمة الافتراضية
---|---|---|---
PRODUCTNUMBER | >> | msdyn_productnumber | 
PRODUCTNAME | >> | الاسم | 
PRODUCTDESCRIPTION | >> | الوصف | 
ITEMNUMBER | >> | msdyn_itemnumber | 
CURRENCYCODE | >> | transactioncurrencyid.isocurrencycode | 
SALESUNITSYMBOL | >> | defaultuomid.msdyn_symbol | 
SALESPRICE | >> | سعر | 
UNITCOST | >> | currentcost | 
PRODUCTTYPE | >> | producttypecode | 
SALESUNITDECIMALPRECISION | >> | quantitydecimal | 0
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight | 
PRODUCTCOLORID | >> | msdyn_productcolor.msdyn_productcolorname | 
PRODUCTCONFIGURATIONID | >> | msdyn_productconfiguration.msdyn_productconfiguration | 
PRODUCTSIZEID | >> | msdyn_productsize.msdyn_productsize | 
PRODUCTSTYLEID | >> | msdyn_productstyle.msdyn_productstyle | 
