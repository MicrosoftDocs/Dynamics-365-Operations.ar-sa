## <a name="fiscal-calendar-year-integration-entity-to-msdyn_fiscalcalendaryears"></a>كيان تكامل سنة التقويم المالي إلى msdyn_fiscalcalendaryears

يقوم هذا القالب بمزامنة البيانات بين تطبيقات Finance and Operations وCommon Data Service.

حقل Finance and Operations | نوع التعيين | حقل Dynamics 365 الآخر | القيمة الافتراضية
---|---|---|---
FISCALCALENDAR_CALENDARID | = | msdyn_fiscalcalendarname | 
الاسم | = | msdyn_name | 
STARTDATE | = | msdyn_startdate | 
ENDDATE | = | msdyn_enddate | 
FISCALCALENDAR_CALENDARID | = | msdyn_calendar.msdyn_calendar | 
