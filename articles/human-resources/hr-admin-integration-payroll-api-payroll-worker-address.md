---
title: عنوان عامل كشف الرواتب
description: توفر هذه المقالة التفاصيل ومثال الاستعلام لكيان عنوان عامل في كشف الرواتب في Dynamics 365 Human Resources.
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
ms.openlocfilehash: 683994b24113b8c2017f1bb3c1055e7e0f0eb75e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901107"
---
# <a name="payroll-worker-address"></a>عنوان عامل كشف الرواتب


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة كيان عنوان العامل في كشف الرواتب في Dynamics 365 Human Resources.

الاسم الفعلي: mshr_payrollworkeraddressentity.

### <a name="description"></a>الوصف

يوفر هذا الكيان موقع إقامة الرواتب وموقع عمل الرواتب لموظف محدد.

## <a name="properties"></a>الخصائص

| الخاصية</br>**الاسم الفعلي**</br>**_النوع_** | استخدام | ‏‏الوصف |
| --- | --- | --- |
| **رقم الموظف**</br>mshr_personnelnumber</br>*سلسلة* | للقراءة فقط | رقم الموظف الفريد الخاص بالموظف. |
| **معرف الموقع**</br>mshr_locationidbr>*String* | للقراءة فقط | المعرف الخاص بالعنوان. |
| **أقام في العنوان**</br>mshr_islivedinaddressbr </br> *[مجموعة خيارات mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | للقراءة فقط | قيمة تشير إلى ما إذا كان العنوان هو المكان الذي يقيم فيه الموظف. |
| **عمل في العنوان** </br> mshr_isworkedinaddressbr </br>*[مجموعة خيارات mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | للقراءة فقط | قيمة تشير إلى ما إذا كان العنوان هو المكان الذي يعمل فيه الموظف. |
| **منطقة البلد**</br>mshr_countryregionid</br>*سلسلة* | للقراءة فقط</br>مرجو | البلد أو المنطقة المحددة للعنوان. |
| **الرمز البريدي**</br>mshr_zipcode<br>*سلسلة* | للقراءة فقط | رقم التعريف المحدد للموظف. |
| **الشارع**</br>mshr_street</br>*سلسلة* | للقراءة فقط | الشارع المحدد للعنوان. |
| **المدينة**</br>mshr_city</br>*سلسلة* | للقراءة فقط | المدينة المحددة للعنوان. |
| **الولاية**</br>mshr_state</br>*سلسلة* | للقراءة فقط | الولاية أو المقاطعة المحددة للعنوان. |
| **المقاطعة**</br>mshr_county</br>*سلسلة* | للقراءة فقط | المقاطعة المحددة للعنوان. |
| **صالح من**</br>mshr_postaladdressvalidfrom</br>*الفرق بالتاريخ والوقت* | للقراءة فقط | تاريخ بدء صلاحية العنوان. |
| **صالح حتى**</br>mshr_postaladdressvalidto</br>*الفرق بالتاريخ والوقت* | للقراءة فقط | تاريخ انتهاء صلاحية العنوان. |
| **الحقل الأساسي**</br>mshr_primaryfield</br>*سلسلة* | للقراءة فقط | الحقل الأساسي. |
| **معرف عنوان عامل كشف الرواتب**</br>mshr_payrollworkeraddressentityid</br>*GUID* | النظام منشأ | قيمة معرف فريد عمومي (GUID) يقوم النظام بإنشائه لتعريف العنوان بشكل فريد. |

## <a name="relations"></a>العلاقات

| قيمة الخاصية | الكيان المرتبط | خاصيه التنقل | نوع التجميع |
| --- | --- | --- | --- |
| _mshr_fk_worker_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Worker_id | mshr_FK_PayrollEmployeeEntity_Address |

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
