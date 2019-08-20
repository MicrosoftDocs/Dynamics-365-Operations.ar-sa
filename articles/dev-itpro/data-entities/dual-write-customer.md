---
title: أصل العميل المتكامل
description: يوضح هذا الموضوع تكامل بيانات العميل بين Finance and Operations وCommon Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.openlocfilehash: a8030d9d1f1f3636a679d334afddad0f573a824e
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789146"
---
## <a name="integrated-customer-master"></a>أصل العميل المتكامل

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

من المعتاد أن تتم عادة إدارة سجلات العملاء في أكثر من تطبيق واحد. على سبيل المثال، بإمكان نشاط المبيعات إحضار سجلات العملاء عبر تطبيق Microsoft Dynamics 365 for Sales، وبإمكان مبيعات التجزئة والتجارة الإلكترونية إحضار سجلات العملاء عبر تطبيق Dynamics 365 for Finance and Operations. بغض النظر عن مصدر سجلات العملاء، فهي تتكامل في الخلفية عبر حدود التطبيق واختلافات البنية التحتية. تساعد إدارة العملاء المتكامل على التعامل مع سيناريوهات إدارة متعددة وتوفر طريقة عرض شاملة للعميل في مجموعة تطبيقات Dynamics 365.

## <a name="customer-data-flow"></a>تدفق بيانات العميل

إن *العميل* عبارة عن مفهوم محدد بطريقة جيدة في كل من Finance and Operations وCommon Data Service. ولذلك، فإن تكامل بيانات العميل ينطوي فقط على مواءمة مفهوم العميل بين Finance and Operations وCommon Data Service. يبين الرسم التوضيحي التالي تدفق بيانات العميل.

![تدفق بيانات العميل](media/dual-write-customer-data-flow.png)

يمكن تصنيف العملاء على نطاق واسع في نوعين: العملاء التجاريين/المؤسسيين والمستهلكين/المستخدمين النهائيين. يتم تخزين هذين النوعين من العملاء والتعامل معهم بطريقة مختلفة في Finance and Operations وCommon Data Service.

في Finance and Operations، تتم إدارة العملاء التجاريين/المؤسسيين والمستهلكين/المستخدمين النهائيين في جدول واحد يسمى **CustTable** (CustomerCustomerV3Entity)، ويتم تصنيفهم استنادًا إلى سمة **النوع**. (إذا تم تعيين **النوع** إلى **مؤسسة**، فسيكون العميل تجاريًا/مؤسسيًا، وإذا تم تعيين **النوع** إلى **شخص**، فسيكون العميل مستهلكًا/مستخدمًا نهائيًا.) يتم التعامل مع معلومات جهة الاتصال الرئيسية عبر الكيان SMMContactPersonEntity.

في Common Data Service، تتم إدارة العملاء التجاريين/المؤسسيين في كيان الحساب، ويتم تعريفهم كعملاء عند تعيين سمة **RelationshipType** إلى **عميل**. يتم تمثيل المستهلكين/المستخدمين النهائيين وشخص جهة الاتصال بواسطة كيان جهة الاتصال. للفصل بشكل واضح بين المستهلك/المستخدم النهائي وشخص جهة الاتصال، يتضمن كيان **جهة الاتصال** علامة منطقية تسمى **قابل للبيع**. عندما تكون قيمة **قابل للبيع** **صواب**، تكون جهة الاتصال عبارة عن عميل مستهلك/مستخدم نهائي، ولا يمكن إنشاء الأوامر وعروض الأسعار لجهة الاتصال هذه. عندما تكون قيمة **قابل للبيع** **خطأ**، تكون جهة الاتصال مجرد جهة اتصال رئيسية للعميل.

عندما تشارك جهة اتصال غير قابلة للبيع في عملية عرض أسعار أو أمر، يتم تعيين قيمة **قابل للبيع** إلى **صواب** لوضع علامة على جهة الاتصال كجهة اتصال قابلة للبيع. جهة الاتصال التي أصبح جهة اتصال قابلة للبيع تبقى جهة اتصال قابلة للبيع.

## <a name="templates"></a>القوالب

تتضمن بيانات العميل كافة المعلومات المتعلقة بالعميل، مثل مجموعة العملاء والعناوين ومعلومات الاتصال وملف تعريف الدفع وملف تعريف الفاتورة وحالة الولاء. تعمل مجموعة من مخططات الكيانات معًا أثناء تفاعل بيانات العميل، كما هو موضح في الجدول التالي.

