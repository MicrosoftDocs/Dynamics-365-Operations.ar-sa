---
title: وظيفة منصب كشف الرواتب
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان وظيفة منصب كشف الرواتب في Dynamics 365 Human Resources.
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
ms.openlocfilehash: 349479d9e77861b54d879bcfd93f7af0e38cff95
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069822"
---
# <a name="payroll-position-job"></a>وظيفة منصب كشف الرواتب


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان وظيف المنصب في الرواتب لـ Dynamics 365 Human Resources.

### <a name="description"></a>الوصف

يوفر هذا الكيان العلاقة بين المنصب والوظيفة لخطة تعويض ثابت معينة.

الاسم الفعلي: mshr_payrollpositionjobentity.

## <a name="properties"></a>الخصائص

| الخاصية</br>**الاسم الفعلي**</br>**_النوع_** | استخدام | ‏‏الوصف |
| --- | --- | --- |
| **معرف المنصب**</br>mshr_positionid</br>*سلسلة* | للقراءة فقط | معرف المنصب. |
| **صالح من**</br>mshr_validto</br>*الفرق بالتاريخ والوقت* | للقراءة فقط | تاريخ بدء صلاحية علاقة المنصب والوظيفة. |
| **صالح حتى**</br>mshr_validto</br>*الفرق بالتاريخ والوقت* | للقراءة فقط | تاريخ انتهاء صلاحية علاقة المنصب والوظيفة. |
| **معرف الوظيفة**</br>mshr_jobid</br>*سلسلة* | للقراءة فقط | معرف الوظيفة. |
| **الحقل الأساسي**</br>mshr_primaryfield</br>*سلسلة* | النظام منشأ | الحقل الأساسي. |
| **معرف كيان وظيفة المنصب في كشف الرواتب**</br>mshr_payrollpositionjobentityid</br>*Guid* | منشأ بواسطة النظام. | قيمة معرف فريد عمومي (GUID) يقوم النظام بإنشائه لتعريف الوظيفة بشكل فريد. |

## <a name="relations"></a>العلاقات

| قيمة الخاصية | الكيان المرتبط | خاصيه التنقل | نوع التجميع |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | غير قابل للتطبيق |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

## <a name="example-query"></a>مثال الاستعلام

**الطلب**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**استجابة**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>راجع أيضًا

[‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
