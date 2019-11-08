---
title: أصل المورّد المتكامل
description: يوضح هذا الموضوع تكامل بيانات المورّد بين تطبيقات Finance and Operations وCommon Data Service.
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
ms.openlocfilehash: d33625b94e7611a256c389a6de4692ae8f4ff2a7
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572462"
---
# <a name="integrated-vendor-master"></a>أصل المورّد المتكامل

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

يشير المصطلح *المورّد* إلى مؤسسه مورّد أو مالك وحيد يعتبر جزءًا من عملية سلسلة التوريد ويوفر السلع للشركات. وعلى الرغم من أن *المورّد* عبارة عن مفهوم تم إنشاؤه في تطبيقات Finance and Operations، فإن مفهوم المورّد غير موجود في تطبيقات Dynamics 365 الأخرى. بدلا من ذلك، تقوم بعض الشركات بإجراء تحميل زائد على لكيان الحساب بتخزين معلومات العملاء ومعلومات المورّدين على حد سواء. وتستخدم شركات أخرى مفهومًا مخصصًا للمورّد. يدعم تكامل Common Data Service هذين التصميمين. وبالتالي، يمكنك تمكين أي واحد من التصميمين، بحسب سيناريو شركتك.

تتيح لك امكانيه تكامل بيانات المورّد بين تطبيقات Finance and Operations وتطبيقات Dynamics 365 الأخرى بإجراء إدارة متعددة للبيانات. بغض النظر عن مصدر بيانات المورّدين، فهي تتكامل في الخلفية عبر حدود التطبيق واختلافات البنية التحتية. 

### <a name="vendor-data-flow"></a>تدفق بيانات المورّد

إذا أردت استخدام تطبيقات Dynamics 365 الأخرى لإدارة المورّدين، وأردت عزل معلومات المورّد عن معلومات العميل، فيمكنك استخدام تصميم المورّد الجديد.

![تدفق بيانات المورّد](media/dual-write-vendor-data-flow.png)

إذا أردت استخدام تطبيقات Dynamics 365 الأخرى لإدارة المورّدين، وأردت متابعة استخدام كيان الحساب لتخزين معلومات المورّدين، فيمكنك استخدام تصميم المورّد الموسع الجديد. في هذا التصميم، يتم تخزين معلومات المورّد الموسعة، مثل مجموعة المورّد ومعلومات ملف تعريف ترحيل المورّد، في تفاصيل المورّد‬.

![تدفق بيانات المورّد الموسّعة](media/dual-write-vendor-detail.jpg)

تشبه معلومات اتصال المورّد معلومات اتصال العميل. في الخلفية، يتم تخزين معلومات جهة الاتصال واستردادها من الكيانات نفسها،.

## <a name="templates"></a>القوالب

تتضمن بيانات المورّد كافة المعلومات المتعلقة بالمورّد، مثل مجموعة المورّدين والعناوين ومعلومات الاتصال وملف تعريف الدفع وملف تعريف الفاتورة. تعمل مجموعة من مخططات الكيانات معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.

تطبيقات Finance and Operations  | تطبيقات Dynamics 365 الأخرى
------------------------|---------------------------------
المورّد V2               | الحساب
المورّد V2               | Msdyn\_vendors
جهات اتصال CDS V2         | جهة الاتصال
مجموعات الموردين           | Msdyn\_vendorgroups
طريقة دفع المورّد   | Msdyn\_vendorpaymentmethods
جدول الدفع        | Msdyn\_paymentschedules
جدول الدفع        | Msdyn\_paymentschedulelines
يوم الدفع CDS         | Msdyn\_paymentdays
بنود يوم الدفع CDS   | Msdyn\_paymentdaylines
شروط الدفع        | Msdyn\_paymentterms
ملحقات الاسم            | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="vendor-v2-and-account"></a>المورّد V2 والحساب 

بإمكان الشركات التي تستخدم كيان الحساب لتخزين معلومات المورّد متابعة استخدامها بالطريقة نفسها. ويمكنها أيضًا الاستفادة من وظيفة المورّد الصريحة التي تأتي بسبب تكامل تطبيقات Finance and Operations.

## <a name="vendor-v2-and-msdyn_vendors"></a>المورّد V2 وMsdyn\_vendors

بإمكان الشركات التي تستخدم حلاً مخصصًا للمورّدين الاستفادة من مفهوم المورّد المبتكر الذي تم تقديمه في Common Data Service بسبب تكامل تطبيقات Finance and Operations. 

