---
title: عنوان عامل كشف الرواتب
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان عنوان عامل كشف الرواتب في Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1ff65a0518232275f7c5d0b4a70d04f77e4936c5
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314103"
---
# <a name="payroll-worker-address"></a>عنوان عامل كشف الرواتب

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان عنوان عامل كشف الرواتب لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_payrollworkeraddressentity.

### <a name="description"></a>الوصف

يوفر هذا الكيان موقع إقامة الرواتب وموقع عمل الرواتب لموظف محدد.

## <a name="properties"></a>الخصائص

| الخاصية</br>**الاسم الفعلي**</br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **المدينة**</br>mshr_city</br>*سلسلة* | للقراءة فقط</br>مطلوب | المدينة المحددة للعنوان.   |
| **رقم الموظف**</br>mshr_personnelnumber</br>*سلسلة* | للقراءة فقط</br>مطلوب | رقم الموظف الفريد الخاص بالموظف.  |
| **منطقة البلد**</br>mshr_countryregionid</br>*سلسلة* | للقراءة فقط</br>مطلوب | منطقة البلد المحددة للعنوان.  |
| **صالح من**</br>mshr_postaladdressvalidfrom</br>*الفرق بالتاريخ والوقت* | للقراءة فقط </br>مطلوب | تاريخ بدء صلاحية العنوان. |
| **عمل في العنوان** </br> mshr_isworkedinaddressbr </br>*[مجموعة خيارات mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | للقراءة فقط</br>مطلوب | الإشارة إلى ما إذا كان العنوان هو المكان الذي يعمل به الموظف. |
| **المقاطعة**</br>mshr_county</br>*سلسلة* | للقراءة فقط</br>مطلوب | البلد المحدد للعنوان.  |
| **معرف عنوان عامل كشف الرواتب**</br>mshr_payrollworkeraddressentityid</br>*GUID* | مطلوب</br>النظام منشأ | قيمة معرف GUID منشأ بواسطة النظام لتعريف العنوان بشكل فريد.  |
| **الحقل الأساسي**</br>mshr_primaryfield</br>*سلسلة* | للقراءة فقط</br>مطلوب |  |
| **الشارع**</br>mshr_street</br>*سلسلة* | للقراءة فقط</br>مطلوب | الشارع المحدد للعنوان. |
| **صالح حتى**</br>mshr_postaladdressvalidto</br>*الفرق بالتاريخ والوقت* | للقراءة فقط </br>مطلوب | تاريخ انتهاء صلاحية العنوان.  |
| **معرف الموقع**</br>mshr_locationidbr>*String* | للقراءة فقط <br>مطلوب | المعرف الخاص بالعنوان.  |
| **الرمز البريدي**</br>mshr_zipcode<br>*سلسلة* | للقراءة فقط <br>مطلوب |رقم التعريف المحدد للموظف.  |
| **أقام في العنوان**</br>mshr_islivedinaddressbr </br> *[مجموعة خيارات mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | للقراءة فقط</br>مطلوب | الإشارة إلى ما إذا كان العنوان هو المكان الذي يقيم فيه الموظف. |
| **الولاية**</br>mshr_state</br>*سلسلة* | للقراءة فقط</br>مطلوب | الولاية المحددة للعنوان.  |

## <a name="example-query"></a>مثال الاستعلام

**الطلب**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**استجابة**

```json
{
    "mshr_personnelnumber": "000041",
    "mshr_locationid": "000000538",
    "mshr_islivedinaddress": 200000001,
    "mshr_isworkedinaddress": 200000000,
    "mshr_countryregionid": "USA",
    "mshr_zipcode": "99025",
    "mshr_street": "6543 Cypress Ave",
    "mshr_city": "Tacoma",
    "mshr_state": "WA",
    "mshr_county": "KING",
    "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
    "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
    "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
    "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

## <a name="see-also"></a>راجع أيضًا

[‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
