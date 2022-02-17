---
title: خطة المزايا للعامل في كشف الرواتب
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان خطة مزايا العامل في كشف الرواتب في Dynamics 365 Human Resources.
author: marcelbf
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1805f7efaf2efc48d5996776f3aa27d75606886f
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068424"
---
# <a name="payroll-worker-benefit-plan"></a>خطة المزايا للعامل في كشف الرواتب


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان خطة مزايا العامل في كشف الرواتب في Dynamics 365 Human Resources.

الاسم الفعلي: mshr_payrollworkerbenefitplanentities.

### <a name="description"></a>الوصف

يوفر هذا الكيان معلومات حول خطة المزايا لعامل معين.

## <a name="properties"></a>الخصائص

| الخاصية</br>**الاسم الفعلي**</br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **رقم الموظف**</br>mshr_personnelnumber</br>*سلسلة* | للقراءة فقط</br>مطلوب | رقم الموظف الفريد الخاص بالموظف. |
| **معرف الكيان القانوني**</br>mshr_legalentityID</br>*سلسلة* | للقراءة فقط | يحدد الكيان القانوني (الشركة). |
| **معرف الفترة**</br>mshr_periodid</br>*سلسلة* | للقراءة فقط | معرف الفترة. |
| **معرف الخطة**</br>mshr_planid</br>*سلسلة* | للقراءة فقط | معرف الخطة. |
| **خيار التغطية**</br>mshr_coverageoptionid</br>*سلسلة* | للقراءة فقط | التعريف الخاص بخيار التغطية. |
| **تاريخ بدء الخصم.**</br>mshr_deductionstartdatetime</br>*الفرق بالتاريخ والوقت* | للقراءة فقط | تاريخ بدء الخصم. |
| **تاريخ انتهاء الخصم**</br>mshr_deductionenddatetime</br>*الفرق بالتاريخ والوقت* | للقراءة فقط | تاريخ انتهاء الخصم. |
| **الحالة**</br>mshr_status</br>*[مجموعة خيارات حالة خطة الموظفين للموظفين](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | للقراءة فقط | حالة خطة المزايا. |
| **صالح من**</br>mshr_validfrom</br>*الفرق بالتاريخ والوقت* | للقراءة فقط | وقت بداية صلاحية هذا السجل. |
| **صالح حتى**</br>mshr_validto</br>*الفرق بالتاريخ والوقت* |  للقراءة فقط | وقت انتهاء صلاحية هذا السجل. |
| **معرف نوع الخطة**</br>mshr_plantypeid</br>*سلسلة* | للقراءة فقط | معرف نوع الخطة. |
| **كود نوع الخطة**</br>mshr_plantypecode</br>*[مجموعة خيارات تغطية نوع خطة الميزة](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | للقراءة فقط | مواصفات نوع الخطة. |
| **عدد فترات الدفع**</br>mshr_payperiod</br>*عدد صحيح* | للقراءة فقط | عدد فترات الدفع التي تمثل عدد المرات التي يقوم بها موفر الميزة أو الموظفين بالدفع. سيتم استخدام هذا المبلغ لحساب مبلغ راتب الميزة السنوي الخاص بالموظف. |
| **مبلغ الموظف**</br>mshr_amountemployee</br>*عشري* | للقراءة فقط | النسبة أو المبلغ لكل موظف. |
| **مبلغ صاحب العمل**</br>mshr_amountemployer</br>*عشري* | للقراءة فقط | النسبة أو المبلغ لكل صاحب عمل. |
| **الحقل الأساسي**</br>mshr_primaryfield</br>*سلسلة* | النظام منشأ | الحقل الأساسي. |
| **قيمة معرف العامل** </br>_mshr_fk_worker_id_value</br>*GUID* | المفتاح الخارجي: mshr_hcmworkerbaseentityid للكيان mshr_hcmworkerbaseentity. | معرف فريد منشأ بواسطة النظام للعامل. |
| **قيمة معرف الفترة**</br> _mshr_fk_period_id_value</br>*GUID* | المفتاح الخارجي: mshr_benefitperiodentityid كيان mshr_benefitperiodentity. | معرف فريد منشأ بواسطة النظام للفترة. |
| **قيمة معرف الخطة**</br> _mshr_fk_plan_id_value</br>*GUID* | المفتاح الخارجي: mshr_benefitplanentityid كيان mshr_benefitplanentity. | معرف فريد منشأ بواسطة النظام للخطة. |
| **قيمة معرف نوع الخطة**</br> _mshr_fk_plantype_id_value</br>*GUID* | المفتاح الخارجي: mshr_benefitplantypeentityid كيان mshr_benefitplantypeentity. | معرف فريد منشأ بواسطة النظام للخطة. |
| **قيمة معرف خيار التغطية**</br> _mshr_fk_coverageoption_id_value</br>*GUID* | المفتاح الخارجي: mshr_benefitcoverageoptionentityid كيان mshr_benefitcoverageoptionentity. | معرف فريد منشأ بواسطة النظام للخطة. |
| **قيمة معرف كيان خطة استحقاق عامل الرواتب**</br> mshr_payrollworkerbenefitplanentityid</br>*GUID* | للقراءة فقط </br> النظام منشأ | معرف فريد منشأ بواسطة النظام للسجل. |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>استعلام مثال لخطة استحقاق عامل الرواتب

**الطلب**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**استجابة**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>راجع أيضًا

[‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