<!-- ![vendor mappings](media/dual-write-vendors-1.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-2.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-3.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
VENDORACCOUNTNUMBER | = | msdyn\_vendoraccountnumber
VENDORGROUPID | = | msdyn\_vendorgroupid.msdyn\_vendorgroup
VENDORORGANIZATIONNAME | = | msdyn\_name
VENDORPARTYTYPE | \>\< | msdyn\_isperson
PERSONFIRSTNAME | = | msdyn\_firstname
PERSONLASTNAME | = | msdyn\_lastname
CREDITLIMIT | = | msdyn\_vendorcreditlimit
ISFOREIGNENTITY | \>\< | msdyn\_isforeignentity
ISONETIMEVENDOR | \>\< | msdyn\_isonetimevendor
ADDRESSBUILDINGCOMPLIMENT | = | msdyn\_addressbuildingcompliment
PERSONCHILDRENNAMES | = | msdyn\_childrennames
ADDRESSCITY | = | msdyn\_addresscity
ADDRESSCOUNTRYREGIONID | = | msdyn\_addresscountryregionid
ADDRESSCOUNTRYREGIONISOCODE | = | msdyn\_addresscountryregionisocode
ADDRESSCOUNTYID | = | msdyn\_addresscountyid
CREDITRATING | = | msdyn\_creditrating
ADDRESSDESCRIPTION | = | msdyn\_addressdescription
ADDRESSDISTRICTNAME | = | msdyn\_addressdistrictname
DUNSNUMBER | = | msdyn\_dunsnumber
ETHNICORIGINID | = | msdyn\_ethnicorigin
FORMATTEDPRIMARYADDRESS | = | msdyn\_formattedprimaryaddress
PERSONHOBBIES | = | msdyn\_hobbies
PERSONINITIALS | = | msdyn\_initials
LANGUAGEID | = | msdyn\_languageid
PERSONLASTNAMEPREFIX | = | msdyn\_lastnameprefix
PERSONMIDDLENAME | = | msdyn\_middlename
ORGANIZATIONNUMBER | = | msdyn\_organizationnumber
OURACCOUNTNUMBER | = | msdyn\_ourvendoraccountnumber
PAYMENTID | = | msdyn\_paymentid
PERSONPHONETICFIRSTNAME | = | msdyn\_phoneticfirstname
PERSONPHONETICMIDDLENAME | = | msdyn\_phoneticmiddlename
PERSONPHONETICLASTNAME | = | msdyn\_phoneticlastname
ORGANIZATIONPHONETICNAME | = | msdyn\_organizationphoneticname
ADDRESSPOSTBOX | = | msdyn\_addresspostbox
PRIMARYURL | = | msdyn\_primarycontacturl
PRIMARYEMAILADDRESS | = | msdyn\_primaryemailaddress
PRIMARYEMAILADDRESSDESCRIPTION | = | msdyn\_primaryemailaddressdescription
PRIMARYFACEBOOK | = | msdyn\_primaryfacebook
PRIMARYFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYFAXNUMBER | = | msdyn\_primaryfaxnumber
PRIMARYFAXNUMBERDESCRIPTION | = | msdyn\_primaryfaxnumberdescription
PRIMARYFAXNUMBEREXTENSION | = | msdyn\_primaryfaxnumberextension
PRIMARYLINKEDIN | = | msdyn\_primarylinkedin
PRIMARYLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescription
PRIMARYPHONENUMBER | = | msdyn\_pimaryphonenumber
PRIMARYPHONENUMBERDESCRIPTION | = | msdyn\_primaryphonenumberdescription
PRIMARYPHONENUMBEREXTENSION | = | msdyn\_primaryphonenumberextension
PRIMARYTELEX | = | msdyn\_primarytelex
PRIMARYTELEXDESCRIPTION | = | msdyn\_primarytelexdescription
PRIMARYTWITTER | = | msdyn\_primarytwitter
PRIMARYTWITTERDESCRIPTION | = | msdyn\_primarytwitterdescription
PRIMARYURLDESCRIPTION | = | msdyn\_primaryurldescription
PERSONPROFESSIONALSUFFIX | = | msdyn\_professionalsuffix
PERSONPROFESSIONALTITLE | = | msdyn\_professionatitle
ADDRESSSTATEID | = | msdyn\_addressstateid
ADDRESSSTREET | = | msdyn\_addressstreet
ADDRESSSTREETNUMBER | = | msdyn\_addressstreetnumber
VENDORKNOWNASNAME | = | msdyn\_vendorknownasname
ADDRESSZIPCODE | = | msdyn\_addresszipcode
DEFAULTPAYMENTDAYNAME | = | msdyn\_defaultpaymentdayname.msdyn\_name
DEFAULTPAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
DEFAULTPAYMENTTERMSNAME | = | msdyn\_paymentterms.msdyn\_name
HASONLYTAKENBIDS | \>\< | msdyn\_hasonlytakenbids
ISMINORITYOWNED | \>\< | msdyn\_isminorityowned
ISVENDORLOCALLYOWNED | \>\< | msdyn\_isvendorlocallyowned
ISSERVICEVETERANOWNED | \>\< | msdyn\_isserviceveteranowned
ISOWNERDISABLED | \>\< | msdyn\_ownerisdisabled
ISWOMANOWNER | \>\< | msdyn\_womanowner
PERSONANNIVERSARYDAY | = | msdyn\_personanniversaryday
PERSONANNIVERSARYYEAR | = | msdyn\_anniversaryyear
PERSONBIRTHDAY | = | msdyn\_birthday
PERSONBIRTHYEAR | = | msdyn\_birthyear
ORGANIZATIONEMPLOYEEAMOUNT | = | msdyn\_numberofemployees
VENDORHOLDRELEASEDATE | = | msdyn\_vendoronholdreleasedate
VENDORPARTYNUMBER | = | msdyn\_vendorpartynumber
ADDRESSLOCATIONID | = | msdyn\_addresslocationid
PERSONANNIVERSARYMONTH | = | msdyn\_vendorpersonanniversarymonth
PERSONBIRTHMONTH | = | msdyn\_vendorpersonbirthmonth
PERSONMARITALSTATUS | \>\< | msdyn\_maritalstatus
ADDRESSLATITUDE | \>\> | msdyn\_addresslatitude
ADDRESSLONGITUDE | \>\> | msdyn\_addresslongitude
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
CURRENCYCODE | = | msdyn\_currencycode.isocurrencycode
ISVENDORLOCATEDINHUBZONE | \>\< | msdyn\_isvendorlocatedinhubzone
DEFAULTVENDORPAYMENTMETHODNAME | = | msdyn\_vendorpaymentmethod.msdyn\_name
INVOICEVENDORACCOUNTNUMBER | = | msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber
PERSONGENDER | \>\< | msdyn\_gender
AREPRICESINCLUDINGSALESTAX | \>\< | msdyn\_priceincludessalestax
SALESTAXGROUPCODE | = | msdyn\_taxgroup.msdyn\_name
VENDORPRICETOLERANCEGROUPID | = | msdyn\_pricetolerancegroup.msdyn\_groupid

## <a name="contacts"></a>جهات الاتصال

يقوم هذا القالب بمزامنة جميع معلومات جهات الاتصال الرئيسية والثانوية والثلاثية لكل من العملاء والمورّدين بين تطبيقات Finance and Operations وتطبيقات Dynamics 365 الأخرى. للحصول على تفاصيل خريطة الكيان، راجع [أصل العميل المتكامل](dual-write-customer.md#contacts).

## <a name="vendor-groups"></a>مجموعات المورّدين

يقوم هذا القالب بمزامنة معلومات مجموعة موردين بين تطبيقات Finance and Operations وتطبيقات Dynamics 365 الأخرى.

<!-- ![vendor groups mappings](media/dual-write-vendor-groups.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
DEFAULTPAYMENTTERMNAME | = | msdyn\_paymentterms.msdyn\_name
DESCRIPTION | = | msdyn\_description
VENDORGROUPID | = | msdyn\_vendorgroup
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymentpermname.msdyn\_name

### <a name="vendor-payment-method"></a>طريقة دفع المورّد

يقوم هذا القالب بمزامنة معلومات طرق دفع المورّد بين Finance and Operations وتطبيقات Dynamics 365 الأخرى.

<!-- ![vendor payment method mappings](media/dual-write-vendor-payment-method.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
الاسم | = | msdyn\_name
الوصف | = | msdyn\_description
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
ALLOWPAYMENTCOPIES | \>\< | msdyn\_allowpaymentcopies
PAYMENTTYPE | \>\< | msdyn\_paymenttype
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
ACCOUNTTYPE | \>\< | msdyn\_accounttype
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingposting
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_postdatedcheckclearingposting
PROMISSORYNOTEDRAFTTYPE | \>\< | msdyn\_promissorynotedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

