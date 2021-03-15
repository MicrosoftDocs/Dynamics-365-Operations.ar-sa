---
title: موقع طلب التعيين
description: يصف هذا الموضوع كيان موقع طلب التعيين لـ Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fa153b1cfcbb70294ed6da3618c83396df04f8db
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125223"
---
# <a name="recruiting-request-location"></a>موقع طلب التعيين

يصف هذا الموضوع كيان موقع طلب التعيين لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>الوصف

قائمة بالمواقع التي تم تعريفها كمواقع حيث سيعمل بها الموظفون المعينون عند التوظيف. وهذه المواقع يتم إنشاؤها عبر الكيانات القانونية.

### <a name="json-representation"></a>تمثيل JSON

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف الموقع**<br>mshr_locationid<br>*سلسلة* | الكتابة مرة واحدة<br>مطلوب | معرف فريد منشأ بواسطة النظام وقابل للقراءة من المستخدم لموقع التعيين. |
| **موقع طلب التعيين**<br>mshr_recruitingrequestlocationid<br>*سلسلة* | الكتابة مرة واحدة<br>مطلوب | المعرف الفريد المحدد بواسطة المستخدم لموقع التعيين. |
| **معرف كيان موقع طلب التعيين**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | للقراءة فقط<br>مطلوب | معرف فريد منشأ بواسطة النظام لسجل موقع طلب التعيين. |
| **‏‏الوصف**<br>mshr_description<br>*سلسلة* | قراءة/كتابة<br>مطلوب | وصف الموقع. |
| **معرف البلد/المنطقة**<br>mshr_countryregionid<br>*سلسلة* | للقراءة فقط<br>اختياري | يحدد البلد أو المنطقة التي هى موطن المرشح. |
| **قيمة معرف البلد/المنطقة**<br>_mshr_fk_countriregion_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: mshr_logisticaddresscountryregionentityid لـ mshr_logisticsaddresscountryregionentity | المعرّف الفريد المنشأ بواسطة النظام الخاص بالبلد/المنطقة في العنوان. |
| **ZipCode**<br>mshr_zipcode<br>*سلسلة* | للقراءة فقط<br>اختياري | الرمز البريدي |
| **الشارع**<br>mshr_street<br>*سلسلة* | للقراءة فقط<br>اختياري | عنوان الشارع. |
| **المدينة**<br>mshr_city<br>*سلسلة* | للقراءة فقط<br>اختياري | المدينة. |
| **الولاية**<br>mshr_state<br>*سلسلة* | للقراءة فقط<br>اختياري | الولاية أو المقاطعة. |
| **المقاطعة**<br>mshr_county<br>*سلسلة* | للقراءة فقط<br>اختياري | المقاطعة. |
| **الهاتف**<br>mshr_telephone<br>*سلسلة* | قراءة/كتابة<br>اختياري | رقم الهاتف الخاص بالموقع. |
| **البريد الإلكتروني**<br>mshr_email<br>*سلسلة* | قراءة/كتابة<br>اختياري | عنوان البريد الإلكتروني. |
| **InternetAddress**<br>mshr_internetaddress<br>*سلسلة* | قراءة/كتابة<br>اختياري | عنوان URL لموقع الويب للموقع. |
| **معرف منطقة البيانات**<br>mshr_dataareaid<br>*سلسلة* | قراءة/كتابة<br>اختياري | يحدد الكيان القانوني (الشركة). |
| **قيمة معرف منطقة البيانات**<br>_mshr_dataareaid_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: cdm_companyid للكيان cdm_company | قيمة GUID تم إنشاؤها بواسطة النظام لتعرف الكيان القانوني (الشركة). |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال لاستعلام عن طلب تعيين](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]