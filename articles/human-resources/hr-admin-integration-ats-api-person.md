---
title: الشخص
description: توضح هذه المقالة كيان الشخص لـ Dynamics 365 Human Resources.
author: jaredha
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c8adb2f06d1fcdfef8a42a04c5ebddd246ffc2ae
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887334"
---
# <a name="person"></a>الشخص


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة كيان الشخص لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_dirpersonentity

### <a name="description"></a>الوصف

يوفر هذا الكيان المعلومات الشخصية للفرد المتقدم كمرشح.

## <a name="json-representation"></a>تمثيل JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "String",
    "mshr_addresslocationroles": "String",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان الشخص**<br>mshr_dirpersonentityid<br>*GUID* | للقراءة فقط<br>مطلوب<br>منشأ بواسطة النظام | معرف فريد منشأ بواسطة النظام لسجل الكيان. |
| **رقم الطرف**<br>mshr_partynumber<br>*سلسلة* | للقراءة فقط<br>مطلوب<br>منشأ بواسطة النظام | معرف فريد منشأ بواسطة النظام للشخص.  |
| **الاسم**<br>mshr_name<br>*سلسلة* | للقراءة فقط<br>مطلوب | تمثل قيمة الحقل سلسلة من الاسم الأول والاسم الأوسط وبادئة اسم العائلة واسم العائلة بالترتيب المعرف في حقل **عرض تسلسل الاسم**. |
| **الاسم المستعار**<br>mshr_namealias<br>*سلسلة* | قراءة/كتابة<br>اختياري | الاسم المستعار الذي قد يكون مقدمًا للشخص. |
| **معروف باسم**<br>mshr_knownas<br>*سلسلة* | قراءة/كتابة<br>اختياري | اسم يمكن استخدامه للشخص إذا كان يُعرف عادة باسم آخر. |
| **معرف اللغة**<br>mshr_languageid<br>*سلسلة* | قراءة/كتابة<br>اختياري | معرف اللغة للغة الأساسية للشخص، كما هو محدد في تنسيق ISO 639-1. |
| **دفاتر العناوين**<br>mshr_addressbooks<br>*سلسلة* | قراءة/كتابة<br>اختياري | دفتر العناوين الذي يمكن تعيين الشخص له. يتم سرد دفاتر العناوين التي تم إعدادها للمؤسسة في الكيان mshr_diraddressbooksentity. |
| **يوم الذكرى السنوية**<br>mshr_anniversaryday<br>*Int* | قراءة/كتابة<br>اختياري | يوم تاريخ الذكري السنوية الخاص بالشخص. |
| **شهر الذكرى السنوية**<br>mshr_anniversarymonth<br>*مجموعة خيارات mshr_monthsofyear* | قراءة/كتابة<br>اختياري | شهر تاريخ الذكري السنوية الخاص بالشخص. |
| **سنة الذكرى السنوية**<br>mshr_anniversaryyear<br>*Int* | قراءة/كتابة<br>اختياري | سنة تاريخ الذكري السنوية الخاص بالشخص. |
| **يوم الميلاد**<br>mshr_birthday<br>*Int* | قراءة/كتابة<br>اختياري | يوم تاريخ ميلاد الشخص. |
| **شهر الميلاد**<br>mshr_birthmonth<br>*مجموعة خيارات mshr_monthsofyear* | قراءة/كتابة<br>اختياري | شهر تاريخ ميلاد الشخص. |
| **سنة الميلاد**<br>mshr_birthyear<br>*Int* | قراءة/كتابة<br>اختياري | سنة تاريخ ميلاد الشخص. |
| **أسماء الأطفال**<br>mshr_childrennames<br>*سلسلة* | قراءة/كتابة<br>اختياري | سلسله لأسماء أطفال الشخص. لا توجد تحديد مطلوب. |
| **الجنس**<br>mshr_gender<br>*مجموعة خيارات mshr_hcmpersongender* | قراءة/كتابة<br>اختياري | جنس الشخص. |
| **الهوايات**<br>mshr_hobbies<br>*سلسلة* | قراءة/كتابة<br>اختياري | هوايات الشخص. |
| **الأحرف الأولى**<br>mshr_initials<br>*سلسلة* | قراءة/كتابة<br>اختياري | الأحرف الأولى لاسم الشخص. |
| **الحالة الاجتماعية**<br>mshr_maritalstatus<br>*مجموعة خيارات mshr_hcmpersonmaritalstatus* | قراءة/كتابة<br>اختياري | الحالة الاجتماعية للشخص. |
| **الاسم الأول الصوتي**<br>mshr_phoneticfirstname<br>*سلسلة* | قراءة/كتابة<br>اختياري | النطق الصوتي للاسم الأول للشخص. |
| **اسم العائلة الصوتي**<br>mshr_phoneticlastname<br>*سلسلة* | قراءة/كتابة<br>اختياري | النطق الصوتي لاسم العائلة للشخص. |
| **الاسم الأوسط الصوتي**<br>mshr_phoneticmiddlename<br>*سلسلة* | قراءة/كتابة<br>اختياري | النطق الصوتي لاسم العائلة للشخص. |
| **لاحقة شخصية**<br>mshr_personalsuffix<br>*سلسلة* | قراءة/كتابة<br>اختياري | اللاحقة الشخصية للشخص. القيم الصالحة في الكيان mshr_dirnameaffixentity عندما يكون mshr_type لاحقة (200000001). |
| **اللقب الشخصي**<br>mshr_personaltitle<br>*سلسلة* | قراءة/كتابة<br>اختياري | اللقب الشخصي للشخص. القيم الصالحة في الكيان mshr_dirnameaffixentity عندما يكون mshr_type اللقب (200000000).
| **اللاحقة المهنية**<br>mshr_professionalsuffix<br>*سلسلة* | قراءة/كتابة<br>اختياري | اللاحقة المهنية. |
| **اللقب المهني**<br>mshr_professionaltitle<br>*سلسلة* | قراءة/كتابة<br>اختياري | اللقب المهني. |
| **العنوان الرئيسي الكامل**<br>mshr_fullprimaryaddress<br>*سلسلة* | قراءة/كتابة<br>اختياري | العنوان الرئيسي الكامل للشخص، سلسلة من حقول العنوان الرئيسي. |
| **مدينة العنوان**<br>mshr_addresscity<br>*سلسلة* | قراءة/كتابة<br>اختياري | المدينة الخاصة بالعنوان الرئيسي للشخص. الإعداد في كيان mshr_logisticsaddresscityentity. |
| **منطقة / بلد العنوان**<br>mshr_addresscountryregionid<br>*سلسلة* | قراءة/كتابة<br>اختياري | البلد/المنطقة الخاصة بالعنوان الرئيسي للشخص. القيم الصالحة في الكيان mshr_logisticsaddresscountryregionentity. |
| **رمز ISO لمنطقة / بلد العنوان**<br>mshr_addresscountryregionisocode<br>*سلسلة* | قراءة/كتابة<br>اختياري | رمز ISO لبلد العنوان الرئيسي للشخص. |
| **بلد العنوان**<br>mshr_addresscounty<br>*سلسلة* | قراءة/كتابة<br>اختياري | البلد الخاص بالعنوان الرئيسي للشخص. الإعداد في كيان mshr_logisticsaddresscountyentity. |
| **اسم منطقة العنوان**<br>mshr_addressdistrictname<br>*سلسلة* | قراءة/كتابة<br>اختياري | المنطقة الخاصة بالعنوان الرئيسي للشخص. الإعداد في كيان mshr_logisticsaddressdistrictentity. |
| **خط الطول في العنوان**<br>mshr_addresslatitude<br>*سلسلة* | قراءة/كتابة<br>اختياري | خط الطول بالعنوان الرئيسي للشخص. |
| **معرف موقع العنوان**<br>mshr_addresslocationid<br>*سلسلة* | قراءة/كتابة<br>اختياري | المعرف الفريد لموقع العنوان الرئيسي للشخص. القيم الصالحة في كيان mshr_logisticspostaladdresslocationcdsentity. |
| **أدوار موقع العنوان**<br>mshr_addresslocationroles<br>*سلسلة* | قراءة/كتابة<br>اختياري | دور الموقع الخاص بالعنوان الرئيسي للشخص. الإعداد في كيان mshr_logisticslocationrolecdsentity. |
| **خط العرض للعنوان**<br>mshr_addresslongitude<br>*سلسلة* |  قراءة/كتابة<br>اختياري | خط العرض بالعنوان الرئيسي للشخص. |
| **ولاية العنوان**<br>mshr_addressstate<br>*سلسلة* | قراءة/كتابة<br>اختياري | الولاية الخاصة بالعنوان الرئيسي للشخص. الإعداد في كيان mshr_logisticsaddressstateentity. |
| **عنوان الشارع**<br>mshr_addressstreet<br>*سلسلة* | قراءة/كتابة<br>اختياري | عنوان الشارع في العنوان الرئيسي للشخص. |
| **العنوان صالح من**<br>mshr_addressvalidfrom<br>*التاريخ* | قراءة/كتابة<br>اختياري | تاريخ بداية صلاحية العنوان الأساسي للشخص. |
| **العنوان صالح إلى**<br>mshr_addressvalidto<br>*التاريخ* | قراءة/كتابة<br>اختياري | تاريخ نهاية صلاحية العنوان الأساسي للشخص. |
| **الرمز البريدي للعنوان**<br>mshr_addresszipcode<br>*سلسلة* | قراءة/كتابة<br>اختياري | الرمز البريدي للعنوان الرئيسي للشخص. الإعداد في كيان mshr_logisticsaddresspostalcodeentity. |
| **العنوان خاص**<br>mshr_addressisprivate<br>*مجموعة خيارات mshr_noyes* | قراءة/كتابة<br>اختياري | يحدد ما إذا كان يمكن مشاركة العنوان الرئيسي للشخص مع الآخرين في المؤسسة أم لا. |
| **وصف العنوان**<br>mshr_addressdescription<br>*سلسلة* | قراءة/كتابة<br>اختياري | وصف العنوان الرئيسي للشخص. |
| **البريد الإلكتروني لجهة الاتصال الرئيسية**<br>mshr_primarycontactemail<br>*سلسلة* | قراءة/كتابة<br>اختياري | عنوان البريد الإلكتروني الرئيسي للشخص. |
| **وصف البريد الإلكتروني لجهة الاتصال الرئيسية**<br>mshr_primarycontactemaildescription<br>*سلسلة* | قراءة/كتابة<br>اختياري | وصف مقدم لعنوان البريد الإلكتروني الرئيسي. |
| **البريد الإلكتروني لجهة الاتصال الرئيسية هو IM**<br>mshr_primarycontactemailisim<br>*مجموعة خيارات mshr_noyes* | قراءة/كتابة<br>اختياري | يحدد ما إذا كان عنوان البريد الإلكتروني الرئيسي متوفرًا للرسائل الفورية أم لا. |
| **الغرض من البريد الإلكتروني لجهة الاتصال الرئيسية**<br>mshr_primarycontactemailpurpose<br>*سلسلة* | قراءة/كتابة<br>اختياري | الغرض الخاص بعنوان البريد الإلكتروني الرئيسي. الإعداد في كيان mshr_logisticslocationroleentity. |
| **فاكس جهة الاتصال الرئيسية**<br>mshr_primarycontactfax<br>*سلسلة* | قراءة/كتابة<br>اختياري | رقم الفاكس الرئيسي. |
| **وصف الفاكس لجهة الاتصال الرئيسية**<br>mshr_primarycontactfaxdescription<br>*سلسلة* | قراءة/كتابة<br>اختياري | وصف مقدم لرقم الفاكس الرئيسي. |
| **امتداد الفاكس لجهة الاتصال الرئيسية**<br>mshr_primarycontactfaxextension<br>*سلسلة* | قراءة/كتابة<br>اختياري | الامتداد الخاص برقم الفاكس الرئيسي. |
| **الغرض من فاكس جهة الاتصال الرئيسية**<br>mshr_primarycontactfaxpurpose<br>*سلسلة* | قراءة/كتابة<br>اختياري | الغرض من رقم الفاكس الرئيسي. الإعداد في كيان mshr_logisticslocationroleentity.
| **هاتف جهة الاتصال الرئيسية**<br>mshr_primarycontactphone<br>*سلسلة* | قراءة/كتابة<br>اختياري | رقم الهاتف الرئيسي. |
| **وصف هاتف جهة الاتصال الرئيسية**<br>mshr_primarycontactphonedescription<br>*سلسلة* | قراءة/كتابة<br>اختياري | وصف مقدم لرقم الهاتف الرئيسي. |
| **امتداد الهاتف لجهة الاتصال الرئيسية**<br>mshr_primarycontactphoneextension<br>*سلسلة* | قراءة/كتابة<br>اختياري | الامتداد الخاص برقم الهاتف الرئيسي. |
| **هاتف جهة الاتصال الرئيسية هو هاتف جوال**<br>mshr_primarycontactphoneismobile<br>*مجموعة خيارات mshr_noyes* | قراءة/كتابة<br>اختياري | تحديد ما إذا كان رقم الهاتف الرئيسي هو رقم جوال أم لا. |
| **الغرض من هاتف جهة الاتصال الرئيسية**<br>mshr_primarycontactphonepurpose<br>*سلسلة* | قراءة/كتابة<br>اختياري | الغرض من رقم الهاتف الرئيسي. الإعداد في كيان mshr_logisticslocationroleentity. |
| **تلكس جهة الاتصال الرئيسية**<br>mshr_primarycontacttelex<br>*سلسلة* | قراءة/كتابة<br>اختياري | رقم التلكس الرئيسي. |
| **وصف تلك جهة الاتصال الرئيسية**<br>mshr_primarycontacttelexdescription<br>*سلسلة* | قراءة/كتابة<br>اختياري | وصف مقدم لرقم التلكس الرئيسي للشخص. |
| **الغرض من تلكس جهة الاتصال الرئيسية**<br>mshr_primarycontacttelexpurpose<br>*سلسلة* | قراءة/كتابة<br>اختياري | الغرض الخاص برقم التلكس الرئيسي للشخص. الإعداد في كيان mshr_logisticslocationroleentity. |
| **عنوان URL لجهة الاتصال الرئيسية**<br>mshr_primarycontacturl<br>*سلسلة* | قراءة/كتابة<br>اختياري | عنوان URL الرئيسي. |
| **وصف عنوان URL لجهة الاتصال الرئيسية**<br>mshr_primarycontacturldescription<br>*سلسلة* | قراءة/كتابة<br>اختياري | وصف مقدم لعنوان URL الرئيسي للشخص. |
| **الغرض من عنوان URL لجهة الاتصال الرئيسية**<br>mshr_primarycontacturldescription<br>*سلسلة* | قراءة/كتابة<br>اختياري | الغرض من عنوان URL الرئيسي للشخص. الإعداد في كيان mshr_logisticslocationroleentity. |
| **جهة اتصال Facebook الرئيسية**<br>mshr_primarycontactfacebook<br>*سلسلة* | قراءة/كتابة<br>اختياري | حساب Facebook الرئيسي يتم تحديده بواسطة معرف المستخدم. |
| **وصف Facebook لجهة الاتصال الرئيسية**<br>mshr_primarycontactfacebookdescription<br>*سلسلة* | قراءة/كتابة<br>اختياري | وصف مقدم لحساب Facebook الرئيسي للشخص. |
| **حساب Facebook لجهة الاتصال الرئيسية خاص**<br>mshr_primarycontactfacebookisprivate<br>*مجموعة خيارات mshr_noyes* | قراءة/كتابة<br>اختياري | يحدد ما إذا كان حساب Facebook الرئيسي مرئيًا للمستخدمين الآخرين أم لا. |
| **الغرض من Facebook لجهة الاتصال الرئيسية**<br>mshr_primarycontactfacebookpurpose<br>*سلسلة* | قراءة/كتابة<br>اختياري | الغرض من حساب Facebook الرئيسي للشخص. الإعداد في كيان mshr_logisticslocationroleentity. |
| **حساب LinkedIn لجهة الاتصال الرئيسية**<br>mshr_primarycontactlinkedin<br>*سلسلة* | قراءة/كتابة<br>اختياري | حساب LinkedIn الرئيسي. يتم تحديده بواسطة اسم المستخدم. |
| **وصف LinkedIn لجهة الاتصال الرئيسية**<br>mshr_primarycontactlinkedindescription<br>*سلسلة* | قراءة/كتابة<br>اختياري | وصف مقدم لحساب LinkedIn الرئيسي للشخص. |
| **حساب LinkedIn لجهة الاتصال الرئيسية خاص**<br>mshr_primarycontactlinkedinisprivate<br>*مجموعة خيارات mshr_noyes* | قراءة/كتابة<br>اختياري | يحدد ما إذا كان يمكن مشاركة معلومات حساب LinkedIn الرئيسي للشخص مع المستخدمين الآخرين أم لا. |
| **غرض حساب LinkedIn لجهة الاتصال الرئيسية**<br>mshr_primarycontactlinkedinpurpose<br>*سلسلة* | قراءة/كتابة<br>اختياري | الغرض من حساب LinkedIn الرئيسي للشخص. الإعداد في كيان mshr_logisticslocationroleentity. |
| **حساب Twitter لجهة الاتصال الرئيسية**<br>mshr_primarycontacttwitter<br>*سلسلة* | قراءة/كتابة<br>اختياري | حساب Twitter الرئيسي الخاص بالشخص. يتم تحديده بواسطة @username. |
| **وصف Twitter لجهة الاتصال الرئيسية**<br>mshr_primarycontacttwitterdescription<br>*سلسلة* | قراءة/كتابة<br>اختياري | وصف مقدم لحساب Twitter الرئيسي للشخص. |
| **حساب Twitter لجهة الاتصال الرئيسية خاص**<br>mshr_primarycontacttwitterisprivate<br>*مجموعة خيارات mshr_noyes* | قراءة/كتابة<br>اختياري | يحدد ما إذا كان يمكن مشاركة معلومات حساب Twitter الرئيسي للشخص مع المستخدمين الآخرين أم لا. |
| **غرض حساب Twitter لجهة الاتصال الرئيسية**<br>mshr_primarycontacttwitterpurpose<br>*سلسلة* | قراءة/كتابة<br>اختياري | الغرض من حساب Twitter الرئيسي للشخص. الإعداد في كيان mshr_logisticslocationroleentity. |
| **نوع الطرف**<br>mshr_partytype<br>*سلسلة* | قراءة/كتابة<br>اختياري | نوع الطرف للشخص. سيكون دائما **الشخص** للمرشحين. |
| **تسلسل الاسم المعروض**<br>mshr_namesequencedisplayas<br>*سلسلة* | قراءة/كتابة<br>اختياري | التسلسل الذي يتم فيه وصل خصائص اسم الشخص لتشكيل قيمة خاصية الاسم (mshr_name). |
| **الاسم الأول**<br>mshr_firstname<br>*سلسلة* | قراءة/كتابة<br>مطلوب | الاسم الأول للشخص. |
| **الاسم الأوسط**<br>mshr_middlename<br>*سلسلة* | قراءة/كتابة<br>اختياري | الاسم الأوسط للشخص. |
| **بادئة اسم العائلة**<br>mshr_lastnameprefix<br>*سلسلة* | قراءة/كتابة<br>اختياري | بادئه اسم العائلة للشخص. |
| **اسم العائلة**<br>mshr_lastname<br>*سلسلة* | قراءة/كتابة<br>اختياري | اسم العائلة للشخص. |
| **معرف الموقع الإلكتروني**<br>mshr_electroniclocationid<br>*سلسلة* | قراءة/كتابة<br>اختياري | معرف الموقع الإلكتروني الخاص بالشخص. |
| **المنطقة الزمنية للعنوان**<br>mshr_addresstimezone<br>*Int* | قراءة/كتابة<br>اختياري | المنطقة الزمنية للعنوان الرئيسي للشخص. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
