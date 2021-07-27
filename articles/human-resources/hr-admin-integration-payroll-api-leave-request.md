---
title: طلب إجازة
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان طلب أجازة في Dynamics 365 Human Resources.
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
ms.openlocfilehash: b7f5744265dd106f11e6ffe7334873e697a7ea13
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314309"
---
# <a name="leave-request"></a>طلب إجازة

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان طلب أجازة لـ Dynamics 365 Human Resources.

### <a name="description"></a>الوصف

يوفر هذا الكيان معلومات لطلب إجازة.

الاسم الفعلي: mshr_essleaverequestentity.

## <a name="properties"></a>الخصائص

| الخاصية</br>**الاسم الفعلي**</br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف الطلب**</br>mshr_requestid</br>*سلسلة* | للقراءة فقط | معرف الطلب. |
| **معرف نوع الإجازة**</br>mshr_leavetypeid</br>*سلسلة* | للقراءة فقط | معرف نوع الإجازة. |
| **التاريخ**</br>mshr_leavedate</br>*الفرق بالتاريخ والوقت* | للقراءة فقط | تاريخ طلب الإجازة. |
| **المبلغ**</br>mshr_amount</br>*عشري* | للقراءة فقط | مبلغ طلب الإجازة. |
| **نوع نصف اليوم**</br>mshr_halfdaydefinition</br>*مجموعة خيارات mshr_LeaveHalfDayDefinition* | للقراءة فقط | نوع إجازة نصف يوم. |
| **التعليق**</br>mshr_comment</br>*سلسلة* | للقراءة فقط | التعليق الخاص بالطلب. |
| **الحالة**</br>mshr_status</br>*مجموعة خيارات mshr_status* | للقراءة فقط | حالة الطلب. |
| **التاريخ**</br>mshr_requestdate</br>*الفرق بالتاريخ والوقت* | للقراءة فقط | تاريخ الطلب. |
| **رقم الموظف**</br>mshr_personnelnumber</br>*سلسلة* | للقراءة فقط | رقم الموظف الفريد الخاص بالموظف. |
| **معرف رمز السبب**</br>mshr_reasoncodeid</br>*سلسلة* | للقراءة فقط | المعرف لرمز السبب. |
| **معرف منطقة البيانات**</br>mshr_dataareaid</br>*سلسلة* | للقراءة فقط | يحدد الكيان القانوني (الشركة). |
| **الحقل الأساسي**</br>mshr_primaryfield</br>*GUID* | للقراءة فقط</br>النظام منشأ | |
| **كيان نوع الأجازة**</br>mshr_essleaverequestentityid</br>*GUID* | النظام منشأ | قيمة معرف GUID منشأ بواسطة النظام لتعريف طلب الأجازة بشكل فريد. |

## <a name="example-query"></a>مثال الاستعلام

**الطلب**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**استجابة**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>راجع أيضًا

[‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
