---
title: خطة التعويض الثابتة لكشف الرواتب
description: توفر هذه المقالة التفاصيل ومثال الاستعلام لكيان خطة التعويض الثابت في كشف الرواتب في Dynamics 365 Human Resources.
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: 83fa8aeb38cc44191242cf029022939cefb22cb8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909835"
---
# <a name="payroll-fixed-compensation-plan"></a>خطة التعويض الثابتة لكشف الرواتب


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة كيان خطة التعويض الثابت لكشف الرواتب في Dynamics 365 Human Resources.

### <a name="description"></a>الوصف

يوفر هذا الكيان خطة التعويض الثابت المعينة لمنصب معين لموظف.

الاسم الفعلي: mshr_payrollfixedcompensationplanentity.

## <a name="properties"></a>الخصائص

| الخاصية</br>**الاسم الفعلي**</br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف الخطة**</br>mshr_planid</br>*سلسلة* | للقراءة فقط | تحدد خطة التعويض.  |
| **رقم الموظف**</br>mshr_personnelnumber</br>*سلسلة* | للقراءة فقط | رقم الموظف الفريد الخاص بالموظف. |
| **معدل الدفع**</br>mshr_payrate</br>*عشري* | للقراءة فقط | معدل الدفع المحدد في خطة التعويض الثابت. |
| **معرف المنصب**</br>mshr_positionid</br>*سلسلة* | للقراءة فقط | معرف المنصب المرتبط بالموظف وتسجيل خطة التعويض الثابت. |
| **صالح من**</br>mshr_validfrom</br>*الفرق بالتاريخ والوقت* |  للقراءة فقط | تاريخ بدء صلاحية التعويض الثابت للموظف.  |
| **صالح حتى**</br>mshr_validto</br>*الفرق بالتاريخ والوقت* | للقراءة فقط | تاريخ انتهاء صلاحية التعويض الثابت للموظف. |
| **تكرار الدفع**</br>mshr_payfrequency</br>*سلسلة* | للقراءة فقط | معرف [تكرار دفع التعويض](hr-admin-integration-payroll-api-compensation-pay-frequency.md) لمعدل الدفع المحدد. |
| **عملة**</br>mshr_currency</br>*سلسلة* | للقراءة فقط | العملة المحددة لخطة التعويض الثابت. |
| **كيان خطة التعويض الثابتة لكشف الرواتب**</br>mshr_payrollfixedcompensationplanentityid</br>*GUID* | النظام منشأ | قيمة معرف GUID منشأ بواسطة النظام لتعريف خطة التعويض بشكل فريد. |

## <a name="relations"></a>العلاقات

|قيمة الخاصية | الكيان المرتبط | خاصيه التنقل | نوع التجميع |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_FixedCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_value | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

## <a name="example-query"></a>مثال الاستعلام

**الطلب**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**استجابة**

```json
{
    "mshr_planid": "GradeC",
    "mshr_personnelnumber": "000041",
    "mshr_payrate": 75200,
    "mshr_positionid": "000276",
    "mshr_validfrom": "2011-04-05T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_payfrequency": "Annual",
    "mshr_currency": "USD",
    "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": null
}
```

## <a name="see-also"></a>راجع أيضًا

[‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
