## <a name="customers-v3-to-contacts"></a>العملاء V3 إلى جهات الاتصال

يقوم هذا القالب بمزامنة البيانات بين تطبيقات Finance and Operations وCommon Data Service.

عامل تصفية المصدر: ((PartyType == "Person"))

عامل تصفية المصدر المعكوس: msdyn_sellable eq true وmsdyn_contactpersonid ne ''

حقل Finance and Operations | نوع التعيين | حقل Dynamics 365 الآخر | القيمة الافتراضية
---|---|---|---
لا‬‬ شيء | >> | msdyn_sellable | صحيح
PARTYTYPE | << | لا‬‬ شيء | الشخص
PARTYNUMBER | = | msdyn_partynumber | 
CUSTOMERACCOUNT | = | msdyn_contactpersonid | 
CUSTOMERGROUPID | = | msdyn_customergroupid.msdyn_groupid | 
PERSONFIRSTNAME | = | firstname | 
PERSONLASTNAME | = | lastname | 
PERSONMIDDLENAME | = | middlename | 
PERSONPROFESSIONALTITLE | = | jobtitle | 
PERSONGENDER | >< | gendercode | 
PERSONMARITALSTATUS | >< | familystatuscode | 
LANGUAGEID | << | لا‬‬ شيء | ar
ADDRESSCITY | = | address1_city | 
ADDRESSCOUNTRYREGIONISOCODE | = | address1_country | 
ADDRESSCOUNTY | = | address1_county | 
ADDRESSLATITUDE | > | address1_latitude | 
ADDRESSLONGITUDE | > | address1_longitude | 
ADDRESSLOCATIONROLES | << | لا‬‬ شيء | العمل
ADDRESSSTATE | = | address1_stateorprovince | 
ADDRESSSTREET | = | address1_line1 | 
ADDRESSZIPCODE | = | address1_postalcode | 
ADDRESSPOSTBOX | = | address1_postofficebox | 
لا‬‬ شيء | >> | address1_addresstypecode | 3
INVOICEADDRESSCITY | = | address2_city | 
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2_country | 
INVOICEADDRESSCOUNTY | = | address2_county | 
INVOICEADDRESSLATITUDE | > | address2_latitude | 
INVOICEADDRESSLONGITUDE | > | address2_longitude | 
INVOICEADDRESSSTATE | = | address2_stateorprovince | 
INVOICEADDRESSSTREET | = | address2_line1 | 
INVOICEADDRESSZIPCODE | = | address2_postalcode | 
DELIVERYADDRESSCITY | = | address3_city | 
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address3_country | 
DELIVERYADDRESSCOUNTY | = | address3_county | 
DELIVERYADDRESSLATITUDE | > | address3_latitude | 
DELIVERYADDRESSLONGITUDE | >> | address3_longitude | 
DELIVERYADDRESSSTATE | = | address3_stateorprovince | 
DELIVERYADDRESSSTREET | = | address3_line1 | 
DELIVERYADDRESSZIPCODE | = | address3_postalcode | 
PRIMARYCONTACTEMAIL | = | emailaddress1 | 
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn_emailaddress1description | 
PRIMARYCONTACTFAX | = | الفاكس | 
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn_faxdescription | 
PRIMARYCONTACTFAXEXTENSION | = | msdyn_faxextension | 
IDENTIFICATIONNUMBER | = | msdyn_identificationnumber | 
PARTYCOUNTRY | = | msdyn_partycountry | 
PARTYSTATE | = | msdyn_partystateprovince | 
PRIMARYCONTACTFACEBOOK | = | msdyn_primaryfacebookid | 
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn_primaryfacebookdescription | 
PRIMARYCONTACTLINKEDIN | = | msdyn_primaryinkedinid | 
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn_primarylinkedindescrption | 
PRIMARYCONTACTPHONE | = | telephone1 | 
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn_telephone1description | 
PRIMARYCONTACTPHONEEXTENSION | = | msdyn_telephone1extension | 
PRIMARYCONTACTTWITTER | = | msdyn_primarytwitterid | 
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn_primarytwitteriddescription | 
PRIMARYCONTACTURL | = | websiteurl | 
PRIMARYCONTACTURLDESCRIPTION | = | msdyn_websiteurldescription | 
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode | 
SALESMEMO | = | الوصف | 
