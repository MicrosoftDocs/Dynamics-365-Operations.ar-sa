## <a name="payment-day-lines-cds-v2-to-msdyn_paymentdaylines"></a>CDS لبنود يوم الدفع V2 إلى msdyn_paymentdaylines

يقوم هذا القالب بمزامنة البيانات بين تطبيقات Finance and Operations وCommon Data Service.

حقل Finance and Operations | نوع التعيين | حقل Dynamics 365 الآخر | القيمة الافتراضية
---|---|---|---
الاسم | = | msdyn_paymentday.msdyn_name | 
LINENUMBER | = | msdyn_linenumber | 
التكرار | >< | msdyn_frequency | 
DAYOFWEEK | >< | msdyn_dayofweek | 
DAYOFMONTH | = | msdyn_dayofmonth | 
