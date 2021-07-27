---
title: خطة التعويض المتغير لكشف الرواتب
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان خطة التعويض المتغير في كشف الرواتب في Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5dc096c08ed808f577c8cdc96ca84000a0b80679
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314311"
---
# <a name="payroll-variable-compensation-plan"></a>خطة التعويض المتغير لكشف الرواتب

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان خطة التعويض المتغير للرواتب في Dynamics 365 Human Resources.

### <a name="description"></a>الوصف

يوفر هذا الكيان خطة التعويض المتغير المعينة لمنصب معين لموظف.

الاسم الفعلي: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>الخصائص

| الخاصية</br>**الاسم الفعلي**</br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **رقم الموظف**</br>mshr_personnelnumber</br>*سلسلة* | للقراءة فقط</br>مطلوب |رقم الموظف الفريد الخاص بالموظف.  |
| **تاريخ المكافأة**</br>mshr_awarddate</br>*الفرق بالتاريخ والوقت* | للقراءة فقط</br>مطلوب | التاريخ الخاص بالمكافأة. |
| **نوع المكافأة**</br>mshr_awardtype</br>*[مجموعة خيارات mshr_HrmCompVarAwardEmplType](hr-admin-integration-payroll-api-award-type.md)* | للقراءة فقط</br>مطلوب | نوع المكافأة المعرّف لخطة التعويض المتغير. |
| **عملة**</br>mshr_unitcurrencycode</br>*سلسلة* | للقراءة فقط </br>مطلوب |العملة المحددة لخطة التعويض المتغير.   |
| **معرف خطة التعويض الثابت**</br>mshr_fixedplanid</br>*سلسلة* | للقراءة فقط | خطة التعويض الثابت التي تُستخدم كأساس لحساب المكافأة. |
| **قيمة الوحدة**</br>mshr_awardamount</br>*عشري* | للقراءة فقط | قيمة الوحدة |
| **نوع العملية**</br>mshr_processtype</br>*[مجموعة خيارات mshr_hrmCompProcessType](hr-admin-integration-payroll-api-process-type.md)* | للقراءة فقط | نوع العملية. |
| **نوع خطة التعويض المتغير**</br>سلسلة</br>*mshr_typeid* | للقراءة فقط | نوع خطة التعويض المتغير. |
| **معرف خطة التعويض المتغير**</br>سلسلة</br>*mshr_planid* | للقراءة فقط | المعرف لخطة التعويض المتغير. |
| **الحقل الأساسي**</br>mshr_primaryfield</br>*GUID* | للقراءة فقط</br>منشأ بواسطة النظام. | |
| **معرف الموظف**</br>mshr_fk_employee_id_value</br>*GUID* | للقراءة فقط</br>مطلوب</br>مفتاح خارجي:mshr_Employee_id لـ mshr_payrollemployeeentity entity  | معرف الموظف. |
| **كيان خطة التعويض المتغير لكشف الرواتب**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | مطلوب</br>النظام منشأ | قيمة معرف GUID منشأ بواسطة النظام لتعريف خطة التعويض بشكل فريد. |


## <a name="example-query"></a>مثال الاستعلام

**الطلب**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000001'
```

**استجابة**

```json
{
    "mshr_personnelnumber": "000001",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_awardamount": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_primaryfield": "000001 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000655-0000-0000-adff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a1-0000-0000-adff-004105000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>راجع أيضًا

[‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
