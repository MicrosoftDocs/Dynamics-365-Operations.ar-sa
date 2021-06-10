---
title: عنوان الشخص
description: يصف هذا الموضوع كيان عنوان الشخص لـ Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
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
ms.openlocfilehash: 14db209e420770234583add93fa72d086f1b5ea6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053769"
---
# <a name="person-address"></a>عنوان الشخص

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان عنوان الشخص لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmpersonaddressentities

## <a name="description"></a>الوصف

يحتوي هذا الكيان على قائمة بالعناوين البريدية لسجلات المرشحين.

## <a name="json-representation"></a>تمثيل JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان عنوان الشخص**<br>mshr_hcmpersonaddressentityid<br>*سلسلة* | للقراءة فقط<br>مطلوب | معرف فريد منشأ بواسطة النظام لسجل الكيان. |
| **رقم الطرف**<br>mshr_partynumber<br>*سلسلة* | قراءة/كتابة<br>مطلوب | معرف سجل الطرف المرتبط (الشخص). |
| **قيمة معرف الشخص**<br>_mshr_fk_person_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_dirpersonentityid لـ mshr_dirpersonentity | المعرف الفريد المنشأ بواسطة النظام لسجل كيان الطرف (الشخص). |
| **معرف الموقع**<br>mshr_locationid<br>*سلسلة* | قراءة/كتابة<br>مطلوب | معرف الموقع الخاص بسجل العنوان. الإعداد في كيان mshr_logisticspostaladdresslocationcdsentity. |
| **‏‏الوصف**<br>mshr_description<br>*سلسلة* | قراءة/كتابة<br>مطلوب | وصف لعنوان المرشح. |
| **الأدوار**<br>mshr_roles<br>*سلسلة* | قراءة/كتابة<br>مطلوب | الأدوار المعينة لهذا العنوان. يمكن تحديد أكثر من دور واحد. يجب فصل كل دور بفاصلة منقوطة. القيم الصالحة الموجودة في الكيان mshr_logisticslocationroleentity. |
| **الشارع**<br>mshr_street<br>*سلسلة* | قراءة/كتابة<br>اختياري | رقم الشارع. |
| **المدينة**<br>mshr_city<br>*سلسلة* | قراءة/كتابة<br>اختياري | مدينة العنوان. الإعداد في كيان mshr_logisticsaddresscityentity. |
| **الولاية**<br>mshr_state<br>*سلسلة* | قراءة/كتابة<br>اختياري | الولاية المذكورة في العنوان. الإعداد في كيان mshr_logisticsaddressstateentity. |
| **المقاطعة**<br>mshr_county<br>*سلسلة* | قراءة/كتابة<br>اختياري | إقليم العنوان. الإعداد في كيان mshr_logisticsaddresscountyentity. |
| **الرمز البريدي**<br>mshr_zipcode<br>*سلسلة* | قراءة/كتابة<br>اختياري | الرمز البريدي الخاص بالعنوان. الإعداد في كيان mshr_logisticsaddresspostalcodeentity. |
| **معرف البلد المنطقة**<br>mshr_countryregionid<br>*سلسلة* | قراءة/كتابة<br>اختياري | بلد أو منطقة العنوان. |
| **قيمة معرف البلد/المنطقة**<br>_mshr_fk_countriregion_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: mshr_logisticaddresscountryregionentityid لـ mshr_logisticsaddresscountryregionentity | المعرّف الفريد المنشأ بواسطة النظام الخاص بالبلد/المنطقة في العنوان. |
| **رئيسي**<br>mshr_isprimary<br>*مجموعة خيارات mshr_noyes* | قراءة/كتابة<br>مطلوب | يحدد ما إذا كان هذا العنوان هو العنوان الرئيسي لشخص في الدور المحدد. |
| **خاص**<br>mshr_isprivate<br>*مجموعة خيارات mshr_noyes* | قراءة/كتابة<br>مطلوب | يحدد ما إذا كان هذا العنوان عبارة عن عنوان خاص للشخص أم لا. |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | للقراءة فقط<br>مطلوب | حقل يستخدم كمعرف أساسي لسجل الكيان. مجموعة رقم الطرف ومعرف الموقع. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]