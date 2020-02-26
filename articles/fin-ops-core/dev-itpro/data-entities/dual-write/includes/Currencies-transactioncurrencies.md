## <a name="currencies-to-transactioncurrencies"></a>العملات إلى transactioncurrencies

يقوم هذا القالب بمزامنة البيانات بين تطبيقات Finance and Operations وCommon Data Service.

عامل تصفية المصدر: ((CURRENCYCODE != "999"))

حقل Finance and Operations | نوع التعيين | حقل Dynamics 365 الآخر | القيمة الافتراضية
---|---|---|---
CURRENCYCODE | = | isocurrencycode | 
الاسم | = | currencyname | 
الرمز | = | currencysymbol | 
لا‬‬ شيء | >> | exchangerate | 1
