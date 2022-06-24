---
title: نوع الإجازة
description: توفر هذه المقالة التفاصيل ومثال الاستعلام لكيان نوع الإجازة في Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6e7905989df92e943b86f86194c87dcb2a7b1446
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893775"
---
# <a name="leave-type"></a>نوع الإجازة


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة كيان نوع الإجازة لـ Dynamics 365 Human Resources.

### <a name="description"></a>‏‏الوصف‬

يوفر هذا الكيان معلومات لنوع إجازة محدد.

الاسم الفعلي: mshr_essleavetypeentity.

## <a name="properties"></a>الخصائص

| الخاصية</br>**الاسم الفعلي**</br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف نوع الإجازة**</br>mshr_leavetypeid</br>*سلسلة* | للقراءة فقط | معرف نوع الإجازة. |
| **‏‏الوصف**</br>mshr_description</br>*سلسلة* | للقراءة فقط | وصف نوع الأجازة. |
| **فئة**</br>mshr_category</br>*مجموعة خيارات mshr_LeaveTypeCategory* | للقراءة فقط | فئة نوع الإجازة. |
| **رمز السبب مطلوب**</br>mshr_isreasoncoderequired</br>*مجموعة خيارات mshr_NoYes* | للقراءة فقط | يحدد ما إذا كان رمز السبب مطلوبا لنوع الإجازة أم لا. |
| **وحدة الأجازة**</br>mshr_leaveamountunit</br>*مجموعة خيارات mshr_LeaveAmountUnit* | للقراءة فقط | الوحدة لنوع الإجازة هذا. |
| **تمكين نصف يوم**</br>mshr_enablehalfdaydefinition</br>*مجموعة خيارات mshr_NoYes* | تحديد ما إذا كان نصف يوم ممكناً لنوع الإجازة أم لا. |
| **معرف منطقة البيانات**</br>mshr_dataareaid_id</br>*سلسلة* | للقراءة فقط | يحدد الكيان القانوني (الشركة). |
| **كيان نوع الأجازة**</br>mshr_essleavetypeentityid</br>*GUID* | النظام منشأ | قيمة معرف GUID منشأ بواسطة النظام لتعريف نوع الأجازة بشكل فريد. |

## <a name="example-query"></a>مثال الاستعلام

**الطلب**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**استجابة**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>راجع أيضًا

[‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
