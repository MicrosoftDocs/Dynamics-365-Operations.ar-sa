## <a name="cds-contacts-v2-to-contacts"></a>جهات اتصال CDS الإصدار V2 إلى جهات الاتصال

يقوم هذا القالب بمزامنة البيانات بين تطبيقات Finance and Operations وCommon Data Service.

عامل التصفية المصدر: (AssociatedContactType = 1)

عامل التصفية المصدر المعكوس: msdyn_contactforvendor eq true وmsdyn_sellable eq false وmsdyn_contactpersonid ne ''

حقل Finance and Operations | نوع التعيين | حقل Dynamics 365 الآخر | القيمة الافتراضية
---|---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn_partynumber | 
ASSOCIATEDCONTACTTYPE | << | لا‬‬ شيء | المورد
FIRSTNAME | = | firstname | 
MIDDLENAME | = | middlename | 
LASTNAME | = | lastname | 
ASSOCIATEDCONTACTNUMBER | = | msdyn_vendorcontactid.msdyn_vendoraccountnumber | 
PRIMARYADDRESSCITY | = | address1_city | 
PRIMARYADDRESSCOUNTRYREGIONID | = | address1_country | 
PRIMARYADDRESSCOUNTYID | = | address1_county | 
PRIMARYFAXNUMBER | = | الفاكس | 
PRIMARYADDRESSSTATEID | = | address1_stateorprovince | 
PRIMARYADDRESSSTREET | = | address1_line1 | 
PRIMARYADDRESSZIPCODE | = | address1_postalcode | 
PRIMARYPHONENUMBER | = | telephone1 | 
PRIMARYEMAILADDRESS | = | emailaddress1 | 
EMPLOYMENTDEPARTMENT | = | القسم | 
ملاحظات | = | الوصف | 
الجنس | >< | gendercode | 
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid | 
PRIMARYURL | = | websiteurl | 
MARITALSTATUS | >< | familystatuscode | 
ISRECEIVINGDIRECTMAIL | >< | donotemail | 
EMPLOYMENTPROFESSION | = | jobtitle | 
SPOUSENAME | = | spousesname | 
لا‬‬ شيء | >> | msdyn_contactforvendor | صحيح
CONTACTPERSONID | = | msdyn_contactpersonid | 
