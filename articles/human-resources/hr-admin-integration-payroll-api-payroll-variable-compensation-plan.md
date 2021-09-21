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
ms.openlocfilehash: c30df23debed9e2ab90745e6ea9d0e6b8a05b6d5
ms.sourcegitcommit: 4d11061f5de0ddba1f968bd5c3fd694a8b104ccc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/26/2021
ms.locfileid: "7429213"
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
| **رقم الموظف**</br>mshr_personnelnumber</br>*سلسلة* | للقراءة فقط | رقم الموظف الفريد الخاص بالموظف.  |
| **تاريخ المكافأة**</br>mshr_awarddate</br>*الفرق بالتاريخ والوقت* | للقراءة فقط | التاريخ الخاص بالمكافأة. |
| **نوع المكافأة**</br>mshr_awardtype</br>*[مجموعة خيارات mshr_HrmCompVarAwardEmplType](hr-admin-integration-payroll-api-award-type.md)* | للقراءة فقط | نوع المكافأة المعرّف لخطة التعويض المتغير. |
| **عملة**</br>mshr_unitcurrencycode</br>*سلسلة* | للقراءة فقط |العملة المحددة لخطة التعويض المتغير.   |
| **معرف خطة التعويض الثابت**</br>mshr_fixedplanid</br>*سلسلة* | للقراءة فقط | خطة التعويض الثابت التي تُستخدم كأساس لحساب المكافأة. |
| **قيمة الوحدة**</br>mshr_awardamount</br>*عشري* | للقراءة فقط | قيمة الوحدة |
| **نوع العملية**</br>mshr_processtype</br>*[مجموعة خيارات mshr_hrmCompProcessType](hr-admin-integration-payroll-api-process-type.md)* | للقراءة فقط | نوع العملية. |
| **نوع خطة التعويض المتغير**</br>سلسلة</br>*mshr_typeid* | للقراءة فقط | نوع خطة التعويض المتغير. |
| **معرف خطة التعويض المتغير**</br>سلسلة</br>*mshr_planid* | للقراءة فقط | المعرف لخطة التعويض المتغير. |
| **عدد الوحدات**</br>عشري</br>*mshr_numberofunits* | للقراءة فقط | عدد وحدات الصنف المكافأة. |
| **الحقل الأساسي**</br>mshr_primaryfield</br>*GUID* | للقراءة فقط</br>منشأ بواسطة النظام. | |
| **كيان خطة التعويض المتغير لكشف الرواتب**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | النظام منشأ | قيمة معرف GUID منشأ بواسطة النظام لتعريف خطة التعويض بشكل فريد. |

## <a name="relations"></a>العلاقات 

|قيمة الخاصية | الكيان المرتبط | خاصيه التنقل | نوع التجميع |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_VariableCompAward |
| _mshr_fk_fixedcomp_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedComp_id | mshr_FK_PayrollFixedCompensationPlanEntity_VariableCompAward |

## <a name="example-query"></a>مثال الاستعلام

**الطلب**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000046'
```

**استجابة**

```json
{
    "mshr_personnelnumber": "000046",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_unitvalue": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_numberofunits": 1500,
    "mshr_primaryfield": "000046 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000666-0000-0000-daff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a4-0000-0000-0d00-005001000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>راجع أيضًا

[‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
