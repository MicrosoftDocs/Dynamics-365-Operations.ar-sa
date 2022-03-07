---
title: تفاصيل كشف الرواتب للمناصب
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لتفاصيل كشف الرواتب لكيان المناصب في Dynamics 365 Human Resources.
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
ms.openlocfilehash: 76131b6cc7ee58d4a095da4ac56cd97124e42587
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559329"
---
# <a name="payroll-position"></a>منصب كشف الرواتب

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان المناصب في الرواتب لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_payrollpositionentity.

### <a name="description"></a>الوصف

يوفر هذا الكيان معلومات متعلقة بالمنصب لموظف محدد.

الاسم الفعلي: mshr_payrollpositionentity.

## <a name="properties"></a>الخصائص

| الخاصية</br>**الاسم الفعلي**</br>**_النوع_** | استخدام | ‏‏الوصف |
| --- | --- | --- |
| **معرف المنصب**</br>mshr_positionid</br>*سلسلة* | للقراءة فقط | معرف المنصب. |
| **معرف دورة الدفع**</br>mshr_paycycleid</br>*سلسلة* | للقراءة فقط | دورة الدفع المحددة على المنصب. |
| **الساعات العادية السنوية**</br>annualregularhours</br>*عشري* | للقراءة فقط | ساعات العمل الدورية السنوية المحددة على المنصب. |
| **الدفع بواسطة الكيان القانوني**</br>paidbylegalentity</br>*سلسلة* | للقراءة فقط | الكيان القانوني المحدد على المنصب والمسؤول عن إصدار الدفع. |
| **صالح حتى**</br>validto</br>*الفرق بالتاريخ والوقت* | للقراءة فقط | تاريخ انتهاء صلاحيه تفاصيل المنصب. |
| **صالح من**</br>validfrom</br>*الفرق بالتاريخ والوقت* | للقراءة فقط | تاريخ بدء صلاحيه تفاصيل المنصب. |
| **الحقل الأساسي**</br>mshr_primaryfield</br>*سلسلة* | النظام منشأ | الحقل الأساسي. |
| **معرف كيان تفاصيل المنصب في كشف الرواتب**</br>payrollpositiondetailsentityid</br>*Guid* | مرجو</br>منشأ بواسطة النظام. | قيمة معرف فريد عمومي (GUID) يقوم النظام بإنشائه لتعريف المنصب بشكل فريد. |

## <a name="relations"></a>العلاقات

| قيمة الخاصية | الكيان المرتبط | خاصيه التنقل | نوع التجميع |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | غير قابل للتطبيق |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | غير قابل للتطبيق |

## <a name="example-query"></a>مثال الاستعلام

**الطلب**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**استجابة**

```json
{
    "mshr_positionid": "000276",
    "mshr_paycycleid": "w",
    "mshr_annualregularhours": 3000,
    "mshr_paidbylegalentity": "USMF",
    "mshr_validfrom": "2021-03-14T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_primaryfield": "000276 | 3/14/2021",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>راجع أيضًا

[‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