Finance and Operations    | تطبيق Customer Engagement
--------------------------|---------------------------------
العميل V3               | الحساب
العميل V3               | جهة الاتصال
جهات اتصال CDS V2           | جهة الاتصال
مجموعات العملاء           | Msdyn\_customergroups
طريقة دفع العميل   | Msdyn\_customerpaymentmethods
بطاقة الولاء              | Msdyn\_loyaltycards
جدول الدفع          | Msdyn\_paymentschedules
جدول الدفع          | Msdyn\_paymentschedulelines
يوم الدفع CDS           | Msdyn\_paymentdays
بنود يوم الدفع CDS     | Msdyn\_paymentdaylines
شروط الدفع          | Msdyn\_paymentterms
ملحقات الاسم              | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="customer-v3-to-account"></a>العميل V3 إلى الحساب

يقوم هذا القالب بمزامنة المعلومات الرئيسية للعميل للعملاء التجاريين والمؤسسين بين Finance and Operations وCommon Data Service.

<!-- ![](media/dual-write-account-1.png) -->

<!-- ![](media/dual-write-account-2.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
CUSTOMERACCOUNT | = | accountnumber
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
CREDITLIMIT | = | creditlimit
DELIVERYADDRESSCITY | = | address1\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
DELIVERYADDRESSCOUNTY | = | address1\_county
DELIVERYADDRESSLATITUDE | \> | address1\_latitude
DELIVERYADDRESSLONGITUDE | \> | address1\_longitude
DELIVERYADDRESSZIPCODE | = | address1\_postalcode
ORGANIZATIONNAME | = | name
ORGANIZATIONNUMBEROFEMPLOYEES | = | numberofemployees
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTTWITTER | = | primarytwitterid
PRIMARYCONTACTURL | = | websiteurl
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | description
CREDITLIMITISMANDATORY | \>\< | msdyn\_creditlimitismandatory
CREDITRATING | = | msdyn\_creditrating
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
INVOICEACCOUNT | = | msdyn\_billingaccount.accountnumber
INVOICEADDRESS | \>\< | msdyn\_invoiceaddress
ISONETIMECUSTOMER | \>\< | msdyn\_onetimecustomer
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PAYMENTDAY | = | msdyn\_paymentday.msdyn\_name
PAYMENTMETHOD | = | msdyn\_customerpaymentmethod.msdyn\_name
PAYMENTSCHEDULE | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTTERMS | = | msdyn\_paymentterm.msdyn\_name
PAYMENTTERMSBASEDAYS | = | msdyn\_paymenttermsbasedays
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
PRIMARYCONTACTLINKEDIN | = | msdyn\_primarylinkedinid
TAXEXEMPTNUMBER | = | msdyn\_taxexemptnumber
VENDORACCOUNT | = | msdyn\_vendor.msdyn\_vendoraccountnumber
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
LANGUAGEID | \<\< | بلا
DELIVERYADDRESSSTREET | = | address1\_line1
DELIVERYADDRESSSTATE | = | address1\_stateorprovince
بلا | \>\> | address1\_addresstypecode
بلا | \>\> | customertypecode
PARTYTYPE | \<\< | بلا
PARTYNUMBER | = | msdyn\_partynumber

## <a name="customer-v3-to-contact"></a>العميل V3 إلى جهة اتصال

يقوم هذا القالب بمزامنة البيانات الرئيسية للعميل للعملاء المستهلكين والمستخدمين النهائيين بين Finance and Operations وCustomer Engagement.

<!-- ![](media/dual-write-contact-1.png) -->
<!-- ![](media/dual-write-contact-2.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
بلا | \>\> | msdyn\_sellable
PARTYTYPE | \<\< | بلا
PARTYNUMBER | = | msdyn\_partynumber
CUSTOMERACCOUNT | = | msdyn\_contactpersonid
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
PERSONFIRSTNAME | = | firstname
PERSONLASTNAME | = | lastname
PERSONMIDDLENAME | = | middlename
PERSONPROFESSIONALTITLE | = | jobtitle
PERSONGENDER | \>\< | gendercode
PERSONMARITALSTATUS | \>\< | familystatuscode
LANGUAGEID | \<\< | بلا
ADDRESSCITY | = | address1\_city
ADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
ADDRESSCOUNTY | = | address1\_county
ADDRESSLATITUDE | \> | address1\_latitude
ADDRESSLONGITUDE | \> | address1\_longitude
ADDRESSLOCATIONROLES | \<\< | بلا
ADDRESSSTATE | = | address1\_stateorprovince
ADDRESSSTREET | = | address1\_line1
ADDRESSZIPCODE | = | address1\_postalcode
ADDRESSPOSTBOX | = | address1\_postofficebox
بلا | \>\> | address1\_addresstypecode
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
بلا | \>\> | address2\_addresstypecode
DELIVERYADDRESSCITY | = | address3\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address3\_country
DELIVERYADDRESSCOUNTY | = | address3\_county
DELIVERYADDRESSLATITUDE | \> | address3\_latitude
DELIVERYADDRESSLONGITUDE | \>\> | address3\_longitude
DELIVERYADDRESSSTATE | = | address3\_stateorprovince
DELIVERYADDRESSSTREET | = | address3\_line1
DELIVERYADDRESSZIPCODE | = | address3\_postalcode
بلا | \>\> | address3\_addresstypecode
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTLINKEDIN | = | msdyn\_primaryinkedinid
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTER | = | msdyn\_primarytwitterid
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURL | = | websiteurl
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | description

## <a name="contacts"></a>جهات الاتصال

يقوم هذا القالب بمزامنة جميع معلومات جهات الاتصال الرئيسية والثانوية والثلاثية لكل من العملاء والمورّدين بين Finance and Operations وCustomer Engagement.

<!-- ![](media/dual-write-contacts.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn\_partynumber
ASSOCIATEDCONTACTTYPE | \<\< | بلا
FIRSTNAME | = | firstname
MIDDLENAME | = | middlename
LASTNAME | = | lastname
ASSOCIATEDCONTACTNUMBER | = | msdyn\_vendorcontactid.msdyn\_vendoraccountnumber
PRIMARYADDRESSCITY | = | address1\_city
PRIMARYADDRESSCOUNTRYREGIONID | = | address1\_country
PRIMARYADDRESSCOUNTYID | = | address1\_county
PRIMARYFAXNUMBER | = | fax
PRIMARYADDRESSSTATEID | = | address1\_stateorprovince
PRIMARYADDRESSSTREET | = | address1\_line1
PRIMARYADDRESSZIPCODE | = | address1\_postalcode
PRIMARYPHONENUMBER | = | telephone1
PRIMARYEMAILADDRESS | = | emailaddress1
EMPLOYMENTDEPARTMENT | = | department
NOTES | = | الوصف
GENDER | \>\< | gendercode
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid
PRIMARYURL | = | websiteurl
MARITALSTATUS | \>\< | familystatuscode
ISRECEIVINGDIRECTMAIL | \>\< | donotemail
EMPLOYMENTPROFESSION | = | jobtitle
SPOUSENAME | = | spousesname
بلا | \>\> | msdyn\_contactforvendor
بلا | \>\> | msdyn\_contactpersonid

## <a name="customer-groups"></a>مجموعات العملاء

يقوم هذا القالب بمزامنة معلومات مجموعة عملاء العميل بين Finance and Operations وCustomer Engagement.

<!-- ![](media/dual-write-customer-groups.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
CUSTOMERGROUPID | = | msdyn\_groupid
DESCRIPTION | = | msdyn\_description
ISSALESTAXINCLUDEDINPRICE | \>\< | msdyn\_issalestaxincludedinprice
PAYMENTTERMID | = | msdyn\_paymenttermid.msdyn\_name
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymenttermname.msdyn\_name

## <a name="customer-payment-methods"></a>طرق دفع العميل

يقوم هذا القالب بمزامنة معلومات طرق دفع العميل بين Finance and Operations وCustomer Engagement.

<!-- ![](media/dual-write-customer-payment-methods.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
الاسم | = | msdyn\_name
ACCOUNTTYPE | \>\< | msdyn\_accounttype
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingpostingenabled
ISSEPA | \>\< | msdyn\_issepa
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
DESCRIPTION | = | msdyn\_description
PAYMENTTYPE | \>\< | msdyn\_paymenttype
CREATEANDDRAWBILLOFEXCHANGEDURINGINVOICEPOSTING | \>\< | msdyn\_invoiceupdate
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_enablepostdatescheckclearingposting
BILLOFEXCHANGEDRAFTTYPE | \>\< | msdyn\_billofexchangedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

## <a name="loyalty-cards"></a>بطاقات الولاء

يقوم هذا القالب بمزامنة معلومات بطاقة الولاء الخاصة بالعميل بين Finance and Operations وCustomer Engagement.

<!-- ![](media/dual-write-loyalty-cards.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
CARDNUMBER | = | msdyn\_cardnumber
CARDTENDERTYPE | \>\< | msdyn\_cardtendertype
PARTYNUMBER | = | msdyn\_partynumber
REPLACEMENTCARDNUMBER | \> | msdyn\_replacementcardnumber
OMOPERATINGUNITNUMBER | = | msdyn\_operatingunitnumber
LOYALTYENROLLMENTDATE | = | msdyn\_enrollmentdate

## <a name="payment-schedules"></a>جداول الدفع

يقوم هذا القالب بمزامنة البيانات المرجعية لجدول الدفع لكل من العملاء والمورّدين بين Finance and Operations وCustomer Engagement.

<!-- ![](media/dual-write-payment-schedules.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
الاسم | = | msdyn\_name
DESCRIPTION | = | msdyn\_description
ALLOCATIONMETHOD | \>\< | msdyn\_allocationmethod
PAYMENTFREQUENCYUNITS | \>\< | msdyn\_paymentfrequencyunit
PAYMENTFREQUENCY | = | msdyn\_paymentfrequency
NUMBEROFPAYMENTS | = | msdyn\_numberofpayments
FIXEDPAYMENTAMOUNT | = | msdyn\_fixedpaymentamount
MINIMUMPAYMENTAMOUNT | = | msdyn\_minimumpaymentamount
SALESTAXALLOCATIONMETHOD | \>\< | msdyn\_salestaxallocationmethod
NOTES | = | msdyn\_note

## <a name="payment-schedule-lines"></a>بنود جدول الدفع

يقوم هذا القالب بمزامنة البيانات المرجعية لبنود جدول الدفع لكل من العملاء والمورّدين بين Finance and Operations وCustomer Engagement.

<!-- ![](media/dual-write-payment-schedule-lines.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTSCHEDULENAME | \> | msdyn\_name
LINENUMBER | = | msdyn\_linenumber
PERIODSAFTERDUEDATE | = | msdyn\_periodsafterduedate
PERCENTORAMOUNT | \>\< | msdyn\_percentoramount
PERCENTORAMOUNTVALUE | = | msdyn\_percentoramountvalue

## <a name="payment-days"></a>أيام الدفع

يقوم هذا القالب بمزامنة البيانات المرجعية لأيام الدفع لكل من العملاء والمورّدين بين Finance and Operations وCustomer Engagement.

<!-- ![](media/dual-write-payment-days.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
الاسم | = | msdyn\_name
DESCRIPTION | = | msdyn\_description

## <a name="payment-day-lines"></a>بنود أيام الدفع

يقوم هذا القالب بمزامنة البيانات المرجعية لبنود أيام الدفع لكل من العملاء والمورّدين بين Finance and Operations وCustomer Engagement.

<!-- ![](media/dual-write-payment-day-lines.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
CDSINTEGRATIONKEY | = | Msdyn\_paymentdaylines
FREQUENCY | \>\< | msdyn\_frequency
DAYOFWEEK | \>\< | msdyn\_dayofweek
DAYOFMONTH | = | msdyn\_dayofmonth
الاسم | = | msdyn\_paymentday.msdyn\_name

## <a name="payment-terms"></a>شروط الدفع

يقوم هذا القالب بمزامنة البيانات المرجعية لشروط الدفع لكل من العملاء والمورّدين بين Finance and Operations وCustomer Engagement.

<!-- ![](media/dual-write-payment-terms.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
DESCRIPTION | = | msdyn\_description
الاسم | = | msdyn\_name
NUMBEROFMONTHS | = | msdyn\_numberofmonth
CUTOFFDAYOFMONTH | = | msdyn\_cutoffdayofmonth
ISCASHPAYMENT | \>\< | msdyn\_iscashpayment
NUMBEROFDAYS | = | msdyn\_days
ISCERTIFIEDCOMPANYCHECK | \>\< | msdyn\_iscertifiedcompanycheck
ISDEFAULTPAYMENTTERM | \>\< | msdyn\_isdefaultpaymentterm
CREDITCARDPAYMENTTYPE | \>\< | msdyn\_creditcardpaymenttype
CREDITCARDCREDITCHECKTYPE | \>\< | msdyn\_creditcardcreditchecktype
PAYMENTDAYNAME | = | msdyn\_paymentdayname.msdyn\_name
PAYMENTMETHODTYPE | \>\< | msdyn\_paymentmethodtype
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedulename.msdyn\_name

## <a name="name-affixes"></a>ملحقات الاسم

يقوم هذا القالب بمزامنة البيانات المرجعية لملحقات الاسم لكل من العملاء والمورّدين بين Finance and Operations وCustomer Engagement.

<!-- ![](media/dual-write-name-affixes.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
AFFIX | = | msdyn\_affix
النوع | \>\< | msdyn\_affixtype
DESCRIPTION | = | msdyn\_description
