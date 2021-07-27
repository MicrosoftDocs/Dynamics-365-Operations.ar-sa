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
ms.openlocfilehash: 842c459acd8b5e1a8b6074243b3afa18dc6a13c5
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314227"
---
# <a name="payroll-position-job"></a>وظيفة منصب كشف الرواتب

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان وظيف المنصب في الرواتب لـ Dynamics 365 Human Resources.

### <a name="description"></a>الوصف

يوفر هذا الكيان العلاقة بين المنصب والوظيفة لخطة تعويض ثابت معينة.

الاسم الفعلي: mshr_payrollpositionjobentity.

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف الوظيفة**<br>mshr_jobid<br>*سلسلة* | للقراءة فقط<br>مطلوب |معرف الوظيفة. |
| **صالح من**<br>mshr_validto<br>*الفرق بالتاريخ والوقت* | للقراءة فقط <br>مطلوب | تاريخ بدء صلاحية علاقة المنصب والوظيفة. |
| **صالح حتى**<br>mshr_validto<br>*الفرق بالتاريخ والوقت* | للقراءة فقط <br>مطلوب | تاريخ انتهاء صلاحية علاقة المنصب والوظيفة.  |
| **معرف المنصب**<br>mshr_positionid<br>*سلسلة* | للقراءة فقط<br>مطلوب | معرف المنصب. |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | مطلوب<br>النظام منشأ |  |
| **قيمة معرف وظيفة المنصب**<br>_mshr_fk_positionjob_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>مفتاح خارجي:mshr_PayrollPositionJobEntity لـ mshr_payrollpositionjobentity |معرف الوظيفة المقترنة بالمنصب.|
| **قيمة معرف خطة التعويض الثابت**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>مفتاح خارجي: mshr_FixedCompPlan_id لـ mshr_payrollfixedcompensationplanentity  | معرف خطة التعويض الثابت المقترنة بالمنصب. |
| **معرف كيان وظيفة المنصب في كشف الرواتب**<br>mshr_payrollpositionjobentityid<br>*Guid* | مطلوب<br>منشأ بواسطة النظام. | قيمة معرف GUID منشأ بواسطة النظام لتعريف الوظيفة بشكل فريد.  |

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
