---
title: رصيد الأجازات
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان رصيد الأجازات في Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab136e9b40de280387dc3c5207a08a6bb357941feb3a8c736d9671f7850f2bf8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782673"
---
# <a name="leave-balance"></a>رصيد الأجازات

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان رصيد الأجازات لـ Dynamics 365 Human Resources.

### <a name="description"></a>الوصف

يوفر هذا الكيان رصيد الإجازة لكل نوع إجازة لموظف معين.

الاسم الفعلي: mshr_essleavebalanceentities.

## <a name="properties"></a>الخصائص

| الخاصية</br>**الاسم الفعلي**</br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **رقم الموظف**</br>mshr_personnelnumber</br>*سلسلة* | للقراءة فقط | رقم الموظف الفريد الخاص بالموظف. |
| **الرصيد الحالي**</br>mshr_balanceavailable</br>*عشري* | للقراءة فقط | الرصيد الحالي للموظف. |
| **النوع**</br>mshr_balanceavailable</br>*سلسلة* | للقراءة فقط | معرف نوع الإجازة. |
| **معدل الاستحقاق**</br>mshr_accrualratedescription</br> | للقراءة فقط | معدل الاستحقاق. |
| **المقدار المنقول الأخير**</br>mshr_lastcarryforwardamount</br>*عشري* | للقراءة فقط | مبلغ الرصيد المحول الأخير. |
| **تم أخذها هذه السنة**</br>mshr_takenthisyear</br>*عشري* | للقراءة فقط | مقدار الإجازة التي أخذت هذا العام. |
| **الإجمالي هذا العام**</br>mshr_totalthisyear</br>*عشري* | للقراءة فقط | المبلغ الإجمالي لهذا العام. |
| **معرف منطقة البيانات**</br>mshr_dataareaid_id</br>*سلسلة* | للقراءة فقط | يحدد الكيان القانوني (الشركة). |
| **الحقل الأساسي**</br>mshr_primaryfield</br>*GUID* | للقراءة فقط</br>النظام منشأ | |
| **معرف نوع الإجازة**</br>_mshr_fk_leavetype_id_value</br>*GUID* | للقراءة فقط</br>المفتاح الخارجي:mshr_essleavetypeentityid لـ mshr_essleavetypeentity entity  | معرف نوع الإجازة |
| **كيان رصيد الأجازات**</br>mshr_essleavebalanceentityid</br>*GUID* | النظام منشأ | قيمة معرف GUID منشأ بواسطة النظام لتعريف الرصيد بشكل فريد. |

## <a name="example-query"></a>مثال الاستعلام

**الطلب**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavebalanceentities?$filter=mshr_personnelnumber eq '000013'
```

**استجابة**

```json
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 67.76,
    "mshr_leavetypeid": "PTO",
    "mshr_accrualratedescription": "6.16 hrs / Semimonthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 67.76,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | PTO",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-0000-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-2703-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 80,
    "mshr_leavetypeid": "Sick",
    "mshr_accrualratedescription": "80.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 80,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Sick",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-ee02-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-3003-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 0,
    "mshr_leavetypeid": "Bereavement",
    "mshr_accrualratedescription": "0.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 0,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Bereavement",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f402-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-4403-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 66.65,
    "mshr_leavetypeid": "Vacation",
    "mshr_accrualratedescription": "13.33 hrs / Monthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 66.65,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Vacation",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f502-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-1009-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>راجع أيضًا

[‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
